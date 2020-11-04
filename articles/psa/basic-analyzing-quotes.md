---
title: Analys av projektofferter
description: I det här ämnet finns information om hur du analyserar projektofferter.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085656"
---
# <a name="analysis-of-project-quotes"></a>Analys av projektofferter

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
