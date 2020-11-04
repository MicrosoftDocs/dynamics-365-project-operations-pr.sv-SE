---
title: Skapa avancerade kontrakt för fakturering baserad på förlopp
description: I det här ämnet beskrivs hur du skapar projektkontrakt så att du kan skapa fakturor för kunder, baserat på en procent färdigt arbete.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085669"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="9679a-103">Skapa avancerade kontrakt för fakturering baserad på förlopp</span><span class="sxs-lookup"><span data-stu-id="9679a-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="9679a-104">I det här ämnet beskrivs hur du skapar projektkontrakt så att du kan skapa fakturor för kunder, baserat på en procent färdigt arbete.</span><span class="sxs-lookup"><span data-stu-id="9679a-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="9679a-105">Fakturabelopp beräknas automatiskt för de budgetkategorier för arbete som du konfigurerar för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9679a-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="9679a-106">Fakturans tidsinställning ställs in när du förhandlar om projektkontraktet med kunden.</span><span class="sxs-lookup"><span data-stu-id="9679a-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="9679a-107">Använd procedurerna i det här ämnet om du vill skapa ett kontrakt, ett associerat projekt och faktureringsregler som beräknar fakturabelopp för de budgetkategorier som du konfigurerar för projektet.</span><span class="sxs-lookup"><span data-stu-id="9679a-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="9679a-108">När du har skapat kontraktet och projektet kan du ange information om projektet.</span><span class="sxs-lookup"><span data-stu-id="9679a-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="9679a-109">Du kan till exempel definiera aktiviteter och tilldela arbetare till projektet.</span><span class="sxs-lookup"><span data-stu-id="9679a-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="9679a-110">Exempel</span><span class="sxs-lookup"><span data-stu-id="9679a-110">Example</span></span>

<span data-ttu-id="9679a-111">Din organisation är ett företag för programutveckling.</span><span class="sxs-lookup"><span data-stu-id="9679a-111">Your organization is a software development firm.</span></span> <span data-ttu-id="9679a-112">Du samtycker till att utveckla ett paket för löneredovisning för en kund för en total avgift på 20 000 dollar (USD).</span><span class="sxs-lookup"><span data-stu-id="9679a-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="9679a-113">Din organisation går med på att fakturera kunden allt eftersom du slutför specifika delar av projektet.</span><span class="sxs-lookup"><span data-stu-id="9679a-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="9679a-114">Du kan ange följande projektkategorier för arbetet, så att du kan använda dem i faktureringsprocessen:</span><span class="sxs-lookup"><span data-stu-id="9679a-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="9679a-115">Konsultverksamhet</span><span class="sxs-lookup"><span data-stu-id="9679a-115">Consulting</span></span>
- <span data-ttu-id="9679a-116">Design</span><span class="sxs-lookup"><span data-stu-id="9679a-116">Design</span></span>
- <span data-ttu-id="9679a-117">Installation</span><span class="sxs-lookup"><span data-stu-id="9679a-117">Installation</span></span>

<span data-ttu-id="9679a-118">Du ställer även in faktureringsregler som automatiskt beräknar fakturabeloppen för den procentandel av projektarbetet som slutförts i varje kategori.</span><span class="sxs-lookup"><span data-stu-id="9679a-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="9679a-119">Budgetansvarig skapar en budget för projektkategorierna.</span><span class="sxs-lookup"><span data-stu-id="9679a-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="9679a-120">Mängden färdigt arbete beräknas automatiskt som en procentandel av det faktiska arbetet i jämförelse med de budgeterade beloppen.</span><span class="sxs-lookup"><span data-stu-id="9679a-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9679a-121">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="9679a-121">Prerequisites</span></span>

<span data-ttu-id="9679a-122">Innan du skapar ett projekt som använder faktureringsregler måste du ange nummerserier för faktureringsregler och en avgiftsjournal som används för att bokföra förloppsfaktureringar.</span><span class="sxs-lookup"><span data-stu-id="9679a-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="9679a-123">Gå till **Projektledning och redovisning** \> **Konfiguration** \> **Parametrar för projektledning och redovisning**.</span><span class="sxs-lookup"><span data-stu-id="9679a-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="9679a-124">På sidan **Parametrar för projektledning och redovisning** , under fliken **Nummerserier** , konfigurerar du nummerserier som du vill använda när faktureringsregler skapas.</span><span class="sxs-lookup"><span data-stu-id="9679a-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="9679a-125">Gå till **Projektledning och redovisning** \> **Journaler** \> **Avgift**.</span><span class="sxs-lookup"><span data-stu-id="9679a-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="9679a-126">På sidan **Avgiftsjournal** väljer du **Ny** och anger journalnamnet.</span><span class="sxs-lookup"><span data-stu-id="9679a-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="9679a-127">Skapa ett kontrakt för förloppsfakturering</span><span class="sxs-lookup"><span data-stu-id="9679a-127">Create a contract for progress billings</span></span>

<span data-ttu-id="9679a-128">Använd den här proceduren om du vill skapa ett projektkontrakt för ett fastprisprojekt.</span><span class="sxs-lookup"><span data-stu-id="9679a-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="9679a-129">Du skapar en projektfaktura när det arbete som har slutförts i projektet uppnår en angiven procentsats.</span><span class="sxs-lookup"><span data-stu-id="9679a-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="9679a-130">Gå till **Projektledning och redovisning** \> **Projekt** \> **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="9679a-131">På sidan **Projektkontrakt** väljer du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9679a-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="9679a-132">I dialogrutan **Nytt projektkontrakt** ställer du in följande fält:</span><span class="sxs-lookup"><span data-stu-id="9679a-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="9679a-133">**Namn**</span><span class="sxs-lookup"><span data-stu-id="9679a-133">**Name**</span></span>
    - <span data-ttu-id="9679a-134">**Finansieringstyp**</span><span class="sxs-lookup"><span data-stu-id="9679a-134">**Funding type**</span></span>
    - <span data-ttu-id="9679a-135">**Finansieringskälla**</span><span class="sxs-lookup"><span data-stu-id="9679a-135">**Funding source**</span></span>
    - <span data-ttu-id="9679a-136">**Försäljningsvaluta** – Som standard används valutan för kundfakturor som är associerade med projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="9679a-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="9679a-137">Du kan emellertid ändra försäljningsvalutan på en specifik kundfaktura.</span><span class="sxs-lookup"><span data-stu-id="9679a-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="9679a-138">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="9679a-138">Select **OK**.</span></span> <span data-ttu-id="9679a-139">Informationen kopieras till huvudet på sidan **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="9679a-140">På sidan **Projektkontrakt** fyller du i resten av den information som krävs för projektet.</span><span class="sxs-lookup"><span data-stu-id="9679a-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="9679a-141">Skapa ett projekt för förloppsfakturering</span><span class="sxs-lookup"><span data-stu-id="9679a-141">Create a project for progress billings</span></span>

<span data-ttu-id="9679a-142">Följ stegen nedan om du vill skapa ett projekt och eventuella delprojekt som är associerade med ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="9679a-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="9679a-143">Gå till **Projektledning och redovisning** \> **Projekt** \> **Alla projekt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="9679a-144">På sidan **Alla projekt** väljer du **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="9679a-145">I dialogrutan **Nytt projekt** , i fältet **Projekttyp** , väljer du **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="9679a-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="9679a-146">Välj en projektgrupp.</span><span class="sxs-lookup"><span data-stu-id="9679a-146">Select a project group.</span></span> <span data-ttu-id="9679a-147">En projektgrupp definierar bokföringsinformationen för de projekt som är tilldelade till gruppen.</span><span class="sxs-lookup"><span data-stu-id="9679a-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="9679a-148">Välj **Skapa projekt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-148">Select **Create project**.</span></span>
6. <span data-ttu-id="9679a-149">När projektet har skapats ställer du in projektstadiet på **Pågår**.</span><span class="sxs-lookup"><span data-stu-id="9679a-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="9679a-150">Skapa en budget för ett projekt</span><span class="sxs-lookup"><span data-stu-id="9679a-150">Create a budget for a project</span></span>

<span data-ttu-id="9679a-151">Budgetkategorier används för att automatiskt beräkna fakturabeloppen för den procentandel av arbetet som slutförts för varje kategori.</span><span class="sxs-lookup"><span data-stu-id="9679a-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="9679a-152">Följ stegen nedan om du vill skapa budgetkategorier för de beräknade kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="9679a-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="9679a-153">Gå till **Projektledning och redovisning** \> **Projekt** \> **Alla projekt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="9679a-154">På sidan **Alla projekt** markerar du och öppnar önskat projekt.</span><span class="sxs-lookup"><span data-stu-id="9679a-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="9679a-155">På sidan **Projekt** , i åtgärdsrutan, under fliken **Plan** , i gruppen **Budget** , välj **Projektbudget**.</span><span class="sxs-lookup"><span data-stu-id="9679a-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="9679a-156">På sidan **Projektbudget** anger du en uppskattad kostnad för varje kategori i projektet.</span><span class="sxs-lookup"><span data-stu-id="9679a-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="9679a-157">Skapa faktureringsregler för förloppsfakturering</span><span class="sxs-lookup"><span data-stu-id="9679a-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="9679a-158">Gå till **Projektledning och redovisning** \> **Projekt** \> **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="9679a-159">På sidan **Projektkontrakt** markerar du och öppnar ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="9679a-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="9679a-160">På projektkontraktsidan, under snabbfliken **Faktureringsregler** , väljer du **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="9679a-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="9679a-161">På sidan **Faktureringsregel** , i fältet **Radtyp** , väljer du **Förlopp**.</span><span class="sxs-lookup"><span data-stu-id="9679a-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="9679a-162">Under snabbfliken **Information om rad för faktureringsregel** , i fältet **Kontraktvärde** , anger du det totala värdet för kontraktet.</span><span class="sxs-lookup"><span data-stu-id="9679a-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="9679a-163">I fältet **Kategori** väljer du den kategori som avgiftstransaktionen ska bokföras i.</span><span class="sxs-lookup"><span data-stu-id="9679a-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="9679a-164">I fältet **Projekt** väljer du det projekt som använder den här faktureringsregeln.</span><span class="sxs-lookup"><span data-stu-id="9679a-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="9679a-165">Valfritt: tilldela faktureringsregeln till ytterligare projekt.</span><span class="sxs-lookup"><span data-stu-id="9679a-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="9679a-166">Under snabbfliken **Projekt** , i avsnittet **Tillgängliga projekt** , väljer du ett projekt och sedan högerpilen för att lägga till projektet i avsnittet **Valda projekt**.</span><span class="sxs-lookup"><span data-stu-id="9679a-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="9679a-167">Valfritt: beräkna procentsatsen som kunden håller inne från betalningar på en faktura.</span><span class="sxs-lookup"><span data-stu-id="9679a-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="9679a-168">Under snabbfliken **Villkor för innehållen betalning** väljer du finansieringskälla och sedan, i fältet **Innehållen procentsats** , anger du innehållen procentsats.</span><span class="sxs-lookup"><span data-stu-id="9679a-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="9679a-169">Upprepa stegen för att skapa ytterligare faktureringsregler för projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="9679a-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
