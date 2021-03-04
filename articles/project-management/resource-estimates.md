---
title: Resursberäkningar
description: I det här ämnet finns information om hur resursuppskattningar beräknas i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127404"
---
# <a name="resource-estimates"></a>Resursberäkningar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Resursuppskattningar kommer från tidsfasade arbetsinsatser som har definierats i den uppdelade arbetsstrukturen tillsammans med tillämpliga prissättningsdimensioner. Vanligtvis är beräkningen **taxa/timme för varje roll x timmar.** Den tidsfasade arbetsinsatsen för varje resurs lagras i resurstilldelningsposten. Prissättningen lagras i en fördefinierad prislista. Enhetskonvertering används på grundval av tillämplig prislista.

![Resursuppskattningar](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standardvärden för självkostnad och kostnadsvaluta

Självkostnader används som standard från organisationsenheten.

## <a name="default-bill-rate-and-sales-currency"></a>Standardvärden för fakturataxan och försäljningsvaluta

Försäljningspriser tillämpas en gång per affär. Hierarkin för försäljningsprislista är som standard följande:

1. Organisation
2. Kund
3. Offert/kontrakt


[!INCLUDE[footer-include](../includes/footer-banner.md)]