---
title: Lös självkostnader för projektberäkningar och utfall
description: Den här artikeln innehåller information om hur kostnadspriser för projektberäkningar och utfall kan lösas.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c278d8994389145c6dbee7574d2354724d985722
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917552"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Lös självkostnader för projektberäkningar och utfall 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Lösa kostnadstaxa på faktiska rader och beräkningsrader för material

Beräkningsrader för material refererar till offert- och kontraktradsinformation för material och de materialberäkningsrader som finns i ett projekt.

Efter att en kostnadsprislista har lösts använder systemet en kombination av fälten **Produkt** och **Enhet** på uppskattningsraden för att en materiell uppskattning ska matcha mot raderna **Prislisteposter** i den stängda prislistan. Om systemet hittar en produktprisrad med en kostnadsnivå för fältkombinationen **Produkt** och **Enhet** blir kostnadstaxan standard. Om systemet inte kan matcha värdena för **Produkt** och **Enhet** eller om den kan hitta en matchande rad i prislistan men prissättningsmetoden baseras på standardkostnad eller aktuell kostnad och ingen av dem definieras på produkten, är enhetskostnaden som standard noll.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
