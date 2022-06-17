---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 35, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 35, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912860"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 35, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 35, version 3. Denna version har versionsnummer V3.10.56.110 och är allmänt tillgänglig via en självuppdatering i september 2021.

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
