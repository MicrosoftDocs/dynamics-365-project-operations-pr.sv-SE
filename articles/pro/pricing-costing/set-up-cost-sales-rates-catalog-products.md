---
title: Konfigurera kostnads- och försäljningstaxa för katalogprodukter
description: I det här ämnet finns information om hur du konfigurerar kostnads- och försäljningstaxor för artiklar i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085607"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Konfigurera kostnads- och försäljningstaxa för katalogprodukter

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Att konfigurera prissättning för produktkatalogsartiklar i Dynamics 365 Project Operations är samma som i Dynamics 365 Sales.

Eftersom produkter inte kan uppskattas eller användas i Project Operations behöver du inte ange produktkatalogspriser på projektprislistor för offerter och kontrakt.

Produktkatalogspriser bör konfigureras i fältet **Produktpris** i en offert, ett kontrakt eller konto. Konfigurera inte produktkatalogspriser i projektprislistorna för dessa entiteter. Projektprislistor är exklusiva för Project Operations. Det finns programspecifik affärslogik som kopierar prislistorna från en offert till ett kontrakt. Resultatet är en kontraktspecifik projektprislista. Kopieringen kan fördröja offertvinsten om projektprislistan i offerten blir för stor. Produktprislistor kopieras inte för att skapa anpassade prislistor i kontrakt. Detta innebär att produktprislistor inte påverkar effektiviteten i offertvinstprocessen.
