---
title: Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite
description: I det här ämnet finns information om hur du konfigurerar kostnads- och försäljningstaxor för artiklar i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176723"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Att konfigurera prissättning för produktkatalogsartiklar i Dynamics 365 Project Operations är samma som i Dynamics 365 Sales.

Eftersom produkter inte kan uppskattas eller användas i Project Operations behöver du inte ange produktkatalogspriser på projektprislistor för offerter och kontrakt.

Produktkatalogspriser bör konfigureras i fältet **Produktpris** i en offert, ett kontrakt eller konto. Konfigurera inte produktkatalogspriser i projektprislistorna för dessa entiteter. Projektprislistor är exklusiva för Project Operations. Det finns programspecifik affärslogik som kopierar prislistorna från en offert till ett kontrakt. Resultatet är en kontraktspecifik projektprislista. Kopieringen kan fördröja offertvinsten om projektprislistan i offerten blir för stor. Produktprislistor kopieras inte för att skapa anpassade prislistor i kontrakt. Detta innebär att produktprislistor inte påverkar effektiviteten i offertvinstprocessen.
