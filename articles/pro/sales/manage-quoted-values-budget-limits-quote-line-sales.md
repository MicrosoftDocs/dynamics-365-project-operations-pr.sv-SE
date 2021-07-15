---
title: Projektbaserade offertrader – Översikt
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369893"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="26b9e-103">Projektbaserade offertrader – Översikt</span><span class="sxs-lookup"><span data-stu-id="26b9e-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="26b9e-104">_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="26b9e-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="26b9e-105">Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="26b9e-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="26b9e-106">Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="26b9e-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="26b9e-107">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="26b9e-107">Billing Method</span></span>
- <span data-ttu-id="26b9e-108">Mappning av projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="26b9e-108">Project and Task Mapping</span></span>
- <span data-ttu-id="26b9e-109">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="26b9e-109">Included Transaction classes</span></span>
- <span data-ttu-id="26b9e-110">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="26b9e-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="26b9e-111">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="26b9e-111">Chargeability setup</span></span>
- <span data-ttu-id="26b9e-112">Uppskattning med hjälp av offertradsinformation</span><span class="sxs-lookup"><span data-stu-id="26b9e-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="26b9e-113">Offertradskunder</span><span class="sxs-lookup"><span data-stu-id="26b9e-113">Quote line Customers</span></span>

<span data-ttu-id="26b9e-114">Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="26b9e-115">Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.</span><span class="sxs-lookup"><span data-stu-id="26b9e-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="26b9e-116">**Fält**</span><span class="sxs-lookup"><span data-stu-id="26b9e-116">**Field**</span></span> | <span data-ttu-id="26b9e-117">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="26b9e-117">**Description**</span></span> | <span data-ttu-id="26b9e-118">**Inverkan nedströms**</span><span class="sxs-lookup"><span data-stu-id="26b9e-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="26b9e-119">Namn</span><span class="sxs-lookup"><span data-stu-id="26b9e-119">Name</span></span> | <span data-ttu-id="26b9e-120">Namnet på offertraden som gör det lättare att identifiera den diskreta komponenten i offerten som beräknas.</span><span class="sxs-lookup"><span data-stu-id="26b9e-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="26b9e-121">Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="26b9e-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-122">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="26b9e-122">Billing Method</span></span> | <span data-ttu-id="26b9e-123">I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="26b9e-124">Fältet innehåller de två huvudkontraktsmodeller som stöds av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="26b9e-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="26b9e-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="26b9e-125">- Fixed price</span></span></br><span data-ttu-id="26b9e-126">- Tid och material.</span><span class="sxs-lookup"><span data-stu-id="26b9e-126">- Time and material.</span></span>| <span data-ttu-id="26b9e-127">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-128">Project</span><span class="sxs-lookup"><span data-stu-id="26b9e-128">Project</span></span> | <span data-ttu-id="26b9e-129">Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="26b9e-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="26b9e-130">När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="26b9e-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="26b9e-131">När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="26b9e-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="26b9e-132">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="26b9e-133">Uppgifter som ingår</span><span class="sxs-lookup"><span data-stu-id="26b9e-133">Included Tasks</span></span> | <span data-ttu-id="26b9e-134">Anger om den här offertraden används för alla eller några av projektuppgifterna för det valda projektet.</span><span class="sxs-lookup"><span data-stu-id="26b9e-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="26b9e-135">Fältet har följande möjliga värden:</span><span class="sxs-lookup"><span data-stu-id="26b9e-135">This field has the following possible values:</span></span></br><span data-ttu-id="26b9e-136">- Alla projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="26b9e-136">- All project tasks</span></span></br><span data-ttu-id="26b9e-137">- Endast valda projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="26b9e-137">- Selected project tasks only</span></span></br><span data-ttu-id="26b9e-138">Ett tomt värde i det här fältet motsvarar alternativet **Alla projektuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="26b9e-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="26b9e-139">När **Endast markerade projektuppgifter** väljs på projektsidan låter fliken **Faktureringsinställningar för uppgift** dig välja specifika uppgifter för att associera dem till denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="26b9e-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="26b9e-140">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-141">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="26b9e-141">Include Time</span></span> | <span data-ttu-id="26b9e-142">Ett värde **Ja**/**Nej** anger om tidstransaktioner eller arbetskostnader för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-143">Ett **Nej**-värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-144">Ett **Ja**-värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="26b9e-145">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-146">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="26b9e-146">Include Expense</span></span> | <span data-ttu-id="26b9e-147">Ett värde **Ja**/**Nej** anger om utgiftskostnader för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-148">Ett **Nej**-värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-149">Ett **Ja**-värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="26b9e-150">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-151">Ta med material</span><span class="sxs-lookup"><span data-stu-id="26b9e-151">Include Material</span></span> | <span data-ttu-id="26b9e-152">Ett värde **Ja**/**Nej** anger om materialkostnader för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-153">Ett värde för **Nej** indikerar att materialkostnaderna inte kommer att inkluderas i uppskattningen på denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="26b9e-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-154">Ett värde för **Ja** indikerar att materialkostnaderna kommer att inkluderas i uppskattningen på denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="26b9e-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="26b9e-155">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-156">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="26b9e-156">Include Fee</span></span> | <span data-ttu-id="26b9e-157">Ett värde **Ja**/**Nej** anger om utgifter för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-158">Ett **Nej**-värde anger att utgifterna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="26b9e-159">Ett **Ja**-värde anger att utgifterna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="26b9e-160">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-161">Offererad belopp</span><span class="sxs-lookup"><span data-stu-id="26b9e-161">Quoted Amount</span></span> | <span data-ttu-id="26b9e-162">Det här är det belopp som kunden ska beräknas för allt arbete som förutses på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="26b9e-163">I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="26b9e-164">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="26b9e-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="26b9e-165">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-166">Beräknad skatt</span><span class="sxs-lookup"><span data-stu-id="26b9e-166">Estimated Tax</span></span> | <span data-ttu-id="26b9e-167">Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="26b9e-168">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="26b9e-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="26b9e-169">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-170">Offererat belopp efter skatt</span><span class="sxs-lookup"><span data-stu-id="26b9e-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="26b9e-171">Fältet är offertradsbeloppet efter skatt och skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="26b9e-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="26b9e-172">Beloppet i det här fältet beräknas som *Offererat belopp + moms*.</span><span class="sxs-lookup"><span data-stu-id="26b9e-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="26b9e-173">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-174">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="26b9e-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="26b9e-175">Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="26b9e-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="26b9e-176">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="26b9e-177">Kundbudget</span><span class="sxs-lookup"><span data-stu-id="26b9e-177">Customer Budget</span></span> | <span data-ttu-id="26b9e-178">Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="26b9e-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="26b9e-179">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="26b9e-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="26b9e-180">Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="26b9e-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="26b9e-181">**Regel 1**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, tas ett projekt med i offertraden.</span><span class="sxs-lookup"><span data-stu-id="26b9e-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="26b9e-182">**Regel 2**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, kan ett projekt och en viss transaktionsklass endast finnas på en projektbaserad offertrad för en offert.</span><span class="sxs-lookup"><span data-stu-id="26b9e-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="26b9e-183">**Regel 3**: om fältet **Inkluderade uppgifter** är inställt på **Endast valda projektuppgifter**, kan ett projekt och en viss transaktionsklass finnas på flera projektbaserade offertrader för en offert.</span><span class="sxs-lookup"><span data-stu-id="26b9e-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="26b9e-184">**Regel 4**: om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="26b9e-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="26b9e-185">**Regel 5**: om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="26b9e-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="26b9e-186">
                    <strong>Affärsmöjlighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="26b9e-187">
                    <strong>Offert</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="26b9e-188">
                    <strong>Offertrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="26b9e-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="26b9e-190">
                    <strong>Inkluderade uppgifter</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="26b9e-191">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="26b9e-192">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="26b9e-193">
                    <strong>Ta med material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="26b9e-194">
                    <strong>Ta med</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="26b9e-195">
                    <strong>Avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="26b9e-196">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="26b9e-197">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26b9e-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-198">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-199">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-200">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-201">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-202">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-203">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-204">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-205">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-206">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-207">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="26b9e-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-208">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="26b9e-208">Violation of Rule #2.</span></span> <span data-ttu-id="26b9e-209">Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-210">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-211">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-212">QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-213">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-214">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-215">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-216">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-217">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-218">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-219">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-220">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-221">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-222">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-223">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-224">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-225">Inga</span><span class="sxs-lookup"><span data-stu-id="26b9e-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-226">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-227">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-228">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="26b9e-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-229">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="26b9e-229">Violation of Rule #2.</span></span> <span data-ttu-id="26b9e-230">Tid, material och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-231">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-232">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-233">QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-234">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-235">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-236">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-237">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-238">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-239">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-240">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-241">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-242">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-243">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-244">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-245">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-246">Inga</span><span class="sxs-lookup"><span data-stu-id="26b9e-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-247">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-248">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-249">Giltig</span><span class="sxs-lookup"><span data-stu-id="26b9e-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-250">Tid, material och avgifter på P1-projekt tas med i QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="26b9e-251">Utgiften på P1-projektet ingår i QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="26b9e-252">Ingen överlappar vad som ingår på varje offertrad och därför är giltigt.</span><span class="sxs-lookup"><span data-stu-id="26b9e-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-253">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-254">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-255">QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-256">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-257">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-258">Inga</span><span class="sxs-lookup"><span data-stu-id="26b9e-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-259">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-260">Inga</span><span class="sxs-lookup"><span data-stu-id="26b9e-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-261">Inga</span><span class="sxs-lookup"><span data-stu-id="26b9e-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-262">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-263">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-264">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-265">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-266">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="26b9e-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-267">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-268">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-269">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-270">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-271">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="26b9e-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-272">Överträdelse av regel #2</span><span class="sxs-lookup"><span data-stu-id="26b9e-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="26b9e-273">Q1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="26b9e-274">QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och därmed överlappar vad som ingår i Q1.</span><span class="sxs-lookup"><span data-stu-id="26b9e-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-275">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-276">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-277">QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-278">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-279">Tom</span><span class="sxs-lookup"><span data-stu-id="26b9e-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-280">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-281">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-282">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-283">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-284">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-285">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-286">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-287">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-288">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="26b9e-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-289">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-290">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-291">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-292">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-293">Giltig</span><span class="sxs-lookup"><span data-stu-id="26b9e-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-294">Per regel #3,</span><span class="sxs-lookup"><span data-stu-id="26b9e-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="26b9e-295">Q1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="26b9e-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="26b9e-296">QL2 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="26b9e-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="26b9e-297">Den enda ytterligare valideringen är runt deluppsättningen av uppgifter på QL1, som skiljer sig från uppgiftsuppsättningen på QL2 för att säkerställa att ingen överlappar.</span><span class="sxs-lookup"><span data-stu-id="26b9e-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="26b9e-298">Detta görs av systemet när uppgifter associeras.</span><span class="sxs-lookup"><span data-stu-id="26b9e-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-299">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-300">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-301">QL2</span><span class="sxs-lookup"><span data-stu-id="26b9e-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-302">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-303">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="26b9e-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-304">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-305">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-306">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-307">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-308">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-309">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-310">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-311">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-312">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="26b9e-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-313">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-314">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-315">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-316">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-317">Giltig</span><span class="sxs-lookup"><span data-stu-id="26b9e-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-318">Per regel #5, Q1 och Q2 är två offerter på samma möjlighet, så de kan båda uppskatta för samma delar av ett projekt.</span><span class="sxs-lookup"><span data-stu-id="26b9e-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-319">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-320">K2</span><span class="sxs-lookup"><span data-stu-id="26b9e-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-321">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-322">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-323">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="26b9e-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-324">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-325">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-326">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-327">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-328">O1</span><span class="sxs-lookup"><span data-stu-id="26b9e-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-329">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-330">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-331">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-332">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="26b9e-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-333">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-334">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-335">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-336">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-337">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="26b9e-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="26b9e-338">Per regel #4, Q1 och Q2 är två offerter på olika möjligheter, så de kan båda uppskatta för samma delar av samma projekt.</span><span class="sxs-lookup"><span data-stu-id="26b9e-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="26b9e-339">O2</span><span class="sxs-lookup"><span data-stu-id="26b9e-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="26b9e-340">K1</span><span class="sxs-lookup"><span data-stu-id="26b9e-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="26b9e-341">QL1</span><span class="sxs-lookup"><span data-stu-id="26b9e-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-342">P1</span><span class="sxs-lookup"><span data-stu-id="26b9e-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="26b9e-343">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="26b9e-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="26b9e-344">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="26b9e-345">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="26b9e-346">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="26b9e-347">Ja</span><span class="sxs-lookup"><span data-stu-id="26b9e-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
