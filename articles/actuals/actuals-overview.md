---
title: Värden
description: Den ämne innehåller information om hur du arbetar med faktiska värden i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852566"
---
# <a name="actuals"></a><span data-ttu-id="5b899-103">Utfall</span><span class="sxs-lookup"><span data-stu-id="5b899-103">Actuals</span></span> 

<span data-ttu-id="5b899-104">_**Gäller till:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="5b899-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b899-105">Faktiska värden representerar den granskade och godkända ekonomiska förloppet och schemalägger förloppet för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="5b899-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="5b899-106">De skapas som ett resultat av godkännande av tid, utgifter, materialanvändningsposter och aktivitetsposter och fakturor.</span><span class="sxs-lookup"><span data-stu-id="5b899-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="5b899-107">Journalrader och tidsöverföring</span><span class="sxs-lookup"><span data-stu-id="5b899-107">Journal lines and time submission</span></span>

<span data-ttu-id="5b899-108">Mer information om tidspost finns i [Översikt över tidspost](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b899-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="5b899-109">Tid och material</span><span class="sxs-lookup"><span data-stu-id="5b899-109">Time and materials</span></span>

<span data-ttu-id="5b899-110">När en tidspost som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="5b899-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="5b899-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-111">Fixed price</span></span>

<span data-ttu-id="5b899-112">När en tidspost som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="5b899-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="5b899-113">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="5b899-113">Default pricing</span></span>

<span data-ttu-id="5b899-114">Logiken för att skapa standardpriser finns på journalraden.</span><span class="sxs-lookup"><span data-stu-id="5b899-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="5b899-115">Fältvärdet från tidsposten kopieras till journalraden.</span><span class="sxs-lookup"><span data-stu-id="5b899-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="5b899-116">Värdena innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="5b899-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="5b899-117">De fält som påverkar standardpriser, t.ex. **Roll** och **Resursenhet** används för att bestämma lämpligt pris på journalraden.</span><span class="sxs-lookup"><span data-stu-id="5b899-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="5b899-118">Du kan lägga till ett anpassat fält i tidsposten.</span><span class="sxs-lookup"><span data-stu-id="5b899-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="5b899-119">Om du vill att fältvärdet ska spridas ut till faktiska värden skapar du fältet i tabellerna **Faktiska värden** och **Journalrad**.</span><span class="sxs-lookup"><span data-stu-id="5b899-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="5b899-120">Använd anpassad kod om du vill föra över det valda fältvärdet från Tidspost till Faktiska värden via raden med hjälp av transaktioners ursprung.</span><span class="sxs-lookup"><span data-stu-id="5b899-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="5b899-121">Mer information om transaktioners ursprung och anslutningar finns i [Länka faktiska värden till ursprungliga poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="5b899-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="5b899-122">Journalrader och grundläggande kostnadsöverföring</span><span class="sxs-lookup"><span data-stu-id="5b899-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="5b899-123">Mer information om utgiftspost finns i [Översikt över utgiftspost](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b899-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="5b899-124">Tid och material</span><span class="sxs-lookup"><span data-stu-id="5b899-124">Time and materials</span></span>

<span data-ttu-id="5b899-125">När en post för grundläggande utgift som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="5b899-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="5b899-126">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-126">Fixed price</span></span>

<span data-ttu-id="5b899-127">När en inlämnad grundläggande utgiftspost är länkad till ett projekt som är mappat till en fast prisavtal, skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="5b899-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="5b899-128">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="5b899-128">Default pricing</span></span>

<span data-ttu-id="5b899-129">Logiken för att ange standardpriser för utgifter baseras på utgiftskategorin.</span><span class="sxs-lookup"><span data-stu-id="5b899-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="5b899-130">Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="5b899-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5b899-131">De fält som påverkar standardpriser, t.ex. **Transaktionskategori** och **Resursenhet** används för att bestämma lämpligt pris på journalraden.</span><span class="sxs-lookup"><span data-stu-id="5b899-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="5b899-132">Detta fungerar emellertid endast om prismodellen i prislistan är **Pris per enhet**.</span><span class="sxs-lookup"><span data-stu-id="5b899-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="5b899-133">Om prismodellen är **Vid kostnad** eller **Pålägg på kostnad** används det pris som anges när kostnadsposten skapas för kostnad och priset på försäljningsjournalraden beräknas baserat på prissättningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="5b899-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="5b899-134">Du kan lägga till ett anpassat fält i utgiftsposten.</span><span class="sxs-lookup"><span data-stu-id="5b899-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="5b899-135">Om du vill att fältvärdet ska spridas ut till faktiska värden skapar du fältet i tabellerna **Faktiska värden** och **Journalrad**.</span><span class="sxs-lookup"><span data-stu-id="5b899-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="5b899-136">Använd anpassad kod om du vill föra över det valda fältvärdet från Tidspost till Faktiska värden via raden med hjälp av transaktioners ursprung.</span><span class="sxs-lookup"><span data-stu-id="5b899-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="5b899-137">Mer information om transaktioners ursprung och anslutningar finns i [Länka faktiska värden till ursprungliga poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="5b899-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="5b899-138">Journalrader och inlämning av materialförbrukningslogg</span><span class="sxs-lookup"><span data-stu-id="5b899-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="5b899-139">Mer information om utgiftspost finns i [materialförbrukningslogg](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="5b899-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="5b899-140">Tid och material</span><span class="sxs-lookup"><span data-stu-id="5b899-140">Time and materials</span></span>

<span data-ttu-id="5b899-141">När en inskickad användningsloggpost för material länkas till ett projekt som är mappat till en tids- och materialkontraktrad skapas två faktureringsrader, en för kostnad och en för ofakturerad försäljning.</span><span class="sxs-lookup"><span data-stu-id="5b899-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="5b899-142">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-142">Fixed price</span></span>

<span data-ttu-id="5b899-143">När en inlämnad post för materialförbrukningslogg är länkad till ett projekt som är mappat till en fast prisavtal, skapar systemet en journalrad för kostnad.</span><span class="sxs-lookup"><span data-stu-id="5b899-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="5b899-144">Standardprissättning</span><span class="sxs-lookup"><span data-stu-id="5b899-144">Default pricing</span></span>

<span data-ttu-id="5b899-145">Logiken för att ange standardpriser för material baseras på produkten och enhetskombinationen.</span><span class="sxs-lookup"><span data-stu-id="5b899-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="5b899-146">Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista.</span><span class="sxs-lookup"><span data-stu-id="5b899-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5b899-147">De fält som påverkar standardpriser, t.ex. **Produkt-ID** och **Enhet** används för att bestämma lämpligt pris på journalraden.</span><span class="sxs-lookup"><span data-stu-id="5b899-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="5b899-148">Detta fungerar emellertid endast för katalogprodukter.</span><span class="sxs-lookup"><span data-stu-id="5b899-148">However, this only works for catalog products.</span></span> <span data-ttu-id="5b899-149">För inskrivningsprodukter används priset som angavs när posten för materialanvändningslogg skapades för kostnad och försäljningspris på journalraderna.</span><span class="sxs-lookup"><span data-stu-id="5b899-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="5b899-150">Du kan lägga till ett anpassat fält i posten **Materialförbrukningslogg**.</span><span class="sxs-lookup"><span data-stu-id="5b899-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="5b899-151">Om du vill att fältvärdet ska spridas ut till faktiska värden skapar du fältet i tabellerna **Faktiska värden** och **Journalrad**.</span><span class="sxs-lookup"><span data-stu-id="5b899-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="5b899-152">Använd anpassad kod om du vill föra över det valda fältvärdet från Tidspost till Faktiska värden via raden med hjälp av transaktioners ursprung.</span><span class="sxs-lookup"><span data-stu-id="5b899-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="5b899-153">Mer information om transaktioners ursprung och anslutningar finns i [Länka faktiska värden till ursprungliga poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="5b899-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="5b899-154">Använda postjournaler för att registrera kostnader</span><span class="sxs-lookup"><span data-stu-id="5b899-154">Use entry journals to record costs</span></span>

<span data-ttu-id="5b899-155">Du kan använda postjournaler för att registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms.</span><span class="sxs-lookup"><span data-stu-id="5b899-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5b899-156">Journaler kan användas för följande ändamål:</span><span class="sxs-lookup"><span data-stu-id="5b899-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="5b899-157">Flytta transaktionsdata från ett annat system till Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5b899-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="5b899-158">Registrera kostnader som har inträffat i ett annat system.</span><span class="sxs-lookup"><span data-stu-id="5b899-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="5b899-159">Kostnaderna kan vara anskaffnings- eller underleverantörskostnader.</span><span class="sxs-lookup"><span data-stu-id="5b899-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b899-160">Programmet verifierar inte journalradtypen eller den relaterade prissättningen som har angetts på journalraden.</span><span class="sxs-lookup"><span data-stu-id="5b899-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5b899-161">Därför bör endast en användare som är helt medveten om redovisningseffekten som faktiska värden har på projektet använda sig av postjournaler för att skapa verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="5b899-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="5b899-162">På grund av den här journaltypens inverkan bör du noggrant välja vem som har åtkomst till att skapa postjournaler.</span><span class="sxs-lookup"><span data-stu-id="5b899-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="5b899-163">Registrera faktiska värden baserat på projekthändelser</span><span class="sxs-lookup"><span data-stu-id="5b899-163">Record actuals based on project events</span></span>

<span data-ttu-id="5b899-164">Project Operations registrerar ekonomiska transaktioner som inträffar under ett projekt.</span><span class="sxs-lookup"><span data-stu-id="5b899-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5b899-165">Dessa transaktioner registreras som faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="5b899-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="5b899-166">I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.</span><span class="sxs-lookup"><span data-stu-id="5b899-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="5b899-167">Resursen tillhör samma organisationsenhet som projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5b899-168">Händelse</span><span class="sxs-lookup"><span data-stu-id="5b899-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5b899-169">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="5b899-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5b899-170">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5b899-171">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="5b899-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5b899-172">Tid och material</span><span class="sxs-lookup"><span data-stu-id="5b899-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5b899-173">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5b899-174">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="5b899-174">Actuals</span></span></th>
<th><span data-ttu-id="5b899-175">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b899-175">Transaction currency</span></span></th>
<th><span data-ttu-id="5b899-176">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-176">Fixed price</span></span></th>
<th><span data-ttu-id="5b899-177">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b899-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5b899-178">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="5b899-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5b899-179">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="5b899-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-180">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="5b899-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5b899-181">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="5b899-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b899-182">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="5b899-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b899-183">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-183">Cost actual</span></span></td>
<td><span data-ttu-id="5b899-184">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-185">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-186">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5b899-187">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-188">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-189">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="5b899-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5b899-190">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b899-191">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="5b899-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b899-192">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-192">Cost actual</span></span></td>
<td><span data-ttu-id="5b899-193">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-194">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-195">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-196">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-197">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-198">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="5b899-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b899-199">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-200">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="5b899-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b899-201">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b899-202">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="5b899-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b899-203">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b899-204">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-205">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="5b899-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-206">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-207">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-208">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-209">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-209">Billed sales</span></span></td>
<td><span data-ttu-id="5b899-210">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b899-211">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="5b899-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b899-212">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b899-213">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-214">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-215">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-216">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-217">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-218">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="5b899-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b899-219">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-220">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="5b899-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b899-221">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b899-222">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="5b899-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b899-223">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="5b899-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b899-224">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5b899-225">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="5b899-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5b899-226">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="5b899-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5b899-227">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-228">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-229">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-230">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-230">Billed sales</span></span></td>
<td><span data-ttu-id="5b899-231">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b899-232">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="5b899-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b899-233">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="5b899-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b899-234">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-235">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="5b899-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5b899-236">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-237">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="5b899-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b899-238">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="5b899-239">Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5b899-240">Händelse</span><span class="sxs-lookup"><span data-stu-id="5b899-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5b899-241">Fakturerbart eller sålt projekt</span><span class="sxs-lookup"><span data-stu-id="5b899-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5b899-242">Projekt i stadiet för försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5b899-243">Internt projekt</span><span class="sxs-lookup"><span data-stu-id="5b899-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5b899-244">Tid och material</span><span class="sxs-lookup"><span data-stu-id="5b899-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5b899-245">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5b899-246">Faktiska värden</span><span class="sxs-lookup"><span data-stu-id="5b899-246">Actuals</span></span></th>
<th><span data-ttu-id="5b899-247">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b899-247">Transaction currency</span></span></th>
<th><span data-ttu-id="5b899-248">Fast pris</span><span class="sxs-lookup"><span data-stu-id="5b899-248">Fixed price</span></span></th>
<th><span data-ttu-id="5b899-249">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="5b899-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5b899-250">En tidspost skapas.</span><span class="sxs-lookup"><span data-stu-id="5b899-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5b899-251">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="5b899-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-252">En tidspost skickas.</span><span class="sxs-lookup"><span data-stu-id="5b899-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5b899-253">Ingen aktivitet i entiteten för faktiska värden</span><span class="sxs-lookup"><span data-stu-id="5b899-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5b899-254">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="5b899-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b899-255">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-255">Cost actual</span></span></td>
<td><span data-ttu-id="5b899-256">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5b899-257">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5b899-258">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5b899-259">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5b899-260">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-261">Ofakturerad faktiskt försäljning - debiterbart</span><span class="sxs-lookup"><span data-stu-id="5b899-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5b899-262">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-263">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="5b899-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5b899-264">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="5b899-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-265">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="5b899-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5b899-266">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5b899-267">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</span><span class="sxs-lookup"><span data-stu-id="5b899-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5b899-268">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-268">Cost actual</span></span></td>
<td><span data-ttu-id="5b899-269">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-270">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-271">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-272">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-273">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="5b899-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-274">Kostnad för resursenhet</span><span class="sxs-lookup"><span data-stu-id="5b899-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5b899-275">Valuta för resursenhet</span><span class="sxs-lookup"><span data-stu-id="5b899-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-276">Försäljning inom organisationen</span><span class="sxs-lookup"><span data-stu-id="5b899-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5b899-277">Valuta för avtalande enhet</span><span class="sxs-lookup"><span data-stu-id="5b899-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-278">Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="5b899-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b899-279">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-280">Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="5b899-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b899-281">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b899-282">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="5b899-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b899-283">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b899-284">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-285">Fakturerad försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="5b899-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-286">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-287">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5b899-288">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-289">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-289">Billed sales</span></span></td>
<td><span data-ttu-id="5b899-290">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b899-291">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</span><span class="sxs-lookup"><span data-stu-id="5b899-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5b899-292">Ofakturerad återförd försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5b899-293">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-294">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-295">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-296">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b899-297">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-298">Fakturerad försäljning - debiterbar för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="5b899-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5b899-299">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-300">Fakturerad försäljning - icke-debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="5b899-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b899-301">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b899-302">En faktura korrigeras för att öka det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="5b899-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b899-303">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="5b899-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b899-304">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5b899-305">Fakturerad återförd försäljning för milstolpe</span><span class="sxs-lookup"><span data-stu-id="5b899-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5b899-306">Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></span><span class="sxs-lookup"><span data-stu-id="5b899-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5b899-307">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-308">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5b899-309">Saknas</span><span class="sxs-lookup"><span data-stu-id="5b899-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-310">Fakturerad försäljning</span><span class="sxs-lookup"><span data-stu-id="5b899-310">Billed sales</span></span></td>
<td><span data-ttu-id="5b899-311">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b899-312">En faktura korrigeras för att minska det debiterbara antalet.</span><span class="sxs-lookup"><span data-stu-id="5b899-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5b899-313">Fakturerad försäljning - återförd</span><span class="sxs-lookup"><span data-stu-id="5b899-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5b899-314">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-315">Fakturerad försäljning för den nya kvantiteten</span><span class="sxs-lookup"><span data-stu-id="5b899-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5b899-316">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b899-317">Ofakturerad försäljning - debiterbar för skillnaden</span><span class="sxs-lookup"><span data-stu-id="5b899-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5b899-318">Projektkontraktets valuta</span><span class="sxs-lookup"><span data-stu-id="5b899-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
