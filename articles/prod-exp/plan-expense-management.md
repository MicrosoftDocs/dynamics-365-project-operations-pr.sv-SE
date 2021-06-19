---
title: Konfigurera utgiftshantering
description: I den här artikeln beskrivs vad du bör tänka på samt vilka beslut du måste fatta under planeringsprocessen innan du konfigurerar utgiftshantering i Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005408"
---
# <a name="configure-expense-management"></a><span data-ttu-id="2d1ed-103">Konfigurera utgiftshantering</span><span class="sxs-lookup"><span data-stu-id="2d1ed-103">Configure expense management</span></span>

<span data-ttu-id="2d1ed-104">I det här ämnet beskrivs vad du bör tänka på samt vilka beslut du måste fatta under planeringsprocessen innan du konfigurerar utgiftshantering.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="2d1ed-105">I utgiftshantering kan du lagra information om betalningsmetoder, reserekvisitioner, utgiftsrapporter, principer och så vidare.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="2d1ed-106">Många av de beslut du fattar när du planerar din konfiguration av utgiftshantering bygger på organisationens hierarki och finansiella struktur, men du måste läsa planeringsdokumenten för dessa områden.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="2d1ed-107">Koncerninterna utgifter</span><span class="sxs-lookup"><span data-stu-id="2d1ed-107">Intercompany expenses</span></span>

<span data-ttu-id="2d1ed-108">När du aktiverar koncerninterna utgifter tillåter du att juridiska personer och medarbetare ådrar sig utgifter för en annan juridisk persons räkning och samlar in betalning från den juridiska personen inom organisationen.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="2d1ed-109">Exempel: En anställd i juridisk person A färdigställer ett projekt för juridisk person B och projektet ådrar sig resekostnader.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="2d1ed-110">Om koncerninterna kostnader har aktiverats kan medarbetaren sedan skicka in en utgiftsrapport som bokför utgiften till juridisk person B och kostnaden måste sedan betalas av juridisk person A. Om organisationen inte har flera juridiska personer behöver du inte aktivera koncerninterna utgifter.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="2d1ed-111">**Beslut:** Vill du aktivera koncerninterna utgifter?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="2d1ed-112">Ekonomihantering</span><span class="sxs-lookup"><span data-stu-id="2d1ed-112">Financial management</span></span>

<span data-ttu-id="2d1ed-113">Utgiftshantering är nära integrerad med den ekonomiska förvaltningen av organisationen.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="2d1ed-114">Mycket av din konfiguration av utgiftshanteringen bygger på de beslut som du har fattat om organisationens ekonomi.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="2d1ed-115">I följande avsnitt beskrivs de olika områden som kräver planering och beslut, utifrån organisationens ekonomiska beslut och vägledning från ditt ledarskapsteam.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="2d1ed-116">Traktamente</span><span class="sxs-lookup"><span data-stu-id="2d1ed-116">Per diems</span></span>

<span data-ttu-id="2d1ed-117">Du måste definiera traktamenten för medarbetare som din organisation tillhandahåller.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="2d1ed-118">Eftersom traktamenten vanligtvis används för att täcka utgifter som måltider, logi och andra oförutsedda utgifter, kan du skapa regler för traktamenten som organisationen erbjuder.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="2d1ed-119">Traktamentstaxa kan baseras på tid på året, resmål eller både och.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="2d1ed-120">När du definierar en traktamentsregel kan du ange att en procentsats av traktamentstaxan ska dras in om en arbetare får gratis måltider eller tjänster.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="2d1ed-121">Du kan även definiera nivåer av traktamentstaxa för att ange ett minsta och högsta antal timmar som traktamentstaxan kan gälla för en arbetares resa.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="2d1ed-122">**Beslut:**</span><span class="sxs-lookup"><span data-stu-id="2d1ed-122">**Decisions:**</span></span>

- <span data-ttu-id="2d1ed-123">Förvalda traktamentsregler för första och sista dagen:</span><span class="sxs-lookup"><span data-stu-id="2d1ed-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="2d1ed-124">Vad är det minsta antalet timmar som en medarbetare kan ansöka om för en dag och fortfarande få traktamente?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="2d1ed-125">Finns det en minskning av beloppet som erbjuds för måltider för första dagen och sista dagen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="2d1ed-126">Om det finns en reducering, vad är procentsatsen för minskningen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="2d1ed-127">Finns det en minskning av beloppet som erbjuds för ett hotell för första dagen och sista dagen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="2d1ed-128">Om det finns en reducering, vad är procentsatsen för minskningen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="2d1ed-129">Finns det en minskning av beloppet som erbjuds för andra utgifter som uppstår för första dagen och sista dagen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="2d1ed-130">Om det finns en reducering, vad är procentsatsen för minskningen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="2d1ed-131">Standardregler för traktamente:</span><span class="sxs-lookup"><span data-stu-id="2d1ed-131">Default per diem rules:</span></span>

    - <span data-ttu-id="2d1ed-132">Finns det till exempel en procentsats för minskning av traktamentet för varje måltid om måltider är kostnadsfria?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="2d1ed-133">Om det finns en reducering, vad är procentsatsen för minskningen för varje måltid?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="2d1ed-134">Beräknas minskningen för måltider per dag, per resa eller per antal måltider per dag?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="2d1ed-135">Ska traktamentets belopp avrundas på vanligt sätt eller avrundas uppåt?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="2d1ed-136">Beräknas traktamentet för en 24-timmarsperiod eller en kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="2d1ed-137">Traktamentsregler som baseras på plats:</span><span class="sxs-lookup"><span data-stu-id="2d1ed-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="2d1ed-138">Varierar traktamentstaxan beroende på plats?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="2d1ed-139">Vilka platser ingår?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-139">What locations are included?</span></span>
    - <span data-ttu-id="2d1ed-140">Om traktamentstaxan varierar beroende på plats kan du för varje plats ange vilken procentsats som ska användas för följande typer av utgifter:</span><span class="sxs-lookup"><span data-stu-id="2d1ed-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="2d1ed-141">Måltider</span><span class="sxs-lookup"><span data-stu-id="2d1ed-141">Meals</span></span>
        - <span data-ttu-id="2d1ed-142">Hotell</span><span class="sxs-lookup"><span data-stu-id="2d1ed-142">Hotel</span></span>
        - <span data-ttu-id="2d1ed-143">Andra utgifter</span><span class="sxs-lookup"><span data-stu-id="2d1ed-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="2d1ed-144">Journaler och konton för utgiftshantering</span><span class="sxs-lookup"><span data-stu-id="2d1ed-144">Expense management journals and accounts</span></span>

<span data-ttu-id="2d1ed-145">Utgiftshantering kräver att du använder flera journaler och konton.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="2d1ed-146">Du måste till exempel bestämma om samma konto ska användas för förskott och kreditkortstvister.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="2d1ed-147">**Beslut:**</span><span class="sxs-lookup"><span data-stu-id="2d1ed-147">**Decisions:**</span></span>

- <span data-ttu-id="2d1ed-148">Vilken redovisningsjournal bokförs godkända utgiftsrapporter i?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="2d1ed-149">Vilket konto används för kontantförskott?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="2d1ed-150">Ska kontantförskott bokföras direkt?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="2d1ed-151">Betalningsmetoder</span><span class="sxs-lookup"><span data-stu-id="2d1ed-151">Payment methods</span></span>

<span data-ttu-id="2d1ed-152">När du tillåter medarbetare att ådra sig utgifter för företagets räkning måste du definiera de betalningsmetoder som medarbetarna får använda.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="2d1ed-153">Du kan till exempel tillåta anställda att använda kontanter eller ett företagskreditkort.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="2d1ed-154">Du kan även tillåta anställda att använda privata kreditkort och sedan återbetala de anställda.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="2d1ed-155">Du måste fatta följande beslut för varje betalningsmetod som du tillåter.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="2d1ed-156">**Beslut:**</span><span class="sxs-lookup"><span data-stu-id="2d1ed-156">**Decisions:**</span></span>

- <span data-ttu-id="2d1ed-157">Vilka betalningsmetoder är tillåtna?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="2d1ed-158">Vem äger utgifterna för betalningsmetoden?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="2d1ed-159">Finns det en motkontotyp?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-159">Is there an offset account type?</span></span> <span data-ttu-id="2d1ed-160">Om det finns en motkontotyp anger du den.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="2d1ed-161">Om det finns en motkontotyp anger du kontot.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="2d1ed-162">Om betalningsmetoden är ett kreditkort ska betalningsmetoden endast användas med importerade transaktioner?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="2d1ed-163">Utgiftskategorier och delade kategorier</span><span class="sxs-lookup"><span data-stu-id="2d1ed-163">Expense categories and shared categories</span></span>

<span data-ttu-id="2d1ed-164">När medarbetare skapar en utgiftsrapport måste varje utgiftspost vara associerad med en utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="2d1ed-165">Utgiftskategorier härleds från delade kategorier som kan delas av alla juridiska entiteter i organisationen.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="2d1ed-166">Kategorierna kan även delas i projekthantering och redovisning, beroende på hur organisationen har definierats.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="2d1ed-167">Baserat på definitionen av din organisation och vägledning från implementeringsteamet avgör du om kategorierna som används i utgiftshantering endast ska användas i utgiftshantering eller delas mellan projekthantering och redovisning och utgiftshantering.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="2d1ed-168">Observera att dessa kategorier kan delas mellan projekt och utgifter eller projekt och produktion, men inte mellan utgifter och produktion.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="2d1ed-169">Du måste fatta följande beslut för varje utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="2d1ed-170">**Beslut:**</span><span class="sxs-lookup"><span data-stu-id="2d1ed-170">**Decisions:**</span></span>

- <span data-ttu-id="2d1ed-171">Vilken är utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-171">What is the expense category?</span></span> <span data-ttu-id="2d1ed-172">Exempel är kategorier för flygningar, hotell och sträcka.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="2d1ed-173">Kan utgiftskategorin också användas i projekthantering och redovisning?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="2d1ed-174">Vilken är utgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-174">What is the expense type?</span></span>
- <span data-ttu-id="2d1ed-175">Vilken är standardbetalningsmetoden för utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="2d1ed-176">Måste utgifter i utgiftskategorin specificeras?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="2d1ed-177">Vilken är det huvudsakliga standardkontot utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="2d1ed-178">Vad är standardmomsgruppen för utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="2d1ed-179">Är fler betalningsmetoder tillåtna i utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="2d1ed-180">Om ytterligare betalningsmetoder tillåts anger du dem.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="2d1ed-181">Finns det några underkategorier i den här utgiftskategorin?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="2d1ed-182">Om det finns underkategorier måste du också fatta följande beslut:</span><span class="sxs-lookup"><span data-stu-id="2d1ed-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="2d1ed-183">Har någon av underkategorierna exkluderats från momsåterbetalning?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="2d1ed-184">Vad är momsgruppen för underkategorierna?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="2d1ed-185">Om utgiftskategorin också används i projekthantering och redovisning ska du besvara de återstående frågorna.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="2d1ed-186">Annars går du vidare till nästa avsnitt.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="2d1ed-187">Vilka kostnadskonton ska användas för följande utgifter?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="2d1ed-188">Kostnad</span><span class="sxs-lookup"><span data-stu-id="2d1ed-188">Cost</span></span>
    - <span data-ttu-id="2d1ed-189">Löneallokering</span><span class="sxs-lookup"><span data-stu-id="2d1ed-189">Payroll allocation</span></span>
    - <span data-ttu-id="2d1ed-190">PIA-kostnadsvärde</span><span class="sxs-lookup"><span data-stu-id="2d1ed-190">WIP-cost value</span></span>
    - <span data-ttu-id="2d1ed-191">Kostnadsartikel</span><span class="sxs-lookup"><span data-stu-id="2d1ed-191">Cost-item</span></span>
    - <span data-ttu-id="2d1ed-192">PIA-kostnad värdeartikel</span><span class="sxs-lookup"><span data-stu-id="2d1ed-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="2d1ed-193">Upplupen förlust</span><span class="sxs-lookup"><span data-stu-id="2d1ed-193">Accrued loss</span></span>
    - <span data-ttu-id="2d1ed-194">PIA, upplupen förlust</span><span class="sxs-lookup"><span data-stu-id="2d1ed-194">WIP-accrued loss</span></span>

- <span data-ttu-id="2d1ed-195">Vilka intäktskonton ska användas för följande?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="2d1ed-196">Fakturerad intäkt</span><span class="sxs-lookup"><span data-stu-id="2d1ed-196">Invoiced revenue</span></span>
    - <span data-ttu-id="2d1ed-197">Upplupna intäkter – försäljningsvärde</span><span class="sxs-lookup"><span data-stu-id="2d1ed-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="2d1ed-198">Pia – försäljningsvärde</span><span class="sxs-lookup"><span data-stu-id="2d1ed-198">WIP-sales value</span></span>
    - <span data-ttu-id="2d1ed-199">Upplupna intäkter – produktion</span><span class="sxs-lookup"><span data-stu-id="2d1ed-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="2d1ed-200">PIA – Produktion</span><span class="sxs-lookup"><span data-stu-id="2d1ed-200">WIP-production</span></span>
    - <span data-ttu-id="2d1ed-201">Upplupna intäkter – vinst</span><span class="sxs-lookup"><span data-stu-id="2d1ed-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="2d1ed-202">PIA – vinst</span><span class="sxs-lookup"><span data-stu-id="2d1ed-202">WIP-profit</span></span>
    - <span data-ttu-id="2d1ed-203">Upplupna intäkter – prenumeration</span><span class="sxs-lookup"><span data-stu-id="2d1ed-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="2d1ed-204">PIA-prenumeration</span><span class="sxs-lookup"><span data-stu-id="2d1ed-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="2d1ed-205">Skatter</span><span class="sxs-lookup"><span data-stu-id="2d1ed-205">Taxes</span></span>

<span data-ttu-id="2d1ed-206">För utgiftrelaterad skatt måste du bestämma vad som ska tas med eller vara aktiverat i utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="2d1ed-207">**Beslut:**</span><span class="sxs-lookup"><span data-stu-id="2d1ed-207">**Decisions:**</span></span>

- <span data-ttu-id="2d1ed-208">Ingår moms i utgiftsbeloppen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="2d1ed-209">Ska återbetalning av skatt aktiveras på utgifter?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="2d1ed-210">När du planerar redovisningen kan du inte aktivera återbetalning av skatt för utgifter om du beslutade att tillämpa amerikanska moms- och skatteregler.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="2d1ed-211">(För att tillämpa amerikanska moms- och skatteregler ställer du in alternativet **Tillämpa momsregler** på **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="2d1ed-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="2d1ed-212">Principer</span><span class="sxs-lookup"><span data-stu-id="2d1ed-212">Policies</span></span>

<span data-ttu-id="2d1ed-213">Genom att skapa principer för utgiftsrapporter kan du hjälpa organisationen att spara tid och pengar när anställda ådrar sig utgifter för dess räkning.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="2d1ed-214">Med hjälp av principer garanteras att medarbetarna håller sig inom budgeten, anger all information som krävs och att de endast spenderar pengar efter behov.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="2d1ed-215">Du måste fatta följande beslut för varje utgiftsrapportprincip och varje princip för godkännande av utgiftsrapporter som du skapar.</span><span class="sxs-lookup"><span data-stu-id="2d1ed-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="2d1ed-216">**Beslut:**</span><span class="sxs-lookup"><span data-stu-id="2d1ed-216">**Decisions:**</span></span>

- <span data-ttu-id="2d1ed-217">Vad är namnet på principen?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-217">What is the name of the policy?</span></span>
- <span data-ttu-id="2d1ed-218">Vad används utgiftsprincipen till?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-218">What is the expense policy for?</span></span>
- <span data-ttu-id="2d1ed-219">Om du tidigare har beslutat att aktivera koncerninterna utgifter, vilka företag i organisationen gäller den här principen för?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="2d1ed-220">När börjar principen gälla?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-220">When does the policy become effective?</span></span>
- <span data-ttu-id="2d1ed-221">När upphör principen att gälla?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-221">When does the policy expire?</span></span>
- <span data-ttu-id="2d1ed-222">Vad är principregeln?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-222">What is the policy rule?</span></span>
- <span data-ttu-id="2d1ed-223">Vad är resultatet av principregeln?</span><span class="sxs-lookup"><span data-stu-id="2d1ed-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]