---
title: Boka namngivna resurser från resursbehov
description: I det här ämnet finns information om hur du bokar namngivna resurser för ett generiskt resursbehov.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085745"
---
# <a name="book-named-resources-from-resource-requirements"></a>Boka namngivna resurser från resursbehov

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan boka en namngiven resurs och ersätta den generiska resurs som har ett resurskrav.

1. I Project Service Automation (PSA), på sidan **Projekt** , klicka på fliken **Team**.
2. Markera den generiska resurs som har ett resurskrav i listan och klicka på **boka**. Du kan också öppna resurskravet och klicka på **boka**.


![Boka en generisk teammedlem](media/RM-how-to-14.png)


3. På sidan **schemaassistenten** markerar du en namngiven resurs som du vill boka i projektteamet och klickar sedan på **boka**.

![Boka en generisk teammedlem med hjälp av schemaassistenten](media/RM-how-to-15.png)

När bokningen är klar och uppfylls av en namngiven resurs, ersätts den generiska resursen med den namngivna resursen.

![Namngiven teammedlem ersätter ett generisk teammedlem](media/RM-how-to-16.png)

Tilldelningarna i schemat uppdateras också med den namngivna resursen.

![Namngiven teammedlem har tilldelats till projektuppgifter](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Utföra en generisk resurs med flera namngivna resurser
Att uppfylla ett krav för en generisk resurs med flera namngivna resurser påminner om att tilldela en enskild namngiven resurs. Det finns till exempel en aktivitet med en varaktighet på fem dagar och 120 timmar. Den här uppgiften kan inte slutföras av en resurs som fungerar på en typisk åtta timmars dag över en vecka på fem dagar. 

![En uppgift som kräver 120 timmars arbete under fem dagar](media/RM-how-to-21.png)

Kravet är 120 timmar av robotteknik över fem dagar, vilket är 24 timmar per dag.

![Krav per dag](media/RM-how-to-22.png)

Det här är ett exempel på när flera namngivna resurser behövs för att utföra en generisk resursbegäran. Du måste boka flera resurser för att uppfylla kravet.

![Boka flera resurser för att uppfylla kravet.](media/RM-how-to-23.png)

Den största skillnaden i det här scenariot är att den generiska resursen finns kvar i teamet som tilldelats uppgiften och den bokade namngivna resursteammedlemmen tilldelas inte som en del av befattningen. Projektledaren kan tilldela arbetet så lämpligt som möjligt med de namngivna resurserna. Vyn **avstämningar** kan hjälpa en projektledare att dela upp bokningarna över flera resurser till uppdragstilldelningar. Detta görs inte automatiskt eftersom du i något scenario är mer komplicerat än det enkla exemplet ovan, t.ex. där du har ett paket med uppgifter som utgör behovet, hur projektledaren vill tilldela, måste antas av systemet. Eftersom systemet inte kan tolka vad som är troligt är det att antagandena är annorlunda än avsett och att ett felaktigt eller oförutsägbart resultat inträffar. Det förutsägbara resultatet är att den allmänna resursen fortfarande är tilldelad tills projektledaren har skapat tilldelningar med hjälp av läget **avstämning**.

