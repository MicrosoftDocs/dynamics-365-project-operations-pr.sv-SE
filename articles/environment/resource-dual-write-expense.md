---
title: Integration av utgiftshantering
description: Den här artikeln ger information om integrering av kostnadsrapporter i Project Operations med dubbelskrivning.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64c318dc1915a9a87b6ae3c6b8a2aa6d3c9cd36
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924636"
---
# <a name="expense-management-integration"></a>Integration av utgiftshantering

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Den här artikeln innehåller information om integrering av kostnadsrapporter i Project Operations [fullständig utgiftsdistribution](../expense/expense-overview.md) med dubbelskrivning.

## <a name="expense-categories"></a>Utgiftskategorier

I en fullständig utgiftsdistribution skapas och hanteras utgiftskategorier i apaprna för ekonomi och drift. Om du vill skapa en ny utgiftskategori gör du följande:

1. Skapa en **transaktionskategori** i Microsoft Dataverse. Integrering med dubbelskrivning synkroniserar denna transaktionskategori med appar för ekonomi och drift. Mer information finns i [Konfigurera projektkategorier](/dynamics365/project-operations/project-accounting/configure-project-categories) och [Konfiguration av Project Operations samt integration av konfigurationsdata](resource-dual-write-setup-integration.md). Som ett resultat av denna integrering skapar systemet fyra delade kategoriposter i apparna för ekonomi och drift.
2. I Ekonomi går du till **Utgiftshantering** > **Inställning** > **Delade kategorier** och väljer en delad kategori med transaktionsklass **Utgift**. Ställ in parametern **Kan användas i utgift** som **True** och definiera den utgiftstypen som ska användas.
3. Med den här delade kategoriposten kan du skapa en ny utgiftskategori genom att gå till **Utgiftshantering** > **Inställning** > **Utgiftskategorier** och välja **Ny**. När posten sparas använder dubbelriktad skrivning tabellmappningen **Project Operations-integration av entitet för export av projektutgiftskategorier (msdyn\_expensecategories)** för att synkronisera posten med Dataverse.

  ![Integration av utgiftskategorier.](./media/DW6ExpenseCategories.png)

Utgiftskategorier i appar för ekonomi och drift är företags- eller juridiskt entitetsspecifika. Det finns separata, motsvarande, juridisk enhets-specifika poster i Dataverse. När en projektansvarig beräknar utgifter kan hen inte välja utgiftskategorier som skapats för ett projekt som ägs av ett annat företag än det företag som äger projektet hen arbetar med. 

## <a name="expense-reports"></a>Utgiftsrapporter

Utgiftsrapporter skapas och godkänns i appar för ekonomi och drift. Mer information finns i [Skapa och bearbeta utgiftsrapporter i Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). När utgiftsrapporten har godkänts av projektansvarig registreras den i huvudboken. I Project Operations registreras projektrelaterade utgiftsrapportrader med specialbokföringsregler:

  - Projektrelaterade kostnader (inklusive icke-återbetalningsbar moms) registreras inte direkt på projektkostnadskontot i huvudboken, utan registreras i stället upp på utgiftsintegrationskontot. Kontot ställs in i **Projekthantering och redovisning** > **Inställning** > **Projekthanterings- och redovisningsparametrar**, på fliken **Project Operations i Dynamics 365 Customer engagement**.
  - Dubbelriktad skrivning synkroniseras med Dataverse med tabellmappningen **Entitet för export av projektutgifter i Project Operations-integration (msdyn \_expenses)**.
  - Momsreskontra, leverantörsreskontra och andra ekonomiska poster registreras som tillämpligt vid tidpunkten för utgiftsrapportregistrering.

  ![Integration av utgiftsrapporter.](./media/DW6ExpenseReports.png)

När en post skrivs till entiteten **Utgift** i Dataverse utlöser systemet den automatiska godkännandeprocessen för posten. Vid behov kan du granska status för den automatiska godkännandeprocessen i Dataverse. Gå till **Avancerade inställningar** > **System** > **Systemjobb**. När godkännande är klart skapas poster för utgiftstransaktionsklassen i entiteten **Faktiska värden**.

Utgiftsrelaterade faktiska värden bearbetas sedan med tabellmappningen med dubbelriktad skrivning **Project Operations-integration med faktiska värden (msdyn\_actuals)**. Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md).

Den regelbundna processen **Importera från mellanlagring** skapar utgiftsrapportrelaterade journalrader i Project Operations-integrationsjournalen. Servicekontot använder som standard utgiftsintegrationskontot. Integrationsjournalen för reskontra rensar kontosaldot för utgiftstransaktionen och flyttar utgiftsbeloppet till projektkostnadskontot. Systemet skapar också projektreskontratransaktioner för fakturering nedströms och intäktsidentifieringsändamål.
