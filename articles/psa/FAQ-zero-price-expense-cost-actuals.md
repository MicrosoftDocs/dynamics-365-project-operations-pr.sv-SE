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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dessa Vanliga frågor och svar gäller utgiftstillgångar där transaktionsklassen anges som Utgift och transaktionstypen som Kostnad.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Felsökning av kostnader för utgiftskostnadstillgångar

Gå till posten för relaterade utgifter och se till att det finns ett belopp i fältet för utgifter. Om den ursprungliga utgiftsposten inte hade fyllts i har du hittat problemet.
 
Lös problemet genom att återskapa utgiftsposten med ett giltigt värde och godkänna den.
