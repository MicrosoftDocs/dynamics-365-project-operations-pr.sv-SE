---
title: Hantera komplexa enheter för produktbaserade kontraktrader - lite
description: I den här ämne finns information om hur du stöder försäljning av prenumerationsprodukter.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273355"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="d3b54-103">Hantera komplexa enheter för produktbaserade kontraktrader - lite</span><span class="sxs-lookup"><span data-stu-id="d3b54-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="d3b54-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="d3b54-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d3b54-105">Dynamics 365 Project Operations används kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter.</span><span class="sxs-lookup"><span data-stu-id="d3b54-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="d3b54-106">För prenumerationsbaserade produkter uttrycks kvantitet på kontrakt- eller projektkontraktraden som antalet användarmånader.</span><span class="sxs-lookup"><span data-stu-id="d3b54-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="d3b54-107">Priset lagras på prenumerationsprogram i katalogen som priset per användare i månaden.</span><span class="sxs-lookup"><span data-stu-id="d3b54-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="d3b54-108">Under försäljningsprocessen är priset på kontraktraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av säljaren.</span><span class="sxs-lookup"><span data-stu-id="d3b54-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="d3b54-109">Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="d3b54-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="d3b54-110">Den kvantitet som används för att beräkna beloppet på kontraktraden är en produkt av antalet användare och antalet prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="d3b54-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="d3b54-111">För att kunna stödja den här typen av försäljning stöder Project Operations begreppet *kvantitetsfaktorer*.</span><span class="sxs-lookup"><span data-stu-id="d3b54-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="d3b54-112">För kvantitetskategorin förlitar sig sig på produktattribut.</span><span class="sxs-lookup"><span data-stu-id="d3b54-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="d3b54-113">När du konfigurerar specifika egenskaper för en produkt kan du använda för att flagga en del uppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="d3b54-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="d3b54-114">Project Operations verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="d3b54-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="d3b54-115">När en produkt med konfigurerade kvantitetsfaktorer läggs till på en kontraktrad blir fältet **kvantitet** skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="d3b54-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="d3b54-116">När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknar Project Operations kvantiteten på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="d3b54-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="d3b54-117">Dynamics 365 Sales kan till exempel ha följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="d3b54-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="d3b54-118">**Antal användare**: antalet användare.</span><span class="sxs-lookup"><span data-stu-id="d3b54-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="d3b54-119">**Antal månader**: antalet prenumerationsmånader.</span><span class="sxs-lookup"><span data-stu-id="d3b54-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="d3b54-120">**Produkt-SKU**: lagerhållningsenhet (SKU) för produkten.</span><span class="sxs-lookup"><span data-stu-id="d3b54-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="d3b54-121">Egenskaperna **Antal användare** och **Antal för månader** kan flaggas som kvantitetsrapporter genom att egenskaperna för produktraden redigeras.</span><span class="sxs-lookup"><span data-stu-id="d3b54-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="d3b54-122">Följ stegen nedan om du vill skapa kvantitetsfaktorer från produktegenskaper.</span><span class="sxs-lookup"><span data-stu-id="d3b54-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="d3b54-123">I **Project Operations**, välj **Försäljningsprodukter**.</span><span class="sxs-lookup"><span data-stu-id="d3b54-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="d3b54-124">Öppna den produkt som du behöver ange kvantitetsfaktorer för.</span><span class="sxs-lookup"><span data-stu-id="d3b54-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="d3b54-125">Kontrollera att någon egenskap redan har konfigurerats för produkten.</span><span class="sxs-lookup"><span data-stu-id="d3b54-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="d3b54-126">På sidan **Projektinformation** väljer du fliken **Kvantitetsfaktorer**.</span><span class="sxs-lookup"><span data-stu-id="d3b54-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="d3b54-127">I underrutnätet väljer du **+ Ny fältberäkning**.</span><span class="sxs-lookup"><span data-stu-id="d3b54-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="d3b54-128">Ange namnet på **kvantitetsfaktorn** och välj egenskapsvärdet som mappas till fältberäkningen.</span><span class="sxs-lookup"><span data-stu-id="d3b54-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="d3b54-129">Spara och stäng formuläret.</span><span class="sxs-lookup"><span data-stu-id="d3b54-129">Save and close the form.</span></span>
7. <span data-ttu-id="d3b54-130">Upprepa steg 2-6 för alla de egenskaper som tillsammans ska utgör kvantiteten för den produktbaserade kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="d3b54-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="d3b54-131">När en användare skapar en kontraktrad för den här produkten är antalet på kontraktraden låst.</span><span class="sxs-lookup"><span data-stu-id="d3b54-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="d3b54-132">Antalet beräknas sedan som en produkt av egenskapsvärdena för den kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="d3b54-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]