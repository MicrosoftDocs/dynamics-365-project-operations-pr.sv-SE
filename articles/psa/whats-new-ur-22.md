---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 22, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085488"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation uppdateringsversion 22, V3

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 22. Den här versionen har ett versionsnummer på V 3.10.33.48 och är allmänt tillgänglig via en självuppdatering i juni 2020.

## <a name="update-release-22"></a>Uppdatering version 22

### <a name="bug-fixes"></a>Felkorrigeringar



**Tid och utgift**

Följande problem har åtgärdats:

- **Tidsposter** läggs inte till automatiskt i tidspostschemat efter import.
- Rutnätet för datumväljaren **Tidspost** känner inte igen en användares nationella inställningar.

**Resurshantering**

Följande problem har åtgärdats:

- I manuellt läge identifieras inte ändringar i profiler för **resurstilldelningar** när de genererar **resurskrav**.
- **Resursförfrågningar** stöder inte status för anpassade begäranden.

**Projektledning**

Följande problem har åtgärdats:

- Om du använder dubbel klickning på EstimateGridControl tolkas inte holländska formatnummer korrekt.
- Tilldelade timmar uppdateras inte korrekt när tilldelningar ändras med hjälp av Microsoft Project-tillägget för klient på stationär dator.
- Rutnät för projektuppföljning och uppskattning visar fel försäljningsvalutakod när kontraktsvalutan är annorlunda än kundvalutan och organisationen är konfigurerad att visa valutakoder i stället för valutasymboler.
- En teammedlems slutdatum lägger till en dag om arbetskalenderns schema är 24 timmar per dag.
- Om du lägger till en transaktionskategori i en aktivitet i projektschemat utlöses inte spara automatiskt.
- Följande fel visas när du lägger till en teammedlem i projektmallen: "resurskrav kan inte associeras med projektmallar". 
- Regelskript för menyfliksområdet "msdyn. Approval. CanApproveOrReject" visar timeout-fel.

**Sales**

Följande problem har åtgärdats:

- Meddelande om valideringsfel visas inte när en kostnadsprislista väljs i prislistesökning i formulär/entitet "Ny prislista för offertprojekt".
- När du stänger offerten som vunnen navigerar den inte till det skapade kontraktet om en BPF som är kopplad till offerten är den sista fasen.
- Återföring av **Fakturerad försäljning** är länkat till den ursprungliga kostnaden när en tidspost återkallas.
- När du väljer knappen **Bekräfta** ändras inte faktura statusen till **Bekräftad** om inte fakturan uppdateras.
