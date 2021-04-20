---
title: Projektbaserade kontraktrader – Översikt
description: I det här ämnet finns information om att arbeta med projektbaserade kontraktrader.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858180"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="a5c9f-103">Projektbaserade kontraktrader – Översikt</span><span class="sxs-lookup"><span data-stu-id="a5c9f-103">Project-based contract lines overview</span></span>

<span data-ttu-id="a5c9f-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="a5c9f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5c9f-105">Projektbaserade kontraktrader i Dynamics 365 Project Operations är utformade för att rymma uppskattningar och faktureringsavtal för specifika komponenter i projektarbetet med ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="a5c9f-106">Strukturen på en projektbaserad kontraktrad utökas för projektuppskattningar och faktureringsscenarier med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="a5c9f-107">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="a5c9f-107">Billing method</span></span>
- <span data-ttu-id="a5c9f-108">Mappning av projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="a5c9f-108">Project and task mapping</span></span>
- <span data-ttu-id="a5c9f-109">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="a5c9f-109">Included transaction classes</span></span>
- <span data-ttu-id="a5c9f-110">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="a5c9f-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="a5c9f-111">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="a5c9f-111">Chargeability setup</span></span>
- <span data-ttu-id="a5c9f-112">Uppskattningar med hjälp av kontraktradsdetaljer</span><span class="sxs-lookup"><span data-stu-id="a5c9f-112">Estimates using contract line details</span></span>
- <span data-ttu-id="a5c9f-113">Kontraktradens kund</span><span class="sxs-lookup"><span data-stu-id="a5c9f-113">Contract line customers</span></span>

<span data-ttu-id="a5c9f-114">Följande tabell innehåller fälten på fliken **Allmänt** i projektbaserade kontraktrader som hjälper dig att ställa in grunden för en detaljerad uppskattning och faktureringsordning för projektbaserade arbeten.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="a5c9f-115">Fält</span><span class="sxs-lookup"><span data-stu-id="a5c9f-115">Field</span></span> | <span data-ttu-id="a5c9f-116">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a5c9f-116">Description</span></span> | <span data-ttu-id="a5c9f-117">Inverkan nedströms</span><span class="sxs-lookup"><span data-stu-id="a5c9f-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a5c9f-118">**Namn**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-118">**Name**</span></span> | <span data-ttu-id="a5c9f-119">Namn på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-119">Name of the contract line.</span></span> <span data-ttu-id="a5c9f-120">Detta identifierar den diskreta komponenten för det kontrakt som uppskattas.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="a5c9f-121">För ett projektkontrakt som har skapats utifrån en offert kopieras värdet från ett motsvarande värde på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="a5c9f-122">Namnet kopieras till projektfakturaraden som skapas från den här kontraktraden när fakturan skapas.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="a5c9f-123">**Faktureringsmetod**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-123">**Billing Method**</span></span> | <span data-ttu-id="a5c9f-124">I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="a5c9f-125">Det här är ett alternativuppsättning som representerar de två huvudsakliga upphandlingsmodellerna som stöds av Project Operations:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="a5c9f-126">- **Fast pris**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-126">- **Fixed Price**</span></span></br><span data-ttu-id="a5c9f-127">- **Tid och material**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-127">- **Time and Material**</span></span> | <span data-ttu-id="a5c9f-128">Den faktiska transaktionen bearbetas i enlighet med faktureringsmetoden för den refererade kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="a5c9f-129">Om den kontraktrad som har refererats av det faktiska värdet har en metod och en metod för materialfakturering skapas en kostnad och en faktisk fakturerad försäljningspost.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="a5c9f-130">Om kontraktraden som refereras av det faktiska värdet har en faktureringsmetod med fast pris skapas endast en verklig kostnad.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="a5c9f-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-131">**Project**</span></span> | <span data-ttu-id="a5c9f-132">Använd det här fältet om du vill identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="a5c9f-133">Detta värde kommer att användas tillsammans med **Uppgifter som ingår** och **Inkluderade transaktionsklasser** för att lösa kontraktsreferensen på en faktisk eller uppskattad radpost.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="a5c9f-134">**Uppgifter som ingår**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-134">**Included Tasks**</span></span> | <span data-ttu-id="a5c9f-135">Anger om den här kontraktraden omfattar alla projektuppgifter för det valda projektet eller endast en del av uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="a5c9f-136">Detta är en alternativuppsättning som har följande möjliga värden:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="a5c9f-137">- **Alla projektuppgifter**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-137">- **All Project Tasks**</span></span></br><span data-ttu-id="a5c9f-138">- **Endast valda projektuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="a5c9f-139">Ett tomt värde i det här fältet är lika med att markera **alla projektuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="a5c9f-140">Om **endast valda uppgifter** är markerade kan du välja specifika uppgifter och associera dem till den här kontraktraden på fliken **Faktureringsinställningar för uppgift** på sidan **projekt**.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="a5c9f-141">Detta värde används tillsammans med **projekt** och **inkluderade transaktionsklasser** för att lösa kontraktradreferensen på en post för en faktisk post eller en post för beräkningsrader.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a5c9f-142">**Inkludera tid**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-142">**Include Time**</span></span> | <span data-ttu-id="a5c9f-143">Ett värde **Ja**/**Nej** anger om tidstransaktioner eller arbetskostnader för det valda projektet kommer att tas med på denna kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a5c9f-144">Ett **Nej**-värde anger att tidstransaktionerna och arbetskraftskostnaderna inte ska tas med på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="a5c9f-145">Ett **Ja**-värde anger att de ska vara.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="a5c9f-146">Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a5c9f-147">**Ta med utgift**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-147">**Include Expense**</span></span> | <span data-ttu-id="a5c9f-148">Ett värde **Ja**/**Nej** anger om utgiftskostnader för det valda projektet kommer att tas med på denna kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a5c9f-149">Ett **Nej**-värde anger att utgiftskostnaden inte ska tas med på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="a5c9f-150">Ett **Ja**-värde anger att det ska vara.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="a5c9f-151">Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a5c9f-152">**Ta med material**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-152">**Include Materials**</span></span> | <span data-ttu-id="a5c9f-153">Ett värde **Ja**/**Nej** anger om materialkostnader för det valda projektet kommer att tas med på denna kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a5c9f-154">Ett värde för **Nej** indikerar att materialkostnaderna inte kommer att inkluderas i på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="a5c9f-155">Ett **Ja**-värde anger att det ska vara.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="a5c9f-156">Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a5c9f-157">**Inkludera avgift**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-157">**Include Fee**</span></span> | <span data-ttu-id="a5c9f-158">Ett värde **Ja**/**Nej** anger om avgifter för det valda projektet kommer att tas med på denna kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="a5c9f-159">Ett **Nej**-värde anger att avgifter inte ska tas med på den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="a5c9f-160">Ett **Ja**-värde anger att de ska vara.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="a5c9f-161">Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="a5c9f-162">**Avtalat belopp**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-162">**Contracted Amount**</span></span> | <span data-ttu-id="a5c9f-163">På en kontraktrad med fast pris är detta belopp det överenskommet värde som ska faktureras kunden för alla arbetskomponenter som är associerade till den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="a5c9f-164">På en kontraktrad för tid och material är detta belopp ett beräknat värde av det som ska faktureras kunden för alla arbetskomponenter som är associerade till den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="a5c9f-165">I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="a5c9f-166">När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån beloppet på kontraktraddetaljer.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="a5c9f-167">När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra beloppen i radinformationen.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="a5c9f-168">På en kontraktrad med fast pris används det här värdet för att generera beloppet före skatt på periodiska faktureringsmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="a5c9f-169">**Beräknad skatt**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-169">**Estimated Tax**</span></span> | <span data-ttu-id="a5c9f-170">Användaren kan redigera fältet och ange det uppskattade momsbeloppet på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="a5c9f-171">När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet på kontraktraddetaljer.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="a5c9f-172">När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra momsbeloppen i radinformationen.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="a5c9f-173">På en kontraktrad med fast pris används det här värdet för att generera skatt på periodiska faktureringsmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="a5c9f-174">**Kontrakterat belopp efter skatt**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="a5c9f-175">Beloppet på kontraktraden efter skatt.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-175">The contract line amount after tax.</span></span> <span data-ttu-id="a5c9f-176">Fältet är skrivskyddat och beräknas som **kontrakterat belopp + moms**.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="a5c9f-177">På en kontraktrad med fast pris används det här värdet för att generera periodiska faktureringsmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="a5c9f-178">**Undre gräns**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="a5c9f-179">Användaren kan redigera det här fältet och det är endast tillgängligt på projektbaserade kontraktrader som har en metod för fakturering av tid och material.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="a5c9f-180">Användaren kan redigera det här fältet.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-180">The user can edit this field.</span></span> <span data-ttu-id="a5c9f-181">När ett faktiskt värde för tid och material refererar den här kontraktraden för tid och material, utvärderas det faktiska beloppet mot gränsen för undre gräns för den här kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="a5c9f-182">Utvärderingen slutförs efter att redan förbrukade och bekräftade belopp redovisas.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="a5c9f-183">**Kundbudget**</span><span class="sxs-lookup"><span data-stu-id="a5c9f-183">**Customer Budget**</span></span> | <span data-ttu-id="a5c9f-184">Det här fältet kan redigeras och kopieras från motsvarande fält på offertraden om kontraktet skapades från en offert.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="a5c9f-185">Det här fältet används endast för information och har inte någon efterföljande betydelse.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="a5c9f-186">Valideringsregler för alternativen på fliken Allmänt i projektbaserade kontraktrader</span><span class="sxs-lookup"><span data-stu-id="a5c9f-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="a5c9f-187">Regel 1: Om **inkluderade uppgifter** är tomt eller har värdet **alla projekt aktiviteter**, tas alla projekt aktiviteter med på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="a5c9f-188">Regel 2: När fältet **inkluderade uppgifter** är tomt eller uttryckligen anges som **alla projekt aktiviteter**, kan ett projekt och en viss transaktionsklass endast tas med på en projektbaserad kontraktrad för ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="a5c9f-189">Regel 3: När fältet **inkluderade uppgifter** anges till **Endast valda projektuppgifter** kan ett projekt och en viss transaktionsklass inkluderas på flera projektbaserade kontraktsrader i ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="a5c9f-190">
                    <strong>Kontrakt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5c9f-191">
                    <strong>Kontraktrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a5c9f-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="a5c9f-193">
                    <strong>Inkluderade uppgifter</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a5c9f-194">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a5c9f-195">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a5c9f-196">
                    <strong>Ta med material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a5c9f-197">
                    <strong>Ta med</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="a5c9f-198">
                    <strong>Avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="a5c9f-199">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="a5c9f-200">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5c9f-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-201">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-202">CL1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-203">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-204">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-205">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-206">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-207">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-208">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-209">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="a5c9f-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-210">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-210">Violation of Rule #2.</span></span> <span data-ttu-id="a5c9f-211">Tid, utgifter, material och avgifter på P1-projekt tas med på båda kontraktraderna, CL1 och CL2.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-212">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-213">CL2</span><span class="sxs-lookup"><span data-stu-id="a5c9f-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-214">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-215">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-216">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-217">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-218">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-219">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-220">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-221">CL1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-222">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-223">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-224">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-225">Inga</span><span class="sxs-lookup"><span data-stu-id="a5c9f-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-226">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-227">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-228">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="a5c9f-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-229">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-229">Violation of Rule #2.</span></span> <span data-ttu-id="a5c9f-230">Tid, material och avgifter på P1-projekt tas med på båda kontraktraderna, CL1 och CL2.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-231">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-232">CL2</span><span class="sxs-lookup"><span data-stu-id="a5c9f-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-233">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-234">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-235">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-236">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-237">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-238">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-239">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-240">CL1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-241">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-242">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-243">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-244">Inga</span><span class="sxs-lookup"><span data-stu-id="a5c9f-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-245">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-246">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-247">Giltig</span><span class="sxs-lookup"><span data-stu-id="a5c9f-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-248">Tid, material och avgifter på P1-projekt tas med i CL1.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="a5c9f-249">Utgiften på P1-projektet ingår i CL2.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="a5c9f-250">Ingen överlappar vad som ingår på varje kontraktrad och därför är giltigt.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-251">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-252">CL2</span><span class="sxs-lookup"><span data-stu-id="a5c9f-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-253">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-254">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-255">Inga</span><span class="sxs-lookup"><span data-stu-id="a5c9f-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-256">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-257">Inga</span><span class="sxs-lookup"><span data-stu-id="a5c9f-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-258">Inga</span><span class="sxs-lookup"><span data-stu-id="a5c9f-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-259">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-260">CL1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-261">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-262">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="a5c9f-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-263">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-264">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-265">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-266">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-267">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="a5c9f-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-268">Överträdelse av regel #2</span><span class="sxs-lookup"><span data-stu-id="a5c9f-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="a5c9f-269">C1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a5c9f-270">CL2 omfattar tid, material, utgifter och avgifter för hela projektet P1 och därmed överlappar vad som ingår i C1.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-271">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-272">CL2</span><span class="sxs-lookup"><span data-stu-id="a5c9f-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-273">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-274">Tom</span><span class="sxs-lookup"><span data-stu-id="a5c9f-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-275">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-276">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-277">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-278">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-279">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-280">CL1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-281">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-282">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="a5c9f-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-283">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-284">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-285">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-286">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-287">Giltig</span><span class="sxs-lookup"><span data-stu-id="a5c9f-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a5c9f-288">Per regel #3</span><span class="sxs-lookup"><span data-stu-id="a5c9f-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="a5c9f-289">C1 inkluderar tid, utgifter, material och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a5c9f-290">CL2 inkluderar tid, utgifter, material och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a5c9f-291">Den enda ytterligare valideringen är runt deluppsättningen av uppgifter på CL1, som skiljer sig från uppgiftsuppsättningen på CL2 för att säkerställa att ingen överlappar.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="a5c9f-292">Detta görs av systemet när uppgifter associeras.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a5c9f-293">C1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5c9f-294">CL2</span><span class="sxs-lookup"><span data-stu-id="a5c9f-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-295">P1</span><span class="sxs-lookup"><span data-stu-id="a5c9f-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="a5c9f-296">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="a5c9f-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-297">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a5c9f-298">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-299">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a5c9f-300">Ja</span><span class="sxs-lookup"><span data-stu-id="a5c9f-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
