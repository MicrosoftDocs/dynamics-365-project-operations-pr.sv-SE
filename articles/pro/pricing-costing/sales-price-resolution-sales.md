---
title: Lös försäljningspriser för projektberäkningar och utfall
description: Det här avsnittet innehåller information om lösa försäljningspriser på projektberäkningar och utfall.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2152b3f59050482cab0d1c5940d6743f420206bfc90e034dc2d754df8bd513a5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996098"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Lös försäljningspriser för projektberäkningar och utfall

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

När försäljningspriser på uppskattningar och faktiska värden löses i Dynamics 365 Project Operations använder systemet först datum och valuta för den relaterade projektofferten eller kontraktet för att lösa försäljningsprislistan. När försäljningsprislistan har lösts löser systemet försäljnings- eller fakturataxan.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Lösa försäljningstaxor på rader för faktiska värden och uppskattningar för tid

I Project Operations används uppskattningsrader för tid för att ange information om offertrader och kontraktrader för tid och resurstilldelningar för projektet.

När en prislista för försäljning har lösts slutför systemet följande steg för att standardisera fakturataxan.

1. Systemet använder fälten **Roll** och **Resursenhet** på uppskattningsraden för tid så att den stämmer överens med rollprisraderna i den lösta prislistan. Matchningen förutsätter att du använder de medföljande prissättningsdimensionerna för fakturataxa. Om du har konfigurerat prissättning utifrån något annat fält i stället för, eller utöver, **Roll** och **Resursenhet** används den kombinationen för att hämta en matchande rollprisrad.
2. Om systemet hittar en rollprisrad som har en fakturataxa för kombinationen av fälten **Roll** och **Resursenhet**, är den fakturataxan standard.
3. Om systemet inte kan matcha värdena för fälten **Roll** och **Resursenhet** hämtar det rollprisrader med en matchande roll, men null-värden för **Resursenheten**. När en matchande rollprispost hittas används fakturataxan från den posten som standard. Matchningen förutsätter en färdig konfiguration för den relativa prioriteten hos **Roll** mot **Resursenhet** som en försäljningsprissättningsdimension.

> [!NOTE]
> Om du konfigurerar en annan prioritering av **Roll** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det här beteendet i enlighet med detta. Systemet hämtar rollprisposter med värden som matchar alla dimensionsvärden för prissättning i prioritetsordning med rader som har null-värden för de dimensionerna sist.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Lösa försäljningstaxor på rader för faktiska värden och uppskattningar för utgift

I Project Operations används uppskattningsrader för utgift för att ange information om offertrader och kontraktrader för utgift och utgiftsuppskattningsrader för projektet.

När en prislista för försäljning har lösts slutför systemet följande steg för att standardisera styckpriset.

1. Systemet använder kombinationen av fälten **Kategori** och **Enhet** på uppskattningsraden för utgift för att matcha mot kategoriprisraderna i prislistan som löstes.
2. Om systemet hittar en kategoriprisrad som har en försäljningstaxa för kombinationen av fälten **Kategori** och **Enhet** används försäljningstaxan som standard.
3. Om en matchande kategoriprisrad hittas i systemet kan prissättningsmetoden användas för att standardisera försäljningspriset. I följande tabell nedan visas standardiseringen av utgiftspriset i Project Operations.

    | Sammanhang | Prismodell | Standardpris |
    | --- | --- | --- |
    | Beräkning | Pris per enhet | Baserat på kategoriprisraden |
    | &nbsp; | Vid kostnad | 0.00 |
    | &nbsp; | Pålägg över kostnad | 0.00 |
    | Faktisk | Pris per enhet | Baserat på kategoriprisraden |
    | &nbsp; | Vid kostnad | Utifrån den relaterade faktiska kostnaden |
    | &nbsp; | Pålägg över kostnad | Tillämpa ett pålägg enligt definitionen på kategoriprisraden i enhetens kostnadstaxa för relaterade faktiska kostnadsvärden |

4. Om systemet inte kan matcha värdena i fälten **Kategori** och **Enhet** blir försäljningstaxan som standard noll (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Lösa försäljningstaxa på faktiska rader och beräkningsrader för material

I Project Operations, beräkningsrader för material används till att ange offert- och kontraktradsinformation för material och de materialberäkningsrader som finns i ett projekt.

När en prislista för försäljning har lösts slutför systemet följande steg för att standardisera styckpriset.

1. Systemet använder kombinationen av fälten **produkt** och **enhet** på beräkningsraden för material för att matcha mot prislisteobjektraderna i den prislista som löstes.
2. Om systemet hittar en prislista artikelrad som har en försäljningsgrad för fälten **Produkt** och **Enhet** kombination och prissättning är **Valutabelopp**, det försäljningspris som anges på prislistan används.
3. Om värdena i fältet **Produkt** och **Enhet** inte matchar standardvärdet noll.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
