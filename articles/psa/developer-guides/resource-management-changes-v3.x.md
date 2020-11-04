---
title: Resurshanteringsändringar (Project Service Automation 3.x)
description: I det här ämnet finns information om ändringarna i området resurshantering.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085731"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="dc5a8-103">Resurshanteringsändringar (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="dc5a8-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="dc5a8-104">Avsnitten i det här ämne innehåller information om de ändringar som har gjorts i området resurshantering i Dynamics 365 Project Service Automation version 3.x.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="dc5a8-105">Projektberäkningar</span><span class="sxs-lookup"><span data-stu-id="dc5a8-105">Project estimates</span></span>

<span data-ttu-id="dc5a8-106">I stället för att basera sig på entiteten **msdyn\_projecttask** ( **Projektuppgift** ), baseras projektberäkningar på entiteten **msdyn\_resourceassignment** ( **resurstilldelning** ).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="dc5a8-107">Resurstilldelningar har blivit "källan till sanningen" för schemaläggning av aktiviteter och priser.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="dc5a8-108">Raduppgifter</span><span class="sxs-lookup"><span data-stu-id="dc5a8-108">Line tasks</span></span>

<span data-ttu-id="dc5a8-109">I PSA 3.x är raduppgifter föråldrade (inaktuella).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="dc5a8-110">Tilldelningarna pekar nu på hela uppgiften i stället för på raduppgifterna.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="dc5a8-111">Följande exempel visar hur en uppgift med namnet "testuppgift" tilldelas teammedlemmar A och B i tidigare versioner av PSA och PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="dc5a8-112">**Före PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="dc5a8-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="dc5a8-113">Testuppgift</span><span class="sxs-lookup"><span data-stu-id="dc5a8-113">Test task</span></span>

        - <span data-ttu-id="dc5a8-114">Testuppgift – raduppgift 1</span><span class="sxs-lookup"><span data-stu-id="dc5a8-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="dc5a8-115">Tilldelning till A</span><span class="sxs-lookup"><span data-stu-id="dc5a8-115">Assignment to A</span></span>

        - <span data-ttu-id="dc5a8-116">Testuppgift – raduppgift 2</span><span class="sxs-lookup"><span data-stu-id="dc5a8-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="dc5a8-117">Tilldelning till B</span><span class="sxs-lookup"><span data-stu-id="dc5a8-117">Assignment to B</span></span>

- <span data-ttu-id="dc5a8-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="dc5a8-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="dc5a8-119">Testuppgift</span><span class="sxs-lookup"><span data-stu-id="dc5a8-119">Test task</span></span>

        - <span data-ttu-id="dc5a8-120">Tilldelning till A</span><span class="sxs-lookup"><span data-stu-id="dc5a8-120">Assignment to A</span></span>
        - <span data-ttu-id="dc5a8-121">Tilldelning till B</span><span class="sxs-lookup"><span data-stu-id="dc5a8-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="dc5a8-122">Otilldelad tilldelning</span><span class="sxs-lookup"><span data-stu-id="dc5a8-122">Unassigned assignment</span></span>

<span data-ttu-id="dc5a8-123">I PSA 3.x är en otilldelad tilldelning en tilldelning som är tilldelad en **NULL** teammedlem och en **NULL** resurs.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="dc5a8-124">Tilldelningar som inte tilldelats kan ske i några situationer:</span><span class="sxs-lookup"><span data-stu-id="dc5a8-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="dc5a8-125">Om en uppgift har skapats men ännu inte tilldelats någon teammedlem skapas alltid en otilldelad tilldelning.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="dc5a8-126">Om alla tilldelningar för en uppgift tas bort, återskapas en otilldelad tilldelning för den uppgiften.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="dc5a8-127">Schemaläggningsfält på entiteten för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="dc5a8-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="dc5a8-128">Fälten i entiteten **msdyn\_projecttask** är inaktuella eller flyttade till entiteten **msdyn\_resourceassignment** eller så refereras de från entiteten **msdyn\_projectteam** ( **projektteammedlem** ).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="dc5a8-129">Inaktuellt fält i msdyn\_projecttask (projektuppgift)</span><span class="sxs-lookup"><span data-stu-id="dc5a8-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="dc5a8-130">Nytt fält i msdyn\_resourceassignment (resurstilldelning)</span><span class="sxs-lookup"><span data-stu-id="dc5a8-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="dc5a8-131">Kommentar</span><span class="sxs-lookup"><span data-stu-id="dc5a8-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="dc5a8-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="dc5a8-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="dc5a8-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc5a8-133">None</span></span> | |
| <span data-ttu-id="dc5a8-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="dc5a8-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="dc5a8-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc5a8-135">None</span></span> | |
| <span data-ttu-id="dc5a8-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="dc5a8-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="dc5a8-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc5a8-137">None</span></span> | |
| <span data-ttu-id="dc5a8-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="dc5a8-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="dc5a8-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc5a8-139">None</span></span> | |
| <span data-ttu-id="dc5a8-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="dc5a8-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="dc5a8-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="dc5a8-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="dc5a8-142">Formatet på datastrukturen för JavaScript Object Notation (JSON) som lagras i fältet har ändrats.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="dc5a8-143">Schemalägg profil</span><span class="sxs-lookup"><span data-stu-id="dc5a8-143">Schedule contour</span></span>

<span data-ttu-id="dc5a8-144">Schemalägg profil lagras i fältet **planerat arbete** ( **msdyn\_plannedwork** ) för varje entitet för **resurstilldelning** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="dc5a8-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="dc5a8-145">Structure</span></span>

<span data-ttu-id="dc5a8-146">Den nya strukturen för schemalägg profil består av flexibla tidsintervall som definieras för varje dag i schemat.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="dc5a8-147">Varje tidssektor har följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="dc5a8-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="dc5a8-148">**Start** – starten av arbetstimmarna för dagen enligt projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="dc5a8-149">**Slut** – Slutet av arbetstimmarna för dagen enligt projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="dc5a8-150">**Timmar** – antalet timmar som har tilldelats den dagen.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="dc5a8-151">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="dc5a8-151">**Example**</span></span>

<span data-ttu-id="dc5a8-152">I det här exemplet används en projektkalender där arbetsdagen är från 9:00 till 17:00 i UTC-8 tidszon.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="dc5a8-153">Automatisk schemaläggning och manuell schemaläggning</span><span class="sxs-lookup"><span data-stu-id="dc5a8-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="dc5a8-154">Om en uppgift schemaläggs automatiskt visas timmarna och uppgiftens varaktighet kan minskas.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="dc5a8-155">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="dc5a8-155">**Example**</span></span>

<span data-ttu-id="dc5a8-156">Följande uppgift schemaläggs automatiskt i 18 timmar om tre dagar (3 december 2018 till 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="dc5a8-157">Om en uppgift är manuellt schemalagd fördelas timmarna med alla datum.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="dc5a8-158">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="dc5a8-158">**Example**</span></span>

<span data-ttu-id="dc5a8-159">Följande uppgift schemaläggs manuellt i 18 timmar om tre dagar (3 december 2018 till 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="dc5a8-160">Tilldelningsenhet</span><span class="sxs-lookup"><span data-stu-id="dc5a8-160">Assignment unit</span></span>

<span data-ttu-id="dc5a8-161">Tilldelningsenheten är inaktuell i PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="dc5a8-162">Uppgiftens arbetsinsatstimmar är nu lika delade per dag, bland alla tilldelade resurser.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="dc5a8-163">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="dc5a8-163">**Example**</span></span>

<span data-ttu-id="dc5a8-164">I det här exemplet tilldelas uppgiften två resurser och schemaläggs automatiskt i 36 timmar om tre dagar (3 december 2018 till 5 december 2018).</span><span class="sxs-lookup"><span data-stu-id="dc5a8-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="dc5a8-165">Tilldelning 1:</span><span class="sxs-lookup"><span data-stu-id="dc5a8-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="dc5a8-166">Tilldelning 2:</span><span class="sxs-lookup"><span data-stu-id="dc5a8-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="dc5a8-167">Prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="dc5a8-167">Pricing dimensions</span></span>

<span data-ttu-id="dc5a8-168">I PSA 3.x har resursspecifika fält för prissättningsdimensioner (t.ex. **Roll** och **Organisationsenhet** ) tagits bort från entiteten **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="dc5a8-169">Dessa fält kan nu hämtas från motsvarande projektteammedlem ( **msdyn\_projectteam** ) för resurstilldelningen ( **msdyn\_resourceassignment** ) när projektberäkningar genereras.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="dc5a8-170">Ett nytt fält **msdyn\_organizationalunit** har lagts till i entiteten **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="dc5a8-171">Inaktuellt fält i msdyn\_projecttask (projektuppgift)</span><span class="sxs-lookup"><span data-stu-id="dc5a8-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="dc5a8-172">Fält från msdyn\_projectteam (projektteammedlem) som används i stället</span><span class="sxs-lookup"><span data-stu-id="dc5a8-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="dc5a8-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="dc5a8-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="dc5a8-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="dc5a8-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="dc5a8-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="dc5a8-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="dc5a8-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="dc5a8-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="dc5a8-177">Profiler</span><span class="sxs-lookup"><span data-stu-id="dc5a8-177">Contours</span></span>

<span data-ttu-id="dc5a8-178">Fälten prissättnings- och beräkningsprofil är inaktuella i entiteten **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="dc5a8-179">De har flyttats till entiteten **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="dc5a8-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="dc5a8-180">Inaktuellt fält i msdyn\_projecttask (projektuppgift)</span><span class="sxs-lookup"><span data-stu-id="dc5a8-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="dc5a8-181">Nytt fält i msdyn\_resourceassignment (resurstilldelning)</span><span class="sxs-lookup"><span data-stu-id="dc5a8-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="dc5a8-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="dc5a8-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="dc5a8-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="dc5a8-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="dc5a8-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="dc5a8-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="dc5a8-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="dc5a8-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="dc5a8-186">Följande fält har lagts till entiteten **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="dc5a8-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="dc5a8-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="dc5a8-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="dc5a8-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dc5a8-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="dc5a8-189">Följande fält för planerade, faktiska och resterande kostnader och försäljningar ändras inte i entiteten **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="dc5a8-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="dc5a8-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="dc5a8-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="dc5a8-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="dc5a8-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="dc5a8-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="dc5a8-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="dc5a8-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="dc5a8-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="dc5a8-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="dc5a8-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="dc5a8-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="dc5a8-195">msdyn\_remainingsales</span></span>
