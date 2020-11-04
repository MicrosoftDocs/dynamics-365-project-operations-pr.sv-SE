---
title: Allmän uppfyllelse av resurskrav
description: I det här ämnet finns information om hur du bokar namngivna resurser för ett generiskt resursbehov.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085485"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="7e330-103">Allmän uppfyllelse av resurskrav</span><span class="sxs-lookup"><span data-stu-id="7e330-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="7e330-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="7e330-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7e330-105">Du kan boka en namngiven resurs och ersätta den generiska resurs som har ett resurskrav.</span><span class="sxs-lookup"><span data-stu-id="7e330-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="7e330-106">På sidan **projekt** väljer du fliken **Team**.</span><span class="sxs-lookup"><span data-stu-id="7e330-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="7e330-107">Markera den generiska resurs som har ett resurskrav i listan och klicka på **boka**.</span><span class="sxs-lookup"><span data-stu-id="7e330-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="7e330-108">Du kan också öppna resurskravet och klicka på **boka**.</span><span class="sxs-lookup"><span data-stu-id="7e330-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="7e330-109">På sidan **schemaassistenten** markerar du en namngiven resurs som du vill boka i projektteamet och klickar sedan på **boka**.</span><span class="sxs-lookup"><span data-stu-id="7e330-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="7e330-110">När bokningen är klar och uppfylls av en namngiven resurs, ersätts den generiska resursen med den namngivna resursen.</span><span class="sxs-lookup"><span data-stu-id="7e330-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="7e330-111">Tilldelningarna i schemat uppdateras också med den namngivna resursen.</span><span class="sxs-lookup"><span data-stu-id="7e330-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="7e330-112">Utföra en generisk resurs med flera namngivna resurser</span><span class="sxs-lookup"><span data-stu-id="7e330-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="7e330-113">Att uppfylla ett krav för en generisk resurs med flera namngivna resurser påminner om att tilldela en enskild namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="7e330-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="7e330-114">Det finns till exempel en aktivitet med en varaktighet på fem dagar och 120 timmar.</span><span class="sxs-lookup"><span data-stu-id="7e330-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="7e330-115">Den här uppgiften kan inte slutföras av en resurs som fungerar på en typisk åtta timmars dag över en vecka på fem dagar.</span><span class="sxs-lookup"><span data-stu-id="7e330-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="7e330-116">Kravet är 120 timmar av robotteknik över fem dagar, vilket är 24 timmar per dag.</span><span class="sxs-lookup"><span data-stu-id="7e330-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="7e330-117">Det här är ett exempel på när flera namngivna resurser behövs för att utföra en generisk resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="7e330-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="7e330-118">Du måste boka flera resurser för att uppfylla kravet.</span><span class="sxs-lookup"><span data-stu-id="7e330-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="7e330-119">Den största skillnaden i det här scenariot är att den generiska resursen finns kvar i teamet som tilldelats uppgiften och den bokade namngivna resursteammedlemmen tilldelas inte som en del av befattningen.</span><span class="sxs-lookup"><span data-stu-id="7e330-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="7e330-120">Projektledaren kan tilldela arbetet så lämpligt som möjligt med de namngivna resurserna.</span><span class="sxs-lookup"><span data-stu-id="7e330-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="7e330-121">Vyn **avstämningar** kan hjälpa en projektledare att dela upp bokningarna över flera resurser till uppdragstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="7e330-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="7e330-122">Detta görs inte automatiskt eftersom du i något scenario är mer komplicerat än det enkla exemplet ovan, t.ex. där du har ett paket med uppgifter som utgör behovet, hur projektledaren vill tilldela, måste antas av systemet.</span><span class="sxs-lookup"><span data-stu-id="7e330-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="7e330-123">Eftersom systemet inte kan tolka vad som är troligt är det att antagandena är annorlunda än avsett och att ett felaktigt eller oförutsägbart resultat inträffar.</span><span class="sxs-lookup"><span data-stu-id="7e330-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="7e330-124">Det förutsägbara resultatet är att den allmänna resursen fortfarande är tilldelad tills projektledaren har skapat tilldelningar med hjälp av läget **avstämning**.</span><span class="sxs-lookup"><span data-stu-id="7e330-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


