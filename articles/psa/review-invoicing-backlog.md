---
title: Granska förhandsgranskningen av faktureringen i projekt och projektkontrakt
description: I det här ämnet finns information om hur du granskar tids-, utgifts- och produkteftersläpningar och hur du markerar dem som klara för fakturering.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bcdcc0cae06ce61bd582d56a8398e718051ff564
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123985"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Granska förhandsgranskningen av faktureringen i projekt och projektkontrakt

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

När en transaktion är klar för att en faktura ska skapas och bearbetas ska transaktionen vara **klar att fakturera**. I det här ämnet beskrivs typerna av transaktioner som kan skapas.

## <a name="review-the-time-and-material-billing-backlog"></a>Granska eftersläpning för fakturering av tid och material

När en tids- eller utgiftspost skickas och godkänns för ett projekt skapar PSA ett faktiskt projektvärde. Om kombinationen av projektet och transaktionsklassen är mappad till en kontraktrad för ett tids- och materialprojekt, skapas två faktiska värden när posten godkänns:

- Faktisk kostnad 
- Ofakturerad faktisk försäljning

Fakturerade försäljningsvärden representerar eftersläpad fakturering och deras faktureringsstatus måste anges som **klar för fakturering**. När en projektfaktura skapas kopieras automatiskt fakturerade försäljningsvärden som är markerade **att faktureras** som fakturaradinformation.

Om du vill granska eftersläpad fakturering för tid och material, gå till **försäljning** \> **fakturering** \> **Eftersläpad fakturering av tid och material**. Markera alla faktiska värden för ofakturerad försäljning som är klara för fakturering och välj sedan **klar för fakturering**. Faktureringsstatusen för dessa verkliga värden ändras till **klart för fakturering**.

![Eftersläpad fakturering av tid och material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Granska eftersläpad produktfakturering

När ett projektkontrakt har produktbaserade kontraktrader beaktas de i PSA för fakturering när en faktura skapas för projektkontraktet. Alla produkter som har kontraktrader som är markerade **Klar att fakturera** kopieras till projektfakturan som projektfakturarader.

Om du vill granska eftersläpad fakturering av produkter, gå till **Försäljning** \> **Fakturering** \> **Eftersläpad produktfakturering**. Markera alla produktbaserade kontraktrader som är klara för fakturering och välj sedan **klar för fakturering**. Faktureringsstatusen för dessa rader ändras till **klart för fakturering**.

![Eftersläpad produktfakturering](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Granska faktureringsmilstolpar i kontrakt med fast pris

Varje projektkontraktrad som har faktureringsmetod med fast pris måste definiera kontraktmilstolpar. De här kontraktsmilstolparna kan endast faktureras om de har markerats **Klar att fakturera**. 

Om du vill granska faktureringsmilstolpar går du **försäljning** \> **fakturering** \> **milstolpar med fast pris**. Markera alla milstolpar för ofakturerad försäljning som är klara för fakturering och välj sedan **klar för fakturering**. Faktureringsstatusen för dessa milstolpar ändras till **klart för fakturering**.

![Milstolpar med fast pris](media/FPBacklog.png)