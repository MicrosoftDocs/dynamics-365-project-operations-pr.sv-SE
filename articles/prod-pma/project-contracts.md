---
title: Projektkontrakt
description: I det här ämnet finns exempel på de projektkontrakt som du kan skapa för olika typer av projekt och finansieringskällor och hur du kan hantera kontrakt och fakturera projektkunder.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085671"
---
# <a name="project-contracts"></a><span data-ttu-id="45449-103">Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="45449-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45449-104">I det här ämnet finns exempel på de projektkontrakt som du kan skapa för olika typer av projekt och finansieringskällor och hur du kan hantera kontrakt och fakturera projektkunder.</span><span class="sxs-lookup"><span data-stu-id="45449-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="45449-105">Den typ av projekt som du skapar för ett projektkontrakt avgör vilken metod som används för att fakturera projektkunderna.</span><span class="sxs-lookup"><span data-stu-id="45449-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="45449-106">Du kan ändra ett projektkontrakt och ett relaterat projekt, men du kan inte ändra projekttypen.</span><span class="sxs-lookup"><span data-stu-id="45449-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="45449-107">Genom att använda ett projektkontrakt kan du fakturera ett eller flera projekt samtidigt.</span><span class="sxs-lookup"><span data-stu-id="45449-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="45449-108">Projektkontraktet ger även garanti för ett konsekvent faktureringsförfarande för varje del projekt i en projektstruktur.</span><span class="sxs-lookup"><span data-stu-id="45449-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="45449-109">Alla projekt som ska faktureras måste kopplas till ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="45449-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="45449-110">Inställningarna för ett projektkontrakt gäller för alla projekt och del projekt som är associerade med projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="45449-111">Ett projektkontrakt kan ange en eller flera finansieringskällor.</span><span class="sxs-lookup"><span data-stu-id="45449-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="45449-112">Därför kan du dela upp faktureringen mellan flera olika fonder, ange finansieringsgränser så att finansieringskällor inte faktureras mer än ett visst belopp och konfigurera finansieringsregler för debitering av utgifter.</span><span class="sxs-lookup"><span data-stu-id="45449-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="45449-113">Finansiering av projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="45449-113">Funding for project contracts</span></span>
<span data-ttu-id="45449-114">I vissa projektkontrakt anges att flera parter delar ansvaret för att finansiera projektkostnaderna.</span><span class="sxs-lookup"><span data-stu-id="45449-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="45449-115">Här följer några exempel:</span><span class="sxs-lookup"><span data-stu-id="45449-115">Here are some examples:</span></span>

-   <span data-ttu-id="45449-116">En stor kund som har en förfrågan om flera divisioner som påverkar projektets finansiering.</span><span class="sxs-lookup"><span data-stu-id="45449-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="45449-117">Företaget delar kostnaderna för ett stort projekt med en extern organisation.</span><span class="sxs-lookup"><span data-stu-id="45449-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="45449-118">Ett vägprojekt finansieras av två kommuner.</span><span class="sxs-lookup"><span data-stu-id="45449-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="45449-119">Ett broprojekt finansieras av ett statligt bidrag och ett privat företag.</span><span class="sxs-lookup"><span data-stu-id="45449-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="45449-120">I Dynamics 365 Finance kan du dela upp faktureringen för en enskild transaktion eller ett helt projekt bland flera kunder, bidrag eller organisationer.</span><span class="sxs-lookup"><span data-stu-id="45449-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="45449-121">I projekt som har flera fonder kallas alla parter som bidrar till finansieringen av ett avancerat finansieringsprojekt för finansieringskällor.</span><span class="sxs-lookup"><span data-stu-id="45449-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="45449-122">När en kund, organisation eller ett bidrag har definierats som en finansieringskälla kan den tilldelas en eller flera finansieringsregler.</span><span class="sxs-lookup"><span data-stu-id="45449-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="45449-123">Finansieringsregler innehåller kriterier som avgör hur avgifter fördelas till olika finansieringskällor för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="45449-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="45449-124">Eftersom lagerartiklar, t.ex. de som visas på inköpsrekvisitioner och inköpsorder, inte kan delas, kan kostnadsbeloppet inte delas upp mellan flera finansieringskällor vid distributionstillfället.</span><span class="sxs-lookup"><span data-stu-id="45449-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="45449-125">Därför kvarstår värdet för finansieringskällan som 0 (noll) tills lagerproblemet bokförs.</span><span class="sxs-lookup"><span data-stu-id="45449-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="45449-126">När lager utleveransen har bokförts fördelas kostnadsbeloppet enligt konto distributionsreglerna för projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="45449-127">Här följer några steg som du kan vidta för att göra det lättare att dela faktureringen mellan flera finansieringskällor:</span><span class="sxs-lookup"><span data-stu-id="45449-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="45449-128">Ange att alla transaktioner som anges för ett projekt använder samma försäljningsvaluta som projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="45449-129">Ställ in finansieringsgränser så att en finansieringskälla inte faktureras mer än ett visst belopp mot ett projekt.</span><span class="sxs-lookup"><span data-stu-id="45449-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="45449-130">Konfigurera finansieringsregler och finansieringsgränser för varje arbetare, artikel, kategori, kategorigrupp och transaktionstyp (eller för alla transaktionstyper).</span><span class="sxs-lookup"><span data-stu-id="45449-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="45449-131">Välj valfria start- och slutdatum för att definiera den period när varje finansieringsregel är giltig.</span><span class="sxs-lookup"><span data-stu-id="45449-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="45449-132">Ange den procentsats som varje finansieringskälla är ansvarig för.</span><span class="sxs-lookup"><span data-stu-id="45449-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="45449-133">Ange vilken finansieringskälla som ansvarar för avrundningsdifferenser som orsakas av beräkningar av finansieringstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="45449-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="45449-134">Ställ in regler som avgör hur projektkostnader faktureras till externa kunder och debiteras interna organisationer.</span><span class="sxs-lookup"><span data-stu-id="45449-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="45449-135">Registrera transaktioner på ett spärrat finansieringskonto tills ytterligare finansiering kan erhållas, eller tills du bestämmer dig för att bära kostnaderna internt.</span><span class="sxs-lookup"><span data-stu-id="45449-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="45449-136">För att avgöra vilken momsgrupp som ska kopplas till en transaktion, genomsöks projektet efter en tilldelning av skattegrupp.</span><span class="sxs-lookup"><span data-stu-id="45449-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="45449-137">Om ingen tilldelning av skattegrupp har gjorts på projektnivån genomsöks projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="45449-138">Exempel: flera finansieringskällor (enkel)</span><span class="sxs-lookup"><span data-stu-id="45449-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="45449-139">Följande tabell innehåller scenarier för hantering av en finansieringsfördelning mellan flera finansieringskällor.</span><span class="sxs-lookup"><span data-stu-id="45449-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="45449-140">De här scenarierna bygger på följande förutsättningar:</span><span class="sxs-lookup"><span data-stu-id="45449-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="45449-141">Prioritetsinställningarna gäller för tilldelning av medel innan andra kriterier för finansieringsregler tillämpas.</span><span class="sxs-lookup"><span data-stu-id="45449-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="45449-142">Inget datumintervall har angetts för att definiera perioden när finansieringsregeln är giltig.</span><span class="sxs-lookup"><span data-stu-id="45449-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45449-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="45449-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="45449-144"><strong>Finansieringskälla</strong></span><span class="sxs-lookup"><span data-stu-id="45449-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="45449-145"><strong>Allokeringsprocent</strong></span><span class="sxs-lookup"><span data-stu-id="45449-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="45449-146"><strong>Allokeringsprioritet</strong></span><span class="sxs-lookup"><span data-stu-id="45449-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45449-147">Du vill fördela kostnaderna till en finansieringskälla tills fonderna är uttömda kan du fördela kostnaderna till en andra finansieringskälla tills medlen är uttömt och slutligen fördela de återstående kostnaderna till en tredje finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-148">Finansieringskälla 1</span><span class="sxs-lookup"><span data-stu-id="45449-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="45449-149">Finansieringskälla 2</span><span class="sxs-lookup"><span data-stu-id="45449-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="45449-150">Finansieringskälla 3</span><span class="sxs-lookup"><span data-stu-id="45449-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-151">100%</span><span class="sxs-lookup"><span data-stu-id="45449-151">100%</span></span></li>
<li><span data-ttu-id="45449-152">100%</span><span class="sxs-lookup"><span data-stu-id="45449-152">100%</span></span></li>
<li><span data-ttu-id="45449-153">100%</span><span class="sxs-lookup"><span data-stu-id="45449-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-154">1</span><span class="sxs-lookup"><span data-stu-id="45449-154">1</span></span></li>
<li><span data-ttu-id="45449-155">2</span><span class="sxs-lookup"><span data-stu-id="45449-155">2</span></span></li>
<li><span data-ttu-id="45449-156">3</span><span class="sxs-lookup"><span data-stu-id="45449-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45449-157">Du vill tilldela 75 procent av kostnader till en finansieringskälla och 25 procent till en andra finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="45449-158">När någon av dessa finansieringskällor är uttömda vill du betala de återstående kostnaderna från en tredje finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-159">Finansieringskälla 1</span><span class="sxs-lookup"><span data-stu-id="45449-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="45449-160">Finansieringskälla 2</span><span class="sxs-lookup"><span data-stu-id="45449-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="45449-161">Finansieringskälla 3</span><span class="sxs-lookup"><span data-stu-id="45449-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-162">75 %</span><span class="sxs-lookup"><span data-stu-id="45449-162">75%</span></span></li>
<li><span data-ttu-id="45449-163">25 %</span><span class="sxs-lookup"><span data-stu-id="45449-163">25%</span></span></li>
<li><span data-ttu-id="45449-164">100%</span><span class="sxs-lookup"><span data-stu-id="45449-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-165">1</span><span class="sxs-lookup"><span data-stu-id="45449-165">1</span></span></li>
<li><span data-ttu-id="45449-166">1</span><span class="sxs-lookup"><span data-stu-id="45449-166">1</span></span></li>
<li><span data-ttu-id="45449-167">2</span><span class="sxs-lookup"><span data-stu-id="45449-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45449-168">Du vill tilldela 75 procent av kostnader till en finansieringskälla och 25 procent till en andra finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="45449-169">När någon av dessa finansieringskällor är uttömda vill du dela upp de återstående kostnaderna mellan en tredje finansieringskälla och en fjärde finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-170">Finansieringskälla 1</span><span class="sxs-lookup"><span data-stu-id="45449-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="45449-171">Finansieringskälla 2</span><span class="sxs-lookup"><span data-stu-id="45449-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="45449-172">Finansieringskälla 3</span><span class="sxs-lookup"><span data-stu-id="45449-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="45449-173">Finansieringskälla 4</span><span class="sxs-lookup"><span data-stu-id="45449-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-174">75 %</span><span class="sxs-lookup"><span data-stu-id="45449-174">75%</span></span></li>
<li><span data-ttu-id="45449-175">25 %</span><span class="sxs-lookup"><span data-stu-id="45449-175">25%</span></span></li>
<li><span data-ttu-id="45449-176">50 %</span><span class="sxs-lookup"><span data-stu-id="45449-176">50%</span></span></li>
<li><span data-ttu-id="45449-177">50 %</span><span class="sxs-lookup"><span data-stu-id="45449-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-178">1</span><span class="sxs-lookup"><span data-stu-id="45449-178">1</span></span></li>
<li><span data-ttu-id="45449-179">1</span><span class="sxs-lookup"><span data-stu-id="45449-179">1</span></span></li>
<li><span data-ttu-id="45449-180">2</span><span class="sxs-lookup"><span data-stu-id="45449-180">2</span></span></li>
<li><span data-ttu-id="45449-181">2</span><span class="sxs-lookup"><span data-stu-id="45449-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45449-182">Du vill tilldela de första 25 procent av kostnader till en finansieringskälla och resten till en andra finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-183">Finansieringskälla 1</span><span class="sxs-lookup"><span data-stu-id="45449-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="45449-184">Finansieringskälla 2</span><span class="sxs-lookup"><span data-stu-id="45449-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-185">25 %</span><span class="sxs-lookup"><span data-stu-id="45449-185">25%</span></span></li>
<li><span data-ttu-id="45449-186">100%</span><span class="sxs-lookup"><span data-stu-id="45449-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="45449-187">1</span><span class="sxs-lookup"><span data-stu-id="45449-187">1</span></span></li>
<li><span data-ttu-id="45449-188">2</span><span class="sxs-lookup"><span data-stu-id="45449-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="45449-189">Exempel: flera finansieringskällor (komplex)</span><span class="sxs-lookup"><span data-stu-id="45449-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="45449-190">Du har tre finansieringskällor som du vill använda i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="45449-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="45449-191">Använd finansieringskälla 2 och finansieringskällan 3 lika tills finansieringskällan 2 är uttömd.</span><span class="sxs-lookup"><span data-stu-id="45449-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="45449-192">Fortsätt använda finansieringskällan 3 tills den är uttömd.</span><span class="sxs-lookup"><span data-stu-id="45449-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="45449-193">Använd finansieringskällan 1 efter att finansieringskällan 3 har uttömts.</span><span class="sxs-lookup"><span data-stu-id="45449-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="45449-194">För att uppnå detta måste du göra följande:</span><span class="sxs-lookup"><span data-stu-id="45449-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="45449-195">Ställ in finansieringsgränser för finansieringskällan 2 och finansieringskällan 3 för respektive belopp.</span><span class="sxs-lookup"><span data-stu-id="45449-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="45449-196">Skapa följande finansieringsregler:</span><span class="sxs-lookup"><span data-stu-id="45449-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="45449-197">Regel 1 (prioritet 1): allokera 50 procent av transaktionerna till finansieringskällan 2 och 50 procent till finansieringskällan 3.</span><span class="sxs-lookup"><span data-stu-id="45449-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="45449-198">Regel 2 (prioritet 2): tilldela 100 procent av transaktionerna till finansieringskällan 3.</span><span class="sxs-lookup"><span data-stu-id="45449-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="45449-199">Regel 3 (prioritet 3): tilldela 100 procent av transaktionerna till finansieringskällan 1.</span><span class="sxs-lookup"><span data-stu-id="45449-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="45449-200">Installationen fungerar eftersom transaktionerna kontrolleras mot regler och begränsningar för att avgöra om någon av dem gäller för transaktionen.</span><span class="sxs-lookup"><span data-stu-id="45449-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="45449-201">Om inga specifika regler eller begränsningar gäller för transaktionen gäller regeln Alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="45449-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="45449-202">Regeln Alla transaktioner matchar alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="45449-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="45449-203">Om en regel hittas som matchar en transaktion tillämpas först den procent som har tilldelats i den regeln, men först efter att matchningarna har kontrollerats mot eventuella begränsningar som har ställts in.</span><span class="sxs-lookup"><span data-stu-id="45449-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="45449-204">Om en gräns har uppnåtts och en finansieringskällas medel är uttömda bortses från finansieringsregeln som är associerad med finansieringsgränsen och programmet kontrollerar om nästa regel som gäller.</span><span class="sxs-lookup"><span data-stu-id="45449-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="45449-205">I vissa fall kan endast en del av en transaktion fördelas under en regel.</span><span class="sxs-lookup"><span data-stu-id="45449-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="45449-206">Detta kan inträffa om en gräns uppnås när transaktionen har fördelats.</span><span class="sxs-lookup"><span data-stu-id="45449-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="45449-207">I det här fallet fördelas endast ett visst belopp enligt den regeln, till exempel 50 procent för varje finansieringskälla.</span><span class="sxs-lookup"><span data-stu-id="45449-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="45449-208">Detta är fallet i regel 1, som beskrivs ovan i det här avsnittet.</span><span class="sxs-lookup"><span data-stu-id="45449-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="45449-209">Återstoden fördelas enligt nästa regel i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="45449-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="45449-210">I följande tabell granskas detta scenario mer detaljerat.</span><span class="sxs-lookup"><span data-stu-id="45449-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45449-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="45449-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="45449-212"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="45449-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45449-213">Finansieringsregler</span><span class="sxs-lookup"><span data-stu-id="45449-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-214">Regel 1 (prioritet 1): alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="45449-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="45449-215">Fördela finansieringskällan 2 med 50 % och finansieringskällan 3 vid 50 %.</span><span class="sxs-lookup"><span data-stu-id="45449-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="45449-216">Regel 2 (prioritet 2): alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="45449-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="45449-217">Fördela finansieringskällan 3 med 100 %.</span><span class="sxs-lookup"><span data-stu-id="45449-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="45449-218">Regel 3 (prioritet 2): alla transaktioner.</span><span class="sxs-lookup"><span data-stu-id="45449-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="45449-219">Fördela finansieringskällan 1 med 100 %.</span><span class="sxs-lookup"><span data-stu-id="45449-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45449-220">Finansieringsgränser</span><span class="sxs-lookup"><span data-stu-id="45449-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-221">Finansieringskälla 1 gräns = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="45449-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="45449-222">Finansieringskälla 2 gräns = 500,00</span><span class="sxs-lookup"><span data-stu-id="45449-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="45449-223">Finansieringskälla 3 gräns = 750,00</span><span class="sxs-lookup"><span data-stu-id="45449-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45449-224">Transaktion 1</span><span class="sxs-lookup"><span data-stu-id="45449-224">Transaction 1</span></span></td>
<td><span data-ttu-id="45449-225"><strong>Transaktionsbelopp:</strong> 100,00<strong>Finansiering:</strong> Transaktionen betalas enligt regel 1 endast på grund av att transaktionen är helt betald efter att regel 1 har tillämpats.</span><span class="sxs-lookup"><span data-stu-id="45449-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="45449-226">Transaktionen finansieras lika mycket mellan finansieringskällan 2 och finansieringskällan 3.</span><span class="sxs-lookup"><span data-stu-id="45449-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="45449-227">Finansieringskälla 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="45449-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="45449-228">Finansieringskälla 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="45449-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45449-229">Transaktion 2</span><span class="sxs-lookup"><span data-stu-id="45449-229">Transaction 2</span></span></td>
<td><span data-ttu-id="45449-230"><strong>Transaktionsbelopp:</strong> 5 000,00<strong>Finansiering:</strong> Transaktionen betalas enligt alla tre regler.</span><span class="sxs-lookup"><span data-stu-id="45449-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="45449-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="45449-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="45449-232">Finansieringskälla 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="45449-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="45449-233">Finansieringskälla 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="45449-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="45449-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="45449-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="45449-235">Finansieringskälla 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="45449-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="45449-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="45449-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="45449-237">Finansieringskälla 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="45449-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45449-238">Totalt antal som fördelas för varje finansieringskälla</span><span class="sxs-lookup"><span data-stu-id="45449-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="45449-239">Finansieringskälla 1: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="45449-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="45449-240">Finansieringskälla 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="45449-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="45449-241">Finansieringskälla 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="45449-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="45449-242">Faktureringsregler</span><span class="sxs-lookup"><span data-stu-id="45449-242">Billing rules</span></span>
<span data-ttu-id="45449-243">När du förhandlar ett projektkontrakt med en kund anger du hur och när du kan fakturera kunden för arbete med ett projekt.</span><span class="sxs-lookup"><span data-stu-id="45449-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="45449-244">När du har ställt in projektkontraktet och projekten kan du ange faktureringsregler för projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="45449-245">Faktureringsregler bygger på de projekt villkor som har angetts i projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="45449-246">Vilka faktureringsregler du kan skapa beror på villkoren i projektkontraktet och projekttypen, till exempel tid och material eller fast pris, som du associerar med faktureringsregeln.</span><span class="sxs-lookup"><span data-stu-id="45449-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="45449-247">Du kan skapa mer än en faktureringsregel för ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="45449-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="45449-248">Du kan också tilldela en faktureringsregel till flera projekt som är associerade med samma projektkontrakt och som har liknande faktureringsvillkor.</span><span class="sxs-lookup"><span data-stu-id="45449-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="45449-249">Du kan ange följande typer av faktureringsregler:</span><span class="sxs-lookup"><span data-stu-id="45449-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="45449-250">**Leveransenhet** – fakturera en kund när du fyller i en leveransenhet.</span><span class="sxs-lookup"><span data-stu-id="45449-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="45449-251">Du anger leveransenheterna i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="45449-252">**Förlopp** – fakturera en kund när du slutför en angiven procentsats av projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="45449-253">Du kan ange att en procentandel av arbetet som har slutförts automatiskt ska beräknas med en faktureringsregel, eller så kan du beräkna kundens procentsats manuellt med beloppet.</span><span class="sxs-lookup"><span data-stu-id="45449-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="45449-254">**Milstolpe** – fakturera en kund med hela beloppet för en projekt milstolpe när milstolpen nås.</span><span class="sxs-lookup"><span data-stu-id="45449-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="45449-255">**Avgift** – fakturera en kund för dina tjänster plus en hanteringsavgift som vanligtvis är en procentandel av servicekostnaden.</span><span class="sxs-lookup"><span data-stu-id="45449-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="45449-256">**Tid och material** – fakturera en kund för värdet av tid och material som används i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="45449-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="45449-257">För alla typer av faktureringsregler kan du ange en kvarhållande procent som dras av från kundfakturor tills ett projekt når ett överenskommet stadium.</span><span class="sxs-lookup"><span data-stu-id="45449-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="45449-258">Procentsats för kvarhållandet anges i projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="45449-259">Beloppet beräknas utifrån och subtraheras det totala värdet på raderna i en kundfaktura.</span><span class="sxs-lookup"><span data-stu-id="45449-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="45449-260">För faktureringsregler för **Tid och material** och **Förlopp** kan du tilldela debiterbara kategorier.</span><span class="sxs-lookup"><span data-stu-id="45449-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="45449-261">Debiterbara kategorier visar de transaktioner som ska tas med på kundfakturor.</span><span class="sxs-lookup"><span data-stu-id="45449-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="45449-262">När du är klar att fakturera kunden beräknas beloppet för att fakturera för projektet utifrån faktureringsregler och ett projektfakturaförslag skapas.</span><span class="sxs-lookup"><span data-stu-id="45449-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="45449-263">I följande avsnitt finns exempel som visar hur du skapar och hanterar faktureringsregler för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="45449-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="45449-264">Exempel: skapa en faktureringsregel som baseras på antalet levererade enheter</span><span class="sxs-lookup"><span data-stu-id="45449-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="45449-265">Företaget går in i ett avtal för att tillhandahålla totalt fem utbildningar till en kunds anställda med en kostnad på 10 000 per utbildningssession.</span><span class="sxs-lookup"><span data-stu-id="45449-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="45449-266">Kunden faktureras efter varje utbildningssession.</span><span class="sxs-lookup"><span data-stu-id="45449-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="45449-267">När du anger faktureringsregler för kontraktet använder du följande värden:</span><span class="sxs-lookup"><span data-stu-id="45449-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="45449-268">Leveransenheten är en utbildningssession.</span><span class="sxs-lookup"><span data-stu-id="45449-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="45449-269">Enhetspriset är 10 000 per utbildningssession.</span><span class="sxs-lookup"><span data-stu-id="45449-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="45449-270">Det totala antalet enheter är fem utbildningssessioner.</span><span class="sxs-lookup"><span data-stu-id="45449-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="45449-271">När du har slutfört en utbildningssession kan du skapa en faktura för 10 000 för den första enheten som levererades och sedan skicka fakturan till kunden.</span><span class="sxs-lookup"><span data-stu-id="45449-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="45449-272">Exempel: skapa en faktureringsregel som bygger på en angiven procentsats av projektslutförande (manuell beräkning)</span><span class="sxs-lookup"><span data-stu-id="45449-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="45449-273">Din organisation, ett programvarukonsultföretag, går in i ett avtal med en kund för att utveckla en del av en produkt som kunden utvecklar.</span><span class="sxs-lookup"><span data-stu-id="45449-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="45449-274">Din organisation godkänner att programvarukoden levereras under en period om sex månader.</span><span class="sxs-lookup"><span data-stu-id="45449-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="45449-275">Kunden går med på att betala organisationen totalt 100 000 för arbetet.</span><span class="sxs-lookup"><span data-stu-id="45449-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="45449-276">Du skapar en faktureringsregel för att fakturera kunden utifrån den procentsats av arbete som har slutförts på projektet, enligt vad som anges i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="45449-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="45449-277">Vid slutet av den första månaden uppfyllde du kunden för att fastställa procentandelen av arbetet som slutförts.</span><span class="sxs-lookup"><span data-stu-id="45449-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="45449-278">När du och kunden har granskat projektet bestämmer du att projektet är 15 procent klart.</span><span class="sxs-lookup"><span data-stu-id="45449-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="45449-279">Du skapar en faktura för 15 000 (15 procent av 100 000) och skickar den till kunden.</span><span class="sxs-lookup"><span data-stu-id="45449-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="45449-280">Exempel: skapa en faktureringsregel som bygger på en angiven procentsats av projektslutförande (automatisk beräkning)</span><span class="sxs-lookup"><span data-stu-id="45449-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="45449-281">Din organisation, ett företag för programutveckling, kan komma att utveckla ett lönebokföringspaket för en kund i 30 000.</span><span class="sxs-lookup"><span data-stu-id="45449-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="45449-282">Kunden samtycker till att betala din organisation baserat på procentandelen av genomfört arbete.</span><span class="sxs-lookup"><span data-stu-id="45449-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="45449-283">Du uppskattar att projektkostnaderna är 20 000.</span><span class="sxs-lookup"><span data-stu-id="45449-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="45449-284">I projektkontraktet anges de arbetskategorier som du använder i faktureringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="45449-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="45449-285">Du ställer in faktureringsregler som automatiskt beräknar fakturabeloppen för den procentandel av arbetet som slutförts för varje kategori.</span><span class="sxs-lookup"><span data-stu-id="45449-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="45449-286">Du lägger upp en budget för varje kategori:</span><span class="sxs-lookup"><span data-stu-id="45449-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="45449-287">**Utveckling** – kostnad på 15 000 och intäkt på 20 000</span><span class="sxs-lookup"><span data-stu-id="45449-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="45449-288">**Installation** – kostnad på 5 000 och intäkt på 10 000</span><span class="sxs-lookup"><span data-stu-id="45449-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="45449-289">När du skapar en kundfaktura för första gången beräknas fakturabeloppet automatiskt utifrån följande information:</span><span class="sxs-lookup"><span data-stu-id="45449-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="45449-290">Efter en månad skickar arbetaren i projektet en tidrapport för projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="45449-291">Kostnaden för arbetarens timmar är 5 000 för utveckling och 1 000 för installation.</span><span class="sxs-lookup"><span data-stu-id="45449-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="45449-292">Utvecklingsarbetet är 33 procent färdigt (5 000 faktiska kostnader/15 000 budgeterad kostnad) och installationen är 20 procent färdig (1 000 faktisk kostnad/5 000 budgetkostnad).</span><span class="sxs-lookup"><span data-stu-id="45449-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="45449-293">Fakturabeloppet på 8 667 beräknas automatiskt (33 procent av 20 000 + 20 procent av 10 000).</span><span class="sxs-lookup"><span data-stu-id="45449-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="45449-294">Du skapar en faktura för 8 667 och skickar den till kunden.</span><span class="sxs-lookup"><span data-stu-id="45449-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="45449-295">Exempel: skapa en faktureringsregel som baseras på avtalade milstolpar</span><span class="sxs-lookup"><span data-stu-id="45449-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="45449-296">Din organisation, ett konsultföretag inom företagsledning, åtar sig att genomföra marknads undersökningar för en konsumentprodukt som kunden planerar att sälja.</span><span class="sxs-lookup"><span data-stu-id="45449-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="45449-297">Kunden accepterar att använda dina tjänster under en period på tre månader, med början i mars och går med på att betala din organisation 50 000.</span><span class="sxs-lookup"><span data-stu-id="45449-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="45449-298">Det finns tre milstolpar i projektet:</span><span class="sxs-lookup"><span data-stu-id="45449-298">The project has three milestones:</span></span>

-   <span data-ttu-id="45449-299">Milstolpe 1: samla in konsumentdata – 31 mars</span><span class="sxs-lookup"><span data-stu-id="45449-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="45449-300">Milstolpe 2: analysera konsumentdata – 30 april</span><span class="sxs-lookup"><span data-stu-id="45449-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="45449-301">Milstolpe 3: presentera ett förslag till produktlivsduglighet – 31 maj</span><span class="sxs-lookup"><span data-stu-id="45449-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="45449-302">Kunden går med på att betala din organisation 10 000 för den första milstolpen, 20 000 för den andra milstolpen och 20 000 för den tredje milstolpen.</span><span class="sxs-lookup"><span data-stu-id="45449-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="45449-303">När du skapar projektkontraktet godkänner du att fakturera kunden utifrån den milstolpe som har slutförts.</span><span class="sxs-lookup"><span data-stu-id="45449-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="45449-304">Inställningarna av faktureringsregler består av följande steg:</span><span class="sxs-lookup"><span data-stu-id="45449-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="45449-305">Definiera projektets milstolpar.</span><span class="sxs-lookup"><span data-stu-id="45449-305">Define the project milestones.</span></span>
-   <span data-ttu-id="45449-306">Definiera beloppet för att fakturera kunden när varje milstolpe är slutförd.</span><span class="sxs-lookup"><span data-stu-id="45449-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="45449-307">När den första milstolpen är avslutad den 31 mars markerar du den som slutförd och skapar sedan en faktura för 10 000 och skickar den till kunden.</span><span class="sxs-lookup"><span data-stu-id="45449-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="45449-308">Du kan inte skapa en faktura för en milstolpe förrän du har markerat milstolpen som slutförd.</span><span class="sxs-lookup"><span data-stu-id="45449-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="45449-309">Exempel: skapa en faktureringsregel som bygger på tjänster plus en hanteringsavgift</span><span class="sxs-lookup"><span data-stu-id="45449-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="45449-310">Din organisation, ett konsultföretag inom företagsledning, åtar sig att genomföra marknadsundersökningar för att utvärdera livskraften hos en produkt som kunden, ett detaljhandelsbolag, utvecklar.</span><span class="sxs-lookup"><span data-stu-id="45449-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="45449-311">Villkoren i avtalet anger att du ska tillhandahålla tjänster för de tre viktigaste ledningskonsulterna, som kommer att utföra forskningen på tid och material.</span><span class="sxs-lookup"><span data-stu-id="45449-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="45449-312">Kunden går med på att betala 100 per timme och en hanteringsavgift på 10 procent för de konsulttider som debiteras för projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="45449-313">När du skapar projektkontraktet skapar du en faktureringsregel som lägger till en hanteringsavgift på 10 procent för de konsulttimmar som debiteras projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="45449-314">När du skapar en faktura för kunden faktureras kunden en hanteringsavgift på 10 procent plus kostnaden för konsulttimmarna.</span><span class="sxs-lookup"><span data-stu-id="45449-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="45449-315">Om de tre konsulterna arbetade med 200 timmar totalt i projektet skapas en faktura på 22 000 på grundval av följande beräkning:</span><span class="sxs-lookup"><span data-stu-id="45449-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="45449-316">200 timmar för 100 per timme = 20 000</span><span class="sxs-lookup"><span data-stu-id="45449-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="45449-317">10 procents hanteringsavgift = 2 000</span><span class="sxs-lookup"><span data-stu-id="45449-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="45449-318">Totalt fakturabelopp = 22 000</span><span class="sxs-lookup"><span data-stu-id="45449-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="45449-319">Om avgifter är momspliktiga till en kund och du väljer en momsgrupp i projektkontraktet, registreras momsgruppen automatiskt i faktureringsregeln för avgifter.</span><span class="sxs-lookup"><span data-stu-id="45449-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="45449-320">Exempel: skapa en faktureringsregel för värdet av tid och material</span><span class="sxs-lookup"><span data-stu-id="45449-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="45449-321">Din organisation, ett programvarukonsultföretag, godkänner att de tillhandahåller fem tekniska konsulter för att arbeta med ett programutvecklingsprojekt för en kund under de kommande sex månaderna.</span><span class="sxs-lookup"><span data-stu-id="45449-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="45449-322">Kunden accepterar att betala 150 för varje konsulttimme plus kostnaden för kontorsmateriel.</span><span class="sxs-lookup"><span data-stu-id="45449-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="45449-323">Din organisation skickar en faktura till kunden i slutet av varje månad.</span><span class="sxs-lookup"><span data-stu-id="45449-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="45449-324">När du skapar projektkontraktet godkänner du att fakturera kunden varje månad för tid och material i projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="45449-325">Du skapar en faktureringsregel som innehåller följande information:</span><span class="sxs-lookup"><span data-stu-id="45449-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="45449-326">Kontraktperioden är sex månader.</span><span class="sxs-lookup"><span data-stu-id="45449-326">The contract period is six months.</span></span>
-   <span data-ttu-id="45449-327">Konsultens tid beräknas till 150 per timme.</span><span class="sxs-lookup"><span data-stu-id="45449-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="45449-328">Kontorsmateriel faktureras till kostnaden och den totala kostnaden för projektet får inte överstiga 10 000.</span><span class="sxs-lookup"><span data-stu-id="45449-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="45449-329">Du skapar en kundfaktura i slutet av varje kalendermånad under projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="45449-330">Under den första månaden registreras sammanlagt 800 timmar av konsulterna i projektet.</span><span class="sxs-lookup"><span data-stu-id="45449-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="45449-331">Kostnaden för kontorsmateriel som debiteras för projektet är 2 000.</span><span class="sxs-lookup"><span data-stu-id="45449-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="45449-332">I slutet av månaden skapar du därför en faktura på 122 000 som beräknas som 800 timmar vid 150 per timme, plus 2 000 för kontorsmateriel.</span><span class="sxs-lookup"><span data-stu-id="45449-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



