---
title: Arbeta med projektbaserade kontraktrader
description: I det här ämnet finns information om projektbaserade kontraktrader.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 14d880eccd5547c122ebe37b63022e64fa2fb6fe
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181744"
---
# <a name="work-with-projectbased-contract-lines"></a><span data-ttu-id="8985c-103">Arbeta med projektbaserade kontraktrader</span><span class="sxs-lookup"><span data-stu-id="8985c-103">Work with project–based contract lines</span></span>

<span data-ttu-id="8985c-104">Projektbaserade kontraktrader i Dynamics 365 Project Operations är utformade för att rymma uppskattningar och faktureringsavtal för specifika komponenter i projektarbetet med ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="8985c-104">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="8985c-105">Strukturen på en projektbaserad kontraktrad utökas för projektuppskattningar och faktureringsscenarier med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="8985c-105">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="8985c-106">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="8985c-106">Billing method</span></span>
- <span data-ttu-id="8985c-107">Mappning av projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="8985c-107">Project and task mapping</span></span>
- <span data-ttu-id="8985c-108">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="8985c-108">Included transaction classes</span></span>
- <span data-ttu-id="8985c-109">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="8985c-109">Not-to-exceed limit</span></span>
- <span data-ttu-id="8985c-110">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="8985c-110">Chargeability setup</span></span>
- <span data-ttu-id="8985c-111">Uppskattningar med hjälp av kontraktradsdetaljer</span><span class="sxs-lookup"><span data-stu-id="8985c-111">Estimates using contract line details</span></span>
- <span data-ttu-id="8985c-112">Kontraktradens kund</span><span class="sxs-lookup"><span data-stu-id="8985c-112">Contract line customers</span></span>

<span data-ttu-id="8985c-113">Följande fält finns på fliken **Allmänt** i projektbaserade kontraktrader.</span><span class="sxs-lookup"><span data-stu-id="8985c-113">The following fields are included on the **General** tab of project–based contract lines.</span></span> <span data-ttu-id="8985c-114">Med hjälp av dessa fält kan du ställa in grunden för en detaljerad grundläggande uppskattning och faktureringsordning för projektbaserat arbete.</span><span class="sxs-lookup"><span data-stu-id="8985c-114">These fields help to set up the basis for a detailed, ground–up estimate and the billing arrangements for project–based work.</span></span>

| <span data-ttu-id="8985c-115">Fält</span><span class="sxs-lookup"><span data-stu-id="8985c-115">Field</span></span> | <span data-ttu-id="8985c-116">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="8985c-116">Description</span></span> | <span data-ttu-id="8985c-117">Inverkan nedströms</span><span class="sxs-lookup"><span data-stu-id="8985c-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8985c-118">**Namn**</span><span class="sxs-lookup"><span data-stu-id="8985c-118">**Name**</span></span> | <span data-ttu-id="8985c-119">Namnet på den kontraktrad som identifierar den diskreta komponenten för det kontrakt som uppskattas.</span><span class="sxs-lookup"><span data-stu-id="8985c-119">The name of the contract line that identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="8985c-120">För ett projektkontrakt som har skapats utifrån en offert kopieras värdet från ett motsvarande värde på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-120">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="8985c-121">Fältvärdet kopieras till projektfakturaraden som skapas från den här kontraktraden när fakturan skapas.</span><span class="sxs-lookup"><span data-stu-id="8985c-121">This field value is copied to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="8985c-122">**Faktureringsmetod**</span><span class="sxs-lookup"><span data-stu-id="8985c-122">**Billing Method**</span></span> | <span data-ttu-id="8985c-123">I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-123">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8985c-124">Det här är ett alternativuppsättning som representerar de två huvudsakliga upphandlingsmodellerna som stöds av Project Operations:</span><span class="sxs-lookup"><span data-stu-id="8985c-124">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="8985c-125">- **Fast pris**</span><span class="sxs-lookup"><span data-stu-id="8985c-125">- **Fixed Price**</span></span></br><span data-ttu-id="8985c-126">- **Tid och material**</span><span class="sxs-lookup"><span data-stu-id="8985c-126">- **Time and Material**</span></span> | <span data-ttu-id="8985c-127">Den faktiska transaktionen bearbetas i enlighet med faktureringsmetoden för den refererade kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-127">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="8985c-128">Om den kontraktrad som har refererats av det faktiska värdet har en metod och en metod för materialfakturering skapas en kostnad och en faktisk fakturerad försäljningspost.</span><span class="sxs-lookup"><span data-stu-id="8985c-128">If the contract line referenced by the actual has a time and material billing method, a cost and an unbilled sales actual record are created.</span></span> <span data-ttu-id="8985c-129">Om kontraktraden som refereras av det faktiska värdet har en faktureringsmetod med fast pris skapas endast en verklig kostnad.</span><span class="sxs-lookup"><span data-stu-id="8985c-129">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="8985c-130">**Project**</span><span class="sxs-lookup"><span data-stu-id="8985c-130">**Project**</span></span> | <span data-ttu-id="8985c-131">Använd det här fältet om du vill identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="8985c-131">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="8985c-132">Värdet i det här fältet används tillsammans med fälten **inkluderade uppgifter** och **inkluderade transaktionsklasser** för att lösa kontraktradreferensen på en post för en faktisk post eller en post för beräkningsrader.</span><span class="sxs-lookup"><span data-stu-id="8985c-132">The value in this field is used in conjunction with **Included Tasks** and **Included Transaction Classes** fields to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8985c-133">**Inkludera tid**</span><span class="sxs-lookup"><span data-stu-id="8985c-133">**Include Time**</span></span> | <span data-ttu-id="8985c-134">En flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ingår på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-134">A flag indicates if time transactions or labor costs on the selected project are included on this contract line.</span></span> <span data-ttu-id="8985c-135">Ett **Nej**-värde anger att tidstransaktionerna och arbetskraftskostnaderna inte ska tas med på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-135">A **No** value indicates that the time transactions or labor costs will not be included on this contract line.</span></span> <span data-ttu-id="8985c-136">Ett **Ja**-värde anger att de ska vara.</span><span class="sxs-lookup"><span data-stu-id="8985c-136">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8985c-137">Fältvärdet används tillsammans med projekt för att lösa en kontraktradsreferens på en faktisk post eller en post för beräkningsrad.</span><span class="sxs-lookup"><span data-stu-id="8985c-137">This field value is used in conjunction with project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8985c-138">**Ta med utgift**</span><span class="sxs-lookup"><span data-stu-id="8985c-138">**Include Expense**</span></span> | <span data-ttu-id="8985c-139">En flagga anger om utgiftskostnader för det valda projektet kommer att ingå i den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-139">A flag indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8985c-140">Ett **Nej**-värde anger att utgiftskostnaden inte ska tas med på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-140">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="8985c-141">Ett **Ja**-värde anger att det ska vara.</span><span class="sxs-lookup"><span data-stu-id="8985c-141">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="8985c-142">Fältvärdet används tillsammans med projekt för att lösa en kontraktradsreferens på en faktisk post eller en post för beräkningsrad.</span><span class="sxs-lookup"><span data-stu-id="8985c-142">This field value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8985c-143">**Inkludera avgift**</span><span class="sxs-lookup"><span data-stu-id="8985c-143">**Include Fee**</span></span> | <span data-ttu-id="8985c-144">En flagga anger om avgifter för det valda projektet kommer att ingå i den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-144">A flag indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8985c-145">Ett **Nej**-värde anger att avgifter inte ska tas med på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-145">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="8985c-146">Ett **Ja**-värde anger att de ska vara.</span><span class="sxs-lookup"><span data-stu-id="8985c-146">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8985c-147">Fältvärdet används tillsammans med projekt för att lösa en kontraktradsreferens på en faktisk post eller en post för beräkningsrad.</span><span class="sxs-lookup"><span data-stu-id="8985c-147">This field value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8985c-148">**Avtalat belopp**</span><span class="sxs-lookup"><span data-stu-id="8985c-148">**Contracted Amount**</span></span> | <span data-ttu-id="8985c-149">På en kontraktrad med fast pris är det överenskommet värde som ska faktureras kunden för alla arbetskomponenter som är associerade med den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-149">On a fixed price contract line, this is the agreed-on value that will be invoiced to the customer for all the work components associated with this contract line.</span></span> <span data-ttu-id="8985c-150">På en kontraktrad för tid och material är detta belopp ett beräknat värde av det som ska faktureras kunden för alla arbetskomponenter som är associerade till den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-150">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="8985c-151">I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-151">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8985c-152">När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån beloppet på kontraktraddetaljer.</span><span class="sxs-lookup"><span data-stu-id="8985c-152">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="8985c-153">När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra beloppen i radinformationen.</span><span class="sxs-lookup"><span data-stu-id="8985c-153">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="8985c-154">På en kontraktrad med fast pris används det här värdet för att generera beloppet före skatt på periodiska faktureringsmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="8985c-154">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8985c-155">**Beräknad skatt**</span><span class="sxs-lookup"><span data-stu-id="8985c-155">**Estimated Tax**</span></span> | <span data-ttu-id="8985c-156">Användaren kan redigera fältet och ange det uppskattade momsbeloppet på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="8985c-156">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="8985c-157">När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet på kontraktraddetaljer.</span><span class="sxs-lookup"><span data-stu-id="8985c-157">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="8985c-158">När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra momsbeloppen i radinformationen.</span><span class="sxs-lookup"><span data-stu-id="8985c-158">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="8985c-159">På en kontraktrad med fast pris används det här värdet för att generera skatt på periodiska faktureringsmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="8985c-159">On a fixed price contract line, this value is used to generate tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8985c-160">**Kontrakterat belopp efter skatt**</span><span class="sxs-lookup"><span data-stu-id="8985c-160">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="8985c-161">Beloppet på kontraktraden efter skatt.</span><span class="sxs-lookup"><span data-stu-id="8985c-161">The contract line amount after tax.</span></span> <span data-ttu-id="8985c-162">Fältet är skrivskyddat och beräknas som **kontrakterat belopp + moms**.</span><span class="sxs-lookup"><span data-stu-id="8985c-162">This field is read-only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="8985c-163">På en kontraktrad med fast pris används det här värdet för att generera periodiska faktureringsmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="8985c-163">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="8985c-164">**Undre gräns**</span><span class="sxs-lookup"><span data-stu-id="8985c-164">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="8985c-165">Användaren kan redigera det här fältet och det är endast tillgängligt på projektbaserade kontraktrader som har en metod för fakturering av tid och material.</span><span class="sxs-lookup"><span data-stu-id="8985c-165">The user can edit this field and it is only available on project-based contract lines that have a time and material billing method.</span></span> | <span data-ttu-id="8985c-166">Användaren kan redigera det här fältet.</span><span class="sxs-lookup"><span data-stu-id="8985c-166">The user can edit this field.</span></span> <span data-ttu-id="8985c-167">När en tid eller kostnad faktiskt refererar till den här kontraktraden för tid och material, utvärderas det faktiska beloppet mot gränsen för undre gräns för den här kontraktraden efter redovisning för redan förbrukade och bekräftade belopp.</span><span class="sxs-lookup"><span data-stu-id="8985c-167">When a time or expense actual references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on this contract line after accounting for the already spent and committed amounts.</span></span> |
| <span data-ttu-id="8985c-168">**Kundbudget**</span><span class="sxs-lookup"><span data-stu-id="8985c-168">**Customer Budget**</span></span> | <span data-ttu-id="8985c-169">Det här fältet kan redigeras och kopieras från motsvarande fält på offertraden om kontraktet skapades från en offert.</span><span class="sxs-lookup"><span data-stu-id="8985c-169">This field is editable and is copied from the corresponding field on the quote line, if the contract was created from a quote.</span></span> | <span data-ttu-id="8985c-170">Det här fältet används endast för information och har inte någon efterföljande betydelse.</span><span class="sxs-lookup"><span data-stu-id="8985c-170">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="8985c-171">Valideringsregel för alternativen på fliken Allmänt i projektbaserade kontraktrader</span><span class="sxs-lookup"><span data-stu-id="8985c-171">Validation rule for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="8985c-172">Regel: ett projekt och en viss transaktionsklass kan endast tas med på en projektbaserade kontraktrad i ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="8985c-172">Rule: A project and a certain transaction class can only be included on one project-based contract line in a contract.</span></span>

| <span data-ttu-id="8985c-173">Kontrakt</span><span class="sxs-lookup"><span data-stu-id="8985c-173">Contract</span></span> | <span data-ttu-id="8985c-174">Kontraktrad</span><span class="sxs-lookup"><span data-stu-id="8985c-174">Contract line</span></span> | <span data-ttu-id="8985c-175">Project</span><span class="sxs-lookup"><span data-stu-id="8985c-175">Project</span></span> | <span data-ttu-id="8985c-176">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="8985c-176">Include time</span></span> | <span data-ttu-id="8985c-177">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="8985c-177">Include expense</span></span> | <span data-ttu-id="8985c-178">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="8985c-178">Include fee</span></span> | <span data-ttu-id="8985c-179">Giltigt/ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-179">Valid/not valid</span></span> | <span data-ttu-id="8985c-180">Anledning</span><span class="sxs-lookup"><span data-stu-id="8985c-180">Reason</span></span>                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8985c-181">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-181">C1</span></span>       | <span data-ttu-id="8985c-182">CL1</span><span class="sxs-lookup"><span data-stu-id="8985c-182">CL1</span></span>           | <span data-ttu-id="8985c-183">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-183">P1</span></span>      | <span data-ttu-id="8985c-184">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-184">Yes</span></span>          | <span data-ttu-id="8985c-185">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-185">Yes</span></span>             | <span data-ttu-id="8985c-186">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-186">Yes</span></span>         | <span data-ttu-id="8985c-187">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-187">Not valid</span></span>       | <span data-ttu-id="8985c-188">Bryter mot regeln.</span><span class="sxs-lookup"><span data-stu-id="8985c-188">Violates the rule.</span></span> <span data-ttu-id="8985c-189">Tid, utgifter och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.</span><span class="sxs-lookup"><span data-stu-id="8985c-189">Time,   expense, and fees on project P1 are included on both contract lines, CL1 and   CL2.</span></span>                                                                                       |
| <span data-ttu-id="8985c-190">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-190">C1</span></span>       | <span data-ttu-id="8985c-191">CL2</span><span class="sxs-lookup"><span data-stu-id="8985c-191">CL2</span></span>           | <span data-ttu-id="8985c-192">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-192">P1</span></span>      | <span data-ttu-id="8985c-193">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-193">Yes</span></span>          | <span data-ttu-id="8985c-194">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-194">Yes</span></span>             | <span data-ttu-id="8985c-195">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-195">Yes</span></span>         | <span data-ttu-id="8985c-196">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-196">Not valid</span></span>       | <span data-ttu-id="8985c-197">Bryter mot regeln.</span><span class="sxs-lookup"><span data-stu-id="8985c-197">Violates the rule.</span></span> <span data-ttu-id="8985c-198">Tid, utgifter och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.</span><span class="sxs-lookup"><span data-stu-id="8985c-198">Time,   expense, and fees on project P1 are included on both contract lines, CL1 and   CL2.</span></span>                                                                                       |
| <span data-ttu-id="8985c-199">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-199">C1</span></span>       | <span data-ttu-id="8985c-200">CL1</span><span class="sxs-lookup"><span data-stu-id="8985c-200">CL1</span></span>           | <span data-ttu-id="8985c-201">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-201">P1</span></span>      | <span data-ttu-id="8985c-202">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-202">Yes</span></span>          | <span data-ttu-id="8985c-203">Inga</span><span class="sxs-lookup"><span data-stu-id="8985c-203">No</span></span>              | <span data-ttu-id="8985c-204">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-204">Yes</span></span>         | <span data-ttu-id="8985c-205">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-205">Not valid</span></span>       | <span data-ttu-id="8985c-206">Bryter mot regeln.</span><span class="sxs-lookup"><span data-stu-id="8985c-206">Violates the rule.</span></span> <span data-ttu-id="8985c-207">Tid och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.</span><span class="sxs-lookup"><span data-stu-id="8985c-207">Time and   fees on project P1 are included on both contract lines, CL1 and CL2.</span></span>                                                                                                   |
| <span data-ttu-id="8985c-208">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-208">C1</span></span>       | <span data-ttu-id="8985c-209">CL2</span><span class="sxs-lookup"><span data-stu-id="8985c-209">CL2</span></span>           | <span data-ttu-id="8985c-210">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-210">P1</span></span>      | <span data-ttu-id="8985c-211">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-211">Yes</span></span>          | <span data-ttu-id="8985c-212">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-212">Yes</span></span>             | <span data-ttu-id="8985c-213">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-213">Yes</span></span>         | <span data-ttu-id="8985c-214">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-214">Not valid</span></span>       | <span data-ttu-id="8985c-215">Bryter mot regeln.</span><span class="sxs-lookup"><span data-stu-id="8985c-215">Violates the rule.</span></span> <span data-ttu-id="8985c-216">Tid och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.</span><span class="sxs-lookup"><span data-stu-id="8985c-216">Time and   fees on project P1 are included on both contract lines, CL1 and CL2.</span></span>                                                                                                   |
| <span data-ttu-id="8985c-217">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-217">C1</span></span>       | <span data-ttu-id="8985c-218">CL1</span><span class="sxs-lookup"><span data-stu-id="8985c-218">CL1</span></span>           | <span data-ttu-id="8985c-219">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-219">P1</span></span>      | <span data-ttu-id="8985c-220">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-220">Yes</span></span>          | <span data-ttu-id="8985c-221">Inga</span><span class="sxs-lookup"><span data-stu-id="8985c-221">No</span></span>              | <span data-ttu-id="8985c-222">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-222">Yes</span></span>         | <span data-ttu-id="8985c-223">Giltig</span><span class="sxs-lookup"><span data-stu-id="8985c-223">Valid</span></span>           | <span data-ttu-id="8985c-224">Tid och avgifter för projekt P1 ingår på CL1.</span><span class="sxs-lookup"><span data-stu-id="8985c-224">Time and fees on project P1 are   included on the CL1.</span></span> <span data-ttu-id="8985c-225">Utgiften på P1-projektet ingår i CL2.</span><span class="sxs-lookup"><span data-stu-id="8985c-225">Expense on project P1 is included on CL2.</span></span> </br>   <span data-ttu-id="8985c-226">Det finns ingen överlappning i vad som ska tas med på varje kontraktrad och är därför giltigt.</span><span class="sxs-lookup"><span data-stu-id="8985c-226">There is no overlap in what is being included on each contract line and is   therefore valid.</span></span>  |
| <span data-ttu-id="8985c-227">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-227">C1</span></span>       | <span data-ttu-id="8985c-228">CL2</span><span class="sxs-lookup"><span data-stu-id="8985c-228">CL2</span></span>           | <span data-ttu-id="8985c-229">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-229">P1</span></span>      | <span data-ttu-id="8985c-230">Inga</span><span class="sxs-lookup"><span data-stu-id="8985c-230">No</span></span>           | <span data-ttu-id="8985c-231">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-231">Yes</span></span>             | <span data-ttu-id="8985c-232">Inga</span><span class="sxs-lookup"><span data-stu-id="8985c-232">No</span></span>          | <span data-ttu-id="8985c-233">Giltig</span><span class="sxs-lookup"><span data-stu-id="8985c-233">Valid</span></span>           | <span data-ttu-id="8985c-234">Tid och avgifter för projekt P1 ingår på CL1.</span><span class="sxs-lookup"><span data-stu-id="8985c-234">Time and fees on project P1 are   included on the CL1.</span></span> <span data-ttu-id="8985c-235">Utgiften på P1-projektet ingår i CL2.</span><span class="sxs-lookup"><span data-stu-id="8985c-235">Expense on project P1 is included on CL2.</span></span> </br>   <span data-ttu-id="8985c-236">Det finns ingen överlappning i vad som ska tas med på varje kontraktrad och är därför giltigt.</span><span class="sxs-lookup"><span data-stu-id="8985c-236">There is no overlap in what is being included on each contract line and is   therefore valid.</span></span>  |
| <span data-ttu-id="8985c-237">C1</span><span class="sxs-lookup"><span data-stu-id="8985c-237">C1</span></span>       | <span data-ttu-id="8985c-238">CL1</span><span class="sxs-lookup"><span data-stu-id="8985c-238">CL1</span></span>           | <span data-ttu-id="8985c-239">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-239">P1</span></span>      | <span data-ttu-id="8985c-240">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-240">Yes</span></span>          | <span data-ttu-id="8985c-241">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-241">Yes</span></span>             | <span data-ttu-id="8985c-242">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-242">Yes</span></span>         | <span data-ttu-id="8985c-243">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-243">Not valid</span></span>       | <span data-ttu-id="8985c-244">Bryter mot regeln.</span><span class="sxs-lookup"><span data-stu-id="8985c-244">Violates the rule.</span></span> <span data-ttu-id="8985c-245">Tid, utgifter och avgifter i projekt P1 tas med på raderna på de två kontrakten.</span><span class="sxs-lookup"><span data-stu-id="8985c-245">Time,   expense, and fees on project P1 are included on the lines of two contracts.</span></span>                                                                                               |
| <span data-ttu-id="8985c-246">CL2</span><span class="sxs-lookup"><span data-stu-id="8985c-246">CL2</span></span>      | <span data-ttu-id="8985c-247">CL2</span><span class="sxs-lookup"><span data-stu-id="8985c-247">CL2</span></span>           | <span data-ttu-id="8985c-248">P1</span><span class="sxs-lookup"><span data-stu-id="8985c-248">P1</span></span>      | <span data-ttu-id="8985c-249">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-249">Yes</span></span>          | <span data-ttu-id="8985c-250">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-250">Yes</span></span>             | <span data-ttu-id="8985c-251">Ja</span><span class="sxs-lookup"><span data-stu-id="8985c-251">Yes</span></span>         | <span data-ttu-id="8985c-252">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8985c-252">Not valid</span></span>       | <span data-ttu-id="8985c-253">Bryter mot regeln.</span><span class="sxs-lookup"><span data-stu-id="8985c-253">Violates the rule.</span></span> <span data-ttu-id="8985c-254">Tid, utgifter och avgifter i projekt P1 tas med på raderna på de två kontrakten.</span><span class="sxs-lookup"><span data-stu-id="8985c-254">Time,   expense, and fees on project P1 are included on the lines of two contracts.</span></span>                                                                                               |