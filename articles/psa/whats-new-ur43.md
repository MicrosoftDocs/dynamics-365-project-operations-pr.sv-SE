---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 43, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915344"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 43, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 43, version 3. Den här versionen har ett versionsnummer på V3.10.74.200 och är allmänt tillgänglig via en självuppdatering i maj 2022.

## <a name="update-release-43"></a>Uppdatering version 43

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.


**Tid och utgift**

- När du importerar tidsposter från allokeringar eller resurstilldelningar upprätthålls inte referensen till den relaterade bokningsbara resursen.
- När tidsinmatningsrutnätet expanderas till helskärm fungerar inte navigeringen i rutnätet med tabbtangenten.
- När du skickar en tidspost som har skapats av en annan användare fylls fältet **Skickades av** i felaktigt med användaren som skapade tidmallen.
