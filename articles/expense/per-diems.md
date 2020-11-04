---
title: Traktamente
description: I det här ämnet finns information om traktamentsregler som används i utgiftshantering.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085414"
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
Om du vill skicka in utgifter med traktamente använder du utgiftskategorin **Traktamente** när du skapar en utgiftsrapport. Ange **Traktamente från datum** , **Traktamente till datum** och **Traktementsplats**. Beloppet beräknas utifrån traktamentstaxan för den valda platsen och måltidsminskningen beräknas baserat på nivåerna av traktamentstaxa.
