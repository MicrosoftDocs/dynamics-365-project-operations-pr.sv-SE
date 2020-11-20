---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 17, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 17, version 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085496"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation uppdateringsversion 17, V3

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.  Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 17. Den här versionen har versionsnummer V3.10.6.34 och är allmänt tillgänglig via en självuppdatering i mars 2020.


## <a name="update-release-17"></a>Uppdatering version 17

### <a name="bug-fixes"></a>Felkorrigeringar

**Allmänt**

- Åtgärdat: Uppdatering för Project Service Automation för att påtvinga licenser för team medlemmar (projektresursens nav omfattar tjänstplan-metadata för teammedlem, version 3.x)
 
**Tid och utgift**

- Åtgärdat: Det går inte att ändra en utgiftsuppskattning från ett pris som inte är noll till noll (0). Ändringen ignoreras.

**Projektledning**

- Åtgärdat: en kontroll för nollvärden har lagts till på en gruppmedlems befattningsnamn.
- Åtgärdat: Fältet **msdyn_userresourceid** i entiteten **msdyn_resourceassignment** har blivit inaktuellt.
- Åtgärdatt: Uppgraderingen från 2.x till 3.x hanterar nu tomma insatsprofiler i aktivitetstilldelningar.

**Sales**

- Åtgärdat: **Invoice.PreValidateInvoiceUpdate** hanterar nu scenariot med att återtilldela postägare korrekt.
- Åtgärdat: När transaktionsklassen är **Tid** är **UnitGroup** icke redigerbart för alla entiteter, inklusive **QuoteLineDetails**. **JournalLine** , **InvoiceLineDetail** och **ContractLineDetails**. **Enhet** är emellertid icke-redigerbart endast för **JournalLine** och **InvoiceLineDetails**.

