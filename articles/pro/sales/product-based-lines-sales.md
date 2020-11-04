---
title: Produktbaserade affärsmöjlighetsrader
description: I det här ämnet finns information om produktbaserade poster i affärsmöjlighetsraden i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085466"
---
# <a name="product-based-opportunity-lines"></a>Produktbaserade affärsmöjlighetsrader

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Produkterbaserade affärsmöjlighetsrader är radartiklar i affärsmöjligheten. Dessa rader levereras till kunden som distinkta radartiklar på den eventuella fakturan utan några andra mervärdestjänster. Den tillhörande utgiften och förbrukningen spåras inte i uppgifter i relaterade projekt.

Produktbaserade rader kan vara katalogartiklar eller oregistrerade produkter. De flesta funktioner i en affärsmöjlighets produktbaserade rader följer funktionerna i programmet Dynamics 365 Sales. Mer information om produktbaserade affärsmöjlighetsrader finns i [Lägga till produkter i en affärsmöjlighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Ett koncept för produktbaserade affärsmöjlighetsrader som är specifika för projektbaserade affärsmöjligheter är **Kundbudget**. Använd det här fältet om du vill spåra det belopp kunden är villig att betala för radartikeln.

Om intäktsmetoden för affärsmöjlighetens sammanfattning är inställd på **System beräknat** , summeras kundbudgeten från produkt- och projektbaserade rader för att beräkna den uppskattade intäkten.
