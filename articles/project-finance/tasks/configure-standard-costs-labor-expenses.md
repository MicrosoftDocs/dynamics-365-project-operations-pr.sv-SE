---
title: Konfigurera standardkostnader för arbete och utgifter
description: I det här ämnet beskrivs hur du skapar standardkostnader för arbete och utgifter för ett projekt.
author: KimANelson
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
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756307"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="b538d-103">Konfigurera standardkostnader för arbete och utgifter</span><span class="sxs-lookup"><span data-stu-id="b538d-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b538d-104">I det här ämnet beskrivs hur du skapar standardkostnader för arbete och utgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b538d-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="b538d-105">I den här uppgiften används USSI-datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b538d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b538d-106">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > självkostnad (timme)**.</span><span class="sxs-lookup"><span data-stu-id="b538d-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="b538d-107">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="b538d-107">Select **New**.</span></span>
3. <span data-ttu-id="b538d-108">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="b538d-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="b538d-109">Ange ett nummer i fältet **självkostnad**.</span><span class="sxs-lookup"><span data-stu-id="b538d-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="b538d-110">Du kan ange en standard självkostnad för projektkategorin, eller så kan du ange att en självkostnad ska vara efter arbetsnummer, projektnummer, kategori, datum eller någon kombination av dessa.</span><span class="sxs-lookup"><span data-stu-id="b538d-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="b538d-111">Den självkostnad som används är den självkostnad som har den högsta detaljnivån.</span><span class="sxs-lookup"><span data-stu-id="b538d-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="b538d-112">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b538d-112">Select **Save**.</span></span>
6. <span data-ttu-id="b538d-113">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > försäljningskostnad (timme)**.</span><span class="sxs-lookup"><span data-stu-id="b538d-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="b538d-114">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="b538d-114">Select **New**.</span></span>
8. <span data-ttu-id="b538d-115">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="b538d-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="b538d-116">I fältet **Giltig för**, välj ett alternativ.</span><span class="sxs-lookup"><span data-stu-id="b538d-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="b538d-117">I fältet **Prissättning** anger du ett nummer.</span><span class="sxs-lookup"><span data-stu-id="b538d-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="b538d-118">Du kan ange ett standard försäljningspris för timtransaktioner eller för en projektkategori.</span><span class="sxs-lookup"><span data-stu-id="b538d-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="b538d-119">Du kan också ange försäljningspriser efter arbetsnummer, projektnummer, kategori, transaktionsdatum eller någon kombination av dessa.</span><span class="sxs-lookup"><span data-stu-id="b538d-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="b538d-120">Det faktiska försäljningspriset, som används när en arbetare registrerar en transaktion i timjournalen, är försäljningspriset på den högsta detaljnivån.</span><span class="sxs-lookup"><span data-stu-id="b538d-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b538d-121">Om t.ex. både ett allmänt försäljningspris och ett arbetar försäljningspris är inställda används det arbetsspecifika försäljningspriset.</span><span class="sxs-lookup"><span data-stu-id="b538d-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="b538d-122">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b538d-122">Select **Save**.</span></span>
12. <span data-ttu-id="b538d-123">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="b538d-123">Close the page.</span></span>
13. <span data-ttu-id="b538d-124">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > självkostnad (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="b538d-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="b538d-125">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="b538d-125">Select **New**.</span></span>
15. <span data-ttu-id="b538d-126">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="b538d-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="b538d-127">Ange ett nummer i fältet **självkostnad**.</span><span class="sxs-lookup"><span data-stu-id="b538d-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="b538d-128">Du kan fylla i flera fält, men det är det minsta som krävs för att spara posten.</span><span class="sxs-lookup"><span data-stu-id="b538d-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="b538d-129">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b538d-129">Select **Save**.</span></span>
18. <span data-ttu-id="b538d-130">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > försäljningspris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="b538d-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="b538d-131">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="b538d-131">Select **New**.</span></span>
20. <span data-ttu-id="b538d-132">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="b538d-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="b538d-133">I fältet **Giltig för**, välj ett alternativ.</span><span class="sxs-lookup"><span data-stu-id="b538d-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="b538d-134">I fältet **Prissättning** anger du ett nummer.</span><span class="sxs-lookup"><span data-stu-id="b538d-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="b538d-135">Det faktiska försäljningspriset, som används när en arbetare registrerar transaktioner i en utgiftsjournal, är försäljningspriset på den högsta detaljnivån.</span><span class="sxs-lookup"><span data-stu-id="b538d-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b538d-136">Om t.ex. både ett allmänt och ett arbetar försäljningspris är inställda används det arbetsspecifika försäljningspriset.</span><span class="sxs-lookup"><span data-stu-id="b538d-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="b538d-137">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b538d-137">Select **Save**.</span></span>

