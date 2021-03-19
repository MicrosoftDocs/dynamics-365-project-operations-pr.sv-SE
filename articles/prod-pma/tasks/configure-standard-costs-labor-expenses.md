---
title: Konfigurera standardkostnader för arbete och utgifter
description: I det här ämnet beskrivs hur du skapar standardkostnader för arbete och utgifter för ett projekt.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288356"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="3b290-103">Konfigurera standardkostnader för arbete och utgifter</span><span class="sxs-lookup"><span data-stu-id="3b290-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b290-104">I det här ämnet beskrivs hur du skapar standardkostnader för arbete och utgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="3b290-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="3b290-105">I den här uppgiften används USSI-datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="3b290-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3b290-106">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > självkostnad (timme)**.</span><span class="sxs-lookup"><span data-stu-id="3b290-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="3b290-107">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="3b290-107">Select **New**.</span></span>
3. <span data-ttu-id="3b290-108">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="3b290-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="3b290-109">Ange ett nummer i fältet **självkostnad**.</span><span class="sxs-lookup"><span data-stu-id="3b290-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="3b290-110">Du kan ange en standard självkostnad för projektkategorin, eller så kan du ange att en självkostnad ska vara efter arbetsnummer, projektnummer, kategori, datum eller någon kombination av dessa.</span><span class="sxs-lookup"><span data-stu-id="3b290-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="3b290-111">Den självkostnad som används är den självkostnad som har den högsta detaljnivån.</span><span class="sxs-lookup"><span data-stu-id="3b290-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="3b290-112">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="3b290-112">Select **Save**.</span></span>
6. <span data-ttu-id="3b290-113">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > försäljningskostnad (timme)**.</span><span class="sxs-lookup"><span data-stu-id="3b290-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="3b290-114">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="3b290-114">Select **New**.</span></span>
8. <span data-ttu-id="3b290-115">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="3b290-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="3b290-116">I fältet **Giltig för**, välj ett alternativ.</span><span class="sxs-lookup"><span data-stu-id="3b290-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="3b290-117">I fältet **Prissättning** anger du ett nummer.</span><span class="sxs-lookup"><span data-stu-id="3b290-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="3b290-118">Du kan ange ett standard försäljningspris för timtransaktioner eller för en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="3b290-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="3b290-119">Du kan också ange försäljningspriser efter arbetsnummer, projektnummer, kategori, transaktionsdatum eller någon kombination av dessa.</span><span class="sxs-lookup"><span data-stu-id="3b290-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="3b290-120">Det faktiska försäljningspriset, som används när en arbetare registrerar en transaktion i timjournalen, är försäljningspriset på den högsta detaljnivån.</span><span class="sxs-lookup"><span data-stu-id="3b290-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="3b290-121">Om t.ex. både ett allmänt försäljningspris och ett arbetar försäljningspris är inställda används det arbetsspecifika försäljningspriset.</span><span class="sxs-lookup"><span data-stu-id="3b290-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="3b290-122">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="3b290-122">Select **Save**.</span></span>
12. <span data-ttu-id="3b290-123">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="3b290-123">Close the page.</span></span>
13. <span data-ttu-id="3b290-124">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > självkostnad (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="3b290-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="3b290-125">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="3b290-125">Select **New**.</span></span>
15. <span data-ttu-id="3b290-126">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="3b290-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="3b290-127">Ange ett nummer i fältet **självkostnad**.</span><span class="sxs-lookup"><span data-stu-id="3b290-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="3b290-128">Du kan fylla i flera fält, men det är det minsta som krävs för att spara posten.</span><span class="sxs-lookup"><span data-stu-id="3b290-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="3b290-129">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="3b290-129">Select **Save**.</span></span>
18. <span data-ttu-id="3b290-130">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > försäljningspris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="3b290-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="3b290-131">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="3b290-131">Select **New**.</span></span>
20. <span data-ttu-id="3b290-132">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="3b290-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="3b290-133">I fältet **Giltig för**, välj ett alternativ.</span><span class="sxs-lookup"><span data-stu-id="3b290-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="3b290-134">I fältet **Prissättning** anger du ett nummer.</span><span class="sxs-lookup"><span data-stu-id="3b290-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="3b290-135">Det faktiska försäljningspriset, som används när en arbetare registrerar transaktioner i en utgiftsjournal, är försäljningspriset på den högsta detaljnivån.</span><span class="sxs-lookup"><span data-stu-id="3b290-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="3b290-136">Om t.ex. både ett allmänt och ett arbetar försäljningspris är inställda används det arbetsspecifika försäljningspriset.</span><span class="sxs-lookup"><span data-stu-id="3b290-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="3b290-137">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="3b290-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]