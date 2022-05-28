---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 39, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Microsoft Dynamics 365 Project Service Automation, uppdateringsversion 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588758"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 39, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 39, version 3. Denna version har versionsnummer V3.10.60.170 och är allmänt tillgänglig via en självuppdatering i januari 2022.

## <a name="update-release-39"></a>Uppdatering version 39

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Allmänt**

- Flera förbättringar har gjorts i webbplatsöversikten för arabisk översättning.

**Projektledning**

- Ett fel uppstår när du ändrar projektledaren för ett projekt till en användare som redan är teammedlem i projektet.

**Försäljning**

- Ägaren till **Prislista för projektkontrakt** är felaktig när prislistan skapas automatiskt. 
- När prislistan tillämpas på projektparametern gäller inte prislistans datum då den har effekt.
- Kontraktenheten kanske inte har rätt standardvärde när två separata offerter redigeras.
