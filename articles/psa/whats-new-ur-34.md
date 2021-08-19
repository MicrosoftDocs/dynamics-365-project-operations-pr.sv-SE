---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 34, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009778"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 34, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 34. Den här versionen har ett versionsnummer för V3.10.55.38 och är allmänt tillgänglig via en självuppdatering i juli 2021.

## <a name="update-release-34"></a>Uppdatering version 34

### <a name="bug-fixes"></a>Felkorrigeringar
Följande problem har åtgärdats.

**Allmänt**

- Utgivarstyrda uppdateringar aktiverar inte det nya moderna godkännandearbetsflödet.
- Attributen **Målstatus** och **Åtgärdstyp** saknas på huvudsidan **Godkännandeuppsättning**.

**Tid och utgift**

- Det går inte att godkänna en återkallningsbegäran med hjälp av det moderna godkännandeflödet.
- Att kopiera en vecka med tidsposter fungerar inte när du kopierar poster som inte är relaterade till den inloggade användaren.

**Projektplanering**

- Resurstilldelningskonturer är skadade när du importerar från tillägget för stationära Microsoft Project-datorer.

**Resurshantering**

- När du publicerar ett projekt från tillägget för Microsoft Project-klienten för stationär dator ändras slutdatum för de befintliga kraven.
- Decimalprecisionen överstiger två decimaler i bekräftelsedialogen för Utöka bokningar.

**Försäljning**

- När du lägger till en produktbaserad rad med en befintlig produkt i ett projektkontrakt visas undantaget **Nyckeln finns inte i ordlistan**.
- Leads kan inte kvalificeras när en ordertyp mappas från ett lead till en affärsmöjlighet.
