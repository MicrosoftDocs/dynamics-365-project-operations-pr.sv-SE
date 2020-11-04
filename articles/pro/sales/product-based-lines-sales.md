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
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="64307-103">Produktbaserade affärsmöjlighetsrader</span><span class="sxs-lookup"><span data-stu-id="64307-103">Product-based opportunity lines</span></span>

<span data-ttu-id="64307-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="64307-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="64307-105">Produkterbaserade affärsmöjlighetsrader är radartiklar i affärsmöjligheten.</span><span class="sxs-lookup"><span data-stu-id="64307-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="64307-106">Dessa rader levereras till kunden som distinkta radartiklar på den eventuella fakturan utan några andra mervärdestjänster.</span><span class="sxs-lookup"><span data-stu-id="64307-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="64307-107">Den tillhörande utgiften och förbrukningen spåras inte i uppgifter i relaterade projekt.</span><span class="sxs-lookup"><span data-stu-id="64307-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="64307-108">Produktbaserade rader kan vara katalogartiklar eller oregistrerade produkter.</span><span class="sxs-lookup"><span data-stu-id="64307-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="64307-109">De flesta funktioner i en affärsmöjlighets produktbaserade rader följer funktionerna i programmet Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="64307-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="64307-110">Mer information om produktbaserade affärsmöjlighetsrader finns i [Lägga till produkter i en affärsmöjlighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="64307-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="64307-111">Ett koncept för produktbaserade affärsmöjlighetsrader som är specifika för projektbaserade affärsmöjligheter är **Kundbudget**.</span><span class="sxs-lookup"><span data-stu-id="64307-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="64307-112">Använd det här fältet om du vill spåra det belopp kunden är villig att betala för radartikeln.</span><span class="sxs-lookup"><span data-stu-id="64307-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="64307-113">Om intäktsmetoden för affärsmöjlighetens sammanfattning är inställd på **System beräknat** , summeras kundbudgeten från produkt- och projektbaserade rader för att beräkna den uppskattade intäkten.</span><span class="sxs-lookup"><span data-stu-id="64307-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
