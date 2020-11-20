---
title: Lösa försäljningspriser för uppskattningar och faktiska värden
description: I det här ämnet finns information om hur du löser försäljningstaxor för uppskattningar och faktiska värden.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119575"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Lösa försäljningspriser för uppskattningar och faktiska värden

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

När försäljningspriser i uppskattningar och faktiska värden löses i Dynamics 365 Project Operations används först datumet och valutan för den relaterade projektofferten eller kontraktet för att lösa försäljningsprislistan. När försäljningsprislistan har lösts löser systemet försäljnings- eller fakturataxan.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Lösa försäljningstaxor på rader för faktiska värden och uppskattningar för tid

I Project Operations används uppskattningsrader för tid för att ange information om offertrader och kontraktrader för tid och resurstilldelningar för projektet.

När en prislista för försäljning har lösts slutför systemet följande steg för att standardisera fakturataxan.

1. Systemet använder fälten **Roll**, **Resursföretag** och **Resursenhet** på uppskattningsraden för tid så att den stämmer överens med rollprisraderna i den lösta prislistan. Matchningen förutsätter att du använder de medföljande prissättningsdimensionerna för fakturataxa. Om du har konfigurerat prissättning utifrån något annat fält i stället för, eller utöver, **Roll**, **Resursföretaget** och **Resursenhet** används den kombinationen för att hämta en matchande rollprisrad.
2. Om systemet hittar en rollprisrad som har en fakturataxa för kombinationen av fälten **Roll**, **Resursföretag** och **Resursenhet**, är den fakturataxan standard.
3. Om systemet inte kan matcha värdena för fälten **Roll**, **Resursföretag** och **Resursenhet** hämtar det rollprisrader med en matchande roll, men null-värden för **Resursenheten**. När en matchande rollprispost hittas används fakturataxan från den posten som standard. Matchningen förutsätter en färdig konfiguration för den relativa prioriteten hos **Roll** mot **Resursenhet** som en försäljningsprissättningsdimension.

> [!NOTE]
> Om du konfigurerade en annan prioritering av **Roll**, **Resursföretag** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det här beteendet i enlighet med detta. Systemet hämtar rollprisposter med värden som matchar alla dimensionsvärden för prissättning i prioritetsordning med rader som har null-värden för de dimensionerna sist.

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
    | &nbsp; | Pålägg över kostnad | Genom att tillämpa ett pålägg enligt definitionen på kategoriprisraden i enhetens kostnadstaxa för relaterade faktiska kostnadsvärden |

4. Om systemet inte kan matcha värdena i fälten **Kategori** och **Enhet** blir försäljningstaxan som standard noll (0).