---
title: Produktbaserade affärsmöjlighetsrader - lite
description: I det här ämnet finns information om produktbaserade poster i affärsmöjlighetsraden i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176362"
---
# <a name="product-based-opportunity-lines---lite"></a>Produktbaserade affärsmöjlighetsrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Produkterbaserade affärsmöjlighetsrader är radartiklar i affärsmöjligheten. Dessa rader levereras till kunden som distinkta radartiklar på den eventuella fakturan utan några andra mervärdestjänster. Den tillhörande utgiften och förbrukningen spåras inte i uppgifter i relaterade projekt.

Produktbaserade rader kan vara katalogartiklar eller oregistrerade produkter. De flesta funktioner i en affärsmöjlighets produktbaserade rader följer funktionerna i programmet Dynamics 365 Sales. Mer information om produktbaserade affärsmöjlighetsrader finns i [Lägga till produkter i en affärsmöjlighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Ett koncept för produktbaserade affärsmöjlighetsrader som är specifika för projektbaserade affärsmöjligheter är **Kundbudget**. Använd det här fältet om du vill spåra det belopp kunden är villig att betala för radartikeln.

Om intäktsmetoden för affärsmöjlighetens sammanfattning är inställd på **System beräknat**, summeras kundbudgeten från produkt- och projektbaserade rader för att beräkna den uppskattade intäkten.
