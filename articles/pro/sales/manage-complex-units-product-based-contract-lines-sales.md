---
title: Hantera komplexa enheter för produktbaserade kontraktrader - lite
description: I den här ämne finns information om hur du stöder försäljning av prenumerationsprodukter.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 214593c5b3fbfc5194031af3d3bef59d01750099
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594002"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Hantera komplexa enheter för produktbaserade kontraktrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Dynamics 365 Project Operations används kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter. För prenumerationsbaserade produkter uttrycks kvantitet på kontrakt- eller projektkontraktraden som antalet användarmånader.

Priset lagras på prenumerationsprogram i katalogen som priset per användare i månaden. Under försäljningsprocessen är priset på kontraktraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av säljaren. Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader. Den kvantitet som används för att beräkna beloppet på kontraktraden är en produkt av antalet användare och antalet prenumerationsmånader.

För att kunna stödja den här typen av försäljning stöder Project Operations begreppet *kvantitetsfaktorer*. För kvantitetskategorin förlitar sig sig på produktattribut. När du konfigurerar specifika egenskaper för en produkt kan du använda för att flagga en del uppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.

Project Operations verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer. När en produkt med konfigurerade kvantitetsfaktorer läggs till på en kontraktrad blir fältet **kvantitet** skrivskyddat. När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknar Project Operations kvantiteten på kontraktraden.

Dynamics 365 Sales kan till exempel ha följande egenskaper:

- **Antal användare**: antalet användare.
- **Antal månader**: antalet prenumerationsmånader.
- **Produkt-SKU**: lagerhållningsenhet (SKU) för produkten.

Egenskaperna **Antal användare** och **Antal för månader** kan flaggas som kvantitetsrapporter genom att egenskaperna för produktraden redigeras.

Följ stegen nedan om du vill skapa kvantitetsfaktorer från produktegenskaper.

1. I **Project Operations**, välj **Försäljningsprodukter**.
2. Öppna den produkt som du behöver ange kvantitetsfaktorer för. Kontrollera att någon egenskap redan har konfigurerats för produkten.
3. På sidan **Projektinformation** väljer du fliken **Kvantitetsfaktorer**.
4. I underrutnätet väljer du **+ Ny fältberäkning**.
5. Ange namnet på **kvantitetsfaktorn** och välj egenskapsvärdet som mappas till fältberäkningen.
6. Spara och stäng formuläret.
7. Upprepa steg 2-6 för alla de egenskaper som tillsammans ska utgör kvantiteten för den produktbaserade kontraktraden.

När en användare skapar en kontraktrad för den här produkten är antalet på kontraktraden låst. Antalet beräknas sedan som en produkt av egenskapsvärdena för den kontraktraden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]