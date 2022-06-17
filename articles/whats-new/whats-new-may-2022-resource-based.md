---
title: Nyheter i maj 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i maj 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921416"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i maj 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.42.0.70
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar
### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Resurshantering | 2634019 | Förbättrade felmeddelanden för affärsvalidering när du lägger till generiska teammedlemmar som resurser. |
| Projektplanering och spårning | 2648515 | Begränsade uppdateringar av **ägar-id**, **tillstånd** och **status** i schemaläggningsentiteter. |
| Fakturering och prissättning | 2653167 | Decimalavgränsaren för rutnätet **Beräkning** måste följa formatinställningarna i **Personliga alternativ**. |
| Fakturering och prissättning| 2662251 | Värden i fälten **Korrigerad enhet** och **Enhetsgrupp** återställs när poster skapas i materialberäkningar. |
| Fakturering och prissättning| 2571408 | Ofakturerade faktiska försäljningsvärden stämplas med ett proformafaktura-ID när en utkastfaktura skapas. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services (LCS) och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
