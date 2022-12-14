---
title: Nyheter i november 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i november 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831103"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i november 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.58.0.119
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av kartan i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2781818 | Det gick inte att hitta nyckeln medan standardpriset för materialanvändningsloggen påträffades. |
| Fakturering och prissättning | 2922373 | Det går inte att länka offertrad till projekt som har stängts som förlorad offert. |
| Fakturering och prissättning | 2943206 | Fältet **Kontraktrad** i projektentiteten bör vara valfritt. |
| Fakturering och prissättning | 2953182 | Förbättra felmeddelandet för korrigeringsfakturor.|
| Fakturering och prissättning | 2959500 | Det går inte att länka offertrad till en projektuppgift som redan är associerad med en förlorad offert.|
| Fakturering och prissättning | 2959560 | Meddelandet "Den här kunden finns redan i projektkontraktet" visas när den stänger offerten som har vunnits i vissa språk. |
| Fakturering och prissättning | 3031727 | Ett fel uppstår när resurstilldelningar misslyckas msdyn_Company fältet "msdyn_Company". |
| Fakturering och prissättning | 3036905 | Att äga företag initieras aldrig i ProjectTeamMember. |
| Administrering av affärsmöjligheter | 2763519 | Null-referensfel i EnsureProjectContractAllowsUpdates. |
| Administrering av affärsmöjligheter | 2783798 | Om ett projekt importeras från en offertrad saknas uppgiftsbeskrivningar för kostnader och material.|
| Administrering av affärsmöjligheter | 2988635 | Förbättra msg-beskrivningen när kunden tas bort i offerten. |
| Administrering av affärsmöjligheter | 3001191 | Det går inte att skapa offert från Affärsmöjlighet där faktureringsmetoden har angetts som null. |
| Uppgradera | 3012324 | Projektkonverteringen misslyckades på ett projekt med kontrolltecken som Tabb i namnet. || Projektplanering och spårning | 2790384 | Timeout för den väntande OperationSet är för kort. |
| Projektplanering och spårning | 3044275 | Saknas lokalisering för: missingProjectSchedulerErrorMessage. |
| Projektplanering och spårning | 3044277 | Projektkonfigureringsrutnätet läses inte in när schemaläggaren är avfälld.|
| Resurshantering | 2943153 | Fliken Uppdatera spårning så att varaktigheten visas med två decimaler.|
| Legotillverkning | 2932774 | Felet för leverantörsfakturaraden Skrivskyddade fel felaktigt. |
| Legotillverkning | 2939556 | Status för leverantörsfakturahuvud ska inte anges till Utkast för online borttagning om det inte är aktivt. |
| Tid och utgift | 2939998 | Ny TESA-version i ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
