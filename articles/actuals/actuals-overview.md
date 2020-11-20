---
title: Värden
description: I det här ämne finns information om hur du arbetar med verkliga värden i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126344"
---
# <a name="actuals"></a><span data-ttu-id="83e62-103">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-103">Actuals</span></span> 

<span data-ttu-id="83e62-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="83e62-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="83e62-105">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="83e62-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="83e62-106">De skapas som ett resultat av tids- och utgiftsposter samt journalposter och fakturor.</span><span class="sxs-lookup"><span data-stu-id="83e62-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="83e62-107">Journalrader och tidsöverföring</span><span class="sxs-lookup"><span data-stu-id="83e62-107">Journal lines and time submission</span></span>

<span data-ttu-id="83e62-108">Mer information om tidspost finns i [Översikt över tidspost](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83e62-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="83e62-109">Tid och material</span><span class="sxs-lookup"><span data-stu-id="83e62-109">Time and materials</span></span>

<span data-ttu-id="83e62-110">När en tidspost som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="83e62-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="83e62-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="83e62-111">Fixed price</span></span>

<span data-ttu-id="83e62-112">När en tidspost som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="83e62-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="83e62-113">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="83e62-113">Default pricing</span></span>

<span data-ttu-id="83e62-114">Logiken för att skapa standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="83e62-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="83e62-115">Fältvärdet från tidsposten kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="83e62-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="83e62-116">Värdena innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="83e62-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="83e62-117">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisationsenhet** används för att fastställa korrekt pris på journalraden.</span><span class="sxs-lookup"><span data-stu-id="83e62-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="83e62-118">Du kan lägga till ett anpassat fält i tidsposten.</span><span class="sxs-lookup"><span data-stu-id="83e62-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="83e62-119">Om du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten Faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="83e62-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="83e62-120">Journalrader och grundläggande kostnadsöverföring</span><span class="sxs-lookup"><span data-stu-id="83e62-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="83e62-121">Mer information om utgiftspost finns i [Översikt över utgiftspost](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83e62-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="83e62-122">Tid och material</span><span class="sxs-lookup"><span data-stu-id="83e62-122">Time and materials</span></span>

<span data-ttu-id="83e62-123">När en post för grundläggande utgift som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="83e62-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="83e62-124">Fast pris</span><span class="sxs-lookup"><span data-stu-id="83e62-124">Fixed price</span></span>

<span data-ttu-id="83e62-125">När en post för grundläggande utgift som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="83e62-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="83e62-126">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="83e62-126">Default pricing</span></span>

<span data-ttu-id="83e62-127">Logiken för att ange standardpriser för utgifter baseras på utgiftskategorin.</span><span class="sxs-lookup"><span data-stu-id="83e62-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="83e62-128">Datumet för transaktionen, kontraktsraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="83e62-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="83e62-129">För själva priset anges emellertid som standard det belopp som har angetts direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning.</span><span class="sxs-lookup"><span data-stu-id="83e62-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="83e62-130">Kategoribaserade poster av standardpriser per enhet på utgiftposter är inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="83e62-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="83e62-131">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="83e62-131">Use entry journals to record costs</span></span>

<span data-ttu-id="83e62-132">Du kan använda postjournaler för att registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="83e62-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="83e62-133">Journaler kan användas för följande ändamål:</span><span class="sxs-lookup"><span data-stu-id="83e62-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="83e62-134">Registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="83e62-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="83e62-135">Flytta faktiska värden för transaktioner från ett annat system till Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="83e62-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="83e62-136">Registrera kostnader som har inträffat i ett annat system.</span><span class="sxs-lookup"><span data-stu-id="83e62-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="83e62-137">Kostnaderna kan vara anskaffnings- eller underleverantörskostnader.</span><span class="sxs-lookup"><span data-stu-id="83e62-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83e62-138">Programmet verifierar inte journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="83e62-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="83e62-139">Därför bör endast en användare som är helt medveten om redovisningseffekten som faktiska värden har på projektet använda sig av postjournaler för att skapa verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="83e62-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="83e62-140">På grund av den här journaltypens inverkan bör du noggrant välja vem som har åtkomst till att skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="83e62-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="83e62-141">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="83e62-141">Record actuals based on project events</span></span>

<span data-ttu-id="83e62-142">Project Operations registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="83e62-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="83e62-143">Dessa transaktioner registreras som faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="83e62-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="83e62-144">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="83e62-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="83e62-145">Resursen tillhör samma organisationsenhet som projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="83e62-146">Händelse</span><span class="sxs-lookup"><span data-stu-id="83e62-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="83e62-147">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="83e62-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="83e62-148">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="83e62-149">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="83e62-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="83e62-150">Tid och material</span><span class="sxs-lookup"><span data-stu-id="83e62-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="83e62-151">Fast pris</span><span class="sxs-lookup"><span data-stu-id="83e62-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83e62-152">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-152">Actuals</span></span></th>
<th><span data-ttu-id="83e62-153">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="83e62-153">Transaction currency</span></span></th>
<th><span data-ttu-id="83e62-154">Fast pris</span><span class="sxs-lookup"><span data-stu-id="83e62-154">Fixed price</span></span></th>
<th><span data-ttu-id="83e62-155">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="83e62-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83e62-156">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="83e62-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="83e62-157">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-158">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="83e62-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="83e62-159">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83e62-160">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="83e62-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83e62-161">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-161">Cost actual</span></span></td>
<td><span data-ttu-id="83e62-162">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-163">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-164">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="83e62-165">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-167">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="83e62-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="83e62-168">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83e62-169">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="83e62-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83e62-170">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-170">Cost actual</span></span></td>
<td><span data-ttu-id="83e62-171">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-172">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-173">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-174">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-175">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-176">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="83e62-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83e62-177">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-178">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="83e62-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83e62-179">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83e62-180">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="83e62-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83e62-181">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83e62-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-183">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="83e62-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-184">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-185">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-187">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-187">Billed sales</span></span></td>
<td><span data-ttu-id="83e62-188">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83e62-189">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="83e62-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83e62-190">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83e62-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-192">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-193">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-194">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-195">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-196">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="83e62-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83e62-197">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-198">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="83e62-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83e62-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83e62-200">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="83e62-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83e62-201">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="83e62-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83e62-202">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="83e62-203">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="83e62-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="83e62-204">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="83e62-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="83e62-205">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-206">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-207">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-208">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-208">Billed sales</span></span></td>
<td><span data-ttu-id="83e62-209">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83e62-210">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="83e62-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83e62-211">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="83e62-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83e62-212">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-213">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="83e62-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="83e62-214">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-215">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="83e62-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="83e62-216">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="83e62-217">Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="83e62-218">Händelse</span><span class="sxs-lookup"><span data-stu-id="83e62-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="83e62-219">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="83e62-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="83e62-220">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="83e62-221">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="83e62-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="83e62-222">Tid och material</span><span class="sxs-lookup"><span data-stu-id="83e62-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="83e62-223">Fast pris</span><span class="sxs-lookup"><span data-stu-id="83e62-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83e62-224">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-224">Actuals</span></span></th>
<th><span data-ttu-id="83e62-225">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="83e62-225">Transaction currency</span></span></th>
<th><span data-ttu-id="83e62-226">Fast pris</span><span class="sxs-lookup"><span data-stu-id="83e62-226">Fixed price</span></span></th>
<th><span data-ttu-id="83e62-227">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="83e62-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83e62-228">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="83e62-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="83e62-229">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-230">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="83e62-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="83e62-231">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="83e62-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="83e62-232">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="83e62-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83e62-233">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-233">Cost actual</span></span></td>
<td><span data-ttu-id="83e62-234">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="83e62-235">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="83e62-236">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="83e62-237">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="83e62-238">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-239">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="83e62-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="83e62-240">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-241">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="83e62-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="83e62-242">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="83e62-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-243">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="83e62-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="83e62-244">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="83e62-245">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="83e62-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83e62-246">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-246">Cost actual</span></span></td>
<td><span data-ttu-id="83e62-247">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-248">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-250">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-251">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="83e62-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-252">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="83e62-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="83e62-253">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="83e62-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-254">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="83e62-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="83e62-255">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="83e62-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-256">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="83e62-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83e62-257">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-258">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="83e62-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83e62-259">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83e62-260">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="83e62-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83e62-261">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83e62-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-263">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="83e62-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-264">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-265">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="83e62-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-267">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-267">Billed sales</span></span></td>
<td><span data-ttu-id="83e62-268">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83e62-269">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="83e62-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83e62-270">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83e62-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-272">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-273">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-274">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83e62-275">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-276">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="83e62-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83e62-277">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-278">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="83e62-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83e62-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83e62-280">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="83e62-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83e62-281">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="83e62-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83e62-282">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="83e62-283">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="83e62-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="83e62-284">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="83e62-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="83e62-285">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-286">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="83e62-287">Saknas</span><span class="sxs-lookup"><span data-stu-id="83e62-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-288">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="83e62-288">Billed sales</span></span></td>
<td><span data-ttu-id="83e62-289">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83e62-290">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="83e62-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83e62-291">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="83e62-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83e62-292">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-293">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="83e62-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="83e62-294">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83e62-295">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="83e62-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="83e62-296">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="83e62-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
