---
title: Skapa anpassade fält och entiteter som prissättningsdimensioner
description: I det här ämnet finns information om hur du skapar anpassade alternativuppsättningar eller entiteter.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130915"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="b557c-103">Skapa anpassade fält och entiteter som prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="b557c-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="b557c-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b557c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b557c-105">Slutför följande steg varje gång du vill skapa en anpassad alternativuppsättning eller entitet på.</span><span class="sxs-lookup"><span data-stu-id="b557c-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b557c-106">Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning.</span><span class="sxs-lookup"><span data-stu-id="b557c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b557c-107">Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans.</span><span class="sxs-lookup"><span data-stu-id="b557c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b557c-108">När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="b557c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="b557c-109">Skapa en anpassad lösning för prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="b557c-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="b557c-110">Klicka på **inställningar** > **lösningar** och klicka sedan på **Ny** för att skapa en ny lösning.</span><span class="sxs-lookup"><span data-stu-id="b557c-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="b557c-111">Ge lösningen ett namn, **\<your organization name> prissättningsdimensioner**, ange den information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b557c-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b557c-112">Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning</span><span class="sxs-lookup"><span data-stu-id="b557c-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b557c-113">En prissättningsdimension kan vara en alternativuppsättning eller en entitet.</span><span class="sxs-lookup"><span data-stu-id="b557c-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b557c-114">Båda måste skapas i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="b557c-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b557c-115">Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="b557c-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b557c-116">Entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="b557c-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="b557c-117">Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b557c-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b557c-118">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="b557c-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b557c-119">Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="b557c-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="b557c-120">Ange återstående information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b557c-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b557c-121">Alternativuppsättningsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="b557c-121">Option set-based dimensions</span></span> 
<span data-ttu-id="b557c-122">Du kan skapa två alternativbaserade dimensioner.</span><span class="sxs-lookup"><span data-stu-id="b557c-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b557c-123">Använd **Resursens arbetsplats** för att spåra priset för platsarbetet **Start** och arbete **på plats** och använda **resursens arbetstider** med värdena **Reguljär** och **Övertid** för att tillämpa en markering när arbetet har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b557c-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b557c-124">Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b557c-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b557c-125">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **alternativuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="b557c-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b557c-126">Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.</span><span class="sxs-lookup"><span data-stu-id="b557c-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b557c-127">Skapa data för entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="b557c-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b557c-128">Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal.</span><span class="sxs-lookup"><span data-stu-id="b557c-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b557c-129">Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="b557c-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b557c-130">Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.</span><span class="sxs-lookup"><span data-stu-id="b557c-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b557c-131">Välj **Avancerad sökning**, markera enhetens **standardrubrik** och välj sedan **resultat**.</span><span class="sxs-lookup"><span data-stu-id="b557c-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="b557c-132">Alla rader i entiteten **standardrubrik** visas.</span><span class="sxs-lookup"><span data-stu-id="b557c-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b557c-133">Välj **Ny** och i fältet **Namn** ange "Systemtekniker" och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b557c-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="b557c-134">Stäng formuläret.</span><span class="sxs-lookup"><span data-stu-id="b557c-134">Close the form.</span></span> 
4. <span data-ttu-id="b557c-135">Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.</span><span class="sxs-lookup"><span data-stu-id="b557c-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="b557c-136">Lägg till alla obligatoriska entiteter och relaterade komponenter i prisdimensionslösningen</span><span class="sxs-lookup"><span data-stu-id="b557c-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="b557c-137">Du måste lägga till följande entiteter i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="b557c-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="b557c-138">Följ stegen i den här proceduren för att göra vissa viktiga schemaändringar i prissättningslösningen så att enheterna blir medvetna om de nya prissättningsdimensionerna.</span><span class="sxs-lookup"><span data-stu-id="b557c-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="b557c-139">Välj **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b557c-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b557c-140">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="b557c-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="b557c-141">I dialogrutan **lösningskomponenter** markerar du följande entiteter:</span><span class="sxs-lookup"><span data-stu-id="b557c-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="b557c-142">Faktiskt</span><span class="sxs-lookup"><span data-stu-id="b557c-142">Actual</span></span>
  - <span data-ttu-id="b557c-143">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="b557c-143">Bookable Resource</span></span>
  - <span data-ttu-id="b557c-144">Beräkningsrad</span><span class="sxs-lookup"><span data-stu-id="b557c-144">Estimate Line</span></span>
  - <span data-ttu-id="b557c-145">Information om fakturarad</span><span class="sxs-lookup"><span data-stu-id="b557c-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="b557c-146">Journalrad</span><span class="sxs-lookup"><span data-stu-id="b557c-146">Journal Line</span></span>
  - <span data-ttu-id="b557c-147">Information om projektkontraktrad</span><span class="sxs-lookup"><span data-stu-id="b557c-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="b557c-148">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="b557c-148">Project Team Member</span></span>
  - <span data-ttu-id="b557c-149">Information om offertrad</span><span class="sxs-lookup"><span data-stu-id="b557c-149">Quote Line Detail</span></span>
  - <span data-ttu-id="b557c-150">Pålägg för rollpris</span><span class="sxs-lookup"><span data-stu-id="b557c-150">Role Price Markup</span></span>
  - <span data-ttu-id="b557c-151">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="b557c-151">Role Price</span></span> 
  - <span data-ttu-id="b557c-152">Tidspost</span><span class="sxs-lookup"><span data-stu-id="b557c-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="b557c-153">Se till att du tar med alla formulär och vyer för varje vald entitet.</span><span class="sxs-lookup"><span data-stu-id="b557c-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="b557c-154">Klicka på **Nej** om du uppmanas att ta med alla beroende entiteter för de valda entiteterna ovan.</span><span class="sxs-lookup"><span data-stu-id="b557c-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

