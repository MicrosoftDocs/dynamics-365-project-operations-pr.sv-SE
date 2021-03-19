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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286540"
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