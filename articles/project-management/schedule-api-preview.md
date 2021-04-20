---
title: Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter
description: Detta ämne innehåller information och exempel för användning av schemaläggnings-API:er.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868151"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="ae7bc-103">Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="ae7bc-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="ae7bc-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="ae7bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="ae7bc-105">Vissa eller alla funktioner som anges i det här ämnet är tillgängliga som en del av en förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="ae7bc-106">Innehållet och funktionerna kan komma att ändras.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="ae7bc-107">Schemaläggningsentiteter</span><span class="sxs-lookup"><span data-stu-id="ae7bc-107">Scheduling entities</span></span>

<span data-ttu-id="ae7bc-108">Schemalägg API:er så att du kan skapa, uppdatera och ta bort åtgärder med **schemaläggningsentiteter**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="ae7bc-109">Dessa entiteter hanteras med schemaläggningsmotorn i Projekt för webben.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="ae7bc-110">Skapa, uppdatera och ta bort operationer med **Schemaläggningsentiteter** begränsades i tidigare versioner av Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="ae7bc-111">I följande tabell visas en fullständig lista över **Schemaläggningsentiteterna**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="ae7bc-112">Entitetsnamn</span><span class="sxs-lookup"><span data-stu-id="ae7bc-112">Entity name</span></span>  | <span data-ttu-id="ae7bc-113">Entitetens logiska namn</span><span class="sxs-lookup"><span data-stu-id="ae7bc-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="ae7bc-114">Project</span><span class="sxs-lookup"><span data-stu-id="ae7bc-114">Project</span></span> | <span data-ttu-id="ae7bc-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ae7bc-115">msdyn_project</span></span> |
| <span data-ttu-id="ae7bc-116">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="ae7bc-116">Project Task</span></span>  | <span data-ttu-id="ae7bc-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="ae7bc-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="ae7bc-118">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="ae7bc-118">Project Task Dependency</span></span>  | <span data-ttu-id="ae7bc-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="ae7bc-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="ae7bc-120">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="ae7bc-120">Resource Assignment</span></span> | <span data-ttu-id="ae7bc-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="ae7bc-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="ae7bc-122">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="ae7bc-122">Project Bucket</span></span>  | <span data-ttu-id="ae7bc-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="ae7bc-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="ae7bc-124">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="ae7bc-124">Project Team Member</span></span> | <span data-ttu-id="ae7bc-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="ae7bc-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="ae7bc-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="ae7bc-126">OperationSet</span></span>

<span data-ttu-id="ae7bc-127">OperationSet är ett enhetsmönster som kan användas när flera schemapåverkande förfrågningar måste bearbetas inom en transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="ae7bc-128">Schemaläggning-API:er</span><span class="sxs-lookup"><span data-stu-id="ae7bc-128">Schedule APIs</span></span>

<span data-ttu-id="ae7bc-129">Följande är en lista med aktuella schemaläggning-API:er.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="ae7bc-130">**msdyn_CreateProjectV1**: Detta API kan användas för att skapa ett projekt.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="ae7bc-131">Projekt och standardprojektgrupp skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="ae7bc-132">**msdyn_CreateTeamMemberV1**: Detta API kan användas för att skapa en projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="ae7bc-133">Teammedlemsposten skapas direkt.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="ae7bc-134">**msdyn_CreateOperationSetV1**: Detta API kan användas för att schemalägga flera förfrågningar som måste utföras inom en transaktionen.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="ae7bc-135">**msdyn_PSSCreateV1**: Det här API:et kan användas för att skapa en entitet.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="ae7bc-136">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden skapa.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="ae7bc-137">**msdyn_PSSUpdateV1**: Det här API:et kan användas för att uppdatera en entitet.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="ae7bc-138">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden uppdatera.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="ae7bc-139">**msdyn_PSSDeleteV1**: Det här API:et kan användas för att ta bort en entitet.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="ae7bc-140">Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden ta bort.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="ae7bc-141">**msdyn_ExecuteOperationSetV1**: Detta API används för att köra alla åtgärder inom den angivna åtgärdsuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="ae7bc-142">Använda schemaläggnings-API:er med OperationSet</span><span class="sxs-lookup"><span data-stu-id="ae7bc-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="ae7bc-143">Eftersom poster med både **CreateProjectV1** och **CreateTeamMemberV1** skapas direkt kan dessa API:er inte användas direkt i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="ae7bc-144">Men du kan använda API för att skapa nödvändiga poster, skapa en **OperationSet** och sedan använda dessa förskapade poster i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="ae7bc-145">Åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="ae7bc-145">Supported operations</span></span>

| <span data-ttu-id="ae7bc-146">Schemaläggningsentitet</span><span class="sxs-lookup"><span data-stu-id="ae7bc-146">Scheduling entity</span></span> | <span data-ttu-id="ae7bc-147">Skapa</span><span class="sxs-lookup"><span data-stu-id="ae7bc-147">Create</span></span> | <span data-ttu-id="ae7bc-148">Uppdatering</span><span class="sxs-lookup"><span data-stu-id="ae7bc-148">Update</span></span> | <span data-ttu-id="ae7bc-149">Delete</span><span class="sxs-lookup"><span data-stu-id="ae7bc-149">Delete</span></span> | <span data-ttu-id="ae7bc-150">Viktigt!</span><span class="sxs-lookup"><span data-stu-id="ae7bc-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="ae7bc-151">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="ae7bc-151">Project task</span></span> | <span data-ttu-id="ae7bc-152">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-152">Yes</span></span> | <span data-ttu-id="ae7bc-153">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-153">Yes</span></span> | <span data-ttu-id="ae7bc-154">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-154">Yes</span></span> | <span data-ttu-id="ae7bc-155">Nej</span><span class="sxs-lookup"><span data-stu-id="ae7bc-155">None</span></span> |
| <span data-ttu-id="ae7bc-156">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="ae7bc-156">Project task dependency</span></span> | <span data-ttu-id="ae7bc-157">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-157">Yes</span></span> | <span data-ttu-id="ae7bc-158">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-158">Yes</span></span> | | <span data-ttu-id="ae7bc-159">Poster för projektuppgiftsberoende uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="ae7bc-160">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ae7bc-161">Resurstilldelning</span><span class="sxs-lookup"><span data-stu-id="ae7bc-161">Resource assignment</span></span> | <span data-ttu-id="ae7bc-162">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-162">Yes</span></span> | <span data-ttu-id="ae7bc-163">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-163">Yes</span></span> | | <span data-ttu-id="ae7bc-164">Operationer med följande fält stöds inte: **BookableResourceID**, **Insats**, **EffortCompleted**, **EffortRemaining** och **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="ae7bc-165">Resurstilldelningsposter uppdateras inte.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="ae7bc-166">I stället kan du ta bort en äldre post och skapa en ny post.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ae7bc-167">Projektgrupp</span><span class="sxs-lookup"><span data-stu-id="ae7bc-167">Project bucket</span></span> | <span data-ttu-id="ae7bc-168">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ae7bc-168">N/A</span></span> | <span data-ttu-id="ae7bc-169">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ae7bc-169">N/A</span></span> | <span data-ttu-id="ae7bc-170">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ae7bc-170">N/A</span></span> | <span data-ttu-id="ae7bc-171">Standardgruppen skapas för att använda API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="ae7bc-172">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="ae7bc-172">Project team member</span></span> | <span data-ttu-id="ae7bc-173">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-173">Yes</span></span> | <span data-ttu-id="ae7bc-174">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-174">Yes</span></span> | <span data-ttu-id="ae7bc-175">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-175">Yes</span></span> | <span data-ttu-id="ae7bc-176">För att skapa operation, använda API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="ae7bc-177">Project</span><span class="sxs-lookup"><span data-stu-id="ae7bc-177">Project</span></span> | <span data-ttu-id="ae7bc-178">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-178">Yes</span></span> | <span data-ttu-id="ae7bc-179">Ja</span><span class="sxs-lookup"><span data-stu-id="ae7bc-179">Yes</span></span> | <span data-ttu-id="ae7bc-180">Inte tillgängligt</span><span class="sxs-lookup"><span data-stu-id="ae7bc-180">N/A</span></span> | <span data-ttu-id="ae7bc-181">Operationer med följande fält stöds inte: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Insats**, **EffortCompleted**, **EffortRemaining**, **Förlopp**, **Slutför**, **TaskEarliestStart** och **Varaktighet**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="ae7bc-182">Dessa API:er kan anropas med entitetsobjekt som innehåller anpassade fält.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="ae7bc-183">ID-egenskapen är valfri.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-183">The ID property is optional.</span></span> <span data-ttu-id="ae7bc-184">Om det finns ett undantag försöker systemet använda det och ett undantag om det inte kan användas.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="ae7bc-185">Om den inte finns genererar systemet den.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="ae7bc-186">Begränsningar och kända problem</span><span class="sxs-lookup"><span data-stu-id="ae7bc-186">Limitations and known issues</span></span>
<span data-ttu-id="ae7bc-187">Följande är en lista med begränsningar och kända problem:</span><span class="sxs-lookup"><span data-stu-id="ae7bc-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="ae7bc-188">Schema-API:er kan endast användas av **Användare med Microsoft Project License.**</span><span class="sxs-lookup"><span data-stu-id="ae7bc-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="ae7bc-189">De kan inte användas av:</span><span class="sxs-lookup"><span data-stu-id="ae7bc-189">They can't be used by:</span></span>
    - <span data-ttu-id="ae7bc-190">Programanvändare</span><span class="sxs-lookup"><span data-stu-id="ae7bc-190">Application users</span></span>
    - <span data-ttu-id="ae7bc-191">Systemanvändare</span><span class="sxs-lookup"><span data-stu-id="ae7bc-191">System users</span></span>
    - <span data-ttu-id="ae7bc-192">Integrationsanvändare</span><span class="sxs-lookup"><span data-stu-id="ae7bc-192">Integration users</span></span>
    - <span data-ttu-id="ae7bc-193">Andra användare som inte har den licens som krävs</span><span class="sxs-lookup"><span data-stu-id="ae7bc-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="ae7bc-194">Varje **OperationSet** kan endast ha högst 100 åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="ae7bc-195">Varje användare kan bara ha högst 10 öppna **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="ae7bc-196">Project Operations stöder för närvarande maximalt 500 totala uppgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="ae7bc-197">**OperationSet** felstatus och felloggar är för närvarande inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="ae7bc-198">Schemaläggnings-API:er är i offentlig förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="ae7bc-199">Microsoft har inte stöd för att använda dessa API:er i en produktionsmiljö.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="ae7bc-200">Exempelscenario</span><span class="sxs-lookup"><span data-stu-id="ae7bc-200">Sample scenario</span></span>

<span data-ttu-id="ae7bc-201">I det här scenariot skapar du ett projekt, en teammedlem, fyra uppgifter och två resurstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="ae7bc-202">Nu ska du uppdatera en uppgift, uppdatera projektet, ta bort en uppgift, ta bort en resurstilldelning och skapa ett aktivitetsberoende.</span><span class="sxs-lookup"><span data-stu-id="ae7bc-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="ae7bc-203">Ytterligare exempel</span><span class="sxs-lookup"><span data-stu-id="ae7bc-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
