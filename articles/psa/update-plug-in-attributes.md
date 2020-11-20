---
title: Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner
description: I den här ämnet finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c42e5fda79d51430f4dedf46037e11c86a38c474
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121870"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner

> [!NOTE]
> Om du inte använder funktionerna för offert och kontrakt i Project Service Automation (PSA) kan du hoppa över det här ämnet.

I den här ämnet förutsätts att du har slutfört procedurerna i avsnittet [Skapa anpassade fält och entiteter](create-custom-fields-entities.md), [Lägg till anpassade fält till prisinställningar och transaktionsenheter](field-references.md) och [Ställ in anpassade fält som prissättningsdimensioner](set-up-pricing-dimensions.md). Om du inte har slutfört de här procedurerna går du tillbaka och slutför dem och går sedan tillbaka till ämne.

När en offertraddetalj skapas på sidan **Offertrad** för en projektoffert rad skapas två uppskattningsrader i bakgrunden, en rad för kostnadssidan för uppskattningen och en för försäljningssidan. Det här är samma för projektkontraktrader.

När du gör en ändring av kvantiteten eller ett fält på kostnadssidan, sprids den ändringen till försäljningssidan. Detta kan bero på att följande plugin-program måste registreras om efter en ändring i prissättningsdimensionerna.

- PreOperationContractLineDetailUpdate - uppdateringar **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - uppdateringar **msdyn_quotelinetransaction**.

Nedan förklaras hur du registrerar plugin-programmen.

1. Öppna **PluginRegistrationTool** och anslut till din online-instans.
2. Klicka på **Sök** och sök efter det plugin-program som du vill uppdatera.

 ![Skärmbild av sökträdet](media/PRT-1.png)

3. När du har hittat plugin-programmet markerar du det och klickar på **Välj på huvudformulär**.

4. Markera steget för det plugin-program som ska uppdateras, högerklicka och välj sedan **uppdatera**.

 ![Skärmbild av det plugin-program som ska uppdateras](media/PRT-2.png)
 
5. I uppdateringsfönstret, klicka på ellipsen (**...**) i filtreringsattributen.

 ![Skärmbild av Uppdatera befintlig stegkonfigurationsinformation](media/PRT-3.png)
 
6. Markera kryssrutorna för prissättningsattribut.

 ![Skärmbild som visar markeringen i kryssrutan för prissättningsattribut](media/PRT-4.png)

7. Klicka på **OK** för att stänga sidan och välj sedan **Updatera steg**.

 ![Skärmbild som visar knappen "Uppdatera steg"](media/PRT-5.png)
 
8. Upprepa den här processen för det andra plugin-programmet **PreOperationQuoteLineDetail - uppdatera msdyn_quotelinetransaction**.

9. Stäng registrering av plugin-program.

