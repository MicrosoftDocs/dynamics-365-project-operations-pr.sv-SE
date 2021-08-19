---
title: Ta fram projektmallar med Kopiera projekt
description: I det här ämnet finns information om hur du skapar projektmallar med den anpassade åtgärden Kopiera projekt.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d12301b4e7baabeb0f045f9a11d4695fc026339af3fa7650db7177c495c71e90
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989297"
---
# <a name="develop-project-templates-with-copy-project"></a>Ta fram projektmallar med Kopiera projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations stöder möjligheten att kopiera ett projekt och återställa eventuella tilldelningar till de generiska resurser som representerar rollen. Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.

När du väljer **Kopiera projekt** uppdateras statusen för målprojektet. Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar. Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.

## <a name="copy-project-custom-action"></a>Den anpassade åtgärden Kopiera projekt 

### <a name="name"></a>Namn 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Indataparametrar
Det finns tre indataparametrar:

| Parameter          | Typ   | Värden                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Sträng | **{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entitetsreferens | Källprojekt |
| Mål             | Entitetsreferens | Målprojekt |


- **{"clearTeamsAndAssignments":true}**: Tre standardbeteenden för Project for the Web och tar bort alla tilldelningar och gruppmedlemmar.
- **{"removeNamedResources":true}** Standardbeteendet för Project Operations och återställer tilldelningar till generiska resurser.

Mer standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Specificera vilka fält som ska kopieras 
När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.


### <a name="example"></a>Exempel
Följande exempel visar hur du anropar den anpassade åtgärden **CopyProject** med parameteruppsättningen **removeNaedResources**.
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