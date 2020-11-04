---
title: Resursberäkningar
description: I det här ämnet finns information om hur resursuppskattningar beräknas i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085460"
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
