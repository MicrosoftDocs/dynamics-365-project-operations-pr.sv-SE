---
title: Lösa självkostnader för uppskattningar och faktiska värden
description: I det här ämnet finns information om hur du löser självkostnader för uppskattningar och faktiska värden.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7395a1845f4a895efbabda36ba3b2a2f3c1eea52
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587930"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Lösa självkostnader för uppskattningar och faktiska värden

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Om du vill lösa självkostnader och prislistan för självkostnad för uppskattningar och faktiska värden använder systemet informationen i fälten **Datum**, **Valuta** och **Kontrakterande enhet** i det relaterade projektet. När prislistan för självkostnad har lösts löser programmet kostnadstaxan.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Lösa kostnadstaxor på faktiska och uppskattade rader för tid

Uppskattningsrader för tid refererar till offert- och kontraktradsinformation för tids- och resurstilldelningar i ett projekt.

När en kostnadsprislista har lösts använder systemet fälten **Roll**, **Resursföretag** och **Resursenhet** på uppskattningsraden för tid så att den stämmer överens med rollprisraderna i prislistan. Matchningen förutsätter att du använder de medföljande prissättningsdimensionerna för arbetskostnaden. Om du konfigurerade systemet för att matcha fält i stället för, eller utöver, **Roll**, **Resursföretaget** och **Resursenhet** används en annan kombination för att hämta en matchande rollprisrad. Om programmet hittar en rollprisrad som har en kostnadstaxa för kombinationen av **Roll**, **Resursföretag** och **Resursenhet**, är detta standardkostnaden. Om applikationen inte kan matcha exakt kombinationen av värdena **Roll**, **Resursföretag** och **Resursenhet** hämtas rollprisrader med ett matchande rollvärde, men har null-värden för **Resursenhet** och **Resursföretag**. När en matchande rollprispost med matchande rollprisvärde påträffats beräknas standardkostnaden för den posten. 

> [!NOTE]
> Om du konfigurerar en annan prioritering av **Roll**, **Resursföretag** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det här beteendet i enlighet med detta. Systemet hämtar rollprisposter med värden som matchar var och en av värdena för prisdimension i prioritetsordning med rader som har nollvärden för de dimensioner som kommer sist i prioritetsordningen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Lösa kostnadstaxor på faktiska och uppskattade rader för utgift

Uppskattningsrader för utgift refererar till offert- och kontraktradsinformation för rader för utgift och utgiftsuppskattning i ett projekt.

När en kostnadsprislista har lösts använder systemet en kombination av fälten **Kategori** och **Enhet** på uppskattningsraden för en utgift så att den stämmer överens med raderna **Kategoripris** i den lösta prislistan. Om systemet hittar en kategoriprisrad som har en kostnadstaxa för kombinationen av fälten **Kategori** och **Enhet** används kostnadstaxan som standard. Om systemet inte kan matcha värdena **Kategori** och **Enhet**, eller om det går att hitta en matchande kategoriprisrad, men prissättningsmetoden inte är **Pris per enhet**, är kostnadstaxan som standard inställd på noll (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Lösa kostnadstaxa på faktiska rader och beräkningsrader för material

Beräkningsrader för material refererar till offert- och kontraktradsinformation för material och de materialberäkningsrader som finns i ett projekt.

Efter att en kostnadsprislista har lösts använder systemet en kombination av fälten **Produkt** och **Enhet** på uppskattningsraden för att en materiell uppskattning ska matcha mot raderna **Prislisteposter** i den stängda prislistan. Om systemet hittar en produktprisrad med en kostnadsnivå för fältkombinationen **Produkt** och **Enhet** blir kostnadstaxan standard. Om systemet inte kan matcha värdena för **Produkt** och **Enhet** kommer enhetskostnaden att vara noll som standard. Standardinställningen kan också inträffa om det finns en matchande prislisteobjektrad, men prismodellen baseras på en standardkostnad eller aktuell kostnad som inte definieras i produkten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
