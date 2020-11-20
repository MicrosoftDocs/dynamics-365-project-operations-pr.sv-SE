---
title: Lösa självkostnader för uppskattningar och faktiska värden
description: I det här ämnet finns information om hur du löser självkostnader för uppskattningar och faktiska värden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119719"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Lösa självkostnader för uppskattningar och faktiska värden

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Om du vill lösa självkostnader och prislistan för självkostnad för uppskattningar och faktiska värden använder systemet informationen i fälten **Datum**, **Valuta** och **Kontrakterande enhet** i det relaterade projektet. När prislistan för självkostnad har lösts löser programmet kostnadstaxan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Lösa kostnadstaxor på faktiska och uppskattade rader för tid

Uppskattningsrader för tid refererar till offert- och kontraktradsinformation för tids- och resurstilldelningar i ett projekt.

När en kostnadsprislista har lösts använder systemet fälten **Roll**, **Resursföretag** och **Resursenhet** på uppskattningsraden för tid så att den stämmer överens med rollprisraderna i prislistan. Matchningen förutsätter att du använder de medföljande prissättningsdimensionerna för arbetskostnaden. Om du konfigurerade systemet för att matcha fält i stället för, eller utöver, **Roll**, **Resursföretaget** och **Resursenhet** används en annan kombination för att hämta en matchande rollprisrad. Om programmet hittar en rollprisrad som har en kostnadstaxa för kombinationen av **Roll**, **Resursföretag** och **Resursenhet**, är detta standardkostnaden. Om programmet inte kan matcha värdena **Roll**, **Resursföretag** och **Resursenhet** hämtar det rollprisrader med en matchande roll, men null-värden för **Resursenheten**. När den har en matchande rollprispost hämtas kostnadstaxan som standard från den posten. 

> [!NOTE]
> Om du konfigurerar en annan prioritering av **Roll**, **Resursföretag** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det här beteendet i enlighet med detta. Systemet hämtar rollprisposter med värden som matchar alla dimensionsvärden för prissättning i prioritetsordning med rader som har null-värden för de dimensionerna sist.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Lösa kostnadstaxor på faktiska och uppskattade rader för utgift

Uppskattningsrader för utgift refererar till offert- och kontraktradsinformation för rader för utgift och utgiftsuppskattning i ett projekt.

När en kostnadsprislista har lösts använder systemet en kombination av fälten **Kategori** och **Enhet** på uppskattningsraden för en utgift så att den stämmer överens med raderna **Kategoripris** i den lösta prislistan. Om systemet hittar en kategoriprisrad som har en kostnadstaxa för kombinationen av fälten **Kategori** och **Enhet** används kostnadstaxan som standard. Om systemet inte kan matcha värdena **Kategori** och **Enhet**, eller om det går att hitta en matchande kategoriprisrad, men prissättningsmetoden inte är **Pris per enhet**, är kostnadstaxan som standard inställd på noll (0).
