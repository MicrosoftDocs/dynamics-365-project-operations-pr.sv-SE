---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 29, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664665"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 29, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 29. Denna version har versionsnummer V3.10.47.7 och är allmänt tillgänglig via en självuppdatering i februari 2021.

## <a name="update-release-29"></a>Uppdatering version 29

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- Användare kan inte se arbetstimmar som är inloggade på icke-arbetsdagar i tidsinmatningsrutnätet.
- Godkända utgiftsposter kan redigeras i rutnätet.

**Projektledning**

Följande problem har åtgärdats:

- Valideringslogik saknas för att säkerställa att arbetstimmarna för resurstilldelning inte kan vara negativa.
- Den anpassade åtgärden **AssignResourcesForTask** uppdaterar alla fält i stället för att endast ändrade fält.
- När du kopierar ett projekt i en miljö med plugin-program eller arbetsflöden som är registrerade på händelsen **CreateProject** uppdateras inte attributet **msdyn_bulkgenerationstatus** om **CopyWBSToProject** misslyckas.
- När du expanderar projektkalendern sorteras inte arbetsdagarna i stigande ordning vilket gör att vissa uppdateringar av projektuppgiften misslyckas.
- Om du ändrar projektledaren för ett befintligt projekt utlöses standardlogiken för organisationsenheten.

**Försäljning**

Följande problem har åtgärdats:

- Fliken **Kontraktresultat** på sidan **Kontrakt** misslyckas i bakgrunden under initiering när inga kontraktrader finns.
