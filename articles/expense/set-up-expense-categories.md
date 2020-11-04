---
title: Konfigurera utgiftskategorier
description: I det här ämnet finns information om hur du konfigurerar utgiftskategorier och delade kategorier för utgiftsrapporter.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085430"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="e6dd9-103">Konfigurera utgiftskategorier</span><span class="sxs-lookup"><span data-stu-id="e6dd9-103">Set up expense categories</span></span>

<span data-ttu-id="e6dd9-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="e6dd9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e6dd9-105">När medarbetarna skapar utgiftsrapporter måste varje utgiftspost vara associerad med en utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="e6dd9-106">Utgiftskategorier härleds från delade kategorier som kan delas av alla juridiska entiteter i organisationen.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="e6dd9-107">Beroende på hur organisationen har definierats kan de här utgiftskategorierna även delas i andra områden.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="e6dd9-108">Baserat på definitionen av din organisation och vägledning från implementeringsteamet måste du avgöra om kategorierna som används i utgiftshantering endast ska användas i utgifts hantering eller delas i andra områden.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="e6dd9-109">Dessa kategorier kan delas mellan projekthantering och redovisnings- och utgiftshantering, eller mellan projekthantering och redovisning och produktion.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="e6dd9-110">De kan emellertid inte delas mellan utgiftshantering och produktion.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="e6dd9-111">Innan du kan börja konfigurationsprocessen måste följande beslut göras för varje utgiftskategori:</span><span class="sxs-lookup"><span data-stu-id="e6dd9-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="e6dd9-112">Vilken är utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-112">What is the expense category?</span></span> <span data-ttu-id="e6dd9-113">Exempel är kategorier för flygningar, hotell och sträcka.</span><span class="sxs-lookup"><span data-stu-id="e6dd9-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="e6dd9-114">Kan utgiftskategorin också användas i projekthantering och redovisning?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="e6dd9-115">Om den kan det måste du också fatta följande beslut:</span><span class="sxs-lookup"><span data-stu-id="e6dd9-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="e6dd9-116">Vilka kostnadskonton ska användas för följande utgifter?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="e6dd9-117">Kostnad</span><span class="sxs-lookup"><span data-stu-id="e6dd9-117">Cost</span></span>
        - <span data-ttu-id="e6dd9-118">Löneallokering</span><span class="sxs-lookup"><span data-stu-id="e6dd9-118">Payroll allocation</span></span>
        - <span data-ttu-id="e6dd9-119">PIA-kostnadsvärde</span><span class="sxs-lookup"><span data-stu-id="e6dd9-119">WIP-cost value</span></span>
        - <span data-ttu-id="e6dd9-120">Kostnadsartikel</span><span class="sxs-lookup"><span data-stu-id="e6dd9-120">Cost-item</span></span>
        - <span data-ttu-id="e6dd9-121">PIA-kostnad värdeartikel</span><span class="sxs-lookup"><span data-stu-id="e6dd9-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="e6dd9-122">Upplupen förlust</span><span class="sxs-lookup"><span data-stu-id="e6dd9-122">Accrued loss</span></span>
        - <span data-ttu-id="e6dd9-123">PIA, upplupen förlust</span><span class="sxs-lookup"><span data-stu-id="e6dd9-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="e6dd9-124">Vilka intäktskonton ska användas för följande intäktskällor?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="e6dd9-125">Fakturerad intäkt</span><span class="sxs-lookup"><span data-stu-id="e6dd9-125">Invoiced revenue</span></span>
        - <span data-ttu-id="e6dd9-126">Upplupna intäkter – försäljningsvärde</span><span class="sxs-lookup"><span data-stu-id="e6dd9-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="e6dd9-127">Pia – försäljningsvärde</span><span class="sxs-lookup"><span data-stu-id="e6dd9-127">WIP-sales value</span></span>
        - <span data-ttu-id="e6dd9-128">Upplupna intäkter – produktion</span><span class="sxs-lookup"><span data-stu-id="e6dd9-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="e6dd9-129">PIA – Produktion</span><span class="sxs-lookup"><span data-stu-id="e6dd9-129">WIP-production</span></span>
        - <span data-ttu-id="e6dd9-130">Upplupna intäkter – vinst</span><span class="sxs-lookup"><span data-stu-id="e6dd9-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="e6dd9-131">PIA – vinst</span><span class="sxs-lookup"><span data-stu-id="e6dd9-131">WIP-profit</span></span>
        - <span data-ttu-id="e6dd9-132">Upplupna intäkter – prenumeration</span><span class="sxs-lookup"><span data-stu-id="e6dd9-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="e6dd9-133">PIA-prenumeration</span><span class="sxs-lookup"><span data-stu-id="e6dd9-133">WIP-subscription</span></span>

- <span data-ttu-id="e6dd9-134">Vilken är utgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-134">What is the expense type?</span></span>
- <span data-ttu-id="e6dd9-135">Vilken är standardbetalningsmetoden för utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="e6dd9-136">Måste utgifter i utgiftskategorin specificeras?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="e6dd9-137">Vilken är det huvudsakliga standardkontot utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="e6dd9-138">Vad är standardmomsgruppen för utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="e6dd9-139">Är fler betalningsmetoder tillåtna i utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="e6dd9-140">Vilka är dessa i så fall?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-140">If so, what are they?</span></span>
- <span data-ttu-id="e6dd9-141">Finns det några underkategorier i den här utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="e6dd9-142">Om det finns underkategorier måste du också fatta följande beslut:</span><span class="sxs-lookup"><span data-stu-id="e6dd9-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="e6dd9-143">Har någon av underkategorierna exkluderats från momsåterbetalning?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="e6dd9-144">Vad är momsgruppen för underkategorierna?</span><span class="sxs-lookup"><span data-stu-id="e6dd9-144">What is the item sales tax group of the subcategories?</span></span>
