---
title: Projektbaserade offertrader – Översikt
description: Det här avsnittet innehåller information om hur du använder projektlinjer för projektarbete.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996318"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="600db-103">Projektbaserade offertrader – Översikt</span><span class="sxs-lookup"><span data-stu-id="600db-103">Project quote lines overview</span></span>

<span data-ttu-id="600db-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="600db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="600db-105">Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="600db-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="600db-106">Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="600db-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="600db-107">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="600db-107">Billing Method</span></span>
- <span data-ttu-id="600db-108">Projektmappning</span><span class="sxs-lookup"><span data-stu-id="600db-108">Project Mapping</span></span>
- <span data-ttu-id="600db-109">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="600db-109">Included Transaction classes</span></span>
- <span data-ttu-id="600db-110">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="600db-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="600db-111">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="600db-111">Chargeability setup</span></span>
- <span data-ttu-id="600db-112">Uppskattning med hjälp av offertradsinformation</span><span class="sxs-lookup"><span data-stu-id="600db-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="600db-113">Offertradskunder</span><span class="sxs-lookup"><span data-stu-id="600db-113">Quote line Customers</span></span>

<span data-ttu-id="600db-114">Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="600db-115">Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.</span><span class="sxs-lookup"><span data-stu-id="600db-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="600db-116">**Fält**</span><span class="sxs-lookup"><span data-stu-id="600db-116">**Field**</span></span> | <span data-ttu-id="600db-117">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="600db-117">**Description**</span></span> | <span data-ttu-id="600db-118">**Inverkan nedströms**</span><span class="sxs-lookup"><span data-stu-id="600db-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="600db-119">Namn</span><span class="sxs-lookup"><span data-stu-id="600db-119">Name</span></span> | <span data-ttu-id="600db-120">Namnet på en offertrad som kan hjälpa dig att identifiera den diskreta komponenten i offerten som uppskattas.</span><span class="sxs-lookup"><span data-stu-id="600db-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="600db-121">Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-122">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="600db-122">Billing Method</span></span> | <span data-ttu-id="600db-123">I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="600db-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="600db-124">Fältet innehåller de två huvudkontraktsmodeller som stöds av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="600db-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="600db-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="600db-125">- Fixed price</span></span></br><span data-ttu-id="600db-126">- Tid och material.</span><span class="sxs-lookup"><span data-stu-id="600db-126">- Time and material.</span></span>| <span data-ttu-id="600db-127">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-128">Project</span><span class="sxs-lookup"><span data-stu-id="600db-128">Project</span></span> | <span data-ttu-id="600db-129">Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="600db-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="600db-130">När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="600db-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="600db-131">När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="600db-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="600db-132">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-133">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="600db-133">Include Time</span></span> | <span data-ttu-id="600db-134">En **Ja**/**Nej**-flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="600db-135">Ett **Nej**-värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="600db-136">Ett **Ja**-värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="600db-137">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-138">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="600db-138">Include Expense</span></span> | <span data-ttu-id="600db-139">En **Ja**/**Nej**-flagga anger om utgiftskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="600db-140">Ett **Nej**-värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="600db-141">Ett **Ja**-värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="600db-142">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-143">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="600db-143">Include Fee</span></span> | <span data-ttu-id="600db-144">En **Ja**/**Nej**-flagga anger om avgifter för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="600db-145">Ett **Nej**-värde anger att avgifterna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="600db-146">Ett **Ja**-värde anger att avgifterna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="600db-147">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-148">Offererad belopp</span><span class="sxs-lookup"><span data-stu-id="600db-148">Quoted Amount</span></span> | <span data-ttu-id="600db-149">Det här är det belopp som är offererat till kunden för allt arbete som baseras på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="600db-150">I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="600db-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="600db-151">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="600db-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="600db-152">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-153">Beräknad skatt</span><span class="sxs-lookup"><span data-stu-id="600db-153">Estimated Tax</span></span> | <span data-ttu-id="600db-154">Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden.</span><span class="sxs-lookup"><span data-stu-id="600db-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="600db-155">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="600db-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="600db-156">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-157">Offererat belopp efter skatt</span><span class="sxs-lookup"><span data-stu-id="600db-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="600db-158">Fältet är offertradsbeloppet efter skatt och skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="600db-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="600db-159">Beloppet i det här fältet beräknas som *Offererat belopp + moms*.</span><span class="sxs-lookup"><span data-stu-id="600db-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="600db-160">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-161">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="600db-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="600db-162">Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="600db-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="600db-163">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="600db-164">Kundbudget</span><span class="sxs-lookup"><span data-stu-id="600db-164">Customer Budget</span></span> | <span data-ttu-id="600db-165">Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="600db-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="600db-166">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="600db-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="600db-167">Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="600db-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="600db-168">**Regel 1**: en viss transaktionsklass i det valda projektet kan bara tas med på en projektbaserad offertrad av en offert.</span><span class="sxs-lookup"><span data-stu-id="600db-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="600db-169">**Regel 2**: om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="600db-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="600db-170">**Regel 3**: om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="600db-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="600db-171">
                    <strong>Affärsmöjlighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="600db-172">
                    <strong>Offert</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="600db-173">
                    <strong>Offertrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="600db-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="600db-175">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="600db-176">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="600db-177">
                    <strong>Inkludera</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="600db-178">
                    <strong>avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="600db-179">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="600db-180">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="600db-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-181">O1</span><span class="sxs-lookup"><span data-stu-id="600db-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-182">K1</span><span class="sxs-lookup"><span data-stu-id="600db-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-183">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-184">P1</span><span class="sxs-lookup"><span data-stu-id="600db-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-185">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-186">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-187">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-188">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="600db-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-189">Överträdelse av regel 1.</span><span class="sxs-lookup"><span data-stu-id="600db-189">Violation of Rule #1.</span></span> <span data-ttu-id="600db-190">Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="600db-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-191">O1</span><span class="sxs-lookup"><span data-stu-id="600db-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-192">K1</span><span class="sxs-lookup"><span data-stu-id="600db-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-193">QL2</span><span class="sxs-lookup"><span data-stu-id="600db-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-194">P1</span><span class="sxs-lookup"><span data-stu-id="600db-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-195">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-196">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-197">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-197">Yes</span></span> </p>
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
<span data-ttu-id="600db-198">O1</span><span class="sxs-lookup"><span data-stu-id="600db-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-199">K1</span><span class="sxs-lookup"><span data-stu-id="600db-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-200">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-201">P1</span><span class="sxs-lookup"><span data-stu-id="600db-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-202">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-203">Inga</span><span class="sxs-lookup"><span data-stu-id="600db-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-204">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-205">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="600db-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-206">Överträdelse av regel 1.</span><span class="sxs-lookup"><span data-stu-id="600db-206">Violation of Rule #1.</span></span> <span data-ttu-id="600db-207">Tid och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="600db-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-208">O1</span><span class="sxs-lookup"><span data-stu-id="600db-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-209">K1</span><span class="sxs-lookup"><span data-stu-id="600db-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-210">QL2</span><span class="sxs-lookup"><span data-stu-id="600db-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-211">P1</span><span class="sxs-lookup"><span data-stu-id="600db-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-212">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-213">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-214">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-214">Yes</span></span> </p>
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
<span data-ttu-id="600db-215">O1</span><span class="sxs-lookup"><span data-stu-id="600db-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-216">K1</span><span class="sxs-lookup"><span data-stu-id="600db-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-217">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-218">P1</span><span class="sxs-lookup"><span data-stu-id="600db-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-219">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-220">Inga</span><span class="sxs-lookup"><span data-stu-id="600db-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-221">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-222">Giltig</span><span class="sxs-lookup"><span data-stu-id="600db-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="600db-223">Tid och avgifter för P1-projekt ingår i QL1.</span><span class="sxs-lookup"><span data-stu-id="600db-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="600db-224">Utgiften på P1-projektet ingår i QL2.</span><span class="sxs-lookup"><span data-stu-id="600db-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="600db-225">Det finns ingen överlappning i vad som ska tas med på varje offertrad så att den är giltig.</span><span class="sxs-lookup"><span data-stu-id="600db-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-226">O1</span><span class="sxs-lookup"><span data-stu-id="600db-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-227">K1</span><span class="sxs-lookup"><span data-stu-id="600db-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-228">QL2</span><span class="sxs-lookup"><span data-stu-id="600db-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-229">P1</span><span class="sxs-lookup"><span data-stu-id="600db-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-230">Inga</span><span class="sxs-lookup"><span data-stu-id="600db-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-231">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-232">Inga</span><span class="sxs-lookup"><span data-stu-id="600db-232">No</span></span> </p>
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
<span data-ttu-id="600db-233">O1</span><span class="sxs-lookup"><span data-stu-id="600db-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-234">K1</span><span class="sxs-lookup"><span data-stu-id="600db-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-235">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-236">P1</span><span class="sxs-lookup"><span data-stu-id="600db-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-237">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-238">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-239">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-240">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="600db-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-241">Överträdelse av regel 1 ovan</span><span class="sxs-lookup"><span data-stu-id="600db-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="600db-242">I Q1 ingår tid, utgifter och avgifter för hela projektet P1.</span><span class="sxs-lookup"><span data-stu-id="600db-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="600db-243">QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och överlappar med vad som ingår i Q1.</span><span class="sxs-lookup"><span data-stu-id="600db-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-244">O1</span><span class="sxs-lookup"><span data-stu-id="600db-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-245">K1</span><span class="sxs-lookup"><span data-stu-id="600db-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-246">QL2</span><span class="sxs-lookup"><span data-stu-id="600db-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-247">P1</span><span class="sxs-lookup"><span data-stu-id="600db-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-248">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-249">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-250">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-250">Yes</span></span> </p>
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
<span data-ttu-id="600db-251">O1</span><span class="sxs-lookup"><span data-stu-id="600db-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-252">K1</span><span class="sxs-lookup"><span data-stu-id="600db-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-253">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-254">P1</span><span class="sxs-lookup"><span data-stu-id="600db-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-255">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-256">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-257">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="600db-258">Giltig</span><span class="sxs-lookup"><span data-stu-id="600db-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-259">Baserat på regel 2 är Q1 och Q2 två offerter av samma affärsmöjlighet, så de båda kan uppskatta samma komponenter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="600db-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-260">O1</span><span class="sxs-lookup"><span data-stu-id="600db-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-261">K2</span><span class="sxs-lookup"><span data-stu-id="600db-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-262">QL1 på Q2</span><span class="sxs-lookup"><span data-stu-id="600db-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-263">P1</span><span class="sxs-lookup"><span data-stu-id="600db-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-264">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-265">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-266">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-266">Yes</span></span> </p>
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
<span data-ttu-id="600db-267">O1</span><span class="sxs-lookup"><span data-stu-id="600db-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-268">K1</span><span class="sxs-lookup"><span data-stu-id="600db-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-269">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-270">P1</span><span class="sxs-lookup"><span data-stu-id="600db-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-271">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-272">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-273">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="600db-274">Giltig</span><span class="sxs-lookup"><span data-stu-id="600db-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="600db-275">Baserat på regel 3 är Q1 och Q2 två offerter av olika affärsmöjligheter, så de kan inte uppskatta samma komponenter i samma projekt.</span><span class="sxs-lookup"><span data-stu-id="600db-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="600db-276">O2</span><span class="sxs-lookup"><span data-stu-id="600db-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="600db-277">K1</span><span class="sxs-lookup"><span data-stu-id="600db-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-278">QL1</span><span class="sxs-lookup"><span data-stu-id="600db-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-279">P1</span><span class="sxs-lookup"><span data-stu-id="600db-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-280">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="600db-281">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="600db-282">Ja</span><span class="sxs-lookup"><span data-stu-id="600db-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="600db-283">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="600db-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
