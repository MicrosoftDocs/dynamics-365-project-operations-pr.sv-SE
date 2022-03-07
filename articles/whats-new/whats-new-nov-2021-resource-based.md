---
title: Nyheter i november 2021 – Project Operations för resursscenarier/icke lagerbaserade scenarier
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i november 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827348"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i november 2021 – Project Operations för resursscenarier/icke lagerbaserade scenarier

*Gäller: Project Operations för resursscenarier/icke lagerbaserade scenarier*

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.26.0.145, 4.26.0.148, or 4.26.0.150
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.22

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- API:er ("application programming interfaces", programmeringsgränssnitt för applikationer) för projektplanering stöder nu möjligheten att skapa och ta bort projektgrupper.

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-in-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2240080 | Fältet **Betalningsvillkor** får inte dupliceras på pro forma-fakturan. |
| Fakturering och prissättning | 2358236 | Fakturakorrigering måste tillåta korrigeringar med nollprisrader. |
| Resurshantering | 2410072 | Tillåt konfigurering av en resurs som har tilldelats uppgiften som en projektansvarig. |
| Fakturering och prissättning | 2430234 | Åtgärda beräkningsproblem för kostnadsprestanda. |
| Tid och utgift | 2436978 | Tillåt tid att anges i tt:mm-format. |
| Fakturering och prissättning | 2448623 | Tillåt att prislistor uppdateras när de har associerats med en organisationsenhet. |
| Tid och utgift | 2460396 | Tillåt att en tidspost tas bort genom att rensa cellen. |
| Fakturering och prissättning | 2467386 | Tillåt att ett projekt med en uppgift tas bort även när uppgiften associerats med en vunnen offert. |
| Tid och utgift | 2461744 | Vyn **Mitt misslyckade godkännande** innehåller endast projektgodkännanden i stadiet **Skickad**. |
| Tid och utgift | 2464082 | Ta bort länken från projektgodkännanden till godkännandeuppsättningen när en målstatus matchas. |
| Tid och utgift | 2468108 | Jobbet Schemalägg bör inte ange statusen **Bearbetning** för godkännandeuppsättningen. |
| Tid och utgift | 2471503 | Ta bort godkännandeuppsättningar som är sju dagar gamla. |
| Fakturering och prissättning | 2480687 | Offertradsreferensen får inte tas bort när en offertradsmilstolpe skapas. |

### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Projektledning och redovisning | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Behållna leverantörsbelopp i transaktioner för projektutgifter visas inte i transaktionslistan. |
| Projektledning och redovisning | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Den koncerninterna leverantörsfakturan blir felaktig när integrering av leverantörsfaktura aktiveras. |
| Projektledning och redovisning | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Betalningsvillkoren i projektfakturor fungerar inte som förväntat. |
| Projektledning och redovisning | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | När kvarhållning av leverantörer frigörs får verifikationspubliceringen ytterligare rader som är felaktiga. |
| Projektledning och redovisning | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | När integreringsjournalen för Project Operations har publicerats misslyckas åtgärden på grund av att det saknas mått för ett konto till vilket publicering inte sker. |
| Projektledning och redovisning | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Fliken **Projekt** kan inte redigeras på en väntande leverantörsfaktura när kategorin för inköp tilldelas objektet. |
| Projektledning och redovisning | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigeringsfönstret saknas om du inte är inloggad i Project Operations Dataverse. |
| Projektledning och redovisning | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | När du publicerar omsättning från en projektfaktura i ett tillämpat retainer-ärende uppstår ett problem eftersom transaktioner på verifikationen inte är i balans. |
| Projektledning och redovisning | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Skapande av en beräkning efter att du har publicerat ett fakturaförslag blockerar korrigeringsrader från att importas. |
| Projektledning och redovisning | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Ändringar av en helt fakturerad milstolpepost bör inte vara möjliga. |
| Resor och utgifter | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alla utgiftsrapporter visas när du söker efter en kategori i mobilappen Utgifter. |
| Resor och utgifter | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Felaktiga belopp för leverantörs- och momstransaktioner publiceras från en utgift som skapats från en kreditkortstransaktion. |
| Resor och utgifter | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | En irrelevant varning inträffar när du uppdaterar sidan **Utgiftsrapport**. |
| Resor och utgifter | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Fel tillfällig godkännare används när du tar bort en tillfällig godkännare och sedan skickar en utgiftsrapport via arbetsflödet igen. |
| Resor och utgifter | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ett publiceringsfe relaterat till konfigurationen för körsträcka uppstår. |
