---
title: Nyheter oktober 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i oktober 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806654"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter oktober 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.57.0.176
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.30

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

| Funktionsområde | Funktionsnamn | Mer information |
| --- | --- | --- |
| Projektplanering och spårning | **Project Operations extern schemaläggning**<br>I det externa schemaläggningsläget kan kunder på ett enhetligt sätt skapa, uppdatera och ta bort entiteter som är relaterade till strukturer för arbete (WBS) med de inbyggda API:erna för Dataverse som är relaterade till arbete, men utan de aktuella begränsningarna som tillämpas av Project for the Web. | [Extern schemaläggning](/dynamics365/project-operations/project-management/external-scheduling) |
| Distribution och konfiguration | <p>**Tillåt kunder att välja distributionstyp**<br>Produktdrivna uppdateringar (PDF-enheter) av Project Operations används för att automatiskt installera Project Operations lösning för dubbelriktad skrivning och orkestrering installeras i miljön.</p><p>Den här funktionen introducerar en ny parameter för **Beteende för lösningsuppgradering** i Projektparametrar. När denna parameter är inställd på **endast Lite**, kommer PUD inte längre automatiskt installera lösningen för dubbelriktad skrivning och orkestrering i Project Operations installeras i miljön. Detta beteende gagnar kunder som planerar att använda lösningar för dubbelriktad skrivning för att integrera försäljningsorder i appar för ekonomi och drift, men som vill använda Project Operations i Lite-läge (d.v.s. utan integrering i appar för ekonomi och drift).</p> | |
| Fakturering och prissättning | <p>**Valutakonvertering för icke-fakturerad försäljningstransaktion i integrerade miljöer**<br>För kunder som använder Project Operations som är integrerade med appar för ekonomi och drift (d.v.s. i distributionstypen resurs/icke-lagrad distribution) behärskar vanligtvis växelkurserna i appar för ekonomi och drift. Men om en utgiftskategori ska prissättas med hjälp av prisberäkningsmetoden "mot kostnad" eller "påläggspris", när kunden faktureras, används växelkursen i inte växelkurserna från appar för ekonomi och drift för den växelkurs i Dataverse som används vid beräkning av försäljningsbeloppet.</p><p>Den här funktionen introducerar en ny parameter för **Valutakonverteringsbeteende** i Projektparametrar. När denna parameter är inställd på **Utökat med reserv till**, ofakturerade försäljningsbelopp på utgiftstransaktioner beräknas med hjälp av växelkurserna från appar för ekonomi och drift.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2316317 | Systemet tillåter att fakturor skapas utan debiteringsbar transaktioner. |
| Fakturering och prissättning | 2737300 | Verifiera att fältet **Kund** är tillgängligt innan formuläret nås. |
| Fakturering och prissättning | 2744948 | Lägg till en null-kontroll för faktureringsmetoden. |
| Fakturering och prissättning | 2763515 | Null-referensfelshanterare när försäljningskontraktet för fakturan saknas. |
| Fakturering och prissättning | 2844301 | Det går inte att skapa batchfaktura på grund av ett fel. |
| Fakturering och prissättning | 2845869 | Felaktig lagring av organisationstjänst. |
| Fakturering och prissättning | 2853729 | Roll- och prisinformation uppdateras när faktureringstyp ändras. |
| Fakturering och prissättning | 2940350 | När faktiska värden prissätts ska endast aktiva prislistor anges automatiskt. |
| Distribution och konfiguration | 3001206 | Den msdyn\_replaylogheader-entiteten förhindrar uppgraderingar av kundorganisationer. |
| Administrering av affärsmöjligheter | 2755582 | Null-referensundan undantag hanteras i hjälp en delad faktureringsregel. |
| Administrering av affärsmöjligheter | 2761477 | När delningsfakturering används innebär borttagningen av en milstolpe (rubrik) att milstolpen blir överbliven. |
| Administrering av affärsmöjligheter | 2767595 | När en materialanvändningspost öppnas i huvudformuläret ändras den bokningsbara resursen för posten till den inloggade användaren. |
| Projektplanering och spårning | 2790384 | Timeout för den väntande OperationSet är för kort. |
| Projektplanering och spårning | 2957840 | Uppgifter kan inte sparas och kolumner kan inte läggas till på sidan **Uppgifter** i Integrerade Project Operations. |
| Resurshantering | 2751560 | Inkonsekventa organisationsenheter i resurskraven. |
| Legotillverkning | 2853245 | Om du matchar leverantörens fakturarad uppdateras inte verifieringsstatusen om en kontraktrad redan är länkad till leverantörens fakturarad. |
| Legotillverkning | 2907231 | Processtadiet för leverantörsfakturor kan inte avancera. |
| Tid och utgift | 2867363 | Poster faller inte ur vyn Frånvaro/Semester för godkännande när de står i kö för godkännande. |
| Tid och utgift | 2894405 | TESA: Den oanvända POC-katalogen orsakar problem med överensstämmelse. |

### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
