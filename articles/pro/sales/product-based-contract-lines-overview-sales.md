---
title: Produktbaserade kontraktrader - lite
description: I det här ämnet finns information om produktbaserade kontraktrader.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272680"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="444f9-103">Produktbaserade kontraktrader - lite</span><span class="sxs-lookup"><span data-stu-id="444f9-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="444f9-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="444f9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="444f9-105">Du kan skapa produktbaserade kontraktrader i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="444f9-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="444f9-106">Produktbaserade kontraktrader kan vara manuellt skapade rader eller vara artiklar från produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="444f9-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="444f9-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="444f9-107">Product catalog</span></span>

<span data-ttu-id="444f9-108">Produkterna i produktkatalogen har en standardenhet och enhetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="444f9-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="444f9-109">Om flera produkter delar samma uppsättning attribut kan du skapa en produktfamilj som även har dessa attribut.</span><span class="sxs-lookup"><span data-stu-id="444f9-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="444f9-110">Alla produkter i samma produktfamilj ärver samma uppsättning attribut.</span><span class="sxs-lookup"><span data-stu-id="444f9-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="444f9-111">Ett företag säljer till exempel prenumerationslicenser för olika sorters program.</span><span class="sxs-lookup"><span data-stu-id="444f9-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="444f9-112">Alla prenumerationsprogram har följande två attribut:</span><span class="sxs-lookup"><span data-stu-id="444f9-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="444f9-113">Antal användare</span><span class="sxs-lookup"><span data-stu-id="444f9-113">Number of users</span></span>
- <span data-ttu-id="444f9-114">Prenumerationens varaktighet (i månader)</span><span class="sxs-lookup"><span data-stu-id="444f9-114">Subscription duration (in months)</span></span>

<span data-ttu-id="444f9-115">Om du vill behålla den här typen av katalog skapar du en produktfamilj som heter **Prenumerationsprogramvara**.</span><span class="sxs-lookup"><span data-stu-id="444f9-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="444f9-116">Lägg till attributen **Antal användare** och **Prenumerationens varaktighet** i produktfamiljen.</span><span class="sxs-lookup"><span data-stu-id="444f9-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="444f9-117">Lägg sedan till enskilda produkter i produktfamiljen **Prenumerationsprogram**.</span><span class="sxs-lookup"><span data-stu-id="444f9-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="444f9-118">Lägga till produktkatalogartiklar i ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="444f9-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="444f9-119">Projektkontrakt har avsnitt för två typer av rader: projektbaserade och produktbaserade.</span><span class="sxs-lookup"><span data-stu-id="444f9-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="444f9-120">Produktbaserade rader innehåller alla produkter och enheter i produktprislistan i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="444f9-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="444f9-121">Produkter som inte ingår i kontraktets produktprislista kan läggas till.</span><span class="sxs-lookup"><span data-stu-id="444f9-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="444f9-122">Du kan välja produkter från andra prislistor eller direkt från produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="444f9-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="444f9-123">När du väljer produkter direkt från en produktkatalog används standardprislistan för produkten för produktens försäljningspris.</span><span class="sxs-lookup"><span data-stu-id="444f9-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="444f9-124">Om ingen standardprislista har angetts sätts priset till 0 (noll).</span><span class="sxs-lookup"><span data-stu-id="444f9-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="444f9-125">Om en kontraktrad bygger på en produktkatalog kan du åsidosätta försäljningspriset direkt på raden.</span><span class="sxs-lookup"><span data-stu-id="444f9-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="444f9-126">En kontraktrad har fältet **Prissättning** med de två värdena:</span><span class="sxs-lookup"><span data-stu-id="444f9-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="444f9-127">**Åsidosätt prissättning**</span><span class="sxs-lookup"><span data-stu-id="444f9-127">**Override pricing**</span></span>
- <span data-ttu-id="444f9-128">**Använd standard**</span><span class="sxs-lookup"><span data-stu-id="444f9-128">**Use default**</span></span>

<span data-ttu-id="444f9-129">Om du här fältet **Prissättning** till **Åsidosätt prissättning** ställs inget standardpris in.</span><span class="sxs-lookup"><span data-stu-id="444f9-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="444f9-130">Ange ett pris för produkten på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="444f9-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="444f9-131">Om du ställer in fältet på **Använd standard** används standardförsäljningspriset och fältet kan inte redigeras.</span><span class="sxs-lookup"><span data-stu-id="444f9-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="444f9-132">När du har installerat Project Operations anges standardförsäljningspriserna på de produktbaserade raderna i ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="444f9-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="444f9-133">Fältet **Prissättning** anges till **Åsidosätt prissättning** så att du kan redigera standardpriset på kontraktraderna.</span><span class="sxs-lookup"><span data-stu-id="444f9-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="444f9-134">Det här är en Project Operations-specifik åsidosättning av beteendet hos projektbaserade rader i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="444f9-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]