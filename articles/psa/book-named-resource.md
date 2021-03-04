---
title: Boka namngivna resurser från resursbehov
description: I det här ämnet finns information om hur du bokar namngivna resurser för ett generiskt resursbehov.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145132"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="80d57-103">Boka namngivna resurser från resursbehov</span><span class="sxs-lookup"><span data-stu-id="80d57-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="80d57-104">Du kan boka en namngiven resurs och ersätta den generiska resurs som har ett resurskrav.</span><span class="sxs-lookup"><span data-stu-id="80d57-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="80d57-105">I Project Service Automation (PSA), på sidan **Projekt**, klicka på fliken **Team**.</span><span class="sxs-lookup"><span data-stu-id="80d57-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="80d57-106">Markera den generiska resurs som har ett resurskrav i listan och klicka på **boka**.</span><span class="sxs-lookup"><span data-stu-id="80d57-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="80d57-107">Du kan också öppna resurskravet och klicka på **boka**.</span><span class="sxs-lookup"><span data-stu-id="80d57-107">Or, open the resource requirement and then click **Book**.</span></span>


![Boka en generisk teammedlem](media/RM-how-to-14.png)


3. <span data-ttu-id="80d57-109">På sidan **schemaassistenten** markerar du en namngiven resurs som du vill boka i projektteamet och klickar sedan på **boka**.</span><span class="sxs-lookup"><span data-stu-id="80d57-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Boka en generisk teammedlem med hjälp av schemaassistenten](media/RM-how-to-15.png)

<span data-ttu-id="80d57-111">När bokningen är klar och uppfylls av en namngiven resurs, ersätts den generiska resursen med den namngivna resursen.</span><span class="sxs-lookup"><span data-stu-id="80d57-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Namngiven teammedlem ersätter ett generisk teammedlem](media/RM-how-to-16.png)

<span data-ttu-id="80d57-113">Tilldelningarna i schemat uppdateras också med den namngivna resursen.</span><span class="sxs-lookup"><span data-stu-id="80d57-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Namngiven teammedlem har tilldelats till projektuppgifter](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="80d57-115">Utföra en generisk resurs med flera namngivna resurser</span><span class="sxs-lookup"><span data-stu-id="80d57-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="80d57-116">Att uppfylla ett krav för en generisk resurs med flera namngivna resurser påminner om att tilldela en enskild namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="80d57-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="80d57-117">Det finns till exempel en aktivitet med en varaktighet på fem dagar och 120 timmar.</span><span class="sxs-lookup"><span data-stu-id="80d57-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="80d57-118">Den här uppgiften kan inte slutföras av en resurs som fungerar på en typisk åtta timmars dag över en vecka på fem dagar.</span><span class="sxs-lookup"><span data-stu-id="80d57-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![En uppgift som kräver 120 timmars arbete under fem dagar](media/RM-how-to-21.png)

<span data-ttu-id="80d57-120">Kravet är 120 timmar av robotteknik över fem dagar, vilket är 24 timmar per dag.</span><span class="sxs-lookup"><span data-stu-id="80d57-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Krav per dag](media/RM-how-to-22.png)

<span data-ttu-id="80d57-122">Det här är ett exempel på när flera namngivna resurser behövs för att utföra en generisk resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="80d57-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="80d57-123">Du måste boka flera resurser för att uppfylla kravet.</span><span class="sxs-lookup"><span data-stu-id="80d57-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Boka flera resurser för att uppfylla kravet.](media/RM-how-to-23.png)

<span data-ttu-id="80d57-125">Den största skillnaden i det här scenariot är att den generiska resursen finns kvar i teamet som tilldelats uppgiften och den bokade namngivna resursteammedlemmen tilldelas inte som en del av befattningen.</span><span class="sxs-lookup"><span data-stu-id="80d57-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="80d57-126">Projektledaren kan tilldela arbetet så lämpligt som möjligt med de namngivna resurserna.</span><span class="sxs-lookup"><span data-stu-id="80d57-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="80d57-127">Vyn **avstämningar** kan hjälpa en projektledare att dela upp bokningarna över flera resurser till uppdragstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="80d57-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="80d57-128">Detta görs inte automatiskt eftersom du i något scenario är mer komplicerat än det enkla exemplet ovan, t.ex. där du har ett paket med uppgifter som utgör behovet, hur projektledaren vill tilldela, måste antas av systemet.</span><span class="sxs-lookup"><span data-stu-id="80d57-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="80d57-129">Eftersom systemet inte kan tolka vad som är troligt är det att antagandena är annorlunda än avsett och att ett felaktigt eller oförutsägbart resultat inträffar.</span><span class="sxs-lookup"><span data-stu-id="80d57-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="80d57-130">Det förutsägbara resultatet är att den allmänna resursen fortfarande är tilldelad tills projektledaren har skapat tilldelningar med hjälp av läget **avstämning**.</span><span class="sxs-lookup"><span data-stu-id="80d57-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


