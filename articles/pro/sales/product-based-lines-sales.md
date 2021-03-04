---
title: Produktbaserade affärsmöjlighetsrader - lite
description: I det här ämnet finns information om produktbaserade poster i affärsmöjlighetsraden i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764976"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="08843-103">Produktbaserade affärsmöjlighetsrader - lite</span><span class="sxs-lookup"><span data-stu-id="08843-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="08843-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="08843-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="08843-105">Produkterbaserade affärsmöjlighetsrader är radartiklar i affärsmöjligheten.</span><span class="sxs-lookup"><span data-stu-id="08843-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="08843-106">De olika radobjekten finns på den faktura som i slutändan ges till kunden.</span><span class="sxs-lookup"><span data-stu-id="08843-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="08843-107">Fakturan innehåller inga ytterligare tjänster.</span><span class="sxs-lookup"><span data-stu-id="08843-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="08843-108">Den tillhörande utgiften och förbrukningen spåras inte i uppgifter i relaterade projekt.</span><span class="sxs-lookup"><span data-stu-id="08843-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="08843-109">Produktbaserade rader kan vara katalogartiklar eller oregistrerade produkter.</span><span class="sxs-lookup"><span data-stu-id="08843-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="08843-110">De flesta funktioner i en affärsmöjlighets produktbaserade rader följer funktionerna i programmet Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="08843-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="08843-111">Mer information om produktbaserade affärsmöjlighetsrader finns i [Lägga till produkter i en affärsmöjlighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="08843-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="08843-112">**Kundbudget** är ett koncept som är specifikt för projektbaserade affärsmöjlighetsrader.</span><span class="sxs-lookup"><span data-stu-id="08843-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="08843-113">I fältet **Kundbudget** spårar du det belopp som kunden är villig att betala för artikeln.</span><span class="sxs-lookup"><span data-stu-id="08843-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="08843-114">När intäktsmetoden för sammanfattningen för affärsmöjlighet är **Systemberäknad** sammanfattas kundbudgetvärdena över affärsmöjlighetsraderna i syfte att beräkna den beräknade omsättningen.</span><span class="sxs-lookup"><span data-stu-id="08843-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

