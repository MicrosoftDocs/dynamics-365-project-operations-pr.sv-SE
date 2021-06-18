---
title: Konfigurera koncernintern projektfakturering
description: I det här ämne visas hur du konfigurerar projektfakturering mellan två företag i organisationen.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001223"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="c2d6b-103">Konfigurera koncernintern projektfakturering</span><span class="sxs-lookup"><span data-stu-id="c2d6b-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2d6b-104">I det här ämne visas hur du konfigurerar projektfakturering mellan två företag i organisationen.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="c2d6b-105">I den här uppgiften används USSI-datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c2d6b-106">I navigeringsfönstret går du till **moduler > leverantörsreskontra > leverantörer > alla leverantörer**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c2d6b-107">I listan **Alla leverantörer** leta upp och markera önskad post.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="c2d6b-108">Välj plan i åtgärdsrutan **Allmänt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c2d6b-109">Välj **Koncerninternt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="c2d6b-110">Ställ in **aktiv** till **Ja** för att aktivera koncernintern handel.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="c2d6b-111">I fältet **Kundens företag** ange eller välja ett värde.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="c2d6b-112">I fältet **Mitt konto** ange eller välj ett värde.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="c2d6b-113">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-113">Select **Save**.</span></span>
9. <span data-ttu-id="c2d6b-114">Stäng sidorna för att återgå till startsidan.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="c2d6b-115">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > projektledning och redovisningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="c2d6b-116">Välj fliken **Koncerninternt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="c2d6b-117">Flytta skjutreglaget till **Ja** för att aktivera koncernintern resursplanering och tidrapporter.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="c2d6b-118">Markera den markerade raden i listan.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c2d6b-119">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-119">Select **New**.</span></span>
15. <span data-ttu-id="c2d6b-120">I fältet **låntagande juridisk person** ange eller välj ett värde.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="c2d6b-121">Markera kryssrutan för **periodiserad intäkt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="c2d6b-122">I fältet **Standardkategori för tidsrapport** ange eller välj ett värde.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="c2d6b-123">I fältet **Standardkategori för utgift** ange eller välj ett värde.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="c2d6b-124">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-124">Select **Save**.</span></span>
20. <span data-ttu-id="c2d6b-125">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-125">Close the page.</span></span>
21. <span data-ttu-id="c2d6b-126">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > bokföring > inställning av bokföring**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="c2d6b-127">I fältet **Typer av redovisningskonton** välj ett alternativ.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="c2d6b-128">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-128">Select **New**.</span></span>
24. <span data-ttu-id="c2d6b-129">I fältet **huvudkonto** för den nya raden, ange önskade värden.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="c2d6b-130">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-130">Select **Save**.</span></span>
26. <span data-ttu-id="c2d6b-131">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-131">Close the page.</span></span>
27. <span data-ttu-id="c2d6b-132">I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > överföringspris**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="c2d6b-133">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-133">Select **New**.</span></span>
29. <span data-ttu-id="c2d6b-134">I fältet **Effektivt datum** anger du ett datum.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="c2d6b-135">I fältet **låntagande juridisk person** ange eller välj ett värde.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="c2d6b-136">I fält **Överföringsprismodell** välj alternativ,</span><span class="sxs-lookup"><span data-stu-id="c2d6b-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="c2d6b-137">I fältet **Prissättning** anger du ett nummer.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="c2d6b-138">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="c2d6b-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]