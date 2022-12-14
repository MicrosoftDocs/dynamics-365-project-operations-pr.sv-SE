---
title: Produktbaserade offertrader för kostnadsredovisning
description: Den här artikeln innehåller information om hur du tillämpar ett kostnadspris på en produktbaserad offertrad.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825634"
---
# <a name="costing-product-based-quote-lines"></a>Produktbaserade offertrader för kostnadsredovisning

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Produktbaserade offertrader i Dynamics 365 Project Operations har även fältet **självkostnad**. Det här fältet används för att spåra självkostnaden för produkten på offertraden och för vinstberäkningarna nedströms.

När en produktbaserad offertrad skapas för en katalogprodukt används kostnaden för den produktbaserade offertraden från fältet **Standardkostnad** i produktkatalogen. Standardkostnadsfältet i produktkatalogen är konfigurerat i organisationens basvaluta. Standardstyckkostnaden på den produktbaserade offertraden omvandlas till försäljningsvalutan i offerten.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Styckkostnad på en produktbaserad offertrad

Syftet med en styckkostnad på en produktbaserad offertrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning. Detta är inte ett typiskt scenario, men ibland kan kostnaden för produkten rabatteras av leverantören, beroende på vilken kund som genomför det slutliga köpet.

Till exempel:

Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer. Fabrikam tillhandahåller installationstjänster, men robotarmarna anskaffas från Trey Robotics. Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Treys robotarmar, kan Trey ge Fabrikam ett särskilt avdrag för den här affären.

I det här fallet skapas en produktbaserad offertrad för robotarmar och du kan ange en särskild styckkostnad för offerten. Den här kostnaden skiljer sig från standardkostnaden för Treys robotarmar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
