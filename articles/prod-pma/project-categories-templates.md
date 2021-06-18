---
title: Synkronisera projektutgiftskategorier mellan Finance and Operations och Project Service Automation
description: I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera projektets utgiftskategorier mellan från Microsoft Dynamics 365 Finance och Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999873"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisera projektutgiftskategorier mellan Finance and Operations och Project Service Automation

[!include[banner](../includes/banner.md)]

I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera projektets utgiftskategorier mellan från Dynamics 365 Finance och Dynamics 365 Project Service Automation.

> [!NOTE]
> - OProjektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.
> - Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.
> - Om du använder Enterprise Edition 7.3.0 kan du, efter att du har installerat KB 4132657 och KB 4132660, använda mallarna för att integrera projektuppgifter, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och faktiska värden samt för att konfigurera låsning av funktioner. Om du måste återställa redovisningsfördelningarna bör du även installera KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Dataflöde för Project Service Automation och Finance

Project Service Automation och Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance. Integreringsmallar som är tillgänglig med funktionen för dataintegrering gör det möjligt för dataflöde om kategorier för utgiftstransaktioner för projekt mellan Finance och Project Service Automation.

Om projektutgiftskategorierna är sammanställda i Finance är integrationsflödet först inställt på Finance till Project Service Automation. Integrerings-ID för projektutgiftskategorierna uppdateras sedan med synkroniseringen från Project Service Automation till Finance.

Om projektutgiftskategorierna är sammanställda i Project Service Automation är integrationsflödet först inställt på Project Service Automation och Finance. Projektkategorierna måste redan vara konfigurerade i Finance innan synkroniseringen mellan Project Service Automation. Synkronisera från Finance tillbaka till Project Service Automation och sedan från Project Service Automation till Finance igen. På det här sättet kan du garantera att kategorierna är länkade och att inga dubbletter skapas.

> [!NOTE]
> Projektutgiftskategorierna hanteras vanligtvis hanterade i Finance. Om de inte är det, eller om utgiftskategorier redan har skapats i Project Service Automation, måste du först synkronisera med hjälp av transaktionskategorier för projektutgifter (PSA till Fin and Ops). Synkronisera sedan med hjälp av mallen för transaktionskategorier för projektutgifter (Fin and Ops till PSA). Kör sedan synkroniseringen från Project Service Automation till Finance en gång till.
>
> Om du synkroniserar först från Project Service Automation måste följande krav uppfyllas i Finance innan synkroniseringen körs:
>
> - Den delade kategorin som överensstämmer med projektkategorin som är inställd i Project Service Automation måste finnas och måste vara aktiverad för både **projekt** och **utgift**.
> - För varje juridisk person i Finance som måste vara integrerad med måste följande projektkategorier finnas:
>
>     - **Projektkategorin** finns. 
>     - **Användning i utgift** har aktiverats.
>     - **Aktiv i journal** har aktiverats.
>     - **Transaktionstyp** har värdet **utgift**.

Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.

[![Dataflöde för Project Service Automation-integrering med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synkronisering av projektutgiftskategorier från Finance till Project Service Automation

### <a name="template-and-task"></a>Mall och uppgift

Om du vill öppna mallen går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.

Följande mall och underliggande uppgift som används för att synkronisera projektutgiftskategorier från Finance till Project Service Automation:

- **Namn på mallen i dataintegrering:** transaktionskategorier för projektutgifter (Fin and Ops till PSA)
- **Namn på uppgiften i projektet:** synkroniserar kategorier till PSA

### <a name="entity-set"></a>Entitetsuppsättning

| Ekonomi                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integreringsentitet för kategorier | Transaktionskategorier     |

### <a name="entity-flow"></a>Entitetsflöde

Projektutgiftskategorier hanteras i Finance och synkroniseras till Project Service Automation som transaktionskategorier.

### <a name="power-query"></a>Power Query

När du synkroniserar med Project Service Automation måste du använda Microsoft Power Query for Excel för att ange faktureringstyp i transaktionskategorin. Kategorierna för projektutgiftstransaktioner mallen (Fin och Ops to PSA) tillhandahåller en standardkolumn och mappning. Om du skapar en egen mall måste du lägga till en villkorskolumn i Power Query. Följ stegen nedan.

1. Klicka på pilen om du vill öppna mappningen av aktiviteten projektutgiftskategorier i mallen Projektutgiftskategorier (Fin and Ops till PSA).
2. Klicka på länken **Avancerad fråga och filtrering** för att öppna Power Query.
2. Välj **Lägg till villkorlig kolumn**.
3. Ange ett namn för den nya kolumnen t.ex. **Faktureringstyp**.
4. Ange följande villkor: **om CATEGORYID inte är null 19235001, annars null**.
5. Klicka på **OK** i kolumnen.
6. Kontrollera att du mappar den nya kolumnen på mappningssidan.

I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Finance till Project Service Automation.

[![Projektutgiftskategori till mallmappning av Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synkronisering av projektutgiftskategorier från Project Service Automation till Finance

### <a name="template-and-task"></a>Mall och uppgift

Följande mall och underliggande uppgift som används för att synkronisera projektutgiftskategorier från Project Service Automation till Finance:

- **Namn på mallen i dataintegrering:** transaktionskategorier för projektutgifter (PSA till Fin and Ops)
- **Namn på uppgiften i projektet:** synkroniserar kategorier till Fin Ops

### <a name="entity-set"></a>Entitetsuppsättning

| Project Service Automation | Ekonomi                           |
|----------------------------|-----------------------------------|
| Transaktionskategorier     | Integreringsentitet för kategorier |

### <a name="entity-flow"></a>Entitetsflöde

Projektutgiftskategorier hanteras i Finance och synkroniseras till Project Service Automation som transaktionskategorier. Synkroniseringen tillbaka till Finance uppdaterar projektkategorin i Finance med integrations-ID från Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering.

> [!NOTE]
> Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.

[![Project Service Automation till Finance-mallmappning](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]