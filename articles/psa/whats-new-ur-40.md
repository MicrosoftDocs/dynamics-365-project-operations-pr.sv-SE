---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 40, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Microsoft Dynamics 365 Project Service Automation, uppdateringsversion 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588666"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 40, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I detta ämne finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 40, version 3. Denna version har versionsnummer V3.10.61.61 och är allmänt tillgänglig via en självuppdatering i februari 2022.

## <a name="update-release-40"></a>Uppdatering version 40

### <a name="features"></a>Funktioner
Fas 1 av uppgraderingen från Project Service Automation till Project Operations - Lite kommer att släppas i februari 2022 till alla kunder. Kontrollera behörighet på [Uppgradera från Project Service Automation till Project Operations](upgrade-project-operations-non-stocked.md). Om programmet inte visas i din instans i administrationscentret för Power Platform kontaktar du supporten och ber att förhandsversionen aktiveras för dina miljöer. Din förfrågan måste innehålla en lista över miljö-ID:n där förhandsversion måste aktiveras.

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Tid och utgift**
- En anteckning saknas när en tidspost avvisas eller annulleras. 

**Försäljning**

- Om du uppdaterar kostnads- eller försäljningsberäkningar med hjälp av färdiga plugin-program har du felaktigt rätt att skicka JSON-nyttolaster som inte är giltiga utanför användargränssnittet.
- När du uppdaterar offertrader i snabbvyn kan du aktivera offerter.
