---
title: Nyheter i februari 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i februari 2022-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933008"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i februari 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

*Gäller: Project Operations för resurs-/icke-lagerbaserade scenarier*

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.28.0.120
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.24

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

- I den här versionen kan du lägga till upp till 300 teammedlemmar i ett enda projekt. Tidigare var gränsen för antalet teammedlemmar 150. Mer information finns i [Projektgränser](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Mappninguppdateringar för dubbelriktad skrivning för Project Operations

I följande lista visas mappningar med dubbelskrivning som har ändrats eller lagts till i februari 2022-versionen av Project Operations.

| Entitetsmappning | Uppdaterad version | Kommentarer |
| --- | --- | --- |
| Entitet för export av projektutgifter i Project Operations-integrering (msdyn\_expenses) | 1.0.0.3 | Utökat för projektaktivitetssynkronisering med Dataverse. |

Den aktuella listan och de aktuella versionerna av Project Operations med dubbla skrivningsmappningar finns i [Project Operations-versioner med dubbla skrivningsmappningar](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade tabellkolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2415109 | Standardvärdet i fältet **Betalningsvillkor för Operations** måste vara projektets kontraktkundposten och proforma-fakturaposten. |
| Fakturering och prissättning | 2497369 | Materialkorrigeringen måste följa datumvärdet i parametrarna för **Korrigering**. |
| Fakturering och prissättning | 2498697 | Förbättrade säkerhetskonfigurationen för **Tidspoståterkallelse**. |
| Fakturering och prissättning | 2513824 | För resursbaserade scenarier får inte ID för transaktionskategori överskrida 28 tecken i Project Operations. |
| Fakturering och prissättning | 2517455 | Åtgärden **Uppdatera fakturaradstransaktioner** får inte utlösas flera gånger samtidigt för samma faktura. |
| Fakturering och prissättning | 2517465 | Åtgärden **Inaktivera fakturaradsinformation** blockeras eftersom den inte stöds. |
| Fakturering och prissättning | 2556660 | Åtgärdade kontrollerna för datumverkställning som görs i prislistan som är bifogad till en projektparameterpost. |
|   Affärsmöjlighetshantering | 2369202 | Rättade affärslogiken som bekräftar att prislistor med överlappande verkställandedatum kan kopplas till samma projektkontrakt. |
|   Affärsmöjlighetshantering | 2385965 | Rättade beteendet på fliken **Kunder** på sidan **Projektkontrakt** när du väljer **Spara och stänga**. |
| Tid och utgift | 2538503 | En projektuppgift måste vara tillgänglig i entiteten **Faktiska projektvärden** när en utgiftsrapport har publicerats. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Projektledning och redovisning | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Under importen av leverantörskreditfakturor inträffar ett fel. Felmeddelandet anger "Behållningsbeloppet får inte vara mer än återstående nettobelopp". |
| Projektledning och redovisning | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Om ett fakturaförslag innehåller transaktioner med nollbeloppsavgift som har ofakturerad försäljning kan fakturering inte ske. |
| Projektledning och redovisning | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Den bokförda kostnaden är inte korrekt efter att inköpspriset har uppdaterats och parametern **Aktivera ändringshantering** har aktiverats.|
| Projektledning och redovisning | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Bokföringsberäkningen för ett projekt med fast pris använder fel valuta och belopp i beräkningsverifikationen, även då funktionen **Aktivera projektkontraktsvaluta för uppskattningsberäkning** har aktiverats. |
| Projektledning och redovisning | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Tillägg** bör inte försöka aktivera ändringsspårning utan att registrera undantag för entiteter som har konfigurationsnycklar som inte är aktiverade. |
| Projektledning och redovisning | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Batchjobbet åtgärdas när flera avancerade journaler läggs upp och ett fel inträffar. |
| Resor och utgifter | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | På grund av ett kvittningsproblem som rör kostnader för kassaförskott i utgiftsrapporter täcks inte momsbeloppet som en del av förskottet. |
| Resor och utgifter | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Momsinformation ingår inte i rapporten **Utgifts – bokförda transaktioner**. |
| Resor och utgifter | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Brott mot utgiftspolicyn **Erforderliga kvitton** visar en varning om utgiftsrapporter. |
| Resor och utgifter | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | I en projekttransaktion ingår inte moms som inte kan återvinnas i det totala försäljningsbeloppet när transaktionen är ett resultat av utgifter för körmil. |
| Resor och utgifter | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | När en specificerad rad har moms kan du inte ändra datumet för artikelanpassningsraden, och ett tillståndsfel i källdokumentet uppstår. |

## <a name="removed-and-deprecated-features"></a>Borttagna och inaktuella funktioner

Artikeln [Borttagna och inaktuella funktioner i Project Operations](removed-depreciated-features-project.md) beskriver funktioner som har tagits bort eller gjorts inaktuella för Dynamics 365 Project Operations.

- En borttagen funktion är inte längre tillgänglig i produkten.
- En borttagen funktion befinner sig inte i aktiv utveckling och kan komma att tas bort i en kommande uppdatering.

Ett meddelande om inaktualisering kommer att visas i artikeln [Borttagna eller inaktuella funktioner i Project Operations](removed-depreciated-features-project.md) 12 månader innan någon funktion tas bort från produkten.

För icke-bakåtkompatibla ändringar som endast påverkar kompileringstiden men är binärt kompatibla med begränsade lägen och produktionsmiljöer, blir utfasningstiden kortare än 12 månader. Vanligtvis är dessa ändringar funktionsuppdateringar som måste göras till kompileraren.
