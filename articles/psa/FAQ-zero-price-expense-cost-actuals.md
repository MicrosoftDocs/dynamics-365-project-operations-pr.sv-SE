---
title: Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för utgiftskostnadstillgångar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085561"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="06390-103">Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?</span><span class="sxs-lookup"><span data-stu-id="06390-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="06390-104">Dessa Vanliga frågor och svar gäller utgiftstillgångar där transaktionsklassen anges som Utgift och transaktionstypen som Kostnad.</span><span class="sxs-lookup"><span data-stu-id="06390-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="06390-105">Felsökning av kostnader för utgiftskostnadstillgångar</span><span class="sxs-lookup"><span data-stu-id="06390-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="06390-106">Gå till posten för relaterade utgifter och se till att det finns ett belopp i fältet för utgifter.</span><span class="sxs-lookup"><span data-stu-id="06390-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="06390-107">Om den ursprungliga utgiftsposten inte hade fyllts i har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="06390-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="06390-108">Lös problemet genom att återskapa utgiftsposten med ett giltigt värde och godkänna den.</span><span class="sxs-lookup"><span data-stu-id="06390-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
