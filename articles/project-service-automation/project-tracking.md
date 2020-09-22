---
title: Projektstatus och kostnadsförbrukning
description: I det här ämnet finns information om hur du spårar projektstatus och kostnadsförbrukning.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756274"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="412d0-103">Projektstatus och kostnadsförbrukning</span><span class="sxs-lookup"><span data-stu-id="412d0-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="412d0-104">Behovet av att följa upp statusen för ett schema varierar efter bransch.</span><span class="sxs-lookup"><span data-stu-id="412d0-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="412d0-105">Vissa branscher spårar på en detaljerad nivå, medan andra branscher spårar på en högre nivå.</span><span class="sxs-lookup"><span data-stu-id="412d0-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="412d0-106">I det här ämnet illustreras hur du schemalägger för att uppfylla organisationens krav.</span><span class="sxs-lookup"><span data-stu-id="412d0-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="412d0-107">Insatsspårningsvy</span><span class="sxs-lookup"><span data-stu-id="412d0-107">Effort tracking view</span></span>

<span data-ttu-id="412d0-108">Vyn **Insatsspårning** spårar förloppet för aktiviteterna i schemat.</span><span class="sxs-lookup"><span data-stu-id="412d0-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="412d0-109">Den jämför de faktiska insatstimmarna som lagts på en uppgift till de planerade insatstimmarna för den uppgiften.</span><span class="sxs-lookup"><span data-stu-id="412d0-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="412d0-110">I PSA används följande formler för att beräkna spårningsmått:</span><span class="sxs-lookup"><span data-stu-id="412d0-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="412d0-111">Förloppsprocent = faktiska insatsen till dagens datum ÷ planerad insats för uppgiften</span><span class="sxs-lookup"><span data-stu-id="412d0-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="412d0-112">Uppskattning för att slutföra (ETC) = planerad insats – den faktiska insatsen hittills</span><span class="sxs-lookup"><span data-stu-id="412d0-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="412d0-113">Uppskattning för att slutföra (EAC) = planerad insats + den faktiska insatsen hittills</span><span class="sxs-lookup"><span data-stu-id="412d0-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="412d0-114">Planerad insatsavvikelse = planerat arbete – EAC</span><span class="sxs-lookup"><span data-stu-id="412d0-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="412d0-115">PSA visar en projektion av insatsavvikelsen för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="412d0-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="412d0-116">Om EAC är större än den planerade ansträngningen projiceras aktiviteten för att ta längre tid än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="412d0-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="412d0-117">Det ligger därför bakom schemat.</span><span class="sxs-lookup"><span data-stu-id="412d0-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="412d0-118">Om EAC är mindre än den planerade ansträngningen projiceras aktiviteten för att ta kortare tid än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="412d0-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="412d0-119">Det ligger därför framför schemat.</span><span class="sxs-lookup"><span data-stu-id="412d0-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="412d0-120">Omprojektion av arbete</span><span class="sxs-lookup"><span data-stu-id="412d0-120">Re-projecting effort</span></span>

<span data-ttu-id="412d0-121">Det är vanligt att projektledaren ändrar de ursprungliga uppskattningarna för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="412d0-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="412d0-122">Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status.</span><span class="sxs-lookup"><span data-stu-id="412d0-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="412d0-123">Vi rekommenderar dock inte att projektledare ändrar baslinjenumren, eftersom projektbaslinjen representerar den etablerade sanningen för projektets schema och kostnadsberäkning, och alla projektintressenter har gått med på det.</span><span class="sxs-lookup"><span data-stu-id="412d0-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="412d0-124">Det finns två sätt som en projektledare kan använda för att förnya arbetet för uppgifter:</span><span class="sxs-lookup"><span data-stu-id="412d0-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="412d0-125">Åsidosätt standard ETC med en ny uppskattning av den faktiska resterande insatsen för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="412d0-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="412d0-126">Åsidosätt standardförlopp i procent med en ny uppskattning av det faktiska förloppen för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="412d0-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="412d0-127">Var och en av dessa är en omberäkning av aktivitetens ETC, EAc och förloppsprocent och den planerade insatsavvikelsen för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="412d0-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="412d0-128">Procenten för EAC, ETC och förloppsprocent för sammanfattningsaktiviteterna beräknas även om, och produktionen skapas som en ny projektion av insatsavvikelsen.</span><span class="sxs-lookup"><span data-stu-id="412d0-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="412d0-129">Omprojektering av ansträngning för sammanfattningsuppgifter</span><span class="sxs-lookup"><span data-stu-id="412d0-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="412d0-130">Arbete för sammanfattningsuppgifter eller behållaruppgifter kan projiceras om.</span><span class="sxs-lookup"><span data-stu-id="412d0-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="412d0-131">Oavsett om användaren återskapar projekt med hjälp av den återstående insatsen eller förloppet i procent av sammanfattningsaktiviteterna börjar följande beräkningar:</span><span class="sxs-lookup"><span data-stu-id="412d0-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="412d0-132">Procentförloppet för EAC, ETC och aktiviteten beräknas.</span><span class="sxs-lookup"><span data-stu-id="412d0-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="412d0-133">Nya EAC fördelas nedåt till de underordnade uppgifterna i samma proportion som original EAC var på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="412d0-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="412d0-134">De nya EAC för var och en av de enskilda aktiviteterna till noderna för lövnoder beräknas.</span><span class="sxs-lookup"><span data-stu-id="412d0-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="412d0-135">De underordnade aktiviteterna som påverkas ned till lövnoder har deras ETC och förloppet omberäknas efter EAC-värdet.</span><span class="sxs-lookup"><span data-stu-id="412d0-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="412d0-136">Detta resulterar i en ny projektion för uppgiftens insatsavvikelse.</span><span class="sxs-lookup"><span data-stu-id="412d0-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="412d0-137">EAC för de sammanfattande aktiviteterna hela vägen till rotnoden beräknas om.</span><span class="sxs-lookup"><span data-stu-id="412d0-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="412d0-138">Vyn Kostnadsspårning</span><span class="sxs-lookup"><span data-stu-id="412d0-138">Cost tracking view</span></span> 

<span data-ttu-id="412d0-139">I vyn **kostnadsspårning** jämförs den faktiska kostnaden som spenderades för en aktivitet med den planerade kostnaden för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="412d0-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="412d0-140">Vyn visar endast arbetskostnader och inkluderar inga kostnader från utgiftsuppskattningarna.</span><span class="sxs-lookup"><span data-stu-id="412d0-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="412d0-141">I PSA används följande formler för att beräkna spårningsmått:</span><span class="sxs-lookup"><span data-stu-id="412d0-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="412d0-142">Procent av förbrukad kostnad = faktisk kostnad spenderad hittills ÷ planerad kostnad för uppgiften</span><span class="sxs-lookup"><span data-stu-id="412d0-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="412d0-143">Kostnad för att slutföra (CTC) = planerad kostnad – den faktiska kostnaden hittills</span><span class="sxs-lookup"><span data-stu-id="412d0-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="412d0-144">EAC = CTC + faktisk kostnad hittills</span><span class="sxs-lookup"><span data-stu-id="412d0-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="412d0-145">Planerad kostnadsavvikelse = planerad kostnad – EAC</span><span class="sxs-lookup"><span data-stu-id="412d0-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="412d0-146">En projektion av kostnadsavvikelsen visas på uppgiften.</span><span class="sxs-lookup"><span data-stu-id="412d0-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="412d0-147">Om EAC är större än den planerade kostnaden projiceras aktiviteten för att kosta mer än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="412d0-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="412d0-148">Därför prognostiseras den över budget.</span><span class="sxs-lookup"><span data-stu-id="412d0-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="412d0-149">Om EAC är mindre än den planerade kostnaden projiceras aktiviteten för att kosta mindre än vad som ursprungligen planerades.</span><span class="sxs-lookup"><span data-stu-id="412d0-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="412d0-150">Därför prognostiseras den under budget.</span><span class="sxs-lookup"><span data-stu-id="412d0-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="412d0-151">Projektledarens återprojektering av kostnaderna</span><span class="sxs-lookup"><span data-stu-id="412d0-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="412d0-152">När arbetsinsatsen återprojiceras räknas CTC, EAC, procent av förbrukad kostnad och planerad kostnadsavvikelse i vyn **kostnadsspårning**.</span><span class="sxs-lookup"><span data-stu-id="412d0-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="412d0-153">Sammanfattning av projektstatus</span><span class="sxs-lookup"><span data-stu-id="412d0-153">Project status summary</span></span>

<span data-ttu-id="412d0-154">Spåra data i **Insatsspårning** och **Kostnadsspårning** visas förloppet och kostnadsförbrukning på projektets rotnod, sammanfattningsaktiviteter och aktivitetsnivåerna på lövnodnivå.</span><span class="sxs-lookup"><span data-stu-id="412d0-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="412d0-155">I avsnittet **status** på sidan **projektentitet** visas en översikt över status på projektnivå.</span><span class="sxs-lookup"><span data-stu-id="412d0-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="412d0-156">Fält för statussammanfattning</span><span class="sxs-lookup"><span data-stu-id="412d0-156">Status summary fields</span></span>

<span data-ttu-id="412d0-157">Fältet **övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status.</span><span class="sxs-lookup"><span data-stu-id="412d0-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="412d0-158">Det använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker.</span><span class="sxs-lookup"><span data-stu-id="412d0-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="412d0-159">I fältet **kommentarer** kan projektledaren ange kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="412d0-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="412d0-160">Fältet **status uppdaterad för** är inte redigerbart och värdet är en tidstämpel som anger när status senast uppdaterades.</span><span class="sxs-lookup"><span data-stu-id="412d0-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="412d0-161">Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsdatumet.</span><span class="sxs-lookup"><span data-stu-id="412d0-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="412d0-162">När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva kan du ange att dessa fält till **Före**.</span><span class="sxs-lookup"><span data-stu-id="412d0-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="412d0-163">När schema och kostnadsavvikelse för rotnoden är negativa kan du ange dem till **Efter**.</span><span class="sxs-lookup"><span data-stu-id="412d0-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
