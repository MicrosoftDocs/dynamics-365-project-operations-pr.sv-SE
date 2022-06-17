---
title: Nyheter i mars 2022 – Distribution av Project Operations lite
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i distributionsversionen av Project Operations Lite för mars 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934250"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Nyheter i mars 2022 – Distribution av Project Operations lite

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.30.0.99

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

- Underleverantör: Skapa och matcha leverantörsfakturaupplevelser

## <a name="quality-updates"></a>Kvalitetsuppdateringar

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Tid och utgift | 2388011 | Visa avvisningskommentarer till inskickare av tidsposter vid massgodkännande. |
| Projektplanering och spårning | 2495294 | Projektinformationen får inte vara redigerbar på sidan **Uppgiftsinformation**. |
| Fakturering och prissättning | 2499605 | Kontraktmilstolpar som skapas från offertmilstolpar är felaktigt markerade som skrivskyddade. |
| Projektplanering och spårning | 2506050 | Åtgärdsuppsättningen förblir väntande i en timme om det inte finns någon ändring att spara. Uppsättningen markeras sedan felaktigt som **Misslyckad** istället för att slutföras omedelbart. |
| Fakturering och prissättning | 2507401 | Standardmässiga kontrakteringsenheter anges felaktigt i projekt på grund av fel i cachelagring. |
| Fakturering och prissättning | 2541660 | **Validering av generering av försäljningsorder** i dubbelskrivning bör endast användas för projektbaserade order. |
| Fakturering och prissättning | 2552745 | Moms delas inte upp mellan kunder som har konfigurerat delade faktureringsregler. |
| Fakturering och prissättning | 2558859 | Bättre felmeddelanden när prissättningsmått konfigureras. |
| Fakturering och prissättning | 2558933 | **Importera från projektberäkningar** misslyckas när **msdyn\_project** läggs till som prissättningsmodell. |
| Fakturering och prissättning | 2559101 | Borttagning av projektparameter blockeras inte och förorsakar problem. |
|   Affärsmöjlighetshantering | 2570390 | Plugin-programmet med dubbelskrivning gör att kontotypen för offerter, order och affärsmöjligheter måste vara **Kund**, även när kontotypen inte är korrekt. |
| Fakturering och prissättning | 2586097 | Faktiska värden för delad kostnad återförs inte när ett projekt tas bort från en projektkontraktrad. |
| Fakturering och prissättning | 2589619 | Moms på oregistrerade material sprids till ofakturerad faktisk försäljning och till fakturan. |
|   Affärsmöjlighetshantering | 2594015 | En offert kan inte stängas som "vunnen" för kunder som har betalningsvillkoren **Net60**. |
| Projektplanering och spårning | 2595841 | I Project for the Web får användarna ett felmeddelande om att **msdyn\_actualstart** saknas när de skapar en ny resursbegäran. |
| Tid och utgift | 2602511 | Fältet **Avvisades av** för tidsposter visar **System** istället för en namngiven användare som avvisare. |
| Tid och utgift | 2602528 | En projektgodkännare kan godkänna tid för projekt där de inte anges som godkännare. |
| Fakturering och prissättning | 2608550 | En korrigeringsfaktura kan bekräftas även om originalversionen inte ändrats. |

## <a name="removed-and-deprecated-features"></a>Borttagna och inaktuella funktioner

Artikeln [Borttagna och inaktuella funktioner i Project Operations](../../whats-new/removed-depreciated-features-project.md) beskriver funktioner som har tagits bort eller gjorts inaktuella för Dynamics 365 Project Operations.

- En borttagen funktion är inte längre tillgänglig i produkten.
- En borttagen funktion befinner sig inte i aktiv utveckling och kan komma att tas bort i en kommande uppdatering.

Ett meddelande om inaktualisering kommer att visas i artikeln [Borttagna eller inaktuella funktioner i Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 månader innan någon funktion tas bort från produkten.
