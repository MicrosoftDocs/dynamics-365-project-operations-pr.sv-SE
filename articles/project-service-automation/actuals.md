---
title: Faktiska värden
description: I det här ämnet finns information om projektets faktiska värden.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756278"
---
# <a name="actuals"></a><span data-ttu-id="9f318-103">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9f318-104">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9f318-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="9f318-105">Projektets faktiska värden kan spåras tillbaka till källdokumenten.</span><span class="sxs-lookup"><span data-stu-id="9f318-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="9f318-106">Dessa källdokument innehåller både tid, utgift och journaltransaktioner samt fakturor.</span><span class="sxs-lookup"><span data-stu-id="9f318-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Så här spåras projektets faktiska resultat till källdokument](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="9f318-108">Skicka tidspost</span><span class="sxs-lookup"><span data-stu-id="9f318-108">Submitting a time entry</span></span>

<span data-ttu-id="9f318-109">I PSA när en tidspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="9f318-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="9f318-110">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="9f318-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="9f318-111">När en tidspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="9f318-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="9f318-112">Logik för att ange standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="9f318-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="9f318-113">Alla fältvärden från en tidspost kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="9f318-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="9f318-114">Fälten innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="9f318-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="9f318-115">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisatinsenhet** gör att ett korrekt pris anges som standard på journalraden.</span><span class="sxs-lookup"><span data-stu-id="9f318-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="9f318-116">Om du lägger till ett anpassat fält i tidsposten och du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="9f318-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="9f318-117">Skicka en utgiftspost</span><span class="sxs-lookup"><span data-stu-id="9f318-117">Submitting an expense entry</span></span>

<span data-ttu-id="9f318-118">I PSA när en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="9f318-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="9f318-119">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="9f318-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="9f318-120">När en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="9f318-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="9f318-121">Logik för att ange standardpriser för utgifter baseras på den utgiftskategori som är vald på sidan **utgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="9f318-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="9f318-122">Datumet för transaktionen, kontraktsraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="9f318-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9f318-123">För själva priset anges emellertid det belopp som användaren har angett direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning som standard.</span><span class="sxs-lookup"><span data-stu-id="9f318-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="9f318-124">I den aktuella versionen av PSA är kategoribaserade poster av per enhet standardpriser på utgiftposter inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="9f318-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="9f318-125">Använda journaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="9f318-125">Using journals to record costs</span></span>

<span data-ttu-id="9f318-126">I PSA kan du med hjälp av journaler registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="9f318-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="9f318-127">En journal har ett huvud, rader och en **Bekräfta**-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="9f318-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="9f318-128">Här följer några scenarier där du kan använda en journal:</span><span class="sxs-lookup"><span data-stu-id="9f318-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="9f318-129">Du måste registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9f318-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="9f318-130">Du måste flytta faktiska värden för transaktioner från ett annat system till PSA.</span><span class="sxs-lookup"><span data-stu-id="9f318-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="9f318-131">Du måste registrera kostnader som inträffat i ett annat system, t.ex. inköp eller legotillverkningskostnader.</span><span class="sxs-lookup"><span data-stu-id="9f318-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="9f318-132">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="9f318-132">Recording actuals based on project events</span></span>

<span data-ttu-id="9f318-133">PSA registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9f318-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="9f318-134">Dessa transaktioner registreras som **faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="9f318-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="9f318-135">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="9f318-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="9f318-136">**Resursen tillhör samma organisationsenhet som projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="9f318-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9f318-137">Händelse</span><span class="sxs-lookup"><span data-stu-id="9f318-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9f318-138">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="9f318-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9f318-139">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9f318-140">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="9f318-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9f318-141">Tid och material</span><span class="sxs-lookup"><span data-stu-id="9f318-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9f318-142">Fast pris</span><span class="sxs-lookup"><span data-stu-id="9f318-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9f318-143">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-143">Actuals</span></span></th>
<th><span data-ttu-id="9f318-144">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="9f318-144">Transaction currency</span></span></th>
<th><span data-ttu-id="9f318-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="9f318-145">Fixed price</span></span></th>
<th><span data-ttu-id="9f318-146">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="9f318-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f318-147">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="9f318-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9f318-148">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-149">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="9f318-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9f318-150">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9f318-151">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="9f318-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9f318-152">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-152">Cost actual</span></span></td>
<td><span data-ttu-id="9f318-153">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-154">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-155">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="9f318-156">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-158">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="9f318-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9f318-159">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9f318-160">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="9f318-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9f318-161">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-161">Cost actual</span></span></td>
<td><span data-ttu-id="9f318-162">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-163">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-164">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-165">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-167">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="9f318-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9f318-168">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-169">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="9f318-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9f318-170">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9f318-171">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="9f318-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9f318-172">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9f318-173">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-174">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="9f318-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-175">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-176">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-177">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-178">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-178">Billed sales</span></span></td>
<td><span data-ttu-id="9f318-179">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9f318-180">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="9f318-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9f318-181">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9f318-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-183">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-184">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-185">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-187">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="9f318-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9f318-188">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-189">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="9f318-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9f318-190">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9f318-191">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="9f318-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9f318-192">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="9f318-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9f318-193">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9f318-194">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="9f318-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9f318-195">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="9f318-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9f318-196">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-197">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-198">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-199">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-199">Billed sales</span></span></td>
<td><span data-ttu-id="9f318-200">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9f318-201">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="9f318-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9f318-202">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="9f318-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9f318-203">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-204">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="9f318-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9f318-205">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-206">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="9f318-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9f318-207">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f318-208">**Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="9f318-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9f318-209">Händelse</span><span class="sxs-lookup"><span data-stu-id="9f318-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9f318-210">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="9f318-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9f318-211">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9f318-212">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="9f318-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9f318-213">Tid och material</span><span class="sxs-lookup"><span data-stu-id="9f318-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9f318-214">Fast pris</span><span class="sxs-lookup"><span data-stu-id="9f318-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9f318-215">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-215">Actuals</span></span></th>
<th><span data-ttu-id="9f318-216">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="9f318-216">Transaction currency</span></span></th>
<th><span data-ttu-id="9f318-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="9f318-217">Fixed price</span></span></th>
<th><span data-ttu-id="9f318-218">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="9f318-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f318-219">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="9f318-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9f318-220">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-221">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="9f318-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9f318-222">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="9f318-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9f318-223">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="9f318-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9f318-224">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-224">Cost actual</span></span></td>
<td><span data-ttu-id="9f318-225">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9f318-226">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9f318-227">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9f318-228">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9f318-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-230">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="9f318-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9f318-231">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-232">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="9f318-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9f318-233">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="9f318-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-234">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="9f318-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9f318-235">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9f318-236">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="9f318-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9f318-237">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-237">Cost actual</span></span></td>
<td><span data-ttu-id="9f318-238">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-239">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-240">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-241">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="9f318-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-243">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="9f318-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9f318-244">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="9f318-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-245">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="9f318-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9f318-246">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="9f318-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-247">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="9f318-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9f318-248">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-249">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="9f318-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9f318-250">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9f318-251">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="9f318-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9f318-252">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9f318-253">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-254">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="9f318-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-255">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-256">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9f318-257">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-258">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-258">Billed sales</span></span></td>
<td><span data-ttu-id="9f318-259">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9f318-260">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="9f318-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9f318-261">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9f318-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-263">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-264">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-265">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9f318-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-267">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="9f318-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9f318-268">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-269">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="9f318-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9f318-270">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9f318-271">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="9f318-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9f318-272">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="9f318-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9f318-273">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9f318-274">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="9f318-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9f318-275">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="9f318-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9f318-276">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-277">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9f318-278">Saknas</span><span class="sxs-lookup"><span data-stu-id="9f318-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-279">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="9f318-279">Billed sales</span></span></td>
<td><span data-ttu-id="9f318-280">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9f318-281">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="9f318-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9f318-282">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="9f318-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9f318-283">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-284">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="9f318-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9f318-285">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f318-286">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="9f318-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9f318-287">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="9f318-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
