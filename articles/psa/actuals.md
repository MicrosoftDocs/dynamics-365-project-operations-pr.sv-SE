---
title: Översikt över värden
description: I det här ämnet finns information om projektets faktiska värden.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285640"
---
# <a name="actuals-overview"></a><span data-ttu-id="669b0-103">Översikt över värden</span><span class="sxs-lookup"><span data-stu-id="669b0-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="669b0-104">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="669b0-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="669b0-105">Projektets faktiska värden kan spåras tillbaka till källdokumenten.</span><span class="sxs-lookup"><span data-stu-id="669b0-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="669b0-106">Dessa källdokument innehåller både tid, utgift och journaltransaktioner samt fakturor.</span><span class="sxs-lookup"><span data-stu-id="669b0-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Så här spåras projektets faktiska resultat till källdokument](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="669b0-108">Skicka tidspost</span><span class="sxs-lookup"><span data-stu-id="669b0-108">Submitting a time entry</span></span>

<span data-ttu-id="669b0-109">I PSA när en tidspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="669b0-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="669b0-110">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="669b0-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="669b0-111">När en tidspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="669b0-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="669b0-112">Logik för att ange standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="669b0-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="669b0-113">Alla fältvärden från en tidspost kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="669b0-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="669b0-114">Fälten innehåller datumet för transaktionen, kontraktraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="669b0-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="669b0-115">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisatinsenhet** gör att ett korrekt pris anges som standard på journalraden.</span><span class="sxs-lookup"><span data-stu-id="669b0-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="669b0-116">Om du lägger till ett anpassat fält i tidsposten och du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="669b0-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="669b0-117">Skicka en utgiftspost</span><span class="sxs-lookup"><span data-stu-id="669b0-117">Submitting an expense entry</span></span>

<span data-ttu-id="669b0-118">I PSA när en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="669b0-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="669b0-119">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="669b0-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="669b0-120">När en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="669b0-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="669b0-121">Logik för att ange standardpriser för utgifter baseras på den utgiftskategori som är vald på sidan **utgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="669b0-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="669b0-122">Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="669b0-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="669b0-123">För själva priset anges emellertid det belopp som användaren har angett direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning som standard.</span><span class="sxs-lookup"><span data-stu-id="669b0-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="669b0-124">I den aktuella versionen av PSA är kategoribaserade poster av per enhet standardpriser på utgiftposter inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="669b0-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="669b0-125">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="669b0-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="669b0-126">I PSA kan du med hjälp av postjournaler registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="669b0-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="669b0-127">En journal har ett huvud, rader och en **Bekräfta**-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="669b0-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="669b0-128">Här följer några scenarier där du kan använda en journal:</span><span class="sxs-lookup"><span data-stu-id="669b0-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="669b0-129">Du måste registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="669b0-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="669b0-130">Du måste flytta faktiska värden för transaktioner från ett annat system till PSA.</span><span class="sxs-lookup"><span data-stu-id="669b0-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="669b0-131">Du måste registrera kostnader som inträffat i ett annat system, t.ex. inköp eller legotillverkningskostnader.</span><span class="sxs-lookup"><span data-stu-id="669b0-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="669b0-132">Att använda postjournaler för att skapa verkliga värden ska endast utföras av en användare som är helt medveten om den redovisning som påverkar de faktiska värdena för projektet.</span><span class="sxs-lookup"><span data-stu-id="669b0-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="669b0-133">Detta beror på att programmet inte validerar journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="669b0-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="669b0-134">På grund av den här journaltypens påverkan bör du vara försiktig med att få tillgång till skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="669b0-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="669b0-135">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="669b0-135">Recording actuals based on project events</span></span>

<span data-ttu-id="669b0-136">PSA registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="669b0-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="669b0-137">Dessa transaktioner registreras som **faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="669b0-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="669b0-138">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="669b0-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="669b0-139">**Resursen tillhör samma organisationsenhet som projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="669b0-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="669b0-140">Händelse</span><span class="sxs-lookup"><span data-stu-id="669b0-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="669b0-141">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="669b0-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="669b0-142">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="669b0-143">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="669b0-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="669b0-144">Tid och material</span><span class="sxs-lookup"><span data-stu-id="669b0-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="669b0-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="669b0-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="669b0-146">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="669b0-146">Actuals</span></span></th>
<th><span data-ttu-id="669b0-147">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="669b0-147">Transaction currency</span></span></th>
<th><span data-ttu-id="669b0-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="669b0-148">Fixed price</span></span></th>
<th><span data-ttu-id="669b0-149">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="669b0-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="669b0-150">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="669b0-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="669b0-151">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="669b0-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-152">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="669b0-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="669b0-153">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="669b0-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="669b0-154">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="669b0-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="669b0-155">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-155">Cost actual</span></span></td>
<td><span data-ttu-id="669b0-156">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-158">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="669b0-159">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-160">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-161">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="669b0-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="669b0-162">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="669b0-163">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="669b0-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="669b0-164">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-164">Cost actual</span></span></td>
<td><span data-ttu-id="669b0-165">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-167">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-168">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-169">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-170">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="669b0-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="669b0-171">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-172">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="669b0-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="669b0-173">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="669b0-174">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="669b0-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="669b0-175">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="669b0-176">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-177">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="669b0-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-178">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-179">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-180">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-181">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-181">Billed sales</span></span></td>
<td><span data-ttu-id="669b0-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="669b0-183">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="669b0-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="669b0-184">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="669b0-185">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-187">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-188">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-189">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-190">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="669b0-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="669b0-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-192">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="669b0-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="669b0-193">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="669b0-194">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="669b0-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="669b0-195">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="669b0-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="669b0-196">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="669b0-197">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="669b0-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="669b0-198">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="669b0-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="669b0-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-200">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-201">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-202">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-202">Billed sales</span></span></td>
<td><span data-ttu-id="669b0-203">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="669b0-204">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="669b0-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="669b0-205">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="669b0-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="669b0-206">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-207">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="669b0-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="669b0-208">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-209">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="669b0-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="669b0-210">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="669b0-211">**Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="669b0-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="669b0-212">Händelse</span><span class="sxs-lookup"><span data-stu-id="669b0-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="669b0-213">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="669b0-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="669b0-214">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="669b0-215">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="669b0-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="669b0-216">Tid och material</span><span class="sxs-lookup"><span data-stu-id="669b0-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="669b0-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="669b0-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="669b0-218">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="669b0-218">Actuals</span></span></th>
<th><span data-ttu-id="669b0-219">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="669b0-219">Transaction currency</span></span></th>
<th><span data-ttu-id="669b0-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="669b0-220">Fixed price</span></span></th>
<th><span data-ttu-id="669b0-221">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="669b0-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="669b0-222">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="669b0-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="669b0-223">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="669b0-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-224">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="669b0-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="669b0-225">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="669b0-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="669b0-226">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="669b0-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="669b0-227">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-227">Cost actual</span></span></td>
<td><span data-ttu-id="669b0-228">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="669b0-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="669b0-230">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="669b0-231">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="669b0-232">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-233">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="669b0-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="669b0-234">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-235">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="669b0-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="669b0-236">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="669b0-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-237">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="669b0-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="669b0-238">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="669b0-239">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="669b0-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="669b0-240">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-240">Cost actual</span></span></td>
<td><span data-ttu-id="669b0-241">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-243">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-244">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-245">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="669b0-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-246">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="669b0-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="669b0-247">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="669b0-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-248">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="669b0-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="669b0-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="669b0-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-250">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="669b0-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="669b0-251">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-252">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="669b0-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="669b0-253">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="669b0-254">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="669b0-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="669b0-255">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="669b0-256">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-257">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="669b0-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-258">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-259">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="669b0-260">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-261">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-261">Billed sales</span></span></td>
<td><span data-ttu-id="669b0-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="669b0-263">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="669b0-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="669b0-264">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="669b0-265">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-267">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-268">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="669b0-269">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-270">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="669b0-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="669b0-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-272">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="669b0-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="669b0-273">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="669b0-274">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="669b0-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="669b0-275">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="669b0-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="669b0-276">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="669b0-277">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="669b0-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="669b0-278">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="669b0-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="669b0-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-280">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="669b0-281">Saknas</span><span class="sxs-lookup"><span data-stu-id="669b0-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-282">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="669b0-282">Billed sales</span></span></td>
<td><span data-ttu-id="669b0-283">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="669b0-284">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="669b0-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="669b0-285">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="669b0-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="669b0-286">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-287">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="669b0-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="669b0-288">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="669b0-289">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="669b0-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="669b0-290">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="669b0-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]