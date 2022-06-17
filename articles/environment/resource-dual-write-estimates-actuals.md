---
title: Projektberäkningar och integration med faktiska värden
description: Den här artikeln innehåller information om integrering med dubbelskrivning av Project Operations för projektuppskattningar och faktiska uppgifter.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914608"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektberäkningar och integration med faktiska värden

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Den här artikeln innehåller information om integrering med dubbelskrivning av Project Operations för projektuppskattningar och faktiska uppgifter.

## <a name="project-estimates"></a>Projektberäkningar

Beräkningar för projektarbete, utgifter och material skapas och underhålls i Microsoft Dataverse och synkroniseras med appar för ekonomi och drift i redovisningssyfte. Åtgärder för att skapa, uppdatera och ta bort stöds inte via apparna för ekonomi och drift.

För att skapa beräkningar krävs en giltig redovisningskonfiguration för projektet. Projekt som är kopplade till kontraktrader måste ha giltig projektkostnads- och intäktsprofil definierad i reglerna för projektkostnads- och intäktsprofil. Mer information finns i [Konfigurera redovisning av fakturerbara projekt](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbetsberäkningar

Arbetsberäkningar skapas av projektledaren eller resursadministratören som också tilldelar en allmän eller namngiven resurs till projektuppgiften. Resurstilldelningsposter kan granskas på fliken **Resurstilldelningar** på sidan **Projektinformation** i Dataverse. Resurstilldelningsposter i Dataverse skapar timprognosposter i appar för ekonomi och drift med hjälp av **integreringsentiteten för timberäkning i Project Operations (msdyn\_resourceassignments)**.

   ![Integration av arbetsberäkningar.](./Media/DW4LaborEstimates.png)

Dubbelriktad skrivning synkroniserar resurstilldelningsposter till mellanlagringstabellen (**ProjCDSEstimateHoursImport**) och affärslogiken används sedan för att skapa och uppdatera timprognosposter (**ProjForecastEmpl**).

Projektets revisor granskar timposter för prognos som skapats i appar för ekonomi och drift genom tatt gå till **Hantering och redovisning för projekt** > **Alla projekt** > **Plan** > **Timprognoser**.

## <a name="expense-estimates"></a>Utgiftsberäkningar

Kostnadsberäkningar skapas av projektledaren på fliken **Kostnadsberäkningar** på sidan **Projektinformation** i Dataverse. Kostnadsberäkningsposter lagras i entiteten **Beräkningsrad** i Dataverse. Dessa beräkningsposter har transaktionsklassen **Utgift** och synkroniseras med poster för utgiftsprognos i appar för ekonomi och drift med hjälp av **integreringsentiteten för utgiftsberäkningar för Project Operations (msdyn\_estimatelines)**

   ![Integration av kostnadsberäkningar.](./Media/DW4ExpenseEstimates.png)

Dubbelriktad skrivning synkroniserar kostnadsberäkningsposter till mellanlagringstabellen **(ProjCDSEstimateExpenseImport)** och affärslogiken används sedan för att skapa och uppdatera kostnadsprognosposter (**ProjForecastCost**). Beräkningsrader lagrar försäljningsberäknings- och kostnadsberäkningsposter separat. Affärslogiken i apparna för ekonomi och drift fyller i en enskild utgiftsprognospost med hjälp av denna information i testtabellen.

Projektets revisor kan granska prognosposter för utgifter i appar för ekonomi och drift genom att gå till **Hantering och redovisning för projekt** > **Alla projekt** > **Plan** > **Utgiftsprognoser**.

## <a name="material-estimates"></a>Materialberäkningar

Materialberäkningar skapas av projektledaren på fliken **Materialberäkningar** på sidan **Projektinformation** i Dataverse. Materialberäkningsposter lagras i entiteten **Beräkningsrad** i Dataverse. Dessa beräkningsposter har transaktionsklassen **Material** och synkroniseras med poster för objektprognos i appar för ekonomi och drift med hjälp av **Projektintegreringstabellen för materialberäkningar (msdyn\_estimatelines)**.

   ![Integration av materialberäkningar.](./Media/DW4MaterialEstimates.png)

Dubbelriktad skrivning synkroniserar materialberäkningsposter till mellanlagringstabellen **ProjForecastSalesImpor** och affärslogiken används sedan för att skapa och uppdatera artikelprognosposter (**ForecastSales**). Beräkningsrader lagrar försäljningsberäknings- och kostnadsberäkningsposter separat. Affärslogiken i apparna för ekonomi och drift fyller i en enskild artikelprognospost med hjälp av denna information i testtabellen.

Projektets revisor kan granska prognosposter för objekt i appar för ekonomi och drift genom att gå till **Hantering och redovisning för projekt** > **Alla projekt** > **Plan** > **Objektprognoser**.

## <a name="project-actuals"></a>Verkliga värden för projekt

Faktiska värden för projekt skapas i Dataverse baserade på tid, kostnader, material och faktureringsaktivitet. Alla verksamhetsattribut för dessa transaktioner, inklusive kvantitet, självkostnad, försäljningspris och projekt, fångas upp i den här Dataverse-entiteten. Mer information finns i [Faktiska värden](../actuals/actuals-overview.md). Faktiska poster synkroniseras med appar för ekonomi och drift med hjälp av tabellmappningen **Faktiska integreringsvärden för Project Operations (msdyn\_actuals)** för redovisning nedströms och med dubbelskrivning.

   ![Integration av faktiska värden.](./Media/DW4Actuals.png)

Tabellmappningen **Faktiska värden för Project Operations-integration** synkroniserar alla poster från entiteten **Faktiska värden** i Dataverse som har attributet **Hoppa över synkronisering (endast intern användning)** inställt som **False**. Attributvärdet anges automatiskt i Dataverse när posten skapas. Exempel på när attributet har angetts som **True** är:

  - Faktiska värden för projektkostnad för koncerninterna transaktioner. Mer information finns i [Skapa koncerninterna transaktioner](../project-accounting/create-intercompany-transactions.md). Dessa poster hoppas över eftersom systemet återskapar den faktiska projektkostnaden i appar för ekonomi och drift när den koncerninterna leverantörsfakturan bokförs.
  - Negativa ofakturerade försäljningsposter skapas när proformafakturan bekräftas. Dessa poster hoppas över eftersom projektunderboken i appar för ekonomi och drift inte vänder den ofakturerade försäljningsposten vid fakturering utan ändrar statusen till "helt fakturerad".

Tabellmappningen med dubbelriktad skrivning synkroniserar faktiska värden för poster till mellanlagringstabellen **ProjCDSActualsImport**. Dessa poster bearbetas av den regelbundna processen **Import från mellanlagringstabell** när journalrader och projektfakturaförslagsrader för Project Operations-integration skapas. Mer information finns i [Integration av journal i Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse samlar även in länkar mellan projektets faktiska transaktioner i entiteten **Transaktionskoppling**. Mer information finns i [Länka faktiska värden till ursprungliga poster](../actuals/linkingactuals.md). Länkar mellan faktiska transaktioner synkroniseras också med appar för ekonomi och drift med hjälp av tabellmappningen med dubbla skrivningar, **integreringsentiteten för projekttransaktionsrelationer (msdyn\_transactionconnections)**. Dessa poster används av den regelbundna processen **Import från mellanlagringstabell** när journalrader och projektfakturaförslagsrader för Project Operations-integration skapas.

Om du publicerar en Project Operations-integrationsjournal och ett projektfakturaförslag utlöses en uppdatering i respektive poster i mellanlagringstabellen, **ProjCDSActualsImport**. Följande redovisningsattribut för faktiska transaktioner fångas upp och registreras i systemet:

- Belopp i redovisningsvaluta
- Växelkurs
- Verifikationsnummer
- Momsbelopp

Tabellmappningen **Faktiska värden för Project Operations-integration** uppdaterar motsvarande faktiska poster i Dataverse med den här informationen.
