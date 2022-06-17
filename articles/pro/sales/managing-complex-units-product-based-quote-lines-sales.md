---
title: Hantera komplexa enheter som per användare, per månad för produktbaserade offertrader - lite
description: Den här artikeln innehåller information om hur du hanterar komplexa enheter för produktbaserade offertrader.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929926"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Hantera komplexa enheter som per användare, per månad för produktbaserade offertrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Dynamics 365 Project Operations används kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter. För prenumerationsbaserade produkter uttrycks kvantitet på offert- eller projektkontraktraden som antalet användarmånader.

Vanligt vis lagras priset på prenumerationsprogram i katalogen som priset per användare i månaden. Under försäljningsprocessen är priset på offertraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av IT-säljaren. Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader. Den kvantitet som används för att beräkna offertraden är en produkt av antalet användare och antalet prenumerationsmånader.

För att kunna stödja den här typen av försäljning introducerade Project Operations begreppet kvantitetsfaktorer. För kvantitetskategorin förlitar sig sig på produktattribut i Dynamics 365. När du konfigurerar specifika egenskaper för en produkt kan du använda Project Operations för att flagga en deluppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.

Project Operations verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer. När du lägger till en produkt med kvantitetsfaktorer på en offertrad blir fältet **Kvantitet** skrivskyddat. När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknar Project Operations kvantiteten på offertraden.

Dynamics 365 Sales kan till exempel ha följande egenskaper:

- **Antal användare**: antalet användare
- **Antal månader**: antalet prenumerationsmånader
- **Produkt-SKU**

Du kan flagga egenskaperna **Antal användare** och **Antal för månader** som kvantitetsfaktorer genom att egenskaperna för produktraden redigeras.

Följ stegen nedan om du vill skapa kvantitetsfaktorer från produktegenskaper:

1. I vänster navigeringsfönster i Project Operations går du till **Försäljning** > **Produkter**.
2. Öppna den produkt som du behöver konfigurera kvantitetsfaktorer för. Kontrollera att produkten har egenskaper som redan är konfigurerade.
3. På sidan **Projektinformation** för produkten väljer du fliken **Kvantitetsfaktorer**.
4. I underrutnätet väljer du **+ Ny fältberäkning**.
5. Ange namnet på kvantitetsfaktorn och välj egenskapsvärdet som mappas till fältberäkningen.
6. Spara och stäng formuläret. Upprepa de här stegen för alla egenskaper som ska användas för att beräkna kvantiteten för den produktbaserade offertraden.

När du skapar en produktbaserad offertrad för en produkt blir antalet offerter automatiskt låsta. Antalet beräknas som en produkt av de egenskapsvärden som du har angett för den offertraden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]