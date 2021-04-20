---
title: Produktprislistor
description: I det här ämne finns information om prislistorna för katalogpriser som används för projektofferter och kontrakt.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877513"
---
# <a name="product-price-lists"></a><span data-ttu-id="98302-103">Produktprislistor</span><span class="sxs-lookup"><span data-stu-id="98302-103">Product price lists</span></span>

<span data-ttu-id="98302-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="98302-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="98302-105">I Project Operations, **Produktprislistor** och relaterad prislistepost stöder funktionen för prissättning av produkter på produktbaserade offert- och avtalsrader.</span><span class="sxs-lookup"><span data-stu-id="98302-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="98302-106">För produkter som används i projekt används prislisteobjektposterna för projektprislistor.</span><span class="sxs-lookup"><span data-stu-id="98302-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="98302-107">Produkterna bör konfigureras så att de har standardkostnads- och prislistor i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="98302-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="98302-108">Använda listpris, standardkostnad och aktuell kostnad om du vill konfigurera standardkostnad och listpriser.</span><span class="sxs-lookup"><span data-stu-id="98302-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="98302-109">Standardprislista används endast på en offertrad eller i en projektkontraktrad om systemet inte kan hitta en prislisterad för produkten i produktprislistan för offert eller projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="98302-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="98302-110">Självkostnaden för produktkatalograder kan ändras mellan offerter.</span><span class="sxs-lookup"><span data-stu-id="98302-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="98302-111">Det här är viktigt eftersom du inte behöver följa upp kostnaderna noggrant, men du kan inte ange driftsvinster för projektåtaganden.</span><span class="sxs-lookup"><span data-stu-id="98302-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="98302-112">Som standard används produktens standardkostnad som självkostnad.</span><span class="sxs-lookup"><span data-stu-id="98302-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="98302-113">Standardsjälvkostnaden kan emellertid uppdateras på offertraden om det finns ett annat självkostnadspris för offerten.</span><span class="sxs-lookup"><span data-stu-id="98302-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="98302-114">Prislisteposter</span><span class="sxs-lookup"><span data-stu-id="98302-114">Price list items</span></span>

<span data-ttu-id="98302-115">Du kan lägga till produkter från en produktkatalog i olika prislistor.</span><span class="sxs-lookup"><span data-stu-id="98302-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="98302-116">Prislistrader för produkter refererar alltid till en specifik enhet.</span><span class="sxs-lookup"><span data-stu-id="98302-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="98302-117">Priser för en produkt på prislisteposter kan konfigureras som ett valutabelopp.</span><span class="sxs-lookup"><span data-stu-id="98302-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="98302-118">Du kan även konfigurera den som en funktion i listpris, aktuell kostnad eller standardkostnad.</span><span class="sxs-lookup"><span data-stu-id="98302-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="98302-119">Prisfunktioner stöder olika avrundningsalternativ när produktpriser konfigureras som en funktion i listpriset, standardkostnad eller aktuell kostnad.</span><span class="sxs-lookup"><span data-stu-id="98302-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="98302-120">Förutom att använda flera prissättningsmetoder och avrundningsalternativ kan du associera rabattlistor med prislisteposter.</span><span class="sxs-lookup"><span data-stu-id="98302-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="98302-121">Standardprislista för en produkt.</span><span class="sxs-lookup"><span data-stu-id="98302-121">Default product price list</span></span>
<span data-ttu-id="98302-122">Varje kundpost har ett fält för **standardprislista** där du kan ange en prislista som överensstämmer med kundens valuta.</span><span class="sxs-lookup"><span data-stu-id="98302-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="98302-123">Ett standardvärde anges inte automatiskt i det här fältet.</span><span class="sxs-lookup"><span data-stu-id="98302-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="98302-124">När ett anpassat prissättningsavtal med en viss kund finns kan du använda det här fältet för att associera en prislista med den kunden.</span><span class="sxs-lookup"><span data-stu-id="98302-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="98302-125">Entiteterna affärsmöjlighet, offert och projektkontrakt använder följande ordning för att ange standardprislistor för produkter.</span><span class="sxs-lookup"><span data-stu-id="98302-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="98302-126">Samma order används för prislistor för projekt.</span><span class="sxs-lookup"><span data-stu-id="98302-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="98302-127">Offert</span><span class="sxs-lookup"><span data-stu-id="98302-127">Quote</span></span>
2.  <span data-ttu-id="98302-128">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="98302-128">Opportunity</span></span>
3.  <span data-ttu-id="98302-129">Kund</span><span class="sxs-lookup"><span data-stu-id="98302-129">Customer</span></span>
4.  <span data-ttu-id="98302-130">Globala inställningar</span><span class="sxs-lookup"><span data-stu-id="98302-130">Global settings</span></span> 

<span data-ttu-id="98302-131">Som standard listar fältet **produkt** på offertraden alla aktiva produkter i offertens produktprislista.</span><span class="sxs-lookup"><span data-stu-id="98302-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="98302-132">Om en produkt har inaktiverats eller om det är en utkast produkt visas den inte, även om den är i prislistan.</span><span class="sxs-lookup"><span data-stu-id="98302-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="98302-133">Produktkatalograder läggs till som fakturarader på den första fakturan som skapas för ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="98302-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="98302-134">På en utkastfaktura kan dessa fakturarader tas bort.</span><span class="sxs-lookup"><span data-stu-id="98302-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="98302-135">I så fall visas raderna på en efterföljande faktura tills de har fakturerats, eller tills fakturan skickas till kunden.</span><span class="sxs-lookup"><span data-stu-id="98302-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="98302-136">Du kan inte fakturera en del av en produktfakturarad.</span><span class="sxs-lookup"><span data-stu-id="98302-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="98302-137">När produktraderna från projektkontraktet faktureras skapas verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="98302-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="98302-138">De faktiska värdena länkas emellertid inte till den relaterade projektentiteten.</span><span class="sxs-lookup"><span data-stu-id="98302-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="98302-139">Produkter som bygger på projektkontraktrader är med andra ord oberoende av projektbaserade användningstider.</span><span class="sxs-lookup"><span data-stu-id="98302-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
