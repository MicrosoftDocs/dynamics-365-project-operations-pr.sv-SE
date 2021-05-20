---
title: Hantera projektbaserade affärsmöjligheter
description: I det här ämnet finns information om hur du arbetar med affärsmöjligheter som är relaterade till projekt.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948442"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="607c0-103">Hantera projektbaserade affärsmöjligheter</span><span class="sxs-lookup"><span data-stu-id="607c0-103">Manage project-based opportunities</span></span>

<span data-ttu-id="607c0-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="607c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="607c0-105">Projektbaserade företag har vanligtvis sina operationer för leveransspridning i flera länder och geografier.</span><span class="sxs-lookup"><span data-stu-id="607c0-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="607c0-106">Kostnaden för projektkörningen och leveransen kan variera beroende på vilken geografi eller avdelning som hanterar leveransen.</span><span class="sxs-lookup"><span data-stu-id="607c0-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="607c0-107">Detta kan i sin tur påverka avtalets marginaler.</span><span class="sxs-lookup"><span data-stu-id="607c0-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="607c0-108">Leverans av projektbaserade tjänster innebär vanligtvis stora kvantiteter mänsklig tid, avsevärda kostnader för resor, materialkostnader och andra utgifter.</span><span class="sxs-lookup"><span data-stu-id="607c0-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="607c0-109">Projektbaserade affärsmöjligheter i Dynamics 365 Project Operations har utformats med tillägg till Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="607c0-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="607c0-110">I ämnet finns information om de olika fälten och affärslogiken i de ytterligare funktioner som krävs av projektbaserade företag för att hantera projektbaserade affärsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="607c0-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="607c0-111">Visa alla projektbaserade affärsmöjligheter</span><span class="sxs-lookup"><span data-stu-id="607c0-111">View all project-based opportunities</span></span>

<span data-ttu-id="607c0-112">En lista över alla projektbaserade affärsmöjligheter kan ses från listsidan **Affärsmöjlighet**.</span><span class="sxs-lookup"><span data-stu-id="607c0-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="607c0-113">Gå till **Försäljning** > **Affärsmöjligheter**.</span><span class="sxs-lookup"><span data-stu-id="607c0-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="607c0-114">Använd **Vyväxlare** för att välja andra filtrerade vyer av affärsmöjligheterna.</span><span class="sxs-lookup"><span data-stu-id="607c0-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="607c0-115">Du kan skapa egna vyer med anpassade filtervillkor för att konfigurera dessa vyer och navigeringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="607c0-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="607c0-116">Projektmöjligheter kan skapas eller tas bort från den här listsidan eller informationssidan.</span><span class="sxs-lookup"><span data-stu-id="607c0-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="607c0-117">Affärsprocessflöde för projektbaserade affärer</span><span class="sxs-lookup"><span data-stu-id="607c0-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="607c0-118">Följande affärsprocessflöden stöds för projektbaserade affärer i Project Operations:</span><span class="sxs-lookup"><span data-stu-id="607c0-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="607c0-119">Affärsprocessen Lead till affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="607c0-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="607c0-120">Affärsmöjlighet, försäljningsprocess</span><span class="sxs-lookup"><span data-stu-id="607c0-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="607c0-121">Affärsprocessen Lead till affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="607c0-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="607c0-122">Affärsprocessen Lead till affärsmöjlighet stöder följande steg:</span><span class="sxs-lookup"><span data-stu-id="607c0-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="607c0-123">Scen</span><span class="sxs-lookup"><span data-stu-id="607c0-123">Stage</span></span> | <span data-ttu-id="607c0-124">Mappad entitet</span><span class="sxs-lookup"><span data-stu-id="607c0-124">Mapped entity</span></span> | <span data-ttu-id="607c0-125">Funktioner</span><span class="sxs-lookup"><span data-stu-id="607c0-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="607c0-126">Kvalificera</span><span class="sxs-lookup"><span data-stu-id="607c0-126">Qualify</span></span> | <span data-ttu-id="607c0-127">Lead</span><span class="sxs-lookup"><span data-stu-id="607c0-127">Lead</span></span> | <span data-ttu-id="607c0-128">Kvalificera lead för att skapa ett konto, en kontakt och en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="607c0-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="607c0-129">Ta fram</span><span class="sxs-lookup"><span data-stu-id="607c0-129">Develop</span></span> | <span data-ttu-id="607c0-130">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="607c0-130">Opportunity</span></span> | <span data-ttu-id="607c0-131">Utveckla affärsmöjligheten och lägg till mer information om det arbete som ingår, viktiga intressenter och konkurrens.</span><span class="sxs-lookup"><span data-stu-id="607c0-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="607c0-132">Föreslå</span><span class="sxs-lookup"><span data-stu-id="607c0-132">Propose</span></span> | <span data-ttu-id="607c0-133">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="607c0-133">Opportunity</span></span> | <span data-ttu-id="607c0-134">Utarbeta förslaget och få godkännande från det interna granskningsteamet.</span><span class="sxs-lookup"><span data-stu-id="607c0-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="607c0-135">Stängning</span><span class="sxs-lookup"><span data-stu-id="607c0-135">Close</span></span> | <span data-ttu-id="607c0-136">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="607c0-136">Opportunity</span></span> | <span data-ttu-id="607c0-137">Vinn affärsmöjligheten för att stänga affären.</span><span class="sxs-lookup"><span data-stu-id="607c0-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="607c0-138">Affärsmöjlighet, försäljningsprocess</span><span class="sxs-lookup"><span data-stu-id="607c0-138">Opportunity sales process</span></span>
<span data-ttu-id="607c0-139">Affärsmöjlighetens försäljningsprocess i Project Operations är ett tillägg till affärsflöde för affärsmöjlighetens försäljningsprocess i programmet Sales.</span><span class="sxs-lookup"><span data-stu-id="607c0-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="607c0-140">Affärsprocessen är utformad för att stödja följande stadier i en projektbaserad affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="607c0-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="607c0-141">Scen</span><span class="sxs-lookup"><span data-stu-id="607c0-141">Stage</span></span> | <span data-ttu-id="607c0-142">Mappad entitet</span><span class="sxs-lookup"><span data-stu-id="607c0-142">Mapped entity</span></span> | <span data-ttu-id="607c0-143">Funktioner</span><span class="sxs-lookup"><span data-stu-id="607c0-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="607c0-144">Kvalificera</span><span class="sxs-lookup"><span data-stu-id="607c0-144">Qualify</span></span> | <span data-ttu-id="607c0-145">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="607c0-145">Opportunity</span></span> | <span data-ttu-id="607c0-146">Kvalificera lead för att skapa ett konto, en kontakt och en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="607c0-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="607c0-147">Föreslå</span><span class="sxs-lookup"><span data-stu-id="607c0-147">Propose</span></span> | <span data-ttu-id="607c0-148">Offert</span><span class="sxs-lookup"><span data-stu-id="607c0-148">Quote</span></span> | <span data-ttu-id="607c0-149">Utarbeta förslaget med hjälp av offerter och få godkännande från det interna granskningsteamet.</span><span class="sxs-lookup"><span data-stu-id="607c0-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="607c0-150">Kontrakt</span><span class="sxs-lookup"><span data-stu-id="607c0-150">Contract</span></span> | <span data-ttu-id="607c0-151">Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="607c0-151">Project Contract</span></span> | <span data-ttu-id="607c0-152">Vinn offerten för att skapa kontraktet och påbörja körning och leverans av projektet.</span><span class="sxs-lookup"><span data-stu-id="607c0-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="607c0-153">Stängning</span><span class="sxs-lookup"><span data-stu-id="607c0-153">Close</span></span> | <span data-ttu-id="607c0-154">Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="607c0-154">Project Contract</span></span> | <span data-ttu-id="607c0-155">Slutför arbetet och stäng projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="607c0-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="607c0-156">Om ditt projektbaserade avtal har inletts med en lead ges affärsprocessen Lead till affärsmöjlighet företräde.</span><span class="sxs-lookup"><span data-stu-id="607c0-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="607c0-157">Om ditt projektbaserade avtal har inletts med en affärsmöjlighet ges försäljningsprocessen för affärsmöjligheten företräde.</span><span class="sxs-lookup"><span data-stu-id="607c0-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="607c0-158">Du kan redigera produktens affärsprocessflöde eller skapa egna affärsprocessflöden för att spåra din försäljningsprocess efter behov.</span><span class="sxs-lookup"><span data-stu-id="607c0-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="607c0-159">Mer information om affärsprocessflödet finns i [Översikt över affärsprocessflöden](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="607c0-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]