---
title: Kostnads- produktbaserade kontraktrader - lite
description: I det här ämnet finns information om hur du skapar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55f74b016b55945433083e11902003cea99f1aa463264cdd95b0aad389592e20
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997358"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kostnads- produktbaserade kontraktrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Produktbaserade kontraktrader Dynamics 365 Project Operations inkluderar fältet **Självkostnad**, som lagrar självkostnadspriset för produkten för lönsamhetsberäkningar i efterföljande led.

När en produktbaserad kontraktrad skapas för en katalogprodukt utgår radkostnaden från fältet **Standardkostnad** i produktkatalogen. Fältet **Standardkostnad** i produktkatalogen är konfigurerat i organisationens basvaluta. När styckkostnaden används på kontraktraden konverteras den till försäljningsvalutan i kontraktet.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Styckkostnad på en produktbaserad kontraktrad

Syftet med en styckkostnad på en produktbaserad kontraktrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning av en enhet. Om du inte alltid behöver det finns vissa scenarier där kostnaden för produkten kan rabatteras av leverantören. Föreställ dig följande scenario:

Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer. Fabrikam tillhandahåller installationstjänster, men robotarmarna är från Trey Research. Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Trey Research, kan de ge Fabrikam en särskild rabatt för den här affären. I det här fallet skapar Fabrikam en produktbaserad kontraktrad för Robotic Arms. En kostnad per enhet anges för detta kontrakt. Kostnaden skiljer sig från kostnaden för robotarmar från Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]