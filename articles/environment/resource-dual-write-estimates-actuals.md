---
title: Projektberäkningar och integration med faktiska värden
description: Detta avsnitt innehåller information om Project Operations-integration med dubbelriktad skrivning för projektberäkningar och faktiska värden.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955844"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektberäkningar och integration med faktiska värden

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Detta avsnitt innehåller information om Project Operations-integration med dubbelriktad skrivning för projektberäkningar och faktiska värden.

## <a name="project-estimates"></a>Projektberäkningar

Projektarbete, utgifter och materialberäkningar skapas och underhålls i Microsoft Dataverse och synkroniseras med Finance and Operations-appar för redovisningsändamål. Åtgärder för att skapa, uppdatera och radera stöds inte i Finance and Operations-apparna.

För att skapa beräkningar krävs en giltig redovisningskonfiguration för projektet. Projekt som är kopplade till kontraktrader måste ha giltig projektkostnads- och intäktsprofil definierad i reglerna för projektkostnads- och intäktsprofil. Mer information finns i [Konfigurera redovisning av fakturerbara projekt](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbetsberäkningar

Arbetsberäkningar skapas av projektledaren eller resursadministratören som också tilldelar en allmän eller namngiven resurs till projektuppgiften. Resurstilldelningsposter kan granskas på fliken **Resurstilldelningar** på sidan **Projektinformation** i Dataverse. Resurstilldelningsposter i Dataverse skapar timprognosposter i Finance and Operations-appar med entiteter för **Project Operations-integration för tidsberäkningar (msdyn\_resourceassignments)**.

   ![Integration av arbetsberäkningar](./Media/DW4LaborEstimates.png)

Dubbelriktad skrivning synkroniserar resurstilldelningsposter till mellanlagringstabellen (**ProjCDSEstimateHoursImport**) och affärslogiken används sedan för att skapa och uppdatera timprognosposter (**ProjForecastEmpl**).

Projektredovisaren granskar poster för prognostiserad tid som har skapats i Finance and Operations-appar genom att gå till **Projektledning och redovisning** > **Alla projekt** > **Planera** > **Tidsprognoser**.

## <a name="expense-estimates"></a>Utgiftsberäkningar

Kostnadsberäkningar skapas av projektledaren på fliken **Kostnadsberäkningar** på sidan **Projektinformation** i Dataverse. Kostnadsberäkningsposter lagras i entiteten **Beräkningsrad** i Dataverse. Dessa beräkningsposter har transaktionsklassen **Utgift** och synkroniseras med kostnadsprognosposter i Finance and Operations-appar med entiteten **Project Operations-integrationsentitet för kostnadsberäkningar (msdyn\_estimatelines)**.

   ![Integration av kostnadsberäkningar](./Media/DW4ExpenseEstimates.png)

Dubbelriktad skrivning synkroniserar kostnadsberäkningsposter till mellanlagringstabellen **(ProjCDSEstimateExpenseImport)** och affärslogiken används sedan för att skapa och uppdatera kostnadsprognosposter (**ProjForecastCost**). Beräkningsrader lagrar försäljningsberäknings- och kostnadsberäkningsposter separat. Affärslogiken i Finance and Operations-apparna fyller i en enskild kostnadsprognospost med hjälp av den här uppgiften i mellanlagringstabellen.

Projektredovisaren kan granska kostnadsprognosposter i Finance and Operations-appar genom att gå till **Projektledning och redovisning** > **Alla projekt** > **Planera** > **Kostnadsprognoser**.

## <a name="material-estimates"></a>Materialberäkningar

Materialberäkningar skapas av projektledaren på fliken **Materialberäkningar** på sidan **Projektinformation** i Dataverse. Materialberäkningsposter lagras i entiteten **Beräkningsrad** i Dataverse. Dessa beräkningsposter har transaktionsklassen **Material** och synkroniseras med artikelprognosposter i Finance and Operations-appar med entiteten **Project Operations-integrationstabell för materialberäkningar (msdyn\_estimatelines)**.

   ![Integration av materialberäkningar](./Media/DW4MaterialEstimates.png)

Dubbelriktad skrivning synkroniserar materialberäkningsposter till mellanlagringstabellen **ProjForecastSalesImpor** och affärslogiken används sedan för att skapa och uppdatera artikelprognosposter (**ForecastSales**). Beräkningsrader lagrar försäljningsberäknings- och kostnadsberäkningsposter separat. Affärslogiken i Finance and Operations-apparna fyller i en enskild artikelprognospost med hjälp av den här uppgiften i mellanlagringstabellen.

Projektredovisaren kan granska artikelprognosposter i Finance and Operations-appar genom att gå till **Projektledning och redovisning** > **Alla projekt** > **Planera** > **Artikelprognoser**.

## <a name="project-actuals"></a>Verkliga värden för projekt

Faktiska värden för projekt skapas i Dataverse baserade på tid, kostnader, material och faktureringsaktivitet. Alla verksamhetsattribut för dessa transaktioner, inklusive kvantitet, självkostnad, försäljningspris och projekt, fångas upp i den här Dataverse-entiteten. Mer information finns i [Faktiska värden](../actuals/actuals-overview.md). Faktiska poster synkroniseras med Finance and Operations-appar med tabellmappningen dubbelriktad skrivning **Faktiska värden för Project Operations-integration (msdyn\_actuals)** för nedströms redovisning.

   ![Integration av faktiska värden](./Media/DW4Actuals.png)

Tabellmappningen **Faktiska värden för Project Operations-integration** synkroniserar alla poster från entiteten **Faktiska värden** i Dataverse som har attributet **Hoppa över synkronisering (endast intern användning)** inställt som **False**. Attributvärdet anges automatiskt i Dataverse när posten skapas. Exempel på när attributet har angetts som **True** är:

  - Faktiska värden för projektkostnad för koncerninterna transaktioner. Mer information finns i [Skapa koncerninterna transaktioner](../project-accounting/create-intercompany-transactions.md). Dessa poster hoppas över eftersom systemet återskapar faktiskt värde för projektkostnaden i Finance and Operations-appar när den koncerninterna leverantörsfakturan registreras.
  - Negativa ofakturerade försäljningsposter skapas när proformafakturan bekräftas. Dessa poster hoppas över eftersom projektets delredovisning i Finance and Operations-appar inte vänder den ofakturerade försäljningsposten vid fakturering utan ändrar status till helt fakturerad.

Tabellmappningen med dubbelriktad skrivning synkroniserar faktiska värden för poster till mellanlagringstabellen **ProjCDSActualsImport**. Dessa poster bearbetas av den regelbundna processen **Import från mellanlagringstabell** när journalrader och projektfakturaförslagsrader för Project Operations-integration skapas. Mer information finns i [Integration av journal i Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse samlar även in länkar mellan projektets faktiska transaktioner i entiteten **Transaktionskoppling**. Mer information finns i [Länka faktiska värden till ursprungliga poster](../actuals/linkingactuals.md). Länkar mellan faktiska transaktioner synkroniseras också till Finance and Operations-appar med tabellmappningen med dubbelriktad skrivning **Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections)**. Dessa poster används av den regelbundna processen **Import från mellanlagringstabell** när journalrader och projektfakturaförslagsrader för Project Operations-integration skapas.

Om du publicerar en Project Operations-integrationsjournal och ett projektfakturaförslag utlöses en uppdatering i respektive poster i mellanlagringstabellen, **ProjCDSActualsImport**. Följande redovisningsattribut för faktiska transaktioner fångas upp och registreras i systemet:

- Belopp i redovisningsvaluta
- Växelkurs
- Verifikationsnummer
- Momsbelopp

Tabellmappningen **Faktiska värden för Project Operations-integration** uppdaterar motsvarande faktiska poster i Dataverse med den här informationen.
