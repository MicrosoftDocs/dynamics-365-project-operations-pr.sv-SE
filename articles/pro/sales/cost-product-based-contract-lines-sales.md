---
title: Kostnads- produktbaserade kontraktrader - lite
description: I det här ämnet finns information om hur du skapar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599292"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kostnads- produktbaserade kontraktrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Produktbaserade kontraktrader Dynamics 365 Project Operations inkluderar fältet **Självkostnad**, som lagrar självkostnadspriset för produkten för lönsamhetsberäkningar i efterföljande led.

När en produktbaserad kontraktrad skapas för en katalogprodukt utgår radkostnaden från fältet **Standardkostnad** i produktkatalogen. Fältet **Standardkostnad** i produktkatalogen är konfigurerat i organisationens basvaluta. När styckkostnaden används på kontraktraden konverteras den till försäljningsvalutan i kontraktet.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Styckkostnad på en produktbaserad kontraktrad

Syftet med en styckkostnad på en produktbaserad kontraktrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning av en enhet. Om du inte alltid behöver det finns vissa scenarier där kostnaden för produkten kan rabatteras av leverantören. Föreställ dig följande scenario:

Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer. Fabrikam tillhandahåller installationstjänster, men robotarmarna är från Trey Research. Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Trey Research, kan de ge Fabrikam ett särskilt avdrag för den här affären. I det här fallet skapar Fabrikam en produktbaserad kontraktrad för Robotic Arms. En kostnad per enhet anges för detta kontrakt. Kostnaden skiljer sig från kostnaden för robotarmar från Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]