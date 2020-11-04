---
title: Översikt över värden
description: I det här ämnet finns information om projektets faktiska värden.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085738"
---
# <a name="actuals-overview"></a><span data-ttu-id="a8c68-103">Översikt över värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a8c68-104">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a8c68-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a8c68-105">Projektets faktiska värden kan spåras tillbaka till källdokumenten.</span><span class="sxs-lookup"><span data-stu-id="a8c68-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a8c68-106">Dessa källdokument innehåller både tid, utgift och journaltransaktioner samt fakturor.</span><span class="sxs-lookup"><span data-stu-id="a8c68-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Så här spåras projektets faktiska resultat till källdokument](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a8c68-108">Skicka tidspost</span><span class="sxs-lookup"><span data-stu-id="a8c68-108">Submitting a time entry</span></span>

<span data-ttu-id="a8c68-109">I PSA när en tidspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="a8c68-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a8c68-110">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="a8c68-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a8c68-111">När en tidspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="a8c68-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a8c68-112">Logik för att ange standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="a8c68-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a8c68-113">Alla fältvärden från en tidspost kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="a8c68-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a8c68-114">Fälten innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="a8c68-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a8c68-115">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisatinsenhet** gör att ett korrekt pris anges som standard på journalraden.</span><span class="sxs-lookup"><span data-stu-id="a8c68-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a8c68-116">Om du lägger till ett anpassat fält i tidsposten och du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a8c68-117">Skicka en utgiftspost</span><span class="sxs-lookup"><span data-stu-id="a8c68-117">Submitting an expense entry</span></span>

<span data-ttu-id="a8c68-118">I PSA när en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader.</span><span class="sxs-lookup"><span data-stu-id="a8c68-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a8c68-119">En rad är för kostnad och den andra raden är för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="a8c68-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a8c68-120">När en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="a8c68-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a8c68-121">Logik för att ange standardpriser för utgifter baseras på den utgiftskategori som är vald på sidan **utgiftspost**.</span><span class="sxs-lookup"><span data-stu-id="a8c68-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a8c68-122">Datumet för transaktionen, kontraktsraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="a8c68-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a8c68-123">För själva priset anges emellertid det belopp som användaren har angett direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning som standard.</span><span class="sxs-lookup"><span data-stu-id="a8c68-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a8c68-124">I den aktuella versionen av PSA är kategoribaserade poster av per enhet standardpriser på utgiftposter inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="a8c68-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="a8c68-125">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="a8c68-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="a8c68-126">I PSA kan du med hjälp av postjournaler registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="a8c68-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a8c68-127">En journal har ett huvud, rader och en **Bekräfta** -åtgärd.</span><span class="sxs-lookup"><span data-stu-id="a8c68-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a8c68-128">Här följer några scenarier där du kan använda en journal:</span><span class="sxs-lookup"><span data-stu-id="a8c68-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a8c68-129">Du måste registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a8c68-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a8c68-130">Du måste flytta faktiska värden för transaktioner från ett annat system till PSA.</span><span class="sxs-lookup"><span data-stu-id="a8c68-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a8c68-131">Du måste registrera kostnader som inträffat i ett annat system, t.ex. inköp eller legotillverkningskostnader.</span><span class="sxs-lookup"><span data-stu-id="a8c68-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8c68-132">Att använda postjournaler för att skapa verkliga värden ska endast utföras av en användare som är helt medveten om den redovisning som påverkar de faktiska värdena för projektet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="a8c68-133">Detta beror på att programmet inte validerar journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="a8c68-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="a8c68-134">På grund av den här journaltypens påverkan bör du vara försiktig med att få tillgång till skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="a8c68-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a8c68-135">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="a8c68-135">Recording actuals based on project events</span></span>

<span data-ttu-id="a8c68-136">PSA registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a8c68-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a8c68-137">Dessa transaktioner registreras som **faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="a8c68-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a8c68-138">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="a8c68-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a8c68-139">**Resursen tillhör samma organisationsenhet som projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="a8c68-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a8c68-140">Händelse</span><span class="sxs-lookup"><span data-stu-id="a8c68-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a8c68-141">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="a8c68-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c68-142">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c68-143">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="a8c68-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a8c68-144">Tid och material</span><span class="sxs-lookup"><span data-stu-id="a8c68-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a8c68-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c68-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8c68-146">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-146">Actuals</span></span></th>
<th><span data-ttu-id="a8c68-147">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c68-147">Transaction currency</span></span></th>
<th><span data-ttu-id="a8c68-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c68-148">Fixed price</span></span></th>
<th><span data-ttu-id="a8c68-149">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c68-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8c68-150">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="a8c68-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c68-151">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-152">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="a8c68-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c68-153">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c68-154">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c68-155">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-155">Cost actual</span></span></td>
<td><span data-ttu-id="a8c68-156">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-158">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a8c68-159">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-160">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-161">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="a8c68-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a8c68-162">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c68-163">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c68-164">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-164">Cost actual</span></span></td>
<td><span data-ttu-id="a8c68-165">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-167">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-168">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-169">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-170">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a8c68-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c68-171">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-172">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a8c68-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c68-173">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c68-174">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a8c68-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c68-175">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c68-176">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-177">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a8c68-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-178">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-179">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-180">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-181">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-181">Billed sales</span></span></td>
<td><span data-ttu-id="a8c68-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c68-183">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a8c68-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c68-184">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c68-185">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-187">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-188">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-189">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-190">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a8c68-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c68-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-192">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a8c68-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c68-193">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c68-194">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c68-195">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a8c68-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c68-196">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a8c68-197">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a8c68-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a8c68-198">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a8c68-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a8c68-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-200">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-201">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-202">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-202">Billed sales</span></span></td>
<td><span data-ttu-id="a8c68-203">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c68-204">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c68-205">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a8c68-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c68-206">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-207">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a8c68-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a8c68-208">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-209">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a8c68-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c68-210">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8c68-211">**Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet**</span><span class="sxs-lookup"><span data-stu-id="a8c68-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a8c68-212">Händelse</span><span class="sxs-lookup"><span data-stu-id="a8c68-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a8c68-213">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="a8c68-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c68-214">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c68-215">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="a8c68-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a8c68-216">Tid och material</span><span class="sxs-lookup"><span data-stu-id="a8c68-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a8c68-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c68-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8c68-218">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-218">Actuals</span></span></th>
<th><span data-ttu-id="a8c68-219">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c68-219">Transaction currency</span></span></th>
<th><span data-ttu-id="a8c68-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c68-220">Fixed price</span></span></th>
<th><span data-ttu-id="a8c68-221">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c68-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8c68-222">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="a8c68-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c68-223">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-224">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="a8c68-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c68-225">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a8c68-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a8c68-226">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c68-227">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-227">Cost actual</span></span></td>
<td><span data-ttu-id="a8c68-228">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c68-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c68-230">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c68-231">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c68-232">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-233">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="a8c68-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a8c68-234">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-235">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a8c68-236">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-237">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="a8c68-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a8c68-238">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a8c68-239">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c68-240">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-240">Cost actual</span></span></td>
<td><span data-ttu-id="a8c68-241">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-243">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-244">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-245">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c68-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-246">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a8c68-247">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-248">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="a8c68-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a8c68-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a8c68-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-250">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a8c68-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c68-251">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-252">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a8c68-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c68-253">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c68-254">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a8c68-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c68-255">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c68-256">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-257">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a8c68-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-258">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-259">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c68-260">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-261">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-261">Billed sales</span></span></td>
<td><span data-ttu-id="a8c68-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c68-263">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a8c68-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c68-264">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c68-265">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-267">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-268">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c68-269">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-270">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a8c68-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c68-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-272">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a8c68-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c68-273">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c68-274">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c68-275">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a8c68-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c68-276">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a8c68-277">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a8c68-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a8c68-278">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a8c68-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a8c68-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-280">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c68-281">Saknas</span><span class="sxs-lookup"><span data-stu-id="a8c68-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-282">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a8c68-282">Billed sales</span></span></td>
<td><span data-ttu-id="a8c68-283">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c68-284">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a8c68-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c68-285">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a8c68-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c68-286">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-287">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a8c68-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a8c68-288">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c68-289">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a8c68-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c68-290">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a8c68-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
