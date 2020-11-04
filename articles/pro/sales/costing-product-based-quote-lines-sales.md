---
title: Produktbaserade offertrader för kostnadsredovisning
description: I det här ämnet finns information om hur man lägger till en självkostnad på en produktbaserad offertrad.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085443"
---
# <a name="costing-product-based-quote-lines"></a>Produktbaserade offertrader för kostnadsredovisning

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


Produktbaserade offertrader i Dynamics 365 Project Operations har också ett fält som heter **Självkostnad**. Det här fältet används för att spåra självkostnaden för produkten på offertraden och för vinstberäkningarna nedströms.

När en produktbaserad offertrad skapas för en katalogprodukt används kostnaden för den produktbaserade offertraden från fältet **Standardkostnad** i produktkatalogen. Standardkostnadsfältet i produktkatalogen är konfigurerat i organisationens basvaluta. Standardstyckkostnaden på den produktbaserade offertraden omvandlas till försäljningsvalutan i offerten.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Styckkostnad på en produktbaserad offertrad

Syftet med en styckkostnad på en produktbaserad offertrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning. Detta är inte ett typiskt scenario, men ibland kan kostnaden för produkten rabatteras av leverantören, beroende på vilken kund som genomför det slutliga köpet.

Till exempel:

Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer. Fabrikam tillhandahåller installationstjänster, men robotarmarna anskaffas från Trey Robotics. Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Treys robotarmar, kan Trey ge Fabrikam en särskild rabatt för den här affären.

I det här fallet skapas en produktbaserad offertrad för robotarmar och du kan ange en särskild styckkostnad för offerten. Den här kostnaden skiljer sig från standardkostnaden för Treys robotarmar.
