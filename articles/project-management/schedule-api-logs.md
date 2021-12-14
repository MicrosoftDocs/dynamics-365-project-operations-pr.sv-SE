---
title: Loggar för projektscheman
description: Detta ämne innehåller information och exempel som hjälper dig att använda loggarna för projektschemaläggning i syfte att spåra problem som är relaterade till API:er för projektschemaläggning och tjänsten Projektschemaläggning.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877640"
---
# <a name="project-scheduling-logs"></a>Loggar för projektscheman

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier, Lite-distribution – avtal med pro forma-fakturering,_, _Project for the Web_

Microsoft Dynamics 365 Project Operations använder [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) som primär schemaläggningsmotor. Istället för att använda standardprogrammeringsgränssnitt för Microsoft Dataverse-webbapplikationer (API:er) använder Project Operations de nya API:erna för Projektschemaläggning för att skapa, uppdatera och ta bort projektuppgifter, resurstilldelningar, uppgiftsberoenden, projektgrupper samt medlemmar i projektteam. När åtgärder för att skapa, uppdatera eller ta bort körs programmässigt på entiteter för uppdelad arbetsstruktur (WDS) kan emellertid fel uppstå. Två nya administrationsloggar har implementerats för att spåra dessa fel samt åtgärdshistoriken: **Åtgärdsuppsättning** och **Tjänsten Projektschemaläggning (PSS)**. Öppna dessa loggar genom att gå till **Inställningar** \> **Schemaintegrering**.

Följande bild visar datamodellen för produktschemaläggningsloggar.

![Datamodell för projektschemaläggningsloggar.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Loggen Åtgärdsuppsättning

Loggen åtgärdsuppsättning spårar körningen av en åtgärdsuppsättning som används för att köra en eller flera skapa-, uppdatera- eller ta bort-åtgärder i en grupp för projekt, projektuppgifter, resurstilldelningar, aktivitetsberoenden, projektgrupper eller projektteammedlemmar. I fältet **Åtgärd i status** visas den övergripande statusen för åtgärdsuppsättningen. Informationen i åtgärdsuppsättningens nyttolast registreras i relaterade detaljposter för åtgärdsuppsättningen.

### <a name="operation-set"></a>Åtgärdsuppsättning

I följande tabell visas de fält som är relaterade till entiteten **Åtgärdsuppsättning**.

| Schemanamn            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum/tid då åtgärdsuppsättningen slutfördes eller misslyckades.                                                | CompletedOn            |
| msdyn_correlationid   | Värdet **correlationId** för begäran.                                                                  | CorrelationId          |
| msdyn_description     | Beskrivningen av åtgärdsuppsättningen.                                                                        | Description            |
| msdyn_executedon      | Datum/tid då posten kördes.                                                                       | Kördes            |
| msdyn_operationsetId  | Unik identifierare för entitetsinstanser.                                                                   | OperationSet           |
| msdyn_Project         | Det projekt som är relaterat till åtgärdsuppsättningen.                                                            | Project                |
| msdyn_projectid       | Värdet **projectId** för begäran.                                                                      | ProjectId (inaktuellt) |
| msdyn_projectName     | Ej tillämpbart.                                                                                              | Gäller inte         |
| msdyn_PSSErrorLog     | Den unika identifieraren för felloggen för projektschemaläggningstjänsten som är associerad med åtgärdsuppsättningen. | PSS-fellogg          |
| msdyn_PSSErrorLogName | Ej tillämpbart.                                                                                              | Gäller inte         |
| msdyn_status          | Åtgärdsuppsättningens status.                                                                             | Status                 |
| msdyn_statusName      | Ej tillämpbart.                                                                                              | Gäller inte         |
| msdyn_useraadid       | Object-ID för Azure Active Directory (Azure AD) för den användare som begäran hör till.                     | UserAADID              |

### <a name="operation-set-detail"></a>Åtgärdsuppsättningsinformation

I följande tabell visas de fält som är relaterade till entiteten **Åtgärdsuppsättningsinformation**.

| Schemanamn                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serialiserade Dataverse-fält för begäran.                                            | CdsPayload            |
| msdyn_entityname           | Namnet på entiteten för begäran.                                                     | EntityName            |
| msdyn_httpverb             | Metoden för begäran.                                                                         | HTTP-verb (inaktuell) |
| msdyn_httpverbName         | Ej tillämpbart.                                                                             | Gäller inte        |
| msdyn_operationset         | Unik identifierare för den åtgärdsuppsättning som posten tillhör.                      | OperationSet          |
| msdyn_operationsetdetailId | Unik identifierare för entitetsinstanser.                                                  | OperationSet-information   |
| msdyn_operationsetName     | Ej tillämpbart.                                                                             | Gäller inte        |
| msdyn_operationtype        | Åtgärdstyp för information om åtgärdsuppsättning.                                             | OperationType         |
| msdyn_operationtypeName    | Ej tillämpbart.                                                                             | Gäller inte        |
| msdyn_psspayload           | De serialiserade fälten för tjänsten Projektschemaläggning för förfrågan.                           | PssPayload            |
| msdyn_recordid             | Identifierare för begärandeposten.                                                       | Post-ID             |
| msdyn_requestnumber        | Ett automatiskt genererat nummer som identifierar den ordning i vilken begärandena togs emot. | Nummer på begäran        |

## <a name="project-scheduling-service-error-logs"></a>Felloggar för tjänsten Projektschemaläggnning

Felloggarna för projektschemaläggningstjänsten visar fel som inträffar när projektschemaläggningstjänsten försöker utföra åtgärden **Spara** eller **Öppna**. Det finns tre scenarier som stöds där dessa loggar genereras:

- Användarinitierade åtgärder fungerar inte (en tilldelning kan till exempel inte skapas på grund av saknade behörigheter).
- Projektschemaläggningstjänsten kan inte programmässigt skapa, uppdatera, ta bort eller utföra någon annan kaskadåtgärd på en entitet.
- Användaren får felmeddelanden när en post inte kan öppnas (till exempel när ett projekt öppnas eller när en teammedlems information uppdateras).

### <a name="project-scheduling-service-log"></a>Logg för tjänsten för projektschemaläggning

I följande tabell visas de fält som omfattas av loggen för tjänsten Projektschemaläggning.

| Schemanamn          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Anropsstacken för undantaget.                                               | Anropsstack     |
| msdyn_correlationid | Felets korrelations-ID.                                               | CorrelationId  |
| msdyn_errorcode     | Ett fält som används för att lagra Dataverse-felkoden eller HTTP-felkoden. | Felkod     |
| msdyn_HelpLink      | En länk till den offentliga hjälpdokumentationen.                                       | Hjälplänk      |
| msdyn_log           | Loggen från tjänsten Projektschemaläggning.                                   | Logg            |
| msdyn_project       | Det projekt som är associerat med felloggen.                             | Project        |
| msdyn_projectName   | Namnet på projektet om nyttolasten för åtgärdsuppsättningen kommer att bevaras. | Gäller inte |
| msdyn_psserrorlogId | Unik identifierare för entitetsinstanser.                                     | PSS-fellogg  |
| msdyn_SessionId     | ID för projektsessionen.                                                        | Sessions-ID     |

## <a name="error-log-cleanup"></a>Rensning av fellogg

Som standard kan både felloggarna för projektschemaläggningstjänsten och loggen för åtgärdsuppsättningen rensas var 90:e dag. Alla poster som är äldre än 90 dagar tas bort. Genom att ändra värdet för fältet **msdyn_StateOperationSetAge** på sidan **Projektparametrar** kan administratörer emellertid justera rensningsintervallet så att detta ligger på mellan 1 och 120 dagar. Flera metoder för att ändra detta värde är tillgängliga:

- Anpassa entiteten **Projektparameter** genom att skapa en anpassad sida och lägga till fältet **Ålder för inaktuell åtgärdsuppsättning**.
- Använd klientkod som använder [Programvaruutvecklingsverktyg för WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Använd Service SDK-kod som använder Xrm SDK-metoden **updateRecord** (referens för klient-API) i modellbaserade appar. Power Apps innehåller en beskrivning och parametrar som stöds för metoden **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
