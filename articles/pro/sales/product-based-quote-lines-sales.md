---
title: Produktbaserade offertrader - lite
description: I det här ämnet finns information om att arbeta med projektbaserade offertrader.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272590"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="41ca3-103">Produktbaserade offertrader - lite</span><span class="sxs-lookup"><span data-stu-id="41ca3-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="41ca3-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="41ca3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="41ca3-105">Du kan skapa produktbaserade offertrader i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="41ca3-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="41ca3-106">Produktbaserade offertrader kan läggas till manuellt eller vara artiklar från produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="41ca3-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="41ca3-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="41ca3-107">Product catalog</span></span>

<span data-ttu-id="41ca3-108">Vara produkterna i en produktkatalog har en standardenhet och enhetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="41ca3-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="41ca3-109">Om flera produkter delar samma uppsättning attribut kan du skapa en produktfamilj som delar dessa attribut.</span><span class="sxs-lookup"><span data-stu-id="41ca3-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="41ca3-110">Ett företag säljer till exempel prenumerationslicenser för olika sorters program.</span><span class="sxs-lookup"><span data-stu-id="41ca3-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="41ca3-111">Alla prenumerationsprogram har följande två attribut:</span><span class="sxs-lookup"><span data-stu-id="41ca3-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="41ca3-112">Antal användare</span><span class="sxs-lookup"><span data-stu-id="41ca3-112">Number of users</span></span>
- <span data-ttu-id="41ca3-113">Prenumerationens varaktighet i månader</span><span class="sxs-lookup"><span data-stu-id="41ca3-113">A subscription duration measured in months</span></span>

<span data-ttu-id="41ca3-114">För att upprätthålla den här typen av katalog är att skapa en produktfamilj som heter **prenumerationsprogram** och lägga till antalet användare och prenumerationens varaktighet som attribut.</span><span class="sxs-lookup"><span data-stu-id="41ca3-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="41ca3-115">Härnäst kan du lägga till enskilda produkter i produktfamiljen **prenumerationsprogram**.</span><span class="sxs-lookup"><span data-stu-id="41ca3-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="41ca3-116">Lägg till produktkatalogartiklar i en projektoffert</span><span class="sxs-lookup"><span data-stu-id="41ca3-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="41ca3-117">Sidorna **Projektofferter** och **projektkontrakt** har avsnitt för projektbaserade rader och produktbaserade rader.</span><span class="sxs-lookup"><span data-stu-id="41ca3-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="41ca3-118">För produktbaserade rader inkluderar listrutan på offertraden eller projektkontraktraden innehåller alla produkter och enheter i produktprislistan.</span><span class="sxs-lookup"><span data-stu-id="41ca3-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="41ca3-119">Du kan även lägga till produkter som inte ingår i produktprislista.</span><span class="sxs-lookup"><span data-stu-id="41ca3-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="41ca3-120">Dessutom kan du välja produkter från andra prislistor eller direkt från produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="41ca3-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="41ca3-121">När du väljer produkter direkt från en produktkatalog används standardprislistan för produkten för att hämta produktens försäljningspris.</span><span class="sxs-lookup"><span data-stu-id="41ca3-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="41ca3-122">Om ingen standardprislista har angetts sätts priset till (0).</span><span class="sxs-lookup"><span data-stu-id="41ca3-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="41ca3-123">När en offertrad bygger på en produktkatalog kan du åsidosätta försäljningspriset direkt på offertraden.</span><span class="sxs-lookup"><span data-stu-id="41ca3-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="41ca3-124">En offertrad i fältet **prissättning** med två tillgängliga värden:</span><span class="sxs-lookup"><span data-stu-id="41ca3-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="41ca3-125">**Åsidosätt prissättning**</span><span class="sxs-lookup"><span data-stu-id="41ca3-125">**Override Pricing**</span></span>
- <span data-ttu-id="41ca3-126">**Använd standard**</span><span class="sxs-lookup"><span data-stu-id="41ca3-126">**Use Default**</span></span>

<span data-ttu-id="41ca3-127">Om du väljer **Åsidosätt prissättning** är inte standardpriset angivet.</span><span class="sxs-lookup"><span data-stu-id="41ca3-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="41ca3-128">Du måste istället ange ett pris för produkten på offertraden.</span><span class="sxs-lookup"><span data-stu-id="41ca3-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="41ca3-129">Om du väljer **Använd standard** används standard försäljningspriset och fältet är låst för redigering.</span><span class="sxs-lookup"><span data-stu-id="41ca3-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="41ca3-130">Standardförsäljningspriser anges på de produktbaserade raderna i en offert.</span><span class="sxs-lookup"><span data-stu-id="41ca3-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="41ca3-131">Fältet **Prissättning** anges sedan till **åsidosätta prissättning** så att du kan redigera standardpriset på offertraderna.</span><span class="sxs-lookup"><span data-stu-id="41ca3-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="41ca3-132">Det här är en projektrelaterad åsidosättning av projekt för de produktbaserade radfunktionerna i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="41ca3-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]