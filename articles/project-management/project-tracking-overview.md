---
title: Spårning av projektansträngning
description: I det här ämnet finns information om hur du spårar projektarbete och framsteg i arbetet.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 037118714cf01ba2fb91cdd94345495d12ccb645
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593818"
---
# <a name="project-effort-tracking"></a>Spårning av projektansträngning

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Behovet av att följa upp statusen för ett schema varierar efter bransch. Vissa branscher spårar på en detaljerad nivå, medan andra branscher spårar på en högre nivå. I det här ämnet illustreras hur du schemalägger för att uppfylla organisationens krav.

## <a name="effort-tracking-view"></a>Insatsspårningsvy

I vyn **Spåra insats** spåras förloppet för uppgifterna i schemat genom att jämföra de faktiska arbetsinsatstimmarna som ägnats åt en uppgift med uppgiftens planerade arbetsinsatstimmar. Dynamics 365 Project Operations använder följande formler för att beräkna spårningsmått:

- **Förloppsprocent**: Den faktiska insatsen hittills ÷ Uppskattning vid slutfört (EAC) 
- **Resterande insats**: Uppskattad insats vid slutföring - Faktisk insats hittills 
- **EAC**: resterande insats + den faktiska insatsen hittills 
- **Planerad insatsavvikelse**: planerat arbete – EAC

Project Operations visar en projektion av insatsavvikelsen för uppgiften. Om EAC är större än den planerade ansträngningen projiceras uppgiften för att ta längre tid än vad som ursprungligen planerades och ligger efter i planeringen. Om EAC är mindre än den planerade ansträngningen projiceras uppgiften för att ta mindre tid än vad som ursprungligen planerades och ligger före i planeringen.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Omprojektera insats för uppgifter på en lövnod

Projektledare ändrar ofta de ursprungliga uppskattningarna för en uppgift. Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status. Vi rekommenderar dock inte att projektansvariga ändrar antalet planerade åtgärder. Detta beror på att projektets planerade insats representerar den etablerade källan till sanning för projektschemat och kostnadsberäkningen, och alla projektintressenter har gått med på det.

En projektledare kan Omprojektera en insats för uppgifter genom att uppdatera standardvärdet **Återstående insats** med en ny beräkning av uppgiften. Denna uppdatering orsakar en omberäkning av uppgiftens uppskattning vid slutförd (EAC), förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, ETC och förlopp för sammanfattningsuppgifterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Omprojektering av ansträngning för sammanfattningsuppgifter

Arbete för sammanfattningsuppgifter eller behållaruppgifter kan projiceras om. Projektansvariga kan uppdatera återstående insats för sammanfattningsuppgifterna. Om du uppdaterar den återstående insatslösningen utlöses följande uppsättning beräkningar i programmet:

- Procentförloppet för EAC och aktiviteten beräknas.
- Nya EAC fördelas nedåt till de underordnade uppgifterna i samma proportion som original EAC var på aktiviteten.
- De nya EAC för var och en av de enskilda aktiviteterna till noderna för lövnoder beräknas. 
- De underordnade aktiviteterna som påverkas ned till lövnoder har deras återstående insats och förloppet omberäknas efter EAC-värdet. Detta resulterar i en ny projektion för uppgiftens insatsavvikelse. 
- EAC för de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.
- En godkänd insats på en sammanfattningsuppgift är summan av den godkända åtgärden för alla underordnade uppgifter plus den godkända åtgärden för sammanfattningsuppgiften.
- Den återstående insatsen för en sammanfattningsuppgift är summan av återstående åtgärd(er) för alla underordnade uppgifter minus den godkända åtgärden för sammanfattningsuppgiften.

## <a name="project-status-summary"></a>Sammanfattning av projektstatus

Spåra data i **Insatsspårning** och **Kostnadsspårning** visas förloppet och kostnadsförbrukning på projektets rotnod, sammanfattningsaktiviteter och aktivitetsnivåerna på lövnodnivå. I avsnittet **status** på sidan **projektentitet** visas en översikt över status på projektnivå.

## <a name="status-summary-fields"></a>Fält för statussammanfattning

Fältet **övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status. Det använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker. I fältet **kommentarer** kan projektledaren ange kommentarer om statusen. Fältet **status uppdaterad för** är inte redigerbart och värdet är en tidstämpel som anger när status senast uppdaterades.

Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsdatumet. När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva kan du ange att dessa fält till **Före**. När schema och kostnadsavvikelse för rotnoden är negativa kan du ange dem till **Efter**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
