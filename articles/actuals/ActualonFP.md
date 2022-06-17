---
title: Faktisk påverkan på ett åtagande med fast pris
description: Den här artikeln innehåller information om påverkan på tabellen Faktiska värden vid olika händelser under livscykeln för ett åtagande med fast pris i Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918150"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Faktisk påverkan på ett åtagande med fast pris

_**Gäller till:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I följande tabell visas faktiska värden för olika transaktionstyper som skapas vid olika händelser i ett åtagande med fast pris.

| Event | Faktisk kostnad | Ofakturerad faktisk försäljning | Fakturerad faktisk försäljning | Exempel |
|---|---|---|---|---|
| Tiden skapas. | Gäller inte | Gäller inte | Gäller inte | <p>Bob Kozack, från organisationsenheten i Fabrikam i USA som har en kostnadstakt på 100 amerikanska dollar (100 USD) i timmen, arbetar med ett projekt med namnet "Arminstallation på Adatum". Det här projektet mappas till en faktureringsmetod med fast pris på kontraktraden. Här följer ett exempel på en tidspost från Bob Kozack:</p><p>Bob Kozack - 8 timmar</p> |
| Tiden skickas in. | Gäller inte | Gäller inte | Gäller inte | En kostnadsjournalrad skapas för tidsposten. Standardkostnadstaxa anges i redovisningstransaktionen. |
| Tidsposten återkallas innan den godkänns. | Gäller inte | Gäller inte | Gäller inte | |
| Tiden godkänd. | En faktisk kostnad skapas. | Gäller inte | Gäller inte | <p>Nytt faktiskt värde som skapas:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 år, USD 800</li></ul> |
| Tidsgodkännandet annulleras. | <p>Justeringsstatusen för den ursprungliga faktiska kostnaden uppdateras till **Justerad**.</p><p>En återförd faktisk kostnad skapas med justeringsstatusen **Ej justerbar**.</p> | Gäller inte | Gäller inte | <p>Befintligt faktiskt värde som uppdateras:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 tim, USD 800, *Justerad*</li></ul><p>Nytt faktiskt värde som skapas för att återställa den tidigare ekonomiska påverkan:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 tim), (USD 800), *Ej justerad*</li></ul> |
| Tidsposten återkallas innan det att den godkänts. | <p>Justeringsstatusen för den ursprungliga faktiska kostnaden uppdateras till **Justerad**.</p><p>En återförd faktisk kostnad skapas med justeringsstatusen **Ej justerbar**.</p> | Gäller inte | Gäller inte | <p>Befintligt faktiskt värde som uppdateras:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 tim, USD 800, *Justerad*</li></ul><p>Nytt faktiskt värde som skapas för att återställa den tidigare ekonomiska påverkan:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 tim), (USD 800), *Ej justerad*</li></ul> |
| Kontraktet bekräftas. | <p>Justeringsstatusen för den tidigare faktiska försäljningen uppdateras till **Justerad**.</p><p>Faktiska återförda kostnader skapas som har justeringsstatusen **Ej justerbar**.</p><p>Nya faktiska kostnadsvärden skapas efter att kontraktreglerna har omvärderats.</p> | Gäller inte | Gäller inte | <p>Befintligt faktiskt värde som uppdateras:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 tim, USD 800, *Justerad*</li></ul><p>Nytt faktiskt värde som skapas för att återställa den tidigare ekonomiska påverkan:</p><ul><li>**Faktisk kostnad:** Bob Kozack, (8 tim), (USD 800), *Ej justerad*</li></ul><p>Nytt faktiskt värde som skapas för omutvärderad ekonomisk påverkan:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 år, USD 800</li></ul> |
| En faktura skapas. | Gäller inte | Gäller inte | Gäller inte | |
| Fakturan bekräftas med en milstolpe. | Gäller inte | Gäller inte | Nya faktiska, milstolpebaserade och fakturerade värden skapas. | <p>Befintligt faktiskt värde som förblir oförändrat:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 år, USD 800</li></ul><p>Ett nytt faktiskt värde som skapas för att registrera fakturerade försäljningsvärden:</p><ul><li>**Fakturerad faktisk försäljning:** Milstolpe, USD 5 000</li></ul> |
| Fakturan korrigeras för att kreditera milstolpen. | Gäller inte | Gäller inte | Fakturerade, återförda faktiska försäljningsvärden skapas. | <p>Befintligt faktiskt värde som förblir oförändrat:</p><ul><li>**Faktisk kostnad:** Bob Kozack, 8 år, USD 800</li></ul><p>Befintligt faktiskt värde som uppdateras:</p><ul><li>**Fakturerad faktisk försäljning:** Milstolpe, USD 5 000, *Justerad*</li></ul><p>Ett nytt faktiskt värde skapas för att återföra tidigare fakturerade försäljningsvärden:</p><ul><li>**Fakturerad faktisk försäljning:** Milstolpe, (USD 5 000), *Ej justerbar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
