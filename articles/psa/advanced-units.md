---
title: Enhetsgrupper och enheter
description: I det här ämnet finns information om enhetsgrupper och enheter.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145605"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="72787-103">Enhetsgrupper och enheter</span><span class="sxs-lookup"><span data-stu-id="72787-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="72787-104">Enhetsgrupper och enheter är grundläggande entiteter i Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="72787-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="72787-105">En enhet är en enskild enhet och flera enheter kan grupperas i enhetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="72787-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="72787-106">En enhetsgrupp kallas ibland för enhetsschema i användargränssnittet i Dynamics 365 (UI).</span><span class="sxs-lookup"><span data-stu-id="72787-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="72787-107">Här är några exempel på enheter och enhetsgrupper:</span><span class="sxs-lookup"><span data-stu-id="72787-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="72787-108">**Enhetsgrupp**: avstånd</span><span class="sxs-lookup"><span data-stu-id="72787-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="72787-109">**Enheter**: mil, kilometer och så vidare.</span><span class="sxs-lookup"><span data-stu-id="72787-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="72787-110">**Enhetsgrupp**: Tid</span><span class="sxs-lookup"><span data-stu-id="72787-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="72787-111">**Enheter**: timme, dag, vecka och så vidare.</span><span class="sxs-lookup"><span data-stu-id="72787-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="72787-112">När du skapar flera enheter i en enhetsgrupp måste du också skapa en konverteringsfaktor mellan dem genom att ange den första enheten som du anger som standardenhet eller primär enhet för enhetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="72787-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="72787-113">Till exempel i enhetsgruppen **Tid** om du ställer in **timme** som den första enheten kommer system ange **timme** som standardenhet.</span><span class="sxs-lookup"><span data-stu-id="72787-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="72787-114">Om nästa enhet som du konfigurerar är **dag** måste du ange en konverteringsfaktor för **dag** till **timme**.</span><span class="sxs-lookup"><span data-stu-id="72787-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="72787-115">Om du sedan lägger till **vecka** som en tredje enhet måste du ange en konverteringsfaktor för **vecka** utifrån **dag** eller **timme**.</span><span class="sxs-lookup"><span data-stu-id="72787-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="72787-116">I följande bild visas en exempelinställning för enheten **Dag** där fältet **kvantitet** visar antalet timmar som befinner sig på en dag och **vecka** där fältet **antal** visar antalet dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="72787-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Enhetsgrupp: informationssida](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="72787-118">Använda enheter och enhetsgrupper</span><span class="sxs-lookup"><span data-stu-id="72787-118">Using units and unit groups</span></span>

<span data-ttu-id="72787-119">Dynamics 365 Project Service Automation använder enheter och enhetsgrupper för att bearbeta beräkningar och transaktioner för både utgifter och tid.</span><span class="sxs-lookup"><span data-stu-id="72787-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="72787-120">För utgifter har varje utgiftskategori en standardenhetsgrupp och enhet.</span><span class="sxs-lookup"><span data-stu-id="72787-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="72787-121">Dessa värden anges som standardvärden för prislistetransaktioner för utgiftskategorier.</span><span class="sxs-lookup"><span data-stu-id="72787-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="72787-122">Du har till exempel en utgiftskategori som heter **Körsträcka**.</span><span class="sxs-lookup"><span data-stu-id="72787-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="72787-123">Den har en enhetsgrupp med namnet **avstånd** och en standardenhet med namnet **mil**.</span><span class="sxs-lookup"><span data-stu-id="72787-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="72787-124">Om du anger enhetsgruppen **avstånd** så att den har två enheter (**Mil** och **Kilometer**) kan du ange två priser för kategorin **körsträcka** på en prislista: pris per mil och pris per kilometer.</span><span class="sxs-lookup"><span data-stu-id="72787-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="72787-125">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="72787-125">Expense category</span></span>  | <span data-ttu-id="72787-126">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="72787-126">Unit group</span></span>  | <span data-ttu-id="72787-127">Enhet</span><span class="sxs-lookup"><span data-stu-id="72787-127">Unit</span></span>      | <span data-ttu-id="72787-128">Prismodell</span><span class="sxs-lookup"><span data-stu-id="72787-128">Pricing method</span></span>  | <span data-ttu-id="72787-129">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="72787-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="72787-130">Körsträcka</span><span class="sxs-lookup"><span data-stu-id="72787-130">Mileage</span></span>           | <span data-ttu-id="72787-131">Avstånd</span><span class="sxs-lookup"><span data-stu-id="72787-131">Distance</span></span>      | <span data-ttu-id="72787-132">Mil</span><span class="sxs-lookup"><span data-stu-id="72787-132">Mile</span></span>      | <span data-ttu-id="72787-133">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="72787-133">Price per unit</span></span>    | <span data-ttu-id="72787-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="72787-134">10 USD</span></span>            |
| <span data-ttu-id="72787-135">Körsträcka</span><span class="sxs-lookup"><span data-stu-id="72787-135">Mileage</span></span>           | <span data-ttu-id="72787-136">Avstånd</span><span class="sxs-lookup"><span data-stu-id="72787-136">Distance</span></span>      | <span data-ttu-id="72787-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="72787-137">Kilometer</span></span> | <span data-ttu-id="72787-138">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="72787-138">Price per unit</span></span>    |  <span data-ttu-id="72787-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="72787-139">6 USD</span></span>            |

<span data-ttu-id="72787-140">När du anger en utgift i ett projekt avgör systemet priset via kombinationen av kategorin och enheten i kostnaden.</span><span class="sxs-lookup"><span data-stu-id="72787-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="72787-141">Beskrivning av utgift</span><span class="sxs-lookup"><span data-stu-id="72787-141">Expense description</span></span>        | <span data-ttu-id="72787-142">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="72787-142">Expense category</span></span>  | <span data-ttu-id="72787-143">Enhet</span><span class="sxs-lookup"><span data-stu-id="72787-143">Unit</span></span>  | <span data-ttu-id="72787-144">Kvantitet</span><span class="sxs-lookup"><span data-stu-id="72787-144">Quantity</span></span>  | <span data-ttu-id="72787-145">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="72787-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="72787-146">Köra till kundens plats</span><span class="sxs-lookup"><span data-stu-id="72787-146">Drive to client location</span></span> | <span data-ttu-id="72787-147">Körsträcka</span><span class="sxs-lookup"><span data-stu-id="72787-147">Mileage</span></span>             | <span data-ttu-id="72787-148">Mil</span><span class="sxs-lookup"><span data-stu-id="72787-148">Mile</span></span>  | <span data-ttu-id="72787-149">10</span><span class="sxs-lookup"><span data-stu-id="72787-149">10</span></span>        | <span data-ttu-id="72787-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="72787-150">10 USD</span></span>         |

<span data-ttu-id="72787-151">För tid har varje prislistehuvud ett fält för **standardtidenhet**.</span><span class="sxs-lookup"><span data-stu-id="72787-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="72787-152">Värdet anges när du skapar ett prislistehuvud.</span><span class="sxs-lookup"><span data-stu-id="72787-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="72787-153">Enheten används sedan för att ange alla rollbaserade priser på den prislistan.</span><span class="sxs-lookup"><span data-stu-id="72787-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="72787-154">Beräkningsrader för fältet **tid på offert** kan uttryckas i valfri tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="72787-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="72787-155">Beräkningsrader i projekt och tidstransaktioner för projekt kan emellertid endast använda tidsenheten **timme**.</span><span class="sxs-lookup"><span data-stu-id="72787-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="72787-156">Om enheten på tidsposten eller uppskattningsraden inte överensstämmer med enheten på prislisteraden för den rollen, konverteras priset till de enheter som är definierade i projektberäkningen eller den faktiska transaktionen i projektet.</span><span class="sxs-lookup"><span data-stu-id="72787-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="72787-157">Följande exempel visar hur PSA använder enhetsgrupperna, enheterna och konverteringsfaktorerna.</span><span class="sxs-lookup"><span data-stu-id="72787-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="72787-158">Enheter</span><span class="sxs-lookup"><span data-stu-id="72787-158">Units</span></span>

   - <span data-ttu-id="72787-159">**Enhetsgrupp**: Tid</span><span class="sxs-lookup"><span data-stu-id="72787-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="72787-160">**Enheter**: timme</span><span class="sxs-lookup"><span data-stu-id="72787-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="72787-161">**Dag** - konverteringsfaktor: 8 timmar</span><span class="sxs-lookup"><span data-stu-id="72787-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="72787-162">**Vecka** - konverteringsfaktor: 40 timmar</span><span class="sxs-lookup"><span data-stu-id="72787-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="72787-163">Inställning av prislista för projekt A:</span><span class="sxs-lookup"><span data-stu-id="72787-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="72787-164">**Namn**: UK förs. pris 2016</span><span class="sxs-lookup"><span data-stu-id="72787-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="72787-165">**Standardtidsenhet**: dag</span><span class="sxs-lookup"><span data-stu-id="72787-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="72787-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="72787-166">**Currency**: GBP</span></span>

| <span data-ttu-id="72787-167">Roll</span><span class="sxs-lookup"><span data-stu-id="72787-167">Role</span></span>      | <span data-ttu-id="72787-168">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="72787-168">Unit group</span></span> | <span data-ttu-id="72787-169">Enhet</span><span class="sxs-lookup"><span data-stu-id="72787-169">Unit</span></span> | <span data-ttu-id="72787-170">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="72787-170">Organizational unit</span></span> | <span data-ttu-id="72787-171">Pris</span><span class="sxs-lookup"><span data-stu-id="72787-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="72787-172">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="72787-172">Developer</span></span> | <span data-ttu-id="72787-173">Time</span><span class="sxs-lookup"><span data-stu-id="72787-173">Time</span></span>       | <span data-ttu-id="72787-174">Day</span><span class="sxs-lookup"><span data-stu-id="72787-174">Day</span></span>  | <span data-ttu-id="72787-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="72787-175">Contoso UK</span></span>          | <span data-ttu-id="72787-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="72787-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="72787-177">Tidspost</span><span class="sxs-lookup"><span data-stu-id="72787-177">Time entry</span></span>

<span data-ttu-id="72787-178">I följande tabell visas den resulterande försäljningstransaktionen som skapats av PSA för ett tre timmars projekt.</span><span class="sxs-lookup"><span data-stu-id="72787-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="72787-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="72787-179">Project</span></span>   | <span data-ttu-id="72787-180">Uppgift</span><span class="sxs-lookup"><span data-stu-id="72787-180">Task</span></span>    | <span data-ttu-id="72787-181">Roll</span><span class="sxs-lookup"><span data-stu-id="72787-181">Role</span></span>      | <span data-ttu-id="72787-182">Kvantitet</span><span class="sxs-lookup"><span data-stu-id="72787-182">Quantity</span></span> | <span data-ttu-id="72787-183">Enhet</span><span class="sxs-lookup"><span data-stu-id="72787-183">Unit</span></span>  | <span data-ttu-id="72787-184">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="72787-184">Unit price</span></span> | <span data-ttu-id="72787-185">Ofakturerat försäljningsbelopp</span><span class="sxs-lookup"><span data-stu-id="72787-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="72787-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="72787-186">Project A</span></span> | <span data-ttu-id="72787-187">Design</span><span class="sxs-lookup"><span data-stu-id="72787-187">Design</span></span>  | <span data-ttu-id="72787-188">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="72787-188">Developer</span></span> | <span data-ttu-id="72787-189">3</span><span class="sxs-lookup"><span data-stu-id="72787-189">3</span></span>        | <span data-ttu-id="72787-190">Hour</span><span class="sxs-lookup"><span data-stu-id="72787-190">Hour</span></span>  | <span data-ttu-id="72787-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="72787-191">100 GBP</span></span>    | <span data-ttu-id="72787-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="72787-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="72787-193">Vanliga frågor om tidsenhet</span><span class="sxs-lookup"><span data-stu-id="72787-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="72787-194">Konverterar PSA till olika enheter vad gäller utgifter?</span><span class="sxs-lookup"><span data-stu-id="72787-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="72787-195">Nr</span><span class="sxs-lookup"><span data-stu-id="72787-195">No.</span></span> <span data-ttu-id="72787-196">Enhetskonvertering fungerar endast för tid.</span><span class="sxs-lookup"><span data-stu-id="72787-196">Unit conversion works only for time.</span></span> <span data-ttu-id="72787-197">För utgifter, om systemet inte kan hitta ett pris för kombinationen av utgiftskategorin och enheten är priset som standard inställt på 0,00.</span><span class="sxs-lookup"><span data-stu-id="72787-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="72787-198">Varför konverterar PSA tidsenheter?</span><span class="sxs-lookup"><span data-stu-id="72787-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="72787-199">I vissa länder eller regioner finns det ett juridiskt krav som faktureringsavgifterna ställs in i dagar.</span><span class="sxs-lookup"><span data-stu-id="72787-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="72787-200">Prisförhandling och rabattering under offertcykeln görs med hjälp av dagsräntor för varje fakturerbar roll.</span><span class="sxs-lookup"><span data-stu-id="72787-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="72787-201">Schemaberäkning och tidsregistrering sker i timmar.</span><span class="sxs-lookup"><span data-stu-id="72787-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="72787-202">För att kunna stödja denna skillnad i tidsenheter kan PSA konvertera tidsenheter.</span><span class="sxs-lookup"><span data-stu-id="72787-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="72787-203">Kan tidsenheter ändras i projektberäkningar?</span><span class="sxs-lookup"><span data-stu-id="72787-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="72787-204">Nr</span><span class="sxs-lookup"><span data-stu-id="72787-204">No.</span></span> <span data-ttu-id="72787-205">Schemaberäkningen är för närvarande begränsad till timmar och kan inte ändras.</span><span class="sxs-lookup"><span data-stu-id="72787-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="72787-206">Kan enheter och enhetsgrupper redigeras, tas bort och läggas till?</span><span class="sxs-lookup"><span data-stu-id="72787-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="72787-207">Ja.</span><span class="sxs-lookup"><span data-stu-id="72787-207">Yes.</span></span> <span data-ttu-id="72787-208">Med undantag för enhetsgruppen **Tid** och enheten **timme** kan alla enheter tas bort och du kan lägga till nya enheter.</span><span class="sxs-lookup"><span data-stu-id="72787-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="72787-209">I PSA kan enhetsgruppen **Tid** och enheten **Timme** inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="72787-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="72787-210">De kan emellertid uppdateras med översatt text för fältet **namn**.</span><span class="sxs-lookup"><span data-stu-id="72787-210">However, they can be updated with a translated text for the **Name** field.</span></span>
