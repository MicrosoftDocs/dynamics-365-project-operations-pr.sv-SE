---
title: Projektbaserade offertrader
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085407"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="d81c9-103">Projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="d81c9-103">Project-based quote lines</span></span>

<span data-ttu-id="d81c9-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="d81c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d81c9-105">Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="d81c9-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d81c9-106">Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="d81c9-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d81c9-107">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="d81c9-107">Billing Method</span></span>
- <span data-ttu-id="d81c9-108">Projektmappning</span><span class="sxs-lookup"><span data-stu-id="d81c9-108">Project Mapping</span></span>
- <span data-ttu-id="d81c9-109">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="d81c9-109">Included Transaction classes</span></span>
- <span data-ttu-id="d81c9-110">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="d81c9-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d81c9-111">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="d81c9-111">Chargeability setup</span></span>
- <span data-ttu-id="d81c9-112">Uppskattning med hjälp av offertradsinformation</span><span class="sxs-lookup"><span data-stu-id="d81c9-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d81c9-113">Offertradskunder</span><span class="sxs-lookup"><span data-stu-id="d81c9-113">Quote line Customers</span></span>

<span data-ttu-id="d81c9-114">Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d81c9-115">Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.</span><span class="sxs-lookup"><span data-stu-id="d81c9-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d81c9-116">**Fält**</span><span class="sxs-lookup"><span data-stu-id="d81c9-116">**Field**</span></span> | <span data-ttu-id="d81c9-117">**Relevans, syfte och vägledning**</span><span class="sxs-lookup"><span data-stu-id="d81c9-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="d81c9-118">**Inverkan nedströms**</span><span class="sxs-lookup"><span data-stu-id="d81c9-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d81c9-119">Namn</span><span class="sxs-lookup"><span data-stu-id="d81c9-119">Name</span></span> | <span data-ttu-id="d81c9-120">Namnet på en offertrad som kan hjälpa dig att identifiera den diskreta komponenten i offerten som uppskattas.</span><span class="sxs-lookup"><span data-stu-id="d81c9-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d81c9-121">Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-122">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="d81c9-122">Billing Method</span></span> | <span data-ttu-id="d81c9-123">I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d81c9-124">Det här fältet innehåller de två huvudmodellerna för kontrakt som stöds av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d81c9-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d81c9-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="d81c9-125">- Fixed price</span></span></br><span data-ttu-id="d81c9-126">- Tid och material.</span><span class="sxs-lookup"><span data-stu-id="d81c9-126">- Time and material.</span></span>| <span data-ttu-id="d81c9-127">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-128">Project</span><span class="sxs-lookup"><span data-stu-id="d81c9-128">Project</span></span> | <span data-ttu-id="d81c9-129">Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="d81c9-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d81c9-130">När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="d81c9-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d81c9-131">När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="d81c9-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d81c9-132">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-133">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="d81c9-133">Include Time</span></span> | <span data-ttu-id="d81c9-134">En **Ja**/**Nej** -flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d81c9-135">Ett **Nej** -värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d81c9-136">Ett **Ja** -värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d81c9-137">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-138">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="d81c9-138">Include Expense</span></span> | <span data-ttu-id="d81c9-139">En **Ja**/**Nej** -flagga anger om utgiftskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d81c9-140">Ett **Nej** -värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d81c9-141">Ett **Ja** -värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d81c9-142">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-143">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="d81c9-143">Include Fee</span></span> | <span data-ttu-id="d81c9-144">En **Ja**/**Nej** -flagga anger om avgifter för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d81c9-145">Ett **Nej** -värde anger att avgifterna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d81c9-146">Ett **Ja** -värde anger att avgifterna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d81c9-147">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-148">Offererad belopp</span><span class="sxs-lookup"><span data-stu-id="d81c9-148">Quoted Amount</span></span> | <span data-ttu-id="d81c9-149">Det här är det belopp som är offererat till kunden för allt arbete som baseras på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d81c9-150">I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d81c9-151">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="d81c9-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d81c9-152">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-153">Beräknad skatt</span><span class="sxs-lookup"><span data-stu-id="d81c9-153">Estimated Tax</span></span> | <span data-ttu-id="d81c9-154">Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden.</span><span class="sxs-lookup"><span data-stu-id="d81c9-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d81c9-155">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="d81c9-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d81c9-156">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-157">Offererat belopp efter skatt</span><span class="sxs-lookup"><span data-stu-id="d81c9-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="d81c9-158">Fältet är offertradsbeloppet efter skatt och skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="d81c9-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d81c9-159">Beloppet i det här fältet beräknas som *Offererat belopp + moms*.</span><span class="sxs-lookup"><span data-stu-id="d81c9-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d81c9-160">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-161">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="d81c9-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="d81c9-162">Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="d81c9-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d81c9-163">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d81c9-164">Kundbudget</span><span class="sxs-lookup"><span data-stu-id="d81c9-164">Customer Budget</span></span> | <span data-ttu-id="d81c9-165">Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="d81c9-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d81c9-166">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="d81c9-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d81c9-167">Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="d81c9-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d81c9-168">**Regel 1** : en viss transaktionsklass i det valda projektet kan bara tas med på en projektbaserad offertrad av en offert.</span><span class="sxs-lookup"><span data-stu-id="d81c9-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d81c9-169">**Regel 2** : om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="d81c9-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d81c9-170">**Regel 3** : om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="d81c9-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d81c9-171">
                    <strong>Affärsmöjlighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d81c9-172">
                    <strong>Offert</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d81c9-173">
                    <strong>Offertrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d81c9-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d81c9-175">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d81c9-176">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d81c9-177">
                    <strong>Inkludera</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d81c9-178">
                    <strong>avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d81c9-179">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d81c9-180">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d81c9-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-181">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-182">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-183">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-184">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-185">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-186">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-187">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-188">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="d81c9-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-189">Överträdelse av regel 1.</span><span class="sxs-lookup"><span data-stu-id="d81c9-189">Violation of Rule #1.</span></span> <span data-ttu-id="d81c9-190">Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="d81c9-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-191">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-192">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-193">QL2</span><span class="sxs-lookup"><span data-stu-id="d81c9-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-194">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-195">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-196">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-197">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-197">Yes</span></span> </p>
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
<span data-ttu-id="d81c9-198">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-199">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-200">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-201">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-202">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-203">Inga</span><span class="sxs-lookup"><span data-stu-id="d81c9-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-204">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-205">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="d81c9-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-206">Överträdelse av regel 1.</span><span class="sxs-lookup"><span data-stu-id="d81c9-206">Violation of Rule #1.</span></span> <span data-ttu-id="d81c9-207">Tid och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="d81c9-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-208">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-209">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-210">QL2</span><span class="sxs-lookup"><span data-stu-id="d81c9-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-211">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-212">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-213">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-214">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-214">Yes</span></span> </p>
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
<span data-ttu-id="d81c9-215">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-216">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-217">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-218">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-219">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-220">Inga</span><span class="sxs-lookup"><span data-stu-id="d81c9-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-221">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-222">Giltig</span><span class="sxs-lookup"><span data-stu-id="d81c9-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="d81c9-223">Tid och avgifter för P1-projekt ingår i QL1.</span><span class="sxs-lookup"><span data-stu-id="d81c9-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d81c9-224">Utgiften på P1-projektet ingår i QL2.</span><span class="sxs-lookup"><span data-stu-id="d81c9-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d81c9-225">Det finns ingen överlappning i vad som ska tas med på varje offertrad så att den är giltig.</span><span class="sxs-lookup"><span data-stu-id="d81c9-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-226">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-227">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-228">QL2</span><span class="sxs-lookup"><span data-stu-id="d81c9-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-229">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-230">Inga</span><span class="sxs-lookup"><span data-stu-id="d81c9-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-231">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-232">Inga</span><span class="sxs-lookup"><span data-stu-id="d81c9-232">No</span></span> </p>
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
<span data-ttu-id="d81c9-233">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-234">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-235">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-236">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-237">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-238">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-239">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-240">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="d81c9-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-241">Överträdelse av regel 1 ovan</span><span class="sxs-lookup"><span data-stu-id="d81c9-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="d81c9-242">I Q1 ingår tid, utgifter och avgifter för hela projektet P1.</span><span class="sxs-lookup"><span data-stu-id="d81c9-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d81c9-243">QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och överlappar med vad som ingår i Q1.</span><span class="sxs-lookup"><span data-stu-id="d81c9-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-244">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-245">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-246">QL2</span><span class="sxs-lookup"><span data-stu-id="d81c9-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-247">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-248">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-249">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-250">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-250">Yes</span></span> </p>
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
<span data-ttu-id="d81c9-251">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-252">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-254">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-255">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-256">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-257">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d81c9-258">Giltig</span><span class="sxs-lookup"><span data-stu-id="d81c9-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-259">Baserat på regel 2 är Q1 och Q2 två offerter av samma affärsmöjlighet, så de båda kan uppskatta samma komponenter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="d81c9-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-260">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-261">K2</span><span class="sxs-lookup"><span data-stu-id="d81c9-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-262">QL1 på Q2</span><span class="sxs-lookup"><span data-stu-id="d81c9-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-263">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-264">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-265">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-266">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-266">Yes</span></span> </p>
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
<span data-ttu-id="d81c9-267">O1</span><span class="sxs-lookup"><span data-stu-id="d81c9-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-268">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-269">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-270">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-271">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-272">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-273">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d81c9-274">Giltig</span><span class="sxs-lookup"><span data-stu-id="d81c9-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d81c9-275">Baserat på regel 3 är Q1 och Q2 två offerter av olika affärsmöjligheter, så de kan inte uppskatta samma komponenter i samma projekt.</span><span class="sxs-lookup"><span data-stu-id="d81c9-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d81c9-276">O2</span><span class="sxs-lookup"><span data-stu-id="d81c9-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d81c9-277">K1</span><span class="sxs-lookup"><span data-stu-id="d81c9-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-278">QL1</span><span class="sxs-lookup"><span data-stu-id="d81c9-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-279">P1</span><span class="sxs-lookup"><span data-stu-id="d81c9-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-280">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d81c9-281">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d81c9-282">Ja</span><span class="sxs-lookup"><span data-stu-id="d81c9-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d81c9-283">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="d81c9-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

