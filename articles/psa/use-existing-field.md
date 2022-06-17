---
title: Använd ett befintligt fält i Project Service som prissättningsdimension
description: I den här artikeln finns information om hur du använder befintliga Project Service-fält som prisdimensioner.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: abc3a3a2b61ea6f8dd34d82bf91546f8f7552a61
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925234"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Använd ett befintligt fält i Project Service som prissättningsdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) har många fält på entiteten **Faktiska värden** som kan användas som prissättningsdimensioner för resursbaserade priser i projektorganisationer. Ett vanligt fält är **Bokningsbar resurs**. Mindre företag som har färre än 20-30 fakturerbara resurser kan upptäcka att fakturerings- och kostnadstaxan som är specifika för varje resurs är en enklare metod. I takt med att den fakturerbara arbetsstyrkan växer kan det emellertid bli orealistiskt att upprätthålla specifika taxor när resurs- och faktureringskostnaderna börjar variera i takt med att resurserna befordras, får mer erfarenheter samt tillgodogör sig olika kompetenser. Eftersom denna metod fortfarande fungerar för företag av en viss storlek går du till [Använd en bokningsbar resurs som prissättningsdimension](bookable-resource-pricing-dimension.md) för att se hur ett befintligt Project Service-fält kan användas som prissättningsdimension.

Ett annat exempel är det i transaktionskategori. Kunder och implementerare har använt transaktionskategorin i PSA för att klassificera arbete och använda fältet till pris och kostnad utifrån arbetskategori. Mer information finns i [använda transaktionskategori som prissättningsdimension](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
