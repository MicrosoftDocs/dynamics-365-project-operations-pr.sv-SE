---
title: Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för utgiftskostnadstillgångar.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756208"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Varför återställs priset till standardvärdet noll för utgiftskostnadstillgångar?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dessa Vanliga frågor och svar gäller utgiftstillgångar där transaktionsklassen anges som Utgift och transaktionstypen som Kostnad.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Felsökning av kostnader för utgiftskostnadstillgångar

Gå till posten för relaterade utgifter och se till att det finns ett belopp i fältet för utgifter. Om den ursprungliga utgiftsposten inte hade fyllts i har du hittat problemet.
 
Lös problemet genom att återskapa utgiftsposten med ett giltigt värde och godkänna den.
