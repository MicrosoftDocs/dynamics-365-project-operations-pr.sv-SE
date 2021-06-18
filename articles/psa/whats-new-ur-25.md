---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 25, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 92dd74378457cf877e8ec26eb85a7883dda97d51
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000233"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 25, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet anges de funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdateringsutgåva 25. Denna version har versionsnumret V 3.10.43.76 och är i allmänhet tillgänglig genom en självuppdatering i oktober 2020.

## <a name="update-release-25"></a>Uppdatering version 25

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har korrigerats:

- Tidstransaktionsdiagram som visar ytterligare data baserat på för stort för ett intervall som hämtas.

**Resurshantering**

Följande problem har korrigerats:

- Lägger till Package Deployer-kod för att hoppa över Universal Resource Scheduling korrigeringsfilen om det redan finns en korrigeringsfil för versionen.

**Projektledning**

Följande problem har åtgärdats:

- Korrigerade skillnader i avrundning och valutakurser resulterar i felaktiga planerade kostnader i rutnätet för projektspårning.
- Stödja möjligheten att visa två eller flera reagera rutnät i formuläret **projekt**.
- Med den här valideringen kan du adressera möjligheten att tilldela en uppgift förbi kalenderns slutdatum, vilket resulterar i en misslyckad resurstilldelning.
- Förbättrad felhantering i adress nollreferens undantag genererat från följande:

    - **PreValidateProjectTeamMemberCreate** plugin
    - **PreValidateProjectTaskCreate** när en projektuppgift skapas utan ett associerat projekt
    - **PreProjectTeamMemberCreate** plugin
    - **PostProjectTeamMemberDelete** plugin
    - **PreValidateProjectTaskDelete** plugin

**Sales**

Följande problem har åtgärdats:

- Förbättrad felhantering för att adressera nollreferens undantag som genererats från **Kopiera projekt: uppskattning av HelperResource-hantering**.
- **Inte redo att fakturera** på en **Eftersläpning av tids- och materialfakturering** rensar inte faktureringsstatus.
- Korrigerade felmärkta knappar **Priser** i **Rollpris** och **Katalogobjekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]