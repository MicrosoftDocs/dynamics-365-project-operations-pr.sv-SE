---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 28, version 3
description: Den här artikeln innehåller funktioner och korrigeringar som är tillgängliga i Project Service Automation uppdateringsutgåva 28, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930616"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 28, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

Den här artikeln innehåller funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdateringsutgåva 28. Den här versionen har ett versionsantal V3.10.46.32 och är vanligtvis tillgänglig via en självuppdatering i januari 2021.

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
