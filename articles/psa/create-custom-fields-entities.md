---
title: Skapa anpassade fält och entiteter
description: I det här ämnet beskrivs hur du skapar alternativuppsättningar och entiteter i din egen lösning i Power Apps-plattformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144885"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="970bd-103">Skapa anpassade fält och entiteter</span><span class="sxs-lookup"><span data-stu-id="970bd-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="970bd-104">Slutför följande steg varje gång du vill skapa en anpassad alternativuppsättning eller entitet på Power Apps-plattformen.</span><span class="sxs-lookup"><span data-stu-id="970bd-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="970bd-105">Procedurerna i det här ämnet ska slutföras med webbgränssnittet för PSA (Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="970bd-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="970bd-106">Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning.</span><span class="sxs-lookup"><span data-stu-id="970bd-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="970bd-107">Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans.</span><span class="sxs-lookup"><span data-stu-id="970bd-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="970bd-108">När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="970bd-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="970bd-109">Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning</span><span class="sxs-lookup"><span data-stu-id="970bd-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="970bd-110">En prissättningsdimension kan vara en alternativuppsättning eller en entitet.</span><span class="sxs-lookup"><span data-stu-id="970bd-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="970bd-111">Båda måste skapas i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="970bd-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="970bd-112">Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="970bd-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="970bd-113">Entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="970bd-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="970bd-114">I PSA, klicka på **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="970bd-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="970bd-115">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="970bd-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="970bd-116">Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="970bd-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="970bd-117">Ange återstående information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="970bd-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Entiteten standardrubrik](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="970bd-119">Alternativuppsättningsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="970bd-119">Option set-based dimensions</span></span> 
<span data-ttu-id="970bd-120">Du kan skapa två alternativbaserade dimensioner.</span><span class="sxs-lookup"><span data-stu-id="970bd-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="970bd-121">Använd **Resursens arbetsplats** för att spåra priset för platsarbetet **Start** och arbete **på plats** och använda **resursens arbetstider** med värdena **Reguljär** och **Övertid** för att tillämpa en markering när arbetet har slutförts.</span><span class="sxs-lookup"><span data-stu-id="970bd-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="970bd-122">I PSA, klicka på **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="970bd-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="970bd-123">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **alternativuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="970bd-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="970bd-124">Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.</span><span class="sxs-lookup"><span data-stu-id="970bd-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="970bd-125">Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetsplats</span><span class="sxs-lookup"><span data-stu-id="970bd-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="970bd-126">Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetstimmar</span><span class="sxs-lookup"><span data-stu-id="970bd-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="970bd-127">Skapa data för entitetsbaserade dimensioner</span><span class="sxs-lookup"><span data-stu-id="970bd-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="970bd-128">Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal.</span><span class="sxs-lookup"><span data-stu-id="970bd-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="970bd-129">Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**.</span><span class="sxs-lookup"><span data-stu-id="970bd-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="970bd-130">Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.</span><span class="sxs-lookup"><span data-stu-id="970bd-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="970bd-131">I PSA, klicka på **Avancerad sökning**.</span><span class="sxs-lookup"><span data-stu-id="970bd-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="970bd-132">Markera entiteten **Standardrubrik** och klicka sedan på **Resultat**.</span><span class="sxs-lookup"><span data-stu-id="970bd-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="970bd-133">Alla rader i entiteten **standardrubrik** visas.</span><span class="sxs-lookup"><span data-stu-id="970bd-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="970bd-134">Klicka på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="970bd-134">Click **New**.</span></span> <span data-ttu-id="970bd-135">I fältet **Namn** anger du på "Systemtekniker" och klicka på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="970bd-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="970bd-136">Stäng formuläret.</span><span class="sxs-lookup"><span data-stu-id="970bd-136">Close the form.</span></span> 
4. <span data-ttu-id="970bd-137">Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.</span><span class="sxs-lookup"><span data-stu-id="970bd-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="970bd-138">Exempeldata för entiteten för standardrubrik</span><span class="sxs-lookup"><span data-stu-id="970bd-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


