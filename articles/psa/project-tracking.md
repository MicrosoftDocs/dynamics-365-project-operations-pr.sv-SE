---
title: Projektstatus och kostnadsförbrukning
description: I det här ämnet finns information om hur du spårar projektstatus och kostnadsförbrukning.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283660"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="3720f-103">Projektstatus och kostnadsförbrukning</span><span class="sxs-lookup"><span data-stu-id="3720f-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3720f-104">Behovet av att följa upp statusen för ett schema varierar efter bransch.</span><span class="sxs-lookup"><span data-stu-id="3720f-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="3720f-105">Vissa branscher spårar på en detaljerad nivå, medan andra branscher spårar på en högre nivå.</span><span class="sxs-lookup"><span data-stu-id="3720f-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="3720f-106">I det här ämnet illustreras hur du schemalägger för att uppfylla organisationens krav.</span><span class="sxs-lookup"><span data-stu-id="3720f-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="3720f-107">Insatsspårningsvy</span><span class="sxs-lookup"><span data-stu-id="3720f-107">Effort tracking view</span></span>

<span data-ttu-id="3720f-108">Vyn **Insatsspårning** spårar förloppet för aktiviteterna i schemat.</span><span class="sxs-lookup"><span data-stu-id="3720f-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="3720f-109">Denna jämför de faktiska insatstimmarna som lagts på en uppgift med en uppgifts planerade insatstimmar.</span><span class="sxs-lookup"><span data-stu-id="3720f-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="3720f-110">I Project Service Automation används följande formler för att beräkna spårningsmått:</span><span class="sxs-lookup"><span data-stu-id="3720f-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="3720f-111">Från början när aktiviteten skapas: Den planerade kostnaden kommer att ställas in till den beräknade kostnaden när den är slutförd.</span><span class="sxs-lookup"><span data-stu-id="3720f-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="3720f-112">När verkliga värden har registrerats för uppgiften beräknas följande i vyn uppföljning för insats</span><span class="sxs-lookup"><span data-stu-id="3720f-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="3720f-113">Förloppsprocent = Den faktiska insatsen hittills ÷ Uppskattning vid slutföra (EAC)</span><span class="sxs-lookup"><span data-stu-id="3720f-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="3720f-114">Uppskattning vid slutföra (ETC) = Uppskattning vid slutföra (EAC) – Den faktiska insatsen hittills</span><span class="sxs-lookup"><span data-stu-id="3720f-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="3720f-115">EAC = resterande insats + den faktiska insatsen hittills</span><span class="sxs-lookup"><span data-stu-id="3720f-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="3720f-116">Planerad insatsavvikelse = planerat arbete – EAC</span><span class="sxs-lookup"><span data-stu-id="3720f-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="3720f-117">Project Service Automation visar en projektion av insatsavvikelsen för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="3720f-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="3720f-118">Om EAC är större än den planerade ansträngningen projiceras aktiviteten för att ta längre tid än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="3720f-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="3720f-119">Det ligger därför bakom schemat.</span><span class="sxs-lookup"><span data-stu-id="3720f-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="3720f-120">Om EAC är mindre än den planerade ansträngningen projiceras aktiviteten för att ta kortare tid än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="3720f-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="3720f-121">Det ligger därför framför schemat.</span><span class="sxs-lookup"><span data-stu-id="3720f-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="3720f-122">Omprojektion av arbete</span><span class="sxs-lookup"><span data-stu-id="3720f-122">Reprojecting effort</span></span>

<span data-ttu-id="3720f-123">Det är vanligt att projektledaren ändrar de ursprungliga uppskattningarna för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="3720f-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="3720f-124">Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status.</span><span class="sxs-lookup"><span data-stu-id="3720f-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="3720f-125">Vi rekommenderar dock inte att projektledare ändrar baslinjenumren, eftersom projektbaslinjen representerar den etablerade sanningen för projektets schema och kostnadsberäkning, och alla projektintressenter har gått med på det.</span><span class="sxs-lookup"><span data-stu-id="3720f-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="3720f-126">Det finns två sätt som en projektledare kan använda för att förnya arbetet för uppgifter:</span><span class="sxs-lookup"><span data-stu-id="3720f-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="3720f-127">Åsidosätt standard ETC med en ny uppskattning av den faktiska resterande insatsen för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3720f-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="3720f-128">Åsidosätt standardförlopp i procent med en ny uppskattning av det faktiska förloppen för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3720f-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="3720f-129">Var och en av dessa är en omberäkning av aktivitetens ETC, EAc och förloppsprocent och den planerade insatsavvikelsen för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="3720f-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="3720f-130">Procenten för EAC, ETC och förloppsprocent för sammanfattningsaktiviteterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.</span><span class="sxs-lookup"><span data-stu-id="3720f-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="3720f-131">Omprojektering av ansträngning för sammanfattningsuppgifter</span><span class="sxs-lookup"><span data-stu-id="3720f-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="3720f-132">Arbete för sammanfattningsuppgifter eller behållaruppgifter kan projiceras om.</span><span class="sxs-lookup"><span data-stu-id="3720f-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="3720f-133">Oavsett om användaren återskapar projekt med hjälp av den återstående insatsen eller förloppet i procent av sammanfattningsaktiviteterna börjar följande beräkningar:</span><span class="sxs-lookup"><span data-stu-id="3720f-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="3720f-134">Procentförloppet för EAC, ETC och aktiviteten beräknas.</span><span class="sxs-lookup"><span data-stu-id="3720f-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="3720f-135">Nya EAC fördelas nedåt till de underordnade uppgifterna i samma proportion som original EAC var på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3720f-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="3720f-136">De nya EAC för var och en av de enskilda aktiviteterna till noderna för lövnoder beräknas.</span><span class="sxs-lookup"><span data-stu-id="3720f-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="3720f-137">De underordnade aktiviteterna som påverkas ned till lövnoder har deras ETC och förloppet omberäknas efter EAC-värdet.</span><span class="sxs-lookup"><span data-stu-id="3720f-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="3720f-138">Detta resulterar i en ny projektion för uppgiftens insatsavvikelse.</span><span class="sxs-lookup"><span data-stu-id="3720f-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="3720f-139">EAC för de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.</span><span class="sxs-lookup"><span data-stu-id="3720f-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="3720f-140">Vyn Kostnadsspårning</span><span class="sxs-lookup"><span data-stu-id="3720f-140">Cost tracking view</span></span> 

<span data-ttu-id="3720f-141">I vyn **kostnadsspårning** jämförs den faktiska kostnaden som spenderades för en aktivitet med den planerade kostnaden.</span><span class="sxs-lookup"><span data-stu-id="3720f-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="3720f-142">Vyn visar endast arbetskostnader och inkluderar inga kostnader från utgiftsuppskattningarna.</span><span class="sxs-lookup"><span data-stu-id="3720f-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="3720f-143">I Project Service Automation används följande formler för att beräkna spårningsmått:</span><span class="sxs-lookup"><span data-stu-id="3720f-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="3720f-144">När en uppgift skapas är den planerade kostnaden lika med den beräknade kostnaden när den är slutförd.</span><span class="sxs-lookup"><span data-stu-id="3720f-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="3720f-145">När verkliga värden har registrerats för uppgiften beräknas följande i vyn **uppföljning** för kostnad.</span><span class="sxs-lookup"><span data-stu-id="3720f-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="3720f-146">Procent av förbrukad kostnad = faktisk kostnad spenderad hittills ÷ uppskattad kostnad vid slutföra uppgiften</span><span class="sxs-lookup"><span data-stu-id="3720f-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="3720f-147">Kostnad vid slutföra (CTC) = uppskattad kostnad vid slutföra – den faktiska kostnaden hittills</span><span class="sxs-lookup"><span data-stu-id="3720f-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="3720f-148">Kostnad vid slutföra = CTC + faktiska kostnaden hittills</span><span class="sxs-lookup"><span data-stu-id="3720f-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="3720f-149">Beräknad kostnadsavvikelse = planerad kostnad – uppskattad kostnad vid slutföra</span><span class="sxs-lookup"><span data-stu-id="3720f-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="3720f-150">En projektion av kostnadsavvikelsen visas på uppgiften.</span><span class="sxs-lookup"><span data-stu-id="3720f-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="3720f-151">Om uppskattad kostnad vid slutföra är större än den planerade kostnaden projiceras aktiviteten för att kosta mer än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="3720f-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="3720f-152">Därför prognostiseras den över budget.</span><span class="sxs-lookup"><span data-stu-id="3720f-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="3720f-153">Om uppskattad kostnad för att slutföra är mindre än den planerade kostnaden projiceras aktiviteten för att kosta mindre än vad som ursprungligen planerades och rör sig under budget.</span><span class="sxs-lookup"><span data-stu-id="3720f-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="3720f-154">Projektledarens återprojektering av kostnaderna</span><span class="sxs-lookup"><span data-stu-id="3720f-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="3720f-155">När arbetsinsatsen återprojiceras räknas CTC, uppskattad kostnad för att slutföra, procent av förbrukad kostnad och planerad kostnadsavvikelse i vyn **kostnadsspårning**.</span><span class="sxs-lookup"><span data-stu-id="3720f-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="3720f-156">Sammanfattning av projektstatus</span><span class="sxs-lookup"><span data-stu-id="3720f-156">Project status summary</span></span>

<span data-ttu-id="3720f-157">Spåra data i **Insatsspårning** och **Kostnadsspårning** visas förloppet och kostnadsförbrukning på projektets rotnod, sammanfattningsaktiviteter och aktivitetsnivåerna på lövnodnivå.</span><span class="sxs-lookup"><span data-stu-id="3720f-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="3720f-158">I avsnittet **status** på sidan **projektentitet** visas en översikt över status på projektnivå.</span><span class="sxs-lookup"><span data-stu-id="3720f-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="3720f-159">Fält för statussammanfattning</span><span class="sxs-lookup"><span data-stu-id="3720f-159">Status summary fields</span></span>

<span data-ttu-id="3720f-160">Fältet **övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status.</span><span class="sxs-lookup"><span data-stu-id="3720f-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="3720f-161">Det använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker.</span><span class="sxs-lookup"><span data-stu-id="3720f-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="3720f-162">I fältet **kommentarer** kan projektledaren ange kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="3720f-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="3720f-163">Fältet **status uppdaterad för** är inte redigerbart och värdet är en tidstämpel som anger när status senast uppdaterades.</span><span class="sxs-lookup"><span data-stu-id="3720f-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="3720f-164">Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsdatumet.</span><span class="sxs-lookup"><span data-stu-id="3720f-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="3720f-165">När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva kan du ange att dessa fält till **Före**.</span><span class="sxs-lookup"><span data-stu-id="3720f-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="3720f-166">När schema och kostnadsavvikelse för rotnoden är negativa kan du ange dem till **Efter**.</span><span class="sxs-lookup"><span data-stu-id="3720f-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]