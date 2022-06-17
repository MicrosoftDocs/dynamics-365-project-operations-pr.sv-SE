---
title: Effekten av faktiska värden för ett internt projekt
description: Den här artikeln innehåller information om påverkan på tabellen Faktiska värden vid olika händelser för ett internt projekt i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921370"
---
# <a name="actuals-impact-for-an-internal-project"></a>Effekten av faktiska värden för ett internt projekt

_**Gäller till:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I följande tabell visas faktiska värden för olika transaktionstyper som skapas vid olika händelser i ett internt projektengagemang.

| Event | Faktisk kostnad | Exempel |
|---|---|---|
| Tiden skapas. | Gäller inte | <p>Bob Kozack, från organisationsenheten i Fabrikam i USA som har en kostnadstakt på 100 amerikanska dollar (100 USD) i timmen, arbetar med ett projekt med namnet "Arminstallation på Adatum". Det här projektet mappas till en faktureringsmetod med fast pris på kontraktraden. Här följer ett exempel på en tidspost från Bob Kozack:</p><p>Bob Kozack - 8 timmar</p> |
| Tiden skickas in. | Gäller inte | En kostnadsjournalrad skapas för tidsposten. Standardkostnadstaxa anges i redovisningstransaktionen. |
| Tidsposten återkallas innan den godkänns. | Gäller inte | |
| Tiden godkänd. | En faktisk kostnad skapas. | <p>Nytt faktiskt värde som skapas:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 år, USD 800</li></ul> |
| Tidsgodkännandet annulleras. | <p>Justeringsstatusen för den ursprungliga faktiska kostnaden uppdateras till **Justerad**.</p><p>En återförd faktisk kostnad skapas med justeringsstatusen **Ej justerbar**.</p> | <p>Befintligt faktiskt värde som uppdateras:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 tim, USD 800, *Justerad*</li></ul><p>Nytt faktiskt värde som skapas för att återställa den tidigare ekonomiska påverkan:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 tim), (USD 800), *Ej justerad*</li></ul> |
| Tidsposten återkallas innan det att den godkänts. | <p>Justeringsstatusen för den ursprungliga faktiska kostnaden uppdateras till **Justerad**.</p><p>En återförd faktisk kostnad skapas med justeringsstatusen **Ej justerbar**.</p> | <p>Befintligt faktiskt värde som uppdateras:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 tim, USD 800, *Justerad*</li></ul><p>Nytt faktiskt värde som skapas för att återställa den tidigare ekonomiska påverkan:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 tim), (USD 800), *Ej justerad*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
