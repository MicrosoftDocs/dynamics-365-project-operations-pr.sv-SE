---
title: Resurshanteringsändringar (Project Service Automation 3.x)
description: I det här ämnet finns information om ändringarna i området resurshantering.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007838"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="2f16a-103">Resurshanteringsändringar (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="2f16a-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="2f16a-104">Avsnitten i det här ämne innehåller information om de ändringar som har gjorts i området resurshantering i Dynamics 365 Project Service Automation version 3.x.</span><span class="sxs-lookup"><span data-stu-id="2f16a-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="2f16a-105">Projektberäkningar</span><span class="sxs-lookup"><span data-stu-id="2f16a-105">Project estimates</span></span>

<span data-ttu-id="2f16a-106">I stället för att basera sig på entiteten **msdyn\_projecttask** (**Projektuppgift**), baseras projektberäkningar på entiteten **msdyn\_resourceassignment** (**resurstilldelning**).</span><span class="sxs-lookup"><span data-stu-id="2f16a-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="2f16a-107">Resurstilldelningar har blivit "källan till sanningen" för schemaläggning av aktiviteter och priser.</span><span class="sxs-lookup"><span data-stu-id="2f16a-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="2f16a-108">Raduppgifter</span><span class="sxs-lookup"><span data-stu-id="2f16a-108">Line tasks</span></span>

<span data-ttu-id="2f16a-109">I PSA 3.x är raduppgifter föråldrade (inaktuella).</span><span class="sxs-lookup"><span data-stu-id="2f16a-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="2f16a-110">Tilldelningarna pekar nu på hela uppgiften i stället för på raduppgifterna.</span><span class="sxs-lookup"><span data-stu-id="2f16a-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="2f16a-111">Följande exempel visar hur en uppgift med namnet "testuppgift" tilldelas teammedlemmar A och B i tidigare versioner av PSA och PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="2f16a-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="2f16a-112">**Före PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="2f16a-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="2f16a-113">Testuppgift</span><span class="sxs-lookup"><span data-stu-id="2f16a-113">Test task</span></span>

        - <span data-ttu-id="2f16a-114">Testuppgift – raduppgift 1</span><span class="sxs-lookup"><span data-stu-id="2f16a-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="2f16a-115">Tilldelning till A</span><span class="sxs-lookup"><span data-stu-id="2f16a-115">Assignment to A</span></span>

        - <span data-ttu-id="2f16a-116">Testuppgift – raduppgift 2</span><span class="sxs-lookup"><span data-stu-id="2f16a-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="2f16a-117">Tilldelning till B</span><span class="sxs-lookup"><span data-stu-id="2f16a-117">Assignment to B</span></span>

- <span data-ttu-id="2f16a-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="2f16a-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="2f16a-119">Testuppgift</span><span class="sxs-lookup"><span data-stu-id="2f16a-119">Test task</span></span>

        - <span data-ttu-id="2f16a-120">Tilldelning till A</span><span class="sxs-lookup"><span data-stu-id="2f16a-120">Assignment to A</span></span>
        - <span data-ttu-id="2f16a-121">Tilldelning till B</span><span class="sxs-lookup"><span data-stu-id="2f16a-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="2f16a-122">Otilldelad tilldelning</span><span class="sxs-lookup"><span data-stu-id="2f16a-122">Unassigned assignment</span></span>

<span data-ttu-id="2f16a-123">I PSA 3.x är en otilldelad tilldelning en tilldelning som är tilldelad en **NULL** teammedlem och en **NULL** resurs.</span><span class="sxs-lookup"><span data-stu-id="2f16a-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="2f16a-124">Tilldelningar som inte tilldelats kan ske i några situationer:</span><span class="sxs-lookup"><span data-stu-id="2f16a-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="2f16a-125">Om en uppgift har skapats men ännu inte tilldelats någon teammedlem skapas alltid en otilldelad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="2f16a-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="2f16a-126">Om alla tilldelningar för en uppgift tas bort, återskapas en otilldelad tilldelning för den uppgiften.</span><span class="sxs-lookup"><span data-stu-id="2f16a-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="2f16a-127">Schemaläggningsfält på entiteten för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="2f16a-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="2f16a-128">Fälten i entiteten **msdyn\_projecttask** är inaktuella eller flyttade till entiteten **msdyn\_resourceassignment** eller så refereras de från entiteten **msdyn\_projectteam** (**projektteammedlem**).</span><span class="sxs-lookup"><span data-stu-id="2f16a-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="2f16a-129">Inaktuellt fält i msdyn\_projecttask (projektuppgift)</span><span class="sxs-lookup"><span data-stu-id="2f16a-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="2f16a-130">Nytt fält i msdyn\_resourceassignment (resurstilldelning)</span><span class="sxs-lookup"><span data-stu-id="2f16a-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="2f16a-131">Kommentar</span><span class="sxs-lookup"><span data-stu-id="2f16a-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="2f16a-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="2f16a-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="2f16a-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f16a-133">None</span></span> | |
| <span data-ttu-id="2f16a-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="2f16a-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="2f16a-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f16a-135">None</span></span> | |
| <span data-ttu-id="2f16a-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="2f16a-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="2f16a-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f16a-137">None</span></span> | |
| <span data-ttu-id="2f16a-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="2f16a-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="2f16a-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f16a-139">None</span></span> | |
| <span data-ttu-id="2f16a-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="2f16a-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="2f16a-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="2f16a-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="2f16a-142">Formatet på datastrukturen för JavaScript Object Notation (JSON) som lagras i fältet har ändrats.</span><span class="sxs-lookup"><span data-stu-id="2f16a-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="2f16a-143">Schemalägg profil</span><span class="sxs-lookup"><span data-stu-id="2f16a-143">Schedule contour</span></span>

<span data-ttu-id="2f16a-144">Schemalägg profil lagras i fältet **planerat arbete** (**msdyn\_plannedwork**) för varje entitet för **resurstilldelning** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="2f16a-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="2f16a-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="2f16a-145">Structure</span></span>

<span data-ttu-id="2f16a-146">Den nya strukturen för schemalägg profil består av flexibla tidsintervall som definieras för varje dag i schemat.</span><span class="sxs-lookup"><span data-stu-id="2f16a-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="2f16a-147">Varje tidssektor har följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="2f16a-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="2f16a-148">**Start** – starten av arbetstimmarna för dagen enligt projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="2f16a-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="2f16a-149">**Slut** – Slutet av arbetstimmarna för dagen enligt projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="2f16a-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="2f16a-150">**Timmar** – antalet timmar som har tilldelats den dagen.</span><span class="sxs-lookup"><span data-stu-id="2f16a-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="2f16a-151">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="2f16a-151">**Example**</span></span>

<span data-ttu-id="2f16a-152">I det här exemplet används en projektkalender där arbetsdagen är från 9:00 till 17:00 i UTC-8 tidszon.</span><span class="sxs-lookup"><span data-stu-id="2f16a-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="2f16a-153">Automatisk schemaläggning och manuell schemaläggning</span><span class="sxs-lookup"><span data-stu-id="2f16a-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="2f16a-154">Om en uppgift schemaläggs automatiskt visas timmarna och uppgiftens varaktighet kan minskas.</span><span class="sxs-lookup"><span data-stu-id="2f16a-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="2f16a-155">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="2f16a-155">**Example**</span></span>

<span data-ttu-id="2f16a-156">Följande uppgift schemaläggs automatiskt i 18 timmar om tre dagar (3 december 2018 till 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="2f16a-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="2f16a-157">Om en uppgift är manuellt schemalagd fördelas timmarna med alla datum.</span><span class="sxs-lookup"><span data-stu-id="2f16a-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="2f16a-158">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="2f16a-158">**Example**</span></span>

<span data-ttu-id="2f16a-159">Följande uppgift schemaläggs manuellt i 18 timmar om tre dagar (3 december 2018 till 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="2f16a-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="2f16a-160">Tilldelningsenhet</span><span class="sxs-lookup"><span data-stu-id="2f16a-160">Assignment unit</span></span>

<span data-ttu-id="2f16a-161">Tilldelningsenheten är inaktuell i PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="2f16a-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="2f16a-162">Uppgiftens arbetsinsatstimmar är nu lika delade per dag, bland alla tilldelade resurser.</span><span class="sxs-lookup"><span data-stu-id="2f16a-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="2f16a-163">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="2f16a-163">**Example**</span></span>

<span data-ttu-id="2f16a-164">I det här exemplet tilldelas uppgiften två resurser och schemaläggs automatiskt i 36 timmar om tre dagar (3 december 2018 till 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="2f16a-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="2f16a-165">Tilldelning 1:</span><span class="sxs-lookup"><span data-stu-id="2f16a-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="2f16a-166">Tilldelning 2:</span><span class="sxs-lookup"><span data-stu-id="2f16a-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="2f16a-167">Prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="2f16a-167">Pricing dimensions</span></span>

<span data-ttu-id="2f16a-168">I PSA 3.x har resursspecifika fält för prissättningsdimensioner (t.ex. **Roll** och **Organisationsenhet**) tagits bort från entiteten **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="2f16a-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="2f16a-169">Dessa fält kan nu hämtas från motsvarande projektteammedlem (**msdyn\_projectteam**) för resurstilldelningen (**msdyn\_resourceassignment**) när projektberäkningar genereras.</span><span class="sxs-lookup"><span data-stu-id="2f16a-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="2f16a-170">Ett nytt fält **msdyn\_organizationalunit** har lagts till i entiteten **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="2f16a-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="2f16a-171">Inaktuellt fält i msdyn\_projecttask (projektuppgift)</span><span class="sxs-lookup"><span data-stu-id="2f16a-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="2f16a-172">Fält från msdyn\_projectteam (projektteammedlem) som används i stället</span><span class="sxs-lookup"><span data-stu-id="2f16a-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="2f16a-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="2f16a-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="2f16a-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="2f16a-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="2f16a-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="2f16a-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="2f16a-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="2f16a-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="2f16a-177">Profiler</span><span class="sxs-lookup"><span data-stu-id="2f16a-177">Contours</span></span>

<span data-ttu-id="2f16a-178">Fälten prissättnings- och beräkningsprofil är inaktuella i entiteten **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="2f16a-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="2f16a-179">De har flyttats till entiteten **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="2f16a-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="2f16a-180">Inaktuellt fält i msdyn\_projecttask (projektuppgift)</span><span class="sxs-lookup"><span data-stu-id="2f16a-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="2f16a-181">Nytt fält i msdyn\_resourceassignment (resurstilldelning)</span><span class="sxs-lookup"><span data-stu-id="2f16a-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="2f16a-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="2f16a-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="2f16a-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="2f16a-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="2f16a-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="2f16a-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="2f16a-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="2f16a-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="2f16a-186">Följande fält har lagts till entiteten **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="2f16a-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="2f16a-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="2f16a-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="2f16a-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2f16a-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="2f16a-189">Följande fält för planerade, faktiska och resterande kostnader och försäljningar ändras inte i entiteten **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="2f16a-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="2f16a-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="2f16a-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="2f16a-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2f16a-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="2f16a-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="2f16a-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="2f16a-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="2f16a-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="2f16a-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="2f16a-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="2f16a-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="2f16a-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]