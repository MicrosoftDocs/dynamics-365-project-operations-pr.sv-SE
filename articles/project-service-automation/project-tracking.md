---
title: Projektstatus och kostnadsförbrukning
description: I det här ämnet finns information om hur du spårar projektstatus och kostnadsförbrukning.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756274"
---
# <a name="project-progress-and-cost-consumption"></a>Projektstatus och kostnadsförbrukning

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Behovet av att följa upp statusen för ett schema varierar efter bransch. Vissa branscher spårar på en detaljerad nivå, medan andra branscher spårar på en högre nivå. I det här ämnet illustreras hur du schemalägger för att uppfylla organisationens krav.

## <a name="effort-tracking-view"></a>Insatsspårningsvy

Vyn **Insatsspårning** spårar förloppet för aktiviteterna i schemat. Den jämför de faktiska insatstimmarna som lagts på en uppgift till de planerade insatstimmarna för den uppgiften. I PSA används följande formler för att beräkna spårningsmått:

- Förloppsprocent = faktiska insatsen till dagens datum ÷ planerad insats för uppgiften 
- Uppskattning för att slutföra (ETC) = planerad insats – den faktiska insatsen hittills 
- Uppskattning för att slutföra (EAC) = planerad insats + den faktiska insatsen hittills 
- Planerad insatsavvikelse = planerat arbete – EAC

PSA visar en projektion av insatsavvikelsen för uppgiften. Om EAC är större än den planerade ansträngningen projiceras aktiviteten för att ta längre tid än vad som ursprungligen planerades. Det ligger därför bakom schemat. Om EAC är mindre än den planerade ansträngningen projiceras aktiviteten för att ta kortare tid än vad som ursprungligen planerades. Det ligger därför framför schemat.

## <a name="re-projecting-effort"></a>Omprojektion av arbete

Det är vanligt att projektledaren ändrar de ursprungliga uppskattningarna för en aktivitet. Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status. Vi rekommenderar dock inte att projektledare ändrar baslinjenumren, eftersom projektbaslinjen representerar den etablerade sanningen för projektets schema och kostnadsberäkning, och alla projektintressenter har gått med på det.

Det finns två sätt som en projektledare kan använda för att förnya arbetet för uppgifter:

- Åsidosätt standard ETC med en ny uppskattning av den faktiska resterande insatsen för aktiviteten. 
- Åsidosätt standardförlopp i procent med en ny uppskattning av det faktiska förloppen för aktiviteten.

Var och en av dessa är en omberäkning av aktivitetens ETC, EAc och förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, ETC och förloppsprocent för sammanfattningsaktiviteterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Omprojektering av ansträngning för sammanfattningsuppgifter

Arbete för sammanfattningsuppgifter eller behållaruppgifter kan projiceras om. Oavsett om användaren återskapar projekt med hjälp av den återstående insatsen eller förloppet i procent av sammanfattningsaktiviteterna börjar följande beräkningar:

- Procentförloppet för EAC, ETC och aktiviteten beräknas.
- Nya EAC fördelas nedåt till de underordnade uppgifterna i samma proportion som original EAC var på aktiviteten.
- De nya EAC för var och en av de enskilda aktiviteterna till noderna för lövnoder beräknas. 
- De underordnade aktiviteterna som påverkas ned till lövnoder har deras ETC och förloppet omberäknas efter EAC-värdet. Detta resulterar i en ny projektion för uppgiftens insatsavvikelse. 
- EAC för de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.

### <a name="cost-tracking-view"></a>Vyn Kostnadsspårning 

I vyn **kostnadsspårning** jämförs den faktiska kostnaden som spenderades för en aktivitet med den planerade kostnaden för en aktivitet. 

> [!NOTE]
> Vyn visar endast arbetskostnader och inkluderar inga kostnader från utgiftsuppskattningarna. 

I PSA används följande formler för att beräkna spårningsmått:

- Procent av förbrukad kostnad = faktisk kostnad spenderad hittills ÷ planerad kostnad för uppgiften
- Kostnad för att slutföra (CTC) = planerad kostnad – den faktiska kostnaden hittills
- EAC = CTC + faktisk kostnad hittills
- Planerad kostnadsavvikelse = planerad kostnad – EAC

En projektion av kostnadsavvikelsen visas på uppgiften. Om EAC är större än den planerade kostnaden projiceras aktiviteten för att kosta mer än vad som ursprungligen planerades. Därför prognostiseras den över budget. Om EAC är mindre än den planerade kostnaden projiceras aktiviteten för att kosta mindre än vad som ursprungligen planerades. Därför prognostiseras den under budget.

## <a name="project-managers-re-projection-of-cost"></a>Projektledarens återprojektering av kostnaderna

När arbetsinsatsen återprojiceras räknas CTC, EAC, procent av förbrukad kostnad och planerad kostnadsavvikelse i vyn **kostnadsspårning**.

## <a name="project-status-summary"></a>Sammanfattning av projektstatus

Spåra data i **Insatsspårning** och **Kostnadsspårning** visas förloppet och kostnadsförbrukning på projektets rotnod, sammanfattningsaktiviteter och aktivitetsnivåerna på lövnodnivå. I avsnittet **status** på sidan **projektentitet** visas en översikt över status på projektnivå.

## <a name="status-summary-fields"></a>Fält för statussammanfattning

Fältet **övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status. Det använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker. I fältet **kommentarer** kan projektledaren ange kommentarer om statusen. Fältet **status uppdaterad för** är inte redigerbart och värdet är en tidstämpel som anger när status senast uppdaterades.

Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsdatumet. När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva kan du ange att dessa fält till **Före**. När schema och kostnadsavvikelse för rotnoden är negativa kan du ange dem till **Efter**.
