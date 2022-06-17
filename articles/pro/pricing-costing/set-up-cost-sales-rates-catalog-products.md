---
title: Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite
description: Den här artikeln innehåller information om hur du anger kostnads- och försäljningstaxa för artiklar i en produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917414"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Att ange priser för produktkatalogsobjekt i Dynamics 365 Project Operations sker på samma sätt som i Dynamics 365 Sales.

I Project Operations kan produkter inte beräknas eller användas i projekt, varför produktkatalogpriser inte behöver anges i projektprislistor för offerter och kontrakt.

Använd fältet **Produktpris** för en offert, ett kontrakt eller ett konto om du vill konfigurera priser för produktkataloger. Ange inga produktkatalogpriser i projektprislistorna. Projektprislistor är exklusiva för Project Operations. Programspecifik affärslogik kopierar prislistorna från en offert till ett kontrakt. Resultatet är en kontraktspecifik projektprislista. Kopieringen kan fördröja offertvinsten om projektprislistan i offerten blir för stor. Produktprislistor kopieras inte för att skapa anpassade prislistor i kontrakt. Eftersom ingen kopiering förekommer påverkas inte offertprocessens prestanda.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]