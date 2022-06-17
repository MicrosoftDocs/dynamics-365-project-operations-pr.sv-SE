---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 39, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 39, V3.
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922474"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 39, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 39, version 3. Denna version har versionsnummer V3.10.60.170 och är allmänt tillgänglig via en självuppdatering i januari 2022.

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
