---
title: Projektförsäljningsspårning
description: Detta ämne ger information om hur Project Operations spårar framsteg mot arbetsintäkten för ett projekt.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f9873dc3e709453a56cb53273b35cc1cd312127
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996993"
---
# <a name="project-sales-tracking"></a>Projektförsäljningsspårning

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations spårar arbetsuppskattningar och intäkter minst granularitet på projektplanen. Uppskattningen av arbetsintäkten baseras på den planerade insatsen och de generiska eller namngivna resurserna som tilldelas varje lövnodsuppgift i projektplanen. När projektet börjar och människor börjar rapportera tid på olika projektaktiviteter summeras de faktiska arbetsintäkterna som startar en beräkning av projektionerna.

## <a name="labor-revenue-tracking-view"></a>Vyn Spårning av arbetsintäkt

På sidan **Projekt** på fliken **Spårning** kan du välja **Spårning** > **Kostnad** för att öppna vyn **Kostnadsspårning**. Du kan också välja **Använd** > **Fakturataxa** om du vill öppna vyn **Intäktsspårning** som visar hur arbetsintäkterna utvecklas för varje uppgift i projektplanen. I den här vyn jämförs också den faktiska arbetsintäkten för en aktivitet med aktivitetens planerade arbetsintäkt. Project Operations använder följande formler för att beräkna arbetsintäktsmått:

- **Planerad intäkt**: Beräknade försäljningsvärden för alla resurstilldelningar för varje lövnodaktivitet
- **Verklig intäkt**: Summan av alla faktiska värden för ofakturerad försäljning för tid som registrerats på aktiviteten
- **Fakturerbar omsättning%**: Faktisk intäkt ÷ intäktsberäkning vid slutförande
- **Återstående intäkt**: Intäktsberäkning vid slutförande - Faktisk intäkt
- **Beräknad intäkt vid färdigställande**: Återstående intäkt + Faktisk intäkt
- **Intäktsavvikelse**: Planerad intäkt - Beräknad intäkt vid färdigställande


> [!NOTE]
> Project Operations visar endast arbetsintäkter på sidan **Projekt** på fliken **Spårning**. Även om material och kostnader kan uppskattas och spåras för konsumtion ingår inte dessa intäkter i intäkterna som visas på fliken **Spårning**. Den här fliken är utformad för att endast fungera för att omprojektera arbetsintäkter genom att omprojektera ansträngning.  
> Alla intäktsbelopp som visas konverteras till projektets kostnadsvaluta. Projektets kostnadsvaluta är den kontrakterande enhetens valuta på projektet. För projekt med fast pris, intäktsnummer i vyn **Spårning av arbetsintäkter** är inte relevant eftersom obegränsad försäljningsreklam inte registreras på tidens godkännande.
> De uppskattade försäljningsvärdena för tiden som visas på fliken **Beräkning** projektets flik kanske inte lägger till det planerade intäktsvärdet på fliken **Spårning** . Källan till denna avvikelse beror på två möjliga orsaker:
><ol>
   ><li> Fliken <b>Beräkningar</b> visar beräknade intäkter i försäljningsvalutan, medan fliken <b>Spårning</b> visar planerade intäkter omvandlade till kostnadsvalutan. </li>
   ><li> När beräknad försäljning omvandlas till avtalsvalutan som visas på fliken <b>Beräkningar</b> till projektvalutan, innebär konverteringen steg som kan leda till viss förlust av noggrannhet: </li>
><ol>
><li> Det beräknade försäljningsbeloppet i kontraktvalutan konverteras först till basvalutan (konvertering 1).</li>
><li> Det beräknade försäljningsbeloppet i basvalutan konverteras först till valutan för projektkostnadens valutan (konvertering 2). </li>
></ol>
></ol>
> Valutaprecision tillämpas i båda stegen, vilket resulterar i att de planerade intäkterna i projektvalutan för den planerade försäljningen i kontraktvalutan förs in.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Omprojektera intäkter för uppgifter på en lövnod

Arbetskraftsintäkter på en lövnodsuppgift kan inte direkt projiceras på **Spårning** på sidan **Projekt**. Du kan dock använda vyn **Insatsspårning** för att återberätta den återstående insatsen för en aktivitet. Detta gör att den återstående intäkten för uppgiften omberäknas. Följande är en beskrivning av hur detta fungerar.

1. En projektledare kan omprojicera insatser på uppgifter genom att uppdatera standardvärdet i fältet **Återstående insats** med en ny beräkning av återstående insats av uppgiften. Denna omprojicering orsakar en omberäkning av uppgiftens insats vid slutförd (EAC), förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, beräknat att slutföra (ETC) och förloppsprocent för sammanfattningsaktiviteterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.
2. Utifrån det nya värdet för den återstående uppgiften beräknar systemet återstående omsättning i vyn **Intäktsspårning**. För att kunna beräkna återstående omsättning utifrån återstående insats beräknar systemet först den genomsnittsintäkten på en timmes insats för uppgiften som planerad intäkt eller planerad insats. Den planerade omsättningen är summan av intäkten av alla resurstilldelningar för uppgiften. Den genomsnittsintäkten per timme används för att beräkna återstående intäkt för den nyligen projekterade återstående åtgärden för uppgiften.
3. Den beräknade omsättningen i procent av totalintäkten och i procent av omsättningen för lövnodsuppgift beräknas om.
4. Intäkterna till komplett värde av de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Omprojektera intäkter för sammanfattningsuppgifter

Du kan omprojicera arbetsintäkten på sammanfattningsuppgifter eller behållaruppgifter. Du kan dock inte direkt omprojicera arbetskraftsintäkterna på en sammanfattande projektuppgift på **Spårning** på sidan **Projekt**. I likhet med uppgifter på en lövnod kan du omprojektera sammanfattnings- och behållaraktiviteter med hjälp av vyn **Insatsspårning**. I den här vyn kan du omprojicera den återstående ansträngningen för en sammanfattande uppgift som orsakar en omberäkning av återstående intäkter för sammanfattningsuppgiften. Följande är en beskrivning av hur detta fungerar.

1. En projektledare kan omprojicera insatser på uppgifter genom att uppdatera standardvärdet i fältet **Återstående insats** med en ny beräkning av **Återstående insats** av uppgiften. Denna omprojicering orsakar en omberäkning av uppgiftens uppskattning vid slutförd (EAC), förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, ETC och förlopp för sammanfattningsuppgifterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.
2. Utifrån det nya värdet för fältet **Återstående insats** beräknar systemet återstående omsättning i vyn **Intäktsspårning**. För att kunna beräkna återstående omsättning utifrån återstående insats beräknar systemet först den genomsnittsintäkten på en timmes insats för uppgiften som planerad intäkt eller planerad insats. Den planerade omsättningen är summan av intäkten av alla resurstilldelningar för uppgiften. Denna genomsnittliga intäkt per timme används sedan för att beräkna intäkten för den nyligen projekterade återstående åtgärden för uppgiften.
3. Den beräknade omsättningen i procent av totalintäkten och i procent av omsättningen för sammafattningsuppgift beräknas om.
4. Det nya värdet för den beräknade intäkten vid slutfördelningen fördelas ner till underordnade uppgifter i samma proportion som den ursprungliga planerade intäkten var för uppgiften.
5. Den nya beräknade intäkten som är fullbordad för var och en av de enskilda uppgifterna fram till uppgifter på en lövnod beräknas. Baserat på detta värde kommer de drabbade underordnade uppgifterna ned till lövnoder att resterande intäkter och intäktsförbrukningsprocent beräknas om baserat på intäkterna till fullständigt värde. Detta resulterar i en ny projektion för uppgiftens intäktsavvikelse. 
6. Intäkterna till komplett värde av de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

