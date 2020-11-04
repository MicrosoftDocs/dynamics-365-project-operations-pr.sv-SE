---
title: Visa debiterbar användning för resurser
description: I den här ämnet finns information om vyn resursanvändning.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085562"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="da4d9-103">Visa debiterbar användning för resurser</span><span class="sxs-lookup"><span data-stu-id="da4d9-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="da4d9-104">**Vyn för resursutnyttjande** på sidan **resursutnyttjande i Project Service** visar debiterbar användning för varje bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="da4d9-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="da4d9-105">Eftersom vyn bygger på schemaläggningstavlan och innehåller därför många av de funktioner.</span><span class="sxs-lookup"><span data-stu-id="da4d9-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Bild på vyn för resursutnyttjande](media/FAQ-utilization-1.png)
 

<span data-ttu-id="da4d9-107">Det debiterbara resursutnyttjandet beräknas så här:</span><span class="sxs-lookup"><span data-stu-id="da4d9-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="da4d9-108">Debiterbar användning = (debiterbara timmar) / (resurskapacitet för tillgång)</span><span class="sxs-lookup"><span data-stu-id="da4d9-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="da4d9-109">Cellerna representerar det beräknade debiterbara resursutnyttjandet under den tidsperiod (dagar, veckor eller månader).</span><span class="sxs-lookup"><span data-stu-id="da4d9-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="da4d9-110">Färgerna i respektive cell visar debiterbart resursutnyttjande för en resurs jämfört med sina respektive debiterbara resursutnyttjandemål.</span><span class="sxs-lookup"><span data-stu-id="da4d9-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="da4d9-111">Målet för resursutnyttjandet kan anges på antingen resursens standardroll eller på den enskilda resursen.</span><span class="sxs-lookup"><span data-stu-id="da4d9-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="da4d9-112">Beräkningen undersöker den enskilda resursen för målet först, därefter resursens standardroll.</span><span class="sxs-lookup"><span data-stu-id="da4d9-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="da4d9-113">Ange mål för en resurs</span><span class="sxs-lookup"><span data-stu-id="da4d9-113">Set target on a resource</span></span>

1. <span data-ttu-id="da4d9-114">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="da4d9-115">Markera en resurs för att öppna posten.</span><span class="sxs-lookup"><span data-stu-id="da4d9-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="da4d9-116">På fliken **Project Service** kan du ange hur målanvändningen av resursen ska vara.</span><span class="sxs-lookup"><span data-stu-id="da4d9-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Bild på användning av fliken Project Service för att ange mål för resursutnyttjande](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="da4d9-118">Ange målutnyttjande för en roll</span><span class="sxs-lookup"><span data-stu-id="da4d9-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="da4d9-119">Gå till **Resurser** \> **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="da4d9-120">Markera en roll och öppna posten.</span><span class="sxs-lookup"><span data-stu-id="da4d9-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="da4d9-121">Ange målutnyttjandet för rollen.</span><span class="sxs-lookup"><span data-stu-id="da4d9-121">Set the target utilization for the role.</span></span>

> ![Bild på användning av resursroller för att ange målutnyttjande](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="da4d9-123">Beräkna debiterbar användning för en resurs</span><span class="sxs-lookup"><span data-stu-id="da4d9-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="da4d9-124">Om du vill beräkna debiterbart utnyttjande för en resurs måste du slutföra några förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="da4d9-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="da4d9-125">Ange standardroll för enskild resurs</span><span class="sxs-lookup"><span data-stu-id="da4d9-125">Set default role for individual resource</span></span>

<span data-ttu-id="da4d9-126">Utnyttjandemålet måste först anges för antingen den enskilda resursen eller för resursroller.</span><span class="sxs-lookup"><span data-stu-id="da4d9-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="da4d9-127">Om du använder resursroller för mål måste respektive enskilda resurs ha en standardroll.</span><span class="sxs-lookup"><span data-stu-id="da4d9-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="da4d9-128">För att ange denna går du till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="da4d9-129">Välj en resurs, öppna posten och välj sedan fliken **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="da4d9-130">I rutnätet **Resursroll** finns en roll för resursen i resursens rutnät **Är standard** anges till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="da4d9-131">Ändra faktureringstyp för resursrollen.</span><span class="sxs-lookup"><span data-stu-id="da4d9-131">Change billing type for resource role</span></span>

<span data-ttu-id="da4d9-132">Rollerna för resursen måste ha en faktureringsadress vars värde är av typen **debiterbar**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="da4d9-133">Gå till **Resurser** \> **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="da4d9-134">Öppna den post du vill uppdatera och ange sedan standarden för faktureringstyp som **Debiterbar**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="da4d9-135">Ange arbetstider för resursroll</span><span class="sxs-lookup"><span data-stu-id="da4d9-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="da4d9-136">Resursen måste ha arbetstimmar för kapacitetsberäkningen.</span><span class="sxs-lookup"><span data-stu-id="da4d9-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="da4d9-137">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="da4d9-138">Klicka på en resurs för att öppna posten och klicka sedan på **Visa arbetstimmar**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="da4d9-139">Du kan bulkuppdatera resurslistan genom att använda en **mall för arbetstimmar** från vyn **Resurslista**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="da4d9-140">Felsökning av debiterbara faktiska timmar</span><span class="sxs-lookup"><span data-stu-id="da4d9-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="da4d9-141">De debiterbara tillgångstimmarna hämtas från den entiteten **Faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="da4d9-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="da4d9-142">Faktiska värden med faktureringstypen **debiterbar** inkluderas i beräkningen, och därför måste du ha projekt där tillgångarna är debiterbara.</span><span class="sxs-lookup"><span data-stu-id="da4d9-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="da4d9-143">Här följer några saker du kan kontrollera om du inte ser något debiterbart resursutnyttjande:</span><span class="sxs-lookup"><span data-stu-id="da4d9-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="da4d9-144">Resursen har arbetstimmar definierade för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="da4d9-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="da4d9-145">Resursen har antingen ett enskilt definierat resursutnyttjandemål eller har tilldelas en standardroll.</span><span class="sxs-lookup"><span data-stu-id="da4d9-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="da4d9-146">Rollen har ett definierat resursutnyttjandemål.</span><span class="sxs-lookup"><span data-stu-id="da4d9-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="da4d9-147">Faktiska värden har faktureringstypen **debiterbar** för den tidsperiod som du förväntar dig en resursutnyttjandeberäkning för.</span><span class="sxs-lookup"><span data-stu-id="da4d9-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="da4d9-148">Kontrollera följande om du ser faktiska värden med faktureringstyper andra än "debiterbar":</span><span class="sxs-lookup"><span data-stu-id="da4d9-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="da4d9-149">Den roll som används för tillgången har en standardfaktureringstyp annan än "debiterbar".</span><span class="sxs-lookup"><span data-stu-id="da4d9-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="da4d9-150">Rollen på projektkontraktraden bakom projektet har angetts som "icke-debiterbar".</span><span class="sxs-lookup"><span data-stu-id="da4d9-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="da4d9-151">Projektet har ingen associerad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="da4d9-151">The project does not have an associated contract line.</span></span>

