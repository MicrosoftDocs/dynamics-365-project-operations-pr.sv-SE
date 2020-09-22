---
title: Skapa anpassade fält och entiteter
description: I det här ämnet beskrivs hur du skapar alternativuppsättningar och entiteter i din egen lösning i Power Apps-plattformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756281"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="b3d39-103">Skapa anpassade fält och entiteter</span><span class="sxs-lookup"><span data-stu-id="b3d39-103">Create custom fields and entities</span></span> 

<span data-ttu-id="b3d39-104">Slutför följande steg varje gång du vill skapa en anpassad alternativuppsättning eller entitet på Power Apps-plattformen.</span><span class="sxs-lookup"><span data-stu-id="b3d39-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="b3d39-105">Procedurerna i det här ämnet ska slutföras med webbgränssnittet för PSA (Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="b3d39-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3d39-106">Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning.</span><span class="sxs-lookup"><span data-stu-id="b3d39-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b3d39-107">Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans.</span><span class="sxs-lookup"><span data-stu-id="b3d39-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b3d39-108">När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="b3d39-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="b3d39-109">Skapa en anpassad lösning för prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="b3d39-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="b3d39-110">Klicka på **inställningar** > **lösningar** i PSA och klicka sedan på **Ny** för att skapa en ny lösning.</span><span class="sxs-lookup"><span data-stu-id="b3d39-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="b3d39-111">Ge lösningen ett namn, **\<din organisations namn > prissättningsdimensioner**, ange den information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Skapa en anpassad lösning för prissättningsdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b3d39-113">Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning</span><span class="sxs-lookup"><span data-stu-id="b3d39-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b3d39-114">En prissättningsdimension kan vara en alternativuppsättning eller en entitet.</span><span class="sxs-lookup"><span data-stu-id="b3d39-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b3d39-115">Båda måste skapas i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="b3d39-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b3d39-116">Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="b3d39-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b3d39-117">Entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="b3d39-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="b3d39-118">I PSA, klicka på **Inställningar** > **Lösningar** och dubbelklicka sedan på  **\<organisationens namn > prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b3d39-119">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b3d39-120">Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="b3d39-121">Ange återstående information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Entiteten standardrubrik](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b3d39-123">Alternativuppsättningsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="b3d39-123">Option set-based dimensions</span></span> 
<span data-ttu-id="b3d39-124">Du kan skapa två alternativbaserade dimensioner.</span><span class="sxs-lookup"><span data-stu-id="b3d39-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b3d39-125">Använd **Resursens arbetsplats** för att spåra priset för platsarbetet **Start** och arbete **på plats** och använda **resursens arbetstider** med värdena **Reguljär** och **Övertid** för att tillämpa en markering när arbetet har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b3d39-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b3d39-126">I PSA, klicka på **Inställningar** > **Lösningar** och dubbelklicka sedan på  **\<organisationens namn > prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b3d39-127">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **alternativuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b3d39-128">Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="b3d39-129">Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetsplats</span><span class="sxs-lookup"><span data-stu-id="b3d39-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="b3d39-130">Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetstimmar</span><span class="sxs-lookup"><span data-stu-id="b3d39-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b3d39-131">Skapa data för entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="b3d39-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b3d39-132">Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal.</span><span class="sxs-lookup"><span data-stu-id="b3d39-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b3d39-133">Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b3d39-134">Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.</span><span class="sxs-lookup"><span data-stu-id="b3d39-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b3d39-135">I PSA, klicka på **Avancerad sökning**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="b3d39-136">Markera entiteten **Standardrubrik** och klicka sedan på **Resultat**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="b3d39-137">Alla rader i entiteten **standardrubrik** visas.</span><span class="sxs-lookup"><span data-stu-id="b3d39-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b3d39-138">Klicka på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-138">Click **New**.</span></span> <span data-ttu-id="b3d39-139">I fältet **Namn** anger du på "Systemtekniker" och klicka på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="b3d39-140">Stäng formuläret.</span><span class="sxs-lookup"><span data-stu-id="b3d39-140">Close the form.</span></span> 
4. <span data-ttu-id="b3d39-141">Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.</span><span class="sxs-lookup"><span data-stu-id="b3d39-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="b3d39-142">Exempeldata för entiteten för standardrubrik</span><span class="sxs-lookup"><span data-stu-id="b3d39-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="b3d39-143">Lägg till alla obligatoriska PSA-entiteter och relaterade komponenter i prisdimensionslösningen</span><span class="sxs-lookup"><span data-stu-id="b3d39-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="b3d39-144">Du måste lägga till följande Project Service-entiteter i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="b3d39-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="b3d39-145">Följ stegen i den här proceduren för att göra vissa viktiga schemaändringar i prissättningslösningen så att enheterna blir medvetna om de nya prissättningsdimensionerna.</span><span class="sxs-lookup"><span data-stu-id="b3d39-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="b3d39-146">I PSA, klicka på **Inställningar** > **Lösningar** och dubbelklicka sedan på  **\<organisationens namn > prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b3d39-147">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="b3d39-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="b3d39-148">I dialogrutan **lösningskomponenter** markerar du följande entiteter:</span><span class="sxs-lookup"><span data-stu-id="b3d39-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="b3d39-149">Faktiskt</span><span class="sxs-lookup"><span data-stu-id="b3d39-149">Actual</span></span>
- <span data-ttu-id="b3d39-150">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="b3d39-150">Bookable Resource</span></span>
- <span data-ttu-id="b3d39-151">Beräkningsrad</span><span class="sxs-lookup"><span data-stu-id="b3d39-151">Estimate Line</span></span>
- <span data-ttu-id="b3d39-152">Information om fakturarad</span><span class="sxs-lookup"><span data-stu-id="b3d39-152">Invoice Line Detail</span></span>
- <span data-ttu-id="b3d39-153">Journalrad</span><span class="sxs-lookup"><span data-stu-id="b3d39-153">Journal Line</span></span>
- <span data-ttu-id="b3d39-154">Information om projektkontraktrad</span><span class="sxs-lookup"><span data-stu-id="b3d39-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="b3d39-155">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="b3d39-155">Project Team Member</span></span>
- <span data-ttu-id="b3d39-156">Information om offertrad</span><span class="sxs-lookup"><span data-stu-id="b3d39-156">Quote Line Detail</span></span>
- <span data-ttu-id="b3d39-157">Pålägg för rollpris</span><span class="sxs-lookup"><span data-stu-id="b3d39-157">Role Price Markup</span></span>
- <span data-ttu-id="b3d39-158">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="b3d39-158">Role Price</span></span> 
- <span data-ttu-id="b3d39-159">Tidspost</span><span class="sxs-lookup"><span data-stu-id="b3d39-159">Time Entry</span></span> 

> ![Lägg till befintliga entiteter i lösningen för prissättningsdimensioner](media/Existing-entities-to-PD-solution.png)

> ![Välj lösningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="b3d39-162">Se till att du tar med alla formulär och vyer för varje vald entitet.</span><span class="sxs-lookup"><span data-stu-id="b3d39-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="b3d39-163">Klicka på **Nej**om du uppmanas att ta med alla beroende entiteter för de valda entiteterna ovan.</span><span class="sxs-lookup"><span data-stu-id="b3d39-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Inkludera inte alla relaterade komponenter](media/Do-not-include-required.png)


