---
title: Skapa och bekräfta korrigeringsjournaler
description: I det här ämnet finns information om hur du skapar och bekräftar en korrigeringsjournal.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582825"
---
# <a name="create-and-confirm-correction-journals"></a>Skapa och bekräfta korrigeringsjournaler

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Ibland kan en tids- eller utgiftspost komma att anges felaktigt. En konsult kan till exempel välja fel datum när han eller hon skapar en tidspost, eller välja fel projekt när de anger en utgift. Om en konsult inte kan uppdatera inskickade poster kan en backend-administratör korrigera faktiska värden för ett projekt direkt.

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

 
## <a name="correct-approved-expense-entries"></a>Korrigera godkända utgiftsposter

Följ stegen nedan om du vill korrigera en eller flera utgiftsposter. 

1. I området **Försäljning**: I vänster navigeringsuta, under **Transaktioner**, väljer du **Godkända utgifter**.

2. I listan **Godkända utgifter** väljer du det projekt som du vill korrigera och väljer sedan **Korrigera poster**. En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Utgiftskorrigering**. 

3. På sidan **Ny journal** anger du en **Beskrivning** för korrigeringen, och på fliken **Utgiftskorrigering**, i avsnittet **Nya utgiftsvärden**, väljer du de datafält som du vill korrigera för valda utgiftsrader. Du kan t.ex. tilldela utgiften till ett annat **Projekt** eller korrigera **Utgiftskategori**, **Utgiftsdatum** eller **Bokningsbar resurs**.

4. Välj **Förhandsversion**. I dialogrutan markerar du **OK**. 

5. Bekräfta ändringarna på fliken **Journalrader**. Du kan visa en lista över de ursprungliga, faktiska värden som är relaterade till de valda utgiftsposterna som har återförts och motsvarande, korrigerade raderna som har skapats.

6. Om de korrigerade värdena visas som de ska väljer du **Bekräfta**. I dialogrutan markerar du **OK**. Om värdena inte visas som de ska väljer du **Avbryt** för att gå tillbaka till listan **Godkända utgifter**. Upprepa steg 2 till 5. 

7. När du har bekräftat korrigeringsjournalen återgår du till det eller de projekt som du har uppdaterat för att visa ändringarna.

8. På fliken **Faktiska värden** på projektsidan granskar du listan **Vy associerad med faktiska värden**. De ursprungliga posterna och de korrigerade posterna visas i listan.


## <a name="correct-approved-material-usage-logs"></a>Korrigera godkända användningsloggar för material

Korrigera en eller flera användningsloggposter för material genom att följa stegen nedan.

1. I avsnittet **Försäljning** > i vänster navigeringsfönster, under **Transaktioner**, väljer du **Faktiska värden**.

2. I listan **Faktiska värden** använder du kolumnfilter för att välja transaktionsklassen **Material**, så att endast faktiska värden för material visas. Med andra kolumnfilter kan du ytterligare begränsa de faktiska värden som visas. När du har hittat den önskade uppsättningen faktiska värden markerar du de faktiska värdena och väljer sedan **Korrigera poster**. En ny korrigeringsjournal skapas automatiskt, och typen **Materialkorrigering** tilldelas.

3. På sidan **Ny journal** anger du en beskrivning för korrigeringen i fältet **Beskrivning**. På fliken **Materialkorrigering**, i avsnittet **Nya värden för material** väljer du sedan de datafält som ska korrigeras för de valda materialraderna. Du kan till exempel tilldela materialet till ett annat projekt eller korrigera produkt, materialdatum eller underleverantör.

4. Välj **Förhandsversion**. Klicka sedan på **OK** i nästa dialogruta.

5. Kontrollera korrigeringarna på fliken **Journalrader**. Du kan visa en lista över de ursprungliga faktiska värden som är relaterade till de valda materialposter som har återförts och de korrigerade motsvarande rader som har skapats.

6. Om de korrigerade värdena visas som de ska väljer du **Bekräfta**. Klicka sedan på **OK** i nästa dialogruta. Om värdena inte är som förväntat väljer du **Avbryt** om du vill återgå till listan **Faktiska värden**. Upprepa sedan stegen 2 till 5.

7. När du har bekräftat korrigeringsjournalen återgår du till det eller de projekt som du har uppdaterat för att visa ändringarna.

8. På fliken **Faktiska värden** på projektsidan granskar du listan **Vy associerad med faktiska värden**. De ursprungliga posterna och de korrigerade posterna visas i listan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
