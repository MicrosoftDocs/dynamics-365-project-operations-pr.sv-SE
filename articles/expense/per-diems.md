---
title: Traktamente
description: Den här artikel innehåller information om de traktamentsregler som används i utgiftshanteringen.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930202"
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