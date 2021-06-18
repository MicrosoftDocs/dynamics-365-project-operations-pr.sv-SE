---
title: Granska föreslagna resurser
description: I det här ämnet finns information om hur du föreslår projektresurser.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000773"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="9b609-103">Granska föreslagna resurser</span><span class="sxs-lookup"><span data-stu-id="9b609-103">Review proposed resources</span></span>

<span data-ttu-id="9b609-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="9b609-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9b609-105">Resursansvariga kan föreslå en resurs till projektledaren genom att använda en resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="9b609-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="9b609-106">Från rutnätet för begäran eller själva begäran, välj **Hitta resurser**.</span><span class="sxs-lookup"><span data-stu-id="9b609-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="9b609-107">På sidan **schemaassistent** markerar du resursen och väljer rutan **Skapa resursbokning** i fältet **bokningsstatus** och väljer **boka**.</span><span class="sxs-lookup"><span data-stu-id="9b609-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="9b609-108">Följande statusuppdateringar inträffar:</span><span class="sxs-lookup"><span data-stu-id="9b609-108">The following status updates occur:</span></span>

- <span data-ttu-id="9b609-109">På sidan **schemaläggningsassistent** uppdateras statusindikatorerna för att indikera att bokningen är föreslagen, inte en fast bokade.</span><span class="sxs-lookup"><span data-stu-id="9b609-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="9b609-110">I resursbegäran ändras status till **måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="9b609-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="9b609-111">På fliken **team** i projektet ändras värdet för den allmänna teammedlemmens **Status för begäran** till **måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="9b609-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="9b609-112">Projektledaren kan antingen acceptera eller avvisa förslaget.</span><span class="sxs-lookup"><span data-stu-id="9b609-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="9b609-113">När resursansvariga behandlar resursbegäranden kan de använda någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="9b609-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="9b609-114">Föreslå flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att uppfylla de timmar som krävs.</span><span class="sxs-lookup"><span data-stu-id="9b609-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="9b609-115">Föreslagna timmar delas sedan mellan flera resurser som kan uppfylla de begärda timmarna.</span><span class="sxs-lookup"><span data-stu-id="9b609-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="9b609-116">I det här scenariot kan timmarna inte överlappas.</span><span class="sxs-lookup"><span data-stu-id="9b609-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="9b609-117">Föreslå färre resurser än vad som krävs.</span><span class="sxs-lookup"><span data-stu-id="9b609-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="9b609-118">I det här scenariot är den föreslagna resurskapaciteten mindre än de timmar som begärdes av den begärande.</span><span class="sxs-lookup"><span data-stu-id="9b609-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="9b609-119">När den som beställt accepterar de föreslagna resurserna skapas därför ett ouppfyllt resursbehov som fångar upp det återstående behovet.</span><span class="sxs-lookup"><span data-stu-id="9b609-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="9b609-120">Boka flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att slutföra arbetet.</span><span class="sxs-lookup"><span data-stu-id="9b609-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="9b609-121">Boka färre resurser än vad som krävs.</span><span class="sxs-lookup"><span data-stu-id="9b609-121">Book fewer resources than are required.</span></span> <span data-ttu-id="9b609-122">I det här scenariot är bokade timmar färre än de timmar som krävs.</span><span class="sxs-lookup"><span data-stu-id="9b609-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="9b609-123">Systemet hjälper dig att föreslå resurser i stället för bokningar, så att den som gör en förfrågan kan verifiera och hålla ordning på återstående efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="9b609-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="9b609-124">Resurstillgänglighet</span><span class="sxs-lookup"><span data-stu-id="9b609-124">Resource availability</span></span>

<span data-ttu-id="9b609-125">Det är viktigt att resursansvariga kan visa tillgängligheten till resurser och uppdatera bokningar.</span><span class="sxs-lookup"><span data-stu-id="9b609-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="9b609-126">I vissa fall finns ingen formell efterfrågan (resursbegäran), men en resursansvarig måste svara på en oplanerad efterfrågan som sker via kanaler som e-post, telefonsamtal eller snabbmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="9b609-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="9b609-127">Resursansvariga kan uppdatera resurser och bokningar med hjälp av schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="9b609-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="9b609-128">Resursens arbetstider används som grund för att beräkna resursens tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="9b609-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="9b609-129">Resursbokningarna förbrukar kapaciteterna för resurserna.</span><span class="sxs-lookup"><span data-stu-id="9b609-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="9b609-130">I schemaläggningstavlan används färger och fyllning för att visa bokningar, tillgänglighet och förbokningar samt även status för bokningar.</span><span class="sxs-lookup"><span data-stu-id="9b609-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="9b609-131">En inställning i schemaläggningstavlan gör att du kan visa en förklaring.</span><span class="sxs-lookup"><span data-stu-id="9b609-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="9b609-132">Om en högerriktad pil visas bredvid en enskild bokningsbar resurs på schemaläggningstavlan kan resursen expanderas så att den innehåller information om det arbete som resursen är bokad på.</span><span class="sxs-lookup"><span data-stu-id="9b609-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="9b609-133">Eftersom Dynamics 365 Project Operations använder Universal Resource Scheduling-motorn, om du även har Dynamics 365 Field Service installerat kan du visa information om resursbokningar för projekt, arbetsorder och andra entiteter som du har utvidgat schemaläggning till.</span><span class="sxs-lookup"><span data-stu-id="9b609-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="9b609-134">Om du vill visa mer information om en enskild resurs högerklickar du på den så att resurskortet öppnas.</span><span class="sxs-lookup"><span data-stu-id="9b609-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]