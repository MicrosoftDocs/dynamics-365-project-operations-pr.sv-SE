---
title: Masskorrigeringar av faktiska värden som skapats av godkända tid- och utgiftsposter
description: I detta ämne förklaras hur en administratör kan göra enstaka eller masskorrigeringar av tidigare godkända tid- eller utgiftsposter om faktureringen inte är klar.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085716"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Masskorrigeringar av faktiska värden som skapats av godkända tid- och utgiftsposter

Ibland kan en tid- eller utgiftspost anges felaktigt. En konsult kan till exempel råka välja fel datum när han eller hon skapar en tidspost, eller också kan de råka transponera värdena när de registrerar en utgift. Om en konsult inte kan göra uppdateringar av de inskickade posterna kan en administratör korrigera posten för ett projekt direkt.

Du måste ha administratörsbehörigheter för att kunna slutföra procedurerna i den här ämnet.

## <a name="correct-approved-time-entries"></a>Korrigera godkända tidsposter     

Utför följande steg för att korrigera enstaka eller flera tidsposter för ett projekt.

1. Välj området **Försäljning** , **Transaktioner** och välj sedan **Godkänd tid**. 

2. I listan **Godkänd tid** letar du upp och markerar en eller flera godkända tidsposter som du vill korrigera. Du kan använda filtret för att söka efter relaterade poster. Du kan till exempel filtrera på ett projekt-ID och sedan välja alla godkända tidsposter med det projekt-ID:t.

3. Välj **Korrigera poster**. En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Tidskorrigering**. De valda posterna läggs till i journalen. 

4. På sidan **Ny journal** anger du en **Beskrivning** för din korrigeringsjournal innan du väljer fliken **Korrigeringar för tidsposter**.  
5. I avsnittet **Nya värden får tidsposter** uppdaterar du fälten med korrekt information efter behov. Du kan till exempel ändra det tilldelade projektet eller den bokningsbara resursen.

6. Välj **Förhandsversion**. I dialogrutan markerar du **OK**. På fliken **Journalrader** kan du Visa en lista över de ursprungliga faktiska värden som är relaterade till de valda tidssoterna som har återförts och de korrigerade motsvarande raderna som har skapats. Om du behöver göra ytterligare korrigeringar upprepar du steg 5 och 6. 

> [!NOTE]
> Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för tidsposter**.

7. Om korrigeringarna visas som de ska väljer du **Bekräfta**. I dialogrutan markerar du **OK**.

8. Gå tillbaka till området **Fförsäljning** , välj **Projekt** och öppna sedan projektet som du precis uppdaterat tidstransaktionerna för. 

9. På sidan **Projekt** i fliken **Faktiska värden** kan du se de ändringar du har gjort. 

> [!NOTE]
> Om fliken **Faktiska värden** inte syns väljer du **Relaterat** > **Faktiska värden**.  

10. I listan **Associerad vy förö faktiska värden** kan du se att de ursprungliga tidsposter som har återförts fortfarande är listade, liksom även motsvarande korrigerade tidsposter. 

I följande bild finns till exempel två radobjekt med kvantiteten 8,00 som har debet förtecknade i kolumnen Belopp. Det finns också två radobjekt med kvantiteten -8,00 som visar krediterade belopp i kolumnen Belopp. Dessa korrigeringar ställer in värdet för kvantitet till noll.

![Associerad vylista för faktiska värden](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Korrigera godkända utgiftsposter

Följ stegen nedan om du vill korrigera en eller flera utgiftsposter. 

1. I området **Försäljning** : I vänster navigeringsuta, under **Transaktioner** , väljer du **Godkända utgifter**.

2. I listan **Godkända utgifter** väljer du det projekt som du vill korrigera och väljer sedan **Korrigera poster**. En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Utgiftskorrigering**. 

3. På sidan **Ny journal** anger du en **Beskrivning** för korrigeringen, och på fliken **Utgiftskorrigering** , i avsnittet **Nya utgiftsvärden** , väljer du de datafält som du vill korrigera för valda utgiftsrader. Du kan t.ex. tilldela utgiften till ett annat **Projekt** eller korrigera **Utgiftskategori** , **Utgiftsdatum** eller **Bokningsbar resurs**.

4. Välj **Förhandsversion**. I dialogrutan markerar du **OK**. 

5. Bekräfta ändringarna på fliken **Journalrader**. Du kan visa en lista över de ursprungliga, faktiska värden som är relaterade till de valda utgiftsposterna som har återförts och motsvarande, korrigerade raderna som har skapats.

6. Om de korrigerade värdena visas som de ska väljer du **Bekräfta**. I dialogrutan markerar du **OK**. Om värdena inte visas som de ska väljer du **Avbryt** för att gå tillbaka till listan **Godkända utgifter**. Upprepa steg 2 till 5. 

> [!NOTE]
> Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för utgifter**.

7. När du har bekräftat korrigeringsjournalen navigerar du tillbaka till det eller de projekt som du uppdaterade och granskar ändringarna.  

8. I fliken **Faktiska värden** på projektsidan granskar du **Associerad vy för faktiska värden**. De ursprungliga posterna och de korrigerade posterna visas i listan. Följande bild illustrerar ursprungliga utgiftspostbelopp och motsvarande, korrigerade utgiftspostbelopp. 

![Faktiska utgifter](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
