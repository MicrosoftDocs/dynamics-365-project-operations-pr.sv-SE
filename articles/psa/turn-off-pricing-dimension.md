---
title: Inaktivera en prissättningsdimension
description: I det här ämnet visas hur du ställer in prissättningsdimensioner i Project Service-lösningen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281860"
---
# <a name="turn-off-a-pricing-dimension"></a>Inaktivera en prissättningsdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Du kan behöva granska och uppdatera din prissättningsstrategi med några års intervall. Alla uppdateringar du gör kanske kräver att du stänger av en befintlig prissättningsdimension och skapar en ny. Du kan till exempel ha tidigare prissättning via **Roll**, men nu har du bestämt dig för att få priset via **Arbetserfarenhet**. Detta kan medföra att du måste stänga **Roll** som en prissättningsdimension och skapa **arbetserfarenhet** som en ny prissättningsdimension. 

Inaktivera en prissättningsmodell, oavsett om den är slut eller anpassad kan göras genom att ange fälten **Gäller för kostnad** och **Gäller för försäljning** i prissättningsdimensionen till **nej**.

När du gör detta kan det emellertid hända att följande felmeddelande visas.

![Affärsprocessfel som uppstår när en prissättningsdimension stängs av](media/Business-Process-Error.png)


Det här felmeddelandet anger att det finns prissättningsposter som har ställts in tidigare för den dimension som ska stängas av. Alla poster för **Rollpris** och **Pålägg för rollpris** som refererar till en dimension måste tas bort innan dimensionens tillämpbarhet kan ställas in på **Nej**. Den här regeln gäller både för medföljande prissättningsdimensioner och för de prissättningsdimensioner som du har skapat. Anledningen till att validera är att Project Service har ett villkor som varje post för **rollpris** måste ha en unik kombination av dimensioner. Till exempel en prislista med namnet **amerikansk kostnadstaxan 2018** har du följande rader för **rollpris**. 

| Standardrubrik         | Organisationsenhet    |Enhet   |Pris  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systemtekniker|Contoso US|Timme| 100|USD|
| Senior systemtekniker|Contoso US|Timme| 150| USD|


När du stänger av **Standardrubrik** som prissättningsdimension och Project Service prissättningsmotor söker efter ett pris används endast värdet för **organisationsenhet** från inmatningskontexten. Om **organisationsenhet** i inmatningskontexten är "Contoso US" är resultatet inte entydigt eftersom båda raderna överensstämmer. För att undvika det här scenariot när du skapar posten **Rollpris** bekräftar Project Service att kombinationen av dimensioner är unik. Om dimensionen inaktiveras efter att posten **Rollpris** har skapats kan den här begränsningen brytas. Därför är det nödvändigt att innan du stänger av en dimension, tar bort alla rader för **Rollpris** och **Rollprispålägg** som har det dimensionsvärdet ifyllt.



[!INCLUDE[footer-include](../includes/footer-banner.md)]