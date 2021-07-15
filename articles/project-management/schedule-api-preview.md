---
title: Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter
description: Detta ämne innehåller information och exempel för användning av API:er för Projektschema.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293249"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="fd506-103">Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="fd506-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="fd506-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="fd506-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="fd506-105">Vissa eller alla funktioner som anges i det här ämnet är tillgängliga som en del av en förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="fd506-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="fd506-106">Innehållet och funktionerna kan komma att ändras.</span><span class="sxs-lookup"><span data-stu-id="fd506-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="fd506-107">Schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="fd506-107">Scheduling entities</span></span>

<span data-ttu-id="fd506-108">API:er för projektschemaläggning gör det möjligt att skapa, uppdatera och ta bort åtgärder med **Schemaläggningsentiteter**.</span><span class="sxs-lookup"><span data-stu-id="fd506-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="fd506-109">Dessa entiteter hanteras med schemaläggningsmotorn i Projekt för webben.</span><span class="sxs-lookup"><span data-stu-id="fd506-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="fd506-110">Skapa, uppdatera och ta bort operationer med **Schemaläggningsentiteter** begränsades i tidigare versioner av Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fd506-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="fd506-111">I följande tabell visas en fullständig lista över entiteterna i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="fd506-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="fd506-112">Entitetsnamn</span><span class="sxs-lookup"><span data-stu-id="fd506-112">Entity name</span></span>  | <span data-ttu-id="fd506-113">Entitetens logiska namn</span><span class="sxs-lookup"><span data-stu-id="fd506-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="fd506-114">Project</span><span class="sxs-lookup"><span data-stu-id="fd506-114">Project</span></span> | <span data-ttu-id="fd506-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="fd506-115">msdyn_project</span></span> |
| <span data-ttu-id="fd506-116">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="fd506-116">Project Task</span></span>  | <span data-ttu-id="fd506-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="fd506-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="fd506-118">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="fd506-118">Project Task Dependency</span></span>  | <span data-ttu-id="fd506-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="fd506-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="fd506-120">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="fd506-120">Resource Assignment</span></span> | <span data-ttu-id="fd506-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="fd506-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="fd506-122">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="fd506-122">Project Bucket</span></span>  | <span data-ttu-id="fd506-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="fd506-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="fd506-124">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="fd506-124">Project Team Member</span></span> | <span data-ttu-id="fd506-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="fd506-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="fd506-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="fd506-126">OperationSet</span></span>

<span data-ttu-id="fd506-127">OperationSet är ett enhetsmönster som kan användas när flera schemapåverkande förfrågningar måste bearbetas inom en transaktioner.</span><span class="sxs-lookup"><span data-stu-id="fd506-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="fd506-128">Projekttidsplan-API</span><span class="sxs-lookup"><span data-stu-id="fd506-128">Project schedule APIs</span></span>

<span data-ttu-id="fd506-129">Följande är en lista med aktuella API:er för Projektschema.</span><span class="sxs-lookup"><span data-stu-id="fd506-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="fd506-130">**msdyn_CreateProjectV1**: Detta API kan användas för att skapa ett projekt.</span><span class="sxs-lookup"><span data-stu-id="fd506-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="fd506-131">Projekt och standardprojektgrupp skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="fd506-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="fd506-132">**msdyn_CreateTeamMemberV1**: Detta API kan användas för att skapa en projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="fd506-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="fd506-133">Teammedlemsposten skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="fd506-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="fd506-134">**msdyn_CreateOperationSetV1**: Detta API kan användas för att schemalägga flera förfrågningar som måste utföras inom en transaktionen.</span><span class="sxs-lookup"><span data-stu-id="fd506-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="fd506-135">**msdyn_PSSCreateV1**: Det här API:et kan användas för att skapa en entitet.</span><span class="sxs-lookup"><span data-stu-id="fd506-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="fd506-136">Entiteten kan vara någon av de projektschemaläggningsentiteter som stöder åtgärden skapa.</span><span class="sxs-lookup"><span data-stu-id="fd506-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="fd506-137">**msdyn_PSSUpdateV1**: Det här API:et kan användas för att uppdatera en entitet.</span><span class="sxs-lookup"><span data-stu-id="fd506-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="fd506-138">Entiteten kan vara någon av de projektschemaläggningsentiteter som stöder åtgärden uppdatera.</span><span class="sxs-lookup"><span data-stu-id="fd506-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="fd506-139">**msdyn_PSSDeleteV1**: Det här API:et kan användas för att ta bort en entitet.</span><span class="sxs-lookup"><span data-stu-id="fd506-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="fd506-140">Entiteten kan vara någon av de projektschemaläggningsentiteter som stöder åtgärden ta bort.</span><span class="sxs-lookup"><span data-stu-id="fd506-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="fd506-141">**msdyn_ExecuteOperationSetV1**: Detta API används för att köra alla åtgärder inom den angivna åtgärdsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="fd506-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="fd506-142">Använda API:er för Projektscheman med OperationSet</span><span class="sxs-lookup"><span data-stu-id="fd506-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="fd506-143">Eftersom poster med både **CreateProjectV1** och **CreateTeamMemberV1** skapas direkt kan dessa API:er inte användas direkt i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="fd506-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="fd506-144">Men du kan använda API för att skapa nödvändiga poster, skapa en **OperationSet** och sedan använda dessa förskapade poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="fd506-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="fd506-145">Åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="fd506-145">Supported operations</span></span>

| <span data-ttu-id="fd506-146">Schemaläggningsentitet</span><span class="sxs-lookup"><span data-stu-id="fd506-146">Scheduling entity</span></span> | <span data-ttu-id="fd506-147">Skapa</span><span class="sxs-lookup"><span data-stu-id="fd506-147">Create</span></span> | <span data-ttu-id="fd506-148">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="fd506-148">Update</span></span> | <span data-ttu-id="fd506-149">Delete</span><span class="sxs-lookup"><span data-stu-id="fd506-149">Delete</span></span> | <span data-ttu-id="fd506-150">Viktigt!</span><span class="sxs-lookup"><span data-stu-id="fd506-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="fd506-151">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="fd506-151">Project task</span></span> | <span data-ttu-id="fd506-152">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-152">Yes</span></span> | <span data-ttu-id="fd506-153">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-153">Yes</span></span> | <span data-ttu-id="fd506-154">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-154">Yes</span></span> | <span data-ttu-id="fd506-155">Nej</span><span class="sxs-lookup"><span data-stu-id="fd506-155">None</span></span> |
| <span data-ttu-id="fd506-156">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="fd506-156">Project task dependency</span></span> | <span data-ttu-id="fd506-157">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-157">Yes</span></span> | <span data-ttu-id="fd506-158">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-158">Yes</span></span> | | <span data-ttu-id="fd506-159">Poster för projektuppgiftsberoende uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="fd506-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="fd506-160">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="fd506-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="fd506-161">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="fd506-161">Resource assignment</span></span> | <span data-ttu-id="fd506-162">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-162">Yes</span></span> | <span data-ttu-id="fd506-163">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-163">Yes</span></span> | | <span data-ttu-id="fd506-164">Operationer med följande fält stöds inte: **BookableResourceID**, **Insats**, **EffortCompleted**, **EffortRemaining** och **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="fd506-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="fd506-165">Resurstilldelningsposter uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="fd506-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="fd506-166">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="fd506-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="fd506-167">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="fd506-167">Project bucket</span></span> | <span data-ttu-id="fd506-168">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="fd506-168">N/A</span></span> | <span data-ttu-id="fd506-169">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="fd506-169">N/A</span></span> | <span data-ttu-id="fd506-170">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="fd506-170">N/A</span></span> | <span data-ttu-id="fd506-171">Standardgruppen skapas för att använda API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="fd506-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="fd506-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="fd506-172">Project team member</span></span> | <span data-ttu-id="fd506-173">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-173">Yes</span></span> | <span data-ttu-id="fd506-174">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-174">Yes</span></span> | <span data-ttu-id="fd506-175">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-175">Yes</span></span> | <span data-ttu-id="fd506-176">För att skapa operation, använda API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="fd506-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="fd506-177">Project</span><span class="sxs-lookup"><span data-stu-id="fd506-177">Project</span></span> | <span data-ttu-id="fd506-178">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-178">Yes</span></span> | <span data-ttu-id="fd506-179">Ja</span><span class="sxs-lookup"><span data-stu-id="fd506-179">Yes</span></span> | <span data-ttu-id="fd506-180">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="fd506-180">N/A</span></span> | <span data-ttu-id="fd506-181">Operationer med följande fält stöds inte: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Insats**, **EffortCompleted**, **EffortRemaining**, **Förlopp**, **Slutför**, **TaskEarliestStart** och **Varaktighet**.</span><span class="sxs-lookup"><span data-stu-id="fd506-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="fd506-182">Dessa API:er kan anropas med entitetsobjekt som innehåller anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="fd506-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="fd506-183">ID-egenskapen är valfri.</span><span class="sxs-lookup"><span data-stu-id="fd506-183">The ID property is optional.</span></span> <span data-ttu-id="fd506-184">Om det finns ett undantag försöker systemet använda det och ett undantag om det inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="fd506-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="fd506-185">Om den inte finns genererar systemet den.</span><span class="sxs-lookup"><span data-stu-id="fd506-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="fd506-186">Begränsade fält</span><span class="sxs-lookup"><span data-stu-id="fd506-186">Restricted fields</span></span>

<span data-ttu-id="fd506-187">I följande tabeller definieras fälten som är begränsade från **Skapa** och **Redigera.**</span><span class="sxs-lookup"><span data-stu-id="fd506-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="fd506-188">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="fd506-188">Project task</span></span>

| <span data-ttu-id="fd506-189">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="fd506-189">**Logical name**</span></span>                       | <span data-ttu-id="fd506-190">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="fd506-190">**Can create**</span></span> | <span data-ttu-id="fd506-191">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="fd506-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="fd506-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="fd506-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="fd506-193">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-193">no</span></span>             | <span data-ttu-id="fd506-194">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-194">no</span></span>               |
| <span data-ttu-id="fd506-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="fd506-196">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-196">no</span></span>             | <span data-ttu-id="fd506-197">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-197">no</span></span>               |
| <span data-ttu-id="fd506-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="fd506-198">msdyn_actualend</span></span>                        | <span data-ttu-id="fd506-199">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-199">no</span></span>             | <span data-ttu-id="fd506-200">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-200">no</span></span>               |
| <span data-ttu-id="fd506-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="fd506-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="fd506-202">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-202">no</span></span>             | <span data-ttu-id="fd506-203">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-203">no</span></span>               |
| <span data-ttu-id="fd506-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="fd506-205">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-205">no</span></span>             | <span data-ttu-id="fd506-206">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-206">no</span></span>               |
| <span data-ttu-id="fd506-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="fd506-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="fd506-208">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-208">no</span></span>             | <span data-ttu-id="fd506-209">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-209">no</span></span>               |
| <span data-ttu-id="fd506-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="fd506-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="fd506-211">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-211">no</span></span>             | <span data-ttu-id="fd506-212">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-212">no</span></span>               |
| <span data-ttu-id="fd506-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="fd506-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="fd506-214">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-214">no</span></span>             | <span data-ttu-id="fd506-215">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-215">no</span></span>               |
| <span data-ttu-id="fd506-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="fd506-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="fd506-217">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-217">no</span></span>             | <span data-ttu-id="fd506-218">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-218">no</span></span>               |
| <span data-ttu-id="fd506-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fd506-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="fd506-220">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-220">no</span></span>             | <span data-ttu-id="fd506-221">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-221">no</span></span>               |
| <span data-ttu-id="fd506-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="fd506-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="fd506-223">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-223">no</span></span>             | <span data-ttu-id="fd506-224">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-224">no</span></span>               |
| <span data-ttu-id="fd506-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="fd506-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="fd506-226">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-226">no</span></span>             | <span data-ttu-id="fd506-227">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-227">no</span></span>               |
| <span data-ttu-id="fd506-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="fd506-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="fd506-229">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-229">no</span></span>             | <span data-ttu-id="fd506-230">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-230">no</span></span>               |
| <span data-ttu-id="fd506-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="fd506-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="fd506-232">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-232">no</span></span>             | <span data-ttu-id="fd506-233">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-233">no</span></span>               |
| <span data-ttu-id="fd506-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="fd506-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="fd506-235">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-235">no</span></span>             | <span data-ttu-id="fd506-236">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-236">no</span></span>               |
| <span data-ttu-id="fd506-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="fd506-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="fd506-238">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-238">no</span></span>             | <span data-ttu-id="fd506-239">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-239">no</span></span>               |
| <span data-ttu-id="fd506-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="fd506-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="fd506-241">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-241">no</span></span>             | <span data-ttu-id="fd506-242">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-242">no</span></span>               |
| <span data-ttu-id="fd506-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="fd506-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="fd506-244">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-244">no</span></span>             | <span data-ttu-id="fd506-245">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-245">no</span></span>               |
| <span data-ttu-id="fd506-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="fd506-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="fd506-247">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-247">no</span></span>             | <span data-ttu-id="fd506-248">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-248">no</span></span>               |
| <span data-ttu-id="fd506-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="fd506-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="fd506-250">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-250">no</span></span>             | <span data-ttu-id="fd506-251">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-251">no</span></span>               |
| <span data-ttu-id="fd506-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="fd506-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="fd506-253">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-253">no</span></span>             | <span data-ttu-id="fd506-254">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-254">no</span></span>               |
| <span data-ttu-id="fd506-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="fd506-256">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-256">no</span></span>             | <span data-ttu-id="fd506-257">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-257">no</span></span>               |
| <span data-ttu-id="fd506-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="fd506-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="fd506-259">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-259">no</span></span>             | <span data-ttu-id="fd506-260">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-260">no</span></span>               |
| <span data-ttu-id="fd506-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="fd506-262">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-262">no</span></span>             | <span data-ttu-id="fd506-263">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-263">no</span></span>               |
| <span data-ttu-id="fd506-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="fd506-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="fd506-265">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-265">no</span></span>             | <span data-ttu-id="fd506-266">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-266">no</span></span>               |
| <span data-ttu-id="fd506-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="fd506-267">msdyn_progress</span></span>                         | <span data-ttu-id="fd506-268">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-268">no</span></span>             | <span data-ttu-id="fd506-269">nej (ja för P4W)</span><span class="sxs-lookup"><span data-stu-id="fd506-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="fd506-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="fd506-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="fd506-271">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-271">no</span></span>             | <span data-ttu-id="fd506-272">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-272">no</span></span>               |
| <span data-ttu-id="fd506-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="fd506-274">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-274">no</span></span>             | <span data-ttu-id="fd506-275">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-275">no</span></span>               |
| <span data-ttu-id="fd506-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="fd506-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="fd506-277">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-277">no</span></span>             | <span data-ttu-id="fd506-278">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-278">no</span></span>               |
| <span data-ttu-id="fd506-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="fd506-280">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-280">no</span></span>             | <span data-ttu-id="fd506-281">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-281">no</span></span>               |
| <span data-ttu-id="fd506-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="fd506-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="fd506-283">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-283">no</span></span>             | <span data-ttu-id="fd506-284">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-284">no</span></span>               |
| <span data-ttu-id="fd506-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="fd506-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="fd506-286">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-286">no</span></span>             | <span data-ttu-id="fd506-287">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-287">no</span></span>               |
| <span data-ttu-id="fd506-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="fd506-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="fd506-289">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-289">no</span></span>             | <span data-ttu-id="fd506-290">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-290">no</span></span>               |
| <span data-ttu-id="fd506-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="fd506-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="fd506-292">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-292">no</span></span>             | <span data-ttu-id="fd506-293">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-293">no</span></span>               |
| <span data-ttu-id="fd506-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="fd506-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="fd506-295">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-295">no</span></span>             | <span data-ttu-id="fd506-296">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-296">no</span></span>               |
| <span data-ttu-id="fd506-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="fd506-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="fd506-298">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-298">no</span></span>             | <span data-ttu-id="fd506-299">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-299">no</span></span>               |
| <span data-ttu-id="fd506-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="fd506-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="fd506-301">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-301">no</span></span>             | <span data-ttu-id="fd506-302">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-302">no</span></span>               |
| <span data-ttu-id="fd506-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="fd506-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="fd506-304">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-304">no</span></span>             | <span data-ttu-id="fd506-305">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-305">no</span></span>               |
| <span data-ttu-id="fd506-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="fd506-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="fd506-307">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-307">no</span></span>             | <span data-ttu-id="fd506-308">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-308">no</span></span>               |
| <span data-ttu-id="fd506-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="fd506-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="fd506-310">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-310">no</span></span>             | <span data-ttu-id="fd506-311">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-311">no</span></span>               |
| <span data-ttu-id="fd506-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="fd506-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="fd506-313">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-313">no</span></span>             | <span data-ttu-id="fd506-314">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-314">no</span></span>               |
| <span data-ttu-id="fd506-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="fd506-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="fd506-316">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-316">no</span></span>             | <span data-ttu-id="fd506-317">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-317">no</span></span>               |
| <span data-ttu-id="fd506-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="fd506-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="fd506-319">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-319">no</span></span>             | <span data-ttu-id="fd506-320">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-320">no</span></span>               |
| <span data-ttu-id="fd506-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="fd506-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="fd506-322">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-322">no</span></span>             | <span data-ttu-id="fd506-323">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-323">no</span></span>               |
| <span data-ttu-id="fd506-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="fd506-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="fd506-325">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-325">no</span></span>             | <span data-ttu-id="fd506-326">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-326">no</span></span>               |
| <span data-ttu-id="fd506-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="fd506-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="fd506-328">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-328">no</span></span>             | <span data-ttu-id="fd506-329">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-329">no</span></span>               |
| <span data-ttu-id="fd506-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="fd506-330">msdyn_summary</span></span>                          | <span data-ttu-id="fd506-331">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-331">no</span></span>             | <span data-ttu-id="fd506-332">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-332">no</span></span>               |
| <span data-ttu-id="fd506-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="fd506-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="fd506-334">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-334">no</span></span>             | <span data-ttu-id="fd506-335">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-335">no</span></span>               |
| <span data-ttu-id="fd506-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="fd506-337">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-337">no</span></span>             | <span data-ttu-id="fd506-338">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="fd506-339">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="fd506-339">Project task dependency</span></span>

| <span data-ttu-id="fd506-340">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="fd506-340">**Logical name**</span></span>              | <span data-ttu-id="fd506-341">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="fd506-341">**Can create**</span></span> | <span data-ttu-id="fd506-342">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="fd506-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="fd506-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="fd506-343">msdyn_linktype</span></span>                | <span data-ttu-id="fd506-344">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-344">no</span></span>             | <span data-ttu-id="fd506-345">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-345">no</span></span>           |
| <span data-ttu-id="fd506-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="fd506-346">msdyn_linktypename</span></span>            | <span data-ttu-id="fd506-347">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-347">no</span></span>             | <span data-ttu-id="fd506-348">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-348">no</span></span>           |
| <span data-ttu-id="fd506-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="fd506-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="fd506-350">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-350">yes</span></span>            | <span data-ttu-id="fd506-351">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-351">no</span></span>           |
| <span data-ttu-id="fd506-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="fd506-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="fd506-353">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-353">yes</span></span>            | <span data-ttu-id="fd506-354">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-354">no</span></span>           |
| <span data-ttu-id="fd506-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="fd506-355">msdyn_project</span></span>                 | <span data-ttu-id="fd506-356">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-356">yes</span></span>            | <span data-ttu-id="fd506-357">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-357">no</span></span>           |
| <span data-ttu-id="fd506-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="fd506-358">msdyn_projectname</span></span>             | <span data-ttu-id="fd506-359">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-359">yes</span></span>            | <span data-ttu-id="fd506-360">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-360">no</span></span>           |
| <span data-ttu-id="fd506-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="fd506-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="fd506-362">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-362">yes</span></span>            | <span data-ttu-id="fd506-363">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-363">no</span></span>           |
| <span data-ttu-id="fd506-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="fd506-364">msdyn_successortask</span></span>           | <span data-ttu-id="fd506-365">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-365">yes</span></span>            | <span data-ttu-id="fd506-366">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-366">no</span></span>           |
| <span data-ttu-id="fd506-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="fd506-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="fd506-368">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-368">yes</span></span>            | <span data-ttu-id="fd506-369">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="fd506-370">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="fd506-370">Resource assignment</span></span>

| <span data-ttu-id="fd506-371">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="fd506-371">**Logical name**</span></span>             | <span data-ttu-id="fd506-372">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="fd506-372">**Can create**</span></span> | <span data-ttu-id="fd506-373">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="fd506-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="fd506-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="fd506-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="fd506-375">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-375">yes</span></span>            | <span data-ttu-id="fd506-376">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-376">no</span></span>           |
| <span data-ttu-id="fd506-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="fd506-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="fd506-378">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-378">yes</span></span>            | <span data-ttu-id="fd506-379">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-379">no</span></span>           |
| <span data-ttu-id="fd506-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="fd506-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="fd506-381">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-381">no</span></span>             | <span data-ttu-id="fd506-382">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-382">no</span></span>           |
| <span data-ttu-id="fd506-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="fd506-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="fd506-384">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-384">no</span></span>             | <span data-ttu-id="fd506-385">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-385">no</span></span>           |
| <span data-ttu-id="fd506-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="fd506-386">msdyn_committype</span></span>             | <span data-ttu-id="fd506-387">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-387">no</span></span>             | <span data-ttu-id="fd506-388">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-388">no</span></span>           |
| <span data-ttu-id="fd506-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="fd506-389">msdyn_committypename</span></span>         | <span data-ttu-id="fd506-390">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-390">no</span></span>             | <span data-ttu-id="fd506-391">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-391">no</span></span>           |
| <span data-ttu-id="fd506-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="fd506-392">msdyn_effort</span></span>                 | <span data-ttu-id="fd506-393">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-393">no</span></span>             | <span data-ttu-id="fd506-394">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-394">no</span></span>           |
| <span data-ttu-id="fd506-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fd506-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="fd506-396">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-396">no</span></span>             | <span data-ttu-id="fd506-397">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-397">no</span></span>           |
| <span data-ttu-id="fd506-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="fd506-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="fd506-399">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-399">no</span></span>             | <span data-ttu-id="fd506-400">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-400">no</span></span>           |
| <span data-ttu-id="fd506-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="fd506-401">msdyn_finish</span></span>                 | <span data-ttu-id="fd506-402">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-402">no</span></span>             | <span data-ttu-id="fd506-403">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-403">no</span></span>           |
| <span data-ttu-id="fd506-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="fd506-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="fd506-405">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-405">no</span></span>             | <span data-ttu-id="fd506-406">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-406">no</span></span>           |
| <span data-ttu-id="fd506-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="fd506-408">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-408">no</span></span>             | <span data-ttu-id="fd506-409">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-409">no</span></span>           |
| <span data-ttu-id="fd506-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="fd506-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="fd506-411">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-411">no</span></span>             | <span data-ttu-id="fd506-412">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-412">no</span></span>           |
| <span data-ttu-id="fd506-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="fd506-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="fd506-414">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-414">no</span></span>             | <span data-ttu-id="fd506-415">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-415">no</span></span>           |
| <span data-ttu-id="fd506-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="fd506-417">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-417">no</span></span>             | <span data-ttu-id="fd506-418">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-418">no</span></span>           |
| <span data-ttu-id="fd506-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="fd506-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="fd506-420">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-420">no</span></span>             | <span data-ttu-id="fd506-421">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-421">no</span></span>           |
| <span data-ttu-id="fd506-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="fd506-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="fd506-423">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-423">no</span></span>             | <span data-ttu-id="fd506-424">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-424">no</span></span>           |
| <span data-ttu-id="fd506-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="fd506-425">msdyn_projectid</span></span>              | <span data-ttu-id="fd506-426">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-426">yes</span></span>            | <span data-ttu-id="fd506-427">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-427">no</span></span>           |
| <span data-ttu-id="fd506-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="fd506-428">msdyn_projectidname</span></span>          | <span data-ttu-id="fd506-429">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-429">no</span></span>             | <span data-ttu-id="fd506-430">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-430">no</span></span>           |
| <span data-ttu-id="fd506-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="fd506-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="fd506-432">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-432">no</span></span>             | <span data-ttu-id="fd506-433">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-433">no</span></span>           |
| <span data-ttu-id="fd506-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="fd506-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="fd506-435">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-435">no</span></span>             | <span data-ttu-id="fd506-436">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-436">no</span></span>           |
| <span data-ttu-id="fd506-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="fd506-437">msdyn_start</span></span>                  | <span data-ttu-id="fd506-438">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-438">no</span></span>             | <span data-ttu-id="fd506-439">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-439">no</span></span>           |
| <span data-ttu-id="fd506-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="fd506-440">msdyn_taskid</span></span>                 | <span data-ttu-id="fd506-441">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-441">no</span></span>             | <span data-ttu-id="fd506-442">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-442">no</span></span>           |
| <span data-ttu-id="fd506-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="fd506-443">msdyn_taskidname</span></span>             | <span data-ttu-id="fd506-444">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-444">no</span></span>             | <span data-ttu-id="fd506-445">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-445">no</span></span>           |
| <span data-ttu-id="fd506-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="fd506-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="fd506-447">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-447">no</span></span>             | <span data-ttu-id="fd506-448">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="fd506-449">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="fd506-449">Project team member</span></span>

| <span data-ttu-id="fd506-450">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="fd506-450">**Logical name**</span></span>                                 | <span data-ttu-id="fd506-451">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="fd506-451">**Can create**</span></span> | <span data-ttu-id="fd506-452">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="fd506-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="fd506-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="fd506-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="fd506-454">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-454">no</span></span>             | <span data-ttu-id="fd506-455">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-455">no</span></span>           |
| <span data-ttu-id="fd506-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="fd506-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="fd506-457">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-457">no</span></span>             | <span data-ttu-id="fd506-458">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-458">no</span></span>           |
| <span data-ttu-id="fd506-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="fd506-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="fd506-460">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-460">no</span></span>             | <span data-ttu-id="fd506-461">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-461">no</span></span>           |
| <span data-ttu-id="fd506-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="fd506-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="fd506-463">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-463">no</span></span>             | <span data-ttu-id="fd506-464">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-464">no</span></span>           |
| <span data-ttu-id="fd506-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="fd506-465">msdyn_effort</span></span>                                     | <span data-ttu-id="fd506-466">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-466">no</span></span>             | <span data-ttu-id="fd506-467">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-467">no</span></span>           |
| <span data-ttu-id="fd506-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fd506-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="fd506-469">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-469">no</span></span>             | <span data-ttu-id="fd506-470">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-470">no</span></span>           |
| <span data-ttu-id="fd506-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="fd506-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="fd506-472">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-472">no</span></span>             | <span data-ttu-id="fd506-473">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-473">no</span></span>           |
| <span data-ttu-id="fd506-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="fd506-474">msdyn_finish</span></span>                                     | <span data-ttu-id="fd506-475">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-475">no</span></span>             | <span data-ttu-id="fd506-476">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-476">no</span></span>           |
| <span data-ttu-id="fd506-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="fd506-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="fd506-478">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-478">no</span></span>             | <span data-ttu-id="fd506-479">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-479">no</span></span>           |
| <span data-ttu-id="fd506-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="fd506-480">msdyn_hours</span></span>                                      | <span data-ttu-id="fd506-481">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-481">no</span></span>             | <span data-ttu-id="fd506-482">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-482">no</span></span>           |
| <span data-ttu-id="fd506-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="fd506-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="fd506-484">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-484">no</span></span>             | <span data-ttu-id="fd506-485">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-485">no</span></span>           |
| <span data-ttu-id="fd506-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="fd506-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="fd506-487">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-487">no</span></span>             | <span data-ttu-id="fd506-488">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-488">no</span></span>           |
| <span data-ttu-id="fd506-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="fd506-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="fd506-490">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-490">no</span></span>             | <span data-ttu-id="fd506-491">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-491">no</span></span>           |
| <span data-ttu-id="fd506-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="fd506-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="fd506-493">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-493">no</span></span>             | <span data-ttu-id="fd506-494">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-494">no</span></span>           |
| <span data-ttu-id="fd506-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="fd506-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="fd506-496">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-496">no</span></span>             | <span data-ttu-id="fd506-497">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-497">no</span></span>           |
| <span data-ttu-id="fd506-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="fd506-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="fd506-499">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-499">no</span></span>             | <span data-ttu-id="fd506-500">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-500">no</span></span>           |
| <span data-ttu-id="fd506-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="fd506-501">msdyn_start</span></span>                                      | <span data-ttu-id="fd506-502">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-502">no</span></span>             | <span data-ttu-id="fd506-503">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="fd506-504">Project</span><span class="sxs-lookup"><span data-stu-id="fd506-504">Project</span></span>

| <span data-ttu-id="fd506-505">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="fd506-505">**Logical name**</span></span>                       | <span data-ttu-id="fd506-506">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="fd506-506">**Can create**</span></span> | <span data-ttu-id="fd506-507">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="fd506-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="fd506-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="fd506-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="fd506-509">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-509">no</span></span>             | <span data-ttu-id="fd506-510">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-510">no</span></span>           |
| <span data-ttu-id="fd506-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="fd506-512">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-512">no</span></span>             | <span data-ttu-id="fd506-513">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-513">no</span></span>           |
| <span data-ttu-id="fd506-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="fd506-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="fd506-515">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-515">no</span></span>             | <span data-ttu-id="fd506-516">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-516">no</span></span>           |
| <span data-ttu-id="fd506-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="fd506-518">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-518">no</span></span>             | <span data-ttu-id="fd506-519">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-519">no</span></span>           |
| <span data-ttu-id="fd506-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="fd506-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="fd506-521">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-521">no</span></span>             | <span data-ttu-id="fd506-522">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-522">no</span></span>           |
| <span data-ttu-id="fd506-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="fd506-524">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-524">no</span></span>             | <span data-ttu-id="fd506-525">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-525">no</span></span>           |
| <span data-ttu-id="fd506-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="fd506-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="fd506-527">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-527">yes</span></span>            | <span data-ttu-id="fd506-528">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-528">no</span></span>           |
| <span data-ttu-id="fd506-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="fd506-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="fd506-530">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-530">yes</span></span>            | <span data-ttu-id="fd506-531">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-531">no</span></span>           |
| <span data-ttu-id="fd506-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="fd506-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="fd506-533">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-533">yes</span></span>            | <span data-ttu-id="fd506-534">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-534">no</span></span>           |
| <span data-ttu-id="fd506-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="fd506-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="fd506-536">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-536">no</span></span>             | <span data-ttu-id="fd506-537">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-537">no</span></span>           |
| <span data-ttu-id="fd506-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="fd506-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="fd506-539">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-539">no</span></span>             | <span data-ttu-id="fd506-540">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-540">no</span></span>           |
| <span data-ttu-id="fd506-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="fd506-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="fd506-542">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-542">no</span></span>             | <span data-ttu-id="fd506-543">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-543">no</span></span>           |
| <span data-ttu-id="fd506-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="fd506-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="fd506-545">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-545">no</span></span>             | <span data-ttu-id="fd506-546">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-546">no</span></span>           |
| <span data-ttu-id="fd506-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="fd506-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="fd506-548">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-548">no</span></span>             | <span data-ttu-id="fd506-549">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-549">no</span></span>           |
| <span data-ttu-id="fd506-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="fd506-550">msdyn_duration</span></span>                         | <span data-ttu-id="fd506-551">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-551">no</span></span>             | <span data-ttu-id="fd506-552">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-552">no</span></span>           |
| <span data-ttu-id="fd506-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="fd506-553">msdyn_effort</span></span>                           | <span data-ttu-id="fd506-554">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-554">no</span></span>             | <span data-ttu-id="fd506-555">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-555">no</span></span>           |
| <span data-ttu-id="fd506-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="fd506-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="fd506-557">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-557">no</span></span>             | <span data-ttu-id="fd506-558">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-558">no</span></span>           |
| <span data-ttu-id="fd506-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="fd506-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="fd506-560">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-560">no</span></span>             | <span data-ttu-id="fd506-561">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-561">no</span></span>           |
| <span data-ttu-id="fd506-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="fd506-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="fd506-563">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-563">no</span></span>             | <span data-ttu-id="fd506-564">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-564">no</span></span>           |
| <span data-ttu-id="fd506-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="fd506-565">msdyn_finish</span></span>                           | <span data-ttu-id="fd506-566">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-566">yes</span></span>            | <span data-ttu-id="fd506-567">ja</span><span class="sxs-lookup"><span data-stu-id="fd506-567">yes</span></span>          |
| <span data-ttu-id="fd506-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="fd506-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="fd506-569">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-569">no</span></span>             | <span data-ttu-id="fd506-570">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-570">no</span></span>           |
| <span data-ttu-id="fd506-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="fd506-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="fd506-572">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-572">no</span></span>             | <span data-ttu-id="fd506-573">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-573">no</span></span>           |
| <span data-ttu-id="fd506-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="fd506-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="fd506-575">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-575">no</span></span>             | <span data-ttu-id="fd506-576">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-576">no</span></span>           |
| <span data-ttu-id="fd506-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="fd506-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="fd506-578">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-578">no</span></span>             | <span data-ttu-id="fd506-579">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-579">no</span></span>           |
| <span data-ttu-id="fd506-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="fd506-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="fd506-581">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-581">no</span></span>             | <span data-ttu-id="fd506-582">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-582">no</span></span>           |
| <span data-ttu-id="fd506-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="fd506-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="fd506-584">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-584">no</span></span>             | <span data-ttu-id="fd506-585">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-585">no</span></span>           |
| <span data-ttu-id="fd506-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="fd506-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="fd506-587">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-587">no</span></span>             | <span data-ttu-id="fd506-588">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-588">no</span></span>           |
| <span data-ttu-id="fd506-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="fd506-590">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-590">no</span></span>             | <span data-ttu-id="fd506-591">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-591">no</span></span>           |
| <span data-ttu-id="fd506-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="fd506-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="fd506-593">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-593">no</span></span>             | <span data-ttu-id="fd506-594">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-594">no</span></span>           |
| <span data-ttu-id="fd506-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="fd506-596">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-596">no</span></span>             | <span data-ttu-id="fd506-597">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-597">no</span></span>           |
| <span data-ttu-id="fd506-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="fd506-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="fd506-599">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-599">no</span></span>             | <span data-ttu-id="fd506-600">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-600">no</span></span>           |
| <span data-ttu-id="fd506-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="fd506-602">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-602">no</span></span>             | <span data-ttu-id="fd506-603">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-603">no</span></span>           |
| <span data-ttu-id="fd506-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="fd506-604">msdyn_progress</span></span>                         | <span data-ttu-id="fd506-605">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-605">no</span></span>             | <span data-ttu-id="fd506-606">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-606">no</span></span>           |
| <span data-ttu-id="fd506-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="fd506-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="fd506-608">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-608">no</span></span>             | <span data-ttu-id="fd506-609">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-609">no</span></span>           |
| <span data-ttu-id="fd506-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="fd506-611">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-611">no</span></span>             | <span data-ttu-id="fd506-612">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-612">no</span></span>           |
| <span data-ttu-id="fd506-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="fd506-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="fd506-614">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-614">no</span></span>             | <span data-ttu-id="fd506-615">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-615">no</span></span>           |
| <span data-ttu-id="fd506-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="fd506-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="fd506-617">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-617">no</span></span>             | <span data-ttu-id="fd506-618">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-618">no</span></span>           |
| <span data-ttu-id="fd506-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="fd506-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="fd506-620">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-620">no</span></span>             | <span data-ttu-id="fd506-621">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-621">no</span></span>           |
| <span data-ttu-id="fd506-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="fd506-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="fd506-623">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-623">no</span></span>             | <span data-ttu-id="fd506-624">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-624">no</span></span>           |
| <span data-ttu-id="fd506-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="fd506-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="fd506-626">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-626">no</span></span>             | <span data-ttu-id="fd506-627">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-627">no</span></span>           |
| <span data-ttu-id="fd506-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="fd506-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="fd506-629">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-629">no</span></span>             | <span data-ttu-id="fd506-630">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-630">no</span></span>           |
| <span data-ttu-id="fd506-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="fd506-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="fd506-632">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-632">no</span></span>             | <span data-ttu-id="fd506-633">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-633">no</span></span>           |
| <span data-ttu-id="fd506-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="fd506-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="fd506-635">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-635">no</span></span>             | <span data-ttu-id="fd506-636">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-636">no</span></span>           |
| <span data-ttu-id="fd506-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="fd506-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="fd506-638">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-638">no</span></span>             | <span data-ttu-id="fd506-639">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-639">no</span></span>           |
| <span data-ttu-id="fd506-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="fd506-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="fd506-641">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-641">no</span></span>             | <span data-ttu-id="fd506-642">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-642">no</span></span>           |
| <span data-ttu-id="fd506-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="fd506-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="fd506-644">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-644">no</span></span>             | <span data-ttu-id="fd506-645">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-645">no</span></span>           |
| <span data-ttu-id="fd506-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="fd506-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="fd506-647">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-647">no</span></span>             | <span data-ttu-id="fd506-648">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-648">no</span></span>           |
| <span data-ttu-id="fd506-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="fd506-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="fd506-650">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-650">no</span></span>             | <span data-ttu-id="fd506-651">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-651">no</span></span>           |
| <span data-ttu-id="fd506-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="fd506-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="fd506-653">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-653">no</span></span>             | <span data-ttu-id="fd506-654">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-654">no</span></span>           |
| <span data-ttu-id="fd506-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="fd506-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="fd506-656">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-656">no</span></span>             | <span data-ttu-id="fd506-657">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-657">no</span></span>           |
| <span data-ttu-id="fd506-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="fd506-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="fd506-659">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-659">no</span></span>             | <span data-ttu-id="fd506-660">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-660">no</span></span>           |
| <span data-ttu-id="fd506-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="fd506-662">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-662">no</span></span>             | <span data-ttu-id="fd506-663">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-663">no</span></span>           |
| <span data-ttu-id="fd506-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="fd506-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="fd506-665">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-665">no</span></span>             | <span data-ttu-id="fd506-666">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-666">no</span></span>           |
| <span data-ttu-id="fd506-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="fd506-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="fd506-668">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-668">no</span></span>             | <span data-ttu-id="fd506-669">nej</span><span class="sxs-lookup"><span data-stu-id="fd506-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="fd506-670">Begränsningar och kända problem</span><span class="sxs-lookup"><span data-stu-id="fd506-670">Limitations and known issues</span></span>
<span data-ttu-id="fd506-671">Följande är en lista med begränsningar och kända problem:</span><span class="sxs-lookup"><span data-stu-id="fd506-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="fd506-672">API:er för projektscheman kan endast användas av **användare med Microsofts projektlicens**.</span><span class="sxs-lookup"><span data-stu-id="fd506-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="fd506-673">De kan inte användas av:</span><span class="sxs-lookup"><span data-stu-id="fd506-673">They can't be used by:</span></span>
    - <span data-ttu-id="fd506-674">Programanvändare</span><span class="sxs-lookup"><span data-stu-id="fd506-674">Application users</span></span>
    - <span data-ttu-id="fd506-675">Systemanvändare</span><span class="sxs-lookup"><span data-stu-id="fd506-675">System users</span></span>
    - <span data-ttu-id="fd506-676">Integrationsanvändare</span><span class="sxs-lookup"><span data-stu-id="fd506-676">Integration users</span></span>
    - <span data-ttu-id="fd506-677">Andra användare som inte har den licens som krävs</span><span class="sxs-lookup"><span data-stu-id="fd506-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="fd506-678">Varje **OperationSet** kan endast ha högst 100 åtgärder.</span><span class="sxs-lookup"><span data-stu-id="fd506-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="fd506-679">Varje användare kan bara ha högst 10 öppna **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="fd506-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="fd506-680">Project Operations stöder för närvarande maximalt 500 totala uppgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="fd506-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="fd506-681">**OperationSet** felstatus och felloggar är för närvarande inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="fd506-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="fd506-682">Gränser för projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="fd506-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="fd506-683">Felhantering</span><span class="sxs-lookup"><span data-stu-id="fd506-683">Error handling</span></span>

   - <span data-ttu-id="fd506-684">Om du vill granska fel som uppstått från Åtgärdsuppsättningar går du till **Inställningar** \> **Schemalägg integration** \> **Åtgärdsuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="fd506-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="fd506-685">Om du vill granska fel som genererats från projektplaneringstjänsten, gå till **Inställningar** \> **Schemaläggningsintegrering** \> **PSS felloggar**.</span><span class="sxs-lookup"><span data-stu-id="fd506-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="fd506-686">Exempelscenario</span><span class="sxs-lookup"><span data-stu-id="fd506-686">Sample scenario</span></span>

<span data-ttu-id="fd506-687">I det här scenariot skapar du ett projekt, en teammedlem, fyra uppgifter och två resurstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="fd506-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="fd506-688">Nu ska du uppdatera en uppgift, uppdatera projektet, ta bort en uppgift, ta bort en resurstilldelning och skapa ett aktivitetsberoende.</span><span class="sxs-lookup"><span data-stu-id="fd506-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="fd506-689">Ytterligare exempel</span><span class="sxs-lookup"><span data-stu-id="fd506-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
