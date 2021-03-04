---
title: Masskorrigeringar av faktiska värden som skapats av godkända tid- och utgiftsposter
description: I detta ämne förklaras hur en administratör kan göra enstaka eller masskorrigeringar av tidigare godkända tid- eller utgiftsposter om faktureringen inte är klar.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144975"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="748fc-103">Masskorrigeringar av faktiska värden som skapats av godkända tid- och utgiftsposter</span><span class="sxs-lookup"><span data-stu-id="748fc-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="748fc-104">Ibland kan en tid- eller utgiftspost anges felaktigt.</span><span class="sxs-lookup"><span data-stu-id="748fc-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="748fc-105">En konsult kan till exempel råka välja fel datum när han eller hon skapar en tidspost, eller också kan de råka transponera värdena när de registrerar en utgift.</span><span class="sxs-lookup"><span data-stu-id="748fc-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="748fc-106">Om en konsult inte kan göra uppdateringar av de inskickade posterna kan en administratör korrigera posten för ett projekt direkt.</span><span class="sxs-lookup"><span data-stu-id="748fc-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="748fc-107">Du måste ha administratörsbehörigheter för att kunna slutföra procedurerna i den här ämnet.</span><span class="sxs-lookup"><span data-stu-id="748fc-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="748fc-108">Korrigera godkända tidsposter</span><span class="sxs-lookup"><span data-stu-id="748fc-108">Correct approved time entries</span></span>     

<span data-ttu-id="748fc-109">Utför följande steg för att korrigera enstaka eller flera tidsposter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="748fc-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="748fc-110">Välj området **Försäljning**, **Transaktioner** och välj sedan **Godkänd tid**.</span><span class="sxs-lookup"><span data-stu-id="748fc-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="748fc-111">I listan **Godkänd tid** letar du upp och markerar en eller flera godkända tidsposter som du vill korrigera.</span><span class="sxs-lookup"><span data-stu-id="748fc-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="748fc-112">Du kan använda filtret för att söka efter relaterade poster.</span><span class="sxs-lookup"><span data-stu-id="748fc-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="748fc-113">Du kan till exempel filtrera på ett projekt-ID och sedan välja alla godkända tidsposter med det projekt-ID:t.</span><span class="sxs-lookup"><span data-stu-id="748fc-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="748fc-114">Välj **Korrigera poster**.</span><span class="sxs-lookup"><span data-stu-id="748fc-114">Select **Correct entries**.</span></span> <span data-ttu-id="748fc-115">En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Tidskorrigering**.</span><span class="sxs-lookup"><span data-stu-id="748fc-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="748fc-116">De valda posterna läggs till i journalen.</span><span class="sxs-lookup"><span data-stu-id="748fc-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="748fc-117">På sidan **Ny journal** anger du en **Beskrivning** för din korrigeringsjournal innan du väljer fliken **Korrigeringar för tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="748fc-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="748fc-118">I avsnittet **Nya värden får tidsposter** uppdaterar du fälten med korrekt information efter behov.</span><span class="sxs-lookup"><span data-stu-id="748fc-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="748fc-119">Du kan till exempel ändra det tilldelade projektet eller den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="748fc-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="748fc-120">Välj **Förhandsversion**.</span><span class="sxs-lookup"><span data-stu-id="748fc-120">Select **Preview**.</span></span> <span data-ttu-id="748fc-121">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="748fc-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="748fc-122">På fliken **Journalrader** kan du Visa en lista över de ursprungliga faktiska värden som är relaterade till de valda tidssoterna som har återförts och de korrigerade motsvarande raderna som har skapats.</span><span class="sxs-lookup"><span data-stu-id="748fc-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="748fc-123">Om du behöver göra ytterligare korrigeringar upprepar du steg 5 och 6.</span><span class="sxs-lookup"><span data-stu-id="748fc-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="748fc-124">Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="748fc-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="748fc-125">Om korrigeringarna visas som de ska väljer du **Bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="748fc-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="748fc-126">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="748fc-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="748fc-127">Gå tillbaka till området **Fförsäljning**, välj **Projekt** och öppna sedan projektet som du precis uppdaterat tidstransaktionerna för.</span><span class="sxs-lookup"><span data-stu-id="748fc-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="748fc-128">På sidan **Projekt** i fliken **Faktiska värden** kan du se de ändringar du har gjort.</span><span class="sxs-lookup"><span data-stu-id="748fc-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="748fc-129">Om fliken **Faktiska värden** inte syns väljer du **Relaterat** > **Faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="748fc-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="748fc-130">I listan **Associerad vy förö faktiska värden** kan du se att de ursprungliga tidsposter som har återförts fortfarande är listade, liksom även motsvarande korrigerade tidsposter.</span><span class="sxs-lookup"><span data-stu-id="748fc-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="748fc-131">I följande bild finns till exempel två radobjekt med kvantiteten 8,00 som har debet förtecknade i kolumnen Belopp.</span><span class="sxs-lookup"><span data-stu-id="748fc-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="748fc-132">Det finns också två radobjekt med kvantiteten -8,00 som visar krediterade belopp i kolumnen Belopp.</span><span class="sxs-lookup"><span data-stu-id="748fc-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="748fc-133">Dessa korrigeringar ställer in värdet för kvantitet till noll.</span><span class="sxs-lookup"><span data-stu-id="748fc-133">These corrections bring the quantity to zero.</span></span>

![Associerad vylista för faktiska värden](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="748fc-135">Korrigera godkända utgiftsposter</span><span class="sxs-lookup"><span data-stu-id="748fc-135">Correct approved expense entries</span></span>

<span data-ttu-id="748fc-136">Följ stegen nedan om du vill korrigera en eller flera utgiftsposter.</span><span class="sxs-lookup"><span data-stu-id="748fc-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="748fc-137">I området **Försäljning**: I vänster navigeringsuta, under **Transaktioner**, väljer du **Godkända utgifter**.</span><span class="sxs-lookup"><span data-stu-id="748fc-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="748fc-138">I listan **Godkända utgifter** väljer du det projekt som du vill korrigera och väljer sedan **Korrigera poster**.</span><span class="sxs-lookup"><span data-stu-id="748fc-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="748fc-139">En ny korrigeringsjournal skapas automatiskt med den tilldelade typen **Utgiftskorrigering**.</span><span class="sxs-lookup"><span data-stu-id="748fc-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="748fc-140">På sidan **Ny journal** anger du en **Beskrivning** för korrigeringen, och på fliken **Utgiftskorrigering**, i avsnittet **Nya utgiftsvärden**, väljer du de datafält som du vill korrigera för valda utgiftsrader.</span><span class="sxs-lookup"><span data-stu-id="748fc-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="748fc-141">Du kan t.ex. tilldela utgiften till ett annat **Projekt** eller korrigera **Utgiftskategori**, **Utgiftsdatum** eller **Bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="748fc-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="748fc-142">Välj **Förhandsversion**.</span><span class="sxs-lookup"><span data-stu-id="748fc-142">Select **Preview**.</span></span> <span data-ttu-id="748fc-143">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="748fc-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="748fc-144">Bekräfta ändringarna på fliken **Journalrader**. Du kan visa en lista över de ursprungliga, faktiska värden som är relaterade till de valda utgiftsposterna som har återförts och motsvarande, korrigerade raderna som har skapats.</span><span class="sxs-lookup"><span data-stu-id="748fc-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="748fc-145">Om de korrigerade värdena visas som de ska väljer du **Bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="748fc-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="748fc-146">I dialogrutan markerar du **OK**.</span><span class="sxs-lookup"><span data-stu-id="748fc-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="748fc-147">Om värdena inte visas som de ska väljer du **Avbryt** för att gå tillbaka till listan **Godkända utgifter**.</span><span class="sxs-lookup"><span data-stu-id="748fc-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="748fc-148">Upprepa steg 2 till 5.</span><span class="sxs-lookup"><span data-stu-id="748fc-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="748fc-149">Alla korrigerade faktiska värden kommer att ha samma värden som du valde i avsnittet **Nya värden för utgifter**.</span><span class="sxs-lookup"><span data-stu-id="748fc-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="748fc-150">När du har bekräftat korrigeringsjournalen navigerar du tillbaka till det eller de projekt som du uppdaterade och granskar ändringarna.</span><span class="sxs-lookup"><span data-stu-id="748fc-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="748fc-151">I fliken **Faktiska värden** på projektsidan granskar du **Associerad vy för faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="748fc-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="748fc-152">De ursprungliga posterna och de korrigerade posterna visas i listan.</span><span class="sxs-lookup"><span data-stu-id="748fc-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="748fc-153">Följande bild illustrerar ursprungliga utgiftspostbelopp och motsvarande, korrigerade utgiftspostbelopp.</span><span class="sxs-lookup"><span data-stu-id="748fc-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Faktiska utgifter](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
