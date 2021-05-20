---
title: Ta fram projektmallar med Kopiera projekt
description: I det här ämnet finns information om hur du skapar projektmallar med den anpassade åtgärden Kopiera projekt.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949836"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="1d3ff-103">Ta fram projektmallar med Kopiera projekt</span><span class="sxs-lookup"><span data-stu-id="1d3ff-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="1d3ff-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="1d3ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1d3ff-105">Dynamics 365 Project Operations stöder möjligheten att kopiera ett projekt och återställa eventuella tilldelningar till de generiska resurser som representerar rollen.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="1d3ff-106">Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="1d3ff-107">När du väljer **Kopiera projekt** uppdateras statusen för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="1d3ff-108">Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="1d3ff-109">Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="1d3ff-110">Den anpassade åtgärden Kopiera projekt</span><span class="sxs-lookup"><span data-stu-id="1d3ff-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="1d3ff-111">Namn</span><span class="sxs-lookup"><span data-stu-id="1d3ff-111">Name</span></span> 

<span data-ttu-id="1d3ff-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="1d3ff-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="1d3ff-113">Indataparametrar</span><span class="sxs-lookup"><span data-stu-id="1d3ff-113">Input parameters</span></span>
<span data-ttu-id="1d3ff-114">Det finns tre indataparametrar:</span><span class="sxs-lookup"><span data-stu-id="1d3ff-114">There are three input parameters:</span></span>

| <span data-ttu-id="1d3ff-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d3ff-115">Parameter</span></span>          | <span data-ttu-id="1d3ff-116">Typ</span><span class="sxs-lookup"><span data-stu-id="1d3ff-116">Type</span></span>   | <span data-ttu-id="1d3ff-117">Värden</span><span class="sxs-lookup"><span data-stu-id="1d3ff-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="1d3ff-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="1d3ff-118">ProjectCopyOption</span></span>  | <span data-ttu-id="1d3ff-119">Sträng</span><span class="sxs-lookup"><span data-stu-id="1d3ff-119">String</span></span> | <span data-ttu-id="1d3ff-120">**{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="1d3ff-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="1d3ff-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="1d3ff-121">SourceProject</span></span>      | <span data-ttu-id="1d3ff-122">Entitetsreferens</span><span class="sxs-lookup"><span data-stu-id="1d3ff-122">Entity Reference</span></span> | <span data-ttu-id="1d3ff-123">Källprojekt</span><span class="sxs-lookup"><span data-stu-id="1d3ff-123">Source Project</span></span> |
| <span data-ttu-id="1d3ff-124">Mål</span><span class="sxs-lookup"><span data-stu-id="1d3ff-124">Target</span></span>             | <span data-ttu-id="1d3ff-125">Entitetsreferens</span><span class="sxs-lookup"><span data-stu-id="1d3ff-125">Entity Reference</span></span> | <span data-ttu-id="1d3ff-126">Målprojekt</span><span class="sxs-lookup"><span data-stu-id="1d3ff-126">Target Project</span></span> |


- <span data-ttu-id="1d3ff-127">**{"clearTeamsAndAssignments":true}**: Tre standardbeteenden för Project for the Web och tar bort alla tilldelningar och gruppmedlemmar.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="1d3ff-128">**{"removeNamedResources":true}** Standardbeteendet för Project Operations och återställer tilldelningar till generiska resurser.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="1d3ff-129">Mer standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="1d3ff-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="1d3ff-130">Specificera vilka fält som ska kopieras</span><span class="sxs-lookup"><span data-stu-id="1d3ff-130">Specify fields to copy</span></span> 
<span data-ttu-id="1d3ff-131">När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="1d3ff-132">Exempel</span><span class="sxs-lookup"><span data-stu-id="1d3ff-132">Example</span></span>
<span data-ttu-id="1d3ff-133">Följande exempel visar hur du anropar den anpassade åtgärden **CopyProject** med parameteruppsättningen **removeNaedResources**.</span><span class="sxs-lookup"><span data-stu-id="1d3ff-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]