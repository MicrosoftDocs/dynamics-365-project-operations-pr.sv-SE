---
title: Project Operations mappningsversioner för dubbelriktad skrivning
description: Detta ämne innehåller listan med mappningar med dubbelriktad skrivning som krävs för Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939052"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations mappningsversioner för dubbelriktad skrivning

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

För att använda Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier krävs att en uppsättning mappningar med dubbelriktad skrivning körs i miljön. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Obligatoriska mappningar: Orkestreringslösning för dubbelriktad skrivning

Följande mappningar är obligatoriska för lösningen Project Operations. Kör de mappningar som visas i följande tabell och relaterade tabellmappningar i miljön.

| Tabellmappning | Initial synkronisering |
| --- | --- |
| Huvudbok (msdyn_ledgers) | Kräver inledande synkning för tabellmappningen och alla förutsättningar. Master för initial synkning är Finance and Operations-apparna. |
| Juridiska entiteter (cdm_companies) | Krävs inte. Systemet fyller automatiskt i den här entiteten när miljöer länkas med dubbelriktad skrivning. |
| Kunder V3 (accounts) | Krävs inte för etablering. |
| Leverantörer V2 (msdyn_vendors) | Krävs inte för etablering. |

1. I mappningslistan väljer du mappningen Huvudbok **(msdyn\_ledgers)** med alla obligatoriska delar och väljer sedan kryssrutan **Initial synkning**. I fältet **Master för initial synkning** väljer du **Finance and Operations-appar** för både huvudboksmappning och obligatoriska mappningar. Markera **Kör**.

![Synkronisering av huvudboksmappning](media/DW6.png)

1. Följ samma steg för alla återstående tabellmappningar som visas i tabellen ovan. Markera inte kryssrutan **Initial synkning** när dessa mappningar körs.

## <a name="project-operations-dual-write-maps"></a>Project Operations mappningar med dubbelriktad skrivning

Följande mappningar krävs för en Project Operations-lösning.

| **Entitetsmappning** | **Senaste versionen** | **Initial synkronisering** |
| --- | --- | --- |
| Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections) | 1.0.0.0 | Krävs inte för etablering. |
| Projektkontraktrubriker (sales orders) | 1.0.0.1 | Krävs inte för etablering. |
| Projektkontraktrader (salesorderdetails) | 1.0.0.0 | Krävs inte för etablering. |
| Källa för projektfinansiering (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Krävs inte för etablering. |
| Project Operations integrationstabell för materialberäkningar (msdyn\_estimatelines) | 1.0.0.0 | Krävs inte för etablering. |
| Projektfakturaförslag V2 (invoices) | 1.0.0.2 | Krävs inte för etablering. |
| Faktiska värden för Project Operations-integration (msdyn_actuals) | 1.0.0.14 | Krävs inte för etablering. |
| Milstolpar för kontraktrad för Project Operations-integration (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Krävs inte för etablering. |
| Entitet för Project Operations-integration för utgiftsuppskattningar (msdyn_estimateslines) | 1.0.0.2 | Krävs inte för etablering. |
| Entitet för Project Operations-integration för tidsuppskattningar (msdyn_resourceassignments) | 1.0.0.5 | Krävs inte för etablering. |
| Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_expensecategories) | 1.0.0.2 | Krävs inte för etablering. |
| Entitet för export av projektutgifter i Project Operations-integration (msdyn_expenses) | 1.0.0.2 | Krävs inte för etablering. |
| Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices) | 1.0.0.0 | Krävs inte för etablering. |
| Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Krävs inte för etablering. |
| Projektresursroller för alla företag (bookableresourcecategories) | 1.0.0.1 | Kräver en initial synkronisering av tabellmappningen för att synkronisera resursrollerna Projektledare och Teammedlem som fylls i i Dynamics 365 Dataverse-miljön under etableringen. Dataverse är huvudkällan för den första synkroniseringen. |
| Projektuppgifter (msdyn_projecttasks) | 1.0.0.4 | Krävs inte för etablering. |
| Projekttransaktionskategorier (msdyn_transactioncategories) | 1.0.0.0 | Krävs inte för etablering. |
| Projekt V2 (msdyn_projects) | 1.0.0.1 | Krävs inte för etablering. |

Kör de listade mappningar genom att följa stegen nedan.

1. Aktivera projektresursrollerna för tabellmappningen **Alla företag (bookableresourcecategories)** eftersom denna mappning kräver första synkronisering. I fältet **Master för första synkning** väljer du **Gemensam datatjänst**. 

 ![Mappningssynkning av resursrolltabell](media/6ResourceInitialSync.jpg)

 Vänta tills mappningen status är **Körs** innan du tar nästa steg.

2. Markera alla återstående obligatoriska mappningar. Du kan filtrera dem i listan med mappningar med dubbelriktad skrivning med nyckelordet **Projekt** i sökfunktionen längst upp till höger. Du kan göra flerval av alla mappningar och sedan köra dem. Mer information finns i [Hantera flera tabellmappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Se till att du även aktiverar och kör relaterade entitetsmappningar.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations mappningsversioner för dubbelriktad skrivning

Kör alltid den senaste versionen av mappningen i miljön. Vissa funktioner kanske inte fungerar korrekt om något av följande villkor finns:

- En mappning har inte aktiverats.
- Den senaste versionen av mappningen har inte aktiverats. 
- Relaterade tabellmappningar har inte aktiverats.

Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du kan aktivera en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning måste du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
