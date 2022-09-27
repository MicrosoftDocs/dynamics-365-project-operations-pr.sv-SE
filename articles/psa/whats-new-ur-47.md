---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 47, V3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 47, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477244"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 47, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 45, V3. Den här versionen har ett versionsnummer för V3.10.78.8 och är allmänt tillgänglig via en självuppdatering i juli 2022.

## <a name="update-release-47"></a>Uppdatering version 47

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Resurshantering**
- En validering uppdaterades för att säkerställa att användarna inte kan utlösa ett null-referens undantag när de försöker skapa en projektteammedlem utan en **bokningsbar resurs**.
