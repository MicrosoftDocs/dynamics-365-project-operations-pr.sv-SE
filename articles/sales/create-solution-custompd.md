---
title: Skapa en lösning för anpassade prissättningsdimensioner
description: I det här ämnet finns information om hur du skapar lösningar för anpassade prissättningsdimensioner.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514029"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="90f5e-103">Skapa en lösning för anpassade prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="90f5e-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="90f5e-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="90f5e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="90f5e-105">Alla anpassningar av ändringar i prisdimension ska vara i en separat lösning.</span><span class="sxs-lookup"><span data-stu-id="90f5e-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="90f5e-106">Denna viktiga rekommenderade metod ger flexibilitet att uppdatera eller ta bort ändringar efter behov, den bidrar till att underlätta återanvändning av ditt arbete samt gör det lättare att överföra ändringar till andra instanser.</span><span class="sxs-lookup"><span data-stu-id="90f5e-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="90f5e-107">När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad** lösning och importerar den sedan till andra instanser för återanvändning.</span><span class="sxs-lookup"><span data-stu-id="90f5e-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="90f5e-108">Skapa en lösning för anpassade prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="90f5e-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="90f5e-109">Välj **Inställningar** > **Lösningar** och välj sedan **Ny**.</span><span class="sxs-lookup"><span data-stu-id="90f5e-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="90f5e-110">Namnge lösningen *<your organization name>-prissättningsdimensioner*.</span><span class="sxs-lookup"><span data-stu-id="90f5e-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="90f5e-111">Ange återstående information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="90f5e-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Skapa en anpassad lösning för prissättningsdimension](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="90f5e-113">Lägg till alla obligatoriska entiteter och relaterade komponenter i prisdimensionslösningen</span><span class="sxs-lookup"><span data-stu-id="90f5e-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="90f5e-114">Lägg till följande Project Service-entiteter i din prissättningslösning för att göra viktiga schemaändringar i prissättningslösningen.</span><span class="sxs-lookup"><span data-stu-id="90f5e-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="90f5e-115">När du har slutfört den här proceduren kommer entiteterna att känna igen de nya prissättningsdimensionerna.</span><span class="sxs-lookup"><span data-stu-id="90f5e-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="90f5e-116">Välj **Inställningar** > **Lösningar** och dubbelklicka sedan på **<*ditt organisationsmamn*> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="90f5e-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="90f5e-117">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="90f5e-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="90f5e-118">I dialogrutan **lösningskomponenter** markerar du följande entiteter:</span><span class="sxs-lookup"><span data-stu-id="90f5e-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="90f5e-119">**Faktisk**</span><span class="sxs-lookup"><span data-stu-id="90f5e-119">**Actual**</span></span>
   - <span data-ttu-id="90f5e-120">**Bokningsbar resurs**</span><span class="sxs-lookup"><span data-stu-id="90f5e-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="90f5e-121">**Beräkningsrad**</span><span class="sxs-lookup"><span data-stu-id="90f5e-121">**Estimate Line**</span></span>
   - <span data-ttu-id="90f5e-122">**Projektuppgift**</span><span class="sxs-lookup"><span data-stu-id="90f5e-122">**Project Task**</span></span>
   - <span data-ttu-id="90f5e-123">**Information om fakturarad**</span><span class="sxs-lookup"><span data-stu-id="90f5e-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="90f5e-124">**Journalrad**</span><span class="sxs-lookup"><span data-stu-id="90f5e-124">**Journal Line**</span></span>
   - <span data-ttu-id="90f5e-125">**Information om projektkontraktrad**</span><span class="sxs-lookup"><span data-stu-id="90f5e-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="90f5e-126">**Projektgruppmedlem**</span><span class="sxs-lookup"><span data-stu-id="90f5e-126">**Project Team Member**</span></span>
   - <span data-ttu-id="90f5e-127">**Information om offertrad**</span><span class="sxs-lookup"><span data-stu-id="90f5e-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="90f5e-128">**Pålägg för rollpris**</span><span class="sxs-lookup"><span data-stu-id="90f5e-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="90f5e-129">**Pris för roll**</span><span class="sxs-lookup"><span data-stu-id="90f5e-129">**Role Price**</span></span>
   - <span data-ttu-id="90f5e-130">**Tidspost**</span><span class="sxs-lookup"><span data-stu-id="90f5e-130">**Time Entry**</span></span>
 
   ![Lägg till lösning för anpassade prissättningsdimensioner](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="90f5e-132">För varje entitet granskar du de komponenter som läggs till och den slutliga listan över entitetstillgångar för respektive entitet.</span><span class="sxs-lookup"><span data-stu-id="90f5e-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="90f5e-133">Inkludera alla formulär och vyer för samtliga valda entiteter.</span><span class="sxs-lookup"><span data-stu-id="90f5e-133">Include all forms and views for each of the selected entities.</span></span>

  ![Tillagda entiteter](./media/solution-component-selection.png)


5.  <span data-ttu-id="90f5e-135">När du uppmanas att inkludera eventuella beroende entiteter för de valda entiteterna väljer du **Nej, inkludera inte nödvändiga komponenter.**</span><span class="sxs-lookup"><span data-stu-id="90f5e-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inkludera beroende enheter](./media/Do-not-include-required.png)
