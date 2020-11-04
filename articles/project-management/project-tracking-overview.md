---
title: Översikt över projektspårning
description: I det här ämnet finns information om hur du spårar projektstatus och kostnadsförbrukning.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085391"
---
# <a name="project-tracking-overview"></a>Översikt över projektspårning

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Behovet av att följa upp statusen för ett schema varierar efter bransch. Vissa branscher spårar på en detaljerad nivå, medan andra branscher spårar på en högre nivå. I det här ämnet illustreras hur du schemalägger för att uppfylla organisationens krav.

## <a name="effort-tracking-view"></a>Insatsspårningsvy

I vyn **Spåra insats** spåras förloppet för uppgifterna i schemat genom att jämföra de faktiska arbetsinsatstimmarna som ägnats åt en uppgift med uppgiftens planerade arbetsinsatstimmar. I Dynamics 365 Project Operations används följande formler för att beräkna spårningsmått:

- **Förloppsprocent** : Den faktiska insatsen hittills ÷ Uppskattning vid slutfört (EAC) 
- **Uppskattning för att slutföra (ETC)** : planerad insats – den faktiska insatsen hittills 
- **EAC** : resterande insats + den faktiska insatsen hittills 
- **Planerad insatsavvikelse** : planerat arbete – EAC

Project Operations visar en projektion av insatsavvikelsen för uppgiften. Om EAC är större än den planerade ansträngningen projiceras uppgiften för att ta längre tid än vad som ursprungligen planerades och ligger efter i planeringen. Om EAC är mindre än den planerade ansträngningen projiceras uppgiften för att ta mindre tid än vad som ursprungligen planerades och ligger före i planeringen.

## <a name="reprojecting-effort"></a>Omprojektion av arbete

Projektledare ändrar ofta de ursprungliga uppskattningarna för en uppgift. Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status. Vi rekommenderar emellertid inte att projektledare ändrar baslinjenumren. Detta eftersom projektbaslinjen representerar den etablerade sanningen för projektets schema och kostnadsberäkning, och alla projektintressenter har gått med på det.

Det finns två sätt som en projektledare kan använda för att förnya arbetet för uppgifter:

- Åsidosätt standard ETC med en ny uppskattning av den faktiska resterande insatsen för aktiviteten. 
- Åsidosätt standardförlopp i procent med en ny uppskattning av det faktiska förloppen för aktiviteten.

Varje metod leder till en omberäkning av uppgiftens ETC, EAC och förloppsprocent och den planerade insatsavvikelsen för en uppgift. Procenten för EAC, ETC och förlopp för sammanfattningsuppgifterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Omprojektering av ansträngning för sammanfattningsuppgifter

Arbete för sammanfattningsuppgifter eller behållaruppgifter kan projiceras om. Oavsett om användaren återskapar projekt med hjälp av den återstående insatsen eller förloppet i procent av sammanfattningsaktiviteterna börjar följande beräkningar:

- Procentförloppet för EAC, ETC och aktiviteten beräknas.
- Nya EAC fördelas nedåt till de underordnade uppgifterna i samma proportion som original EAC var på aktiviteten.
- De nya EAC för var och en av de enskilda aktiviteterna till noderna för lövnoder beräknas. 
- De underordnade aktiviteterna som påverkas ned till lövnoder har deras ETC och förloppet omberäknas efter EAC-värdet. Detta resulterar i en ny projektion för uppgiftens insatsavvikelse. 
- EAC för de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.

### <a name="cost-tracking-view"></a>Vyn Kostnadsspårning 

I vyn **kostnadsspårning** jämförs den faktiska kostnaden som spenderades för en aktivitet med den planerade kostnaden för en aktivitet. 

> [!NOTE]
> Vyn visar endast arbetskostnader och inkluderar inga kostnader från utgiftsuppskattningarna. I Project Operations används följande formler för att beräkna spårningsmått:

- **Procent av förbrukad kostnad** : faktisk kostnad spenderad hittills ÷ uppskattad kostnad vid slutförande
- **Kostnad för att slutföra (CTC)** : planerad kostnad – den faktiska kostnaden hittills
- **EAC** : Återstående kostnad + Faktisk kostnad hittills
- **Planerad kostnadsavvikelse** : planerad kostnad – EAC

En projektion av kostnadsavvikelsen visas på uppgiften. Om EAC är större än den planerade kostnaden projiceras aktiviteten för att kosta mer än vad som ursprungligen planerades. Därför prognostiseras den över budget. Om EAC är mindre än den planerade kostnaden projiceras aktiviteten för att kosta mindre än vad som ursprungligen planerades. Därför prognostiseras den under budget.

## <a name="project-managers-reprojection-of-cost"></a>Projektledarens återprojektering av kostnaderna

När arbetsinsatsen återprojiceras räknas CTC, EAC, procent av förbrukad kostnad och planerad kostnadsavvikelse i vyn **kostnadsspårning**.

## <a name="project-status-summary"></a>Sammanfattning av projektstatus

Spåra data i **Insatsspårning** och **Kostnadsspårning** visas förloppet och kostnadsförbrukning på projektets rotnod, sammanfattningsaktiviteter och aktivitetsnivåerna på lövnodnivå. I avsnittet **status** på sidan **projektentitet** visas en översikt över status på projektnivå.

## <a name="status-summary-fields"></a>Fält för statussammanfattning

Fältet **övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status. Det använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker. I fältet **kommentarer** kan projektledaren ange kommentarer om statusen. Fältet **status uppdaterad för** är inte redigerbart och värdet är en tidstämpel som anger när status senast uppdaterades.

Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsdatumet. När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva kan du ange att dessa fält till **Före**. När schema och kostnadsavvikelse för rotnoden är negativa kan du ange dem till **Efter**.
