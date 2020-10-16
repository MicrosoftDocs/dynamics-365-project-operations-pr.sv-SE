---
title: Hantera komplexa enheter som per användare, per månad för produktbaserade offertrader
description: I det här ämnet finns information om hur du hanterar komplexa enheter för produktbaserade offertrader.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965901"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="f62d4-103">Hantera komplexa enheter som per användare, per månad för produktbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="f62d4-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="f62d4-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="f62d4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f62d4-105">I Dynamics 365 Project Operations används kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter.</span><span class="sxs-lookup"><span data-stu-id="f62d4-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="f62d4-106">För prenumerationsbaserade produkter uttrycks kvantitet på offert- eller projektkontraktraden som antalet användarmånader.</span><span class="sxs-lookup"><span data-stu-id="f62d4-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="f62d4-107">Vanligt vis lagras priset på prenumerationsprogram i katalogen som priset per användare i månaden.</span><span class="sxs-lookup"><span data-stu-id="f62d4-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="f62d4-108">Under försäljningsprocessen är priset på offertraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av IT-säljaren.</span><span class="sxs-lookup"><span data-stu-id="f62d4-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="f62d4-109">Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="f62d4-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="f62d4-110">Den kvantitet som används för att beräkna offertraden är en produkt av antalet användare och antalet prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="f62d4-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="f62d4-111">För att kunna stödja den här typen av försäljning introducerade Project Operations begreppet kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="f62d4-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="f62d4-112">För kvantitetskategorin förlitar sig sig på produktattribut i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f62d4-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="f62d4-113">När du konfigurerar specifika egenskaper för en produkt kan du använda Project Operations för att flagga en deluppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="f62d4-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="f62d4-114">Project Operations verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="f62d4-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="f62d4-115">När du lägger till en produkt med kvantitetsfaktorer på en offertrad blir fältet **Kvantitet** skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="f62d4-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="f62d4-116">När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknar Project Operations kvantiteten på offertraden.</span><span class="sxs-lookup"><span data-stu-id="f62d4-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="f62d4-117">Dynamics 365 Sales kan till exempel ha följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="f62d4-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="f62d4-118">**Antal användare**: antalet användare</span><span class="sxs-lookup"><span data-stu-id="f62d4-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="f62d4-119">**Antal månader**: antalet prenumerationsmånader</span><span class="sxs-lookup"><span data-stu-id="f62d4-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="f62d4-120">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="f62d4-120">**Product SKU**</span></span>

<span data-ttu-id="f62d4-121">Du kan flagga egenskaperna **Antal användare** och **Antal för månader** som kvantitetsfaktorer genom att egenskaperna för produktraden redigeras.</span><span class="sxs-lookup"><span data-stu-id="f62d4-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="f62d4-122">Följ stegen nedan om du vill skapa kvantitetsfaktorer från produktegenskaper:</span><span class="sxs-lookup"><span data-stu-id="f62d4-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="f62d4-123">I vänster navigeringsfönster i Project Operations går du till **Försäljning** > **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="f62d4-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="f62d4-124">Öppna den produkt som du behöver konfigurera kvantitetsfaktorer för.</span><span class="sxs-lookup"><span data-stu-id="f62d4-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="f62d4-125">Kontrollera att produkten har egenskaper som redan är konfigurerade.</span><span class="sxs-lookup"><span data-stu-id="f62d4-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="f62d4-126">På sidan **Projektinformation** för produkten väljer du fliken **Kvantitetsfaktorer**.</span><span class="sxs-lookup"><span data-stu-id="f62d4-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="f62d4-127">I underrutnätet väljer du **+ Ny fältberäkning**.</span><span class="sxs-lookup"><span data-stu-id="f62d4-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="f62d4-128">Ange namnet på kvantitetsfaktorn och välj egenskapsvärdet som mappas till fältberäkningen.</span><span class="sxs-lookup"><span data-stu-id="f62d4-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="f62d4-129">Spara och stäng formuläret.</span><span class="sxs-lookup"><span data-stu-id="f62d4-129">Save and close the form.</span></span> <span data-ttu-id="f62d4-130">Upprepa de här stegen för alla egenskaper som ska användas för att beräkna kvantiteten för den produktbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="f62d4-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="f62d4-131">När du skapar en produktbaserad offertrad för en produkt blir antalet offerter automatiskt låsta.</span><span class="sxs-lookup"><span data-stu-id="f62d4-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="f62d4-132">Antalet beräknas som en produkt av de egenskapsvärden som du har angett för den offertraden.</span><span class="sxs-lookup"><span data-stu-id="f62d4-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
