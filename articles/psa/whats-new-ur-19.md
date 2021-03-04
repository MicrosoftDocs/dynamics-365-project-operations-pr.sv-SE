---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 19, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143673"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation uppdateringsversion 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 19. Den här versionen har ett versionsnummer på V3.10.30.41 och är allmänt tillgänglig via en självuppdatering i maj 2020.

## <a name="update-release-19"></a>Uppdatering version 19

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats: 

- Fel som härletts från import av tidspost visas inte korrekt.
- Tidspostrutnätet stöder inte fältfunktionen **Endast datum**.
- Projektresurser kan inte skapa en utgift med ett projekt.

**Projektledning**

Följande problem har åtgärdats: 

-  Nästa underordnade aktivitet orsakar en felaktig beräkning av insatser under slutförande (EAC).

**Sales**

Följande problem har åtgärdats: 

- Åtgärden **Omberäkna** fungerar inte med information om utgiftskontraktrader eller information om offertrader.
- **Uppdatera priser** saknas för utgiftsuppskattningar.
-  Kunder kan inte välja anpassade kontraktstatusorsaker från sidan **projektkontrakt**.
- Kunder försämrar prestanda när de skapar en anpassad prislista från en offert.
- Kunder är inkonsekventa med standardinställningen **enhet** på sidorna **Information om offertrad** och **Kontraktradsinformation**.
- Om du lägger till icke debiterbara transaktionskategoriartiklar på en debiterbar kontraktrad respekteras inte faktureringstypen **Icke debiterbar** för transaktionskategorin.
- Kunder kan inte använda de nyligen tillagda rollerna och kategorierna i tidigare skapade kontrakt.
- Kunder upplever försämrad prestanda onödig hämtning i PreValidateProjectTeamMemberUpdate.cs
- Roller som har ställts in icke-debiterbara i listan **resurskategorier** bör läggas till på fliken **Debiterbara roller** som **Icke debiterbar** på kontraktraden för ett projekt.
- Kunderna kan få försämrade prestanda när de skapar ett projekt eftersom **GetBookableResourceIdFromUser** hämtar alla bokningsbara resurser i stället för bara det primära ID:t.
- **TransactionType**-entiteten saknar plugin-programmet för valideringsuppdatering för att förhindra att användare anger **Enheter** och **UnitGroups** som inte är giltiga för transaktionstyper.
- Steget **Ta bort** fungerar inte för import av tidsposter.
