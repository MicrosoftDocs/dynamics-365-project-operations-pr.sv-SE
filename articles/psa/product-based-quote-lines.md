---
title: Produktbaserade offertrader
description: I det här ämnet finns information om produktbaserade offertrader.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284110"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="736e9-103">Produktbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="736e9-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="736e9-104">Du kan skapa produktbaserade offertrader i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="736e9-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="736e9-105">Produktbaserade offertrader kan vara "skriva in" eller vara artiklar från produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="736e9-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="736e9-106">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="736e9-106">Product catalog</span></span>

<span data-ttu-id="736e9-107">Produkterna i en Dynamics 365-produktkatalog har en standardenhet och enhetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="736e9-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="736e9-108">Om flera produkter delar samma uppsättning attribut kan du skapa en produktfamilj som även har dessa attribut.</span><span class="sxs-lookup"><span data-stu-id="736e9-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="736e9-109">Alla produkter i samma produktfamilj ärver samma uppsättning attribut.</span><span class="sxs-lookup"><span data-stu-id="736e9-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="736e9-110">Ett företag säljer till exempel prenumerationslicenser för en mängd olika program.</span><span class="sxs-lookup"><span data-stu-id="736e9-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="736e9-111">Alla prenumerationsprogram har följande två attribut:</span><span class="sxs-lookup"><span data-stu-id="736e9-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="736e9-112">Antal användare</span><span class="sxs-lookup"><span data-stu-id="736e9-112">Number of users</span></span> 
- <span data-ttu-id="736e9-113">Prenumerationens varaktighet (i månader)</span><span class="sxs-lookup"><span data-stu-id="736e9-113">Subscription duration (in months)</span></span>

<span data-ttu-id="736e9-114">Ett bra sätt att upprätthålla den här typen av katalog är att skapa en produktfamilj som heter **prenumerationsprogram** och som har **antal användare** och **prenumerationens varaktighet** som attribut.</span><span class="sxs-lookup"><span data-stu-id="736e9-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="736e9-115">Du kan sedan lägga till enskilda produkter, till **Dynamics 365 Sales** eller **Dynamics 365 Field Service** till produktfamiljen **prenumerationsprogram**.</span><span class="sxs-lookup"><span data-stu-id="736e9-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="736e9-116">Lägga till produktkatalogartiklar i en projektoffert</span><span class="sxs-lookup"><span data-stu-id="736e9-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="736e9-117">Projektofferter och projektkontraktsidor har avsnitt för två typer av rader: projektbaserade rader och produktbaserade rader.</span><span class="sxs-lookup"><span data-stu-id="736e9-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="736e9-118">För produktbaserade rader används Dynamics 365 för att lägga till objekt från en produktkatalog i en offert.</span><span class="sxs-lookup"><span data-stu-id="736e9-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="736e9-119">Listrutan på offertraden eller projektkontraktraden innehåller alla produkter och enheter i produktprislistan som är kopplade till offerten eller projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="736e9-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="736e9-120">Du kan även lägga till produkter som inte ingår i offertens produktprislista.</span><span class="sxs-lookup"><span data-stu-id="736e9-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="736e9-121">Dessutom kan du välja produkter från andra prislistor eller välja produkter direkt från produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="736e9-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="736e9-122">När du väljer produkter direkt från en produktkatalog används standardprislistan för produkten för att hämta produktens försäljningspris.</span><span class="sxs-lookup"><span data-stu-id="736e9-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="736e9-123">Om ingen standardprislista har angetts sätts priset till 0 (noll).</span><span class="sxs-lookup"><span data-stu-id="736e9-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="736e9-124">Om en offertrad bygger på en produktkatalog kan du åsidosätta försäljningspriset direkt på offertraden.</span><span class="sxs-lookup"><span data-stu-id="736e9-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="736e9-125">Observera att en offertrad i fältet Dynamics 365 har fältet **prissättning**.</span><span class="sxs-lookup"><span data-stu-id="736e9-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="736e9-126">Två värden är tillgängliga:</span><span class="sxs-lookup"><span data-stu-id="736e9-126">Two values are available:</span></span>

- <span data-ttu-id="736e9-127">Åsidosätt prissättning</span><span class="sxs-lookup"><span data-stu-id="736e9-127">Override pricing</span></span>  
- <span data-ttu-id="736e9-128">Använd standard</span><span class="sxs-lookup"><span data-stu-id="736e9-128">Use default</span></span>

<span data-ttu-id="736e9-129">Om du anger det här fältet till **Åsidosätt prissättning** anger Dynamics 365 inte något standardpris.</span><span class="sxs-lookup"><span data-stu-id="736e9-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="736e9-130">Du måste ange ett pris för produkten på offertraden.</span><span class="sxs-lookup"><span data-stu-id="736e9-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="736e9-131">Om du anger det här fältet till **använd standard** använder Dynamics 365 standardförsäljningspriset och låser fältet för att förhindra redigering.</span><span class="sxs-lookup"><span data-stu-id="736e9-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="736e9-132">När du har installerat PSA anges standardförsäljningspriserna på de produktbaserade raderna i en offert.</span><span class="sxs-lookup"><span data-stu-id="736e9-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="736e9-133">Fältet **Prissättning** anges sedan till **åsidosätta prissättning** så att du kan redigera standardpriset på offertraderna.</span><span class="sxs-lookup"><span data-stu-id="736e9-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Ställa in åsidosätta prissättning](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="736e9-135">Kvantitetsfaktorer för produkter</span><span class="sxs-lookup"><span data-stu-id="736e9-135">Quantity factors for products</span></span>

<span data-ttu-id="736e9-136">I PSA används kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter.</span><span class="sxs-lookup"><span data-stu-id="736e9-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="736e9-137">För prenumerationsbaserade produkter uttrycks kvantitet på offert- eller projektkontraktraden som antalet användarmånader.</span><span class="sxs-lookup"><span data-stu-id="736e9-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="736e9-138">Vanligt vis lagras priset på prenumerationsprogram i katalogen som priset per användare i månaden.</span><span class="sxs-lookup"><span data-stu-id="736e9-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="736e9-139">Du kan emellertid använda andra tidsbeskrivningar i stället.</span><span class="sxs-lookup"><span data-stu-id="736e9-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="736e9-140">Under försäljningsprocessen är priset på offertraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av IT-säljaren.</span><span class="sxs-lookup"><span data-stu-id="736e9-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="736e9-141">Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="736e9-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="736e9-142">Den kvantitet som används för att beräkna beloppet på offertraden är en produkt av antalet användare och antalet prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="736e9-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="736e9-143">För att kunna stödja den här typen av försäljning introducerade PSA begreppet kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="736e9-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="736e9-144">För kvantitetskategorin förlitar sig sig på produktattribut i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="736e9-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="736e9-145">När du konfigurerar specifika egenskaper för en produkt kan du använda PSA för att flagga en del uppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="736e9-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="736e9-146">PSA verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="736e9-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="736e9-147">När en produkt som du har konfigurerat kvantitetsfaktorer för läggs till på en offertrad blir fältet **kvantitet** på offertraden skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="736e9-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="736e9-148">När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknar PSA kvantiteten på offertraden.</span><span class="sxs-lookup"><span data-stu-id="736e9-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="736e9-149">Dynamics 365 kan till exempel ha följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="736e9-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="736e9-150">**Antal användare** - antalet användare</span><span class="sxs-lookup"><span data-stu-id="736e9-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="736e9-151">**Antal månader** - antalet prenumerationsmånader</span><span class="sxs-lookup"><span data-stu-id="736e9-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="736e9-152">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="736e9-152">**Product SKU**</span></span> 

<span data-ttu-id="736e9-153">Egenskaperna **Antal användare** och **Antal för månader** kan flaggas som kvantitetsrapporter genom att egenskaperna för produktraden redigeras.</span><span class="sxs-lookup"><span data-stu-id="736e9-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Flaggantalet användare och inga månader som kvalitetsfaktorer](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]