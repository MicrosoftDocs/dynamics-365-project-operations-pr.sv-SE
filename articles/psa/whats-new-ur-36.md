---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 36, version 3
description: Den här artikeln innehåller information om de funktioner och korrigeringar som är tillgängliga i Microsoft Dynamics 365 Project Service Automation uppdateringsutgåva 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925004"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Nyheter och ändringar i Project Service Automation, uppdateringsversion 36, version 3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, uppdateringsversion 36, version 3. Den här versionen har ett versionsnummer på V3.10.57.152 och är allmänt tillgänglig via en självuppdatering i oktober 2021.

## <a name="update-release-36"></a>Uppdatering version 36

### <a name="bug-fixes"></a>Felkorrigeringar

Följande problem har åtgärdats.

**Allmänt**
- Fältnamn **Standardmall för arbetstid** översätts felaktigt på **Projektparametrar**.
- Async plugin-program hanterar inte undantag som är relaterade till korrekt **SharedVariableService**.

**Tid och utgift**
- Om körader saknas eller användaren inte har rätt läsprivilegier, inträffar ett felaktigt fel när projektgodkännanden annulleras.
- Användare kan inte avbryta ett godkännande när en kostnad eller tidspost har mer än ett associerat projektgodkännande.
- **Frånvaro** och **Semester** är felaktigt översatta för det kinesiska språket i ett uppslag på snabbstartssidan för **tidsinmatning**.

**Resurshantering**
- Användaren kan inte söka efter resurser i **Schemaläggningsassistenten** vyläget har angetts till **Dag**, **Vecka** eller **Månad**.
- Generiska resurser får inte ha tomma befattningsnamn. 
- Om du stänger ett kontrakt som förlorats annulleras inte det framtida kontraktet.

**Försäljning**
- När en miljö har en stor volym produkter bryts prestanda ned i rutnätet **materialberäkning**.
- När du skapar ett projekt från en mall är projektvalutan inte standardvärdet för respektive projektledares kontraktenhet.
- Faktiska belopp matchar inte alltid vad som reflekteras i det förfallna projektet eller så blir beloppen negativa i specifika scenarier.
- Ett fel uppstår när du associerar ett projekt som skapats från projektmall till en kontraktrad.
- Användare kan ta bort en kontraktrad med milstolpen, **Redo att faktureras** och **Faktura skapas**. Detta bör inte tillåtas.
- När uppskattningar importeras från ett projekt, är avgiftsradens debitering felaktigt inställd när uppgiftsbaserad fakturering är aktiverad för offertraden.
- När du lägger till en faktureringsmilstolpar med fast pris återspeglas inte milstolpen i underrutnätet förrän sidan har uppdaterats.
- Ett null-referens undantag skapas när du skapar ett projektkontrakt med ett offertnamn som är null.
- Manuella lägesuppgifter där projektvalutan skiljer sig från resursens valuta leder till felaktiga priser.
- Användare kan inte skapa fel i en transaktioner som har korrigerats med hjälp av en korrigeringsfaktura.
- Inaktiverade transaktionskategorier visas i rutnätet för **Utgiftsberäkningar**.



