---
title: Använd ett befintligt fält i Project Service som prissättningsdimension
description: I det här ämnet finns information om hur du använder befintliga Project Service-fält som prisdimensioner.
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
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008108"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="f05bc-103">Använd ett befintligt fält i Project Service som prissättningsdimension</span><span class="sxs-lookup"><span data-stu-id="f05bc-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f05bc-104">Project Service Automation (PSA) har många fält på entiteten **Faktiska värden** som kan användas som prissättningsdimensioner för resursbaserade priser i projektorganisationer.</span><span class="sxs-lookup"><span data-stu-id="f05bc-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="f05bc-105">Ett vanligt fält är **Bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="f05bc-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="f05bc-106">Mindre företag som har färre än 20-30 fakturerbara resurser kan upptäcka att fakturerings- och kostnadstaxan som är specifika för varje resurs är en enklare metod.</span><span class="sxs-lookup"><span data-stu-id="f05bc-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="f05bc-107">I takt med att den fakturerbara arbetsstyrkan växer kan det emellertid bli orealistiskt att upprätthålla specifika taxor när resurs- och faktureringskostnaderna börjar variera i takt med att resurserna befordras, får mer erfarenheter samt tillgodogör sig olika kompetenser.</span><span class="sxs-lookup"><span data-stu-id="f05bc-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="f05bc-108">Eftersom denna metod fortfarande fungerar för företag av en viss storlek går du till [Använd en bokningsbar resurs som prissättningsdimension](bookable-resource-pricing-dimension.md) för att se hur ett befintligt Project Service-fält kan användas som prissättningsdimension.</span><span class="sxs-lookup"><span data-stu-id="f05bc-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="f05bc-109">Ett annat exempel är det i transaktionskategori.</span><span class="sxs-lookup"><span data-stu-id="f05bc-109">Another example is that of transaction category.</span></span> <span data-ttu-id="f05bc-110">Kunder och implementerare har använt transaktionskategorin i PSA för att klassificera arbete och använda fältet till pris och kostnad utifrån arbetskategori.</span><span class="sxs-lookup"><span data-stu-id="f05bc-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="f05bc-111">Mer information finns i [använda transaktionskategori som prissättningsdimension](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="f05bc-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]