---
title: Konfigurera de debiterbara komponenterna på en offertrad
description: I det här ämnet finns information om hur du konfigurerar debiterbara och icke debiterbara komponenter på en projektbaserad offertrad.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003788"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="849bd-103">Konfigurera debiterbara komponenter på en offertrad</span><span class="sxs-lookup"><span data-stu-id="849bd-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="849bd-104">_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="849bd-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="849bd-105">En projektrelaterad offertrad har konceptet av *inkluderade* komponenter och *debiterbara* komponenter.</span><span class="sxs-lookup"><span data-stu-id="849bd-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="849bd-106">Inkluderade komponenter är föremål för följande:</span><span class="sxs-lookup"><span data-stu-id="849bd-106">Included components are subject to:</span></span>

  - <span data-ttu-id="849bd-107">Faktureringsmetod och kunddelning</span><span class="sxs-lookup"><span data-stu-id="849bd-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="849bd-108">Undre gränser</span><span class="sxs-lookup"><span data-stu-id="849bd-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="849bd-109">Inställningar för faktureringsfrekvenser som definierats på den projektbaserade offertraden</span><span class="sxs-lookup"><span data-stu-id="849bd-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="849bd-110">En delmängd av de inkluderade komponenterna kan markeras som debiterbar med hjälp av fältet **Faktureringstyp**.</span><span class="sxs-lookup"><span data-stu-id="849bd-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="849bd-111">Fältet **Faktureringstyp** är en alternativuppsättning som gör det möjligt att använda följande värden i offertradens sammanhang:</span><span class="sxs-lookup"><span data-stu-id="849bd-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="849bd-112">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-112">Chargeable</span></span>
  - <span data-ttu-id="849bd-113">Ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-113">Non-chargeable</span></span>

<span data-ttu-id="849bd-114">Debiterbara komponenter kan definieras för uppgifter, roller och transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="849bd-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="849bd-115">Debiterbarhet anges för uppgifter för en offertrad och gäller alla transaktionsklasser som finns på raden.</span><span class="sxs-lookup"><span data-stu-id="849bd-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="849bd-116">Om fältet **Inkludera uppgifter** är inställt på **Hela projektet** eller är tomt, är fliken **Debiterbara uppgifter** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="849bd-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="849bd-117">Debiterbarhet definieras på roller för en offertrad och gäller endast för transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="849bd-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="849bd-118">Om fältet **Inkludera tid** är inställt på **Nej** på en projektoffertsrad, är fliken **Debiterbara roller** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="849bd-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="849bd-119">Debiterbarhet definieras på transaktionskategorier för en offertrad och gäller endast för transaktionsklassen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="849bd-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="849bd-120">Om fältet **Inkludera utgifter** är inställt på **Nej** på en projektoffertsrad, är fliken **Debiterbara kategorier** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="849bd-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="849bd-121">Uppdatera en projektuppgift så att den är debiterbar eller ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="849bd-122">En projektuppgift kan vara debiterbar eller ej debiterbar i kontexten för en specifik projektbaserad offertrad, vilket gör följande konfiguration möjlig.</span><span class="sxs-lookup"><span data-stu-id="849bd-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="849bd-123">Om en projektbaserad offertrad innehåller **Tid** och uppgiften **T1** associeras uppgiften till offertraden som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="849bd-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="849bd-124">Om det finns en andra offertrad som inkluderar **Utgifter** kan du associera uppgiften **T1** på offertraden som icke debiterbar.</span><span class="sxs-lookup"><span data-stu-id="849bd-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="849bd-125">Resultatet blir att all tid som registreras på uppgiften är debiterbar och att alla utgifter som registreras på uppgiften är icke debiterbara.</span><span class="sxs-lookup"><span data-stu-id="849bd-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="849bd-126">Faktureringstypen för en uppgift kan konfigureras på **Debiterbara uppgifter** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **offertradens uppgifter**.</span><span class="sxs-lookup"><span data-stu-id="849bd-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="849bd-127">Alternativt kan du uppdatera faktureringstypen för en projektuppgift i **faktureringstyp** fält på undernätet för uppgiftsfakturering för ett projekt som visar offertraderna som är associerade med en uppgift.</span><span class="sxs-lookup"><span data-stu-id="849bd-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="849bd-128">Uppdatera en roll så att den är debiterbar eller ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="849bd-129">En roll kan vara debiterbar eller inte debiterbar i kontexten för en specifik projektbaserad offertrad.</span><span class="sxs-lookup"><span data-stu-id="849bd-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="849bd-130">Faktureringstypen för roller uppgift kan konfigureras på **Debiterbara roller** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **Debiterbara roller**.</span><span class="sxs-lookup"><span data-stu-id="849bd-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="849bd-131">Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="849bd-132">En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik offertrad.</span><span class="sxs-lookup"><span data-stu-id="849bd-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="849bd-133">En transaktion faktureringstyp kan konfigureras på **Debiterbara kategorier** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** på underrutnätet **Debiterbara kategorier**.</span><span class="sxs-lookup"><span data-stu-id="849bd-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="849bd-134">Åtgärda debiteringsbarhet</span><span class="sxs-lookup"><span data-stu-id="849bd-134">Resolve chargeability</span></span>
<span data-ttu-id="849bd-135">En beräkning eller faktisk beräkning för tid kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="849bd-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="849bd-136">**Tid** finns med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="849bd-137">**Roll** konfigureras som debiterbar på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="849bd-138">**Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="849bd-139">Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="849bd-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="849bd-140">En beräkning eller faktisk beräkning för utgift kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="849bd-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="849bd-141">**Utgift** finns med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="849bd-142">**Transaktionskategori** konfigureras som debiterbar på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="849bd-143">**Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="849bd-144">Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="849bd-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="849bd-145">En beräkning eller faktisk beräkning för material kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="849bd-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="849bd-146">**Material** finns med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="849bd-147">**Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.</span><span class="sxs-lookup"><span data-stu-id="849bd-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="849bd-148">Om de här två sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="849bd-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-149">
                    <strong>Inkluderar tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="849bd-150">
                    <strong>Inkluderar utgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="849bd-151">
                    <strong>Ta med material</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="849bd-152">
                    <strong>Uppgifter som ingår</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-153">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-155">
                    <strong>Uppgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="849bd-156">
                    <strong>Påverkan av debiterbarhet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-157">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-158">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-159">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-160">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-161">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-162">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-163">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-164">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-165">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-166">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-167">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-168">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-169">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-170">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="849bd-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-171">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-172">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-173">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-174">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-175">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-176">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-177">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-178">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-179">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-180">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="849bd-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-181">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-182">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-183">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-184">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-185">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-186">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-187">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-188">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-189">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-190">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="849bd-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-191">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-192">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-193">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-194">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-195">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-196">Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-197">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-198">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-199">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-200">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="849bd-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-201">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-202">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-203">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-204">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-205">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-206">Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-207">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-208">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-209">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-210">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="849bd-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-211">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-212">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-213">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-214">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-215">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-216">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-217">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-218">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-219">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-220">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-221">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-222">
                    <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-223">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-224">Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-225">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-226">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-227">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-228">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-229">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-230">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-231">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-232">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-233">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-234">Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-235">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-236">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-237">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="849bd-238">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-239">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-240">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-241">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-242">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-243">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-244">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-245">Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-246">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-247">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="849bd-248">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="849bd-249">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-250">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-251">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-252">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-253">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-254">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-255">Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-256">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="849bd-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-257">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-258">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="849bd-259">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-260">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-261">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-262">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-263">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-264">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-265">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="849bd-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="849bd-266">Faktureringstyp för faktiskt värde för material:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="849bd-267">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="849bd-268">Ja</span><span class="sxs-lookup"><span data-stu-id="849bd-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="849bd-269">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="849bd-270">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="849bd-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="849bd-271">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="849bd-272">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="849bd-273">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="849bd-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="849bd-274">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-275">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="849bd-276">Faktureringstyp för faktiskt värde för material: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="849bd-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
