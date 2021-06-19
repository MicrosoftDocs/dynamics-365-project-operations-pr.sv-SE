---
title: Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter
description: Detta ämne innehåller information och exempel för användning av schemaläggnings-API:er.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116819"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="82cb9-103">Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="82cb9-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="82cb9-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="82cb9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="82cb9-105">Vissa eller alla funktioner som anges i det här ämnet är tillgängliga som en del av en förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="82cb9-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="82cb9-106">Innehållet och funktionerna kan komma att ändras.</span><span class="sxs-lookup"><span data-stu-id="82cb9-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="82cb9-107">Schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="82cb9-107">Scheduling entities</span></span>

<span data-ttu-id="82cb9-108">Schemalägg API:er så att du kan skapa, uppdatera och ta bort åtgärder med **schemaläggningsentiteter**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="82cb9-109">Dessa entiteter hanteras med schemaläggningsmotorn i Projekt för webben.</span><span class="sxs-lookup"><span data-stu-id="82cb9-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="82cb9-110">Skapa, uppdatera och ta bort operationer med **Schemaläggningsentiteter** begränsades i tidigare versioner av Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="82cb9-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="82cb9-111">I följande tabell visas en fullständig lista över **Schemaläggningsentiteterna**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="82cb9-112">Entitetsnamn</span><span class="sxs-lookup"><span data-stu-id="82cb9-112">Entity name</span></span>  | <span data-ttu-id="82cb9-113">Entitetens logiska namn</span><span class="sxs-lookup"><span data-stu-id="82cb9-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="82cb9-114">Project</span><span class="sxs-lookup"><span data-stu-id="82cb9-114">Project</span></span> | <span data-ttu-id="82cb9-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="82cb9-115">msdyn_project</span></span> |
| <span data-ttu-id="82cb9-116">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="82cb9-116">Project Task</span></span>  | <span data-ttu-id="82cb9-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="82cb9-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="82cb9-118">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="82cb9-118">Project Task Dependency</span></span>  | <span data-ttu-id="82cb9-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="82cb9-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="82cb9-120">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="82cb9-120">Resource Assignment</span></span> | <span data-ttu-id="82cb9-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="82cb9-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="82cb9-122">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="82cb9-122">Project Bucket</span></span>  | <span data-ttu-id="82cb9-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="82cb9-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="82cb9-124">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="82cb9-124">Project Team Member</span></span> | <span data-ttu-id="82cb9-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="82cb9-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="82cb9-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="82cb9-126">OperationSet</span></span>

<span data-ttu-id="82cb9-127">OperationSet är ett enhetsmönster som kan användas när flera schemapåverkande förfrågningar måste bearbetas inom en transaktioner.</span><span class="sxs-lookup"><span data-stu-id="82cb9-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="82cb9-128">Schemaläggning-API:er</span><span class="sxs-lookup"><span data-stu-id="82cb9-128">Schedule APIs</span></span>

<span data-ttu-id="82cb9-129">Följande är en lista med aktuella schemaläggning-API:er.</span><span class="sxs-lookup"><span data-stu-id="82cb9-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="82cb9-130">**msdyn_CreateProjectV1**: Detta API kan användas för att skapa ett projekt.</span><span class="sxs-lookup"><span data-stu-id="82cb9-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="82cb9-131">Projekt och standardprojektgrupp skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="82cb9-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="82cb9-132">**msdyn_CreateTeamMemberV1**: Detta API kan användas för att skapa en projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="82cb9-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="82cb9-133">Teammedlemsposten skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="82cb9-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="82cb9-134">**msdyn_CreateOperationSetV1**: Detta API kan användas för att schemalägga flera förfrågningar som måste utföras inom en transaktionen.</span><span class="sxs-lookup"><span data-stu-id="82cb9-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="82cb9-135">**msdyn_PSSCreateV1**: Det här API:et kan användas för att skapa en entitet.</span><span class="sxs-lookup"><span data-stu-id="82cb9-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="82cb9-136">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden skapa.</span><span class="sxs-lookup"><span data-stu-id="82cb9-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="82cb9-137">**msdyn_PSSUpdateV1**: Det här API:et kan användas för att uppdatera en entitet.</span><span class="sxs-lookup"><span data-stu-id="82cb9-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="82cb9-138">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden uppdatera.</span><span class="sxs-lookup"><span data-stu-id="82cb9-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="82cb9-139">**msdyn_PSSDeleteV1**: Det här API:et kan användas för att ta bort en entitet.</span><span class="sxs-lookup"><span data-stu-id="82cb9-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="82cb9-140">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden ta bort.</span><span class="sxs-lookup"><span data-stu-id="82cb9-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="82cb9-141">**msdyn_ExecuteOperationSetV1**: Detta API används för att köra alla åtgärder inom den angivna åtgärdsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="82cb9-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="82cb9-142">Använda schemaläggnings-API:er med OperationSet</span><span class="sxs-lookup"><span data-stu-id="82cb9-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="82cb9-143">Eftersom poster med både **CreateProjectV1** och **CreateTeamMemberV1** skapas direkt kan dessa API:er inte användas direkt i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="82cb9-144">Men du kan använda API för att skapa nödvändiga poster, skapa en **OperationSet** och sedan använda dessa förskapade poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="82cb9-145">Åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="82cb9-145">Supported operations</span></span>

| <span data-ttu-id="82cb9-146">Schemaläggningsentitet</span><span class="sxs-lookup"><span data-stu-id="82cb9-146">Scheduling entity</span></span> | <span data-ttu-id="82cb9-147">Skapa</span><span class="sxs-lookup"><span data-stu-id="82cb9-147">Create</span></span> | <span data-ttu-id="82cb9-148">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="82cb9-148">Update</span></span> | <span data-ttu-id="82cb9-149">Delete</span><span class="sxs-lookup"><span data-stu-id="82cb9-149">Delete</span></span> | <span data-ttu-id="82cb9-150">Viktigt!</span><span class="sxs-lookup"><span data-stu-id="82cb9-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="82cb9-151">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="82cb9-151">Project task</span></span> | <span data-ttu-id="82cb9-152">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-152">Yes</span></span> | <span data-ttu-id="82cb9-153">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-153">Yes</span></span> | <span data-ttu-id="82cb9-154">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-154">Yes</span></span> | <span data-ttu-id="82cb9-155">Nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-155">None</span></span> |
| <span data-ttu-id="82cb9-156">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="82cb9-156">Project task dependency</span></span> | <span data-ttu-id="82cb9-157">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-157">Yes</span></span> | <span data-ttu-id="82cb9-158">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-158">Yes</span></span> | | <span data-ttu-id="82cb9-159">Poster för projektuppgiftsberoende uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="82cb9-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="82cb9-160">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="82cb9-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="82cb9-161">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="82cb9-161">Resource assignment</span></span> | <span data-ttu-id="82cb9-162">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-162">Yes</span></span> | <span data-ttu-id="82cb9-163">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-163">Yes</span></span> | | <span data-ttu-id="82cb9-164">Operationer med följande fält stöds inte: **BookableResourceID**, **Insats**, **EffortCompleted**, **EffortRemaining** och **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="82cb9-165">Resurstilldelningsposter uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="82cb9-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="82cb9-166">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="82cb9-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="82cb9-167">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="82cb9-167">Project bucket</span></span> | <span data-ttu-id="82cb9-168">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="82cb9-168">N/A</span></span> | <span data-ttu-id="82cb9-169">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="82cb9-169">N/A</span></span> | <span data-ttu-id="82cb9-170">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="82cb9-170">N/A</span></span> | <span data-ttu-id="82cb9-171">Standardgruppen skapas för att använda API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="82cb9-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="82cb9-172">Project team member</span></span> | <span data-ttu-id="82cb9-173">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-173">Yes</span></span> | <span data-ttu-id="82cb9-174">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-174">Yes</span></span> | <span data-ttu-id="82cb9-175">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-175">Yes</span></span> | <span data-ttu-id="82cb9-176">För att skapa operation, använda API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="82cb9-177">Project</span><span class="sxs-lookup"><span data-stu-id="82cb9-177">Project</span></span> | <span data-ttu-id="82cb9-178">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-178">Yes</span></span> | <span data-ttu-id="82cb9-179">Ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-179">Yes</span></span> | <span data-ttu-id="82cb9-180">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="82cb9-180">N/A</span></span> | <span data-ttu-id="82cb9-181">Operationer med följande fält stöds inte: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Insats**, **EffortCompleted**, **EffortRemaining**, **Förlopp**, **Slutför**, **TaskEarliestStart** och **Varaktighet**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="82cb9-182">Dessa API:er kan anropas med entitetsobjekt som innehåller anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="82cb9-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="82cb9-183">ID-egenskapen är valfri.</span><span class="sxs-lookup"><span data-stu-id="82cb9-183">The ID property is optional.</span></span> <span data-ttu-id="82cb9-184">Om det finns ett undantag försöker systemet använda det och ett undantag om det inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="82cb9-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="82cb9-185">Om den inte finns genererar systemet den.</span><span class="sxs-lookup"><span data-stu-id="82cb9-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="82cb9-186">Begränsade fält</span><span class="sxs-lookup"><span data-stu-id="82cb9-186">Restricted fields</span></span>

<span data-ttu-id="82cb9-187">I följande tabeller definieras fälten som är begränsade från **Skapa** och **Redigera.**</span><span class="sxs-lookup"><span data-stu-id="82cb9-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="82cb9-188">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="82cb9-188">Project task</span></span>

| <span data-ttu-id="82cb9-189">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="82cb9-189">**Logical name**</span></span>                       | <span data-ttu-id="82cb9-190">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="82cb9-190">**Can create**</span></span> | <span data-ttu-id="82cb9-191">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="82cb9-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="82cb9-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="82cb9-193">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-193">no</span></span>             | <span data-ttu-id="82cb9-194">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-194">no</span></span>               |
| <span data-ttu-id="82cb9-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="82cb9-196">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-196">no</span></span>             | <span data-ttu-id="82cb9-197">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-197">no</span></span>               |
| <span data-ttu-id="82cb9-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="82cb9-198">msdyn_actualend</span></span>                        | <span data-ttu-id="82cb9-199">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-199">no</span></span>             | <span data-ttu-id="82cb9-200">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-200">no</span></span>               |
| <span data-ttu-id="82cb9-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="82cb9-202">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-202">no</span></span>             | <span data-ttu-id="82cb9-203">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-203">no</span></span>               |
| <span data-ttu-id="82cb9-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="82cb9-205">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-205">no</span></span>             | <span data-ttu-id="82cb9-206">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-206">no</span></span>               |
| <span data-ttu-id="82cb9-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="82cb9-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="82cb9-208">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-208">no</span></span>             | <span data-ttu-id="82cb9-209">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-209">no</span></span>               |
| <span data-ttu-id="82cb9-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="82cb9-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="82cb9-211">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-211">no</span></span>             | <span data-ttu-id="82cb9-212">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-212">no</span></span>               |
| <span data-ttu-id="82cb9-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="82cb9-214">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-214">no</span></span>             | <span data-ttu-id="82cb9-215">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-215">no</span></span>               |
| <span data-ttu-id="82cb9-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="82cb9-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="82cb9-217">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-217">no</span></span>             | <span data-ttu-id="82cb9-218">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-218">no</span></span>               |
| <span data-ttu-id="82cb9-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="82cb9-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="82cb9-220">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-220">no</span></span>             | <span data-ttu-id="82cb9-221">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-221">no</span></span>               |
| <span data-ttu-id="82cb9-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="82cb9-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="82cb9-223">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-223">no</span></span>             | <span data-ttu-id="82cb9-224">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-224">no</span></span>               |
| <span data-ttu-id="82cb9-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="82cb9-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="82cb9-226">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-226">no</span></span>             | <span data-ttu-id="82cb9-227">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-227">no</span></span>               |
| <span data-ttu-id="82cb9-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="82cb9-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="82cb9-229">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-229">no</span></span>             | <span data-ttu-id="82cb9-230">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-230">no</span></span>               |
| <span data-ttu-id="82cb9-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="82cb9-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="82cb9-232">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-232">no</span></span>             | <span data-ttu-id="82cb9-233">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-233">no</span></span>               |
| <span data-ttu-id="82cb9-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="82cb9-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="82cb9-235">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-235">no</span></span>             | <span data-ttu-id="82cb9-236">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-236">no</span></span>               |
| <span data-ttu-id="82cb9-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="82cb9-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="82cb9-238">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-238">no</span></span>             | <span data-ttu-id="82cb9-239">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-239">no</span></span>               |
| <span data-ttu-id="82cb9-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="82cb9-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="82cb9-241">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-241">no</span></span>             | <span data-ttu-id="82cb9-242">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-242">no</span></span>               |
| <span data-ttu-id="82cb9-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="82cb9-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="82cb9-244">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-244">no</span></span>             | <span data-ttu-id="82cb9-245">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-245">no</span></span>               |
| <span data-ttu-id="82cb9-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="82cb9-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="82cb9-247">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-247">no</span></span>             | <span data-ttu-id="82cb9-248">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-248">no</span></span>               |
| <span data-ttu-id="82cb9-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="82cb9-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="82cb9-250">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-250">no</span></span>             | <span data-ttu-id="82cb9-251">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-251">no</span></span>               |
| <span data-ttu-id="82cb9-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="82cb9-253">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-253">no</span></span>             | <span data-ttu-id="82cb9-254">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-254">no</span></span>               |
| <span data-ttu-id="82cb9-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="82cb9-256">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-256">no</span></span>             | <span data-ttu-id="82cb9-257">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-257">no</span></span>               |
| <span data-ttu-id="82cb9-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="82cb9-259">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-259">no</span></span>             | <span data-ttu-id="82cb9-260">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-260">no</span></span>               |
| <span data-ttu-id="82cb9-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="82cb9-262">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-262">no</span></span>             | <span data-ttu-id="82cb9-263">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-263">no</span></span>               |
| <span data-ttu-id="82cb9-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="82cb9-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="82cb9-265">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-265">no</span></span>             | <span data-ttu-id="82cb9-266">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-266">no</span></span>               |
| <span data-ttu-id="82cb9-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="82cb9-267">msdyn_progress</span></span>                         | <span data-ttu-id="82cb9-268">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-268">no</span></span>             | <span data-ttu-id="82cb9-269">nej (ja för P4W)</span><span class="sxs-lookup"><span data-stu-id="82cb9-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="82cb9-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="82cb9-271">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-271">no</span></span>             | <span data-ttu-id="82cb9-272">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-272">no</span></span>               |
| <span data-ttu-id="82cb9-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="82cb9-274">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-274">no</span></span>             | <span data-ttu-id="82cb9-275">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-275">no</span></span>               |
| <span data-ttu-id="82cb9-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="82cb9-277">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-277">no</span></span>             | <span data-ttu-id="82cb9-278">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-278">no</span></span>               |
| <span data-ttu-id="82cb9-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="82cb9-280">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-280">no</span></span>             | <span data-ttu-id="82cb9-281">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-281">no</span></span>               |
| <span data-ttu-id="82cb9-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="82cb9-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="82cb9-283">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-283">no</span></span>             | <span data-ttu-id="82cb9-284">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-284">no</span></span>               |
| <span data-ttu-id="82cb9-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="82cb9-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="82cb9-286">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-286">no</span></span>             | <span data-ttu-id="82cb9-287">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-287">no</span></span>               |
| <span data-ttu-id="82cb9-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="82cb9-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="82cb9-289">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-289">no</span></span>             | <span data-ttu-id="82cb9-290">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-290">no</span></span>               |
| <span data-ttu-id="82cb9-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="82cb9-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="82cb9-292">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-292">no</span></span>             | <span data-ttu-id="82cb9-293">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-293">no</span></span>               |
| <span data-ttu-id="82cb9-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="82cb9-295">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-295">no</span></span>             | <span data-ttu-id="82cb9-296">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-296">no</span></span>               |
| <span data-ttu-id="82cb9-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="82cb9-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="82cb9-298">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-298">no</span></span>             | <span data-ttu-id="82cb9-299">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-299">no</span></span>               |
| <span data-ttu-id="82cb9-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="82cb9-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="82cb9-301">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-301">no</span></span>             | <span data-ttu-id="82cb9-302">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-302">no</span></span>               |
| <span data-ttu-id="82cb9-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="82cb9-304">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-304">no</span></span>             | <span data-ttu-id="82cb9-305">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-305">no</span></span>               |
| <span data-ttu-id="82cb9-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="82cb9-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="82cb9-307">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-307">no</span></span>             | <span data-ttu-id="82cb9-308">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-308">no</span></span>               |
| <span data-ttu-id="82cb9-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="82cb9-310">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-310">no</span></span>             | <span data-ttu-id="82cb9-311">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-311">no</span></span>               |
| <span data-ttu-id="82cb9-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="82cb9-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="82cb9-313">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-313">no</span></span>             | <span data-ttu-id="82cb9-314">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-314">no</span></span>               |
| <span data-ttu-id="82cb9-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="82cb9-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="82cb9-316">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-316">no</span></span>             | <span data-ttu-id="82cb9-317">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-317">no</span></span>               |
| <span data-ttu-id="82cb9-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="82cb9-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="82cb9-319">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-319">no</span></span>             | <span data-ttu-id="82cb9-320">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-320">no</span></span>               |
| <span data-ttu-id="82cb9-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="82cb9-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="82cb9-322">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-322">no</span></span>             | <span data-ttu-id="82cb9-323">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-323">no</span></span>               |
| <span data-ttu-id="82cb9-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="82cb9-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="82cb9-325">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-325">no</span></span>             | <span data-ttu-id="82cb9-326">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-326">no</span></span>               |
| <span data-ttu-id="82cb9-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="82cb9-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="82cb9-328">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-328">no</span></span>             | <span data-ttu-id="82cb9-329">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-329">no</span></span>               |
| <span data-ttu-id="82cb9-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="82cb9-330">msdyn_summary</span></span>                          | <span data-ttu-id="82cb9-331">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-331">no</span></span>             | <span data-ttu-id="82cb9-332">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-332">no</span></span>               |
| <span data-ttu-id="82cb9-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="82cb9-334">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-334">no</span></span>             | <span data-ttu-id="82cb9-335">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-335">no</span></span>               |
| <span data-ttu-id="82cb9-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="82cb9-337">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-337">no</span></span>             | <span data-ttu-id="82cb9-338">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="82cb9-339">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="82cb9-339">Project task dependency</span></span>

| <span data-ttu-id="82cb9-340">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="82cb9-340">**Logical name**</span></span>              | <span data-ttu-id="82cb9-341">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="82cb9-341">**Can create**</span></span> | <span data-ttu-id="82cb9-342">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="82cb9-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="82cb9-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="82cb9-343">msdyn_linktype</span></span>                | <span data-ttu-id="82cb9-344">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-344">no</span></span>             | <span data-ttu-id="82cb9-345">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-345">no</span></span>           |
| <span data-ttu-id="82cb9-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="82cb9-346">msdyn_linktypename</span></span>            | <span data-ttu-id="82cb9-347">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-347">no</span></span>             | <span data-ttu-id="82cb9-348">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-348">no</span></span>           |
| <span data-ttu-id="82cb9-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="82cb9-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="82cb9-350">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-350">yes</span></span>            | <span data-ttu-id="82cb9-351">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-351">no</span></span>           |
| <span data-ttu-id="82cb9-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="82cb9-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="82cb9-353">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-353">yes</span></span>            | <span data-ttu-id="82cb9-354">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-354">no</span></span>           |
| <span data-ttu-id="82cb9-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="82cb9-355">msdyn_project</span></span>                 | <span data-ttu-id="82cb9-356">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-356">yes</span></span>            | <span data-ttu-id="82cb9-357">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-357">no</span></span>           |
| <span data-ttu-id="82cb9-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="82cb9-358">msdyn_projectname</span></span>             | <span data-ttu-id="82cb9-359">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-359">yes</span></span>            | <span data-ttu-id="82cb9-360">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-360">no</span></span>           |
| <span data-ttu-id="82cb9-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="82cb9-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="82cb9-362">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-362">yes</span></span>            | <span data-ttu-id="82cb9-363">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-363">no</span></span>           |
| <span data-ttu-id="82cb9-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="82cb9-364">msdyn_successortask</span></span>           | <span data-ttu-id="82cb9-365">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-365">yes</span></span>            | <span data-ttu-id="82cb9-366">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-366">no</span></span>           |
| <span data-ttu-id="82cb9-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="82cb9-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="82cb9-368">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-368">yes</span></span>            | <span data-ttu-id="82cb9-369">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="82cb9-370">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="82cb9-370">Resource assignment</span></span>

| <span data-ttu-id="82cb9-371">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="82cb9-371">**Logical name**</span></span>             | <span data-ttu-id="82cb9-372">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="82cb9-372">**Can create**</span></span> | <span data-ttu-id="82cb9-373">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="82cb9-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="82cb9-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="82cb9-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="82cb9-375">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-375">yes</span></span>            | <span data-ttu-id="82cb9-376">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-376">no</span></span>           |
| <span data-ttu-id="82cb9-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="82cb9-378">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-378">yes</span></span>            | <span data-ttu-id="82cb9-379">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-379">no</span></span>           |
| <span data-ttu-id="82cb9-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="82cb9-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="82cb9-381">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-381">no</span></span>             | <span data-ttu-id="82cb9-382">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-382">no</span></span>           |
| <span data-ttu-id="82cb9-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="82cb9-384">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-384">no</span></span>             | <span data-ttu-id="82cb9-385">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-385">no</span></span>           |
| <span data-ttu-id="82cb9-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="82cb9-386">msdyn_committype</span></span>             | <span data-ttu-id="82cb9-387">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-387">no</span></span>             | <span data-ttu-id="82cb9-388">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-388">no</span></span>           |
| <span data-ttu-id="82cb9-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="82cb9-389">msdyn_committypename</span></span>         | <span data-ttu-id="82cb9-390">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-390">no</span></span>             | <span data-ttu-id="82cb9-391">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-391">no</span></span>           |
| <span data-ttu-id="82cb9-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="82cb9-392">msdyn_effort</span></span>                 | <span data-ttu-id="82cb9-393">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-393">no</span></span>             | <span data-ttu-id="82cb9-394">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-394">no</span></span>           |
| <span data-ttu-id="82cb9-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="82cb9-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="82cb9-396">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-396">no</span></span>             | <span data-ttu-id="82cb9-397">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-397">no</span></span>           |
| <span data-ttu-id="82cb9-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="82cb9-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="82cb9-399">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-399">no</span></span>             | <span data-ttu-id="82cb9-400">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-400">no</span></span>           |
| <span data-ttu-id="82cb9-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="82cb9-401">msdyn_finish</span></span>                 | <span data-ttu-id="82cb9-402">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-402">no</span></span>             | <span data-ttu-id="82cb9-403">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-403">no</span></span>           |
| <span data-ttu-id="82cb9-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="82cb9-405">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-405">no</span></span>             | <span data-ttu-id="82cb9-406">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-406">no</span></span>           |
| <span data-ttu-id="82cb9-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="82cb9-408">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-408">no</span></span>             | <span data-ttu-id="82cb9-409">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-409">no</span></span>           |
| <span data-ttu-id="82cb9-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="82cb9-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="82cb9-411">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-411">no</span></span>             | <span data-ttu-id="82cb9-412">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-412">no</span></span>           |
| <span data-ttu-id="82cb9-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="82cb9-414">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-414">no</span></span>             | <span data-ttu-id="82cb9-415">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-415">no</span></span>           |
| <span data-ttu-id="82cb9-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="82cb9-417">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-417">no</span></span>             | <span data-ttu-id="82cb9-418">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-418">no</span></span>           |
| <span data-ttu-id="82cb9-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="82cb9-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="82cb9-420">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-420">no</span></span>             | <span data-ttu-id="82cb9-421">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-421">no</span></span>           |
| <span data-ttu-id="82cb9-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="82cb9-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="82cb9-423">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-423">no</span></span>             | <span data-ttu-id="82cb9-424">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-424">no</span></span>           |
| <span data-ttu-id="82cb9-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="82cb9-425">msdyn_projectid</span></span>              | <span data-ttu-id="82cb9-426">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-426">yes</span></span>            | <span data-ttu-id="82cb9-427">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-427">no</span></span>           |
| <span data-ttu-id="82cb9-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-428">msdyn_projectidname</span></span>          | <span data-ttu-id="82cb9-429">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-429">no</span></span>             | <span data-ttu-id="82cb9-430">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-430">no</span></span>           |
| <span data-ttu-id="82cb9-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="82cb9-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="82cb9-432">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-432">no</span></span>             | <span data-ttu-id="82cb9-433">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-433">no</span></span>           |
| <span data-ttu-id="82cb9-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="82cb9-435">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-435">no</span></span>             | <span data-ttu-id="82cb9-436">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-436">no</span></span>           |
| <span data-ttu-id="82cb9-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="82cb9-437">msdyn_start</span></span>                  | <span data-ttu-id="82cb9-438">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-438">no</span></span>             | <span data-ttu-id="82cb9-439">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-439">no</span></span>           |
| <span data-ttu-id="82cb9-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="82cb9-440">msdyn_taskid</span></span>                 | <span data-ttu-id="82cb9-441">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-441">no</span></span>             | <span data-ttu-id="82cb9-442">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-442">no</span></span>           |
| <span data-ttu-id="82cb9-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-443">msdyn_taskidname</span></span>             | <span data-ttu-id="82cb9-444">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-444">no</span></span>             | <span data-ttu-id="82cb9-445">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-445">no</span></span>           |
| <span data-ttu-id="82cb9-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="82cb9-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="82cb9-447">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-447">no</span></span>             | <span data-ttu-id="82cb9-448">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="82cb9-449">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="82cb9-449">Project team member</span></span>

| <span data-ttu-id="82cb9-450">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="82cb9-450">**Logical name**</span></span>                                 | <span data-ttu-id="82cb9-451">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="82cb9-451">**Can create**</span></span> | <span data-ttu-id="82cb9-452">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="82cb9-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="82cb9-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="82cb9-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="82cb9-454">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-454">no</span></span>             | <span data-ttu-id="82cb9-455">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-455">no</span></span>           |
| <span data-ttu-id="82cb9-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="82cb9-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="82cb9-457">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-457">no</span></span>             | <span data-ttu-id="82cb9-458">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-458">no</span></span>           |
| <span data-ttu-id="82cb9-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="82cb9-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="82cb9-460">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-460">no</span></span>             | <span data-ttu-id="82cb9-461">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-461">no</span></span>           |
| <span data-ttu-id="82cb9-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="82cb9-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="82cb9-463">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-463">no</span></span>             | <span data-ttu-id="82cb9-464">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-464">no</span></span>           |
| <span data-ttu-id="82cb9-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="82cb9-465">msdyn_effort</span></span>                                     | <span data-ttu-id="82cb9-466">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-466">no</span></span>             | <span data-ttu-id="82cb9-467">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-467">no</span></span>           |
| <span data-ttu-id="82cb9-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="82cb9-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="82cb9-469">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-469">no</span></span>             | <span data-ttu-id="82cb9-470">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-470">no</span></span>           |
| <span data-ttu-id="82cb9-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="82cb9-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="82cb9-472">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-472">no</span></span>             | <span data-ttu-id="82cb9-473">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-473">no</span></span>           |
| <span data-ttu-id="82cb9-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="82cb9-474">msdyn_finish</span></span>                                     | <span data-ttu-id="82cb9-475">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-475">no</span></span>             | <span data-ttu-id="82cb9-476">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-476">no</span></span>           |
| <span data-ttu-id="82cb9-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="82cb9-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="82cb9-478">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-478">no</span></span>             | <span data-ttu-id="82cb9-479">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-479">no</span></span>           |
| <span data-ttu-id="82cb9-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="82cb9-480">msdyn_hours</span></span>                                      | <span data-ttu-id="82cb9-481">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-481">no</span></span>             | <span data-ttu-id="82cb9-482">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-482">no</span></span>           |
| <span data-ttu-id="82cb9-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="82cb9-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="82cb9-484">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-484">no</span></span>             | <span data-ttu-id="82cb9-485">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-485">no</span></span>           |
| <span data-ttu-id="82cb9-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="82cb9-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="82cb9-487">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-487">no</span></span>             | <span data-ttu-id="82cb9-488">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-488">no</span></span>           |
| <span data-ttu-id="82cb9-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="82cb9-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="82cb9-490">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-490">no</span></span>             | <span data-ttu-id="82cb9-491">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-491">no</span></span>           |
| <span data-ttu-id="82cb9-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="82cb9-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="82cb9-493">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-493">no</span></span>             | <span data-ttu-id="82cb9-494">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-494">no</span></span>           |
| <span data-ttu-id="82cb9-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="82cb9-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="82cb9-496">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-496">no</span></span>             | <span data-ttu-id="82cb9-497">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-497">no</span></span>           |
| <span data-ttu-id="82cb9-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="82cb9-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="82cb9-499">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-499">no</span></span>             | <span data-ttu-id="82cb9-500">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-500">no</span></span>           |
| <span data-ttu-id="82cb9-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="82cb9-501">msdyn_start</span></span>                                      | <span data-ttu-id="82cb9-502">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-502">no</span></span>             | <span data-ttu-id="82cb9-503">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="82cb9-504">Project</span><span class="sxs-lookup"><span data-stu-id="82cb9-504">Project</span></span>

| <span data-ttu-id="82cb9-505">**Logiskt namn**</span><span class="sxs-lookup"><span data-stu-id="82cb9-505">**Logical name**</span></span>                       | <span data-ttu-id="82cb9-506">**Kan skapa**</span><span class="sxs-lookup"><span data-stu-id="82cb9-506">**Can create**</span></span> | <span data-ttu-id="82cb9-507">**Kan redigera**</span><span class="sxs-lookup"><span data-stu-id="82cb9-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="82cb9-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="82cb9-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="82cb9-509">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-509">no</span></span>             | <span data-ttu-id="82cb9-510">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-510">no</span></span>           |
| <span data-ttu-id="82cb9-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="82cb9-512">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-512">no</span></span>             | <span data-ttu-id="82cb9-513">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-513">no</span></span>           |
| <span data-ttu-id="82cb9-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="82cb9-515">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-515">no</span></span>             | <span data-ttu-id="82cb9-516">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-516">no</span></span>           |
| <span data-ttu-id="82cb9-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="82cb9-518">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-518">no</span></span>             | <span data-ttu-id="82cb9-519">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-519">no</span></span>           |
| <span data-ttu-id="82cb9-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="82cb9-521">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-521">no</span></span>             | <span data-ttu-id="82cb9-522">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-522">no</span></span>           |
| <span data-ttu-id="82cb9-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="82cb9-524">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-524">no</span></span>             | <span data-ttu-id="82cb9-525">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-525">no</span></span>           |
| <span data-ttu-id="82cb9-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="82cb9-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="82cb9-527">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-527">yes</span></span>            | <span data-ttu-id="82cb9-528">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-528">no</span></span>           |
| <span data-ttu-id="82cb9-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="82cb9-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="82cb9-530">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-530">yes</span></span>            | <span data-ttu-id="82cb9-531">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-531">no</span></span>           |
| <span data-ttu-id="82cb9-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="82cb9-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="82cb9-533">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-533">yes</span></span>            | <span data-ttu-id="82cb9-534">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-534">no</span></span>           |
| <span data-ttu-id="82cb9-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="82cb9-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="82cb9-536">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-536">no</span></span>             | <span data-ttu-id="82cb9-537">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-537">no</span></span>           |
| <span data-ttu-id="82cb9-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="82cb9-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="82cb9-539">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-539">no</span></span>             | <span data-ttu-id="82cb9-540">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-540">no</span></span>           |
| <span data-ttu-id="82cb9-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="82cb9-542">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-542">no</span></span>             | <span data-ttu-id="82cb9-543">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-543">no</span></span>           |
| <span data-ttu-id="82cb9-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="82cb9-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="82cb9-545">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-545">no</span></span>             | <span data-ttu-id="82cb9-546">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-546">no</span></span>           |
| <span data-ttu-id="82cb9-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="82cb9-548">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-548">no</span></span>             | <span data-ttu-id="82cb9-549">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-549">no</span></span>           |
| <span data-ttu-id="82cb9-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="82cb9-550">msdyn_duration</span></span>                         | <span data-ttu-id="82cb9-551">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-551">no</span></span>             | <span data-ttu-id="82cb9-552">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-552">no</span></span>           |
| <span data-ttu-id="82cb9-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="82cb9-553">msdyn_effort</span></span>                           | <span data-ttu-id="82cb9-554">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-554">no</span></span>             | <span data-ttu-id="82cb9-555">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-555">no</span></span>           |
| <span data-ttu-id="82cb9-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="82cb9-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="82cb9-557">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-557">no</span></span>             | <span data-ttu-id="82cb9-558">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-558">no</span></span>           |
| <span data-ttu-id="82cb9-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="82cb9-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="82cb9-560">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-560">no</span></span>             | <span data-ttu-id="82cb9-561">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-561">no</span></span>           |
| <span data-ttu-id="82cb9-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="82cb9-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="82cb9-563">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-563">no</span></span>             | <span data-ttu-id="82cb9-564">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-564">no</span></span>           |
| <span data-ttu-id="82cb9-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="82cb9-565">msdyn_finish</span></span>                           | <span data-ttu-id="82cb9-566">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-566">yes</span></span>            | <span data-ttu-id="82cb9-567">ja</span><span class="sxs-lookup"><span data-stu-id="82cb9-567">yes</span></span>          |
| <span data-ttu-id="82cb9-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="82cb9-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="82cb9-569">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-569">no</span></span>             | <span data-ttu-id="82cb9-570">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-570">no</span></span>           |
| <span data-ttu-id="82cb9-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="82cb9-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="82cb9-572">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-572">no</span></span>             | <span data-ttu-id="82cb9-573">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-573">no</span></span>           |
| <span data-ttu-id="82cb9-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="82cb9-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="82cb9-575">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-575">no</span></span>             | <span data-ttu-id="82cb9-576">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-576">no</span></span>           |
| <span data-ttu-id="82cb9-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="82cb9-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="82cb9-578">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-578">no</span></span>             | <span data-ttu-id="82cb9-579">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-579">no</span></span>           |
| <span data-ttu-id="82cb9-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="82cb9-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="82cb9-581">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-581">no</span></span>             | <span data-ttu-id="82cb9-582">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-582">no</span></span>           |
| <span data-ttu-id="82cb9-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="82cb9-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="82cb9-584">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-584">no</span></span>             | <span data-ttu-id="82cb9-585">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-585">no</span></span>           |
| <span data-ttu-id="82cb9-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="82cb9-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="82cb9-587">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-587">no</span></span>             | <span data-ttu-id="82cb9-588">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-588">no</span></span>           |
| <span data-ttu-id="82cb9-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="82cb9-590">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-590">no</span></span>             | <span data-ttu-id="82cb9-591">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-591">no</span></span>           |
| <span data-ttu-id="82cb9-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="82cb9-593">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-593">no</span></span>             | <span data-ttu-id="82cb9-594">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-594">no</span></span>           |
| <span data-ttu-id="82cb9-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="82cb9-596">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-596">no</span></span>             | <span data-ttu-id="82cb9-597">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-597">no</span></span>           |
| <span data-ttu-id="82cb9-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="82cb9-599">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-599">no</span></span>             | <span data-ttu-id="82cb9-600">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-600">no</span></span>           |
| <span data-ttu-id="82cb9-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="82cb9-602">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-602">no</span></span>             | <span data-ttu-id="82cb9-603">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-603">no</span></span>           |
| <span data-ttu-id="82cb9-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="82cb9-604">msdyn_progress</span></span>                         | <span data-ttu-id="82cb9-605">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-605">no</span></span>             | <span data-ttu-id="82cb9-606">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-606">no</span></span>           |
| <span data-ttu-id="82cb9-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="82cb9-608">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-608">no</span></span>             | <span data-ttu-id="82cb9-609">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-609">no</span></span>           |
| <span data-ttu-id="82cb9-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="82cb9-611">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-611">no</span></span>             | <span data-ttu-id="82cb9-612">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-612">no</span></span>           |
| <span data-ttu-id="82cb9-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="82cb9-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="82cb9-614">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-614">no</span></span>             | <span data-ttu-id="82cb9-615">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-615">no</span></span>           |
| <span data-ttu-id="82cb9-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="82cb9-617">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-617">no</span></span>             | <span data-ttu-id="82cb9-618">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-618">no</span></span>           |
| <span data-ttu-id="82cb9-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="82cb9-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="82cb9-620">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-620">no</span></span>             | <span data-ttu-id="82cb9-621">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-621">no</span></span>           |
| <span data-ttu-id="82cb9-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="82cb9-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="82cb9-623">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-623">no</span></span>             | <span data-ttu-id="82cb9-624">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-624">no</span></span>           |
| <span data-ttu-id="82cb9-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="82cb9-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="82cb9-626">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-626">no</span></span>             | <span data-ttu-id="82cb9-627">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-627">no</span></span>           |
| <span data-ttu-id="82cb9-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="82cb9-629">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-629">no</span></span>             | <span data-ttu-id="82cb9-630">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-630">no</span></span>           |
| <span data-ttu-id="82cb9-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="82cb9-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="82cb9-632">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-632">no</span></span>             | <span data-ttu-id="82cb9-633">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-633">no</span></span>           |
| <span data-ttu-id="82cb9-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="82cb9-635">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-635">no</span></span>             | <span data-ttu-id="82cb9-636">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-636">no</span></span>           |
| <span data-ttu-id="82cb9-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="82cb9-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="82cb9-638">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-638">no</span></span>             | <span data-ttu-id="82cb9-639">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-639">no</span></span>           |
| <span data-ttu-id="82cb9-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="82cb9-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="82cb9-641">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-641">no</span></span>             | <span data-ttu-id="82cb9-642">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-642">no</span></span>           |
| <span data-ttu-id="82cb9-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="82cb9-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="82cb9-644">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-644">no</span></span>             | <span data-ttu-id="82cb9-645">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-645">no</span></span>           |
| <span data-ttu-id="82cb9-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="82cb9-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="82cb9-647">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-647">no</span></span>             | <span data-ttu-id="82cb9-648">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-648">no</span></span>           |
| <span data-ttu-id="82cb9-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="82cb9-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="82cb9-650">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-650">no</span></span>             | <span data-ttu-id="82cb9-651">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-651">no</span></span>           |
| <span data-ttu-id="82cb9-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="82cb9-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="82cb9-653">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-653">no</span></span>             | <span data-ttu-id="82cb9-654">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-654">no</span></span>           |
| <span data-ttu-id="82cb9-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="82cb9-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="82cb9-656">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-656">no</span></span>             | <span data-ttu-id="82cb9-657">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-657">no</span></span>           |
| <span data-ttu-id="82cb9-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="82cb9-659">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-659">no</span></span>             | <span data-ttu-id="82cb9-660">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-660">no</span></span>           |
| <span data-ttu-id="82cb9-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="82cb9-662">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-662">no</span></span>             | <span data-ttu-id="82cb9-663">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-663">no</span></span>           |
| <span data-ttu-id="82cb9-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="82cb9-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="82cb9-665">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-665">no</span></span>             | <span data-ttu-id="82cb9-666">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-666">no</span></span>           |
| <span data-ttu-id="82cb9-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="82cb9-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="82cb9-668">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-668">no</span></span>             | <span data-ttu-id="82cb9-669">nej</span><span class="sxs-lookup"><span data-stu-id="82cb9-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="82cb9-670">Begränsningar och kända problem</span><span class="sxs-lookup"><span data-stu-id="82cb9-670">Limitations and known issues</span></span>
<span data-ttu-id="82cb9-671">Följande är en lista med begränsningar och kända problem:</span><span class="sxs-lookup"><span data-stu-id="82cb9-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="82cb9-672">Schema-API:er kan endast användas av **Användare med Microsoft Project License.**</span><span class="sxs-lookup"><span data-stu-id="82cb9-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="82cb9-673">De kan inte användas av:</span><span class="sxs-lookup"><span data-stu-id="82cb9-673">They can't be used by:</span></span>
    - <span data-ttu-id="82cb9-674">Programanvändare</span><span class="sxs-lookup"><span data-stu-id="82cb9-674">Application users</span></span>
    - <span data-ttu-id="82cb9-675">Systemanvändare</span><span class="sxs-lookup"><span data-stu-id="82cb9-675">System users</span></span>
    - <span data-ttu-id="82cb9-676">Integrationsanvändare</span><span class="sxs-lookup"><span data-stu-id="82cb9-676">Integration users</span></span>
    - <span data-ttu-id="82cb9-677">Andra användare som inte har den licens som krävs</span><span class="sxs-lookup"><span data-stu-id="82cb9-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="82cb9-678">Varje **OperationSet** kan endast ha högst 100 åtgärder.</span><span class="sxs-lookup"><span data-stu-id="82cb9-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="82cb9-679">Varje användare kan bara ha högst 10 öppna **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="82cb9-680">Project Operations stöder för närvarande maximalt 500 totala uppgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="82cb9-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="82cb9-681">**OperationSet** felstatus och felloggar är för närvarande inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="82cb9-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="82cb9-682">Gränser för projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="82cb9-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="82cb9-683">Felhantering</span><span class="sxs-lookup"><span data-stu-id="82cb9-683">Error handling</span></span>

   - <span data-ttu-id="82cb9-684">Om du vill granska fel som uppstått från Åtgärdsuppsättningar går du till **Inställningar** \> **Schemalägg integration** \> **Åtgärdsuppsättningar**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="82cb9-685">Om du vill granska fel som uppstått från tjänsten Projektschemaläggning går du till **Inställningar** \> **Schemalägg integration** \> **PSS-felloggar**.</span><span class="sxs-lookup"><span data-stu-id="82cb9-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="82cb9-686">Exempelscenario</span><span class="sxs-lookup"><span data-stu-id="82cb9-686">Sample scenario</span></span>

<span data-ttu-id="82cb9-687">I det här scenariot skapar du ett projekt, en teammedlem, fyra uppgifter och två resurstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="82cb9-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="82cb9-688">Nu ska du uppdatera en uppgift, uppdatera projektet, ta bort en uppgift, ta bort en resurstilldelning och skapa ett aktivitetsberoende.</span><span class="sxs-lookup"><span data-stu-id="82cb9-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="82cb9-689">Ytterligare exempel</span><span class="sxs-lookup"><span data-stu-id="82cb9-689">Additional samples</span></span>

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
