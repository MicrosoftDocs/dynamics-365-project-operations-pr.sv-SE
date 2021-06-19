---
title: Vad är nytt i maj 2021 - Lite-distribution för Project Operations
description: Det här ämnet innehåller information om kvalitetsuppdateringarna som är tillgängliga i maj 2021-versionen av Lite-distribution för Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060455"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Vad är nytt i maj 2021 - Lite-distribution för Project Operations

_Gäller: Lite-distribution - avtal till proforma-fakturering_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

   - Project Operations i Dataverse-miljöversion 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- [Schemaläggningslägen](../../project-management/scheduling-modes.md): Projektledare kan nu definiera om ett projekt bör hanteras med en fast varaktighet, fast arbete eller fasta enheter.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2224568 | Lade till logik för att aktivera anpassningar som omfattar plugin-programmet för fakturabekräftelsen. |
| Fakturering och prissättning | 2101098 | Förbättrade logiken för standardfälten för proforma-faktura. Dessa fält inbegriper **Faktureringsadress**, **Faktureringsnamn** och **Betalningsvillkor**. Fälten kommer nu att visas som standard i motsvarande projektkontraktskundpost. |
| Fakturering och prissättning | 2021413 | Uppdaterade fälten **Faktisk kostnad** och **Försäljning** i entiteten **Uppgift** för att inkludera försäljningsvärden från ofakturerade och fakturerade kostnader för uppgifter. |
| Fakturering och prissättning | 2182110 | När du kopierar ett projektkontrakt återskapas kontraktrads-ID:t i målprojektkontraktet så att det är unikt. |
| Administrering av affärsmöjligheter | 2186741 | Lade till valideringar för att säkerställa att fältet **Ursprung** och transaktionstyp inte kan uppdateras om befintliga detaljer för offertrader. |
| Administrering av affärsmöjligheter | 2191353 | Skapande av milstolpar får inte tillåtas på en tids- och materialkontraktrad. |
| Administrering av affärsmöjligheter | 2216956 | Åtgärdade problem med **Uppdatera priser**. |
| Planering och spårning | 2182979 | Projektkopieringsfunktionen har förbättrats så att utläggsberäkningsraderna kopieras från det ursprungliga projektet. |
| Planering och spårning | 2184144 | Projektkopieringsfunktionen har förbättrats så att resurspositionens namn kopieras från det ursprungliga projektet. |
| Planering och spårning | 2184799 | Skärpte kontrollen vid kopiering av ett projekt för att säkerställa att det uppskattade startdatumet inte kan ändras när kopieringen pågår. |
| Planering och spårning | 2185134 | Under kopieringen av ett projekt anges beräknat startdatum för målprojektet till dagens datum. |
| Planering och spårning | 2196373 | Kontrollera att projektansvarig- och teammedlemsposter inte dupliceras i projektteamet vid kopiering av ett projekt. |
| Planering och spårning | 2211833 | Resurstilldelningar kopieras från källprojektuppgiften till målprojektet. |
| Planering och spårning | 2186541 | Åtgärdade problem i rutnätet **Beräkningar** när du grupperar efter **Resurs**. |
| Planering och spårning | 2166906 | Transaktionskategorin från en uppgift måste kopieras till entiteten **Resurstilldelning**. |
| Resurshantering | 2125362 | Åtgärdade problem med att skapa en generisk teammedlem med en timbaserad allokeringsmetod. |
| Tid och utgift | 2113603 | Åtgärdade det anpassningsrelaterade problemet genom att ta bort attribut från sidan **Tidspost**. Systemet kontrollerar om attributet finns på sidan innan det går att komma attributet med hjälp av ett skript. |
| Tid och utgift | 2204377 | Kopierade tidsscheman måste visas automatiskt när du väljer **Kopiera vecka**. |
| Tid och utgift | 2209059 | Fältet **Status** kan redigeras för Dynamics 365 Field Service-tidsposter. |
