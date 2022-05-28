---
title: Spårning av projektkostnad
description: Detta ämne ger information om hur Project Operations spårar framsteg mot arbetskostnader och utgifter för ett projekt.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f724ee29728a363c58ed0e69087f4c18be89ea2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591472"
---
# <a name="labor-cost-tracking-on-projects"></a>Spårning av arbetskostnader för projekt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations spårar arbetsuppskattningar och spenderar minst granularitet på projektplanen. Den ekonomiska uppskattningen av arbetskraftskostnaderna baseras på den planerade insatsen och de generiska eller namngivna resurserna som tilldelas varje lövnodsuppgift i projektplanen. När projektet börjar och människor börjar rapportera tid på olika projektaktiviteter summeras de faktiska arbetsutgifter som startar en beräkning av projektionerna.

## <a name="labor-cost-tracking-view"></a>Vyn Spårning av arbetskostnader

På sidan **Projekt** på fliken **Spårning** kan du välja **Spårning** > **Kostnad** för att öppna vyn **Kostnadsspårning** och se utvecklingen av arbetskraftsutgifterna för varje uppgift i projektplanen. I den här vyn jämförs också den faktiska arbetskostnaden för en aktivitet med aktivitetens planerade arbetskostnad. Project Operations använder följande formler för att beräkna arbetskostnadsmått:

- **Planerad kostnad**: Beräknad kostnad för alla resurstilldelningar för varje lövnodaktivitet
- **Verklig kostnad**: Summan av alla kostnadssummor för tid som registrerats på aktiviteten
- **Procentsats för kostnadsförbrukning**: Faktisk kostnad ÷ Kostnadsberäkning vid färdigställande
- **Återstående kostnad**: Kostnadsberäkning vid färdigställande - Faktisk kostnad
- **Kostnad vid färdigställande**: Återstående kostnad + Faktisk kostnad
- **Kostnadsavvikelse**: Planerad kostnad - Kostnadsberäkning vid färdigställande

Varje uppgift visar en projektion av kostnadsavvikelsen på uppgiften. Om kostnadsberäkning vid färdigställande som slutförs är mer än den planerade kostnaden beräknas aktiviteten gå över budget. Om kostnadsberäkning vid färdigställande som slutförs är mindre än den planerade kostnaden beräknas aktiviteten avslutas under budgeten.

>[!NOTE]
> Project Operations visar endast arbetskostnader på sidan **Projekt** på fliken **Spårning**. Även om material och kostnader kan uppskattas och spåras för konsumtion ingår inte dessa kostnader i kostnader som visas på fliken **Spårning**. Den här fliken är utformad för att endast fungera för att omprojektera arbetskostnader genom att omprojektera ansträngning.
Alla kostnadsbelopp som visas konverteras till projektets kostnadsvaluta från projektets självkostnadsvaluta som används för att fastställa självkostnaden. Projektets kostnadsvaluta är den kontrakterande enhetens valuta på projektet. De beräknade kostnadsvärdena för tiden som visas på fliken **Beräkningar** på sidan **Projekt** kanske inte lägger till den planerade kostnaden på fliken **Spårning**. Anledningen till denna avvikelse beror på skillnaderna i hur beräknade kostnader sammanfattas på rutnätet **Beräkningar** och hur planerad kostnad beräknas i rutnätet **Spårning**. 
>
> - Beräkna **Fliken Beräkningar** den beräknade kostnaden med samma valuta som kostnadstaxan i prislistan. Sedan konverteras den uppskattade kostnaden i prislistevalutan till den uppskattade kostnaden i projektets kostnadsvaluta. Den uppskattade kostnaden i projektvalutan visas avrundat till 2 decimaler. Inte vid något tillfälle under denna konvertering tillämpas valutaprecision. 
> - På fliken **Spårning** följer den planerade kostnadsberäkningen en något annorlunda beräkningsordning som innebär att valutaprecision tillämpas i två steg: 
   ><ol>
   ><li>Det beräknade kostnadsbeloppet i prislistans omvandlas till basvalutan (konvertering 1).</li>
   ><li>Det beräknade kostnadsbeloppet i basvaluta omvandlas till projektkostnadens valuta (konvertering 2). </li>
   ></ol>
   >Valutaprecision tillämpas i båda stegen för att få en planerad kostnad (på fliken **Spårning**) som avviker något från den beräknade kostnaden (i vyn **Tidsfasad** i fliken **Beräkningar**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Omprojektera kostnader för uppgifter på en lövnod

Arbetskostnader på en lövnodsuppgift kan inte direkt projiceras på **Spårning** på sidan **Projekt**. Du kan dock använda vyn **Insatsspårning** för att återberätta den återstående insatsen för en aktivitet. Detta gör att den återstående kostnaden för uppgiften omberäknas. Följande är en beskrivning av hur detta fungerar.

1. En projektledare kan omprojicera insatser på uppgifter genom att uppdatera standardvärdet i fältet **Återstående insats** med en ny beräkning av återstående insats av uppgiften. Denna omprojicering orsakar en omberäkning av uppgiftens insats vid slutförd (EAC), förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, beräknat att slutföra (ETC) och förloppsprocent för sammanfattningsaktiviteterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.
2. Utifrån det nya värdet för den återstående uppgiften beräknar systemet återstående kostnad i vyn **Kostnadsspårning**. För att kunna beräkna återstående kostnad utifrån återstående insats beräknar systemet först den genomsnittskostnaden på en timmes insats för uppgiften som planerad kostnad eller planerad insats. Den planerade kostnaden är summan av kostnaden av alla resurstilldelningar för uppgiften. Genomsnittskostnaden per timme används för att beräkna återstående kostnad för den nyligen projekterade återstående åtgärden för uppgiften.
3. Den beräknade kostnaden i procent av totalkostnaden och i procent av omsättningen för lövnodsuppgift beräknas om.
4. Kostnaden till komplett värde av de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.

## <a name="reprojecting-costs-on-summary-tasks"></a>Omprojicering kostnader för sammanfattningsuppgifter

Du kan omprojicera arbetskostnader på sammanfattningsuppgifter eller behållaruppgifter. Du kan dock inte direkt omprojicera arbetskraftkostnad på en sammanfattande projektuppgift på **Spårning** på sidan **Projekt**. I likhet med uppgifter på en lövnod kan du omprojektera sammanfattnings- och behållaraktiviteter med hjälp av vyn **Insatsspårning**. I den här vyn kan du omprojicera den återstående ansträngningen för en sammanfattande uppgift som orsakar en omberäkning av återstående kostnader för sammanfattningsuppgiften. Följande är en beskrivning av hur detta fungerar.

1. En projektledare kan Omprojektera en insats för sammanfattningsuppgifter genom att uppdatera standardvärdet för återstående insats med en ny beräkning av uppgiften. Denna uppdatering orsakar en omberäkning av sammanfattningsuppgifter uppskattning vid slutförd (EAC), förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, ETC och förlopp för sammanfattningsuppgifterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.
2. Utifrån det nya värdet för den återstående sammanfattningsuppgiften beräknar systemet återstående kostnad i vyn **Kostnadsspårning**. För att kunna beräkna återstående kostnad utifrån återstående insats beräknar systemet först den genomsnittskostnaden på en timmes insats för sammanfattningsuppgiften som planerad kostnad eller planerad insats. Genomsnittskostnaden per timme används för att beräkna kostnaden för den nyligen projekterade återstående åtgärden för sammanfattningsuppgift.
3. Den beräknade kostnaden i procent av totalkostnaden och i procent av omsättningen för sammanfattningsuppgift beräknas om.
4. Den nya kostnaden vid slutfördelning fördelas ner till underordnade uppgifter i samma proportion som den ursprungliga planerade kostnaden var för uppgiften.
5. Den nya kostnaden till komplett värde för var och en av de enskilda uppgifterna fram till uppgifter på en lövnod beräknas. Baserat på detta värde kommer de drabbade underordnade uppgifterna ned till lövnoder att resterande kostnad och kostnadsförbrukningsprocent beräknas om baserat på kostnaderna till fullständigt värde. Detta värde resulterar i en ny projektion för uppgiftens kostnadsavvikelse. 


Fältet **Kostnadsprestanda** kan ställas in från spårningsdata. När kostnadsavvikelsen för rotnoden i vyn **Kostnadsspårning** är negativ kan du ange det här fältet till **Under budget**. När kostnadsavvikelsen för rotnoden är positiv kan du ange värdet till **Över budget**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
