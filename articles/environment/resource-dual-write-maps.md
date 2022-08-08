---
title: Project Operations mappningsversioner för dubbelriktad skrivning
description: Den här artikeln innehåller en lista över mappningar med dubbelskrivning som krävs för Dynamics 365 Project Operations.
author: sigitac
ms.date: 07/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e904ad18b6ea94cd6d31d1878b5bc9e7c52be741
ms.sourcegitcommit: c8b8fef5626790208c5290b1bb92b17a5d90d286
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112451"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations mappningsversioner för dubbelriktad skrivning

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

För att använda Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier krävs att en uppsättning mappningar med dubbelriktad skrivning körs i miljön. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Obligatoriska mappningar: Orkestreringslösning för dubbelriktad skrivning

Följande mappningar är obligatoriska för lösningen Project Operations. Kör de mappningar som visas i följande tabell och relaterade tabellmappningar i miljön.

| Tabellmappning | Initial synkronisering |
| --- | --- |
| Huvudbok (msdyn_ledgers) | Kräver inledande synkning för tabellmappningen och alla förutsättningar. Appar för ekonomi och drift utgör huvud för första synkronisering. |
| Juridiska entiteter (cdm_companies) | Krävs inte. Systemet fyller automatiskt i den här entiteten när miljöer länkas med dubbelriktad skrivning. |
| Kunder V3 (accounts) | Krävs inte för etablering. |
| Leverantörer V2 (msdyn_vendors) | Krävs inte för etablering. |

1. I mappningslistan väljer du mappningen Huvudbok **(msdyn\_ledgers)** med alla obligatoriska delar och väljer sedan kryssrutan **Initial synkning**. I fältet **Huvud för första synkronisering** väljer du **Appar för ekonomi och drift** för både redovisningsmappning och samtliga erforderliga mappningar. Markera **Kör**.

![Synkronisering av transaktionsregistermappning.](media/DW6.png)

2. Följ samma steg för alla återstående tabellmappningar som visas i tabellen ovan. Markera inte kryssrutan **Initial synkning** när dessa mappningar körs.

## <a name="project-operations-dual-write-maps"></a>Project Operations mappningar med dubbelriktad skrivning

Följande mappningar krävs för en Project Operations-lösning. Mappningsversioner med dubbel skrivning visas från och med uppdateringen av Project Operations i 2021, version 4.10.0.186.

| Entitetsmappning | Senaste versionen | Initial synkronisering | Obligatorisk Dynamics 365 Finance-version |
| --- | --- | --- | --- |
| Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections) | 1.0.0.0 | Krävs inte för etablering. ||
| Projektkontraktrubriker (sales orders) | 1.0.0.1 | Krävs inte för etablering. ||
| Projektkontraktrader (salesorderdetails) | 1.0.0.0 | Krävs inte för etablering. ||
| Källa för projektfinansiering (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Krävs inte för etablering. ||
| Projekt integrationstabell för materialberäkningar (msdyn\_estimatelines) | 1.0.0.0 | Krävs inte för etablering. ||
| Projektfakturaförslag V2 (invoices) | 1.0.0.3 | Krävs inte för etablering. ||
| Faktiska värden för Project Operations-integration (msdyn_actuals) | 1.0.0.14 | Krävs inte för etablering. ||
| Project Operations-integrering för milstolpar för kontraktrad (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Krävs inte för etablering. ||
| Entitet för Project Operations-integrering för utgiftsberäkningar (msdyn_estimatelines) | 1.0.0.2 | Krävs inte för etablering. ||
| Entitet för Project Operations-integration för tidsuppskattningar (msdyn_resourceassignments) | 1.0.0.5 | Krävs inte för etablering. ||
| Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_expensecategories) | 1.0.0.1 | Krävs inte för etablering. ||
| Entitet för export av projektutgifter i Project Operations-integration (msdyn_expenses) | 1.0.0.3 | Krävs inte för etablering. ||
| Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices) | 1.0.0.1 | Krävs inte för etablering. |10.0.26 eller senare|
| Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Krävs inte för etablering. | 10.0.26 eller senare |
| Projektresursroller för alla företag (bookableresourcecategories) | 1.0.0.1 | Kräver en initial synkronisering av tabellmappningen för att synkronisera resursrollerna Projektledare och Teammedlem som fylls i i Dynamics 365 Dataverse-miljön under etableringen. Dataverse är huvudkällan för den första synkroniseringen. ||
| Projektuppgifter (msdyn_projecttasks) | 1.0.0.4 | Krävs inte för etablering. ||
| Projekttransaktionskategorier (msdyn_transactioncategories) | 1.0.0.0 | Krävs inte för etablering. ||
| Projekt V2 (msdyn_projects) | 1.0.0.2 | Krävs inte för etablering. ||

Kör de listade mappningar genom att följa stegen nedan.

1. Aktivera projektresursrollerna för tabellmappningen **Alla företag (bookableresourcecategories)** eftersom denna mappning kräver första synkronisering. I fältet **Master för första synkning** väljer du **Gemensam datatjänst**. 

 ![Mappningssynkning av resursrolltabell.](media/6ResourceInitialSync.jpg)

 Vänta tills mappningen status är **Körs** innan du tar nästa steg.

2. Markera alla återstående obligatoriska mappningar. Du kan filtrera dem i listan med mappningar med dubbelriktad skrivning med nyckelordet **Projekt** i sökfunktionen längst upp till höger. Du kan göra flerval av alla mappningar och sedan köra dem. Mer information finns i [Hantera flera tabellmappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Se till att du även aktiverar och kör relaterade entitetsmappningar.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations mappningsversioner för dubbelriktad skrivning

Kör alltid den senaste versionen av mappningen i miljön. Vissa funktioner kanske inte fungerar korrekt om något av följande villkor finns:

- En mappning har inte aktiverats.
- Den senaste versionen av mappningen har inte aktiverats. 
- Relaterade tabellmappningar har inte aktiverats.

Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du kan aktivera en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning måste du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
