---
title: Traktamente
description: I det här ämnet finns information om traktamentsregler som används i utgiftshantering.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: e537d6c6112eb4baf38229e3e40897eacdf21983
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578316"
---
# <a name="per-diems"></a>Traktamente

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_


Ett traktamente är ett belopp som betalas till en arbetare som reser i arbetet. I utgiftshantering kan du skapa traktamentsregler för olika resesituationer. Traktamentstaxa kan baseras på tid på året, resmål eller både och. När du skapar en traktamentsregel kan du ange att en procentsats av traktamentstaxan ska dras in om en arbetare får gratis måltider eller tjänster. Du kan även ange ett minsta och högsta antal timmar som traktamentstaxan kan gälla för en arbetares resa.

## <a name="configuration"></a>Konfiguration 

1. Om du vill lägga till traktamentsplatser går du till **Konfigurera** > **Beräkningar och koder** > **Traktamentsplatser**.
2. För varje plats som läggs till ovan väljer du en traktamentstaxa och en valuta som är giltig mellan ett specifikt start- och slutdatum för hotell, måltider och andra utgifter. Traktamentstaxa och valutor konfigureras under **Konfigurera** > **Beräkningar och koder** > **Traktamente**.
3. På sidan **Traktamentsplatser** konfigurerar du nivåer av traktamentstaxa. Med nivåerna av traktamentstaxa kan du definiera procentandelen av en daglig ersättning för hotell, måltider och andra utgifter. 
4. Om du vill ange reducering av procentandel för frukost, lunch eller middag, uppdaterar du fälten på sidan **Parametrar för utgiftshantering** under fliken **Traktamente**. 
    
## <a name="submit-expenses-using-per-diem"></a>Skicka utgifter med traktamente
Om du vill skicka in utgifter med traktamente använder du utgiftskategorin **Traktamente** när du skapar en utgiftsrapport. Ange **Traktamente från datum**, **Traktamente till datum** och **Traktementsplats**. Beloppet beräknas utifrån traktamentstaxan för den valda platsen och måltidsminskningen beräknas baserat på nivåerna av traktamentstaxa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]