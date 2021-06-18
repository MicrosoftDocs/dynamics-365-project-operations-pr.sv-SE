---
title: Traktamente
description: I det här ämnet finns information om traktamentsregler som används i utgiftshantering.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995283"
---
# <a name="per-diems"></a>Traktamente

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


Ett traktamente är ett belopp som betalas till en arbetare som reser i arbetet. I utgiftshantering kan du skapa traktamentsregler för olika resesituationer. Traktamentstaxa kan baseras på tid på året, resmål eller både och. När du skapar en traktamentsregel kan du ange att en procentsats av traktamentstaxan ska dras in om en arbetare får gratis måltider eller tjänster. Du kan även ange ett minsta och högsta antal timmar som traktamentstaxan kan gälla för en arbetares resa.

## <a name="configuration"></a>Konfiguration 

1. Om du vill lägga till traktamentsplatser går du till **Konfigurera** > **Beräkningar och koder** > **Traktamentsplatser**.
2. För varje plats som läggs till ovan väljer du en traktamentstaxa och en valuta som är giltig mellan ett specifikt start- och slutdatum för hotell, måltider och andra utgifter. Traktamentstaxa och valutor konfigureras under **Konfigurera** > **Beräkningar och koder** > **Traktamente**.
3. På sidan **Traktamentsplatser** konfigurerar du nivåer av traktamentstaxa. Med nivåerna av traktamentstaxa kan du definiera procentandelen av en daglig ersättning för hotell, måltider och andra utgifter. 
4. Om du vill ange reducering av procentandel för frukost, lunch eller middag, uppdaterar du fälten på sidan **Parametrar för utgiftshantering** under fliken **Traktamente**. 
    
## <a name="submit-expenses-using-per-diem"></a>Skicka utgifter med traktamente
Om du vill skicka in utgifter med traktamente använder du utgiftskategorin **Traktamente** när du skapar en utgiftsrapport. Ange **Traktamente från datum**, **Traktamente till datum** och **Traktementsplats**. Beloppet beräknas utifrån traktamentstaxan för den valda platsen och måltidsminskningen beräknas baserat på nivåerna av traktamentstaxa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]