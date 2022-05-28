---
title: Ta fram projektmallar med Kopiera projekt
description: I det här ämnet finns information om hur du skapar projektmallar med den anpassade åtgärden Kopiera projekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590923"
---
# <a name="develop-project-templates-with-copy-project"></a>Ta fram projektmallar med Kopiera projekt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations stöder möjligheten att kopiera ett projekt och återställa eventuella tilldelningar till de generiska resurser som representerar rollen. Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.

När du väljer **Kopiera projekt** uppdateras statusen för målprojektet. Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar. Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.

## <a name="copy-project-custom-action"></a>Den anpassade åtgärden Kopiera projekt

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Indataparametrar

Det finns tre indataparametrar:

- **ReplaceNamedResources** eller **ClearTeamsAndAssignments** – Ange endast ett av dessa alternativ. Ange inte båda.

    - **\{"ReplaceNamallResources":true\}** – Standardbeteendet för Project Operations. Eventuella angivna resurser ersätts av allmänna resurser.
    - **\{"ClearTeamsAndAssignments":true\}** – Standardbeteendet för Project for the Web. Alla tilldelningar och teammedlemmar tas bort.

- **SourceProject** – Entitetsreferensen för det källprojekt som ska kopieras från. Denna parameter får inte vara noll.
- **Mål** – Entitetsreferensen för det målprojekt som ska kopieras till. Denna parameter får inte vara noll.

Följande tabell innehåller en sammanfattning av de tre parametrarna.

| Parameter                | Type             | Värde                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Sant** eller **Falskt** |
| ClearTeamsAndAssignments | Boolean          | **Sant** eller **Falskt** |
| SourceProject            | Entitetsreferens | Källprojekt    |
| Target                   | Entitetsreferens | Målprojekt    |

Fler standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

### <a name="validations"></a>Valideringar

Följande valideringar är klara.

1. "Noll" kontrollerar och hämtar käll- och målprojekt för att bekräfta att båda projekt finns inom organisationen.
2. Systemet verifierar att målprojektet är giltigt för kopiering genom att kontrollera följande villkor:

    - Det finns ingen föregående aktivitet i projektet (inklusive urval av fliken **Uppgifter**), och projektet är nyskapat.
    - Det finns ingen föregående kopia, ingen import har begärts för det här projektet, och projektet har inte statusen **Misslyckades**.

3. Åtgärden anropas inte med hjälp av HTTP.

## <a name="specify-fields-to-copy"></a>Specificera vilka fält som ska kopieras

När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.

### <a name="example"></a>Exempel

Följande exempel visar hur du anropar den anpassade åtgärden **CopyProjectV3** med parameteruppsättningen **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
