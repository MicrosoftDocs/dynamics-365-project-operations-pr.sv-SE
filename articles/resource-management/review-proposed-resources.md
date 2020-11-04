---
title: Granska föreslagna resurser
description: I det här ämnet finns information om hur du föreslår projektresurser.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085507"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="fb744-103">Granska föreslagna resurser</span><span class="sxs-lookup"><span data-stu-id="fb744-103">Review proposed resources</span></span>

<span data-ttu-id="fb744-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="fb744-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb744-105">Resursansvariga kan föreslå en resurs till projektledaren genom att använda en resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="fb744-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="fb744-106">Från rutnätet för begäran eller själva begäran, välj **Hitta resurser**.</span><span class="sxs-lookup"><span data-stu-id="fb744-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="fb744-107">På sidan **schemaassistent** markerar du resursen och väljer rutan **Skapa resursbokning** i fältet **bokningsstatus** och väljer **boka**.</span><span class="sxs-lookup"><span data-stu-id="fb744-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="fb744-108">Följande statusuppdateringar inträffar:</span><span class="sxs-lookup"><span data-stu-id="fb744-108">The following status updates occur:</span></span>

- <span data-ttu-id="fb744-109">På sidan **schemaläggningsassistent** uppdateras statusindikatorerna för att indikera att bokningen är föreslagen, inte en fast bokade.</span><span class="sxs-lookup"><span data-stu-id="fb744-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="fb744-110">I resursbegäran ändras status till **måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="fb744-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="fb744-111">På fliken **team** i projektet ändras värdet för den allmänna teammedlemmens **Status för begäran** till **måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="fb744-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="fb744-112">Projektledaren kan antingen acceptera eller avvisa förslaget.</span><span class="sxs-lookup"><span data-stu-id="fb744-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="fb744-113">När resursansvariga behandlar resursbegäranden kan de använda någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="fb744-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="fb744-114">Föreslå flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att uppfylla de timmar som krävs.</span><span class="sxs-lookup"><span data-stu-id="fb744-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="fb744-115">Föreslagna timmar delas sedan mellan flera resurser som kan uppfylla de begärda timmarna.</span><span class="sxs-lookup"><span data-stu-id="fb744-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="fb744-116">I det här scenariot kan timmarna inte överlappas.</span><span class="sxs-lookup"><span data-stu-id="fb744-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="fb744-117">Föreslå färre resurser än vad som krävs.</span><span class="sxs-lookup"><span data-stu-id="fb744-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="fb744-118">I det här scenariot är den föreslagna resurskapaciteten mindre än de timmar som begärdes av den begärande.</span><span class="sxs-lookup"><span data-stu-id="fb744-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="fb744-119">När den som beställt accepterar de föreslagna resurserna skapas därför ett ouppfyllt resursbehov som fångar upp det återstående behovet.</span><span class="sxs-lookup"><span data-stu-id="fb744-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="fb744-120">Boka flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att slutföra arbetet.</span><span class="sxs-lookup"><span data-stu-id="fb744-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="fb744-121">Boka färre resurser än vad som krävs.</span><span class="sxs-lookup"><span data-stu-id="fb744-121">Book fewer resources than are required.</span></span> <span data-ttu-id="fb744-122">I det här scenariot är bokade timmar färre än de timmar som krävs.</span><span class="sxs-lookup"><span data-stu-id="fb744-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="fb744-123">Systemet hjälper dig att föreslå resurser i stället för bokningar, så att den som gör en förfrågan kan verifiera och hålla ordning på återstående efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="fb744-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="fb744-124">Fakturerbar användning</span><span class="sxs-lookup"><span data-stu-id="fb744-124">Billable utilization</span></span>

<span data-ttu-id="fb744-125">Resurser kan ha fakturerbar användning.</span><span class="sxs-lookup"><span data-stu-id="fb744-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="fb744-126">Den här målanvändningen definieras som ett attribut för en resurs standardroll eller anges i posten för den enskilda bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="fb744-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="fb744-127">Användningsberäkningar baseras på de faktiska timmarna som resurserna har rapporterat med hjälp av godkända tidtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="fb744-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="fb744-128">Följande formler används för att beräkna användningen:</span><span class="sxs-lookup"><span data-stu-id="fb744-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="fb744-129">Fakturerbar användning = debiterbara faktiska timmar ÷ resurskapacitet för tillgång</span><span class="sxs-lookup"><span data-stu-id="fb744-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="fb744-130">Användning av ej fakturerbar tid = faktisk tid med faktureringstyp-ID = inte debiterbar, komplementär eller ej disponibelt ÷ resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="fb744-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="fb744-131">Intern = faktisk tid utan försäljningskontrakt ÷ resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="fb744-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="fb744-132">Resurskapacitet = resursens arbetstider – frånvarande – lediga dagar</span><span class="sxs-lookup"><span data-stu-id="fb744-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="fb744-133">Du hittar vyn **Resursutnyttjande** i fönstret **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="fb744-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="fb744-134">Varje cell i rutnätet representerar resursens fakturerbara användningsprocent i en period, t.ex. dag, vecka eller månad.</span><span class="sxs-lookup"><span data-stu-id="fb744-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="fb744-135">Följande formler används för att färglägga cellerna:</span><span class="sxs-lookup"><span data-stu-id="fb744-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="fb744-136">**Grön:** fakturerbart resursutnyttjande \>= resursutnyttjande för målet</span><span class="sxs-lookup"><span data-stu-id="fb744-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="fb744-137">**Gul:** mål för resursutnyttjande – 20 \<= fakturerbart resursutnyttjande \< mål för resursutnyttjande.</span><span class="sxs-lookup"><span data-stu-id="fb744-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="fb744-138">**Röd:** fakturerbart resursutnyttjande \< mål för resursutnyttjande – 20</span><span class="sxs-lookup"><span data-stu-id="fb744-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="fb744-139">Eftersom vyn **Resursutnyttjande** baseras på schemaläggningstavlan kan du filtrera resultaten med hjälp av filtreringsfunktionerna i schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="fb744-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="fb744-140">Rutnätet kräver att du anger ett utnyttjandemål för antingen rollen eller den enskilda resursen.</span><span class="sxs-lookup"><span data-stu-id="fb744-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="fb744-141">För att göra detta går du till **Resurser** \> **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="fb744-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="fb744-142">Dessutom måste en standardroll tilldelas varje bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="fb744-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="fb744-143">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="fb744-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="fb744-144">På fliken **Project Service** kontrollera att en resursroll är definierad och att fältet **är standard** anges till **ja**.</span><span class="sxs-lookup"><span data-stu-id="fb744-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="fb744-145">Du kan lägga till ytterligare roller där **är standard = nej**.</span><span class="sxs-lookup"><span data-stu-id="fb744-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="fb744-146">Rollen där **är standard = ja** används för att utvärdera resursutnyttjande för resursen mot målet för rollen.</span><span class="sxs-lookup"><span data-stu-id="fb744-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="fb744-147">På fliken **Project Service** kan du också ange ett enskilt målutnyttjande för resursen.</span><span class="sxs-lookup"><span data-stu-id="fb744-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="fb744-148">Utnyttjandeberäkningen använder då målutnyttjande för att utvärdera resursens mål i stället för resursens standardroll.</span><span class="sxs-lookup"><span data-stu-id="fb744-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="fb744-149">Utnyttjande visas endast för en resurs om resursen har godkänt, debiterbar tid under den period som visas i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="fb744-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="fb744-150">Resurstillgänglighet</span><span class="sxs-lookup"><span data-stu-id="fb744-150">Resource availability</span></span>

<span data-ttu-id="fb744-151">Det är viktigt att resursansvariga kan visa tillgängligheten till resurser och uppdatera bokningar.</span><span class="sxs-lookup"><span data-stu-id="fb744-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="fb744-152">I vissa fall finns ingen formell efterfrågan (resursbegäran), men en resursansvarig måste svara på en oplanerad efterfrågan som sker via kanaler som e-post, telefonsamtal eller snabbmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="fb744-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="fb744-153">Resursansvariga kan uppdatera resurser och bokningar med hjälp av schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="fb744-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="fb744-154">Resursens arbetstider används som grund för att beräkna resursens tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="fb744-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="fb744-155">Resursbokningarna förbrukar kapaciteterna för resurserna.</span><span class="sxs-lookup"><span data-stu-id="fb744-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="fb744-156">I schemaläggningstavlan används färger och fyllning för att visa bokningar, tillgänglighet och förbokningar samt även status för bokningar.</span><span class="sxs-lookup"><span data-stu-id="fb744-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="fb744-157">En inställning i schemaläggningstavlan gör att du kan visa en förklaring.</span><span class="sxs-lookup"><span data-stu-id="fb744-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="fb744-158">Om en högerriktad pil visas bredvid en enskild bokningsbar resurs på schemaläggningstavlan kan resursen expanderas så att den innehåller information om det arbete som resursen är bokad på.</span><span class="sxs-lookup"><span data-stu-id="fb744-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="fb744-159">Eftersom Dynamics 365 Project Operation använder Universal Resource Scheduling-motorn, om du även har Dynamics 365 Field Service installerat kan du visa information om resursbokningar för projekt, arbetsorder och andra entiteter som du har utvidgat schemaläggning till.</span><span class="sxs-lookup"><span data-stu-id="fb744-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="fb744-160">Om du vill visa mer information om en enskild resurs högerklickar du på den så att resurskortet öppnas.</span><span class="sxs-lookup"><span data-stu-id="fb744-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

