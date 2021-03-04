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
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147315"
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

