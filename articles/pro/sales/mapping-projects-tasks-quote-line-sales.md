---
title: Mappa projekt och uppgifter till en projektbaserad offertrad
description: I det här ämnet finns information om hur du mappar projekt och uppgifter till en projektbaserad uppgiftsrad.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964929"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="afb6f-103">Mappa projekt och uppgifter till en projektbaserad offertrad</span><span class="sxs-lookup"><span data-stu-id="afb6f-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="afb6f-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="afb6f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="afb6f-105">På projektbaserade offertrader kan du mappa specifika uppgifter för ett projekt som redan är associerat till en offertrad.</span><span class="sxs-lookup"><span data-stu-id="afb6f-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="afb6f-106">När du mappar uppgifter till en offertrad gäller följande artiklar som du har definierat på offertraden endast för dessa uppgifter:</span><span class="sxs-lookup"><span data-stu-id="afb6f-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="afb6f-107">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="afb6f-107">Billing method</span></span>
- <span data-ttu-id="afb6f-108">Debiterbara alternativ</span><span class="sxs-lookup"><span data-stu-id="afb6f-108">Chargeability options</span></span>
- <span data-ttu-id="afb6f-109">Undre gränser</span><span class="sxs-lookup"><span data-stu-id="afb6f-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="afb6f-110">Kunder</span><span class="sxs-lookup"><span data-stu-id="afb6f-110">Customers</span></span>

<span data-ttu-id="afb6f-111">Du kanske till exempel har ett projekt där en fas är ett fast pris och alla andra faser är tid och material.</span><span class="sxs-lookup"><span data-stu-id="afb6f-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="afb6f-112">I det här fallet kan du associera den första fasen och alla dess underordnade uppgifter till offertraden för den fasen med en faktureringsmetod med fast pris.</span><span class="sxs-lookup"><span data-stu-id="afb6f-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="afb6f-113">Därefter kan du koppla alla andra faser till den tids- och det materialbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="afb6f-114">Associera uppgifter till projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="afb6f-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="afb6f-115">Du kan associera uppgifter med offertrader från följande platser:</span><span class="sxs-lookup"><span data-stu-id="afb6f-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="afb6f-116">Sidan **Projekt** > fliken **Uppgiftsfakturering** (optimal)</span><span class="sxs-lookup"><span data-stu-id="afb6f-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="afb6f-117">Sidan **Offertrad** > fliken **Debiterbara uppgifter**</span><span class="sxs-lookup"><span data-stu-id="afb6f-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="afb6f-118">Från sidan Projekt</span><span class="sxs-lookup"><span data-stu-id="afb6f-118">From the Project page</span></span>

<span data-ttu-id="afb6f-119">Sidan **Projekt** ger den optimala upplevelsen vid associering av uppgifter till offertrader.</span><span class="sxs-lookup"><span data-stu-id="afb6f-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="afb6f-120">Du kan använda den här sidan om du vill välja flera uppgifter och associera alla, plus underordnade uppgifter, till den valda offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="afb6f-121">Under fliken **Allmänt** på en projektbaserad offertrad verifierar du att fältet **Projekt** har fyllts i.</span><span class="sxs-lookup"><span data-stu-id="afb6f-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="afb6f-122">I fältet **Inkluderade uppgifter** väljer du **Endast valda uppgifter**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="afb6f-123">Spara den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-123">Save the project-based quote line.</span></span> <span data-ttu-id="afb6f-124">När formuläret uppdateras visa fliken **Debiterbara uppgifter**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="afb6f-125">Under fliken **Allmänt** väljer du länken för projektet från fältet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="afb6f-126">På sidan **Projekt** väljer du fliken **Uppgiftsfakturering**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="afb6f-127">I det andra rutnätet, som gäller för uppgiftsspecifika faktureringsinställningar, väljer du en eller flera uppgifter och väljer sedan **Associera offertrader**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="afb6f-128">I dialogrutan som visas väljer du en offertrad som visar projektbaserade offertrader i offerten.</span><span class="sxs-lookup"><span data-stu-id="afb6f-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="afb6f-129">I fältet **Faktureringstyp** anger du om dessa uppgifter är debiterbara eller icke debiterbara.</span><span class="sxs-lookup"><span data-stu-id="afb6f-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="afb6f-130">Markera kryssrutan för att ange om associationen ska innehålla underordnade uppgifter för de valda uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="afb6f-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="afb6f-131">Om du markerar rutan associeras de underordnade uppgifterna för de valda uppgifterna till offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="afb6f-132">Stäng dialogrutan genom att välja **OK**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="afb6f-133">Från sidan Offertrad</span><span class="sxs-lookup"><span data-stu-id="afb6f-133">From the Quote line page</span></span>

<span data-ttu-id="afb6f-134">Du kan associera projektuppgifter till offertrader från fliken **Debiterbara uppgifter** på sidan **Offertrad**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="afb6f-135">Det bästa stället att associera projektuppgifter med offertrader finns under fliken **Uppgiftsfakturering** på sidan **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="afb6f-136">Om du associerar uppgifter från fliken **Debiterbara uppgifter** på sidan **Offertrad**, måste du manuellt associera varje projekt.</span><span class="sxs-lookup"><span data-stu-id="afb6f-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="afb6f-137">Under fliken **Allmänt** på en projektbaserad offertrad verifierar du att ett projekt har valts i fältet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="afb6f-138">I fältet **Inkluderade uppgifter** väljer du **Endast valda uppgifter**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="afb6f-139">Spara den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-139">Save the project-based quote line.</span></span> <span data-ttu-id="afb6f-140">När formuläret uppdateras visa fliken **Debiterbara uppgifter**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="afb6f-141">Under fliken **Debiterbara uppgifter** väljer du **Lägg till en offertradsuppgift**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="afb6f-142">På sidan **Offertradsuppgift**, i fältet **Uppgifter**, väljer du uppgiften och i fältet **Faktureringstyp** väljer du **Spara**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="afb6f-143">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="afb6f-143">Close the page.</span></span> <span data-ttu-id="afb6f-144">Den valda uppgiften är nu kopplad till offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="afb6f-145">Avassociera uppgifter från projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="afb6f-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="afb6f-146">Från sidan Projekt</span><span class="sxs-lookup"><span data-stu-id="afb6f-146">From the Project page</span></span>

<span data-ttu-id="afb6f-147">Den här metoden ger den optimala upplevelsen vid avassociering av uppgifter från offertrader.</span><span class="sxs-lookup"><span data-stu-id="afb6f-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="afb6f-148">Du kan välja flera uppgifter och avassociera alla, plus underordnade uppgifter, från den valda offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="afb6f-149">Under fliken **Allmänt** på en projektbaserad offertrad, i fältet **Projekt**, väljer du projektlänken.</span><span class="sxs-lookup"><span data-stu-id="afb6f-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="afb6f-150">På sidan **Projekt** väljer du fliken **Uppgiftsfakturering**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="afb6f-151">I det andra rutnätet, som gäller för uppgiftsspecifika faktureringsinställningar, väljer du en eller flera uppgifter och väljer sedan **Avassociera offertrader**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="afb6f-152">Välj en offertrad på den dialogruta som visas.</span><span class="sxs-lookup"><span data-stu-id="afb6f-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="afb6f-153">Markera kryssrutan för att ange om associationen också ska tas bort från underordnade uppgifter för de valda uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="afb6f-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="afb6f-154">Om du markerar rutan avassocieras även de underordnade uppgifterna för de valda uppgifterna från offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="afb6f-155">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-155">Select **OK**.</span></span> <span data-ttu-id="afb6f-156">Ett varningsmeddelande visas om att du har tagit bort den här associationen. alla verkliga värden som tidigare registrerats för uppgiften kan återföras.</span><span class="sxs-lookup"><span data-stu-id="afb6f-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="afb6f-157">Välj **OK** om du vill fortsätta och ta bort kopplingen mellan uppgiften och den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="afb6f-158">Från sidan Offertrad</span><span class="sxs-lookup"><span data-stu-id="afb6f-158">From the Quote line page</span></span>

<span data-ttu-id="afb6f-159">Du kan även avassociera projektuppgifter från offertrader från fliken **Debiterbara uppgifter** på sidan **Offertrad**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="afb6f-160">Under fliken **Debiterbara uppgifter** väljer du **Ta bort en offertradsuppgift**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="afb6f-161">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="afb6f-161">Select **OK**.</span></span> <span data-ttu-id="afb6f-162">Ett varningsmeddelande visas om att du har tagit bort den här associationen. alla verkliga värden som tidigare registrerats för uppgiften kan återföras.</span><span class="sxs-lookup"><span data-stu-id="afb6f-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="afb6f-163">Välj **OK** om du vill fortsätta och ta bort kopplingen mellan uppgiften och den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="afb6f-164">Med den här proceduren tas inte uppgiften bort från projektet.</span><span class="sxs-lookup"><span data-stu-id="afb6f-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="afb6f-165">Det är bara uppgiftskopplingen som tas bort från den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="afb6f-165">It only removes the task association from the project-based quote line.</span></span>
