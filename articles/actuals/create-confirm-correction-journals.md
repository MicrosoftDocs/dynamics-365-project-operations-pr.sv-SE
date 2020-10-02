---
title: Skapa och bekräfta korrigeringsjournaler
description: I det här ämnet finns information om hur du skapar och bekräftar en korrigeringsjournal.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896978"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="23f8b-103">Skapa och bekräfta korrigeringsjournaler</span><span class="sxs-lookup"><span data-stu-id="23f8b-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="23f8b-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="23f8b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23f8b-105">Ibland kan en tid- eller utgiftspost anges felaktigt.</span><span class="sxs-lookup"><span data-stu-id="23f8b-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="23f8b-106">En konsult kan till exempel råka välja fel datum när han eller hon skapar en tidspost, eller också kan de råka transponera värdena när de registrerar en utgift.</span><span class="sxs-lookup"><span data-stu-id="23f8b-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="23f8b-107">Om en konsult inte kan göra uppdateringar av de inskickade posterna kan en administratör korrigera posten för ett projekt direkt.</span><span class="sxs-lookup"><span data-stu-id="23f8b-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="23f8b-108">Du måste ha administratörsbehörigheter för att kunna slutföra procedurerna i den här ämnet.</span><span class="sxs-lookup"><span data-stu-id="23f8b-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="23f8b-109">Korrigera godkända tidsposter</span><span class="sxs-lookup"><span data-stu-id="23f8b-109">Correct approved time entries</span></span>     

<span data-ttu-id="23f8b-110">Utför följande steg för att korrigera enstaka eller flera tidsposter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="23f8b-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="23f8b-111">Välj området **Försäljning**, **Transaktioner** och välj sedan **Godkänd tid**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="23f8b-112">I listan **Godkänd tid** letar du upp och markerar en eller flera godkända tidsposter som du vill korrigera.</span><span class="sxs-lookup"><span data-stu-id="23f8b-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="23f8b-113">Du kan använda filtret för att söka efter relaterade poster.</span><span class="sxs-lookup"><span data-stu-id="23f8b-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="23f8b-114">Du kan till exempel filtrera på ett projekt-ID och sedan välja alla godkända tidsposter med det projekt-ID:t.</span><span class="sxs-lookup"><span data-stu-id="23f8b-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="23f8b-115">Välj **Korrigera poster**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-115">Select **Correct entries**.</span></span> <span data-ttu-id="23f8b-116">En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Tidskorrigering**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="23f8b-117">De valda posterna läggs till i journalen.</span><span class="sxs-lookup"><span data-stu-id="23f8b-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="23f8b-118">På sidan **Ny journal** anger du en **Beskrivning** för din korrigeringsjournal innan du väljer fliken **Korrigeringar för tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="23f8b-119">I avsnittet **Nya värden får tidsposter** uppdaterar du fälten med korrekt information efter behov.</span><span class="sxs-lookup"><span data-stu-id="23f8b-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="23f8b-120">Du kan till exempel ändra det tilldelade projektet eller den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="23f8b-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="23f8b-121">Välj **Förhandsversion**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-121">Select **Preview**.</span></span> <span data-ttu-id="23f8b-122">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="23f8b-123">På fliken **Journalrader** kan du Visa en lista över de ursprungliga faktiska värden som är relaterade till de valda tidssoterna som har återförts och de korrigerade motsvarande raderna som har skapats.</span><span class="sxs-lookup"><span data-stu-id="23f8b-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="23f8b-124">Om du behöver göra ytterligare korrigeringar upprepar du steg 5 och 6.</span><span class="sxs-lookup"><span data-stu-id="23f8b-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="23f8b-125">Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="23f8b-126">Om korrigeringarna visas som de ska väljer du **Bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="23f8b-127">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="23f8b-128">Gå tillbaka till området **Fförsäljning**, välj **Projekt** och öppna sedan projektet som du precis uppdaterat tidstransaktionerna för.</span><span class="sxs-lookup"><span data-stu-id="23f8b-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="23f8b-129">På sidan **Projekt** i fliken **Faktiska värden** kan du se de ändringar du har gjort.</span><span class="sxs-lookup"><span data-stu-id="23f8b-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="23f8b-130">Om fliken **Faktiska värden** inte syns väljer du **Relaterat** > **Faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="23f8b-131">I listan **Associerad vy förö faktiska värden** kan du se att de ursprungliga tidsposter som har återförts fortfarande är listade, liksom även motsvarande korrigerade tidsposter.</span><span class="sxs-lookup"><span data-stu-id="23f8b-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="23f8b-132">I följande bild finns till exempel två radobjekt med kvantiteten 8,00 som har debet förtecknade i kolumnen Belopp.</span><span class="sxs-lookup"><span data-stu-id="23f8b-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="23f8b-133">Det finns också två radobjekt med kvantiteten -8,00 som visar krediterade belopp i kolumnen Belopp.</span><span class="sxs-lookup"><span data-stu-id="23f8b-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="23f8b-134">Dessa korrigeringar ställer in värdet för kvantitet till noll.</span><span class="sxs-lookup"><span data-stu-id="23f8b-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="23f8b-135">Korrigera godkända utgiftsposter</span><span class="sxs-lookup"><span data-stu-id="23f8b-135">Correct approved expense entries</span></span>

<span data-ttu-id="23f8b-136">Följ stegen nedan om du vill korrigera en eller flera utgiftsposter.</span><span class="sxs-lookup"><span data-stu-id="23f8b-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="23f8b-137">I området **Försäljning**: I vänster navigeringsuta, under **Transaktioner**, väljer du **Godkända utgifter**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="23f8b-138">I listan **Godkända utgifter** väljer du det projekt som du vill korrigera och väljer sedan **Korrigera poster**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="23f8b-139">En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Utgiftskorrigering**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="23f8b-140">På sidan **Ny journal** anger du en **Beskrivning** för korrigeringen, och på fliken **Utgiftskorrigering**, i avsnittet **Nya utgiftsvärden**, väljer du de datafält som du vill korrigera för valda utgiftsrader.</span><span class="sxs-lookup"><span data-stu-id="23f8b-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="23f8b-141">Du kan t.ex. tilldela utgiften till ett annat **Projekt** eller korrigera **Utgiftskategori**, **Utgiftsdatum**eller **Bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="23f8b-142">Välj **Förhandsversion**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-142">Select **Preview**.</span></span> <span data-ttu-id="23f8b-143">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="23f8b-144">Bekräfta ändringarna på fliken **Journalrader**. Du kan visa en lista över de ursprungliga, faktiska värden som är relaterade till de valda utgiftsposterna som har återförts och motsvarande, korrigerade raderna som har skapats.</span><span class="sxs-lookup"><span data-stu-id="23f8b-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="23f8b-145">Om de korrigerade värdena visas som de ska väljer du **Bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="23f8b-146">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="23f8b-147">Om värdena inte visas som de ska väljer du **Avbryt** för att gå tillbaka till listan **Godkända utgifter**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="23f8b-148">Upprepa steg 2 till 5.</span><span class="sxs-lookup"><span data-stu-id="23f8b-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="23f8b-149">Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för utgifter**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="23f8b-150">När du har bekräftat korrigeringsjournalen navigerar du tillbaka till det eller de projekt som du uppdaterade och granskar ändringarna.</span><span class="sxs-lookup"><span data-stu-id="23f8b-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="23f8b-151">I fliken **Faktiska värden** på projektsidan granskar du **Associerad vy för faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="23f8b-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="23f8b-152">De ursprungliga posterna och de korrigerade posterna visas i listan.</span><span class="sxs-lookup"><span data-stu-id="23f8b-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="23f8b-153">Följande bild illustrerar ursprungliga utgiftspostbelopp och motsvarande, korrigerade utgiftspostbelopp.</span><span class="sxs-lookup"><span data-stu-id="23f8b-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


