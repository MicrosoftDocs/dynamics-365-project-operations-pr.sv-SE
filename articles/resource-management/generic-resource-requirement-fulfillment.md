---
title: Allmän uppfyllelse av resurskrav
description: I det här ämnet finns information om hur du bokar namngivna resurser för ett generiskt resursbehov.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897608"
---
# <a name="generic-resource-requirement-fulfillment"></a>Allmän uppfyllelse av resurskrav

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan boka en namngiven resurs och ersätta den generiska resurs som har ett resurskrav.

1. På sidan **projekt** väljer du fliken **Team**.
2. Markera den generiska resurs som har ett resurskrav i listan och klicka på **boka**. Du kan också öppna resurskravet och klicka på **boka**.
3. På sidan **schemaassistenten** markerar du en namngiven resurs som du vill boka i projektteamet och klickar sedan på **boka**.

När bokningen är klar och uppfylls av en namngiven resurs, ersätts den generiska resursen med den namngivna resursen.

Tilldelningarna i schemat uppdateras också med den namngivna resursen.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Utföra en generisk resurs med flera namngivna resurser
Att uppfylla ett krav för en generisk resurs med flera namngivna resurser påminner om att tilldela en enskild namngiven resurs. Det finns till exempel en aktivitet med en varaktighet på fem dagar och 120 timmar. Den här uppgiften kan inte slutföras av en resurs som fungerar på en typisk åtta timmars dag över en vecka på fem dagar. 

Kravet är 120 timmar av robotteknik över fem dagar, vilket är 24 timmar per dag.

Det här är ett exempel på när flera namngivna resurser behövs för att utföra en generisk resursbegäran. Du måste boka flera resurser för att uppfylla kravet.

Den största skillnaden i det här scenariot är att den generiska resursen finns kvar i teamet som tilldelats uppgiften och den bokade namngivna resursteammedlemmen tilldelas inte som en del av befattningen. Projektledaren kan tilldela arbetet så lämpligt som möjligt med de namngivna resurserna. Vyn **avstämningar** kan hjälpa en projektledare att dela upp bokningarna över flera resurser till uppdragstilldelningar. Detta görs inte automatiskt eftersom du i något scenario är mer komplicerat än det enkla exemplet ovan, t.ex. där du har ett paket med uppgifter som utgör behovet, hur projektledaren vill tilldela, måste antas av systemet. Eftersom systemet inte kan tolka vad som är troligt är det att antagandena är annorlunda än avsett och att ett felaktigt eller oförutsägbart resultat inträffar. Det förutsägbara resultatet är att den allmänna resursen fortfarande är tilldelad tills projektledaren har skapat tilldelningar med hjälp av läget **avstämning**.


