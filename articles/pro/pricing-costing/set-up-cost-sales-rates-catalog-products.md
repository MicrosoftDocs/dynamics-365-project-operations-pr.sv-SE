---
title: Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite
description: I det här ämnet finns information om hur du konfigurerar kostnads- och försäljningstaxor för artiklar i en produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996053"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Att ange priser för produktkatalogsobjekt i Dynamics 365 Project Operations sker på samma sätt som i Dynamics 365 Sales.

I Project Operations kan produkter inte beräknas eller användas i projekt, varför produktkatalogpriser inte behöver anges i projektprislistor för offerter och kontrakt.

Använd fältet **Produktpris** för en offert, ett kontrakt eller ett konto om du vill konfigurera priser för produktkataloger. Ange inga produktkatalogpriser i projektprislistorna. Projektprislistor är exklusiva för Project Operations. Programspecifik affärslogik kopierar prislistorna från en offert till ett kontrakt. Resultatet är en kontraktspecifik projektprislista. Kopieringen kan fördröja offertvinsten om projektprislistan i offerten blir för stor. Produktprislistor kopieras inte för att skapa anpassade prislistor i kontrakt. Eftersom ingen kopiering förekommer påverkas inte offertprocessens prestanda.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]