---
title: Skapa anpassade fält och entiteter som prissättningsdimensioner
description: I det här ämnet finns information om hur du skapar anpassade alternativuppsättningar eller entiteter.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275650"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="3a870-103">Skapa anpassade fält och entiteter som prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="3a870-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="3a870-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="3a870-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3a870-105">Slutför följande steg när du vill skapa en anpassad alternativuppsättning eller -entitet för att använda denna som en prissättningsdimension.</span><span class="sxs-lookup"><span data-stu-id="3a870-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="3a870-106">Mer information finns i [Översikt över prissättningsdimensioner](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3a870-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3a870-107">Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning.</span><span class="sxs-lookup"><span data-stu-id="3a870-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="3a870-108">Denna viktiga bästa praxis ger flexibilitet i framtiden att uppdatera eller ta bort ändringar efter behov.</span><span class="sxs-lookup"><span data-stu-id="3a870-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="3a870-109">Detta kommer också att bidra till återanvändningen av ditt arbete och göra det enklare att överföra dessa ändringar till en annan instans När du har gjort alla nödvändiga ändringar, exportera då denna lösning som en **hanterad lösning** och importera den till andra instanser för att återanvända din prissättningskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a870-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="3a870-110">Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning</span><span class="sxs-lookup"><span data-stu-id="3a870-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="3a870-111">En prissättningsdimension kan vara en alternativuppsättning eller en entitet.</span><span class="sxs-lookup"><span data-stu-id="3a870-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="3a870-112">Båda måste skapas i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="3a870-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="3a870-113">Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="3a870-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="3a870-114">Entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="3a870-114">Entity-based dimensions</span></span>
<span data-ttu-id="3a870-115">Skapa entitetsbaserade dimensioner genom att följa dessa steg:</span><span class="sxs-lookup"><span data-stu-id="3a870-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="3a870-116">Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="3a870-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="3a870-117">I det vänstra navigeringsfönstret i lösningsutforskaren väljer du **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="3a870-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="3a870-118">Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="3a870-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="3a870-119">Ange återstående information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="3a870-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Entiteten standardrubrik](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="3a870-121">Alternativuppsättningsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="3a870-121">Option set-based dimensions</span></span> 
<span data-ttu-id="3a870-122">Du kan skapa två alternativbaserade dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3a870-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="3a870-123">Använd **Arbetsplats för resurs** för att spåra priset för arbete på platsen **Start** och platsen **På plats**.</span><span class="sxs-lookup"><span data-stu-id="3a870-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="3a870-124">Använd **Arbetstider för resurs** med värdena **Vanlig** och **Övertid** för att tillämpa ett pålägg när arbetet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="3a870-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="3a870-125">Följande grafik ger en vy över dimensionen **Arbetsplats för resurs**.</span><span class="sxs-lookup"><span data-stu-id="3a870-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetsplats](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="3a870-127">Följande grafik ger en vy över dimensionen **Arbetstider för resurs**.</span><span class="sxs-lookup"><span data-stu-id="3a870-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetstimmar](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="3a870-129">Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="3a870-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3a870-130">I det vänstra navigeringsfönstret i lösningsutforskaren väljer du **Alternativuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="3a870-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="3a870-131">Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.</span><span class="sxs-lookup"><span data-stu-id="3a870-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="3a870-132">Skapa data för entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="3a870-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="3a870-133">Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal.</span><span class="sxs-lookup"><span data-stu-id="3a870-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="3a870-134">Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="3a870-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="3a870-135">Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.</span><span class="sxs-lookup"><span data-stu-id="3a870-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="3a870-136">Välj **Avancerad sökning**.</span><span class="sxs-lookup"><span data-stu-id="3a870-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="3a870-137">Markera entiteten **Standardrubrik** och välj sedan **Resultat**.</span><span class="sxs-lookup"><span data-stu-id="3a870-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="3a870-138">Alla rader i entiteten **standardrubrik** visas.</span><span class="sxs-lookup"><span data-stu-id="3a870-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="3a870-139">Välj **Ny** och i fältet **Namn** ange "Systemtekniker" och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="3a870-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="3a870-140">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="3a870-140">Close the page.</span></span> 
5. <span data-ttu-id="3a870-141">Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.</span><span class="sxs-lookup"><span data-stu-id="3a870-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Exempeldata för entiteten Standardrubrik](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]