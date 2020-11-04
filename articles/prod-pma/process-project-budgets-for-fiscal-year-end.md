---
title: Överför projektbudgetar vid räkenskapsårsslut
description: Den här artikeln innehåller information om hur du kan överföra resterande budgetbelopp till framtida år och skapa budgetregisterinformation.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085673"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="b2850-103">Överför projektbudgetar vid räkenskapsårsslut</span><span class="sxs-lookup"><span data-stu-id="b2850-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2850-104">När du arbetar med ett projekt för flera år kanske du har resterande budget i slutet av räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="b2850-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="b2850-105">Du kan överföra de resterande budgetbeloppen till ett kommande år och skapa budgetregisterinformation för beloppen i de associerade redovisningskontona.</span><span class="sxs-lookup"><span data-stu-id="b2850-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="b2850-106">Innan du överför de återstående beloppen bör du granska och analysera de resterande budgetbeloppen.</span><span class="sxs-lookup"><span data-stu-id="b2850-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="b2850-107">Granska och analysera resterande budgetbelopp</span><span class="sxs-lookup"><span data-stu-id="b2850-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="b2850-108">Följ stegen nedan om du vill granska budgetbeloppen för årets slut för projekt, men inte föra beloppen framåt.</span><span class="sxs-lookup"><span data-stu-id="b2850-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="b2850-109">Gå till **Projekthantering och redovisning** > **Periodisk** > **Budget** > **För budget framåt**.</span><span class="sxs-lookup"><span data-stu-id="b2850-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="b2850-110">På sidan **Process för att föra projektbudget framåt** , under fliken **Alternativ för årsslut** , kontrollerar du att **För återstående budgetbelopp framåt** inte har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="b2850-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="b2850-111">Under fliken **Parametrar** , i fältet **Projektbudgetår** , väljer du det räkenskapsår som du vill visa återstående budgetbelopp för.</span><span class="sxs-lookup"><span data-stu-id="b2850-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="b2850-112">I fältet **Inledande räkenskapsår** väljer du det räkenskapsår som du vill visa återstående budgetbelopp för.</span><span class="sxs-lookup"><span data-stu-id="b2850-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="b2850-113">I fältet **Från prognosmodell** väljer du **Återstående budget**.</span><span class="sxs-lookup"><span data-stu-id="b2850-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="b2850-114">Om du vill ta med projekt som uppfyller de valda villkoren och inte har någon resterande budget väljer du **Visa noll kvar**.</span><span class="sxs-lookup"><span data-stu-id="b2850-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="b2850-115">Under fliken **Välj budget** väljer du **Hämta alla budgetar** för att läsa in alla budgetar som matchar de valda villkoren och väljer sedan **Behandla**.</span><span class="sxs-lookup"><span data-stu-id="b2850-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="b2850-116">Om du vill utforma en databasfråga som läser in en specifik uppsättning budgetar i rutan väljer du **Hämta valda budgetar**.</span><span class="sxs-lookup"><span data-stu-id="b2850-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="b2850-117">Om du vill ha mer information om en specifik rad i fönstret markerar du raden och väljer **Visa budgetinformation** eller **Visa konton**.</span><span class="sxs-lookup"><span data-stu-id="b2850-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="b2850-118">För resterande budgetbelopp framåt</span><span class="sxs-lookup"><span data-stu-id="b2850-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="b2850-119">När du bearbetar resterande budgetbelopp kan du skapa transaktioner i redovisningen för de belopp som du för framåt.</span><span class="sxs-lookup"><span data-stu-id="b2850-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="b2850-120">Skapa redovisningstransaktioner genom att följa stegen i avsnittet [För budgetbelopp framåt och skapa redovisningstransaktioner](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="b2850-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="b2850-121">Budgetbelopp som förs framåt överförs till den prognosmodell som är vald på sidan **Prognosmodeller** som prognosmodell för överföring framåt.</span><span class="sxs-lookup"><span data-stu-id="b2850-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="b2850-122">Föra budgetbelopp framåt och skapa redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="b2850-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="b2850-123">Välj **Projekthantering och redovisning** > **Periodisk** > **Budget** > **För budget framåt**.</span><span class="sxs-lookup"><span data-stu-id="b2850-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="b2850-124">På sidan **Process för att föra projektbudget framåt** väljer du **Årsslut** och aktiverar sedan **För återstående budgetbelopp framåt** och **Skapa budgetregisterposter i redovisningen**.</span><span class="sxs-lookup"><span data-stu-id="b2850-124">On the **Project budget carry-forward process** page, select **Year-end** , and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="b2850-125">Under fliken **Parametrar** , i fältgruppen **Projektparametrar** , väljer du följande:</span><span class="sxs-lookup"><span data-stu-id="b2850-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="b2850-126">**Projektbudgetår** : Välj början av räkenskapsåret för vilket du vill visa återstående budgetbelopp.</span><span class="sxs-lookup"><span data-stu-id="b2850-126">**Project budget year** : Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="b2850-127">**Vinst och förlust** : Skapa vinst- och förlusttransaktioner i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b2850-127">**Profit and loss** : Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="b2850-128">**PIA** : Skapa PIA-transaktioner (pågående arbete) i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b2850-128">**WIP** : Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="b2850-129">**Lön** : Skapa löneallokeringskonton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b2850-129">**Payroll** : Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="b2850-130">I fältgruppen **Redovisning** anger du följande information:</span><span class="sxs-lookup"><span data-stu-id="b2850-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="b2850-131">I fältet **Inledande räkenskapsår** väljer du det räkenskapsår som du vill överföra återstående budgetbelopp till för projekten.</span><span class="sxs-lookup"><span data-stu-id="b2850-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="b2850-132">Standardvärdet är ett år efter värdet i fältet **Projektbudgetår**.</span><span class="sxs-lookup"><span data-stu-id="b2850-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="b2850-133">I fältet **Överföringsperiod** väljer du den period som du vill skapa budgetregisterinformationen för i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b2850-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="b2850-134">Det är vanligtvis den första perioden i det inledande räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="b2850-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="b2850-135">I fältgruppen **Kopiera från/till** anger du följande information:</span><span class="sxs-lookup"><span data-stu-id="b2850-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="b2850-136">I fältet **Från prognosmodell** väljer du den prognosmodell för projektbudget som är kopplad till de resterande budgetbelopp du vill överföra för projekten.</span><span class="sxs-lookup"><span data-stu-id="b2850-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="b2850-137">I fältet **Till transaktionsregistrets budgetmodell** väljer du den budgetmodell för transaktionsregistret som är kopplad till de budgetbelopp du vill överföra till redovisningen.</span><span class="sxs-lookup"><span data-stu-id="b2850-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="b2850-138">Välj **Överför försäljningsvaluta** om du vill använda projektets försäljningsvaluta för de redovisningstransaktioner som skapas när du överför budgetbeloppen för projekten.</span><span class="sxs-lookup"><span data-stu-id="b2850-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="b2850-139">Om alternativet inte är valt används redovisningsvalutan för transaktionerna.</span><span class="sxs-lookup"><span data-stu-id="b2850-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="b2850-140">Välj **Visa noll kvar** om du vill inkludera projekt som inte har några resterande budgetbelopp, men som uppfyller de övriga kriterier som du väljer bland de projekt som visas i den nedre rutan.</span><span class="sxs-lookup"><span data-stu-id="b2850-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="b2850-141">Under fliken **Välj budget** väljer du **Hämta alla budgetar** för att läsa in alla budgetar som matchar de villkor du har valt.</span><span class="sxs-lookup"><span data-stu-id="b2850-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="b2850-142">Om du föredrar att utforma en databasfråga som läser in en specifik uppsättning projektbudgetar i rutan väljer du **Hämta valda budgetar**.</span><span class="sxs-lookup"><span data-stu-id="b2850-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="b2850-143">För varje projekt som du vill bearbeta markerar du alternativet i början av raden för projektet.</span><span class="sxs-lookup"><span data-stu-id="b2850-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="b2850-144">Markera alla eller de flesta av projekten genom att markera kryssrutan längst upp till vänster.</span><span class="sxs-lookup"><span data-stu-id="b2850-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="b2850-145">Avmarkera kryssrutan för det aktuella projektet om du vill utesluta bearbetning av ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b2850-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="b2850-146">Om du vill överföra de resterande budgetbeloppen för de valda projekten till det valda räkenskapsåret och skapa budgetregisterinformation i redovisningen väljer du **Behandla**.</span><span class="sxs-lookup"><span data-stu-id="b2850-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="b2850-147">Föra budgetbelopp framåt utan att skapa redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="b2850-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="b2850-148">Gå till **Projekthantering och redovisning** > **Periodisk** > **Budget** > **För budget framåt**.</span><span class="sxs-lookup"><span data-stu-id="b2850-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="b2850-149">På sidan **Process för att föra projektbudget framåt** , i fältet **Alternativ för årsslut** , väljer du **För återstående budgetbelopp framåt**.</span><span class="sxs-lookup"><span data-stu-id="b2850-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="b2850-150">I gruppen **Parametrar** , i fältet **Projektbudgetår** , väljer du det räkenskapsår som du vill visa återstående budgetbelopp för.</span><span class="sxs-lookup"><span data-stu-id="b2850-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="b2850-151">I gruppen **Kopiera från/till** anger du följande information:</span><span class="sxs-lookup"><span data-stu-id="b2850-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="b2850-152">I fältet **Från prognosmodell** väljer du den prognosmodell för projektbudget som är kopplad till de resterande budgetbelopp som du vill överföra för projekten.</span><span class="sxs-lookup"><span data-stu-id="b2850-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="b2850-153">Välj **Visa noll kvar** om du vill inkludera projekt som inte har något återstående budgetbelopp, men som uppfyller övriga villkor du har valt.</span><span class="sxs-lookup"><span data-stu-id="b2850-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="b2850-154">I gruppen **Välj budget** väljer du **Hämta alla budgetar** för att läsa in alla budgetar som matchar de villkor du har valt.</span><span class="sxs-lookup"><span data-stu-id="b2850-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="b2850-155">Om du vill utforma en databasfråga som läser in en specifik uppsättning projektbudgetar i rutan väljer du **Hämta valda budgetar**.</span><span class="sxs-lookup"><span data-stu-id="b2850-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="b2850-156">För varje projekt som du vill bearbeta markerar du alternativet i början av raden för projektet.</span><span class="sxs-lookup"><span data-stu-id="b2850-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="b2850-157">Välj **Behandla** för att överföra de resterande budgetbeloppen för de valda projekten till det valda räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="b2850-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

