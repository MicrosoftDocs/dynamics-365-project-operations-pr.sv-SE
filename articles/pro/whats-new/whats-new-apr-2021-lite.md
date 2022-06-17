---
title: Vad är nytt i april 2021 - Lite-distribution för Project Operations
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i distributionsversionen av Project Operations Lite för april 2021.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 987eeaf2e57659a6facae6b0a3688f15992e8bb9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931261"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Vad är nytt i april 2021 - Lite-distribution för Project Operations

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Denna artikel gäller följande Dynamics 365 Project Operations komponenter och versioner:

  - Project Operations i Dataverse-miljöversion 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- Material som inte är i lager för projekt. Viktiga funktioner är:
  - Uppskatta och prissätta icke lagrade material under försäljningscykeln för ett projekt. För mer information, se [Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Spåra användning av icke-lagermaterial under projektleveransen. För mer information, se [Registrera materialanvändning för projekt och projektuppgifter](../../material/material-usage-log.md).
  - Fakturera kostnader för använt icke-lagermaterial. Mer information finns i [Hantera eftersläpad fakturering - Lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nya API:er i Dynamics 365 Dataverse tillåter att åtgärder skapas, uppdateras och tas bort med **Schemaläggningsentiteter**. För mer information, se [Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2224568 | Lade till logik för att aktivera anpassningar som omfattar plugin-programmet för fakturabekräftelsen. |
| Fakturering och prissättning | 2101098 | Förbättrad logiken för standardfält till proforma-faktura: **Faktureringsadress**, **Faktureringsnamn** och **Betalningsvillkor** nu standard från motsvarande projektkontrakts kundpost. |
| Fakturering och prissättning | 2021413 | Uppdaterade fälten **Faktisk kostnad** och **Försäljning** i entiteten **Uppgift** för att inkludera försäljningsvärden från obelagda och fakturerade kostnader för uppgifter. |
| Fakturering och prissättning | 2182110 | När du kopierar ett projektkontrakt återskapas kontraktrads-ID:t i målprojektkontraktet så att det är unikt. |
| Administrering av affärsmöjligheter | 2186741 | Lade till valideringar för att säkerställa fältet **Ursprung** och **Transaktionstyp** kan inte uppdateras om befintliga detaljer för offertrader. |
| Administrering av affärsmöjligheter | 2191353 | Milstolpar får inte skapas på en tids- och materialkontraktrad. |
| Administrering av affärsmöjligheter | 2216956 | Åtgärdade problem med **Uppdatera priser**. |
| Planering och spårning | 2182979 | Projektkopieringsfunktionen har förbättrats så att utläggsberäkningsraderna kopieras från det ursprungliga projektet. |
| Planering och spårning | 2184144 | Projektkopieringsfunktionen har förbättrats så att resurspositionens namn kopieras från det ursprungliga projektet. |
| Planering och spårning | 2184799 | Projektkopia: Kontroll som är försedd med syfte att säkerställa att det uppskattade startdatumet inte kan ändras medan kopiering pågår. |
| Planering och spårning | 2185134 | Projektkopia: Beräknat startdatum för målprojektet har angetts till dagens datum. |
| Planering och spårning | 2196373 | Projektkopia: Kontrollera att projektansvarig- och teammedlemsposter inte dupliceras i projektteamet. |
| Planering och spårning | 2211833 | Projektkopia: Resurstilldelningar kopieras från källprojektuppgiften till målprojektet. |
| Planering och spårning | 2186541 | Åtgärdade problem i rutnätet **Beräkningar** när du grupperar efter resurs. |
| Planering och spårning | 2166906 | Transaktionskategorin från en uppgift måste kopieras till entiteten **Resurstilldelning**. |
| Resurshantering | 2125362 | Åtgärdade problem med att skapa en generisk teammedlem med en timbaserad allokeringsmetod. |
| Tid och utgift | 2113603 | Åtgärdade det anpassningsrelaterade problemet genom att ta bort attribut från sidan **Tidspost**. Nu kontrollerar systemet om attributet finns på sidan innan det går att komma åt dem med hjälp av ett skript. |
| Tid och utgift | 2204377 | Kopierade tidsscheman måste visas automatiskt när du väljer **Kopiera vecka** under tidsposten. |
| Tid och utgift | 2209059 | Fältet **Status** kan redigeras för Dynamics 365 Field Service tidsposter. |
