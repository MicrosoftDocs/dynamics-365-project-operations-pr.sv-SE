---
title: Resurshanteringsändringar (Project Service Automation 3.x)
description: I det här ämnet finns information om ändringarna i området resurshantering.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d19b8b453c544bb4c6fd11a8b9f750cb08e0c168
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595520"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Resurshanteringsändringar (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Avsnitten i det här ämne innehåller information om de ändringar som har gjorts i området resurshantering i Dynamics 365 Project Service Automation version 3.x.

## <a name="project-estimates"></a>Projektberäkningar

I stället för att basera sig på entiteten **msdyn\_projecttask** (**Projektuppgift**), baseras projektberäkningar på entiteten **msdyn\_resourceassignment** (**resurstilldelning**). Resurstilldelningar har blivit "källan till sanningen" för schemaläggning av aktiviteter och priser.

## <a name="line-tasks"></a>Raduppgifter

I PSA 3.x är raduppgifter föråldrade (inaktuella). Tilldelningarna pekar nu på hela uppgiften i stället för på raduppgifterna.

Följande exempel visar hur en uppgift med namnet "testuppgift" tilldelas teammedlemmar A och B i tidigare versioner av PSA och PSA 3.x.

- **Före PSA 3.x:**

    - Testuppgift

        - Testuppgift – raduppgift 1

            - Tilldelning till A

        - Testuppgift – raduppgift 2

            - Tilldelning till B

- **PSA 3.x:**

    - Testuppgift

        - Tilldelning till A
        - Tilldelning till B

## <a name="unassigned-assignment"></a>Otilldelad tilldelning

I PSA 3.x är en otilldelad tilldelning en tilldelning som är tilldelad en **NULL** teammedlem och en **NULL** resurs. Tilldelningar som inte tilldelats kan ske i några situationer:

- Om en uppgift har skapats men ännu inte tilldelats någon teammedlem skapas alltid en otilldelad tilldelning. 
- Om alla tilldelningar för en uppgift tas bort, återskapas en otilldelad tilldelning för den uppgiften.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Schemaläggningsfält på entiteten för projektuppgift

Fälten i entiteten **msdyn\_projecttask** är inaktuella eller flyttade till entiteten **msdyn\_resourceassignment** eller så refereras de från entiteten **msdyn\_projectteam** (**projektteammedlem**).

| Inaktuellt fält i msdyn\_projecttask (projektuppgift) | Nytt fält i msdyn\_resourceassignment (resurstilldelning) | Kommentar |
|---|---|---|
| msdyn\_assignedresources | Ingen | |
| msdyn\_assignedteammembers | Ingen | |
| msdyn\_numberofresources | Ingen | |
| msdyn\_scheduledhours | Ingen | |
| msdyn\_effortcontour | msdyn\_plannedwork | Formatet på datastrukturen för JavaScript Object Notation (JSON) som lagras i fältet har ändrats. |

## <a name="schedule-contour"></a>Schemalägg profil

Schemalägg profil lagras i fältet **planerat arbete** (**msdyn\_plannedwork**) för varje entitet för **resurstilldelning** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktur

Den nya strukturen för schemalägg profil består av flexibla tidsintervall som definieras för varje dag i schemat. Varje tidssektor har följande egenskaper:

- **Start** – starten av arbetstimmarna för dagen enligt projektkalendern.
- **Slut** – Slutet av arbetstimmarna för dagen enligt projektkalendern.
- **Timmar** – antalet timmar som har tilldelats den dagen.

**Exempel**

I det här exemplet används en projektkalender där arbetsdagen är från 9:00 till 17:00 i UTC-8 tidszon.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatisk schemaläggning och manuell schemaläggning

Om en uppgift schemaläggs automatiskt visas timmarna och uppgiftens varaktighet kan minskas.

**Exempel**

Följande uppgift schemaläggs automatiskt i 18 timmar om tre dagar (3 december 2018 till 5 december 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Om en uppgift är manuellt schemalagd fördelas timmarna med alla datum.

**Exempel**

Följande uppgift schemaläggs manuellt i 18 timmar om tre dagar (3 december 2018 till 5 december 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Tilldelningsenhet

Tilldelningsenheten är inaktuell i PSA 3.x. Uppgiftens arbetsinsatstimmar är nu lika delade per dag, bland alla tilldelade resurser.

**Exempel**

I det här exemplet tilldelas uppgiften två resurser och schemaläggs automatiskt i 36 timmar om tre dagar (3 december 2018 till 5 december 2018).

- Tilldelning 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Tilldelning 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Prissättningsdimensioner

I PSA 3.x har resursspecifika fält för prissättningsdimensioner (t.ex. **Roll** och **Organisationsenhet**) tagits bort från entiteten **msdyn\_projecttask**. Dessa fält kan nu hämtas från motsvarande projektteammedlem (**msdyn\_projectteam**) för resurstilldelningen (**msdyn\_resourceassignment**) när projektberäkningar genereras. Ett nytt fält **msdyn\_organizationalunit** har lagts till i entiteten **msdyn\_projectteam**.

| Inaktuellt fält i msdyn\_projecttask (projektuppgift) | Fält från msdyn\_projectteam (projektteammedlem) som används i stället |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Profiler

Fälten prissättnings- och beräkningsprofil är inaktuella i entiteten **msdyn\_projecttask**. De har flyttats till entiteten **msdyn\_resourceassignment**.

| Inaktuellt fält i msdyn\_projecttask (projektuppgift) | Nytt fält i msdyn\_resourceassignment (resurstilldelning) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Följande fält har lagts till entiteten **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Följande fält för planerade, faktiska och resterande kostnader och försäljningar ändras inte i entiteten **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
