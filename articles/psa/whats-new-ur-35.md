---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 35, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Microsoft Dynamics 365 Project Service Automation, uppdateringsversion 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473287"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 35, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 35, version 3. Denna version har versionsnummer V3.10.56.110 och är allmänt tillgänglig via en självuppdatering i september 2021.

## <a name="update-release-35"></a>Uppdatering version 35

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Tid och utgift**

- Projekt godkännaren får ett läsprivilegiumsfel när han eller hon godkänner utgiftsposter med rollen **Projektgodkännare**.
- Projekt godkännaren får ett skrivprivilegiumsfel för **msdyn_projectapproval** när han eller hon avbryter en godkänd **Projektgodkännar**-roll.
- När du väljer **Kopiera vecka** i en tidspost i appmodulen Dynamics 365 för telefoner - Projektresursnav uppstår följande fel: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Policyn **Försök igen** godkänner automatiskt poster som tidigare avvisats.
- Underrutnätet **Godkännandeuppsättningar** visar icke-tillämpliga menyfliksåtgärder.
- Ikoner saknas för **Projektuppgift** och **Resursroll** i entiteten **Tidspost**.
- När du importerar resurstilldelningar har importerade tidsposter inte rätt varaktighet för tilldelningar som skapats med hjälp av manuella åtgärder.
- **Borttagning** saknas på sidan **Avancerad sökning för tidsposter**.
- **Spara** saknas på sidan **Tidspostinformation**. Detta problem förhindrar att ändringar sparas när sidan stängs.

**Projektplanering**

- Rutnäten **Resurstilldelning** och **Resurstilldelning** sorterar inte grupperade attribut alfabetiskt.
- Uppgifter kan inte skapas om datumet har anpassats till **Endast datum**.

**Resurshantering**

- Om både Dynamics 365 Field Service och Project Service Automation har installerats uppstår överläggsproblem när **Vy associerad med resurskrav** associeras med en huvudsida.
- Om du dubbelklickar på **Spara** i dialogrutan **Snabbregistrera teammedlem** går det inte att skapa resurskravet.

**Försäljning**

- Ett undantag visas om du tar bort en uppgift som är associerad med en offert som har statusen **Vunnen**.
