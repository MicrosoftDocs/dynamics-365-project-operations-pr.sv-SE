---
title: Nyheter i augusti 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i augusti 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348029"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i augusti 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.45.0.53
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
|   Affärsmöjlighetshantering | 2762089 | Felhantering vid stängning av kontraktet som förlorat om automatisk spara är inaktiverat i organisationen.|

### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services (LCS) och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).