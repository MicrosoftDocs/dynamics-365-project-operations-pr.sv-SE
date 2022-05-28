---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 42, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Microsoft Dynamics 365 Project Service Automation, uppdateringsversion 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589218"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 42, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 42, version 3. Den här versionen har ett versionsnummer på V3.10.73.61 och är allmänt tillgänglig via en självuppdatering i april 2022.

## <a name="update-release-42"></a>Uppdatering version 42

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Tid och utgift**

- När en tidrapport avvisas identifieras den användare som avvisade den felaktigt som **System**.
- När tidsposter importeras saknas värdet för **Resurskategori**.
- Projektgodkännare kan godkänna skickade projekt när deras behörigheter inte är specifikt inställda på **Kan godkänna**.

**Försäljning**

- När faktiska värden loggas på uppgifter som inte är på rotnivå, aggregeras de faktiska kostnaderna felaktigt.
