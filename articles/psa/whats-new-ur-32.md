---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 32, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129688"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 32, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 32. Den här versionen har versionsnummer V3.10.53.108 och är allmänt tillgänglig via en självuppdatering i juni 2021.

## <a name="update-release-32"></a>Uppdatering version 32

### <a name="bug-fixes"></a>Felkorrigeringar

#### <a name="general"></a>Allmänt

- Om en större uppgradering misslyckas bör endast huvudprogrammets ingångspunkter blockeras för att se till att delade entiteter fortfarande är tillgängliga.

#### <a name="time-and-expense"></a>Tid och utgift

Följande problem har åtgärdats:

- **TimeEntriesImportFromResourceAssignment** upprätthåller inte start- och sluttiderna för resurstilldelningsutsnittet.
- Om du väljer **Öppna post** i rutnätet **Tidspost** kan det hända att du inte kan välja andra formulär.
- När du importerar tilldelningar till tidsposter kan klientkodsfrågan skapa en lång URL som misslyckas.
- I rutnätet **Tidspost**, när ett värde har tagits bort från en cell, förblir inte fokus i rutnätet.
- Knappen **Avvisa** har tagits bort från vyn **Bearbetar godkännanden** för moderna godkännanden.
- Stabilitet och prestanda för godkännande av tidsposter i bulk påverkas av deadlock och ett fel i att korrekt hantera anpassningar som är relaterade till entiteten **Tidspost**.

#### <a name="project-planning"></a>Projektplanering

- Ett null-referensundantag skapas när du uppdaterar ett projekt som har ett null-värde i fältet **Upphandlande enhet**.
- **Uppdatera projektsummor** beräknar felaktigt den återstående kostnaden och återstående försäljning i ett projekt.
- Överflödiga prisberäkningar påverkar prestanda för uppdateringar av resurstilldelningar.

#### <a name="resource-management"></a>Resurshantering

Följande problem har korrigerats:

- När en bokningsbar resurs kalenderkapacitet är fler än 1 identifierar Project Service Automation felaktigt kapaciteten som 0 (noll). Därför uppstår en oändlig loop i schemavyn.

#### <a name="sales"></a>Försäljning

Följande problem har åtgärdats:

- När en journalrad skapas som har en anpassad transaktionstyp sker följande nullreferensundantag: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Roller och kategorier som inaktiveras innan en offert kopieras ska inte läggas till i debiterbara roller och kategorier för den nyligen kopierade offerten.
- Dokumentdatum och redovisningsdatum justeras inte mot startdatumet som anges på en fakturaradsdetalj som skapas direkt på en utkastfaktura.
- Null-referensundantag skapas i scenarier som är relaterade till inaktivering av roller och kategorier innan en offert kopieras.
- Åtgärden **Uppdatera priser** på sidan **Projekt** uppdaterar inte utgiftsberäkningar och materialberäkningar.
