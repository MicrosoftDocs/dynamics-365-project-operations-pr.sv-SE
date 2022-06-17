---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 24, V3
description: Den här artikeln innehåller funktioner och korrigeringar som är tillgängliga i Project Service Automation uppdateringsutgåva 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
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
ms.openlocfilehash: d2cd8c18a2ea10ae090d8258d835453b279d717f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926430"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation uppdateringsversion 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, V3, uppdateringsversion 24. Den här versionen har versionsnummer V 3.10.42.43 och är allmänt tillgänglig via en självuppdatering i oktober 2020.

## <a name="update-release-24"></a>Uppdatering version 24

### <a name="bug-fixes"></a>Felkorrigeringar

**Sales**

Följande problem har åtgärdats:

- Problem när standardprislistan för produkter anges.
- Resultatet av offertvinst är långsamt på grund av den inbäddade prislistan och kopian av rollprisregister.
- **Projektkontrakt/försäljningsnav** > **produktradartikel/orderradkvantitet** avrundas automatiskt till närmsta heltal.
- Höj till systemprivilegierna vid läsning av prislistor.
- Kopiera adressfält för kunder **address1_freighttermscode** och **address1_shippingmethodcode** till offert/order. 


**Tid och utgift**

Följande problem har åtgärdats:

- **Tidsinmatningsrutnätet** stöder inte tidsfunktionen **endast datum**.
- **Tidsposten** uppdateras inte automatiskt. En manuell uppdatering krävs.
- Det går inte att importera tidsposterna från en tilldelning när det finns en rast (0 timme) i en resurs tilldelningar.
- När du skapar en tidspost anger du startvärdet som **msdyn_date**.
- Aktivera massredigering för tidsregistrering igen.

**Resurshantering**

Följande problem har åtgärdats:

- Om du försöker uppdatera statusen för en bokning inom en dag utan ett krav kommer ett null-ref-undantag att resultera.
- Det gick inte att läsa in **avstämningsvyn**.


**Projektledning**

Följande problem har åtgärdats:

- I **Projektschema** när du ändrar från **Manuell** till **Auto** slutförs inte spara automatiskt.
- Utgiftskostnader ska inte beräknas mot varians i **projektspårningsrutnätet**.
- Inkonsekvent beteende för kolumnerna **taggen uppskattningar** under inläsning jämfört med ändring av typen **tidsfas**.
- Den faktiska kostnaden för ett projekt kan inte återspegla summorna från **faktiska värden**.
- **Det uppskattade avslutningsdatumet** på fliken **Sammanfattning** matchar inte **WBS-schemat**.
- **Uppdatera faktiska timmar** vid utdragning fungerar inte korrekt.
- En projektledare utanför roten **BU** kan inte skapa ett projekt.
- Ändringar i uppgift eller kategori i **utgiftsuppskattningar** kvarstår inte.
- **Kopia av kontrakt** kopierar fakturascheman och körningsstatus.
- Knappen **Uppdatera faktiska värden** för beräkning av sammanfattningsuppgifter.
- Microsoft Project-tillägg: korrigera null-referens-fel om en teammedlem har en tom resursenhet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
