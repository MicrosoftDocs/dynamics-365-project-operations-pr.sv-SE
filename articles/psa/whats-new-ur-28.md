---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 28, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948711"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 28, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet anges de funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdateringsutgåva 28. Denna version har versionsnummer V3.10.46.32 och är i allmänhet tillgänglig genom en självuppdatering i januari 2021.

## <a name="update-release-28"></a>Uppdatering version 28

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- Användare kan använda **Massredigering** för att uppdatera tidsposter som har godkänts och skickats.

**Projektledning**

Följande problem har åtgärdats:

- I de fall där uppgiftens GUID tolkas som ett tal, kan aktiviteter inte öppnas för redigering med **Redigera aktivitet** i menyfliksområdet på sidan **Uppdelad arbetsstruktur**.

**Sales**

Följande problem har åtgärdats:

- Ett null-referensundantag genereras när plugin-programmet **GetEstimatesForProject** åberopas.
- **Markera redo att fakturera** i milstolprutnätet uppdaterar attribut endast delvis, med undantag för attributet **InvoiceStatus**, som uppdateras.



[!INCLUDE[footer-include](../includes/footer-banner.md)]