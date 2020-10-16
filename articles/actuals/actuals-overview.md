---
title: Faktiska värden
description: I det här ämne finns information om hur du arbetar med verkliga värden i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907340"
---
# <a name="actuals"></a><span data-ttu-id="b7714-103">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-103">Actuals</span></span>

<span data-ttu-id="b7714-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="b7714-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b7714-105">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b7714-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="b7714-106">De skapas som ett resultat av tids- och utgiftsposter samt journalposter och fakturor.</span><span class="sxs-lookup"><span data-stu-id="b7714-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="b7714-107">Journalrader och tidsöverföring</span><span class="sxs-lookup"><span data-stu-id="b7714-107">Journal lines and time submission</span></span>

<span data-ttu-id="b7714-108">Mer information om tidspost finns i [Översikt över tidspost](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b7714-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b7714-109">Tid och material</span><span class="sxs-lookup"><span data-stu-id="b7714-109">Time and materials</span></span>

<span data-ttu-id="b7714-110">När en tidspost som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="b7714-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b7714-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b7714-111">Fixed price</span></span>

<span data-ttu-id="b7714-112">När en tidspost som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="b7714-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b7714-113">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="b7714-113">Default pricing</span></span>

<span data-ttu-id="b7714-114">Logiken för att skapa standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="b7714-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="b7714-115">Fältvärdet från tidsposten kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="b7714-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="b7714-116">Värdena innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="b7714-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="b7714-117">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisationsenhet** används för att fastställa korrekt pris på journalraden.</span><span class="sxs-lookup"><span data-stu-id="b7714-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="b7714-118">Du kan lägga till ett anpassat fält i tidsposten.</span><span class="sxs-lookup"><span data-stu-id="b7714-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="b7714-119">Om du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten Faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="b7714-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="b7714-120">Journalrader och grundläggande kostnadsöverföring</span><span class="sxs-lookup"><span data-stu-id="b7714-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="b7714-121">Mer information om utgiftspost finns i [Översikt över utgiftspost](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b7714-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="b7714-122">Tid och material</span><span class="sxs-lookup"><span data-stu-id="b7714-122">Time and materials</span></span>

<span data-ttu-id="b7714-123">När en post för grundläggande utgift som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="b7714-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="b7714-124">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b7714-124">Fixed price</span></span>

<span data-ttu-id="b7714-125">När en post för grundläggande utgift som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="b7714-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="b7714-126">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="b7714-126">Default pricing</span></span>

<span data-ttu-id="b7714-127">Logiken för att ange standardpriser för utgifter baseras på utgiftskategorin.</span><span class="sxs-lookup"><span data-stu-id="b7714-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="b7714-128">Datumet för transaktionen, kontraktsraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="b7714-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b7714-129">För själva priset anges emellertid som standard det belopp som har angetts direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning.</span><span class="sxs-lookup"><span data-stu-id="b7714-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="b7714-130">Kategoribaserade poster av standardpriser per enhet på utgiftposter är inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="b7714-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="b7714-131">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="b7714-131">Use entry journals to record costs</span></span>

<span data-ttu-id="b7714-132">Du kan använda postjournaler för att registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="b7714-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="b7714-133">Journaler kan användas för följande ändamål:</span><span class="sxs-lookup"><span data-stu-id="b7714-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="b7714-134">Registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b7714-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="b7714-135">Flytta faktiska värden för transaktioner från ett annat system till Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b7714-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="b7714-136">Registrera kostnader som har inträffat i ett annat system.</span><span class="sxs-lookup"><span data-stu-id="b7714-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="b7714-137">Kostnaderna kan vara anskaffnings- eller underleverantörskostnader.</span><span class="sxs-lookup"><span data-stu-id="b7714-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7714-138">Programmet verifierar inte journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="b7714-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="b7714-139">Därför bör endast en användare som är helt medveten om redovisningseffekten som faktiska värden har på projektet använda sig av postjournaler för att skapa verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="b7714-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="b7714-140">På grund av den här journaltypens inverkan bör du noggrant välja vem som har åtkomst till att skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="b7714-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="b7714-141">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="b7714-141">Record actuals based on project events</span></span>

<span data-ttu-id="b7714-142">Project Operations registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b7714-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="b7714-143">Dessa transaktioner registreras som faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="b7714-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="b7714-144">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="b7714-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="b7714-145">Resursen tillhör samma organisationsenhet som projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b7714-146">Händelse</span><span class="sxs-lookup"><span data-stu-id="b7714-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b7714-147">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="b7714-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b7714-148">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b7714-149">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="b7714-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b7714-150">Tid och material</span><span class="sxs-lookup"><span data-stu-id="b7714-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b7714-151">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b7714-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b7714-152">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-152">Actuals</span></span></th>
<th><span data-ttu-id="b7714-153">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b7714-153">Transaction currency</span></span></th>
<th><span data-ttu-id="b7714-154">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b7714-154">Fixed price</span></span></th>
<th><span data-ttu-id="b7714-155">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b7714-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7714-156">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="b7714-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b7714-157">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-158">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="b7714-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b7714-159">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b7714-160">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="b7714-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b7714-161">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-161">Cost actual</span></span></td>
<td><span data-ttu-id="b7714-162">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-163">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-164">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="b7714-165">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-167">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="b7714-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b7714-168">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b7714-169">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="b7714-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b7714-170">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-170">Cost actual</span></span></td>
<td><span data-ttu-id="b7714-171">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-172">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-173">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-174">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-175">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-176">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="b7714-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b7714-177">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-178">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="b7714-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b7714-179">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b7714-180">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="b7714-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b7714-181">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b7714-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-183">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="b7714-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-184">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-185">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-187">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-187">Billed sales</span></span></td>
<td><span data-ttu-id="b7714-188">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b7714-189">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="b7714-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b7714-190">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b7714-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-192">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-193">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-194">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-195">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-196">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="b7714-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b7714-197">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-198">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="b7714-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b7714-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b7714-200">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="b7714-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b7714-201">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="b7714-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b7714-202">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b7714-203">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="b7714-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b7714-204">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="b7714-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b7714-205">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-206">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-207">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-208">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-208">Billed sales</span></span></td>
<td><span data-ttu-id="b7714-209">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b7714-210">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="b7714-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b7714-211">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="b7714-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b7714-212">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-213">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="b7714-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b7714-214">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-215">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="b7714-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b7714-216">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="b7714-217">Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b7714-218">Händelse</span><span class="sxs-lookup"><span data-stu-id="b7714-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b7714-219">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="b7714-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b7714-220">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b7714-221">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="b7714-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b7714-222">Tid och material</span><span class="sxs-lookup"><span data-stu-id="b7714-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b7714-223">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b7714-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b7714-224">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-224">Actuals</span></span></th>
<th><span data-ttu-id="b7714-225">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b7714-225">Transaction currency</span></span></th>
<th><span data-ttu-id="b7714-226">Fast pris</span><span class="sxs-lookup"><span data-stu-id="b7714-226">Fixed price</span></span></th>
<th><span data-ttu-id="b7714-227">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="b7714-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7714-228">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="b7714-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b7714-229">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-230">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="b7714-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b7714-231">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b7714-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b7714-232">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="b7714-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b7714-233">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-233">Cost actual</span></span></td>
<td><span data-ttu-id="b7714-234">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b7714-235">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b7714-236">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b7714-237">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b7714-238">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-239">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="b7714-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b7714-240">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-241">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="b7714-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b7714-242">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="b7714-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-243">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="b7714-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b7714-244">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b7714-245">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="b7714-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b7714-246">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-246">Cost actual</span></span></td>
<td><span data-ttu-id="b7714-247">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-248">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-250">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-251">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="b7714-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-252">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="b7714-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b7714-253">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="b7714-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-254">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="b7714-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b7714-255">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="b7714-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-256">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="b7714-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b7714-257">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-258">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="b7714-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b7714-259">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b7714-260">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="b7714-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b7714-261">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b7714-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-263">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="b7714-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-264">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-265">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b7714-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-267">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-267">Billed sales</span></span></td>
<td><span data-ttu-id="b7714-268">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b7714-269">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="b7714-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b7714-270">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b7714-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-272">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-273">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-274">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b7714-275">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-276">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="b7714-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b7714-277">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-278">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="b7714-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b7714-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b7714-280">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="b7714-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b7714-281">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="b7714-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b7714-282">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b7714-283">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="b7714-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b7714-284">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="b7714-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b7714-285">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-286">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b7714-287">Saknas</span><span class="sxs-lookup"><span data-stu-id="b7714-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-288">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="b7714-288">Billed sales</span></span></td>
<td><span data-ttu-id="b7714-289">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b7714-290">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="b7714-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b7714-291">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="b7714-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b7714-292">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-293">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="b7714-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b7714-294">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7714-295">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="b7714-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b7714-296">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="b7714-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
