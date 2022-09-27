---
title: Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter
description: Den här artikeln innehåller information och exempel på hur du använder API:er för projektschema.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541147"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


**Schemaläggningsentiteter**

API:er för projektschemaläggning gör det möjligt att skapa, uppdatera och ta bort åtgärder med **Schemaläggningsentiteter**. Dessa entiteter hanteras med schemaläggningsmotorn i Project for the Web. Skapa, uppdatera och ta bort operationer med **Schemaläggningsentiteter** begränsades i tidigare versioner av Dynamics 365 Project Operations.

I följande tabell visas en fullständig lista över entiteterna i projektschemat.

| **Entitetsnamn**         | **Entitetens logiska namn**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektuppgift            | msdyn_projecttask           |
| Beroende för projektuppgift | msdyn_projecttaskdependency |
| Resurstilldelning     | msdyn_resourceassignment    |
| Projektgrupp          | msdyn_projectbucket         |
| Projektgruppmedlem     | msdyn_projectteam           |
| Projektchecklistor      | msdyn_projectchecklist      |
| Projektetikett           | msdyn_projectlabel          |
| Projektuppgift till etikett   | msdyn_projecttasktolabel    |
| Projektsprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet är ett enhetsmönster som kan användas när flera schemapåverkande förfrågningar måste bearbetas inom en transaktioner.

**Projekttidsplan-API**

Följande är en lista med aktuella API:er för Projektschema.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Detta API används för att skapa ett projekt. Projekt och bucket för standardprojekt skapas direkt.                         |
| **msdyn_CreateTeamMemberV1**            | Detta API används för att skapa en teammedlem. Teammedlemsposten skapas direkt.                                  |
| **msdyn_CreateOperationSetV1**          | Detta API används för att schemalägga flera förfrågningar som måste utföras inom en transaktionen.                                        |
| **msdyn_PssCreateV1**                   | Detta API används för att skapa en enhet. Entiteten kan vara någon av de projektschemaläggningsentiteter som stöder åtgärden skapa. |
| **msdyn_PssUpdateV1**                   | Detta API används för att uppdatera en enhet. Entiteten kan vara någon av de projektschemaläggningsentiteter som stöder åtgärden uppdatera  |
| **msdyn_PssDeleteV1**                   | Detta API används för att ta bort en enhet. Entiteten kan vara någon av de projektschemaläggningsentiteter som stöder åtgärden ta bort. |
| **msdyn_ExecuteOperationSetV1**         | Detta API används för att köra alla åtgärder inom den angivna åtgärdsuppsättningen.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Detta API används för att uppdatera ett planerat arbete för resurstilldelning.                                                        |



**Använda API:er för Projektscheman med OperationSet**

Eftersom poster med både **CreateProjectV1** och **CreateTeamMemberV1** skapas direkt kan dessa API:er inte användas direkt i **OperationSet**. Men du kan använda API för att skapa nödvändiga poster, skapa en **OperationSet** och sedan använda dessa förskapade poster i **OperationSet**.

**Åtgärder som stöds**

| **Schemaläggningsentitet**   | **Skapa** | **Update** | **Delete** | **Viktigt!**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektuppgift            | Ja        | Ja        | Ja        | Fälten **Förlopp**, **EffortCompleted** och **EffortRemaining** kan redigeras i Project for the Web, men de kan inte redigeras i Project Operations.                                                                                                                                                                                             |
| Beroende för projektuppgift | Ja        | No         | Ja        | Poster för projektuppgiftsberoende uppdateras inte. Istället kan du ta bort en äldre post och skapa en ny post.                                                                                                                                                                                                                                 |
| Resurstilldelning     | Ja        | Ja\*      | Ja        | Operationer med följande fält stöds inte: **BookableResourceID**, **Insats**, **EffortCompleted**, **EffortRemaining** och **PlannedWork**. Resurstilldelningsposter uppdateras inte. Istället kan den äldre posten tas bort och en ny skapas. Ett separat API har angetts för att uppdatera resurstilldelning rekommendationer. |
| Projektgrupp          | Ja        | Ja        | Ja        | Bycket för standardvärde skapas med hjälp av API:n för **CreateProjectV1**. I uppdateringsversion 16 lades stöd för att skapa och ta bort projektbuckets till.                                                                                                                                                                                                   |
| Projektteammedlem     | Ja        | Ja        | Ja        | För att skapa operation, använda API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ja        | Ja        |            | Operationer med följande fält stöds inte: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Insats**, **EffortCompleted**, **EffortRemaining**, **Förlopp**, **Slutför**, **TaskEarliestStart** och **Varaktighet**.                                                                                       |
| Projektchecklistor      | Ja        | Ja        | Ja        |                                                                                                                                                                                                                                                                                                                                                         |
| Projektetikett           | No         | Ja        | No         | Etikettnamn kan ändras. Den här funktionen finns endast för Project for the Web                                                                                                                                                                                                                                                                      |
| Projektuppgift till etikett   | Ja        | No         | Ja        | Den här funktionen finns endast för Project for the Web                                                                                                                                                                                                                                                                                                  |
| Projektsprint          | Ja        | Ja        | Ja        | Fältet **Start** måste ha ett tidigare datum än fältet **Slutför**. En del projekt kan inte överlappa varandra. Den här funktionen finns endast för Project for the Web                                                                                                                                                                    |




ID-egenskapen är valfri. Om det finns ett undantag försöker systemet använda det och ett undantag om det inte kan användas. Om den inte finns genererar systemet den.

**Begränsningar och kända problem**

Följande är en lista med begränsningar och kända problem:

-   API:er för projektscheman kan endast användas av **användare med Microsoft Project-licens**. De kan inte användas av:
    -   Programanvändare
    -   Systemanvändare
    -   Integrationsanvändare
    -   Andra användare som inte har den licens som krävs
-   Varje **OperationSet** kan endast ha högst 100 åtgärder.
-   Varje användare kan bara ha högst 10 öppna **OperationSets**.
-   Project Operations stöder för närvarande maximalt 500 totala uppgifter för ett projekt.
-   Varje åtgärd som uppdaterar resurstilldelningstilldelning räknas som en enskild åtgärd.
-   Varje lista med uppdaterade uppdateringar kan innehålla högst 100 gånger.
-   **OperationSet** felstatus och felloggar är för närvarande inte tillgängliga.
-   Det finns maximalt 400 antal per projekt.
-   [Gränser för projekt och uppgifter](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Etiketter är för närvarande finns endast för Project for the Web.

**Felhantering**

-   Om du vill granska fel som uppstått från Åtgärdsuppsättningar går du till **Inställningar** \> **Schemalägg integration** \> **Åtgärdsuppsättningar**.
-   Om du vill granska fel som genererats från projektplaneringstjänsten, gå till **Inställningar** \> **Schemaläggningsintegrering** \> **PSS felloggar**.

**Redigera resurstilldelningsprofiler**

Till skillnad från alla andra API:er för projektschemaläggning som uppdaterar en entitet, är API för resurstilldelning på egen hand ansvarig för uppdateringar av ett enskilt fält, msdyn_plannedwork, på en enda entitet, msydn_resourceassignment.

Schemaläget är:

-   **fasta enheter**
-   projektkalendern är 9-5p är 9-5pst, mån, tis, tors, fre (INGEN ARBETE ONSDAGAR)
-   Och resurskalendern är 9-1p PST mån till fre

Tilldelningen gäller i en vecka, fyra timmar per dag. Detta beror på att resurskalendern är från 9 till 1 PST eller fyra timmar per dag.

| &nbsp;     | Aktivitet | Startdatum | Slutdatum  | Kvantitet | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 Arbetare |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Om du till exempel vill att arbetaren bara ska arbeta tre timmar varje dag den här veckan och tillåta en timme för andra uppgifter.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours exempel på nyttolast:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Det här är tilldelningen efter att API:et för uppdatering av schemauppdateringen har körts.

| &nbsp;     | Aktivitet | Startdatum | Slutdatum  | Kvantitet | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 Arbetare | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Exempelscenario**

I det här scenariot skapar du ett projekt, en teammedlem, fyra uppgifter och två resurstilldelningar. Nu ska du uppdatera en uppgift, uppdatera projektet, ta bort en uppgift, ta bort en resurstilldelning och skapa ett aktivitetsberoende.

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

** Ytterligare exempel

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
