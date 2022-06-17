---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 33, version 3
description: Den här artikeln innehåller funktioner och korrigeringar som är tillgängliga i Project Service Automation uppdateringsutgåva 33, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915438"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 33, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, V3, uppdateringsversion 33. Den här versionen har ett versionsnummer för V3.10.54.98 och är allmänt tillgänglig via en självuppdatering i juli 2021.

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
