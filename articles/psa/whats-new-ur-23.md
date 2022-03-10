---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 23, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996638"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation uppdateringsversion 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 23. Den här versionen har versionsnummer V 3.10.34.30 och är allmänt tillgänglig via en självuppdatering i augusti 2020.

## <a name="update-release-23"></a>Uppdatering version 23

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:
- Hantera edge-ärende i **ta bort projektteammedlem** om du vill ge ett meningsfullt undantag.
- Tilldelningsimporten resulterar i en tom borttagningssida.

**Resurshantering**

Följande problem har åtgärdats:

- **Resurskortet för rutnät för resursutnyttjande** visar felaktiga data när tidsskalan är längre än fem dagar.
- När en kund skapar en bokningsbar resurs misslyckas plugin-programmet att automatiskt lägga till resursen i en Microsoft Office 365-grupp.
- Vyn **avstämning** visar manuella guidade fel i vyerna **Vecka** eller **Månad**.

**Projektledning**

Följande problem har åtgärdats:

- Ett alltför stort antal entiteter för **RetrieveMultiple för usersettings** orsakar försämrad prestanda för projektgodkännanden och andra operationer.
- Rutnätet **Uppgiftsplanering** är begränsad till att endast visa upp till fem teammedlemmar från projektteamet. 
- Rutnätet **Uppgiftsplanering** resursuppslag filtrerar inte inaktiva resurser.
- Manuellt läge fungerar inte som förväntat i uppdelad arbetsstruktur för projektplanering.
- Rutnätet **Uppgiftsplanering** visar **Inaktiva transaktionskategorier**.
- Rutnätet **resurstilldelningar** avrundar fel när en uppgift har flera tilldelningar.
- Avrundningsvärden skiljer sig mellan den planerade kostnaden och den faktiska kostnaden för en enskild aktivitet.

**Sales**

Följande problem har åtgärdats:

- **Hämta alla transaktionskategorier** dubbelklicka på skapar flera rader.


[!INCLUDE[footer-include](../includes/footer-banner.md)]