---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 41, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Microsoft Dynamics 365 Project Service Automation, uppdateringsversion 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580984"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 41, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 41, version 3. Den här versionen har versionsnummer V3.10.62.162 och är allmänt tillgänglig via en självuppdatering i mars 2022.

## <a name="update-release-41"></a>Uppdatering version 41

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Projektledning**
- När du försöker skapa ett projekt från en mall som bygger på ett projekt som skapats från tillägget för stationär dator visas följande fel: "Valideringen av fältet Planerat arbete för resurstilldelning: Slutdatum för varje resurstilldelningstidsutsnitt får inte vara tidigare än startdatum".

**Tid och utgift**
- När du försöker ta bort en tidspost visas följande felmeddelande: "Ett oväntat fel uppstår från ISV-kod".

**Försäljning**
- När du skapar en faktura för en milstolpe med fast pris fylls inte fälten **Beskrivning** och **Extern beskrivning** i. 
