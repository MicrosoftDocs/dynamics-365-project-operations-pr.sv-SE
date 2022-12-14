---
title: Nya oktober 2022 – Distribution av Project Operations Lite
description: Denna artikel innehåller information om de kvalitetsuppdateringar som är tillgängliga i distributionsversionen av Microsoft Dynamics 365 Project Operations lite för oktober 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806655"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Nya oktober 2022 – Distribution av Project Operations Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.57.0.176

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

| Funktionsområde | Funktionsnamn | Mer information |
| --- | --- | --- |
| Projektplanering och spårning | **Project Operations extern schemaläggning**<br>I det externa schemaläggningsläget kan kunder på ett enhetligt sätt skapa, uppdatera och ta bort entiteter som är relaterade till strukturer för arbete (WBS) med de inbyggda API:erna för Dataverse som är relaterade till arbete, men utan de aktuella begränsningarna som tillämpas av Project for the Web. | [Extern schemaläggning](/dynamics365/project-operations/project-management/external-scheduling) |
| Distribution och konfiguration | <p>**Tillåt kunder att välja distributionstyp**<br>Produktdrivna uppdateringar (PDF-enheter) av Project Operations används för att automatiskt installera Project Operations lösning för dubbelriktad skrivning och orkestrering installeras i miljön.</p><p>Den här funktionen introducerar en ny parameter för **Beteende för lösningsuppgradering** i Projektparametrar. När denna parameter är inställd på **endast Lite**, kommer PUD inte längre automatiskt installera lösningen för dubbelriktad skrivning och orkestrering i Project Operations installeras i miljön. Detta beteende gagnar kunder som planerar att använda lösningar för dubbelriktad skrivning för att integrera försäljningsorder i appar för ekonomi och drift, men som vill använda Project Operations i Lite-läge (d.v.s. utan integrering i appar för ekonomi och drift).</p> | |

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2316317 | Systemet tillåter att fakturor skapas utan debiteringsbar transaktioner. |
| Fakturering och prissättning | 2737300 | Verifiera att fältet Kund är tillgängligt innan formuläret nås. |
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
| Resurshantering | 2751560 | Inkonsekventa organisationsenheter i resurskraven. |
| Legotillverkning | 2907231 | Processtadiet för leverantörsfakturor kan inte avancera. |
| Tid och utgift | 2867363 | Poster faller inte ur vyn Frånvaro/Semester för godkännande när de står i kö för godkännande. |
| Tid och utgift | 2894405 | TESA: Den oanvända POC-katalogen orsakar problem med överensstämmelse. |
