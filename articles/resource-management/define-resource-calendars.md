---
title: Ange resurskalendrar
description: I det här ämnet finns information om hur du definierar arbetstidskalendrar för resurser i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961956"
---
# <a name="define-resource-calendars"></a>Ange resurskalendrar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Varje bokningsbar resurs som arbetar i ett projekt måste ha en kalender med arbetstid för att definiera deras tillgänglighet. Arbetstider för en resurs kan definieras på två sätt: 

   - Definiera enskilda kalenderregler för en resurs
   - Använda en befintlig kalendermall för resursen

## <a name="define-a-resources-working-hours"></a>Definiera arbetstider för en resurs

1. I menyn **Resurser** väljer du **Resurser**.
2. Från rutnätsvyn väljer du tillämplig **bokningsbar resurs**.
3. På sidan **Resursinformation** väljer du fliken **Arbetstider**. Som standard använder kalendern för bokningsbara resurser arbetstiderna från mallen med normala arbetstider som definierats för organisationen.
4. Om du vill uppdatera arbetstiderna högerklickar du på startdatumet för den föreslagna kalenderregeln som ska definieras. Använd menyn Kalenderregel om du vill definiera en kalenderregel för en specifik dag, återstoden av serien eller hela kalendern.
5. När du har valt alternativet kan du definiera:

    - Den veckodag då arbetstiderna ska gälla.
    - Arbetstiderna för varje dag.
    - Tidszonen för kalenderregeln.
    - I tillämpliga fall kan du även ange ledig tid för regeln.

## <a name="applying-a-calendar-template-to-a-resource"></a>Tillämpa en kalendermall på en resurs

1. I menyn **Resurser** väljer du **Resurser**.
2. Välj upp till 25 **bokningsbara resurser** som ska uppdateras från rutnätsvyn.
3. Välj **Ange kalender** så visas en dialogruta med en lista över tillgängliga arbetstidsmallar.
4. Välj mallen du vill använda och välj sedan **Tillämpa**.
