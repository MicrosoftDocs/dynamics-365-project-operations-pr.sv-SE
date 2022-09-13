---
title: Nyheter i juli 2022 – Project Operations för resurs/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i juli 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403974"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i juli 2022 – Project Operations för resurs/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.44.0.22
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Distribution och konfiguration | 2761472 | Ett installationsfel för Project Operations hanteras. |
| Fakturering och prissättning | 2746940 | Namnet på undermappsraden ska ha maximal längd på 100 tecken. |
| Fakturering och prissättning | 2739162 | Kunderna måste kunna se menyfliksknappar i rutnätsvyn för faktiska värden. |
| Projektplanering och spårning | 2730318 | Uppdaterad validering för tecken som inte stöds i projektämnet. |
| Fakturering och prissättning | 2705361 | Faktiska milstolpefakturerade försäljningssiffror måste tas med i projektspårningsfälten. |
| Fakturering och prissättning | 2675880 | Förhindra att ett projekt länkas till en kontraktrad som inte är arbetsbaserad. |
| Fakturering och prissättning | 2664396 | Om en offertprislista sparas utan en offert måste det finnas ett felmeddelande om att offerten inte kan vara tom. |
| Fakturering och prissättning | 2184019 | Fliken **Uppgiftsbaserad fakturering** ska inte visas för projekt som inte har något uppbackningskontrakt eller någon offert. |
| Tid och utgift | 2754459 | När återkommande schemaläggningsmolnflöde är inaktivt, visa banderoll och kringgå asynkron bearbetning. |
| Fakturering och prissättning | 2724391 | Fel undantag kastas när ett projektkontraktets regel för delad fakturering saknar ett kundvärde. |
| Fakturering och prissättning | 2708638 | Posten hittades inte när du sökte med rutnätssökning i Materialanvändningar och Godkännanden för materialanvändningar.|
| Fakturering och prissättning | 2686977 | Förhindra validering av fakturarad när fakturan skapas. |
| Fakturering och prissättning | 2683032 | Kopiering av debiterbara roller och kategorier kan inte skalas längre än 5 000 poster.|
| Fakturering och prissättning | 2673363 | Kostnadsanvändningen i % för Projekt blir skadad när det finns både uppskattningar och utfall för Insats och Utgift för ett projekt. |

### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services (LCS) och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktioner aktiveras som standard i kommande version

Följande tabeller listar de funktioner som aktiveras som standard i version 10.0.29. De flesta funktioner som har aktiverats automatiskt kan inaktiveras i [Funktionshantering](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). I framtiden kan vissa funktioner som har aktiverats automatiskt tas bort från funktionshanteringen och bli obligatoriska. Den här förändringen säkerställer att kunderna använder aktuella funktioner så att förbättringarna kan bygga på den aktuella funktionen när de läggs till. Funktioner aktiveras aldrig automatiskt på mindre än ett år, såvida de inte är nödvändiga.

| Funktionsnamn | Aktiveringsdatum | Funktion som lagts till | Funktionens tillstånd | Modul |
| --- | --- | --- |--- |--- |
| Aktivera justering av timtransaktioner baserat på ändring av regelallokering för regel för regel | 16 september 2022 | 7 oktober 2020 | På som standard | Projektledning och redovisning |
| Funktion för förbetald faktura för projektorder | 16 september 2022 | 6 oktober 2021 | På som standard | Projektledning och redovisning |
| Ta bort fakturaförslagsrader när du använder Project Operations för resursbaserade/icke-lagerbaserade scenarier | 16 september 2022 | 6 oktober 2021 | På som standard | Projektledning och redovisning |
| Justera redovisning för en bokförd projekttransaktion | 16 september 2022 | 10 maj 2020 | På som standard | Projektledning och redovisning |
| Aktivera standardinställningar för redovisning av projekt | 16 september 2022 | 19 februari 2020 | På som standard | Projektledning och redovisning |
| Aktivera flera kontraktrader för ett projekt | 16 september 2022 | 29 juni 2020 | På som standard | Projektledning och redovisning |
| Gör journaler för projekttimmar skrivskyddade om aktuell godkännandestatus inte tillåter redigering | 16 september 2022 | 6 oktober 2021 | På som standard | Projektledning och redovisning |
| Aktivera synkroniseringsförsäljningsrader från inköpsrader när köprader uppdateras och parametern för hantering av köporderändring är aktiverad | 16 september 2022 | 7 oktober 2020 | På som standard | Projektledning och redovisning |
| Aktivera Project Operations på Dynamics 365 Customer Engagement | 16 september 2022 | 29 juni 2020 | På som standard | Projektledning och redovisning |
| Funktion för korrigering av projekttransaktioner | 16 september 2022 | 13 juli 2020 | På som standard | Projektledning och redovisning |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funktioner som blir obligatoriska i den kommande versionen

Följande tabeller listar de funktioner som är obligatoriska från version 10.0.29 och framåt.

| Funktionsnamn | Aktiveringsdatum | Funktion som lagts till | Funktionens tillstånd | Modul |
| --- | --- | --- | --- | --- |
| Beräkna det bekräftade värdet baserat på källan för källan utan att avrunda växelkursen | 16 september 2022 | 14 juni 2020 | Obligatorisk | Projektledning och redovisning |
| Aktivera bokföring av projektjustering med samma huvudbokskonto som den ursprungliga transaktionen | 16 september 2022 | 14 juni 2020 | Obligatorisk | Projektledning och redovisning |
| Uppgift om godkänt belopp för projektkontrakt | 16 september 2022 | 31 augusti 2019 | Obligatorisk | Projektledning och redovisning |
| Aktivera sortering efter resurs under skapandet av projektfakturaförslag | 16 september 2022 | 31 augusti 2019 | Obligatorisk | Projektledning och redovisning |
