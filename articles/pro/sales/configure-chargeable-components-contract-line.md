---
title: Konfigurera debiteringsbara komponenter på en projektbaserad kontraktrad
description: I det här ämnet finns information om hur du lägger till debiterbara komponenter i kontraktrader i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858495"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="6898d-103">Konfigurera debiteringsbara komponenter på en projektbaserad kontraktrad</span><span class="sxs-lookup"><span data-stu-id="6898d-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="6898d-104">_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="6898d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6898d-105">En projektrelaterad kontraktrad har *inkluderade* komponenter och *debiterbara* komponenter.</span><span class="sxs-lookup"><span data-stu-id="6898d-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="6898d-106">Inkluderade komponenter är komponenter som är föremål för:</span><span class="sxs-lookup"><span data-stu-id="6898d-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="6898d-107">Faktureringsmetod och kunddelning</span><span class="sxs-lookup"><span data-stu-id="6898d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="6898d-108">Undre gränser</span><span class="sxs-lookup"><span data-stu-id="6898d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="6898d-109">Inställningar för faktureringsfrekvenser som definierats på den projektbaserade kontraktraden</span><span class="sxs-lookup"><span data-stu-id="6898d-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="6898d-110">En delmängd av de inkluderade komponenterna kan markeras som debiterbar med hjälp av fältet **Faktureringstyp**.</span><span class="sxs-lookup"><span data-stu-id="6898d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="6898d-111">Fältet **Faktureringstyp** är en alternativuppsättning som gör det möjligt att använda följande värden i kontraktradens sammanhang:</span><span class="sxs-lookup"><span data-stu-id="6898d-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="6898d-112">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-112">Chargeable</span></span>
  - <span data-ttu-id="6898d-113">Ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-113">Non-chargeable</span></span>

<span data-ttu-id="6898d-114">Debiterbara komponenter kan definieras för uppgifter, roller och transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="6898d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="6898d-115">Debiteringsbarhet anges för uppgifter för en projektkontraktrad och gäller alla transaktionsklasser som finns på raden.</span><span class="sxs-lookup"><span data-stu-id="6898d-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="6898d-116">Om fältet **Inkludera uppgifter** på en kontraktrad är tomt eller har värdet **Hela projektet** är fliken **Debiterbara uppgifter** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="6898d-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="6898d-117">Debiteringsbarhet som definieras på roller för en projektkontraktsrad gäller endast för transaktionsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="6898d-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="6898d-118">Om fältet **Inkludera tid** på en kontraktrad är angiven till **Nej**, är fliken **Debiterbara roller** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="6898d-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="6898d-119">Debiteringsbarhet som definieras på transaktionskategorier för en projektkontraktsrad gäller endast för transaktionsklassen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="6898d-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="6898d-120">Om fältet **Inkludera utgifter** på en kontraktrad är angiven till **Nej**, är fliken **Debiterbara kategorier** inte tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="6898d-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6898d-121">Uppdatera en projektuppgift som debiterbar eller ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="6898d-122">En projektuppgift kan vara debiterbar eller ej debiterbar på en specifik kontraktrad som gör följande inställningar möjliga:</span><span class="sxs-lookup"><span data-stu-id="6898d-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="6898d-123">Om en projektbaserad kontraktrad innehåller **Tid** och en viss uppgift associerad **T1** till den som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="6898d-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="6898d-124">Om det finns en andra kontraktrad som inkluderar **Utgift** kan du associera T1-uppgiften på kontraktraden som icke debiterbar.</span><span class="sxs-lookup"><span data-stu-id="6898d-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="6898d-125">Resultatet blir att all tid som har registrerats på uppgiften är debiterbar och att alla utgifter är icke debiterbara.</span><span class="sxs-lookup"><span data-stu-id="6898d-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="6898d-126">Faktureringstypen för en uppgift kan konfigureras på **Debiterbara uppgifter** på kontraktraden genom att uppdatera fält **Faktureringstyp** i underrutnätet uppgifter i kontraktsraden.</span><span class="sxs-lookup"><span data-stu-id="6898d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="6898d-127">Du kan också uppdatera fältet **faktureringstyp** i underrutnätet i inställningarna för uppgiftsfakturering i ett projekt som visar de kontraktrader som är associerade med en uppgift.</span><span class="sxs-lookup"><span data-stu-id="6898d-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6898d-128">Uppdatera en roll som debiterbar eller ej debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="6898d-129">En roll kan vara debiterbar eller inte debiterbar på en specifik kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="6898d-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6898d-130">En rolls faktureringstyp kan konfigureras under fliken **Debiterbara roller** på en kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="6898d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="6898d-131">Det gör du genom att uppdatera fältet **faktureringstyp** i under rutnätet **debiterbara roller**.</span><span class="sxs-lookup"><span data-stu-id="6898d-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="6898d-132">Uppdatera en transaktionskategori som debiterbar eller inte debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="6898d-133">En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="6898d-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="6898d-134">En transaktions faktureringstyp kan konfigureras under fliken **Debiterbara kategorier** på en projektbaserad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="6898d-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="6898d-135">Det gör du genom att uppdatera fältet **faktureringstyp** i under rutnätet **debiterbara kategorier**.</span><span class="sxs-lookup"><span data-stu-id="6898d-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="6898d-136">Åtgärda debiteringsbarhet</span><span class="sxs-lookup"><span data-stu-id="6898d-136">Resolve chargeability</span></span>

<span data-ttu-id="6898d-137">En beräkning eller faktisk beräkning för tiden kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="6898d-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="6898d-138">**Tid** finns med på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="6898d-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="6898d-139">**Roll** konfigureras som debiterbar på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="6898d-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="6898d-140">**Uppgifter som ingår** anges till **Markerade uppgifter** på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="6898d-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="6898d-141">Om de här tre sakerna stämmer konfigureras uppgiften som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="6898d-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="6898d-142">En beräkning eller faktisk beräkning för utgift kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="6898d-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="6898d-143">**Utgift** finns med på kontraktraden</span><span class="sxs-lookup"><span data-stu-id="6898d-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="6898d-144">**Transaktionskategori** konfigureras som debiterbar på kontraktraden</span><span class="sxs-lookup"><span data-stu-id="6898d-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="6898d-145">**Uppgifter som ingår** anges till **Markerad uppgift** på kontraktraden</span><span class="sxs-lookup"><span data-stu-id="6898d-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="6898d-146">Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="6898d-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="6898d-147">En beräkning eller faktisk beräkning för material kommer endast att anses vara debiterbar om:</span><span class="sxs-lookup"><span data-stu-id="6898d-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="6898d-148">**Material** finns med på kontraktraden</span><span class="sxs-lookup"><span data-stu-id="6898d-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="6898d-149">**Uppgifter som ingår** anges till **Markerade uppgifter** på kontraktraden</span><span class="sxs-lookup"><span data-stu-id="6898d-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="6898d-150">Om de här två sakerna stämmer konfigureras **uppgiften** som debiterbar.</span><span class="sxs-lookup"><span data-stu-id="6898d-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-151">
                    <strong>Inkluderar tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6898d-152">
                    <strong>Inkluderar utgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6898d-153">
                    <strong>Ta med material</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="6898d-154">
                    <strong>Uppgifter som ingår</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-155">
                    <strong>Roll</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-157">
                    <strong>Uppgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="6898d-158">
                    <strong>Påverkan av debiterbarhet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-159">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-160">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-161">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-162">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-163">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-164">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-165">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-166">Fakturering för faktiskt värde för Tid: <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-167">Faktureringstyp för faktiskt värde för Utgift: <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-168">Faktureringstyp för faktiskt material: <strong>Debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-169">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-170">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-171">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-172">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="6898d-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-173">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-174">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-175">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-176">Fakturering för faktiskt värde för Tid: <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-177">Faktureringstyp för faktiskt värde för Utgift: <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-178">Faktureringstyp för faktiskt material: <strong>Debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-179">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-180">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-181">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-182">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="6898d-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-183">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-184">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-185">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-186">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-187">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6898d-188">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-189">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-190">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-191">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-192">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="6898d-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-193">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-194">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-195">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-196">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-197">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-198">Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-199">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-200">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-201">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-202">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="6898d-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-203">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-204">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-205">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-206">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-207">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-208">Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-209">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-210">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-211">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-212">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="6898d-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-213">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-214">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-215">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-216">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-217">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-218">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-219">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-220">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-221">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-222">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-223">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-224">
                    <strong>Debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-225">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-226">Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-227">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6898d-228">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-229">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-230">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-231">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-232">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-233">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-234">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-235">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-236">Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-237">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-238">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-239">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6898d-240">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-241">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-242">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-243">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-244">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-245">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-246">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6898d-247">Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-248">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-249">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="6898d-250">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="6898d-251">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-252">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-253">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-254">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-255">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-256">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-257">Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-258">Faktureringstyp för faktiskt material: Debiterbar</span><span class="sxs-lookup"><span data-stu-id="6898d-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-259">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-260">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6898d-261">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-262">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-263">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-264">Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-265">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-266">Fakturering för faktiskt värde för Tid: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6898d-267">Faktureringstyp för faktiskt värde för Utgift: Debiterbart</span><span class="sxs-lookup"><span data-stu-id="6898d-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="6898d-268">Faktureringstyp för faktiskt värde för material:<strong> Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="6898d-269">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="6898d-270">Ja</span><span class="sxs-lookup"><span data-stu-id="6898d-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="6898d-271">
                    <strong>Inga</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="6898d-272">Hela projektet</span><span class="sxs-lookup"><span data-stu-id="6898d-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="6898d-273">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="6898d-274">
                    <strong>Ej debiterbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="6898d-275">Kan inte anges</span><span class="sxs-lookup"><span data-stu-id="6898d-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="6898d-276">Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-277">Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="6898d-278">Faktureringstyp för faktiskt värde för material: <strong>Inte tillgängligt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6898d-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
