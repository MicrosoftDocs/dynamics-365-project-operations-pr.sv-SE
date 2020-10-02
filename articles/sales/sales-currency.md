---
title: Valuta
description: I det här ämnet finns information om hur du lägger till och tar bort valutatyper i Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: d53bae2f64e7b427f762161ff08917598217bb5a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898373"
---
# <a name="currency"></a>Valuta

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med valutor bestäms priserna för produkter i produktkatalogen och kostnaden för transaktioner, till exempel försäljningsorder. Om dina kunder är utspridda över flera områden, lägga då till deras valutor för att hantera dina transaktioner. Lägg till de valutor som är de mest lämpliga för dina nuvarande och framtida affärsbehov.  

> [!NOTE]
> Om miljön är en Common Data Service-miljö kan du vara i Power Platform administratörscenter och välja sidan **valutor** (**Miljöer** > [välj miljö] > **Inställningar** > **Företag** > **Valutor**), sidan är tom. Detta beror på att inställning av en valuta inte stöds i Common Data Service-miljöer.

## <a name="add-a-currency"></a>Lägga till en valuta  
Innan du börjar med den här proceduren bör du kontrollera att säkerhetsrollen inkluderar systemadministratörsbehörighet. 

1. I Power Platform administrationscentret, välj en miljö. 
2. Välj **Inställning** > **Företag**.
3. Välj **Valutor**.  
4. Välj **Nytt**.  
5. Fyll i informationen.  


   |          Fält          |                                                                                                                                                                                                                                                                                                                                                                            Beskrivning                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valutatyp**    | - **System** - Välj det här alternativet om du vill använda valutorna som är tillgängliga i modellstyrda appar i Dynamics 365. Välj **Slå upp** om du vill söka efter en valuta. När du väljer en valutakod läggs **valutanamnet** och **valutasymbolen** automatiskt till för den valda valutan.<br />- **Anpassa** - Välj det här alternativet om du vill lägga till en valuta som inte är tillgänglig i modellstyrda appar i Dynamics 365. I detta fall måste du manuellt ange värdena för **valutakod**, **valutadecimaler**, **valutanamn**, **valutasymbol** och **valutakonvertering**. |
   |    **Valutakod**    |                                                                                                                                                                                                                                                                                                                                            Kortform för valutan. Till exempel **USD** för amerikanska dollar.                                                                                                                                                                                                                                                                                                                                            |
   | **Valutadecimaler**  |                                                                                                                                                                                  Skriv antalet decimaler som ska visas för valutan.  Du kan lägga till ett värde mellan 0 och 4. **Obs!**  Om du har angett ett precisionsvärde dialogrutan för **systeminställningar** kommer värdet att visas här.                                                                                                                                                                                  |
   |    **Valutanamn**    |                                                                                                                                                                                                                                         Om du har valt en valutakod i listan över tillgängliga valutor i modellstyrda appar i Dynamics 365 kommer valutanamnet för den valda koden att visas här. Om du har valt **Anpassad** som valutatyp, ange namnet på valutan.                                                                                                                                                                                                                                          |
   |   **Valutasymbol**   |                                                                                                                                                                                                                                                                      Om du har valt en valutakod i listan över tillgängliga valutor, kommer symbolen för den valda valutan att visas här. Om du har valt **Anpassad** som valutatyp, ange då symbolen för den nya valutan.                                                                                                                                                                                                                                                                       |
   | **Valutakonvertering** |                                                                                                                                                                                                                                     Ange värdet för den valda valutan i form av en (1) amerikansk dollar. Detta är det belopp vid vilket valda valutan konverteras till basvalutan. **Viktigt:**  Kontrollera att du kan uppdatera detta värde så ofta som det krävs, detta för att undvika eventuella felaktiga beräkningar i dina transaktioner.                                                                                                                                                                                                                                      |


6. När du är klar väljer du **Spara** eller **Spara och Stäng** i kommandofältet.  

   > [!TIP]
   >  Om du vill redigera en valuta klickar du på valutan innan du anger eller väljer nya värden.  

## <a name="delete-a-currency"></a>Ta bort en valuta  

1. I Power Platform administrationscentret, välj en miljö. 
2. Välj **Inställning** > **Företag**.
3. Välj **Valutor**.  
4. Välj den valuta som ska tas i listan över visade valutor.  
5. Välj **Ta bort**.  
6. Bekräfta borttagningen.  

> [!IMPORTANT]
>  Du kan inte ta bort valutor som används av andra poster, du kan bara inaktivera dem. Om du inaktiverar valutaposter innebär inte detta att valutainformationen som sparats i befintliga poster bort, till exempel för affärsmöjligheter eller ordrar. Du kommer emellertid inte att kunna välja den inaktiverade valutan för nya transaktioner.  
