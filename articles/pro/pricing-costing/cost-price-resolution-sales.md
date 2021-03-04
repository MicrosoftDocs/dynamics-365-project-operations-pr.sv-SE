---
title: Lös självkostnader för beräkningar och utfall – Lite
description: I det här ämnet finns information om hur du löser självkostnader för uppskattningar och faktiska värden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764616"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Lös självkostnader för beräkningar och utfall – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Om du vill lösa självkostnader och prislistan för självkostnad för uppskattningar och faktiska värden använder systemet informationen i fälten **Datum**, **Valuta** och **Kontrakterande enhet** i det relaterade projektet. När prislistan för självkostnad har lösts löser programmet kostnadstaxan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Lösa kostnadstaxor på faktiska och uppskattade rader för tid

Uppskattningsrader för tid refererar till offert- och kontraktradsinformation för tids- och resurstilldelningar i ett projekt.

När en kostnadsprislista har lösts matchas fälten **Roll** och **Resursenhet** på uppskattningsraden för Tid mot rollprisraderna i prislistan. Denna matchning förutsätter att du använder standardprissättningsdimensionerna för arbetskostnad. Om du konfigurerade systemet för att matcha fält i stället för, eller utöver, **Roll** och **Resursenhet** används en annan kombination för att hämta en matchande rollprisrad. Om programmet hittar en rollprisrad som har en kostnadstaxa för kombinationen av **Roll** och **Resursenhet**, är detta standardkostnaden. Om programmet inte kan matcha värdena **Roll** och **Resursenhet** hämtar det rollprisrader med en matchande roll, men null-värden för **Resursenheten**. När den har en matchande rollprispost hämtas kostnadstaxan som standard från den posten. 

> [!NOTE]
> Om du konfigurerar en annan prioritering av **Roll** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det här beteendet i enlighet med detta. Systemet hämtar rollprisposter med värden som matchar alla dimensionsvärden för prissättning i prioritetsordning med rader som har null-värden för de dimensionerna sist.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Lösa kostnadstaxor på faktiska och uppskattade rader för utgift

Uppskattningsrader för utgift refererar till offert- och kontraktradsinformation för rader för utgift och utgiftsuppskattning i ett projekt.

När en självkostnadslista har lösts använder systemet en kombination av fälten **Kategori** och **Enhet** på utgiftsuppskattningsraden för att matcha mot raderna **Kategoripris** i den lösta prislistan. Om systemet hittar en kategoriprisrad som har en kostnadstaxa för kombinationen av fälten **Kategori** och **Enhet** används kostnadstaxan som standard. Om systemet inte kan matcha värdena **Kategori** och **Enhet**, eller om det går att hitta en matchande kategoriprisrad, men prismodellen inte är **Pris per enhet**, kommer standardkostnaden att nollställas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]