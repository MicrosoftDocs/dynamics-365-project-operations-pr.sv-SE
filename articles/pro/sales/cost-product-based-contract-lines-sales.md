---
title: Kostnads- produktbaserade kontraktrader - lite
description: I det här ämnet finns information om hur du skapar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177264"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kostnads- produktbaserade kontraktrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Produktbaserade kontraktrader i Dynamics 365 Project Operations inkluderar fältet **Självkostnad**, som lagrar produktens självkostnad för beräkningar av vinsten.

När en produktbaserad kontraktrad skapas för en katalogprodukt används kostnaden för den produktbaserade kontraktraden från fältet **Standardkostnad** i produktkatalogen. Fältet **Standardkostnad** i produktkatalogen är konfigurerat i organisationens basvaluta. När styckkostnaden används på kontraktraden konverteras den till försäljningsvalutan i kontraktet.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Styckkostnad på en produktbaserad kontraktrad

Syftet med en styckkostnad på en produktbaserad kontraktrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning av en enhet. Om du inte alltid behöver det finns vissa scenarier där kostnaden för produkten kan rabatteras av leverantören. Föreställ dig följande scenario:

Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer. Fabrikam tillhandahåller installationstjänster, men robotarmarna anskaffas från Trey Research. Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Trey Research, kan de ge Fabrikam en särskild rabatt för den här affären. I det här fallet skapar Fabrikam en produktbaserad kontraktrad för robotarmar och inför ett styckpris för det här kontraktet som skiljer sig från standardkostnaden för robotarmar från Trey Research.
