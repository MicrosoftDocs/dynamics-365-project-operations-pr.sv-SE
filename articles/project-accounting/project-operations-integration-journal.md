---
title: Integrationsjournal i Project Operations
description: I det här ämnet finns information om hur du arbetar med integrations journalen i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133456"
---
# <a name="integration-journal-in-project-operations"></a>Integrationsjournal i Project Operations

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Tid- och utgiftsposter skapa **Faktisk** transaktioner som representerar den operativa vyn för arbete som slutförts mot ett projekt. Dynamics 365 Project Operations tillhandahåller revisorer ett verktyg för att granska transaktioner och justera redovisningsinformationen efter behov. När granskningen och justeringen har slutförts bokförs transaktionerna i projektredovisningen och redovisningen. En revisor kan utföra dessa aktiviteter med hjälp av journalen **Project Operations-integrering** **Dynamics 365 Finance** > **Projektledning och redovisning** > **Journaler** > **Project Operations-integrering** journal.

![Integrationsjournalflöde](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Skapa poster i integrationsjournal för Project Operations

Poster i Project Operations integrationsjournalen skapas med periodisk process, **import från testtabell**. Du kan köra den här processen genom att gå till **Dynamics 365 Finance** > **Projektledning och redovisning** > **Periodisk** > **Project Operations-integrering** > **Importera från testtabell**. Du kan köra processen interaktivt eller konfigurera processen så att den körs i bakgrunden efter behov.

När den periodiska processen körs, hittas alla verkliga värden som ännu inte har lagts till i Project Operations-integreringsjournale. En journalrad för varje aktuell transaktion skapas.
Systemet grupperar journalrader i separata journaler baserat på det värde som valts i fältet **Periodenhet på Project Operations-integrationsjournal** (**Finance** > **Projektledning och redovisning** > **Konfiguration** > **Projektledning och redovisningsparametrar**, **Project Operations på fliken Dynamics 365 Customer Engagement** _). Möjliga värden för det här fältet är:

  - _*Dagar**: faktiska värden grupperas efter transaktionsdatum. En separatjournal skapas för varje dag.
  - **Månader**: faktiska värden grupperas efter kalendermånad. En separat journal skapas för varje månad.
  - **År**: faktiska värden grupperas efter kalenderår. En separatjournal skapas för varje år.
  - **Alla**: alla faktiska transaktioner ingår i samma integrationsjournal. Om journalen inte är tillgänglig när den periodiska processen körs, till exempel om journalen är under bokföring av transaktioner, skapas en ny journal.

Journalrader skapas utifrån projektets faktiska värden. Följande lista innehåller några av de mest bevarade standard- och omvandlingsreglerna:

  - Varje projekt faktiska transaktion har en rad i integrationsjournalen för Project Operations. Kostnads- och ofakturerade försäljningstransaktioner för tid och material faktureringstyp visas på separata rader.
  - Fältet **Datum** representerar datumet för transaktionen. Fältet **bokföringsdatum** representerar det datum då transaktionen registreras i redovisningsmodulen. Om redovisningsdatumet infaller i en [stängd finansiell period](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) och parametern **ställ automatiskt in redovisningsdatum för att öppna redovisningsperiod** anges på fliken **finans** på sidan **Projektledning och redovisningsparametrar**, justeras redovisningsdatumet för transaktionen till det första datumet i nästa öppna redovisningsperiod.
  - I fältet **verifikation** visas verifikationsnumret för varje aktuell transaktion. Verifikations nummer serien definieras på fliken **nummerserier** på sidan **projektledning och redovisningsparametrar**. Varje rad tilldelas ett nytt nummer. När verifikationen har bokförts kan du visa hur kostnaden och den fakturerade försäljningstransaktionen är relaterade genom att välja **relaterad verifikation** på sidan **verifikationstransaktion**.
  - Fältet **kategori** representerar en projekttransaktion och standardvärden baserat på transaktionskategorin för det relaterade projektet.
    - Om en **transaktionskategori** ställs in i projektets faktiska och en relaterad **projektkategori** finns i en viss juridisk person får kategorin standardvärden för projektkategorin.
    - Om **transaktionskategori** har ställts in i projektet faktiskt, använder systemet värdet i **Standard för projektkategori** på fliken **Project Operations på Dynamics 365 Customer Engagement** på sidan **projektledning och redovisningsparametrar**.
  - Fältet **Resurs** representerar projektresursen som är kopplad till den här transaktionen. Resursen används som referens i projektfaktura förslag till kunder.
  - Fältet **Valutakursen** standardvärden är från valutakursen inställd **Valutakurs** i Dynamics 365 Finance. Om valutakursinställningarna saknas lägger periodiska processen för **Import från faser** inte till posten i en journal och ett felmeddelande läggs till i jobbkörningsloggen.
  - Fältet **Radegenskap** representerar faktureringstypen i projektets verkliga värden. Radegenskap och mappning av faktureringstyp har definierats för **Project Operations på fliken Dynamics 365 Customer Engagement** på sidan **Projekthantering och redovisningsparametrar**.

Endast följande redovisningsattribut kan uppdateras i raderna i Project Operation integreringsjournalen:

- **Momsgrupp för fakturering** och **Momsgrupp för faktureringsartikel**
- **Ekonomiska dimensioner** (med hjälp av åtgärden **Fördela belopp**)

Integrerings journalrader kan tas bort, men alla ej bokförda rader infogas i journalen igen när du kör periodiska processen **importen från faser**.

När du bokför integrationsjournalen skapas en projekttransaktion och en redovisningstransaktion. De används i underordnad kundfakturering, intäktsredovisning och ekonomisk rapportering.
