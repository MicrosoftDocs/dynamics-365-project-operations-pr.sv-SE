---
title: Projektstadier
description: I det här ämnet finns information om de projektstadier som är tillgängliga i Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996948"
---
# <a name="project-stages"></a><span data-ttu-id="b5b5f-103">Projektstadier</span><span class="sxs-lookup"><span data-stu-id="b5b5f-103">Project stages</span></span>

<span data-ttu-id="b5b5f-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b5b5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5b5f-105">Projektstadier designas för att återspegla projektets status allt eftersom det fortlöper.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b5b5f-106">Anpassningar kan användas för att automatiskt uppdatera stadier i flöden för affärsprocesser, Power Automate eller tillägg för plugin-program.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="b5b5f-107">Följande stadier definieras i standardvärdet för affärsprocessflöde:</span><span class="sxs-lookup"><span data-stu-id="b5b5f-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="b5b5f-108">Skapa</span><span class="sxs-lookup"><span data-stu-id="b5b5f-108">New</span></span>
- <span data-ttu-id="b5b5f-109">Offert</span><span class="sxs-lookup"><span data-stu-id="b5b5f-109">Quote</span></span>
- <span data-ttu-id="b5b5f-110">Planera</span><span class="sxs-lookup"><span data-stu-id="b5b5f-110">Plan</span></span>
- <span data-ttu-id="b5b5f-111">Leverera</span><span class="sxs-lookup"><span data-stu-id="b5b5f-111">Deliver</span></span>
- <span data-ttu-id="b5b5f-112">Slutför</span><span class="sxs-lookup"><span data-stu-id="b5b5f-112">Complete</span></span>
- <span data-ttu-id="b5b5f-113">Stängning</span><span class="sxs-lookup"><span data-stu-id="b5b5f-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b5b5f-114">Skapa</span><span class="sxs-lookup"><span data-stu-id="b5b5f-114">New</span></span>

<span data-ttu-id="b5b5f-115">När du skapar ett projekt anges projektstadiet till **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b5b5f-116">Om projektet skapades från en mall kan det finnas schema-, uppskattnings- och teamdata.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b5b5f-117">I annat fall är det en disposition av projektet och resterande komponenter måste anges.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b5b5f-118">Offert</span><span class="sxs-lookup"><span data-stu-id="b5b5f-118">Quote</span></span>

<span data-ttu-id="b5b5f-119">När du associerar ett projekt med en offert eller när du skapar det från ett projekt från offert, anges projektstadiet som **Offert**, och de uppskattade start- och slutdatumen uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b5b5f-120">När projektet är i stadiet **Offert** visas information om offerten på fliken **Försäljning** fliken på sidan **Projektentitet**.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b5b5f-121">Planera</span><span class="sxs-lookup"><span data-stu-id="b5b5f-121">Plan</span></span>

<span data-ttu-id="b5b5f-122">När du vinner en offert som är associerad med ett projekt och projekt flyttas till fasen **Kontrakt** uppdateras projektfasen till **Planera**.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b5b5f-123">När projektet är i stadiet **Planera** visas information om kontraktet på fliken **Projektentitet**.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b5b5f-124">Leverera</span><span class="sxs-lookup"><span data-stu-id="b5b5f-124">Deliver</span></span>

<span data-ttu-id="b5b5f-125">När projektplanen är klar och du är redo att starta projektet ska projektledaren uppdatera projektfasen till **Leverera** för att visar att projektet har påbörjats.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b5b5f-126">Slutför</span><span class="sxs-lookup"><span data-stu-id="b5b5f-126">Complete</span></span> 

<span data-ttu-id="b5b5f-127">När arbetet för projektet har slutförts kan projektledaren uppdatera fasen till att **slutföras**.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b5b5f-128">Om du uppdaterar projektfasen till **Slutföra** anger projektledaren att arbetet är 100 procent klart, men att projektet hålls öppet så att väntande tid- eller utgiftsposter kan registreras.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b5b5f-129">Stäng</span><span class="sxs-lookup"><span data-stu-id="b5b5f-129">Close</span></span>

<span data-ttu-id="b5b5f-130">När alla transaktioner har registreras kan projektledaren uppdatera fasen till att **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b5b5f-131">Vid den tidpunkten kan inga transaktioner registreras och projektet får värdet skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="b5b5f-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]