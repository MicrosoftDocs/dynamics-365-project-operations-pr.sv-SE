---
title: Projektbaserade offertrader (Pro)
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085470"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="170c5-104">Projektbaserade offertrader (Pro)</span><span class="sxs-lookup"><span data-stu-id="170c5-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="170c5-105">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="170c5-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="170c5-106">Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="170c5-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="170c5-107">Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="170c5-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="170c5-108">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="170c5-108">Billing Method</span></span>
- <span data-ttu-id="170c5-109">Mappning av projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="170c5-109">Project and Task Mapping</span></span>
- <span data-ttu-id="170c5-110">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="170c5-110">Included Transaction classes</span></span>
- <span data-ttu-id="170c5-111">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="170c5-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="170c5-112">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="170c5-112">Chargeability setup</span></span>
- <span data-ttu-id="170c5-113">Uppskattning med hjälp av offertradsinformation</span><span class="sxs-lookup"><span data-stu-id="170c5-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="170c5-114">Offertradskunder</span><span class="sxs-lookup"><span data-stu-id="170c5-114">Quote line Customers</span></span>

<span data-ttu-id="170c5-115">Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="170c5-116">Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.</span><span class="sxs-lookup"><span data-stu-id="170c5-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="170c5-117">**Fält**</span><span class="sxs-lookup"><span data-stu-id="170c5-117">**Field**</span></span> | <span data-ttu-id="170c5-118">**Relevans, syfte och vägledning**</span><span class="sxs-lookup"><span data-stu-id="170c5-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="170c5-119">**Inverkan nedströms**</span><span class="sxs-lookup"><span data-stu-id="170c5-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="170c5-120">Namn</span><span class="sxs-lookup"><span data-stu-id="170c5-120">Name</span></span> | <span data-ttu-id="170c5-121">Namnet på en offertrad som kan hjälpa dig att identifiera den diskreta komponenten i offerten som uppskattas.</span><span class="sxs-lookup"><span data-stu-id="170c5-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="170c5-122">Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-123">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="170c5-123">Billing Method</span></span> | <span data-ttu-id="170c5-124">I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="170c5-125">Det här fältet innehåller de två huvudmodellerna för kontrakt som stöds av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="170c5-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="170c5-126">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="170c5-126">- Fixed price</span></span></br><span data-ttu-id="170c5-127">- Tid och material.</span><span class="sxs-lookup"><span data-stu-id="170c5-127">- Time and material.</span></span>| <span data-ttu-id="170c5-128">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-129">Project</span><span class="sxs-lookup"><span data-stu-id="170c5-129">Project</span></span> | <span data-ttu-id="170c5-130">Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="170c5-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="170c5-131">När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="170c5-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="170c5-132">När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="170c5-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="170c5-133">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="170c5-134">Uppgifter som ingår</span><span class="sxs-lookup"><span data-stu-id="170c5-134">Included Tasks</span></span> | <span data-ttu-id="170c5-135">Anger om den här offertraden används för alla eller några av projektuppgifterna för det valda projektet.</span><span class="sxs-lookup"><span data-stu-id="170c5-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="170c5-136">Fältet har följande möjliga värden:</span><span class="sxs-lookup"><span data-stu-id="170c5-136">This field has the following possible values:</span></span></br><span data-ttu-id="170c5-137">- Alla projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="170c5-137">- All project tasks</span></span></br><span data-ttu-id="170c5-138">- Endast valda projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="170c5-138">- Selected project tasks only</span></span></br><span data-ttu-id="170c5-139">Ett tomt värde i det här fältet motsvarar alternativet **Alla projektuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="170c5-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="170c5-140">När **Endast valda projektuppgifter** har valts kan du på projektsidan, under fliken **Konfiguration av uppgiftsfakturering** välja specifika uppgifter för att associera dem med denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="170c5-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="170c5-141">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-142">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="170c5-142">Include Time</span></span> | <span data-ttu-id="170c5-143">En **Ja**/**Nej** -flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="170c5-144">Ett **Nej** -värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="170c5-145">Ett **Ja** -värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="170c5-146">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-147">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="170c5-147">Include Expense</span></span> | <span data-ttu-id="170c5-148">En **Ja**/**Nej** -flagga anger om utgiftskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="170c5-149">Ett **Nej** -värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="170c5-150">Ett **Ja** -värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="170c5-151">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-152">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="170c5-152">Include Fee</span></span> | <span data-ttu-id="170c5-153">En **Ja**/**Nej** -flagga anger om avgifter för det valda projektet ska tas med i uppskattningen på den här offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="170c5-154">Ett **Nej** -värde anger att avgifterna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="170c5-155">Ett **Ja** -värde anger att avgifterna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="170c5-156">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-157">Offererad belopp</span><span class="sxs-lookup"><span data-stu-id="170c5-157">Quoted Amount</span></span> | <span data-ttu-id="170c5-158">Det här är det belopp som är offererat till kunden för allt arbete som baseras på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="170c5-159">I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="170c5-160">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="170c5-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="170c5-161">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-162">Beräknad skatt</span><span class="sxs-lookup"><span data-stu-id="170c5-162">Estimated Tax</span></span> | <span data-ttu-id="170c5-163">Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="170c5-164">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="170c5-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="170c5-165">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-166">Offererat belopp efter skatt</span><span class="sxs-lookup"><span data-stu-id="170c5-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="170c5-167">Fältet är offertradsbeloppet efter skatt och skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="170c5-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="170c5-168">Beloppet i det här fältet beräknas som *Offererat belopp + moms*.</span><span class="sxs-lookup"><span data-stu-id="170c5-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="170c5-169">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-170">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="170c5-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="170c5-171">Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="170c5-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="170c5-172">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="170c5-173">Kundbudget</span><span class="sxs-lookup"><span data-stu-id="170c5-173">Customer Budget</span></span> | <span data-ttu-id="170c5-174">Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="170c5-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="170c5-175">Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="170c5-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="170c5-176">Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="170c5-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="170c5-177">**Regel 1** : om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter** , tas ett projekt med i offertraden.</span><span class="sxs-lookup"><span data-stu-id="170c5-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="170c5-178">**Regel 2** : om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter** , kan ett projekt och en viss transaktionsklass endast finnas på en projektbaserad offertrad för en offert.</span><span class="sxs-lookup"><span data-stu-id="170c5-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="170c5-179">**Regel 3** : om fältet **Inkluderade uppgifter** är inställt på **Endast valda projektuppgifter** , kan ett projekt och en viss transaktionsklass finnas på flera projektbaserade offertrader för en offert.</span><span class="sxs-lookup"><span data-stu-id="170c5-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="170c5-180">**Regel 4** : om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="170c5-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="170c5-181">**Regel 5** : om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="170c5-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="170c5-182">
                    <strong>Affärsmöjlighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="170c5-183">
                    <strong>Offert</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="170c5-184">
                    <strong>Offertrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="170c5-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="170c5-186">
                    <strong>Inkluderade uppgifter</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="170c5-187">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="170c5-188">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="170c5-189">
                    <strong>Inkludera</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="170c5-190">
                    <strong>Avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="170c5-191">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="170c5-192">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="170c5-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-193">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-194">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-195">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-196">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-197">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-198">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-199">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-200">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-201">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="170c5-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-202">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="170c5-202">Violation of Rule #2.</span></span> <span data-ttu-id="170c5-203">Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="170c5-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-204">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-205">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-206">QL2</span><span class="sxs-lookup"><span data-stu-id="170c5-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-207">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-208">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-209">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-210">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-211">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-211">Yes</span></span> </p>
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
<span data-ttu-id="170c5-212">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-213">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-214">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-215">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-216">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-217">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-218">Inga</span><span class="sxs-lookup"><span data-stu-id="170c5-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-219">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-220">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="170c5-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-221">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="170c5-221">Violation of Rule #2.</span></span> <span data-ttu-id="170c5-222">Tid och avgifter på P1-projekt tas med på offertraderna QL1 och QL2.</span><span class="sxs-lookup"><span data-stu-id="170c5-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-223">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-224">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-225">QL2</span><span class="sxs-lookup"><span data-stu-id="170c5-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-226">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-227">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-228">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-229">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-230">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-230">Yes</span></span> </p>
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
<span data-ttu-id="170c5-231">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-232">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-233">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-234">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-235">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-236">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-237">Inga</span><span class="sxs-lookup"><span data-stu-id="170c5-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-238">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-239">Giltig</span><span class="sxs-lookup"><span data-stu-id="170c5-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="170c5-240">Tid och avgifter för P1-projekt ingår i QL1.</span><span class="sxs-lookup"><span data-stu-id="170c5-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="170c5-241">Utgiften på P1-projektet ingår i QL2.</span><span class="sxs-lookup"><span data-stu-id="170c5-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="170c5-242">Det finns ingen överlappning i vad som ska tas med på varje offertrad och är giltig.</span><span class="sxs-lookup"><span data-stu-id="170c5-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-243">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-244">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-245">QL2</span><span class="sxs-lookup"><span data-stu-id="170c5-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-246">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-247">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-248">Inga</span><span class="sxs-lookup"><span data-stu-id="170c5-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-249">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-250">Inga</span><span class="sxs-lookup"><span data-stu-id="170c5-250">No</span></span> </p>
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
<span data-ttu-id="170c5-251">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-252">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-253">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-254">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-255">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="170c5-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-256">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-257">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-258">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-259">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="170c5-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-260">Överträdelse av regel 2 ovan</span><span class="sxs-lookup"><span data-stu-id="170c5-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="170c5-261">I Q1 ingår tid, utgifter och avgifter för en deluppsättning av uppgifter i Project P1.</span><span class="sxs-lookup"><span data-stu-id="170c5-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="170c5-262">QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och överlappar med vad som ingår i Q1.</span><span class="sxs-lookup"><span data-stu-id="170c5-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-263">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-264">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-265">QL2</span><span class="sxs-lookup"><span data-stu-id="170c5-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-266">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-267">Tom</span><span class="sxs-lookup"><span data-stu-id="170c5-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-268">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-269">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-270">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-270">Yes</span></span> </p>
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
<span data-ttu-id="170c5-271">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-272">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-273">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-274">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-275">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="170c5-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-276">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-277">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-278">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-279">Giltig</span><span class="sxs-lookup"><span data-stu-id="170c5-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-280">Per regel 3 ovan,</span><span class="sxs-lookup"><span data-stu-id="170c5-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="170c5-281">I Q1 ingår tid, utgifter och avgifter för en deluppsättning av uppgifter i Project P1.</span><span class="sxs-lookup"><span data-stu-id="170c5-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="170c5-282">I QL2 ingår tid, utgifter och avgifter för en deluppsättning av uppgifter i Project P1.</span><span class="sxs-lookup"><span data-stu-id="170c5-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="170c5-283">Den enda ytterligare valideringen sker runt den deluppsättning av uppgifter i QL1 som skiljer sig från deluppsättningen av uppgifter i QL2.</span><span class="sxs-lookup"><span data-stu-id="170c5-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="170c5-284">Detta garanterar att det inte finns några överlappningar.</span><span class="sxs-lookup"><span data-stu-id="170c5-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="170c5-285">Detta görs av systemet när uppgifter associeras.</span><span class="sxs-lookup"><span data-stu-id="170c5-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-286">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-287">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-288">QL2</span><span class="sxs-lookup"><span data-stu-id="170c5-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-289">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-290">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="170c5-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-291">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-292">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-293">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-293">Yes</span></span> </p>
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
<span data-ttu-id="170c5-294">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-295">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-296">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-297">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-298">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="170c5-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-299">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-300">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-301">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="170c5-302">Giltig</span><span class="sxs-lookup"><span data-stu-id="170c5-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-303">Baserat på regel 5 är Q1 och Q2 två offerter av samma affärsmöjlighet, så de båda kan uppskatta samma komponenter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="170c5-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-304">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-305">K2</span><span class="sxs-lookup"><span data-stu-id="170c5-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-306">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-307">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-308">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="170c5-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-309">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-310">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-311">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-311">Yes</span></span> </p>
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
<span data-ttu-id="170c5-312">O1</span><span class="sxs-lookup"><span data-stu-id="170c5-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-313">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-314">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-315">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-316">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="170c5-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-317">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-318">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-319">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="170c5-320">Giltig</span><span class="sxs-lookup"><span data-stu-id="170c5-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="170c5-321">Baserat på regel 4 är Q1 och Q2 två offerter av olika affärsmöjligheter, så de kan inte uppskatta samma komponenter i samma projekt.</span><span class="sxs-lookup"><span data-stu-id="170c5-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="170c5-322">O2</span><span class="sxs-lookup"><span data-stu-id="170c5-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="170c5-323">K1</span><span class="sxs-lookup"><span data-stu-id="170c5-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-324">QL1</span><span class="sxs-lookup"><span data-stu-id="170c5-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-325">P1</span><span class="sxs-lookup"><span data-stu-id="170c5-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="170c5-326">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="170c5-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-327">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="170c5-328">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="170c5-329">Ja</span><span class="sxs-lookup"><span data-stu-id="170c5-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="170c5-330">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="170c5-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

