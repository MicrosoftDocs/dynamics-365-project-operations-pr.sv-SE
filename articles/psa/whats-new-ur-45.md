---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 45, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169167"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 45, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 45, V3. Den här versionen har ett versionsnummer för V3.10.76.168 och är allmänt tillgänglig via en självuppdatering i juli 2022.

## <a name="update-release-45"></a>Uppdatering version 45

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Försäljning**

- Användarna kan inte skapa fakturor efter att de har försökt skapa en faktura utan någon ofakturerad försäljning, om de även visar samma instans av sidan och inte uppdaterar den.

**Tid och utgift**

- När moderna godkännanden har aktiverats och ett godkänt projektgodkännande godkänns, uppdateras poststadiet felaktigt till stadiet för **Återkalla godkänd begäran**.
- När Modern Approvals har aktiverats och molnflöden är inaktiva, lyckas inte godkännandeprocessen och inga användare som skickar eller godkänner dem meddelas.
