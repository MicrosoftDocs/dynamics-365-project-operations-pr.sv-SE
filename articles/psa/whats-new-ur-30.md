---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 30, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 07ca20425d05d1d638d9b2b8c3425562e39dd6627916794d1ad8441f00658459
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987008"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 30, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution.md).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 30. Den här versionen har ett versionsnummer på V3.10.51.61 och är allmänt tillgänglig via en självuppdatering i april 2021.

## <a name="update-release-30"></a>Uppdatering version 30

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- Ett fel uppstår när du skapar och sparar en tidspost på sidan **Snabb skapa** om fältet **Roll** tas bort.
- Med filtret Tidspost används fel filteroperator.
- Kopierade tidsscheman visas inte automatiskt när du väljer **Kopiera vecka** i tidsinmatningskontrollen.

**Resurshantering**

Följande problem har åtgärdats:

- När du utökar en bokning blir den bokningsstatus som tilldelats den svåra bokningsstatusen felaktig. Om en bokning utökas gäller den bokningsstatus som har definierats som **Genomförd** i metadata för bokningskonfigurationen.
- När en giltig bokningsstatus inte anges lokaliseras inte felmeddelandet korrekt.

**Projektledning**

Följande problem har åtgärdats:

- Projekt kan inte skapas i en valuta och omfattar relaterade uppgifter i en annan valuta.

**Försäljning**

Följande problem har åtgärdats:

- När en prislista kopieras uppdateras inte priserna.
- Det går inte att stänga en offert som den har vunnit när kostnadsdetaljen har ett ursprungsvärde.
- I entiteten **Projektuppgift**, **Beräknad kostnad** har bytt namn till **Planerad kostnad (bas)**.
- Ett null-referensfel skapas när fakturor skapas eller tas bort.
