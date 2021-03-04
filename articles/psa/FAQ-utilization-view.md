---
title: Visa debiterbar användning för resurser
description: I den här ämnet finns information om vyn resursanvändning.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146415"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="00edc-103">Visa debiterbar användning för resurser</span><span class="sxs-lookup"><span data-stu-id="00edc-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="00edc-104">**Vyn för resursutnyttjande** på sidan **resursutnyttjande i Project Service** visar debiterbar användning för varje bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="00edc-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="00edc-105">Eftersom vyn bygger på schemaläggningstavlan och innehåller därför många av de funktioner.</span><span class="sxs-lookup"><span data-stu-id="00edc-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Bild på vyn för resursutnyttjande](media/FAQ-utilization-1.png)
 

<span data-ttu-id="00edc-107">Det debiterbara resursutnyttjandet beräknas så här:</span><span class="sxs-lookup"><span data-stu-id="00edc-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="00edc-108">Debiterbar användning = (debiterbara timmar) / (resurskapacitet för tillgång)</span><span class="sxs-lookup"><span data-stu-id="00edc-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="00edc-109">Cellerna representerar det beräknade debiterbara resursutnyttjandet under den tidsperiod (dagar, veckor eller månader).</span><span class="sxs-lookup"><span data-stu-id="00edc-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="00edc-110">Färgerna i respektive cell visar debiterbart resursutnyttjande för en resurs jämfört med sina respektive debiterbara resursutnyttjandemål.</span><span class="sxs-lookup"><span data-stu-id="00edc-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="00edc-111">Målet för resursutnyttjandet kan anges på antingen resursens standardroll eller på den enskilda resursen.</span><span class="sxs-lookup"><span data-stu-id="00edc-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="00edc-112">Beräkningen undersöker den enskilda resursen för målet först, därefter resursens standardroll.</span><span class="sxs-lookup"><span data-stu-id="00edc-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="00edc-113">Ange mål för en resurs</span><span class="sxs-lookup"><span data-stu-id="00edc-113">Set target on a resource</span></span>

1. <span data-ttu-id="00edc-114">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="00edc-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="00edc-115">Markera en resurs för att öppna posten.</span><span class="sxs-lookup"><span data-stu-id="00edc-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="00edc-116">På fliken **Project Service** kan du ange hur målanvändningen av resursen ska vara.</span><span class="sxs-lookup"><span data-stu-id="00edc-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Bild på användning av fliken Project Service för att ange mål för resursutnyttjande](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="00edc-118">Ange målutnyttjande för en roll</span><span class="sxs-lookup"><span data-stu-id="00edc-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="00edc-119">Gå till **Resurser** \> **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="00edc-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="00edc-120">Markera en roll och öppna posten.</span><span class="sxs-lookup"><span data-stu-id="00edc-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="00edc-121">Ange målutnyttjandet för rollen.</span><span class="sxs-lookup"><span data-stu-id="00edc-121">Set the target utilization for the role.</span></span>

> ![Bild på användning av resursroller för att ange målutnyttjande](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="00edc-123">Beräkna debiterbar användning för en resurs</span><span class="sxs-lookup"><span data-stu-id="00edc-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="00edc-124">Om du vill beräkna debiterbart utnyttjande för en resurs måste du slutföra några förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="00edc-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="00edc-125">Ange standardroll för enskild resurs</span><span class="sxs-lookup"><span data-stu-id="00edc-125">Set default role for individual resource</span></span>

<span data-ttu-id="00edc-126">Utnyttjandemålet måste först anges för antingen den enskilda resursen eller för resursroller.</span><span class="sxs-lookup"><span data-stu-id="00edc-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="00edc-127">Om du använder resursroller för mål måste respektive enskilda resurs ha en standardroll.</span><span class="sxs-lookup"><span data-stu-id="00edc-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="00edc-128">För att ange denna går du till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="00edc-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="00edc-129">Välj en resurs, öppna posten och välj sedan fliken **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="00edc-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="00edc-130">I rutnätet **Resursroll** finns en roll för resursen i resursens rutnät **Är standard** anges till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="00edc-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="00edc-131">Ändra faktureringstyp för resursrollen.</span><span class="sxs-lookup"><span data-stu-id="00edc-131">Change billing type for resource role</span></span>

<span data-ttu-id="00edc-132">Rollerna för resursen måste ha en faktureringsadress vars värde är av typen **debiterbar**.</span><span class="sxs-lookup"><span data-stu-id="00edc-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="00edc-133">Gå till **Resurser** \> **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="00edc-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="00edc-134">Öppna den post du vill uppdatera och ange sedan standarden för faktureringstyp som **Debiterbar**.</span><span class="sxs-lookup"><span data-stu-id="00edc-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="00edc-135">Ange arbetstider för resursroll</span><span class="sxs-lookup"><span data-stu-id="00edc-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="00edc-136">Resursen måste ha arbetstimmar för kapacitetsberäkningen.</span><span class="sxs-lookup"><span data-stu-id="00edc-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="00edc-137">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="00edc-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="00edc-138">Klicka på en resurs för att öppna posten och klicka sedan på **Visa arbetstimmar**.</span><span class="sxs-lookup"><span data-stu-id="00edc-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="00edc-139">Du kan bulkuppdatera resurslistan genom att använda en **mall för arbetstimmar** från vyn **Resurslista**.</span><span class="sxs-lookup"><span data-stu-id="00edc-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="00edc-140">Felsökning av debiterbara faktiska timmar</span><span class="sxs-lookup"><span data-stu-id="00edc-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="00edc-141">De debiterbara tillgångstimmarna hämtas från den entiteten **Faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="00edc-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="00edc-142">Faktiska värden med faktureringstypen **debiterbar** inkluderas i beräkningen, och därför måste du ha projekt där tillgångarna är debiterbara.</span><span class="sxs-lookup"><span data-stu-id="00edc-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="00edc-143">Här följer några saker du kan kontrollera om du inte ser något debiterbart resursutnyttjande:</span><span class="sxs-lookup"><span data-stu-id="00edc-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="00edc-144">Resursen har arbetstimmar definierade för kapacitet.</span><span class="sxs-lookup"><span data-stu-id="00edc-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="00edc-145">Resursen har antingen ett enskilt definierat resursutnyttjandemål eller har tilldelas en standardroll.</span><span class="sxs-lookup"><span data-stu-id="00edc-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="00edc-146">Rollen har ett definierat resursutnyttjandemål.</span><span class="sxs-lookup"><span data-stu-id="00edc-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="00edc-147">Faktiska värden har faktureringstypen **debiterbar** för den tidsperiod som du förväntar dig en resursutnyttjandeberäkning för.</span><span class="sxs-lookup"><span data-stu-id="00edc-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="00edc-148">Kontrollera följande om du ser faktiska värden med faktureringstyper andra än "debiterbar":</span><span class="sxs-lookup"><span data-stu-id="00edc-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="00edc-149">Den roll som används för tillgången har en standardfaktureringstyp annan än "debiterbar".</span><span class="sxs-lookup"><span data-stu-id="00edc-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="00edc-150">Rollen på projektkontraktraden bakom projektet har angetts som "icke-debiterbar".</span><span class="sxs-lookup"><span data-stu-id="00edc-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="00edc-151">Projektet har ingen associerad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="00edc-151">The project does not have an associated contract line.</span></span>

