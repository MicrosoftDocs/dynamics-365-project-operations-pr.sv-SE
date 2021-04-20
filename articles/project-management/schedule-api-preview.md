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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Använd schema-API:er för att utföra åtgärder med schemaläggningsentiteter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

> [!IMPORTANT] 
> Vissa eller alla funktioner som anges i det här ämnet är tillgängliga som en del av en förhandsversion. Innehållet och funktionerna kan komma att ändras. 

## <a name="scheduling-entities"></a>Schemaläggningsentiteter

Schemalägg API:er så att du kan skapa, uppdatera och ta bort åtgärder med **schemaläggningsentiteter**. Dessa entiteter hanteras med schemaläggningsmotorn i Projekt för webben. Skapa, uppdatera och ta bort operationer med **Schemaläggningsentiteter** begränsades i tidigare versioner av Dynamics 365 Project Operations.

I följande tabell visas en fullständig lista över **Schemaläggningsentiteterna**.

| Entitetsnamn  | Entitetens logiska namn |
| --- | --- |
| Project | msdyn_project |
| Projektuppgift  | msdyn_projecttask  |
| Beroende för projektuppgift  | msdyn_projecttaskdependency  |
| Resurstilldelning | msdyn_resourceassignment |
| Projektgrupp  | msdyn_projectbucket |
| Projektteammedlem | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet är ett enhetsmönster som kan användas när flera schemapåverkande förfrågningar måste bearbetas inom en transaktioner.

## <a name="schedule-apis"></a>Schemaläggning-API:er

Följande är en lista med aktuella schemaläggning-API:er.

- **msdyn_CreateProjectV1**: Detta API kan användas för att skapa ett projekt. Projekt och standardprojektgrupp skapas direkt.
- **msdyn_CreateTeamMemberV1**: Detta API kan användas för att skapa en projektteammedlem. Teammedlemsposten skapas direkt.
- **msdyn_CreateOperationSetV1**: Detta API kan användas för att schemalägga flera förfrågningar som måste utföras inom en transaktionen.
- **msdyn_PSSCreateV1**: Det här API:et kan användas för att skapa en entitet. Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden skapa.
- **msdyn_PSSUpdateV1**: Det här API:et kan användas för att uppdatera en entitet. Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden uppdatera.
- **msdyn_PSSDeleteV1**: Det här API:et kan användas för att ta bort en entitet. Entiteten kan vara någon av de schemaläggningsentiteter som har stöd för åtgärden ta bort.
- **msdyn_ExecuteOperationSetV1**: Detta API används för att köra alla åtgärder inom den angivna åtgärdsuppsättningen.

## <a name="using-schedule-apis-with-operationset"></a>Använda schemaläggnings-API:er med OperationSet

Eftersom poster med både **CreateProjectV1** och **CreateTeamMemberV1** skapas direkt kan dessa API:er inte användas direkt i **OperationSet**. Men du kan använda API för att skapa nödvändiga poster, skapa en **OperationSet** och sedan använda dessa förskapade poster i **OperationSet**.

## <a name="supported-operations"></a>Åtgärder som stöds

| Schemaläggningsentitet | Skapa | Uppdatering | Delete | Viktigt! |
| --- | --- | --- | --- | --- |
Projektuppgift | Ja | Ja | Ja | Nej |
| Beroende för projektuppgift | Ja | Ja | | Poster för projektuppgiftsberoende uppdateras inte. I stället kan du ta bort en äldre post och skapa en ny post. |
| Resurstilldelning | Ja | Ja | | Operationer med följande fält stöds inte: **BookableResourceID**, **Insats**, **EffortCompleted**, **EffortRemaining** och **PlannedWork**. Resurstilldelningsposter uppdateras inte. I stället kan du ta bort en äldre post och skapa en ny post. |
| Projektgrupp | Inte tillgängligt | Inte tillgängligt | Inte tillgängligt | Standardgruppen skapas för att använda API **CreateProjectV1**. |
| Projektteammedlem | Ja | Ja | Ja | För att skapa operation, använda API **CreateTeamMemberV1**. |
| Project | Ja | Ja | Inte tillgängligt | Operationer med följande fält stöds inte: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Insats**, **EffortCompleted**, **EffortRemaining**, **Förlopp**, **Slutför**, **TaskEarliestStart** och **Varaktighet**. |

Dessa API:er kan anropas med entitetsobjekt som innehåller anpassade fält.

ID-egenskapen är valfri. Om det finns ett undantag försöker systemet använda det och ett undantag om det inte kan användas. Om den inte finns genererar systemet den.

## <a name="limitations-and-known-issues"></a>Begränsningar och kända problem
Följande är en lista med begränsningar och kända problem:

- Schema-API:er kan endast användas av **Användare med Microsoft Project License.** De kan inte användas av:
    - Programanvändare
    - Systemanvändare
    - Integrationsanvändare
    - Andra användare som inte har den licens som krävs
- Varje **OperationSet** kan endast ha högst 100 åtgärder.
- Varje användare kan bara ha högst 10 öppna **OperationSets**.
- Project Operations stöder för närvarande maximalt 500 totala uppgifter för ett projekt.
- **OperationSet** felstatus och felloggar är för närvarande inte tillgängliga.
- Schemaläggnings-API:er är i offentlig förhandsversion. Microsoft har inte stöd för att använda dessa API:er i en produktionsmiljö.

## <a name="sample-scenario"></a>Exempelscenario

I det här scenariot skapar du ett projekt, en teammedlem, fyra uppgifter och två resurstilldelningar. Nu ska du uppdatera en uppgift, uppdatera projektet, ta bort en uppgift, ta bort en resurstilldelning och skapa ett aktivitetsberoende.

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

## <a name="additional-samples"></a>Ytterligare exempel

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
