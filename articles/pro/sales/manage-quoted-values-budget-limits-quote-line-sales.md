---
title: Projektbaserade offertrader - lite
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181114"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="1fdf4-104">Projektbaserade offertrader - lite</span><span class="sxs-lookup"><span data-stu-id="1fdf4-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="1fdf4-105">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="1fdf4-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1fdf4-106">Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="1fdf4-107">Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="1fdf4-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="1fdf4-108">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="1fdf4-108">Billing Method</span></span>
- <span data-ttu-id="1fdf4-109">Mappning av projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="1fdf4-109">Project and Task Mapping</span></span>
- <span data-ttu-id="1fdf4-110">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="1fdf4-110">Included Transaction classes</span></span>
- <span data-ttu-id="1fdf4-111">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="1fdf4-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="1fdf4-112">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="1fdf4-112">Chargeability setup</span></span>
- <span data-ttu-id="1fdf4-113">Uppskattning med hjälp av offertradsinformation</span><span class="sxs-lookup"><span data-stu-id="1fdf4-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="1fdf4-114">Offertradskunder</span><span class="sxs-lookup"><span data-stu-id="1fdf4-114">Quote line Customers</span></span>

<span data-ttu-id="1fdf4-115">Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="1fdf4-116">Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="1fdf4-117">**Fält**</span><span class="sxs-lookup"><span data-stu-id="1fdf4-117">**Field**</span></span> | <span data-ttu-id="1fdf4-118">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="1fdf4-118">**Description**</span></span> | <span data-ttu-id="1fdf4-119">**Inverkan nedströms**</span><span class="sxs-lookup"><span data-stu-id="1fdf4-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1fdf4-120">Namn</span><span class="sxs-lookup"><span data-stu-id="1fdf4-120">Name</span></span> | <span data-ttu-id="1fdf4-121">Namnet på en offertrad som kan hjälpa dig att identifiera den diskreta komponenten i offerten som uppskattas.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="1fdf4-122">Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-123">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="1fdf4-123">Billing Method</span></span> | <span data-ttu-id="1fdf4-124">I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="1fdf4-125">Det här fältet innehåller de två huvudmodellerna för kontrakt som stöds av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1fdf4-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="1fdf4-126">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="1fdf4-126">- Fixed price</span></span></br><span data-ttu-id="1fdf4-127">- Tid och material.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-127">- Time and material.</span></span>| <span data-ttu-id="1fdf4-128">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-129">Project</span><span class="sxs-lookup"><span data-stu-id="1fdf4-129">Project</span></span> | <span data-ttu-id="1fdf4-130">Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="1fdf4-131">När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="1fdf4-132">När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="1fdf4-133">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="1fdf4-134">Uppgifter som ingår</span><span class="sxs-lookup"><span data-stu-id="1fdf4-134">Included Tasks</span></span> | <span data-ttu-id="1fdf4-135">Anger om den här offertraden används för alla eller några av projektuppgifterna för det valda projektet.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="1fdf4-136">Fältet har följande möjliga värden:</span><span class="sxs-lookup"><span data-stu-id="1fdf4-136">This field has the following possible values:</span></span></br><span data-ttu-id="1fdf4-137">- Alla projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="1fdf4-137">- All project tasks</span></span></br><span data-ttu-id="1fdf4-138">- Endast valda projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="1fdf4-138">- Selected project tasks only</span></span></br><span data-ttu-id="1fdf4-139">Ett tomt värde i det här fältet motsvarar alternativet **Alla projektuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="1fdf4-140">När **Endast valda projektuppgifter** har valts kan du på projektsidan, under fliken **Konfiguration av uppgiftsfakturering** välja specifika uppgifter för att associera dem med denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="1fdf4-141">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-142">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="1fdf4-142">Include Time</span></span> | <span data-ttu-id="1fdf4-143">En **Ja**/**Nej**-flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1fdf4-144">Ett **Nej**-värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1fdf4-145">Ett **Ja**-värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1fdf4-146">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-147">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="1fdf4-147">Include Expense</span></span> | <span data-ttu-id="1fdf4-148">En **Ja**/**Nej**-flagga anger om utgiftskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1fdf4-149">Ett **Nej**-värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1fdf4-150">Ett **Ja**-värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1fdf4-151">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-152">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="1fdf4-152">Include Fee</span></span> | <span data-ttu-id="1fdf4-153">En **Ja**/**Nej**-flagga anger om avgifter för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1fdf4-154">Ett **Nej**-värde anger att avgifterna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1fdf4-155">Ett **Ja**-värde anger att avgifterna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1fdf4-156">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-157">Offererad belopp</span><span class="sxs-lookup"><span data-stu-id="1fdf4-157">Quoted Amount</span></span> | <span data-ttu-id="1fdf4-158">Det här är det belopp som är offererat till kunden för allt arbete som baseras på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="1fdf4-159">I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="1fdf4-160">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="1fdf4-161">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-162">Beräknad skatt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-162">Estimated Tax</span></span> | <span data-ttu-id="1fdf4-163">Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="1fdf4-164">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="1fdf4-165">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-166">Offererat belopp efter skatt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="1fdf4-167">Fältet är offertradsbeloppet efter skatt och skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="1fdf4-168">Beloppet i det här fältet beräknas som *Offererat belopp + moms*.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="1fdf4-169">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-170">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="1fdf4-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="1fdf4-171">Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="1fdf4-172">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1fdf4-173">Kundbudget</span><span class="sxs-lookup"><span data-stu-id="1fdf4-173">Customer Budget</span></span> | <span data-ttu-id="1fdf4-174">Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="1fdf4-175">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="1fdf4-176">Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="1fdf4-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="1fdf4-177">**Regel 1**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, tas ett projekt med i offertraden.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="1fdf4-178">**Regel 2**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, kan ett projekt och en viss transaktionsklass endast finnas på en projektbaserad offertrad för en offert.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="1fdf4-179">**Regel 3**: om fältet **Inkluderade uppgifter** är inställt på **Endast valda projektuppgifter**, kan ett projekt och en viss transaktionsklass finnas på flera projektbaserade offertrader för en offert.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="1fdf4-180">**Regel 4**: om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="1fdf4-181">**Regel 5**: om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="1fdf4-182">
                    <strong>Affärsmöjlighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1fdf4-183">
                    <strong>Offert</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1fdf4-184">
                    <strong>Offertrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1fdf4-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="1fdf4-186">
                    <strong>Inkluderade uppgifter</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1fdf4-187">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1fdf4-188">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1fdf4-189">
                    <strong>Inkludera</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1fdf4-190">
                    <strong>Avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="1fdf4-191">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="1fdf4-192">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1fdf4-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-193">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-194">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-195">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-196">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-197">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-198">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-199">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-200">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-201">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-202">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-202">Violation of Rule #2.</span></span> <span data-ttu-id="1fdf4-203">Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-204">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-205">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-206">QL2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-207">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-208">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-209">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-210">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-211">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-212">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-213">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-214">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-215">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-216">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-217">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-218">Inga</span><span class="sxs-lookup"><span data-stu-id="1fdf4-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-219">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-220">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-221">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-221">Violation of Rule #2.</span></span> <span data-ttu-id="1fdf4-222">Tid och avgifter på P1-projekt tas med på offertraderna QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-223">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-224">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-225">QL2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-226">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-227">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-228">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-229">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-230">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-231">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-232">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-233">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-234">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-235">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-236">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-237">Inga</span><span class="sxs-lookup"><span data-stu-id="1fdf4-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-238">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-239">Giltig</span><span class="sxs-lookup"><span data-stu-id="1fdf4-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="1fdf4-240">Tid och avgifter för P1-projekt ingår i QL1.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="1fdf4-241">Utgiften på P1-projektet ingår i QL2.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="1fdf4-242">Det finns ingen överlappning i vad som ska tas med på varje offertrad och är giltig.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-243">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-244">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-245">QL2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-246">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-247">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-248">Inga</span><span class="sxs-lookup"><span data-stu-id="1fdf4-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-249">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-250">Inga</span><span class="sxs-lookup"><span data-stu-id="1fdf4-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-251">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-252">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-253">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-254">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-255">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="1fdf4-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-256">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-257">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-258">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-259">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-260">Överträdelse av regel 2 ovan</span><span class="sxs-lookup"><span data-stu-id="1fdf4-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="1fdf4-261">I Q1 ingår tid, utgifter och avgifter för en deluppsättning av uppgifter i Project P1.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1fdf4-262">QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och överlappar med vad som ingår i Q1.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-263">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-264">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-265">QL2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-266">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-267">Tom</span><span class="sxs-lookup"><span data-stu-id="1fdf4-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-268">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-269">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-270">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-271">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-272">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-273">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-274">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-275">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="1fdf4-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-276">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-277">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-278">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-279">Giltig</span><span class="sxs-lookup"><span data-stu-id="1fdf4-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-280">Per regel 3 ovan,</span><span class="sxs-lookup"><span data-stu-id="1fdf4-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="1fdf4-281">I Q1 ingår tid, utgifter och avgifter för en deluppsättning av uppgifter i Project P1.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1fdf4-282">I QL2 ingår tid, utgifter och avgifter för en deluppsättning av uppgifter i Project P1.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1fdf4-283">Den enda ytterligare valideringen sker runt den deluppsättning av uppgifter i QL1 som skiljer sig från deluppsättningen av uppgifter i QL2.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="1fdf4-284">Detta garanterar att det inte finns några överlappningar.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="1fdf4-285">Detta görs av systemet när uppgifter associeras.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-286">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-287">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-288">QL2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-289">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-290">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="1fdf4-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-291">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-292">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-293">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-294">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-295">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-296">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-297">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-298">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-299">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-300">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-301">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1fdf4-302">Giltig</span><span class="sxs-lookup"><span data-stu-id="1fdf4-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-303">Baserat på regel 5 är Q1 och Q2 två offerter av samma affärsmöjlighet, så de båda kan uppskatta samma komponenter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-304">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-305">K2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-306">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-307">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-308">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-309">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-310">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-311">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-312">O1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-313">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-314">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-315">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-316">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-317">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-318">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-319">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1fdf4-320">Giltig</span><span class="sxs-lookup"><span data-stu-id="1fdf4-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1fdf4-321">Baserat på regel 4 är Q1 och Q2 två offerter av olika affärsmöjligheter, så de kan inte uppskatta samma komponenter i samma projekt.</span><span class="sxs-lookup"><span data-stu-id="1fdf4-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1fdf4-322">O2</span><span class="sxs-lookup"><span data-stu-id="1fdf4-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1fdf4-323">K1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-324">QL1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-325">P1</span><span class="sxs-lookup"><span data-stu-id="1fdf4-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1fdf4-326">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-327">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1fdf4-328">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1fdf4-329">Ja</span><span class="sxs-lookup"><span data-stu-id="1fdf4-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1fdf4-330">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="1fdf4-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

