---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 41, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 41, V3.
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930570"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 41, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 41, version 3. Den här versionen har versionsnummer V3.10.62.162 och är allmänt tillgänglig via en självuppdatering i mars 2022.

## <a name="update-release-41"></a>Uppdatering version 41

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Projektledning**
- När du försöker skapa ett projekt från en mall som bygger på ett projekt som skapats från tillägget för stationär dator visas följande fel: "Valideringen av fältet Planerat arbete för resurstilldelning: Slutdatum för varje resurstilldelningstidsutsnitt får inte vara tidigare än startdatum".

**Tid och utgift**
- När du försöker ta bort en tidspost visas följande felmeddelande: "Ett oväntat fel uppstår från ISV-kod".

**Försäljning**
- När du skapar en faktura för en milstolpe med fast pris fylls inte fälten **Beskrivning** och **Extern beskrivning** i. 
