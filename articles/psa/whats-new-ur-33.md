---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 33, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334608"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 33, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 33. Den här versionen har ett versionsnummer för V3.10.54.98 och är allmänt tillgänglig via en självuppdatering i juli 2021.

## <a name="update-release-33"></a>Uppdatering version 33

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- Två låsta fält, **msdyn_description** och **msdyn_externaldescription** redigerbara efter att de har skickas in.
- Ett felmeddelande visas om en kostnad skapas som inte är relaterad till ett projekt.
- När en tidspost skapas blir resursrollen en inaktiv roll som standard.
- Rader som hör till en förterad och borttagna utgifter tas inte bort.
- I **Snabbregistreringsformulär för tidspost**, uppdatera vyn **Projektuppgiftslista** för att ändra datumet som visas som standard till uppgiftens startdatum.
- När du skapar en tidspost från fliken **Relaterade** för den bokningsbara resursen, skapas tidsposten felaktigt för den inloggade användaren i stället för den överordnat bokningsbara resursen.
- Nya fält läggs till i dialogrutan **MDD för massgodkännande**.

**Projektplanering**

Följande problem har åtgärdats:
- Gör projektgenereringen långsammare när mallar för projektarbete i timmen tillämpas med komplexa kalendrar.
- När startdatum är större än slutdatumet visas ett fel i projektmallen för kopian på grund av skillnader i tidskomponenten för varje fält.

**Resurshantering**

Följande problem har åtgärdats:
- En felaktig parameter används i resursutnyttjandefrågan och XML-leadsen leder till felaktiga filterresultat i rutnätet **resursutnyttjande**.
- Bekräftelsen **Utöka bokningar** visar felaktigt slutdatum för bokningar.

**Försäljning**

Följande problem har åtgärdats:
- Ett felmeddelande visas om ett kategoripris skapas med värden som saknas.
- Ett felmeddelande visas om en kontraktradsmilstolpar skapas utan en orderrad.