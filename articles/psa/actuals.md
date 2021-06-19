---
title: Översikt över värden
description: I det här ämnet finns information om projektets faktiska värden.
author: rumant
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
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014678"
---
# <a name="actuals-overview"></a><span data-ttu-id="29f11-103">Översikt över värden</span><span class="sxs-lookup"><span data-stu-id="29f11-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="29f11-104">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="29f11-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="29f11-105">Projektets faktiska värden kan spåras tillbaka till källdokumenten.</span><span class="sxs-lookup"><span data-stu-id="29f11-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="29f11-106">Dessa källdokument innehåller både tid, utgift och journaltransaktioner samt fakturor.</span><span class="sxs-lookup"><span data-stu-id="29f11-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Så här spåras projektets faktiska resultat till källdokument](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="29f11-108">Skicka tidspost</span><span class="sxs-lookup"><span data-stu-id="29f11-108">Submitting a time entry</span></span>

<span data-ttu-id="29f11-109">I PSA när en tidspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="29f11-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="29f11-110">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="29f11-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="29f11-111">När en tidspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="29f11-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="29f11-112">Logik för att ange standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="29f11-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="29f11-113">Alla fältvärden från en tidspost kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="29f11-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="29f11-114">Fälten innehåller datumet för transaktionen, kontraktraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="29f11-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="29f11-115">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisatinsenhet** gör att ett korrekt pris anges som standard på journalraden.</span><span class="sxs-lookup"><span data-stu-id="29f11-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="29f11-116">Om du lägger till ett anpassat fält i tidsposten och du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="29f11-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="29f11-117">Skicka en utgiftspost</span><span class="sxs-lookup"><span data-stu-id="29f11-117">Submitting an expense entry</span></span>

<span data-ttu-id="29f11-118">I PSA när en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="29f11-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="29f11-119">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="29f11-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="29f11-120">När en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="29f11-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="29f11-121">Logik för att ange standardpriser för utgifter baseras på den utgiftskategori som är vald på sidan **utgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="29f11-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="29f11-122">Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="29f11-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="29f11-123">För själva priset anges emellertid det belopp som användaren har angett direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning som standard.</span><span class="sxs-lookup"><span data-stu-id="29f11-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="29f11-124">I den aktuella versionen av PSA är kategoribaserade poster av per enhet standardpriser på utgiftposter inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="29f11-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="29f11-125">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="29f11-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="29f11-126">I PSA kan du med hjälp av postjournaler registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="29f11-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="29f11-127">En journal har ett huvud, rader och en **Bekräfta**-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="29f11-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="29f11-128">Här följer några scenarier där du kan använda en journal:</span><span class="sxs-lookup"><span data-stu-id="29f11-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="29f11-129">Du måste registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="29f11-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="29f11-130">Du måste flytta faktiska värden för transaktioner från ett annat system till PSA.</span><span class="sxs-lookup"><span data-stu-id="29f11-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="29f11-131">Du måste registrera kostnader som inträffat i ett annat system, t.ex. inköp eller legotillverkningskostnader.</span><span class="sxs-lookup"><span data-stu-id="29f11-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29f11-132">Att använda postjournaler för att skapa verkliga värden ska endast utföras av en användare som är helt medveten om den redovisning som påverkar de faktiska värdena för projektet.</span><span class="sxs-lookup"><span data-stu-id="29f11-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="29f11-133">Detta beror på att programmet inte validerar journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="29f11-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="29f11-134">På grund av den här journaltypens påverkan bör du vara försiktig med att få tillgång till skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="29f11-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="29f11-135">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="29f11-135">Recording actuals based on project events</span></span>

<span data-ttu-id="29f11-136">PSA registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="29f11-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="29f11-137">Dessa transaktioner registreras som **faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="29f11-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="29f11-138">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="29f11-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="29f11-139">**Resursen tillhör samma organisationsenhet som projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="29f11-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="29f11-140">Händelse</span><span class="sxs-lookup"><span data-stu-id="29f11-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="29f11-141">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="29f11-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="29f11-142">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="29f11-143">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="29f11-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="29f11-144">Tid och material</span><span class="sxs-lookup"><span data-stu-id="29f11-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="29f11-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="29f11-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29f11-146">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="29f11-146">Actuals</span></span></th>
<th><span data-ttu-id="29f11-147">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="29f11-147">Transaction currency</span></span></th>
<th><span data-ttu-id="29f11-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="29f11-148">Fixed price</span></span></th>
<th><span data-ttu-id="29f11-149">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="29f11-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29f11-150">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="29f11-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="29f11-151">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="29f11-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-152">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="29f11-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="29f11-153">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="29f11-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29f11-154">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="29f11-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29f11-155">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-155">Cost actual</span></span></td>
<td><span data-ttu-id="29f11-156">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-158">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="29f11-159">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-160">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-161">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="29f11-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="29f11-162">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29f11-163">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="29f11-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29f11-164">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-164">Cost actual</span></span></td>
<td><span data-ttu-id="29f11-165">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-167">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-168">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-169">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-170">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="29f11-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29f11-171">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-172">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="29f11-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29f11-173">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29f11-174">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="29f11-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29f11-175">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29f11-176">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-177">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="29f11-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-178">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-179">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-180">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-181">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-181">Billed sales</span></span></td>
<td><span data-ttu-id="29f11-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29f11-183">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="29f11-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29f11-184">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29f11-185">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-187">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-188">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-189">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-190">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="29f11-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29f11-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-192">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="29f11-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29f11-193">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29f11-194">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="29f11-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29f11-195">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="29f11-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29f11-196">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="29f11-197">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="29f11-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="29f11-198">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="29f11-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="29f11-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-200">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-201">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-202">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-202">Billed sales</span></span></td>
<td><span data-ttu-id="29f11-203">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29f11-204">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="29f11-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29f11-205">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="29f11-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29f11-206">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-207">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="29f11-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="29f11-208">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-209">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="29f11-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="29f11-210">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29f11-211">**Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="29f11-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="29f11-212">Händelse</span><span class="sxs-lookup"><span data-stu-id="29f11-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="29f11-213">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="29f11-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="29f11-214">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="29f11-215">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="29f11-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="29f11-216">Tid och material</span><span class="sxs-lookup"><span data-stu-id="29f11-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="29f11-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="29f11-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29f11-218">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="29f11-218">Actuals</span></span></th>
<th><span data-ttu-id="29f11-219">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="29f11-219">Transaction currency</span></span></th>
<th><span data-ttu-id="29f11-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="29f11-220">Fixed price</span></span></th>
<th><span data-ttu-id="29f11-221">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="29f11-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29f11-222">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="29f11-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="29f11-223">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="29f11-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-224">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="29f11-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="29f11-225">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="29f11-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="29f11-226">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="29f11-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29f11-227">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-227">Cost actual</span></span></td>
<td><span data-ttu-id="29f11-228">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="29f11-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="29f11-230">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="29f11-231">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="29f11-232">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-233">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="29f11-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="29f11-234">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-235">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="29f11-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="29f11-236">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="29f11-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-237">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="29f11-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="29f11-238">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="29f11-239">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="29f11-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29f11-240">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-240">Cost actual</span></span></td>
<td><span data-ttu-id="29f11-241">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-243">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-244">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-245">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="29f11-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-246">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="29f11-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="29f11-247">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="29f11-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-248">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="29f11-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="29f11-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="29f11-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-250">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="29f11-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29f11-251">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-252">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="29f11-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29f11-253">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29f11-254">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="29f11-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29f11-255">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29f11-256">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-257">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="29f11-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-258">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-259">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="29f11-260">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-261">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-261">Billed sales</span></span></td>
<td><span data-ttu-id="29f11-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29f11-263">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="29f11-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29f11-264">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29f11-265">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-267">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-268">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29f11-269">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-270">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="29f11-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29f11-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-272">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="29f11-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29f11-273">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29f11-274">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="29f11-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29f11-275">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="29f11-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29f11-276">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="29f11-277">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="29f11-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="29f11-278">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="29f11-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="29f11-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-280">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="29f11-281">Saknas</span><span class="sxs-lookup"><span data-stu-id="29f11-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-282">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="29f11-282">Billed sales</span></span></td>
<td><span data-ttu-id="29f11-283">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29f11-284">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="29f11-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29f11-285">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="29f11-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29f11-286">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-287">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="29f11-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="29f11-288">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29f11-289">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="29f11-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="29f11-290">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="29f11-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]