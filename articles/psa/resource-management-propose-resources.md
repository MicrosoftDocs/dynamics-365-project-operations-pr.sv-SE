---
title: Föreslå projektresurser
description: I det här ämnet finns information om hur du föreslår projektresurser.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 18d7dcd95806841c952ea621ec65b513ef614958
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085759"
---
# <a name="propose-project-resources"></a><span data-ttu-id="7c928-103">Föreslå projektresurser</span><span class="sxs-lookup"><span data-stu-id="7c928-103">Propose project resources</span></span>

<span data-ttu-id="7c928-104">Resursansvariga kan föreslå en resurs till projektledaren genom att använda en resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="7c928-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="7c928-105">Från rutnätet för begäran eller själva begäran, välj **Hitta resurser**.</span><span class="sxs-lookup"><span data-stu-id="7c928-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="7c928-106">På sidan **schemaassistent** markerar du resursen och väljer rutan **Skapa resursbokning** i fältet **bokningsstatus** och väljer **boka**.</span><span class="sxs-lookup"><span data-stu-id="7c928-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Föreslagen resurs vald](media/Resource-Management-image62.png)

<span data-ttu-id="7c928-108">Följande statusuppdateringar inträffar:</span><span class="sxs-lookup"><span data-stu-id="7c928-108">The following status updates occur:</span></span>

- <span data-ttu-id="7c928-109">På sidan **schemaläggningsassistent** uppdateras statusindikatorerna för att indikera att bokningen är föreslagen, inte en fast bokade.</span><span class="sxs-lookup"><span data-stu-id="7c928-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Statusindikatorer för föreslagen bokning på sidan schemaläggningsassistenten](media/Resource-Management-image63.png)

- <span data-ttu-id="7c928-111">I resursbegäran ändras status till **måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="7c928-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Resursbegärans status ändrad till måste granskas.](media/Resource-Management-image64.png)

- <span data-ttu-id="7c928-113">På fliken **team** i projektet ändras värdet för den allmänna teammedlemmens **Status för begäran** till **måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="7c928-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Status för begäran för generisk teammedlem ändras till Måste granskas på fliken Team.](media/Resource-Management-image48.png)

<span data-ttu-id="7c928-115">Projektledaren kan antingen acceptera eller avvisa förslaget.</span><span class="sxs-lookup"><span data-stu-id="7c928-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="7c928-116">När resursansvariga behandlar resursbegäranden kan de använda någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="7c928-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="7c928-117">Föreslå flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att uppfylla de timmar som krävs.</span><span class="sxs-lookup"><span data-stu-id="7c928-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="7c928-118">Föreslagna timmar delas sedan mellan flera resurser som kan uppfylla de begärda timmarna.</span><span class="sxs-lookup"><span data-stu-id="7c928-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="7c928-119">I det här scenariot kan timmarna inte överlappas.</span><span class="sxs-lookup"><span data-stu-id="7c928-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="7c928-120">Föreslå färre resurser än vad som krävs.</span><span class="sxs-lookup"><span data-stu-id="7c928-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="7c928-121">I det här scenariot är den föreslagna resurskapaciteten mindre än de timmar som begärdes av den begärande.</span><span class="sxs-lookup"><span data-stu-id="7c928-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="7c928-122">När den som beställt accepterar de föreslagna resurserna skapas därför ett ouppfyllt resursbehov som fångar upp det återstående behovet.</span><span class="sxs-lookup"><span data-stu-id="7c928-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="7c928-123">Boka flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att slutföra arbetet.</span><span class="sxs-lookup"><span data-stu-id="7c928-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="7c928-124">Boka färre resurser än vad som krävs.</span><span class="sxs-lookup"><span data-stu-id="7c928-124">Book fewer resources than are required.</span></span> <span data-ttu-id="7c928-125">I det här scenariot är bokade timmar färre än de timmar som krävs.</span><span class="sxs-lookup"><span data-stu-id="7c928-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="7c928-126">Systemet hjälper dig att föreslå resurser i stället för bokningar, så att den som gör en förfrågan kan verifiera och hålla ordning på återstående efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="7c928-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="7c928-127">Fakturerbar användning</span><span class="sxs-lookup"><span data-stu-id="7c928-127">Billable utilization</span></span>

<span data-ttu-id="7c928-128">Resurser kan ha fakturerbar användning.</span><span class="sxs-lookup"><span data-stu-id="7c928-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="7c928-129">Den här målanvändningen definieras som ett attribut för en resurs standardroll eller anges i posten för den enskilda bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="7c928-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="7c928-130">Användningsberäkningar baseras på de faktiska timmarna som resurserna har rapporterat med hjälp av godkända tidtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7c928-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="7c928-131">Följande formler används för att beräkna användningen:</span><span class="sxs-lookup"><span data-stu-id="7c928-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="7c928-132">Fakturerbar användning = debiterbara faktiska timmar ÷ resurskapacitet för tillgång</span><span class="sxs-lookup"><span data-stu-id="7c928-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="7c928-133">Användning av ej fakturerbar tid = faktisk tid med faktureringstyp-ID = inte debiterbar, komplementär eller ej disponibelt ÷ resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="7c928-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="7c928-134">Intern = faktisk tid utan försäljningskontrakt ÷ resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="7c928-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="7c928-135">Resurskapacitet = resursens arbetstider – frånvarande – lediga dagar</span><span class="sxs-lookup"><span data-stu-id="7c928-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="7c928-136">Du hittar vyn **Resursutnyttjande** i fönstret **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="7c928-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Vy för resursutnyttjande](media/Resource-Management-image65.png)

<span data-ttu-id="7c928-138">Varje cell i rutnätet representerar resursens fakturerbara användningsprocent i en period, t.ex. dag, vecka eller månad.</span><span class="sxs-lookup"><span data-stu-id="7c928-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="7c928-139">Följande formler används för att färglägga cellerna:</span><span class="sxs-lookup"><span data-stu-id="7c928-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="7c928-140">**Grön:** fakturerbart resursutnyttjande \>= resursutnyttjande för målet</span><span class="sxs-lookup"><span data-stu-id="7c928-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="7c928-141">**Gul:** mål för resursutnyttjande – 20 \<= fakturerbart resursutnyttjande \< mål för resursutnyttjande.</span><span class="sxs-lookup"><span data-stu-id="7c928-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="7c928-142">**Röd:** fakturerbart resursutnyttjande \< mål för resursutnyttjande – 20</span><span class="sxs-lookup"><span data-stu-id="7c928-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="7c928-143">Eftersom vyn **Resursutnyttjande** baseras på schemaläggningstavlan kan du filtrera resultaten med hjälp av filtreringsfunktionerna i schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="7c928-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="7c928-144">Rutnätet kräver att du anger ett utnyttjandemål för antingen rollen eller den enskilda resursen.</span><span class="sxs-lookup"><span data-stu-id="7c928-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="7c928-145">För att göra detta går du till **Resurser** \> **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="7c928-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="7c928-146">Dessutom måste en standardroll tilldelas varje bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="7c928-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="7c928-147">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="7c928-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="7c928-148">På fliken **Project Service** kontrollera att en resursroll är definierad och att fältet **är standard** anges till **ja**.</span><span class="sxs-lookup"><span data-stu-id="7c928-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="7c928-149">Du kan lägga till ytterligare roller där **är standard = nej**.</span><span class="sxs-lookup"><span data-stu-id="7c928-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="7c928-150">Rollen där **är standard = ja** används för att utvärdera resursutnyttjande för resursen mot målet för rollen.</span><span class="sxs-lookup"><span data-stu-id="7c928-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Standardrolluppsättning](media/Resource-Management-image67.png)

<span data-ttu-id="7c928-152">På fliken **Project Service** kan du också ange ett enskilt målutnyttjande för resursen.</span><span class="sxs-lookup"><span data-stu-id="7c928-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="7c928-153">Utnyttjandeberäkningen använder då målutnyttjande för att utvärdera resursens mål i stället för resursens standardroll.</span><span class="sxs-lookup"><span data-stu-id="7c928-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="7c928-154">Utnyttjande visas endast för en resurs om resursen har godkänt, debiterbar tid under den period som visas i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="7c928-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="7c928-155">Resurstillgänglighet</span><span class="sxs-lookup"><span data-stu-id="7c928-155">Resource availability</span></span>

<span data-ttu-id="7c928-156">Det är viktigt att resursansvariga kan visa tillgängligheten till resurser och uppdatera bokningar.</span><span class="sxs-lookup"><span data-stu-id="7c928-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="7c928-157">I vissa fall finns ingen formell efterfrågan (resursbegäran), men en resursansvarig måste svara på en oplanerad efterfrågan som sker via kanaler som e-post, telefonsamtal eller snabbmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="7c928-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="7c928-158">Resursansvariga kan uppdatera resurser och bokningar med hjälp av schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="7c928-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="7c928-159">Resursens arbetstider används som grund för att beräkna resursens tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="7c928-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="7c928-160">Resursbokningarna förbrukar kapaciteterna för resurserna.</span><span class="sxs-lookup"><span data-stu-id="7c928-160">Resource bookings consume the capacity of the resources.</span></span>

![Schemaläggningstavla](media/Resource-Management-image68.png)

<span data-ttu-id="7c928-162">I schemaläggningstavlan används färger och fyllning för att visa bokningar, tillgänglighet och förbokningar samt även status för bokningar.</span><span class="sxs-lookup"><span data-stu-id="7c928-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="7c928-163">En inställning i schemaläggningstavlan gör att du kan visa en förklaring.</span><span class="sxs-lookup"><span data-stu-id="7c928-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="7c928-164">Om en högerriktad pil visas bredvid en enskild bokningsbar resurs på schemaläggningstavlan kan resursen expanderas så att den innehåller information om det arbete som resursen är bokad på.</span><span class="sxs-lookup"><span data-stu-id="7c928-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Bokningsbar resurs visas på schemaläggningstavlan](media/Resource-Management-image69.png)

<span data-ttu-id="7c928-166">Eftersom Dynamics 365 Project Service Automation använder Universal Resource Scheduling-motorn, om du även har Dynamics 365 Field Service installerat kan du visa information om resursbokningar för projekt, arbetsorder och andra entiteter som du har utvidgat schemaläggning till.</span><span class="sxs-lookup"><span data-stu-id="7c928-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Information om resursbokningar för projekt och arbetsorder](media/Resource-Management-image70.png)

<span data-ttu-id="7c928-168">Om du vill visa mer information om en enskild resurs högerklickar du på den så att resurskortet öppnas.</span><span class="sxs-lookup"><span data-stu-id="7c928-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Resurskort](media/Resource-Management-image71.png)
