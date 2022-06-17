---
title: Analys av projektofferter
description: I denna artikel finns information om hur du analyserar projektofferter.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 9db924c16c5eca17e7962ff1d88b09e581347fa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919300"
---
# <a name="analysis-of-project-quotes"></a>Analys av projektofferter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyserar projektofferter för uppskattning av lönsamheten. Den analyserar även hur väl offerten är justerad mot kundförväntningarna om leveransdatum eller slutdatum och om budget.

## <a name="profitability-analysis"></a>Lönsamhetsanalys

Project Service Automation analyserar lönsamheten med hjälp av bruttomarginalen och den justerade bruttomarginalen.

- Bruttomarginaler beräknas med hjälp av följande formel:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Den justerade bruttomarginalen beräknas med hjälp av följande formel:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Om värdena för bruttomarginal och justerad bruttomarginal skiljer sig åt med en bred marginal, klassificeras mycket av arbetet i offerten som icke debiterbart.

## <a name="analysis-of-customer-expectations"></a>Analys av kundens förväntningar

Du kan analysera offerter och skapa diagram för kundförväntningar om schemat och budgeten om du anger värden för följande fält:

- Fältet **begärt leveransdatum** i offerthuvudet.
- Fältet **Kundbudget** för varje offertrad (för projektbaserade rader och produktbaserade rader).

Analys av kundens förväntningar om schemat görs genom att jämföra det senaste slutdatumet för offertraddetaljerna med begärt leveransdatum för alla offertrader i offerten.

Analys av kundförväntningar för budgeten sker genom att summan av den totala kundbudgeten jämförs med det offererade beloppet över alla offertrader.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
