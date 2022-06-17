---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 37, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922520"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 37, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 37, version 3. Denna version har versionsnummer V3.10.58.120 och är allmänt tillgänglig via en självuppdatering i november 2021.

## <a name="update-release-37"></a>Uppdatering version 37

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Tid och utgift**
- Användare kan inte ta bort en tidspost genom att rensa cellen.
- Vyn **Mitt misslyckade godkännande** innehåller endast projektgodkännanden med statusen **Skickad**.

**Projektledning**
- Användare får ett null-referens undantagsfel när de öppnar ett projekt i Microsoft Desktop-tillägget om projektteammedlemmens befattningsnamn är tomt.
- Det finns ingen **Spara**-knapp på sidan **Projektuppgift**, varför användare inte kan spara ändringar i uppgiftsposter.
- Användare kan inte ta bort ett projekt som har en uppgift associerad med en offert med statusen **Vunnen**.

**Försäljning**
- Fältet **Valuta** på sidan **Projekt** uppdateras så att det överensstämmer med valutan för tillämpad mall.
- Kostnaden beräknas felaktigt för uppgifter med flera valutor.
