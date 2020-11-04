---
title: Project Operations-fält som prissättningsdimensioner
description: I det här ämnet finns information om hur du använder befintliga dimensioner i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085603"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="a2b53-103">Project Operations-fält som prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="a2b53-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="a2b53-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="a2b53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a2b53-105">Entiteten **Faktiska värden** har många fält som kan användas som prisdimensioner för resursbaserade priser.</span><span class="sxs-lookup"><span data-stu-id="a2b53-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="a2b53-106">Ett vanligt fält är **Bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="a2b53-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="a2b53-107">Mindre företag som har färre än 20-30 fakturerbara resurser kan upptäcka att fakturerings- och kostnadstaxan som är specifika för varje resurs är en enklare metod.</span><span class="sxs-lookup"><span data-stu-id="a2b53-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="a2b53-108">Eftersom den fakturerbara arbetspersonalen växer kunde emellertid resursspecifika avgifter bli för realistiska.</span><span class="sxs-lookup"><span data-stu-id="a2b53-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="a2b53-109">Resurskostnader och faktureringskostnaderna börjar variera när resurser befordras, får mer erfarenhet eller får en annan uppsättning färdigheter.</span><span class="sxs-lookup"><span data-stu-id="a2b53-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="a2b53-110">Ett annat exempel är det i transaktionskategori.</span><span class="sxs-lookup"><span data-stu-id="a2b53-110">Another example is that of transaction category.</span></span> <span data-ttu-id="a2b53-111">Kunder och implementerare har använt transaktionskategorin för att klassificera arbete och använda fältet till pris och kostnad utifrån arbetskategori.</span><span class="sxs-lookup"><span data-stu-id="a2b53-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
