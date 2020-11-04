---
title: Konfigurera prislista för försäljning
description: I det här ämne finns information om prislista för försäljning för projektprissättning.
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
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085595"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="dc1a9-103">Konfigurera prislista för försäljning</span><span class="sxs-lookup"><span data-stu-id="dc1a9-103">Sales price list setup</span></span>

<span data-ttu-id="dc1a9-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="dc1a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc1a9-105">För projektofferter och kontrakt har en projektprislista ett annat pris för åsidosättningsmönster än en produktprislista.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="dc1a9-106">På en produktkatalogbaserad offertrad kan du åsidosätta priset till roller och kategorier direkt på offertraden, eftersom varje offertrad pekar till exakt ett katalogobjekt.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="dc1a9-107">På en projektrelaterad offertrad kan du emellertid inte åsidosätta priset för roller och kategorier direkt på offertraden.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="dc1a9-108">Du kan använda projektprislistan för att arbeta med de två distinkta åsidosättningarna.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="dc1a9-109">Vi rekommenderar att du har en separat prislista för dina projektresurser och dina katalogobjekt, eftersom det finns skillnader mellan de två när du åsidosätter priserna.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="dc1a9-110">Följande entiteter kan ha en eller flera associerade försäljningsprislistor för projektprissättning:</span><span class="sxs-lookup"><span data-stu-id="dc1a9-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="dc1a9-111">Kund (konto)</span><span class="sxs-lookup"><span data-stu-id="dc1a9-111">Customer (account)</span></span> 
- <span data-ttu-id="dc1a9-112">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="dc1a9-112">Opportunity</span></span> 
- <span data-ttu-id="dc1a9-113">Offert</span><span class="sxs-lookup"><span data-stu-id="dc1a9-113">Quote</span></span> 
- <span data-ttu-id="dc1a9-114">Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="dc1a9-114">Project Contract</span></span>

<span data-ttu-id="dc1a9-115">Associationen mellan dessa entiteter och en prislista visas i projektprislistorna.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="dc1a9-116">Du kan associera en eller flera prislistor med entiteterna kund, affärsmöjlighet, offert och projektkontraktförsäljning.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="dc1a9-117">En standardprislista för projekt anges inte automatiskt i en kundpost.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="dc1a9-118">Du kan emellertid bifoga en projektprislista manuellt till kundposten.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="dc1a9-119">Däremot bör du endast bifoga en projektprislista manuellt när du har ett anpassat prissättningsavtal med kunden.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="dc1a9-120">När en projektpris lista är kopplad till en försäljningsenhet verifieras följande information:</span><span class="sxs-lookup"><span data-stu-id="dc1a9-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="dc1a9-121">Prislistan har kontexten **försäljning**.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="dc1a9-122">Prislistans valuta matchar kundvalutan.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="dc1a9-123">I ett projektkontrakt använder följande prioriteringsordning för att automatiskt ange relaterade projektprislistor:</span><span class="sxs-lookup"><span data-stu-id="dc1a9-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="dc1a9-124">Offert</span><span class="sxs-lookup"><span data-stu-id="dc1a9-124">Quote</span></span>
2. <span data-ttu-id="dc1a9-125">Affärsmöjlighet</span><span class="sxs-lookup"><span data-stu-id="dc1a9-125">Opportunity</span></span>
3. <span data-ttu-id="dc1a9-126">Kund</span><span class="sxs-lookup"><span data-stu-id="dc1a9-126">Customer</span></span> 
4. <span data-ttu-id="dc1a9-127">Globala inställningar</span><span class="sxs-lookup"><span data-stu-id="dc1a9-127">Global settings</span></span> 

<span data-ttu-id="dc1a9-128">När en projektprislista anges som standard verifierar systemet att valutan överensstämmer med kundens valuta och att standardprislistorna som har angetts har kontexten **försäljning**.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="dc1a9-129">Du kan associera flera projektprislistor med entiteterna kund, affärsmöjlighet, offert och projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="dc1a9-130">Den här funktionen har stöd för tidsspecifika standardpriser för ett långvarigt projektkontrakt, där du kan behöva mer än en prislista för att ta hänsyn till prisuppdateringar som sker på grund av inflation.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="dc1a9-131">Om de prislistor som du associerar med en entitet för kund, affärsmöjlighet, offert eller projektkontrakt har överlappande giltighetsdatum kan standardpriset vara fel.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="dc1a9-132">Därför bör du kontrollera att projektprislistor som har överlappande giltighetsdatum inte är associerade med dessa entiteter.</span><span class="sxs-lookup"><span data-stu-id="dc1a9-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
