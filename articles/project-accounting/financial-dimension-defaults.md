---
title: Standardvärden för ekonomisk dimension
description: I det här ämnet finns information om hur du ställer in standardvärden för ekonomiska dimensioner.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131905"
---
# <a name="financial-dimension-defaults"></a>Standardvärden för ekonomisk dimension

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Dynamics 365 Project Operations använder [finansiella dimensioner](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) ramverk i Dynamics 365 Finance för att ge ytterligare insikter i projektredovisning och redovisnings transaktioner.

Det går att ange ekonomiska standarddimensioner för en kund, projektfinansieringskälla, milstolpe, projektkontraktrad eller projekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definiera ekonomiska standarddimensioner för en kund

Standardvärden för kunddimensioner anges i Finance. Slutför följande steg för att ställa in standardinställningar.

1. Gå till **kundreskontra** > **kunder** > **alla kunder**.
2. På sidan **kunder** på fliken **ekonomiska dimensioner** anger du värden för den ekonomiska dimensionen för en specifik kund.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definiera ekonomiska standarddimensioner för projektkontrakt

Projektkontrakt skapas och underhålls i Common Data Service (CDS). Redovisningsproviders för projektkontrakt anges i modulen **projektledning och redovisning** i Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Ange ekonomiska dimensioner för en projektfinansieringskälla

1. Gå till **Projektledning och redovisning** > **Projekt** > **Projektkontrakt**.
2. Markera den post du vill uppdatera och på fliken **Projektkontrakt** väljer du **Visa standardredovisning**.
3. Visa **Relaterad information** och välj fliken **Finansieringskällor**.
4. Ange standardvärden för ekonomisk dimension. Observera att de ekonomiska dimensionerna standard från kundkontot.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Ange ekonomiska dimensioner för en projektkontraktrad

1. Gå till **Projektledning och redovisning** > **Projekt** > **Projektkontrakt**.
2. Markera den post du vill uppdatera och på fliken **Projektkontrakt** väljer du **Visa standardredovisning**.
3. Visa **Relaterad information** och välj fliken **Kontraktrader**.
4. Ange standardvärden för ekonomisk dimension. De ekonomiska dimensionerna är tillämpliga och kan endast användas med kontraktrader av fast pris (milstolpe).

Dessa standardvärden används för relaterade a conto-transaktioner och fakturarader.

## <a name="define-default-financial-dimensions-for-projects"></a>Definiera ekonomiska standarddimensioner för projekt

Projekt skapas och underhålls i CDS. Redovisningsproviders för projekt anges i modulen **projektledning och redovisning** i Finance.

1. Gå till **projektledning och redovisning** > **projekt** > **alla projekt**.
2. Markera den post du vill uppdatera och på fliken **Projekt** väljer du **Visa standardredovisning**.
3. Visa **Relaterad information** och välj fliken **Inställning**.
4. Ange standardvärden för ekonomisk dimension. Observera att de ekonomiska dimensionerna standard från kundkontot. Om projektet är associerat med en kontraktrad med flera projektkontraktkunder används den primära kunden för att standardisera ekonomiska dimensioner.

Projektets ekonomiska standarddimensioner används för att ange standard för journalrader för tid-, utgifts- och avgiftstransaktioner i **Project Operations integrationsjournalen** och på relaterade projekt fakturarader.
