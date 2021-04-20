---
title: Konfigurera de debiterbara komponenterna på en offertrad
description: I det här ämnet finns information om hur du konfigurerar debiterbara och icke debiterbara komponenter på en projektbaserad offertrad.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858315"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="0b293-103">Konfigurera debiterbara komponenter på en offertrad</span><span class="sxs-lookup"><span data-stu-id="0b293-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="0b293-104">_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="0b293-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0b293-105">En projektrelaterad offertrad har konceptet av *inkluderade* komponenter och *debiterbara* komponenter.</span><span class="sxs-lookup"><span data-stu-id="0b293-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="0b293-106">Inkluderade komponenter är föremål för följande:</span><span class="sxs-lookup"><span data-stu-id="0b293-106">Included components are subject to:</span></span>

  - <span data-ttu-id="0b293-107">Faktureringsmetod och kunddelning</span><span class="sxs-lookup"><span data-stu-id="0b293-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="0b293-108">Undre gränser</span><span class="sxs-lookup"><span data-stu-id="0b293-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="0b293-109">Inställningar för faktureringsfrekvenser som definierats på den projektbaserade offertraden</span><span class="sxs-lookup"><span data-stu-id="0b293-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="0b293-110">En delmängd av de inkluderade komponenterna kan markeras som debiterbar med hjälp av fältet **Faktureringstyp**.</span><span class="sxs-lookup"><span data-stu-id="0b293-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="0b293-111">Fältet **Faktureringstyp** är en alternativuppsättning som gör det möjligt att använda följande värden i offertradens sammanhang:</span><span class="sxs-lookup"><span data-stu-id="0b293-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="0b293-112">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-112">Chargeable</span></span>
  - <span data-ttu-id="0b293-113">Ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-113">Non-chargeable</span></span>

<span data-ttu-id="0b293-114">Debiterbara komponenter kan definieras för uppgifter, roller och transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="0b293-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="0b293-115">Debiterbarhet anges för uppgifter för en offertrad och gäller alla transaktionsklasser som finns på raden.</span><span class="sxs-lookup"><span data-stu-id="0b293-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="0b293-116">Om fältet **Inkludera uppgifter** är inställt på **Hela projektet** eller är tomt, är fliken **Debiterbara uppgifter** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="0b293-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="0b293-117">Debiterbarhet definieras på roller för en offertrad och gäller endast för transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="0b293-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="0b293-118">Om fältet **Inkludera tid** är inställt på **Nej** på en projektoffertsrad, är fliken **Debiterbara roller** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="0b293-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="0b293-119">Debiterbarhet definieras på transaktionskategorier för en offertrad och gäller endast för transaktionsklassen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="0b293-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="0b293-120">Om fältet **Inkludera utgifter** är inställt på **Nej** på en projektoffertsrad, är fliken **Debiterbara kategorier** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="0b293-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0b293-121">Uppdatera en projektuppgift så att den är debiterbar eller ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0b293-122">En projektuppgift kan vara debiterbar eller ej debiterbar i kontexten för en specifik projektbaserad offertrad, vilket gör följande konfiguration möjlig.</span><span class="sxs-lookup"><span data-stu-id="0b293-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="0b293-123">Om en projektbaserad offertrad innehåller **Tid** och uppgiften **T1** associeras uppgiften till offertraden som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="0b293-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="0b293-124">Om det finns en andra offertrad som inkluderar **Utgifter** kan du associera uppgiften **T1** på offertraden som icke debiterbar.</span><span class="sxs-lookup"><span data-stu-id="0b293-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="0b293-125">Resultatet blir att all tid som registreras på uppgiften är debiterbar och att alla utgifter som registreras på uppgiften är icke debiterbara.</span><span class="sxs-lookup"><span data-stu-id="0b293-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="0b293-126">Faktureringstypen för en uppgift kan konfigureras på **Debiterbara uppgifter** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **offertradens uppgifter**.</span><span class="sxs-lookup"><span data-stu-id="0b293-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="0b293-127">Alternativt kan du uppdatera faktureringstypen för en projektuppgift i **faktureringstyp** fält på undernätet för uppgiftsfakturering för ett projekt som visar offertraderna som är associerade med en uppgift.</span><span class="sxs-lookup"><span data-stu-id="0b293-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0b293-128">Uppdatera en roll så att den är debiterbar eller ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0b293-129">En roll kan vara debiterbar eller inte debiterbar i kontexten för en specifik projektbaserad offertrad.</span><span class="sxs-lookup"><span data-stu-id="0b293-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="0b293-130">Faktureringstypen för roller uppgift kan konfigureras på **Debiterbara roller** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **Debiterbara roller**.</span><span class="sxs-lookup"><span data-stu-id="0b293-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0b293-131">Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0b293-132">En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik offertrad.</span><span class="sxs-lookup"><span data-stu-id="0b293-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="0b293-133">En transaktion faktureringstyp kan konfigureras på **Debiterbara kategorier** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** på underrutnätet **Debiterbara kategorier**.</span><span class="sxs-lookup"><span data-stu-id="0b293-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="0b293-134">Åtgärda debiteringsbarhet</span><span class="sxs-lookup"><span data-stu-id="0b293-134">Resolve chargeability</span></span>
<span data-ttu-id="0b293-135">En beräkning eller faktisk beräkning för tid kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="0b293-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="0b293-136">**Tid** finns med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="0b293-137">**Roll** konfigureras som debiterbar på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="0b293-138">**Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="0b293-139">Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="0b293-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="0b293-140">En beräkning eller faktisk beräkning för utgift kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="0b293-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="0b293-141">**Utgift** finns med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="0b293-142">**Transaktionskategori** konfigureras som debiterbar på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="0b293-143">**Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="0b293-144">Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="0b293-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="0b293-145">En beräkning eller faktisk beräkning för material kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="0b293-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="0b293-146">**Material** finns med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="0b293-147">**Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.</span><span class="sxs-lookup"><span data-stu-id="0b293-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="0b293-148">Om de här två sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="0b293-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-149">
                    <strong>Inkluderar tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="0b293-150">
                    <strong>Inkluderar utgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="0b293-151">
                    <strong>Ta med material</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="0b293-152">
                    <strong>Uppgifter som ingår</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-153">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-155">
                    <strong>Uppgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="0b293-156">
                    <strong>Påverkan av debiterbarhet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-157">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-158">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-159">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-160">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-161">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-162">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-163">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-164">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-165">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-166">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-167">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-168">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-169">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-170">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="0b293-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-171">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-172">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-173">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-174">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-175">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-176">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-177">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-178">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-179">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-180">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="0b293-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-181">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-182">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-183">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-184">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-185">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-186">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-187">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-188">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-189">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-190">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="0b293-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-191">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-192">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-193">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-194">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-195">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-196">Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-197">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-198">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-199">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-200">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="0b293-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-201">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-202">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-203">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-204">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-205">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-206">Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-207">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-208">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-209">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-210">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="0b293-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-211">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-212">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-213">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-214">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-215">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-216">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-217">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-218">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-219">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-220">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-221">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-222">
                    <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-223">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-224">Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-225">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-226">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-227">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-228">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-229">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-230">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-231">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-232">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-233">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-234">Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-235">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-236">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-237">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="0b293-238">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-239">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-240">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-241">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-242">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-243">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-244">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-245">Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-246">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-247">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="0b293-248">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0b293-249">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-250">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-251">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-252">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-253">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-254">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-255">Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-256">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="0b293-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-257">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-258">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="0b293-259">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-260">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-261">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-262">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-263">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-264">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-265">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="0b293-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0b293-266">Faktureringstyp för faktiskt värde för material:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0b293-267">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0b293-268">Ja</span><span class="sxs-lookup"><span data-stu-id="0b293-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="0b293-269">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0b293-270">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="0b293-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0b293-271">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0b293-272">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0b293-273">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="0b293-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0b293-274">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-275">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="0b293-276">Faktureringstyp för faktiskt värde för material: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b293-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
