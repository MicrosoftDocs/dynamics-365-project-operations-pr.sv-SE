---
title: Översikt över schemaläggningsassistenten
description: I det här ämnet finns information om hur du arbetar med schemaläggningsassistenten för att boka resurser.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125650"
---
# <a name="schedule-assistant-overview"></a>Översikt över schemaläggningsassistenten

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Schemaläggningsassistenten används för att boka resurser baserat på de krav som projektledaren har definierat. Schemaläggningsassistenten använder de parametrar som ges i resurskravet för att hitta resursen. Schemaläggningsassistenten rekommenderar resurser som uppfyller relevanta krav, t.ex. vilka tidsfönster eller kunskaper som behövs.

När lämpliga resurser identifieras kan resursen eller projektledaren boka resursen för arbetet.

## <a name="prerequisites"></a>Förutsättningar

Schemaläggningsassistenten ingår i lösningen Universal Resource Scheduling. Lösningen ingår i och installeras med Dynamics 365 Project Operations, Dynamics 365 Field Service och Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Matchningskrav och resurser

Ett genererat resurskrav bygger på information som:

-   Egenskaper
-   Roller
-   Affärsenheter
-   Resursinställningar
-   Insatsprofiler
-   Tidszon

I schemaläggningsassistenten används dessa uppgifter för att filtrera resurser.

## <a name="launch-the-schedule-assistant"></a>Öppna schemaläggningsassistenten

Det finns två sätt att starta schemaläggningsassistenten. Om du använder hybridläget kan du välja valfri teammedlem i rutnätet med teammedlemmar med ett resurskrav som inte har uppfyllts och sedan välja **Boka**. Om du använder centralläget söker resurshanteraren efter och väljer resursen.

## <a name="schedule-assistant-filters"></a>Filter för schemaläggningsassistenten

När schemaläggningsassistenten har körts visas informationen från resurskravet som filtrerade värden i den vänstra rutan. Resurshanteraren eller projektledaren kan finjustera resultaten genom att justera filter så att det motsvarar schemaläggningsbehoven.

I filterrutan visas alternativen för arbete, t.ex.:

-   Arbetets start och slut
-   Egenskaper
-   Roller
-   Organisationsenheter
-   Resursföretag
-   Resurstyper
-   Prioriterade resurser
