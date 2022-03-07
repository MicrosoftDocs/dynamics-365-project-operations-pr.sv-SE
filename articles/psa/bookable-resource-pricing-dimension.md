---
title: Använda bokningsbar resurs som prissättningsdimension
description: I det här ämnet finns information om hur du använder en bokningsbar resurs som prissättningsdimension.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: d3f5ed7da5972cec5b22524bdcb3dc34a83eee28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290966"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Använda bokningsbar resurs som prissättningsdimension

[!include [banner](../includes/psa-now-project-operations.md)]

I det här ämnet finns information om hur du använder en bokningsbar resurs som prissättningsdimension. Innan du börjar måste du, om du inte redan har skapat en dimensionslösning för prissättning, skapa en ny. Om du redan har en dimensionslösning för prissättning kan du göra ändringarna i den lösningen. Om du inte har skapat en ny dimensionslösning för prissättning för organisationen ska du slutföra procedurerna i ämnet [skapa anpassade fält och entiteter](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Lägga till bokningsbar resurs i formulär och vyer
Om du vill att fälten ska visas i användargränssnittet i dimensionslösningen för prissättning måste du gå igenom alla formulären och vyerna för de huvudsakliga Project Service-enheterna och lägga till dessa fält i formulären och vyerna för dessa entiteter.
Följande tabell är en fullständig lista över de formulär och vyer som inte ingår i rutan efter entitet som behöver uppdateras. Om det finns ytterligare vyer eller formulär i anpassningarna i dessa entiteter kan du lägga till de nya fälten i dem.
Öppna lösningsutforskaren för dimensionslösningen för prissättning och klicka sedan på **publicera alla anpassningar**.


|   Entitet        | Formulär   |Vyer        |
| ------------------------------|---------------------------------|----------------------------------|
|  Pris för roll|• Information |• Aktiva resurskategoripriser<br> • Associerad vy för resurskategoripris|
|  Pålägg för rollpris|• Information|• Aktivt pålägg för rollpris<br>• Associerad vy för pålägg för rollpris|
|  Information om offertrad|• Projektinformation<br>• Snabbregistrera projekt|• Aktiv information om offertrad<br>• Kombinerad information om offertrad<br>• Associerad vy för information om offertrad|
|  Information om projektkontraktrad|• Projektinformation<br>• Snabbregistrera projekt|• Kombinerad kontraktradsinformation<br>• Aktiv kontraktradsinformation<br>• Associerad vy för kontraktradsinformation|
|  Projektuppgift|• Information<br>• Nytt formulär||
|  Projektteammedlem|• Information<br>• Nytt formulär|• Aktiva projektteammedlemmar<br>• Projektgruppmedlemmar<br>• Associerad vy för projektgruppmedlemmar|
|  Tidspost|• Information<br>• Skapa tidspost|• Mina tidsposter efter datum<br>• Mina tidsposter för den här veckan<br>• Tidsposter för godkännande.|
|  Journalrad|• Information<br>• Snabbregistrering|• Aktiva journalrader<br>• Associerad vy för journalrad|
|  Information om fakturarad|• Information<br>• Snabbregistrering|• Information om aktiv fakturarad<br>• Debiterbara fakturatransaktioner<br>• Kostnadsfria fakturatransaktioner<br>• Associerad vy för information om fakturarad<br>• Icke debiterbar fakturatransaktion|
|  Faktiskt|• Information<br>• Aktiva faktiska värden|• Associerad vy för faktiska värden|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Ställ in bokningsbar resurs som prissättningsdimension

1. I webbgränssnittet, gå till **Project Service** > **inställningar** > **parametrar**. På fliken **Parameter** på fliken **Beloppsbaserade prissättningsdimensioner** kan du notera att i rutnätet på fliken visas posterna i entiteten prissättningsdimensioner. 
2. Lägg till **Bokningsbar resurs** i den här listan över prisdimensioner som **msdyn_bookableresource**. 
3. Ange det sammanhang i vilket bokningsbara resursen fungerar som en prissättningsdimension och ange värdena **Gäller för kostnad** och **Gäller för försäljning**.
4. I fältet **dimensionstyp** väljer du **beloppsberoende**. 
5. Välj kostnads- och försäljningsprioritet för den bokningsbara resursen. När en bokningsbar resurs ingår som en prissättningsdimension har den högst prioritet så att ange en till **1** (eller **0** beroende på hur prioriteten räknas) ser till att beteendet fungerar.

## <a name="set-up-pricing-dimension-field-names"></a>Ange fältnamn för prissättningsdimension

När fältnamnet för en prisdimension i tabellen **Rollpris** skiljer sig från dess fältnamn i någon av de andra entiteterna där prisstandard ska användas, måste posten för prisdimension vara medveten om de olika namnen.    
För den bokningsbara resursen **Projektteammedlemmar** något annorlunda fältnamn (**msdyn_bookableresourceid**) som den benämns för entiteten **Rollpris** (**msdyn_bookableresource**). Dimensionen för prissättningsdimension för **msydn_bookableresource** måste göras medveten om detta. 
1. Det gör du genom att dubbelklicka på raden i rutnätet **prisdimensioner** för att öppna dimensionssidan med **msdyn_bookableresource**.
2. På dimensionssidan på fliken **Relaterad**, klicka på **Fältnamn för prissättningsdimensioner**.

 ![Fliken fältnamn för prissättningsdimensionerr](media/PD-fieldname.png)

4. Klicka på **Lägg till fältnamn på ny prissättningsdimensionen** i den associerade vyn som öppnas.

 ![Lägg till nya fältnamn för prissättningsdimensioner](media/Add-NewPD-fieldname.png)


Då öppnas sidan **nya prissättningsdimensioner** för **msdyn_bookableresource**. 

5. Lägg till **msdyn_projectteam** till fältet **entiteten logiskt namn** och **msdyn_bookableresourceid** till fältet **fältnamn**. Spara posten.

 ![Formulär för fältnamn för prissättningsdimensioner](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]