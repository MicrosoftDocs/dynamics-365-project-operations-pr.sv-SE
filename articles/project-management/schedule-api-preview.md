---
title: Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter
description: Detta ämne innehåller information och exempel för användning av schemaläggnings-API:er.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950826"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="4165a-103">Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="4165a-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="4165a-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="4165a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="4165a-105">Vissa eller alla funktioner som anges i det här ämnet är tillgängliga som en del av en förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="4165a-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="4165a-106">Innehållet och funktionerna kan komma att ändras.</span><span class="sxs-lookup"><span data-stu-id="4165a-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="4165a-107">Schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="4165a-107">Scheduling entities</span></span>

<span data-ttu-id="4165a-108">Schemalägg API:er så att du kan skapa, uppdatera och ta bort åtgärder med **schemaläggningsentiteter**.</span><span class="sxs-lookup"><span data-stu-id="4165a-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="4165a-109">Dessa entiteter hanteras med schemaläggningsmotorn i Projekt för webben.</span><span class="sxs-lookup"><span data-stu-id="4165a-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="4165a-110">Skapa, uppdatera och ta bort operationer med **Schemaläggningsentiteter** begränsades i tidigare versioner av Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4165a-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="4165a-111">I följande tabell visas en fullständig lista över **Schemaläggningsentiteterna**.</span><span class="sxs-lookup"><span data-stu-id="4165a-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="4165a-112">Entitetsnamn</span><span class="sxs-lookup"><span data-stu-id="4165a-112">Entity name</span></span>  | <span data-ttu-id="4165a-113">Entitetens logiska namn</span><span class="sxs-lookup"><span data-stu-id="4165a-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="4165a-114">Project</span><span class="sxs-lookup"><span data-stu-id="4165a-114">Project</span></span> | <span data-ttu-id="4165a-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="4165a-115">msdyn_project</span></span> |
| <span data-ttu-id="4165a-116">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4165a-116">Project Task</span></span>  | <span data-ttu-id="4165a-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="4165a-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="4165a-118">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4165a-118">Project Task Dependency</span></span>  | <span data-ttu-id="4165a-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="4165a-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="4165a-120">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="4165a-120">Resource Assignment</span></span> | <span data-ttu-id="4165a-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="4165a-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="4165a-122">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="4165a-122">Project Bucket</span></span>  | <span data-ttu-id="4165a-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="4165a-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="4165a-124">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="4165a-124">Project Team Member</span></span> | <span data-ttu-id="4165a-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="4165a-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="4165a-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="4165a-126">OperationSet</span></span>

<span data-ttu-id="4165a-127">OperationSet är ett enhetsmönster som kan användas när flera schemapåverkande förfrågningar måste bearbetas inom en transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4165a-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="4165a-128">Schemaläggning-API:er</span><span class="sxs-lookup"><span data-stu-id="4165a-128">Schedule APIs</span></span>

<span data-ttu-id="4165a-129">Följande är en lista med aktuella schemaläggning-API:er.</span><span class="sxs-lookup"><span data-stu-id="4165a-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="4165a-130">**msdyn_CreateProjectV1**: Detta API kan användas för att skapa ett projekt.</span><span class="sxs-lookup"><span data-stu-id="4165a-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="4165a-131">Projekt och standardprojektgrupp skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="4165a-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="4165a-132">**msdyn_CreateTeamMemberV1**: Detta API kan användas för att skapa en projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="4165a-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="4165a-133">Teammedlemsposten skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="4165a-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="4165a-134">**msdyn_CreateOperationSetV1**: Detta API kan användas för att schemalägga flera förfrågningar som måste utföras inom en transaktionen.</span><span class="sxs-lookup"><span data-stu-id="4165a-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="4165a-135">**msdyn_PSSCreateV1**: Det här API:et kan användas för att skapa en entitet.</span><span class="sxs-lookup"><span data-stu-id="4165a-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="4165a-136">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden skapa.</span><span class="sxs-lookup"><span data-stu-id="4165a-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="4165a-137">**msdyn_PSSUpdateV1**: Det här API:et kan användas för att uppdatera en entitet.</span><span class="sxs-lookup"><span data-stu-id="4165a-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="4165a-138">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden uppdatera.</span><span class="sxs-lookup"><span data-stu-id="4165a-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="4165a-139">**msdyn_PSSDeleteV1**: Det här API:et kan användas för att ta bort en entitet.</span><span class="sxs-lookup"><span data-stu-id="4165a-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="4165a-140">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden ta bort.</span><span class="sxs-lookup"><span data-stu-id="4165a-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="4165a-141">**msdyn_ExecuteOperationSetV1**: Detta API används för att köra alla åtgärder inom den angivna åtgärdsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="4165a-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="4165a-142">Använda schemaläggnings-API:er med OperationSet</span><span class="sxs-lookup"><span data-stu-id="4165a-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="4165a-143">Eftersom poster med både **CreateProjectV1** och **CreateTeamMemberV1** skapas direkt kan dessa API:er inte användas direkt i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="4165a-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="4165a-144">Men du kan använda API för att skapa nödvändiga poster, skapa en **OperationSet** och sedan använda dessa förskapade poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="4165a-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="4165a-145">Åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="4165a-145">Supported operations</span></span>

| <span data-ttu-id="4165a-146">Schemaläggningsentitet</span><span class="sxs-lookup"><span data-stu-id="4165a-146">Scheduling entity</span></span> | <span data-ttu-id="4165a-147">Skapa</span><span class="sxs-lookup"><span data-stu-id="4165a-147">Create</span></span> | <span data-ttu-id="4165a-148">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="4165a-148">Update</span></span> | <span data-ttu-id="4165a-149">Delete</span><span class="sxs-lookup"><span data-stu-id="4165a-149">Delete</span></span> | <span data-ttu-id="4165a-150">Viktigt!</span><span class="sxs-lookup"><span data-stu-id="4165a-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="4165a-151">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4165a-151">Project task</span></span> | <span data-ttu-id="4165a-152">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-152">Yes</span></span> | <span data-ttu-id="4165a-153">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-153">Yes</span></span> | <span data-ttu-id="4165a-154">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-154">Yes</span></span> | <span data-ttu-id="4165a-155">Nej</span><span class="sxs-lookup"><span data-stu-id="4165a-155">None</span></span> |
| <span data-ttu-id="4165a-156">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4165a-156">Project task dependency</span></span> | <span data-ttu-id="4165a-157">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-157">Yes</span></span> | <span data-ttu-id="4165a-158">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-158">Yes</span></span> | | <span data-ttu-id="4165a-159">Poster för projektuppgiftsberoende uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="4165a-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="4165a-160">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="4165a-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="4165a-161">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="4165a-161">Resource assignment</span></span> | <span data-ttu-id="4165a-162">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-162">Yes</span></span> | <span data-ttu-id="4165a-163">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-163">Yes</span></span> | | <span data-ttu-id="4165a-164">Operationer med följande fält stöds inte: **BookableResourceID**, **Insats**, **EffortCompleted**, **EffortRemaining** och **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="4165a-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="4165a-165">Resurstilldelningsposter uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="4165a-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="4165a-166">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="4165a-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="4165a-167">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="4165a-167">Project bucket</span></span> | <span data-ttu-id="4165a-168">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="4165a-168">N/A</span></span> | <span data-ttu-id="4165a-169">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="4165a-169">N/A</span></span> | <span data-ttu-id="4165a-170">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="4165a-170">N/A</span></span> | <span data-ttu-id="4165a-171">Standardgruppen skapas för att använda API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="4165a-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="4165a-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="4165a-172">Project team member</span></span> | <span data-ttu-id="4165a-173">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-173">Yes</span></span> | <span data-ttu-id="4165a-174">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-174">Yes</span></span> | <span data-ttu-id="4165a-175">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-175">Yes</span></span> | <span data-ttu-id="4165a-176">För att skapa operation, använda API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="4165a-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="4165a-177">Project</span><span class="sxs-lookup"><span data-stu-id="4165a-177">Project</span></span> | <span data-ttu-id="4165a-178">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-178">Yes</span></span> | <span data-ttu-id="4165a-179">Ja</span><span class="sxs-lookup"><span data-stu-id="4165a-179">Yes</span></span> | <span data-ttu-id="4165a-180">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="4165a-180">N/A</span></span> | <span data-ttu-id="4165a-181">Operationer med följande fält stöds inte: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Insats**, **EffortCompleted**, **EffortRemaining**, **Förlopp**, **Slutför**, **TaskEarliestStart** och **Varaktighet**.</span><span class="sxs-lookup"><span data-stu-id="4165a-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="4165a-182">Dessa API:er kan anropas med entitetsobjekt som innehåller anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="4165a-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="4165a-183">ID-egenskapen är valfri.</span><span class="sxs-lookup"><span data-stu-id="4165a-183">The ID property is optional.</span></span> <span data-ttu-id="4165a-184">Om det finns ett undantag försöker systemet använda det och ett undantag om det inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="4165a-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="4165a-185">Om den inte finns genererar systemet den.</span><span class="sxs-lookup"><span data-stu-id="4165a-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="4165a-186">Begränsade fält</span><span class="sxs-lookup"><span data-stu-id="4165a-186">Restricted fields</span></span>

<span data-ttu-id="4165a-187">I följande tabeller definieras fälten som är begränsade från **Skapa** och **Redigera.**</span><span class="sxs-lookup"><span data-stu-id="4165a-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="4165a-188">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4165a-188">Project task</span></span>

| <span data-ttu-id="4165a-189">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="4165a-189">**Logical name**</span></span>                       | <span data-ttu-id="4165a-190">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="4165a-190">**Can create**</span></span> | <span data-ttu-id="4165a-191">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="4165a-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="4165a-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="4165a-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="4165a-193">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-193">no</span></span>             | <span data-ttu-id="4165a-194">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-194">no</span></span>               |
| <span data-ttu-id="4165a-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="4165a-196">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-196">no</span></span>             | <span data-ttu-id="4165a-197">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-197">no</span></span>               |
| <span data-ttu-id="4165a-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="4165a-198">msdyn_actualend</span></span>                        | <span data-ttu-id="4165a-199">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-199">no</span></span>             | <span data-ttu-id="4165a-200">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-200">no</span></span>               |
| <span data-ttu-id="4165a-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="4165a-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="4165a-202">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-202">no</span></span>             | <span data-ttu-id="4165a-203">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-203">no</span></span>               |
| <span data-ttu-id="4165a-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="4165a-205">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-205">no</span></span>             | <span data-ttu-id="4165a-206">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-206">no</span></span>               |
| <span data-ttu-id="4165a-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="4165a-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="4165a-208">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-208">no</span></span>             | <span data-ttu-id="4165a-209">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-209">no</span></span>               |
| <span data-ttu-id="4165a-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="4165a-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="4165a-211">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-211">no</span></span>             | <span data-ttu-id="4165a-212">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-212">no</span></span>               |
| <span data-ttu-id="4165a-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="4165a-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="4165a-214">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-214">no</span></span>             | <span data-ttu-id="4165a-215">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-215">no</span></span>               |
| <span data-ttu-id="4165a-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="4165a-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="4165a-217">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-217">no</span></span>             | <span data-ttu-id="4165a-218">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-218">no</span></span>               |
| <span data-ttu-id="4165a-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4165a-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="4165a-220">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-220">no</span></span>             | <span data-ttu-id="4165a-221">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-221">no</span></span>               |
| <span data-ttu-id="4165a-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4165a-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="4165a-223">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-223">no</span></span>             | <span data-ttu-id="4165a-224">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-224">no</span></span>               |
| <span data-ttu-id="4165a-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="4165a-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="4165a-226">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-226">no</span></span>             | <span data-ttu-id="4165a-227">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-227">no</span></span>               |
| <span data-ttu-id="4165a-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="4165a-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="4165a-229">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-229">no</span></span>             | <span data-ttu-id="4165a-230">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-230">no</span></span>               |
| <span data-ttu-id="4165a-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="4165a-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="4165a-232">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-232">no</span></span>             | <span data-ttu-id="4165a-233">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-233">no</span></span>               |
| <span data-ttu-id="4165a-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="4165a-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="4165a-235">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-235">no</span></span>             | <span data-ttu-id="4165a-236">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-236">no</span></span>               |
| <span data-ttu-id="4165a-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="4165a-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="4165a-238">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-238">no</span></span>             | <span data-ttu-id="4165a-239">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-239">no</span></span>               |
| <span data-ttu-id="4165a-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="4165a-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="4165a-241">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-241">no</span></span>             | <span data-ttu-id="4165a-242">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-242">no</span></span>               |
| <span data-ttu-id="4165a-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="4165a-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="4165a-244">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-244">no</span></span>             | <span data-ttu-id="4165a-245">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-245">no</span></span>               |
| <span data-ttu-id="4165a-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="4165a-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="4165a-247">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-247">no</span></span>             | <span data-ttu-id="4165a-248">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-248">no</span></span>               |
| <span data-ttu-id="4165a-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="4165a-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="4165a-250">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-250">no</span></span>             | <span data-ttu-id="4165a-251">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-251">no</span></span>               |
| <span data-ttu-id="4165a-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4165a-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="4165a-253">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-253">no</span></span>             | <span data-ttu-id="4165a-254">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-254">no</span></span>               |
| <span data-ttu-id="4165a-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="4165a-256">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-256">no</span></span>             | <span data-ttu-id="4165a-257">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-257">no</span></span>               |
| <span data-ttu-id="4165a-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4165a-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="4165a-259">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-259">no</span></span>             | <span data-ttu-id="4165a-260">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-260">no</span></span>               |
| <span data-ttu-id="4165a-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="4165a-262">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-262">no</span></span>             | <span data-ttu-id="4165a-263">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-263">no</span></span>               |
| <span data-ttu-id="4165a-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="4165a-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="4165a-265">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-265">no</span></span>             | <span data-ttu-id="4165a-266">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-266">no</span></span>               |
| <span data-ttu-id="4165a-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="4165a-267">msdyn_progress</span></span>                         | <span data-ttu-id="4165a-268">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-268">no</span></span>             | <span data-ttu-id="4165a-269">nej (ja för P4W)</span><span class="sxs-lookup"><span data-stu-id="4165a-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="4165a-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4165a-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="4165a-271">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-271">no</span></span>             | <span data-ttu-id="4165a-272">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-272">no</span></span>               |
| <span data-ttu-id="4165a-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="4165a-274">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-274">no</span></span>             | <span data-ttu-id="4165a-275">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-275">no</span></span>               |
| <span data-ttu-id="4165a-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4165a-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="4165a-277">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-277">no</span></span>             | <span data-ttu-id="4165a-278">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-278">no</span></span>               |
| <span data-ttu-id="4165a-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="4165a-280">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-280">no</span></span>             | <span data-ttu-id="4165a-281">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-281">no</span></span>               |
| <span data-ttu-id="4165a-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="4165a-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="4165a-283">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-283">no</span></span>             | <span data-ttu-id="4165a-284">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-284">no</span></span>               |
| <span data-ttu-id="4165a-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4165a-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="4165a-286">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-286">no</span></span>             | <span data-ttu-id="4165a-287">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-287">no</span></span>               |
| <span data-ttu-id="4165a-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="4165a-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="4165a-289">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-289">no</span></span>             | <span data-ttu-id="4165a-290">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-290">no</span></span>               |
| <span data-ttu-id="4165a-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="4165a-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="4165a-292">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-292">no</span></span>             | <span data-ttu-id="4165a-293">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-293">no</span></span>               |
| <span data-ttu-id="4165a-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="4165a-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="4165a-295">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-295">no</span></span>             | <span data-ttu-id="4165a-296">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-296">no</span></span>               |
| <span data-ttu-id="4165a-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="4165a-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="4165a-298">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-298">no</span></span>             | <span data-ttu-id="4165a-299">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-299">no</span></span>               |
| <span data-ttu-id="4165a-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4165a-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="4165a-301">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-301">no</span></span>             | <span data-ttu-id="4165a-302">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-302">no</span></span>               |
| <span data-ttu-id="4165a-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="4165a-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="4165a-304">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-304">no</span></span>             | <span data-ttu-id="4165a-305">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-305">no</span></span>               |
| <span data-ttu-id="4165a-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="4165a-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="4165a-307">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-307">no</span></span>             | <span data-ttu-id="4165a-308">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-308">no</span></span>               |
| <span data-ttu-id="4165a-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="4165a-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="4165a-310">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-310">no</span></span>             | <span data-ttu-id="4165a-311">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-311">no</span></span>               |
| <span data-ttu-id="4165a-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="4165a-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="4165a-313">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-313">no</span></span>             | <span data-ttu-id="4165a-314">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-314">no</span></span>               |
| <span data-ttu-id="4165a-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="4165a-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="4165a-316">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-316">no</span></span>             | <span data-ttu-id="4165a-317">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-317">no</span></span>               |
| <span data-ttu-id="4165a-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="4165a-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="4165a-319">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-319">no</span></span>             | <span data-ttu-id="4165a-320">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-320">no</span></span>               |
| <span data-ttu-id="4165a-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="4165a-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="4165a-322">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-322">no</span></span>             | <span data-ttu-id="4165a-323">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-323">no</span></span>               |
| <span data-ttu-id="4165a-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="4165a-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="4165a-325">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-325">no</span></span>             | <span data-ttu-id="4165a-326">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-326">no</span></span>               |
| <span data-ttu-id="4165a-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="4165a-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="4165a-328">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-328">no</span></span>             | <span data-ttu-id="4165a-329">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-329">no</span></span>               |
| <span data-ttu-id="4165a-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="4165a-330">msdyn_summary</span></span>                          | <span data-ttu-id="4165a-331">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-331">no</span></span>             | <span data-ttu-id="4165a-332">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-332">no</span></span>               |
| <span data-ttu-id="4165a-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="4165a-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="4165a-334">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-334">no</span></span>             | <span data-ttu-id="4165a-335">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-335">no</span></span>               |
| <span data-ttu-id="4165a-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="4165a-337">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-337">no</span></span>             | <span data-ttu-id="4165a-338">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="4165a-339">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4165a-339">Project task dependency</span></span>

| <span data-ttu-id="4165a-340">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="4165a-340">**Logical name**</span></span>              | <span data-ttu-id="4165a-341">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="4165a-341">**Can create**</span></span> | <span data-ttu-id="4165a-342">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="4165a-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="4165a-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="4165a-343">msdyn_linktype</span></span>                | <span data-ttu-id="4165a-344">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-344">no</span></span>             | <span data-ttu-id="4165a-345">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-345">no</span></span>           |
| <span data-ttu-id="4165a-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="4165a-346">msdyn_linktypename</span></span>            | <span data-ttu-id="4165a-347">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-347">no</span></span>             | <span data-ttu-id="4165a-348">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-348">no</span></span>           |
| <span data-ttu-id="4165a-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="4165a-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="4165a-350">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-350">yes</span></span>            | <span data-ttu-id="4165a-351">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-351">no</span></span>           |
| <span data-ttu-id="4165a-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="4165a-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="4165a-353">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-353">yes</span></span>            | <span data-ttu-id="4165a-354">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-354">no</span></span>           |
| <span data-ttu-id="4165a-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="4165a-355">msdyn_project</span></span>                 | <span data-ttu-id="4165a-356">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-356">yes</span></span>            | <span data-ttu-id="4165a-357">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-357">no</span></span>           |
| <span data-ttu-id="4165a-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="4165a-358">msdyn_projectname</span></span>             | <span data-ttu-id="4165a-359">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-359">yes</span></span>            | <span data-ttu-id="4165a-360">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-360">no</span></span>           |
| <span data-ttu-id="4165a-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="4165a-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="4165a-362">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-362">yes</span></span>            | <span data-ttu-id="4165a-363">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-363">no</span></span>           |
| <span data-ttu-id="4165a-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="4165a-364">msdyn_successortask</span></span>           | <span data-ttu-id="4165a-365">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-365">yes</span></span>            | <span data-ttu-id="4165a-366">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-366">no</span></span>           |
| <span data-ttu-id="4165a-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="4165a-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="4165a-368">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-368">yes</span></span>            | <span data-ttu-id="4165a-369">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="4165a-370">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="4165a-370">Resource assignment</span></span>

| <span data-ttu-id="4165a-371">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="4165a-371">**Logical name**</span></span>             | <span data-ttu-id="4165a-372">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="4165a-372">**Can create**</span></span> | <span data-ttu-id="4165a-373">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="4165a-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="4165a-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="4165a-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="4165a-375">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-375">yes</span></span>            | <span data-ttu-id="4165a-376">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-376">no</span></span>           |
| <span data-ttu-id="4165a-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="4165a-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="4165a-378">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-378">yes</span></span>            | <span data-ttu-id="4165a-379">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-379">no</span></span>           |
| <span data-ttu-id="4165a-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="4165a-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="4165a-381">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-381">no</span></span>             | <span data-ttu-id="4165a-382">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-382">no</span></span>           |
| <span data-ttu-id="4165a-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="4165a-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="4165a-384">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-384">no</span></span>             | <span data-ttu-id="4165a-385">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-385">no</span></span>           |
| <span data-ttu-id="4165a-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="4165a-386">msdyn_committype</span></span>             | <span data-ttu-id="4165a-387">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-387">no</span></span>             | <span data-ttu-id="4165a-388">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-388">no</span></span>           |
| <span data-ttu-id="4165a-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="4165a-389">msdyn_committypename</span></span>         | <span data-ttu-id="4165a-390">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-390">no</span></span>             | <span data-ttu-id="4165a-391">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-391">no</span></span>           |
| <span data-ttu-id="4165a-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4165a-392">msdyn_effort</span></span>                 | <span data-ttu-id="4165a-393">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-393">no</span></span>             | <span data-ttu-id="4165a-394">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-394">no</span></span>           |
| <span data-ttu-id="4165a-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4165a-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="4165a-396">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-396">no</span></span>             | <span data-ttu-id="4165a-397">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-397">no</span></span>           |
| <span data-ttu-id="4165a-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4165a-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="4165a-399">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-399">no</span></span>             | <span data-ttu-id="4165a-400">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-400">no</span></span>           |
| <span data-ttu-id="4165a-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4165a-401">msdyn_finish</span></span>                 | <span data-ttu-id="4165a-402">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-402">no</span></span>             | <span data-ttu-id="4165a-403">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-403">no</span></span>           |
| <span data-ttu-id="4165a-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4165a-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="4165a-405">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-405">no</span></span>             | <span data-ttu-id="4165a-406">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-406">no</span></span>           |
| <span data-ttu-id="4165a-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="4165a-408">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-408">no</span></span>             | <span data-ttu-id="4165a-409">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-409">no</span></span>           |
| <span data-ttu-id="4165a-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="4165a-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="4165a-411">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-411">no</span></span>             | <span data-ttu-id="4165a-412">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-412">no</span></span>           |
| <span data-ttu-id="4165a-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4165a-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="4165a-414">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-414">no</span></span>             | <span data-ttu-id="4165a-415">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-415">no</span></span>           |
| <span data-ttu-id="4165a-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="4165a-417">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-417">no</span></span>             | <span data-ttu-id="4165a-418">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-418">no</span></span>           |
| <span data-ttu-id="4165a-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="4165a-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="4165a-420">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-420">no</span></span>             | <span data-ttu-id="4165a-421">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-421">no</span></span>           |
| <span data-ttu-id="4165a-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="4165a-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="4165a-423">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-423">no</span></span>             | <span data-ttu-id="4165a-424">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-424">no</span></span>           |
| <span data-ttu-id="4165a-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="4165a-425">msdyn_projectid</span></span>              | <span data-ttu-id="4165a-426">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-426">yes</span></span>            | <span data-ttu-id="4165a-427">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-427">no</span></span>           |
| <span data-ttu-id="4165a-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="4165a-428">msdyn_projectidname</span></span>          | <span data-ttu-id="4165a-429">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-429">no</span></span>             | <span data-ttu-id="4165a-430">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-430">no</span></span>           |
| <span data-ttu-id="4165a-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="4165a-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="4165a-432">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-432">no</span></span>             | <span data-ttu-id="4165a-433">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-433">no</span></span>           |
| <span data-ttu-id="4165a-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="4165a-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="4165a-435">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-435">no</span></span>             | <span data-ttu-id="4165a-436">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-436">no</span></span>           |
| <span data-ttu-id="4165a-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="4165a-437">msdyn_start</span></span>                  | <span data-ttu-id="4165a-438">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-438">no</span></span>             | <span data-ttu-id="4165a-439">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-439">no</span></span>           |
| <span data-ttu-id="4165a-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="4165a-440">msdyn_taskid</span></span>                 | <span data-ttu-id="4165a-441">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-441">no</span></span>             | <span data-ttu-id="4165a-442">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-442">no</span></span>           |
| <span data-ttu-id="4165a-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="4165a-443">msdyn_taskidname</span></span>             | <span data-ttu-id="4165a-444">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-444">no</span></span>             | <span data-ttu-id="4165a-445">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-445">no</span></span>           |
| <span data-ttu-id="4165a-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="4165a-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="4165a-447">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-447">no</span></span>             | <span data-ttu-id="4165a-448">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="4165a-449">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="4165a-449">Project team member</span></span>

| <span data-ttu-id="4165a-450">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="4165a-450">**Logical name**</span></span>                                 | <span data-ttu-id="4165a-451">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="4165a-451">**Can create**</span></span> | <span data-ttu-id="4165a-452">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="4165a-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="4165a-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="4165a-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="4165a-454">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-454">no</span></span>             | <span data-ttu-id="4165a-455">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-455">no</span></span>           |
| <span data-ttu-id="4165a-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="4165a-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="4165a-457">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-457">no</span></span>             | <span data-ttu-id="4165a-458">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-458">no</span></span>           |
| <span data-ttu-id="4165a-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="4165a-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="4165a-460">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-460">no</span></span>             | <span data-ttu-id="4165a-461">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-461">no</span></span>           |
| <span data-ttu-id="4165a-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="4165a-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="4165a-463">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-463">no</span></span>             | <span data-ttu-id="4165a-464">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-464">no</span></span>           |
| <span data-ttu-id="4165a-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4165a-465">msdyn_effort</span></span>                                     | <span data-ttu-id="4165a-466">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-466">no</span></span>             | <span data-ttu-id="4165a-467">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-467">no</span></span>           |
| <span data-ttu-id="4165a-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4165a-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="4165a-469">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-469">no</span></span>             | <span data-ttu-id="4165a-470">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-470">no</span></span>           |
| <span data-ttu-id="4165a-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4165a-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="4165a-472">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-472">no</span></span>             | <span data-ttu-id="4165a-473">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-473">no</span></span>           |
| <span data-ttu-id="4165a-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4165a-474">msdyn_finish</span></span>                                     | <span data-ttu-id="4165a-475">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-475">no</span></span>             | <span data-ttu-id="4165a-476">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-476">no</span></span>           |
| <span data-ttu-id="4165a-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="4165a-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="4165a-478">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-478">no</span></span>             | <span data-ttu-id="4165a-479">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-479">no</span></span>           |
| <span data-ttu-id="4165a-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="4165a-480">msdyn_hours</span></span>                                      | <span data-ttu-id="4165a-481">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-481">no</span></span>             | <span data-ttu-id="4165a-482">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-482">no</span></span>           |
| <span data-ttu-id="4165a-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="4165a-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="4165a-484">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-484">no</span></span>             | <span data-ttu-id="4165a-485">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-485">no</span></span>           |
| <span data-ttu-id="4165a-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="4165a-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="4165a-487">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-487">no</span></span>             | <span data-ttu-id="4165a-488">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-488">no</span></span>           |
| <span data-ttu-id="4165a-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="4165a-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="4165a-490">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-490">no</span></span>             | <span data-ttu-id="4165a-491">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-491">no</span></span>           |
| <span data-ttu-id="4165a-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="4165a-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="4165a-493">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-493">no</span></span>             | <span data-ttu-id="4165a-494">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-494">no</span></span>           |
| <span data-ttu-id="4165a-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="4165a-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="4165a-496">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-496">no</span></span>             | <span data-ttu-id="4165a-497">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-497">no</span></span>           |
| <span data-ttu-id="4165a-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="4165a-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="4165a-499">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-499">no</span></span>             | <span data-ttu-id="4165a-500">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-500">no</span></span>           |
| <span data-ttu-id="4165a-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="4165a-501">msdyn_start</span></span>                                      | <span data-ttu-id="4165a-502">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-502">no</span></span>             | <span data-ttu-id="4165a-503">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="4165a-504">Project</span><span class="sxs-lookup"><span data-stu-id="4165a-504">Project</span></span>

| <span data-ttu-id="4165a-505">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="4165a-505">**Logical name**</span></span>                       | <span data-ttu-id="4165a-506">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="4165a-506">**Can create**</span></span> | <span data-ttu-id="4165a-507">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="4165a-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="4165a-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="4165a-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="4165a-509">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-509">no</span></span>             | <span data-ttu-id="4165a-510">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-510">no</span></span>           |
| <span data-ttu-id="4165a-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="4165a-512">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-512">no</span></span>             | <span data-ttu-id="4165a-513">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-513">no</span></span>           |
| <span data-ttu-id="4165a-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="4165a-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="4165a-515">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-515">no</span></span>             | <span data-ttu-id="4165a-516">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-516">no</span></span>           |
| <span data-ttu-id="4165a-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="4165a-518">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-518">no</span></span>             | <span data-ttu-id="4165a-519">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-519">no</span></span>           |
| <span data-ttu-id="4165a-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="4165a-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="4165a-521">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-521">no</span></span>             | <span data-ttu-id="4165a-522">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-522">no</span></span>           |
| <span data-ttu-id="4165a-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="4165a-524">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-524">no</span></span>             | <span data-ttu-id="4165a-525">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-525">no</span></span>           |
| <span data-ttu-id="4165a-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="4165a-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="4165a-527">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-527">yes</span></span>            | <span data-ttu-id="4165a-528">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-528">no</span></span>           |
| <span data-ttu-id="4165a-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="4165a-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="4165a-530">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-530">yes</span></span>            | <span data-ttu-id="4165a-531">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-531">no</span></span>           |
| <span data-ttu-id="4165a-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="4165a-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="4165a-533">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-533">yes</span></span>            | <span data-ttu-id="4165a-534">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-534">no</span></span>           |
| <span data-ttu-id="4165a-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="4165a-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="4165a-536">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-536">no</span></span>             | <span data-ttu-id="4165a-537">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-537">no</span></span>           |
| <span data-ttu-id="4165a-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4165a-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="4165a-539">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-539">no</span></span>             | <span data-ttu-id="4165a-540">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-540">no</span></span>           |
| <span data-ttu-id="4165a-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="4165a-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="4165a-542">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-542">no</span></span>             | <span data-ttu-id="4165a-543">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-543">no</span></span>           |
| <span data-ttu-id="4165a-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="4165a-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="4165a-545">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-545">no</span></span>             | <span data-ttu-id="4165a-546">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-546">no</span></span>           |
| <span data-ttu-id="4165a-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="4165a-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="4165a-548">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-548">no</span></span>             | <span data-ttu-id="4165a-549">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-549">no</span></span>           |
| <span data-ttu-id="4165a-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="4165a-550">msdyn_duration</span></span>                         | <span data-ttu-id="4165a-551">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-551">no</span></span>             | <span data-ttu-id="4165a-552">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-552">no</span></span>           |
| <span data-ttu-id="4165a-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4165a-553">msdyn_effort</span></span>                           | <span data-ttu-id="4165a-554">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-554">no</span></span>             | <span data-ttu-id="4165a-555">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-555">no</span></span>           |
| <span data-ttu-id="4165a-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4165a-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="4165a-557">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-557">no</span></span>             | <span data-ttu-id="4165a-558">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-558">no</span></span>           |
| <span data-ttu-id="4165a-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="4165a-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="4165a-560">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-560">no</span></span>             | <span data-ttu-id="4165a-561">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-561">no</span></span>           |
| <span data-ttu-id="4165a-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4165a-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="4165a-563">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-563">no</span></span>             | <span data-ttu-id="4165a-564">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-564">no</span></span>           |
| <span data-ttu-id="4165a-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4165a-565">msdyn_finish</span></span>                           | <span data-ttu-id="4165a-566">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-566">yes</span></span>            | <span data-ttu-id="4165a-567">ja</span><span class="sxs-lookup"><span data-stu-id="4165a-567">yes</span></span>          |
| <span data-ttu-id="4165a-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="4165a-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="4165a-569">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-569">no</span></span>             | <span data-ttu-id="4165a-570">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-570">no</span></span>           |
| <span data-ttu-id="4165a-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="4165a-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="4165a-572">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-572">no</span></span>             | <span data-ttu-id="4165a-573">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-573">no</span></span>           |
| <span data-ttu-id="4165a-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="4165a-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="4165a-575">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-575">no</span></span>             | <span data-ttu-id="4165a-576">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-576">no</span></span>           |
| <span data-ttu-id="4165a-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="4165a-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="4165a-578">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-578">no</span></span>             | <span data-ttu-id="4165a-579">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-579">no</span></span>           |
| <span data-ttu-id="4165a-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="4165a-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="4165a-581">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-581">no</span></span>             | <span data-ttu-id="4165a-582">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-582">no</span></span>           |
| <span data-ttu-id="4165a-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="4165a-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="4165a-584">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-584">no</span></span>             | <span data-ttu-id="4165a-585">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-585">no</span></span>           |
| <span data-ttu-id="4165a-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="4165a-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="4165a-587">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-587">no</span></span>             | <span data-ttu-id="4165a-588">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-588">no</span></span>           |
| <span data-ttu-id="4165a-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="4165a-590">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-590">no</span></span>             | <span data-ttu-id="4165a-591">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-591">no</span></span>           |
| <span data-ttu-id="4165a-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="4165a-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="4165a-593">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-593">no</span></span>             | <span data-ttu-id="4165a-594">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-594">no</span></span>           |
| <span data-ttu-id="4165a-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="4165a-596">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-596">no</span></span>             | <span data-ttu-id="4165a-597">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-597">no</span></span>           |
| <span data-ttu-id="4165a-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4165a-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="4165a-599">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-599">no</span></span>             | <span data-ttu-id="4165a-600">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-600">no</span></span>           |
| <span data-ttu-id="4165a-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="4165a-602">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-602">no</span></span>             | <span data-ttu-id="4165a-603">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-603">no</span></span>           |
| <span data-ttu-id="4165a-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="4165a-604">msdyn_progress</span></span>                         | <span data-ttu-id="4165a-605">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-605">no</span></span>             | <span data-ttu-id="4165a-606">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-606">no</span></span>           |
| <span data-ttu-id="4165a-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4165a-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="4165a-608">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-608">no</span></span>             | <span data-ttu-id="4165a-609">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-609">no</span></span>           |
| <span data-ttu-id="4165a-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="4165a-611">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-611">no</span></span>             | <span data-ttu-id="4165a-612">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-612">no</span></span>           |
| <span data-ttu-id="4165a-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4165a-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="4165a-614">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-614">no</span></span>             | <span data-ttu-id="4165a-615">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-615">no</span></span>           |
| <span data-ttu-id="4165a-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="4165a-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="4165a-617">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-617">no</span></span>             | <span data-ttu-id="4165a-618">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-618">no</span></span>           |
| <span data-ttu-id="4165a-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="4165a-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="4165a-620">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-620">no</span></span>             | <span data-ttu-id="4165a-621">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-621">no</span></span>           |
| <span data-ttu-id="4165a-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="4165a-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="4165a-623">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-623">no</span></span>             | <span data-ttu-id="4165a-624">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-624">no</span></span>           |
| <span data-ttu-id="4165a-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="4165a-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="4165a-626">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-626">no</span></span>             | <span data-ttu-id="4165a-627">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-627">no</span></span>           |
| <span data-ttu-id="4165a-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="4165a-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="4165a-629">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-629">no</span></span>             | <span data-ttu-id="4165a-630">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-630">no</span></span>           |
| <span data-ttu-id="4165a-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="4165a-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="4165a-632">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-632">no</span></span>             | <span data-ttu-id="4165a-633">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-633">no</span></span>           |
| <span data-ttu-id="4165a-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="4165a-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="4165a-635">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-635">no</span></span>             | <span data-ttu-id="4165a-636">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-636">no</span></span>           |
| <span data-ttu-id="4165a-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="4165a-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="4165a-638">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-638">no</span></span>             | <span data-ttu-id="4165a-639">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-639">no</span></span>           |
| <span data-ttu-id="4165a-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="4165a-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="4165a-641">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-641">no</span></span>             | <span data-ttu-id="4165a-642">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-642">no</span></span>           |
| <span data-ttu-id="4165a-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="4165a-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="4165a-644">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-644">no</span></span>             | <span data-ttu-id="4165a-645">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-645">no</span></span>           |
| <span data-ttu-id="4165a-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="4165a-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="4165a-647">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-647">no</span></span>             | <span data-ttu-id="4165a-648">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-648">no</span></span>           |
| <span data-ttu-id="4165a-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="4165a-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="4165a-650">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-650">no</span></span>             | <span data-ttu-id="4165a-651">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-651">no</span></span>           |
| <span data-ttu-id="4165a-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="4165a-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="4165a-653">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-653">no</span></span>             | <span data-ttu-id="4165a-654">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-654">no</span></span>           |
| <span data-ttu-id="4165a-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="4165a-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="4165a-656">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-656">no</span></span>             | <span data-ttu-id="4165a-657">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-657">no</span></span>           |
| <span data-ttu-id="4165a-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="4165a-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="4165a-659">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-659">no</span></span>             | <span data-ttu-id="4165a-660">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-660">no</span></span>           |
| <span data-ttu-id="4165a-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="4165a-662">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-662">no</span></span>             | <span data-ttu-id="4165a-663">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-663">no</span></span>           |
| <span data-ttu-id="4165a-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="4165a-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="4165a-665">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-665">no</span></span>             | <span data-ttu-id="4165a-666">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-666">no</span></span>           |
| <span data-ttu-id="4165a-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4165a-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="4165a-668">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-668">no</span></span>             | <span data-ttu-id="4165a-669">nej</span><span class="sxs-lookup"><span data-stu-id="4165a-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="4165a-670">Begränsningar och kända problem</span><span class="sxs-lookup"><span data-stu-id="4165a-670">Limitations and known issues</span></span>
<span data-ttu-id="4165a-671">Följande är en lista med begränsningar och kända problem:</span><span class="sxs-lookup"><span data-stu-id="4165a-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="4165a-672">Schema-API:er kan endast användas av **Användare med Microsoft Project License.**</span><span class="sxs-lookup"><span data-stu-id="4165a-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="4165a-673">De kan inte användas av:</span><span class="sxs-lookup"><span data-stu-id="4165a-673">They can't be used by:</span></span>
    - <span data-ttu-id="4165a-674">Programanvändare</span><span class="sxs-lookup"><span data-stu-id="4165a-674">Application users</span></span>
    - <span data-ttu-id="4165a-675">Systemanvändare</span><span class="sxs-lookup"><span data-stu-id="4165a-675">System users</span></span>
    - <span data-ttu-id="4165a-676">Integrationsanvändare</span><span class="sxs-lookup"><span data-stu-id="4165a-676">Integration users</span></span>
    - <span data-ttu-id="4165a-677">Andra användare som inte har den licens som krävs</span><span class="sxs-lookup"><span data-stu-id="4165a-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="4165a-678">Varje **OperationSet** kan endast ha högst 100 åtgärder.</span><span class="sxs-lookup"><span data-stu-id="4165a-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="4165a-679">Varje användare kan bara ha högst 10 öppna **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="4165a-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="4165a-680">Project Operations stöder för närvarande maximalt 500 totala uppgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="4165a-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="4165a-681">**OperationSet** felstatus och felloggar är för närvarande inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="4165a-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="4165a-682">Schemaläggnings-API:er är i offentlig förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="4165a-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="4165a-683">Microsoft har inte stöd för att använda dessa API:er i en produktionsmiljö.</span><span class="sxs-lookup"><span data-stu-id="4165a-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="4165a-684">Gränser för projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="4165a-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="4165a-685">Felhantering</span><span class="sxs-lookup"><span data-stu-id="4165a-685">Error handling</span></span>

   - <span data-ttu-id="4165a-686">Om du vill granska fel som uppstått från Åtgärdsuppsättningar går du till **Inställningar** \> **Schemalägg integration** \> **Åtgärdsuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="4165a-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="4165a-687">Om du vill granska fel som uppstått från tjänsten Projektschemaläggning går du till **Inställningar** \> **Schemalägg integration** \> **PSS-felloggar**.</span><span class="sxs-lookup"><span data-stu-id="4165a-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="4165a-688">Exempelscenario</span><span class="sxs-lookup"><span data-stu-id="4165a-688">Sample scenario</span></span>

<span data-ttu-id="4165a-689">I det här scenariot skapar du ett projekt, en teammedlem, fyra uppgifter och två resurstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="4165a-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="4165a-690">Nu ska du uppdatera en uppgift, uppdatera projektet, ta bort en uppgift, ta bort en resurstilldelning och skapa ett aktivitetsberoende.</span><span class="sxs-lookup"><span data-stu-id="4165a-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="4165a-691">Ytterligare exempel</span><span class="sxs-lookup"><span data-stu-id="4165a-691">Additional samples</span></span>

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
