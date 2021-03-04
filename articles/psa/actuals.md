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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146145"
---
# <a name="actuals-overview"></a><span data-ttu-id="869c6-103">Översikt över värden</span><span class="sxs-lookup"><span data-stu-id="869c6-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="869c6-104">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="869c6-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="869c6-105">Projektets faktiska värden kan spåras tillbaka till källdokumenten.</span><span class="sxs-lookup"><span data-stu-id="869c6-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="869c6-106">Dessa källdokument innehåller både tid, utgift och journaltransaktioner samt fakturor.</span><span class="sxs-lookup"><span data-stu-id="869c6-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Så här spåras projektets faktiska resultat till källdokument](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="869c6-108">Skicka tidspost</span><span class="sxs-lookup"><span data-stu-id="869c6-108">Submitting a time entry</span></span>

<span data-ttu-id="869c6-109">I PSA när en tidspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="869c6-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="869c6-110">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="869c6-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="869c6-111">När en tidspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="869c6-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="869c6-112">Logik för att ange standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="869c6-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="869c6-113">Alla fältvärden från en tidspost kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="869c6-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="869c6-114">Fälten innehåller datumet för transaktionen, kontraktraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="869c6-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="869c6-115">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisatinsenhet** gör att ett korrekt pris anges som standard på journalraden.</span><span class="sxs-lookup"><span data-stu-id="869c6-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="869c6-116">Om du lägger till ett anpassat fält i tidsposten och du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="869c6-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="869c6-117">Skicka en utgiftspost</span><span class="sxs-lookup"><span data-stu-id="869c6-117">Submitting an expense entry</span></span>

<span data-ttu-id="869c6-118">I PSA när en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="869c6-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="869c6-119">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="869c6-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="869c6-120">När en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="869c6-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="869c6-121">Logik för att ange standardpriser för utgifter baseras på den utgiftskategori som är vald på sidan **utgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="869c6-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="869c6-122">Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="869c6-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="869c6-123">För själva priset anges emellertid det belopp som användaren har angett direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning som standard.</span><span class="sxs-lookup"><span data-stu-id="869c6-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="869c6-124">I den aktuella versionen av PSA är kategoribaserade poster av per enhet standardpriser på utgiftposter inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="869c6-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="869c6-125">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="869c6-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="869c6-126">I PSA kan du med hjälp av postjournaler registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="869c6-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="869c6-127">En journal har ett huvud, rader och en **Bekräfta**-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="869c6-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="869c6-128">Här följer några scenarier där du kan använda en journal:</span><span class="sxs-lookup"><span data-stu-id="869c6-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="869c6-129">Du måste registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="869c6-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="869c6-130">Du måste flytta faktiska värden för transaktioner från ett annat system till PSA.</span><span class="sxs-lookup"><span data-stu-id="869c6-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="869c6-131">Du måste registrera kostnader som inträffat i ett annat system, t.ex. inköp eller legotillverkningskostnader.</span><span class="sxs-lookup"><span data-stu-id="869c6-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="869c6-132">Att använda postjournaler för att skapa verkliga värden ska endast utföras av en användare som är helt medveten om den redovisning som påverkar de faktiska värdena för projektet.</span><span class="sxs-lookup"><span data-stu-id="869c6-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="869c6-133">Detta beror på att programmet inte validerar journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="869c6-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="869c6-134">På grund av den här journaltypens påverkan bör du vara försiktig med att få tillgång till skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="869c6-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="869c6-135">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="869c6-135">Recording actuals based on project events</span></span>

<span data-ttu-id="869c6-136">PSA registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="869c6-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="869c6-137">Dessa transaktioner registreras som **faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="869c6-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="869c6-138">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="869c6-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="869c6-139">**Resursen tillhör samma organisationsenhet som projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="869c6-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="869c6-140">Händelse</span><span class="sxs-lookup"><span data-stu-id="869c6-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="869c6-141">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="869c6-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="869c6-142">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="869c6-143">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="869c6-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="869c6-144">Tid och material</span><span class="sxs-lookup"><span data-stu-id="869c6-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="869c6-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="869c6-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="869c6-146">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="869c6-146">Actuals</span></span></th>
<th><span data-ttu-id="869c6-147">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="869c6-147">Transaction currency</span></span></th>
<th><span data-ttu-id="869c6-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="869c6-148">Fixed price</span></span></th>
<th><span data-ttu-id="869c6-149">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="869c6-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="869c6-150">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="869c6-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="869c6-151">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="869c6-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-152">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="869c6-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="869c6-153">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="869c6-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="869c6-154">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="869c6-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="869c6-155">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-155">Cost actual</span></span></td>
<td><span data-ttu-id="869c6-156">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-158">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="869c6-159">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-160">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-161">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="869c6-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="869c6-162">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="869c6-163">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="869c6-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="869c6-164">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-164">Cost actual</span></span></td>
<td><span data-ttu-id="869c6-165">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-167">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-168">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-169">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-170">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="869c6-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="869c6-171">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-172">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="869c6-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="869c6-173">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="869c6-174">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="869c6-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="869c6-175">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="869c6-176">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-177">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="869c6-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-178">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-179">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-180">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-181">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-181">Billed sales</span></span></td>
<td><span data-ttu-id="869c6-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="869c6-183">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="869c6-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="869c6-184">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="869c6-185">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-187">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-188">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-189">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-190">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="869c6-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="869c6-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-192">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="869c6-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="869c6-193">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="869c6-194">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="869c6-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="869c6-195">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="869c6-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="869c6-196">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="869c6-197">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="869c6-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="869c6-198">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="869c6-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="869c6-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-200">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-201">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-202">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-202">Billed sales</span></span></td>
<td><span data-ttu-id="869c6-203">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="869c6-204">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="869c6-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="869c6-205">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="869c6-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="869c6-206">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-207">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="869c6-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="869c6-208">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-209">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="869c6-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="869c6-210">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="869c6-211">**Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="869c6-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="869c6-212">Händelse</span><span class="sxs-lookup"><span data-stu-id="869c6-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="869c6-213">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="869c6-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="869c6-214">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="869c6-215">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="869c6-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="869c6-216">Tid och material</span><span class="sxs-lookup"><span data-stu-id="869c6-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="869c6-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="869c6-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="869c6-218">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="869c6-218">Actuals</span></span></th>
<th><span data-ttu-id="869c6-219">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="869c6-219">Transaction currency</span></span></th>
<th><span data-ttu-id="869c6-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="869c6-220">Fixed price</span></span></th>
<th><span data-ttu-id="869c6-221">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="869c6-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="869c6-222">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="869c6-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="869c6-223">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="869c6-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-224">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="869c6-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="869c6-225">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="869c6-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="869c6-226">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="869c6-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="869c6-227">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-227">Cost actual</span></span></td>
<td><span data-ttu-id="869c6-228">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="869c6-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="869c6-230">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="869c6-231">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="869c6-232">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-233">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="869c6-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="869c6-234">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-235">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="869c6-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="869c6-236">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="869c6-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-237">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="869c6-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="869c6-238">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="869c6-239">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="869c6-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="869c6-240">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-240">Cost actual</span></span></td>
<td><span data-ttu-id="869c6-241">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-243">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-244">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-245">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="869c6-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-246">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="869c6-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="869c6-247">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="869c6-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-248">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="869c6-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="869c6-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="869c6-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-250">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="869c6-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="869c6-251">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-252">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="869c6-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="869c6-253">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="869c6-254">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="869c6-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="869c6-255">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="869c6-256">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-257">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="869c6-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-258">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-259">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="869c6-260">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-261">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-261">Billed sales</span></span></td>
<td><span data-ttu-id="869c6-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="869c6-263">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="869c6-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="869c6-264">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="869c6-265">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-267">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-268">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="869c6-269">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-270">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="869c6-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="869c6-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-272">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="869c6-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="869c6-273">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="869c6-274">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="869c6-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="869c6-275">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="869c6-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="869c6-276">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="869c6-277">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="869c6-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="869c6-278">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="869c6-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="869c6-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-280">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="869c6-281">Saknas</span><span class="sxs-lookup"><span data-stu-id="869c6-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-282">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="869c6-282">Billed sales</span></span></td>
<td><span data-ttu-id="869c6-283">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="869c6-284">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="869c6-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="869c6-285">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="869c6-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="869c6-286">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-287">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="869c6-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="869c6-288">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="869c6-289">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="869c6-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="869c6-290">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="869c6-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
