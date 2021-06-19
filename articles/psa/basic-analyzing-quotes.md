---
title: Analys av projektofferter
description: I det här ämnet finns information om hur du analyserar projektofferter.
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012473"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="72642-103">Analys av projektofferter</span><span class="sxs-lookup"><span data-stu-id="72642-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="72642-104">Dynamics 365 Project Service Automation analyserar projektofferter för uppskattning av lönsamheten.</span><span class="sxs-lookup"><span data-stu-id="72642-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="72642-105">Den analyserar även hur väl offerten är justerad mot kundförväntningarna om leveransdatum eller slutdatum och om budget.</span><span class="sxs-lookup"><span data-stu-id="72642-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="72642-106">Lönsamhetsanalys</span><span class="sxs-lookup"><span data-stu-id="72642-106">Profitability analysis</span></span>

<span data-ttu-id="72642-107">Project Service Automation analyserar lönsamheten med hjälp av bruttomarginalen och den justerade bruttomarginalen.</span><span class="sxs-lookup"><span data-stu-id="72642-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="72642-108">Bruttomarginaler beräknas med hjälp av följande formel:</span><span class="sxs-lookup"><span data-stu-id="72642-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="72642-109">Den justerade bruttomarginalen beräknas med hjälp av följande formel:</span><span class="sxs-lookup"><span data-stu-id="72642-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="72642-110">Om värdena för bruttomarginal och justerad bruttomarginal skiljer sig åt med en bred marginal, klassificeras mycket av arbetet i offerten som icke debiterbart.</span><span class="sxs-lookup"><span data-stu-id="72642-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="72642-111">Analys av kundens förväntningar</span><span class="sxs-lookup"><span data-stu-id="72642-111">Analysis of customer expectations</span></span>

<span data-ttu-id="72642-112">Du kan analysera offerter och skapa diagram för kundförväntningar om schemat och budgeten om du anger värden för följande fält:</span><span class="sxs-lookup"><span data-stu-id="72642-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="72642-113">Fältet **begärt leveransdatum** i offerthuvudet.</span><span class="sxs-lookup"><span data-stu-id="72642-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="72642-114">Fältet **Kundbudget** för varje offertrad (för projektbaserade rader och produktbaserade rader).</span><span class="sxs-lookup"><span data-stu-id="72642-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="72642-115">Analys av kundens förväntningar om schemat görs genom att jämföra det senaste slutdatumet för offertraddetaljerna med begärt leveransdatum för alla offertrader i offerten.</span><span class="sxs-lookup"><span data-stu-id="72642-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="72642-116">Analys av kundförväntningar för budgeten sker genom att summan av den totala kundbudgeten jämförs med det offererade beloppet över alla offertrader.</span><span class="sxs-lookup"><span data-stu-id="72642-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]