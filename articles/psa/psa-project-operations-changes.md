---
title: Funktionsändringar från Project Service Automation till Project Operations
description: Denna artikel innehåller en översikt över funktionsändringar från Project Service Automation till Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925372"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funktionsändringar från Project Service Automation till Project Operations

Uppgraderingen från Dynamics 365 Project Service Automation till Dynamics 365 Project Operations Lite levereras i tre faser. Denna artikel innehåller information om de större förändringar du kan förvänta dig när uppgraderingen är slutförd.

| Uppgraderingsleverans | Fas 1 <br>(januari 2022) | Fas 2 <br>(lanseringsvåg i april 2022) | Fas 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Inget beroende av uppdelad arbetsstruktur (WBS) för projekt. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS omfattas av de gränser som för närvarande stöds för Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS utanför de för närvarande stödda begränsningarna för Project Operations, inklusive stöd för Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektledning

De viktigaste förändringarna i användarupplevelsen kommer att finnas på projektplaneringsområdet. Project Operations har en ny modern för att hantera en uppdelad arbetsstruktur (work breakdown structure, WBS) genom att utnyttja de schemaläggningsfunktioner som [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) tillhandahåller.

## <a name="differences-in-the-scheduling-experience"></a>Skillnader i schemaläggningsupplevelsen

I följande tabell sammanfattas schemaläggningsskillnaderna mellan Project Service Automation och Project Operations.

|  Schemaläggning     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektmallar – Möjlighet att definiera och använda projektmallar när ett projekt skapas  |  &nbsp;    | :heavy_check_mark: |
| Projektintegrering av uppdelad arbetsstruktur (WBS) med stationär klient   |    &nbsp;  | :heavy_check_mark: |
| Begränsningar – Starta inte tidigare än, slutför senast  | :heavy_check_mark: |   &nbsp;  |
| Milstolpar – Uppgifter med noll varaktighet   | :heavy_check_mark:  |  &nbsp;  |
| Resursdrivna uppgifter följer tillgängligheten för tilldelade resurser   | :heavy_check_mark: |  &nbsp;    |
| Tidsfasad redigering – Redigera scheman och arbete på daglig basis   |   &nbsp;  | :heavy_check_mark: |
| Automatisk/manuell schemaläggning – Använd motorn för projektschemaläggning för att automatiskt eller manuellt schemalägga uppgifter |  &nbsp; | :heavy_check_mark:  |
| Redigera stora projekt direkt i användargränssnittet: Det finns ingen begränsning för storleken på scheman som kan redigeras  | Uppgiftsbegränsning 500  | :heavy_check_mark:       |
| Slutförd procent – Markera uppgiftsförloppet   | :heavy_check_mark:  |  &nbsp;  |
| [Projektschemalägen](../project-management/scheduling-modes.md) – Definiera projektet som fasta enheter, fast insats eller fast varaktighet | :heavy_check_mark: | &nbsp; |
| Tidslinje – Skapa och anpassa tidslinjevyn för att visualisera schemainformation och kommunicera med intressenter. | :heavy_check_mark:  | &nbsp; |
| Insatsdrivna uppgifter – Schemaläggning av motorns stöd för schemaläggning av en uppgift som insatsbaserad  | :heavy_check_mark:  | &nbsp; |
| Dialogrutan **Uppgiftsinformation** – Spara uppgiftsinformation med hjälp av en dialogruta | :heavy_check_mark:  |  &nbsp;  |
| Dra och släpp – Välj flera uppgifter och ändra deras position på WBS | :heavy_check_mark: | &nbsp;  |
| Flexibla, återkommande vyer – Definiera mer detaljerade vyer över uppgiftsattribut   | :heavy_check_mark:  | &nbsp; |
| Sortera och filtrera WBS  | :heavy_check_mark:  | &nbsp; |
| Tavelvy för projektleverans av icke-vattenfallsprojekt  | :heavy_check_mark:   | &nbsp; |
| Tidslinjevy - Interaktivt Gantt-schema som används för att åskådliggöra och redigera WBS   | :heavy_check_mark:  | &nbsp; |
| Kortkommandon – Använd kortkommandon vid vanliga åtgärder, t.ex. indrag eller infogning  | :heavy_check_mark:  |  &nbsp; |
| Ångra på flera nivåer – Utför konsekvensanalys för att få en full förståelse för ändringarna genom att reversera och återanvända en hel uppsättning åtgärder | :heavy_check_mark: | &nbsp; |
| Klipp ut/Kopiera/Klistra in – Samarbeta med schemautveckling genom att kopiera och klistra in schemainformation mellan program  | :heavy_check_mark: | &nbsp; |
| Checklista för uppgifter – Lägg till upp till 20 checklisteobjekt i en uppgift   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projektplanering

Sidan **Projekt** i Project Operations har ett stort antal skillnader jämfört med sidan **Projekt** i Project Service Automation.

Följande åtgärder har tagits bort från sidan **Projekt** som en del av uppgraderingen av fas 1:

  - **Öppna i MS Project**
  - **Skapa mall**
  - **Ta bort kopplingen mellan MS Project**

Sidan **Projekt** i Project Operations omfattar följande nya flikar.

- **Materialberäkningar**
- **Faktureringsinställningar för uppgift**

Fliken **Status** har tagits bort, och fältet **Status** finns nu på fliken **Sammanfattning** tillsammans med projektets schemaläggningsläge.

   ![Uppdateringar av projektsidan.](media/projectform.png)

Fliken **Schema** har bytt namn till fliken **Uppgift** och innehåller den nya projektplaneringsupplevelsen med Project for the Web.

   ![Fliken Nya projektuppgifter.](media/tasktab.png)

## <a name="scheduling-modes"></a>Schemaläggningslägen

Project Operations har introducerat en ny funktion: [schemaläggningslägen](../project-management/scheduling-modes.md). Alla befintliga projekt för Project Service Automation återgår som standard till inställningen **Fast varaktighet** i Project Operations. Standardvärdet för nya projekt kan emellertid hanteras genom att gå till **Inställningar** > **Parametrar** > **Parameter** > **Schemaläggningsläge**.

   ![Inställningar för projektparameter för schemaläge.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Gränser för projektplanering

Project Operations förlitar sig på Project for the Web för alla projektschemaläggningsåtgärder. Project for the Web hanterar den uppdelade arbetsstrukturen med hjälp av begränsningarna i följande tabell.

| **Fält**                                          | **Gräns**             |
|----------------------------------------------------|-----------------------|
| Maximalt antal uppgifter för ett projekt                  | 500                   |
| Längsta varaktighet för ett projekt               | 3 650 dagar (10 år)  |
| Maximalt antal resurser för ett projekt              | 300                   |
| Maximalt antal länkar (endast efterföljare) för ett projekt | 600                   |
| Maximalt antal anpassade fält för ett projekt          | 10                    |
| Maximal hierarkinivå                            | 10 nivåer             |
| Maximalt antal länkar (efterföljare + föregångare)            | 20                    |
| Längsta varaktighet för lövuppgift                      | 1250 dagar             |
| Längsta varaktighet för en sammanfattningsuppgift                 | 3 650 dagar (10 år)  |
| Maximalt antal resurser tilldelade till en uppgift               | 20 resurser          |
| Datumintervall som stöds för en uppgift                    | 2000-01-01 - 2149-12-31 |
| Checklistepunkter                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projektplanering – utbyggbarhet och utveckling

När du har uppgraderat till Project Operations måste du använda API:er för projektschemaläggning för att skapa, uppdatera och ta bort åtgärder för följande entiteter:

|   Entitetsnamn           |   Entitetens logiska namn       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektuppgift            | msdyn_projecttask           |
| Beroende för projektuppgift | msdyn_projecttaskdependency |
| Resurstilldelning     | msdyn_resourceassignment    |
| Projektgrupp          | msdyn_projectbucket         |
| Projektgruppmedlem     | msdyn_projectteam           |

Om du för närvarande har anpassningar som omfattar dessa entiteter, se [Använda API:er för projektschemaläggning för att utföra åtgärder med schemaläggningsentiteter](../project-management/schedule-api-preview.md) för implementeringsvägledning.

## <a name="data-model-changes"></a>Ändringar i datamodell

Som en del av uppgraderingsfas 1 sker ändringar i datamodellen. Ändringarna är primärt fältändringar för befintliga entiteter. I fas 1 används entiteterna, **msydn_project** och **msdyn_projectteam** för att skapa anpassningar på nytt. 

> [!IMPORTANT]
> Detta avsnitt uppdateras med ytterligare entiteter allteftersom framtida uppgraderingsfaser slutförs.

Följande fält har ersatts med nya fält.

|   Enhet          |   Tidigare logiskt namn   |   Nytts logiskt namn    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Följande fält har lagts till.

|   Enhet          |   Logiskt namn                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Visar projektets ackumulerade faktiska arvodesförsäljning. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Visar den ackumulerade faktiska material kostnaden för projektet. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Visar projektets ackumulerade faktiska materialförsäljning. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Kontraktraden associerad med detta projekt. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Detta är ett internt systemfält som används för funktionen **Kopiera projekt** relaterad till korrelationsidentifieraren. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Detta är ett internt systemfält som används för funktionen **Kopiera projekt** relaterad till sessionsidentifieraren. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Senaste synkronisering av xRM Global Revision-token från projektschemaläggningstjänsten. |
| msdyn_project     | msdyn_msprojectdocument                      | Det Microsoft Project-dokument som tillhör projektet. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Den ackumulerade planerade materialkostnaden för projektet. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Den ackumulerade planerade materialförsäljningen för projektet. Endast för användning i Project Service Automation. |
| msdyn_project     | msdyn_program                                | Det program som det här projektet är relaterat till. |
| msdyn_project     | msdyn_quotelineproject                       | Offertraden associerad med det här projektet. |
| msdyn_project     | msdyn_replaylogheader                        | Rubrik för återuppspelningsloggar. |
| msdyn_project     | msdyn_schedulemode                           | Det standardschemaläge som används för alla uppgifter i projektet.  |
| msdyn_project     | msdyn_taskearlieststart                      | Det tidigaste startdatumet för en uppgift i projektet.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Den projektteammedlemm som denna projektteammedlem kopierades från. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Anger huruvida resurskravet ska skapas för en nyligen skapad allmän teammedlem.  |
| msdyn_projectteam | msdyn_deletestatus                           | Borttagningsstatusen för den teammedlem som ska spåras om det finns en borttagningsbegäran skickad till projektets schemaläggningstjänst PSS, samt huruvida PSS skickar tillbaka svar inom den förväntade tiden. |
| msdyn_projectteam | msdyn_effortcompleted                        | Spårar de insatser som åstadkommits av teammedlemmen i dennes tilldelningar. |
| msdyn_projectteam | msdyn_effortremaining                        | Spårar de insatser som ännu inte åstadkommits av teammedlemmen i dennes tilldelningar. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Väntetiden från det att teammedlemmen skickar en borttagningsbegäran till schemaläggningstjänsten för projekt tills teammedlemmen faktiskt tas bort på Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Tidsstämpeln som registrerar när begäran att ta bort teammedlemmen skickas till PSS. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Visar projektteammedlemmen som den här projektteammedlemmen kopierades från.  |

## <a name="project-templates"></a>Projektmallar

Project Operations tillhandahåller inte stöd för projektmallar. Du kan emellertid replikera mycket av kärnfunktionerna med hjälp av [API för projektkopia](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Tilläggssupport för stationära datorer

Support för tillägget Microsoft Project Desktop är inte tillgängligt under de första två stadierna av uppgraderingen. I fas 3 kan kunder som har projekt som är större än de gränser som för närvarande stöds för Project for the Web använda tillägget för stationära datorer.

## <a name="editing-resource-assignment-contours"></a>Redigera resurstilldelningsprofiler

Möjligheten att redigera resurstilldelningsprofiler är tillgänglig när uppgraderingsfas 2 är tillgänglig.

## <a name="billing-and-pricing"></a>Fakturering och prissättning

Följande nya funktioner har lagts till i Project Operations. Dessa funktioner är additiva och påverkar inte datamodellen Project Service Automation.

- [Registrera materialanvändning för projekt och projektuppgifter](../material/material-usage-log.md)
- [Underleverantörshantering](../pro/subcontracting/managing-subcontracts-overview.md)
- [Förskott och arvodesbaserade kontrakt](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontrakts undre status och valideringar](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Uppgiftsbaserad fakturering](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Inaktuella komponenter

I följande tabeller dokumenteras alla inaktuella fält som flyttas till den inaktuella komponentlösningen efter uppgradering. Mer information och en länk till lösningen finns i [Dynamics 365 Project Service Automation 3x till Project Operations 4x inaktuella komponenter](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Fält                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

