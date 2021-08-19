---
title: Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för utgiftskostnadstillgångar.
author: rumant
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
ms.openlocfilehash: a6e971ff0477d5a9cb8652541095538b9f9039c0870362077218df609871ed4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990968"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Varför återställs priset till standardvärdet noll för faktiska utgiftskostnader?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dessa Vanliga frågor och svar gäller utgiftstillgångar där transaktionsklassen anges som Utgift och transaktionstypen som Kostnad.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Felsökning av kostnader för utgiftskostnadstillgångar

Gå till posten för relaterade utgifter och se till att det finns ett belopp i fältet för utgifter. Om den ursprungliga utgiftsposten inte hade fyllts i har du hittat problemet.
 
Lös problemet genom att återskapa utgiftsposten med ett giltigt värde och godkänna den.


[!INCLUDE[footer-include](../includes/footer-banner.md)]