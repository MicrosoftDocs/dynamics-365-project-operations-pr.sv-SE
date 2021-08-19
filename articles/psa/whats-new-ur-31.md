---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 31, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002173"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 31. Den här versionen har ett versionsnummer på V3.10.52.77 och är allmänt tillgänglig via en självuppdatering i maj 2021.

## <a name="update-release-31"></a>Uppdatering version 31

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- Knapparna för tidsinmatningskontroll på sidan **Bokningsbar resurs** var förvirrande.
- Ett null-referensundantag skapades i **Project.SetTrackingFields** när en tidspost godkändes.

**Resurshantering**

Följande problem har åtgärdats:

- **Skapa teammedlem** visar inte korrekt metadatainställning för bokning för **Standardstatus för bekräftad bokning**.
- Vid uppgradering från PSA 1.X till 3.X misslyckas uppgraderingsprocessen vid **UpgradeResourceRequirements**.


**Försäljning**

Följande problem har åtgärdats:

- Faktisk intäkt konverterar beloppen till projektvaluta i spårningsrutnätet.
- Standardvalutan skiljer sig när journalrader, offertrader och kontraktrader skapas i scenarier där företagets basvaluta skiljer sig från projektvalutan.
- Förfrågan **Väntar på validering av korrigeringsjournal** filtreras inte per projekt.
- Återstående försäljning beräknas felaktigt på ett projekt.
- Offerter baserade på en kontakt misslyckas när de skapas utan en prislista.
- Det visas inget bearbetningsfält när du väljer **Bekräfta faktura**.
- Det visas inget bearbetningsfält när du väljer **Skapa faktura**.
- Om du stänger en offert som förlorad annulleras inte bokningar.







