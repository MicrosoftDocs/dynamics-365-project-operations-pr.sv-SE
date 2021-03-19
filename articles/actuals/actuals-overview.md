---
title: Värden
description: Den ämne innehåller information om hur du arbetar med faktiska värden i Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291821"
---
# <a name="actuals"></a><span data-ttu-id="a58f5-103">Utfall</span><span class="sxs-lookup"><span data-stu-id="a58f5-103">Actuals</span></span> 

<span data-ttu-id="a58f5-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="a58f5-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a58f5-105">Faktiska värden är den mängd arbete som har slutförts i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a58f5-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a58f5-106">De skapas som ett resultat av tids- och utgiftsposter samt journalposter och fakturor.</span><span class="sxs-lookup"><span data-stu-id="a58f5-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="a58f5-107">Journalrader och tidsöverföring</span><span class="sxs-lookup"><span data-stu-id="a58f5-107">Journal lines and time submission</span></span>

<span data-ttu-id="a58f5-108">Mer information om tidspost finns i [Översikt över tidspost](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a58f5-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a58f5-109">Tid och material</span><span class="sxs-lookup"><span data-stu-id="a58f5-109">Time and materials</span></span>

<span data-ttu-id="a58f5-110">När en tidspost som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="a58f5-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a58f5-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a58f5-111">Fixed price</span></span>

<span data-ttu-id="a58f5-112">När en tidspost som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="a58f5-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a58f5-113">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="a58f5-113">Default pricing</span></span>

<span data-ttu-id="a58f5-114">Logiken för att skapa standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="a58f5-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="a58f5-115">Fältvärdet från tidsposten kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="a58f5-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="a58f5-116">Värdena innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="a58f5-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="a58f5-117">De fält som påverkar standardpriser, t.ex. **Roll** och **Organisationsenhet** används för att fastställa korrekt pris på journalraden.</span><span class="sxs-lookup"><span data-stu-id="a58f5-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a58f5-118">Du kan lägga till ett anpassat fält i tidsposten.</span><span class="sxs-lookup"><span data-stu-id="a58f5-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="a58f5-119">Om du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten Faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="a58f5-120">Journalrader och grundläggande kostnadsöverföring</span><span class="sxs-lookup"><span data-stu-id="a58f5-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="a58f5-121">Mer information om utgiftspost finns i [Översikt över utgiftspost](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a58f5-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a58f5-122">Tid och material</span><span class="sxs-lookup"><span data-stu-id="a58f5-122">Time and materials</span></span>

<span data-ttu-id="a58f5-123">När en post för grundläggande utgift som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="a58f5-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a58f5-124">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a58f5-124">Fixed price</span></span>

<span data-ttu-id="a58f5-125">När en post för grundläggande utgift som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="a58f5-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a58f5-126">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="a58f5-126">Default pricing</span></span>

<span data-ttu-id="a58f5-127">Logiken för att ange standardpriser för utgifter baseras på utgiftskategorin.</span><span class="sxs-lookup"><span data-stu-id="a58f5-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="a58f5-128">Datumet för transaktionen, kontraktsraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="a58f5-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a58f5-129">För själva priset anges emellertid som standard det belopp som har angetts direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning.</span><span class="sxs-lookup"><span data-stu-id="a58f5-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="a58f5-130">Kategoribaserade poster av standardpriser per enhet på utgiftposter är inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="a58f5-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="a58f5-131">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="a58f5-131">Use entry journals to record costs</span></span>

<span data-ttu-id="a58f5-132">Du kan använda postjournaler för att registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="a58f5-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a58f5-133">Journaler kan användas för följande ändamål:</span><span class="sxs-lookup"><span data-stu-id="a58f5-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="a58f5-134">Registrera materialets faktiska kostnader och försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a58f5-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="a58f5-135">Flytta transaktionsdata från ett annat system till Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a58f5-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="a58f5-136">Registrera kostnader som har inträffat i ett annat system.</span><span class="sxs-lookup"><span data-stu-id="a58f5-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="a58f5-137">Kostnaderna kan vara anskaffnings- eller underleverantörskostnader.</span><span class="sxs-lookup"><span data-stu-id="a58f5-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a58f5-138">Programmet verifierar inte journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="a58f5-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="a58f5-139">Därför bör endast en användare som är helt medveten om redovisningseffekten som faktiska värden har på projektet använda sig av postjournaler för att skapa verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="a58f5-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="a58f5-140">På grund av den här journaltypens inverkan bör du noggrant välja vem som har åtkomst till att skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="a58f5-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="a58f5-141">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="a58f5-141">Record actuals based on project events</span></span>

<span data-ttu-id="a58f5-142">Project Operations registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a58f5-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a58f5-143">Dessa transaktioner registreras som faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="a58f5-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="a58f5-144">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="a58f5-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="a58f5-145">Resursen tillhör samma organisationsenhet som projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a58f5-146">Händelse</span><span class="sxs-lookup"><span data-stu-id="a58f5-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a58f5-147">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="a58f5-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a58f5-148">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a58f5-149">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="a58f5-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a58f5-150">Tid och material</span><span class="sxs-lookup"><span data-stu-id="a58f5-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a58f5-151">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a58f5-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a58f5-152">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a58f5-152">Actuals</span></span></th>
<th><span data-ttu-id="a58f5-153">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a58f5-153">Transaction currency</span></span></th>
<th><span data-ttu-id="a58f5-154">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a58f5-154">Fixed price</span></span></th>
<th><span data-ttu-id="a58f5-155">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a58f5-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a58f5-156">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="a58f5-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a58f5-157">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a58f5-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-158">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="a58f5-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a58f5-159">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a58f5-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a58f5-160">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a58f5-161">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-161">Cost actual</span></span></td>
<td><span data-ttu-id="a58f5-162">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-163">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-164">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a58f5-165">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-167">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="a58f5-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a58f5-168">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a58f5-169">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a58f5-170">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-170">Cost actual</span></span></td>
<td><span data-ttu-id="a58f5-171">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-172">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-173">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-174">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-175">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-176">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a58f5-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a58f5-177">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-178">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a58f5-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a58f5-179">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a58f5-180">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a58f5-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a58f5-181">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a58f5-182">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-183">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a58f5-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-184">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-185">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-186">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-187">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-187">Billed sales</span></span></td>
<td><span data-ttu-id="a58f5-188">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a58f5-189">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a58f5-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a58f5-190">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a58f5-191">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-192">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-193">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-194">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-195">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-196">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a58f5-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a58f5-197">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-198">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a58f5-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a58f5-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a58f5-200">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a58f5-201">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a58f5-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a58f5-202">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a58f5-203">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a58f5-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a58f5-204">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a58f5-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a58f5-205">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-206">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-207">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-208">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-208">Billed sales</span></span></td>
<td><span data-ttu-id="a58f5-209">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a58f5-210">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a58f5-211">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a58f5-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a58f5-212">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-213">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a58f5-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a58f5-214">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-215">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a58f5-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a58f5-216">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="a58f5-217">Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a58f5-218">Händelse</span><span class="sxs-lookup"><span data-stu-id="a58f5-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a58f5-219">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="a58f5-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a58f5-220">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a58f5-221">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="a58f5-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a58f5-222">Tid och material</span><span class="sxs-lookup"><span data-stu-id="a58f5-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a58f5-223">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a58f5-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a58f5-224">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a58f5-224">Actuals</span></span></th>
<th><span data-ttu-id="a58f5-225">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a58f5-225">Transaction currency</span></span></th>
<th><span data-ttu-id="a58f5-226">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a58f5-226">Fixed price</span></span></th>
<th><span data-ttu-id="a58f5-227">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="a58f5-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a58f5-228">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="a58f5-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a58f5-229">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a58f5-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-230">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="a58f5-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a58f5-231">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="a58f5-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a58f5-232">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a58f5-233">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-233">Cost actual</span></span></td>
<td><span data-ttu-id="a58f5-234">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a58f5-235">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a58f5-236">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a58f5-237">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a58f5-238">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-239">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="a58f5-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a58f5-240">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-241">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a58f5-242">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-243">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="a58f5-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a58f5-244">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a58f5-245">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a58f5-246">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-246">Cost actual</span></span></td>
<td><span data-ttu-id="a58f5-247">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-248">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-249">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-250">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-251">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a58f5-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-252">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a58f5-253">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-254">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="a58f5-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a58f5-255">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="a58f5-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-256">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a58f5-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a58f5-257">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-258">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a58f5-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a58f5-259">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a58f5-260">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a58f5-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a58f5-261">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a58f5-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-263">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a58f5-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-264">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-265">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a58f5-266">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-267">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-267">Billed sales</span></span></td>
<td><span data-ttu-id="a58f5-268">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a58f5-269">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="a58f5-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a58f5-270">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a58f5-271">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-272">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-273">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-274">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a58f5-275">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-276">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a58f5-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a58f5-277">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-278">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a58f5-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a58f5-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a58f5-280">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a58f5-281">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a58f5-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a58f5-282">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a58f5-283">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="a58f5-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a58f5-284">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a58f5-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a58f5-285">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-286">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a58f5-287">Saknas</span><span class="sxs-lookup"><span data-stu-id="a58f5-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-288">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="a58f5-288">Billed sales</span></span></td>
<td><span data-ttu-id="a58f5-289">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a58f5-290">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="a58f5-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a58f5-291">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="a58f5-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a58f5-292">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-293">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="a58f5-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a58f5-294">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a58f5-295">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="a58f5-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a58f5-296">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="a58f5-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]