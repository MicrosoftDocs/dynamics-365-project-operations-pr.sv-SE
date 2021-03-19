---
title: Skapa och bekräfta korrigeringsjournaler
description: I det här ämnet finns information om hur du skapar och bekräftar en korrigeringsjournal.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8ca35d1e66cbacaf65b7cd43493e3588f213788e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276955"
---
# <a name="create-and-confirm-correction-journals"></a>Skapa och bekräfta korrigeringsjournaler

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Ibland kan en tid- eller utgiftspost anges felaktigt. En konsult kan till exempel råka välja fel datum när han eller hon skapar en tidspost, eller också kan de råka transponera värdena när de registrerar en utgift. Om en konsult inte kan göra uppdateringar av de inskickade posterna kan en administratör korrigera posten för ett projekt direkt.

Du måste ha administratörsbehörigheter för att kunna slutföra procedurerna i den här ämnet.

## <a name="correct-approved-time-entries"></a>Korrigera godkända tidsposter     

Utför följande steg för att korrigera enstaka eller flera tidsposter för ett projekt.

1. Välj området **Försäljning**, **Transaktioner** och välj sedan **Godkänd tid**. 

2. I listan **Godkänd tid** letar du upp och markerar en eller flera godkända tidsposter som du vill korrigera. Du kan använda filtret för att söka efter relaterade poster. Du kan till exempel filtrera på ett projekt-ID och sedan välja alla godkända tidsposter med det projekt-ID:t.

3. Välj **Korrigera poster**. En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Tidskorrigering**. De valda posterna läggs till i journalen. 

4. På sidan **Ny journal** anger du en **Beskrivning** för din korrigeringsjournal innan du väljer fliken **Korrigeringar för tidsposter**.  

5. I avsnittet **Nya värden får tidsposter** uppdaterar du fälten med korrekt information efter behov. Du kan till exempel ändra det tilldelade projektet eller den bokningsbara resursen.

6. Välj **Förhandsversion**. I dialogrutan markerar du **OK**. På fliken **Journalrader** kan du Visa en lista över de ursprungliga faktiska värden som är relaterade till de valda tidssoterna som har återförts och de korrigerade motsvarande raderna som har skapats. Om du behöver göra ytterligare korrigeringar upprepar du steg 5 och 6. 

> [!NOTE]
> Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för tidsposter**.

7. Om korrigeringarna visas som de ska väljer du **Bekräfta**. I dialogrutan markerar du **OK**.

8. Gå tillbaka till området **Fförsäljning**, välj **Projekt** och öppna sedan projektet som du precis uppdaterat tidstransaktionerna för. 

9. På sidan **Projekt** i fliken **Faktiska värden** kan du se de ändringar du har gjort. 

> [!NOTE]
> Om fliken **Faktiska värden** inte syns väljer du **Relaterat** > **Faktiska värden**.  

10. I listan **Associerad vy förö faktiska värden** kan du se att de ursprungliga tidsposter som har återförts fortfarande är listade, liksom även motsvarande korrigerade tidsposter. 

I följande bild finns till exempel två radobjekt med kvantiteten 8,00 som har debet förtecknade i kolumnen Belopp. Det finns också två radobjekt med kvantiteten -8,00 som visar krediterade belopp i kolumnen Belopp. Dessa korrigeringar ställer in värdet för kvantitet till noll.

 
## <a name="correct-approved-expense-entries"></a>Korrigera godkända utgiftsposter

Följ stegen nedan om du vill korrigera en eller flera utgiftsposter. 

1. I området **Försäljning**: I vänster navigeringsuta, under **Transaktioner**, väljer du **Godkända utgifter**.

2. I listan **Godkända utgifter** väljer du det projekt som du vill korrigera och väljer sedan **Korrigera poster**. En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Utgiftskorrigering**. 

3. På sidan **Ny journal** anger du en **Beskrivning** för korrigeringen, och på fliken **Utgiftskorrigering**, i avsnittet **Nya utgiftsvärden**, väljer du de datafält som du vill korrigera för valda utgiftsrader. Du kan t.ex. tilldela utgiften till ett annat **Projekt** eller korrigera **Utgiftskategori**, **Utgiftsdatum** eller **Bokningsbar resurs**.

4. Välj **Förhandsversion**. I dialogrutan markerar du **OK**. 

5. Bekräfta ändringarna på fliken **Journalrader**. Du kan visa en lista över de ursprungliga, faktiska värden som är relaterade till de valda utgiftsposterna som har återförts och motsvarande, korrigerade raderna som har skapats.

6. Om de korrigerade värdena visas som de ska väljer du **Bekräfta**. I dialogrutan markerar du **OK**. Om värdena inte visas som de ska väljer du **Avbryt** för att gå tillbaka till listan **Godkända utgifter**. Upprepa steg 2 till 5. 

> [!NOTE]
> Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för utgifter**.

7. När du har bekräftat korrigeringsjournalen navigerar du tillbaka till det eller de projekt som du uppdaterade och granskar ändringarna.  

8. I fliken **Faktiska värden** på projektsidan granskar du **Associerad vy för faktiska värden**. De ursprungliga posterna och de korrigerade posterna visas i listan. Följande bild illustrerar ursprungliga utgiftspostbelopp och motsvarande, korrigerade utgiftspostbelopp. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]