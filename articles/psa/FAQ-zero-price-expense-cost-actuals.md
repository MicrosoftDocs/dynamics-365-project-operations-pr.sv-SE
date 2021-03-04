---
title: Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för utgiftskostnadstillgångar.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146370"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="7bbe8-103">Varför återställs priset till standardvärdet noll för faktiska utgiftskostnader?</span><span class="sxs-lookup"><span data-stu-id="7bbe8-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7bbe8-104">Dessa Vanliga frågor och svar gäller utgiftstillgångar där transaktionsklassen anges som Utgift och transaktionstypen som Kostnad.</span><span class="sxs-lookup"><span data-stu-id="7bbe8-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="7bbe8-105">Felsökning av kostnader för utgiftskostnadstillgångar</span><span class="sxs-lookup"><span data-stu-id="7bbe8-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="7bbe8-106">Gå till posten för relaterade utgifter och se till att det finns ett belopp i fältet för utgifter.</span><span class="sxs-lookup"><span data-stu-id="7bbe8-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="7bbe8-107">Om den ursprungliga utgiftsposten inte hade fyllts i har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="7bbe8-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="7bbe8-108">Lös problemet genom att återskapa utgiftsposten med ett giltigt värde och godkänna den.</span><span class="sxs-lookup"><span data-stu-id="7bbe8-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
