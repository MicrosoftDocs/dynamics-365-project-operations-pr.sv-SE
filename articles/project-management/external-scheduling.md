---
title: Extern schemaläggning
description: I den här artikeln finns information om extern schemaläggning.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736974"
---
# <a name="external-scheduling"></a>Extern schemaläggning

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I det externa schemaläggningsläget kan du på ett enhetligt sätt skapa, uppdatera och ta bort entiteter som är relaterade till strukturer för arbete som är relaterade till arbete, men utan de aktuella begränsningarna som tillämpas av Microsoft Project for the Web. Den ger också begränsad validering. Det här läget bör endast användas av följande kunder:

- Kunder som har de verktyg som krävs för att definiera en WBS utanför schemaläggningslogiken som tillhandahålls av Project Operations
- Kunder som måste hantera schemahierarki, beroenden eller varaktighet för uppgiften

> [!IMPORTANT]
> Data som inte är korrekt angivna i WBS-relaterade entiteterna kanske inte renderas i resursrutnätet, rutnät för allokering, spårningsrutnät eller resurstilldelningsrutnät.

## <a name="configuration"></a>Configuration

Den här funktionen aktiveras som standard. Men på den medföljande huvudsidan för projekt är det relaterade fältet inte synligt som standard. För att aktivera fältet, i Maker Portal, öppna huvudsidan för projektenheten, välj fältet **Schemaläggningsmotor** och ändra sedan fältet till **Visas som standard**. Om du inte använder den färdiga projekthuvudsidan, redigera din befintliga sida och lägg till fältet **Schemaläggningsmotor** i den.

## <a name="settings"></a>Inställningar

För att använda det externa schemaläggningsläget måste du först skapa ett nytt projekt och välja **Externt schemalagt** schemaläggningsmotor i rullgardinsmenyn på projektets huvudsida. När det här läget har ställts in för ett projekt går det inte att ändra det.

## <a name="viewing-the-wbs"></a>Visa WBS

Om ett projekt är externt schemalagt är åtkomsten till Project for the Web begränsad för det projektet. För att se WBS måste du gå till spårningsrutnätet, där hela WBS visas.

## <a name="creating-and-editing-the-wbs"></a>Skapa och redigera WBS

Om extern schemaläggning har aktiverats för ett projekt måste du definiera data för alla WBS-relaterade entiteter, t.ex. uppgifter, teammedlemmar, resurstilldelningar och beroenden.

Följande bild visar datamodellen för produktschemaläggning.

![Datamodell för projektplanering.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funktionsbegränsningar

Följande åtgärder tillåts inte för externt schemalagda projekt.

### <a name="project-planning"></a>Projektplanering

- **Kopiera projekt** – Den här åtgärden stöds inte för externt schemalagda projekt.
- **Flytta projekt** – Ändringar av startdatum för ett projekt flyttar inte början på uppgifter eller resurstilldelningar i WBS.
- **Uppdatera projektledaren** – Ändringar av projektledaren på projektets huvudsida skapar inte automatiskt en ny projektteammedlem förrän projektet har konverterats.
- **Uppdatera projektets arbetstimmarsmall** – Ändringar i projektets arbetstimmarsmall beräknas inte om projektets schema.
- **Resurstilldelningsprofiler** – När du skapar resurstilldelningar uppdateras inte fältet **mdyn\_PlannedWork**. Det här fältet används för att lagra konturer för resurstilldelning. Om du visar en tidsfasad insats i resurstilldelningsrutnätet eller rutnätet för resurstilldelningar måste du definiera giltiga resurstilldelningsallokeringar. Dessa konturer måste vara korrekt formaterade så att de utlöser beräkningen av både kostnadskonturer och försäljningspriskonturer. Vi rekommenderar att du skapar ett testprojekt som schemaläggs av Project for the Web och granskar tillhörande data för att bekräfta kraven och formateringen.

### <a name="resource-management"></a>Resurshantering

- **Allmän resursuppfyllelse** – Generisk resursuppfyllelse stöds inte för externt schemalagda projekt. Om du försöker uppfylla aktiva öppna krav skapas nya projektteammedlemmar, men den generiska teammedlemmen tas inte bort eller den generiska teammedlemmen ersätts vid befintliga resurstilldelningar.
- **Ta bort teammedlem** – om en teammedlem tas bort tas inte resurstilldelningar bort automatiskt.

### <a name="quoting-and-contracting"></a>Offerter och kontraktering

- **Importera offertlinje och kontraktslinjedetaljer** – När offert- eller kontraktsradsdetaljer importeras från ett projekt har applikationen testats för att stödja maximalt endast 500 uppgifter i WBA, baserat på en gräns på 20 uppdrag per uppgift.

### <a name="actuals-and-invoicing"></a>Faktiska värden och fakturering

- Även om det inte finns några ändringar i befintliga valideringar mellan WBS och finansiella transaktioner, är det viktigt att du följer den medföljande datamodellen för att säkerställa att alla nedströmstransaktioner fungerar som förväntat.
