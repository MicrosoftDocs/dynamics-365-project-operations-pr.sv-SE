---
title: Lös försäljningspriser för beräkningar och utfall – Lite
description: I det här ämnet finns information om hur du löser försäljningspriser för uppskattningar och faktiska värden.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25620704570fa702e1e5e09c83005be50f98f20a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274525"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Lös försäljningspriser för beräkningar och utfall – Lite

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]