---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 38, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Microsoft Dynamics 365 Project Service Automation, uppdateringsversion 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901498"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 38, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 38, version 3. Denna version har versionsnummer V3.10.59.117 och är allmänt tillgänglig via en självuppdatering i december 2021.

## <a name="update-release-38"></a>Uppdatering version 38

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Tid och utgift**

- Ett undantag uppstår om längden på godkännandeuppsättningsloggar överstiger 100 000 poster.
- Användare kommer inte åt rutnätet **Tidspost** från huvudsidan **Tidspost**.
- I dialogrutan **Import av tidspost** visas inte någon text när inga objekt kan importeras.
- Användare kan skapa godkännandeuppsättningar där fältet **Målstatus** har angetts till **Okänd**.

**Projektledning**

- Konturer visas inte korrekt i resurstilldelning för UTC(+09:30) och UTC(+10:00) när sommartid börjar.
- Fältet **Ytterligare kolumner** för uppdelad arbetsstruktur är dolt på vissa språk.
- Datumväljaren för kalenderkontrollen i rutnätet **Projektuppgift** är inte korrekt lokaliserad på kinesiska.

**Försäljning**

- Värdena **Kontaktprestanda** och **Projekts faktiska kostnad** stämmer inte överens när bokningsbara resurser med olika kontrakterande enheter och valutor anger tidsposter.
- Ett anpassat arbetsflöde för att automatiskt bekräfta fakturor misslyckas när fakturorna importeras som en hanterad lösning. Följande meddelande visas: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Ogiltig fakturastatus."
- När **Rot** väljs som summeringsalternativ och projektet har uppskattningar från ett antal olika transaktionsklasser (till exempel en kombination av uppskattningar av tid, utgift och material) summerar systemet transaktionsklasserna som en enda avgiftsrad.
- Om en utgiftsrad läggs till innan en kontraktrad associeras med ett projekt, anges inte rätt prissättning som standardvärde i fältet **Uppdatera pris**.
- Negativa försäljningsbelopp tillåts inte i entiteterna **Projekt** och **Uppgift**.