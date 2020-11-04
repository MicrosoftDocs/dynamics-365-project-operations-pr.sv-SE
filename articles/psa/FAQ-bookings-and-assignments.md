---
title: Resursbokningar och hur de relaterar till uppgiftstilldelningar
description: I det här ämnet finns information om hur du hanterar namngivna resurser, resursbokningar och aktivitetstilldelningar samt hur de relaterar till varandra.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085727"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Resursbokningar och hur de relaterar till uppgiftstilldelningar


Det finns två sätt som namngivna resurser bokas för ett projektteam och tilldelas projektaktiviteter:

- Resursen kan bokas direkt till ett projekt och därefter tilldelas till projektaktiviteter.
- Uppgifterna kan tilldelas en allmän resurs som sedan används för att söka och ersätta den generiska resursen med en namngiven resurs. 

I båda fallen reserveras resursens kapacitet genom bokningen av resursen.

Den projektledare som planerar projektet äger projektplan och -schema. Genom att använda den generiska resursen för tilldelning och sedan skapa en resursbegäran från den kan projektledaren boka resurser till projektet med profiler som anges i projektplanen. De kan boka resurser till ett projekt och sedan tilldela dem till aktiviteter, men det finns inget sätt att justera profiler för bokning med aktiviteternas profiler. Bokningarna påverkar inte projektschemat.

Föreställ dig ett komplext projekt med flera överlappande aktiviteter där flera resurser av samma typ behöver fungera samtidigt. Det är svårt att ändra uppgifter så att dessa passar profilerna tillhörande deras respektive diskreta uppgifter och deras ursprungliga profiler, om du anger en resursprofil som skiljer sig från summan av dess tilldelningar.

I exemplet nedan uppgår den totala insatsen som krävs av samma resurs från en uppsättning med fyra uppgifter till 62 timmar under en tvåveckorsperiod, och det finns en specifik profil. Om resursen Johan är bokad i 62 timmar under samma två veckor men med en annan profil, så är krav och bokning i enlighet med varandra.

| **Profiler för uppgift**    | **Totalt antal timmar** | Mån 6/4 | Tis 6/5 | Ons 6/6 | Tors 6/7 | Fre 6/8 | Lör 6/9 | Sön 6/10 | Mån 6/11 | Tis 6/12 | Ons 6/13 | Tors 6/14 | Fre 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Uppgift 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Uppgift 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Uppgift 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Uppgift 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Summor**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Johans tillgänglighet
| **Resursbokning** | **Totalt antal timmar** | Mån 6/4 | Tis 6/5 | Ons 6/6 | Tors 6/7 | Fre 6/8 | Lör 6/9 | Sön 6/10 | Mån 6/11 | Tis 6/12 | Ons 6/13 | Tors 6/14 | Fre 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Johan                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Det finns emellertid inget systematiskt sätt att tilldela profiler för bokade timmar till aktiviteter på en per-dag-basis. Om projektledaren är villig att ändra projektets schema så att detta passar resursens tillgänglighet måste han/hon ta bort tilldelningen och ändra alla aktiviteter så att dessa matchar bokningens profiler.

Om en organisation har tilldelat uppgiften att projektplanera till såväl en projektledare som en resursansvarig anger projektledaren schemat, inklusive en profil över erforderligt arbete. Resurshanteraren ska inte kunna påverka schemat utan projektledarens vetskap genom att ändra insatsprofiler i samband med bokning av verkliga resurser. Om resurshanteraren uppfyller något annat än vad projektledaren begärt, måste de komma överens om vilka ändringar som behövs i projektschemat.

Eftersom bokningar och tilldelningar inte är nära sammankopplade, är det möjligt att boka profiler som skiljer sig från uppgiftsprofilerna eller att ändra tilldelningar så att dessa resulterar i situationer där bokningar och tilldelningar inte längre är i harmoni med varandra.

**Avstämningsvyn** gör att projektledaren kan se bokningar och tilldelningar för respektive teammedlem i projektet. Vyn använder färger och mönster för att visa om det finns skillnader mellan bokningar och tilldelningar för teammedlemmar. Utifrån den här informationen kan projektledaren vidta rätt åtgärd i syfte att antingen utöka resursbokningar för ärenden med tilldelningar men utan bokningar, eller att avbryta bokningar där resurser har bokats men inga tilldelningar.

> [!NOTE]
> Om du flyttar en aktivitet som du själv har profilerat, så bibehålls inte profilerna. Profilerna återskapas enligt projektkalendern för att reflektera ändringar i arbetstimmar och helgdagar. Detta är avsiktligt eftersom systemet inte känner till syftet med den ursprungliga profilen och inte kan avgöra om det är rätt att behålla profilen under en ny tidsperiod. Eftersom bokningar och tilldelningar separeras behåller bokningarna de ursprungliga profilerna för bokning. I så fall måste du avbryta och omboka till den nya tilldelningsprofilen.

