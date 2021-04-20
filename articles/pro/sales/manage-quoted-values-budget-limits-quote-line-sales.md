---
title: Projektbaserade offertrader – Översikt
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858720"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="8edaa-103">Projektbaserade offertrader – Översikt</span><span class="sxs-lookup"><span data-stu-id="8edaa-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="8edaa-104">_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="8edaa-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8edaa-105">Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande.</span><span class="sxs-lookup"><span data-stu-id="8edaa-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="8edaa-106">Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:</span><span class="sxs-lookup"><span data-stu-id="8edaa-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="8edaa-107">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="8edaa-107">Billing Method</span></span>
- <span data-ttu-id="8edaa-108">Mappning av projekt och uppgifter</span><span class="sxs-lookup"><span data-stu-id="8edaa-108">Project and Task Mapping</span></span>
- <span data-ttu-id="8edaa-109">Inkluderade transaktionsklasser</span><span class="sxs-lookup"><span data-stu-id="8edaa-109">Included Transaction classes</span></span>
- <span data-ttu-id="8edaa-110">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="8edaa-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="8edaa-111">Debiterbar inställning</span><span class="sxs-lookup"><span data-stu-id="8edaa-111">Chargeability setup</span></span>
- <span data-ttu-id="8edaa-112">Uppskattning med hjälp av offertradsinformation</span><span class="sxs-lookup"><span data-stu-id="8edaa-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="8edaa-113">Offertradskunder</span><span class="sxs-lookup"><span data-stu-id="8edaa-113">Quote line Customers</span></span>

<span data-ttu-id="8edaa-114">Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="8edaa-115">Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.</span><span class="sxs-lookup"><span data-stu-id="8edaa-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="8edaa-116">**Fält**</span><span class="sxs-lookup"><span data-stu-id="8edaa-116">**Field**</span></span> | <span data-ttu-id="8edaa-117">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="8edaa-117">**Description**</span></span> | <span data-ttu-id="8edaa-118">**Inverkan nedströms**</span><span class="sxs-lookup"><span data-stu-id="8edaa-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8edaa-119">Namn</span><span class="sxs-lookup"><span data-stu-id="8edaa-119">Name</span></span> | <span data-ttu-id="8edaa-120">Namnet på offertraden som gör det lättare att identifiera den diskreta komponenten i offerten som beräknas.</span><span class="sxs-lookup"><span data-stu-id="8edaa-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="8edaa-121">Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits.</span><span class="sxs-lookup"><span data-stu-id="8edaa-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-122">Faktureringsmetod</span><span class="sxs-lookup"><span data-stu-id="8edaa-122">Billing Method</span></span> | <span data-ttu-id="8edaa-123">I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="8edaa-124">Fältet innehåller de två huvudkontraktsmodeller som stöds av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="8edaa-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="8edaa-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="8edaa-125">- Fixed price</span></span></br><span data-ttu-id="8edaa-126">- Tid och material.</span><span class="sxs-lookup"><span data-stu-id="8edaa-126">- Time and material.</span></span>| <span data-ttu-id="8edaa-127">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-128">Project</span><span class="sxs-lookup"><span data-stu-id="8edaa-128">Project</span></span> | <span data-ttu-id="8edaa-129">Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="8edaa-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="8edaa-130">När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="8edaa-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="8edaa-131">När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation.</span><span class="sxs-lookup"><span data-stu-id="8edaa-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="8edaa-132">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="8edaa-133">Uppgifter som ingår</span><span class="sxs-lookup"><span data-stu-id="8edaa-133">Included Tasks</span></span> | <span data-ttu-id="8edaa-134">Anger om den här offertraden används för alla eller några av projektuppgifterna för det valda projektet.</span><span class="sxs-lookup"><span data-stu-id="8edaa-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="8edaa-135">Fältet har följande möjliga värden:</span><span class="sxs-lookup"><span data-stu-id="8edaa-135">This field has the following possible values:</span></span></br><span data-ttu-id="8edaa-136">- Alla projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="8edaa-136">- All project tasks</span></span></br><span data-ttu-id="8edaa-137">- Endast valda projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="8edaa-137">- Selected project tasks only</span></span></br><span data-ttu-id="8edaa-138">Ett tomt värde i det här fältet motsvarar alternativet **Alla projektuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="8edaa-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="8edaa-139">När **Endast markerade projektuppgifter** väljs på projektsidan låter fliken **Faktureringsinställningar för uppgift** dig välja specifika uppgifter för att associera dem till denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="8edaa-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="8edaa-140">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-141">Inkludera tid</span><span class="sxs-lookup"><span data-stu-id="8edaa-141">Include Time</span></span> | <span data-ttu-id="8edaa-142">Ett värde **Ja**/**Nej** anger om tidstransaktioner eller arbetskostnader för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-143">Ett **Nej**-värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-144">Ett **Ja**-värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8edaa-145">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-146">Ta med utgift</span><span class="sxs-lookup"><span data-stu-id="8edaa-146">Include Expense</span></span> | <span data-ttu-id="8edaa-147">Ett värde **Ja**/**Nej** anger om utgiftskostnader för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-148">Ett **Nej**-värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-149">Ett **Ja**-värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8edaa-150">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-151">Ta med material</span><span class="sxs-lookup"><span data-stu-id="8edaa-151">Include Material</span></span> | <span data-ttu-id="8edaa-152">Ett värde **Ja**/**Nej** anger om materialkostnader för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-153">Ett värde för **Nej** indikerar att materialkostnaderna inte kommer att inkluderas i uppskattningen på denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="8edaa-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-154">Ett värde för **Ja** indikerar att materialkostnaderna kommer att inkluderas i uppskattningen på denna offertrad.</span><span class="sxs-lookup"><span data-stu-id="8edaa-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8edaa-155">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-156">Inkludera avgift</span><span class="sxs-lookup"><span data-stu-id="8edaa-156">Include Fee</span></span> | <span data-ttu-id="8edaa-157">Ett värde **Ja**/**Nej** anger om utgifter för det valda projektet kommer att tas med i beräkningen på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-158">Ett **Nej**-värde anger att utgifterna inte inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8edaa-159">Ett **Ja**-värde anger att utgifterna inkluderas i uppskattningen i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8edaa-160">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-161">Offererad belopp</span><span class="sxs-lookup"><span data-stu-id="8edaa-161">Quoted Amount</span></span> | <span data-ttu-id="8edaa-162">Det här är det belopp som kunden ska beräknas för allt arbete som förutses på den projektbaserade offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="8edaa-163">I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="8edaa-164">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="8edaa-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="8edaa-165">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-166">Beräknad skatt</span><span class="sxs-lookup"><span data-stu-id="8edaa-166">Estimated Tax</span></span> | <span data-ttu-id="8edaa-167">Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="8edaa-168">När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="8edaa-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="8edaa-169">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-170">Offererat belopp efter skatt</span><span class="sxs-lookup"><span data-stu-id="8edaa-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="8edaa-171">Fältet är offertradsbeloppet efter skatt och skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="8edaa-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="8edaa-172">Beloppet i det här fältet beräknas som *Offererat belopp + moms*.</span><span class="sxs-lookup"><span data-stu-id="8edaa-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="8edaa-173">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-174">Undre gräns</span><span class="sxs-lookup"><span data-stu-id="8edaa-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="8edaa-175">Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**.</span><span class="sxs-lookup"><span data-stu-id="8edaa-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="8edaa-176">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8edaa-177">Kundbudget</span><span class="sxs-lookup"><span data-stu-id="8edaa-177">Customer Budget</span></span> | <span data-ttu-id="8edaa-178">Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet.</span><span class="sxs-lookup"><span data-stu-id="8edaa-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="8edaa-179">Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.</span><span class="sxs-lookup"><span data-stu-id="8edaa-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="8edaa-180">Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader</span><span class="sxs-lookup"><span data-stu-id="8edaa-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="8edaa-181">**Regel 1**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, tas ett projekt med i offertraden.</span><span class="sxs-lookup"><span data-stu-id="8edaa-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="8edaa-182">**Regel 2**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, kan ett projekt och en viss transaktionsklass endast finnas på en projektbaserad offertrad för en offert.</span><span class="sxs-lookup"><span data-stu-id="8edaa-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="8edaa-183">**Regel 3**: om fältet **Inkluderade uppgifter** är inställt på **Endast valda projektuppgifter**, kan ett projekt och en viss transaktionsklass finnas på flera projektbaserade offertrader för en offert.</span><span class="sxs-lookup"><span data-stu-id="8edaa-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="8edaa-184">**Regel 4**: om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="8edaa-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="8edaa-185">**Regel 5**: om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.</span><span class="sxs-lookup"><span data-stu-id="8edaa-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="8edaa-186">
                    <strong>Affärsmöjlighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="8edaa-187">
                    <strong>Offert</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="8edaa-188">
                    <strong>Offertrad</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="8edaa-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="8edaa-190">
                    <strong>Inkluderade uppgifter</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="8edaa-191">
                    <strong>Inkludera tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="8edaa-192">
                    <strong>Ta med utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="8edaa-193">
                    <strong>Ta med material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="8edaa-194">
                    <strong>Ta med</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="8edaa-195">
                    <strong>Avgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="8edaa-196">
                    <strong>Giltigt/ogiltigt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="8edaa-197">
                    <strong>Orsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8edaa-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-198">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-199">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-200">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-201">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-202">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-203">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-204">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-205">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-206">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-207">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8edaa-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-208">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="8edaa-208">Violation of Rule #2.</span></span> <span data-ttu-id="8edaa-209">Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-210">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-211">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-212">QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-213">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-214">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-215">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-216">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-217">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-218">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-218">Yes</span></span> </p>
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
<span data-ttu-id="8edaa-219">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-220">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-221">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-222">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-223">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-224">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-225">Inga</span><span class="sxs-lookup"><span data-stu-id="8edaa-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-226">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-227">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-228">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8edaa-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-229">Överträdelse av regel 2.</span><span class="sxs-lookup"><span data-stu-id="8edaa-229">Violation of Rule #2.</span></span> <span data-ttu-id="8edaa-230">Tid, material och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-231">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-232">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-233">QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-234">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-235">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-236">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-237">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-238">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-239">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-239">Yes</span></span> </p>
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
<span data-ttu-id="8edaa-240">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-241">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-242">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-243">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-244">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-245">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-246">Inga</span><span class="sxs-lookup"><span data-stu-id="8edaa-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-247">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-248">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-249">Giltig</span><span class="sxs-lookup"><span data-stu-id="8edaa-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-250">Tid, material och avgifter på P1-projekt tas med i QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="8edaa-251">Utgiften på P1-projektet ingår i QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="8edaa-252">Ingen överlappar vad som ingår på varje offertrad och därför är giltigt.</span><span class="sxs-lookup"><span data-stu-id="8edaa-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-253">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-254">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-255">QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-256">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-257">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-258">Inga</span><span class="sxs-lookup"><span data-stu-id="8edaa-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-259">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-260">Inga</span><span class="sxs-lookup"><span data-stu-id="8edaa-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-261">Inga</span><span class="sxs-lookup"><span data-stu-id="8edaa-261">No</span></span> </p>
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
<span data-ttu-id="8edaa-262">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-263">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-264">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-265">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-266">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="8edaa-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-267">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-268">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-269">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-270">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-271">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8edaa-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-272">Överträdelse av regel #2</span><span class="sxs-lookup"><span data-stu-id="8edaa-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="8edaa-273">Q1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="8edaa-274">QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och därmed överlappar vad som ingår i Q1.</span><span class="sxs-lookup"><span data-stu-id="8edaa-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-275">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-276">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-277">QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-278">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-279">Tom</span><span class="sxs-lookup"><span data-stu-id="8edaa-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-280">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-281">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-282">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-283">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-283">Yes</span></span> </p>
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
<span data-ttu-id="8edaa-284">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-285">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-286">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-287">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-288">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="8edaa-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-289">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-290">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-291">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-292">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-293">Giltig</span><span class="sxs-lookup"><span data-stu-id="8edaa-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-294">Per regel #3,</span><span class="sxs-lookup"><span data-stu-id="8edaa-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="8edaa-295">Q1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="8edaa-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8edaa-296">QL2 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.</span><span class="sxs-lookup"><span data-stu-id="8edaa-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8edaa-297">Den enda ytterligare valideringen är runt deluppsättningen av uppgifter på QL1, som skiljer sig från uppgiftsuppsättningen på QL2 för att säkerställa att ingen överlappar.</span><span class="sxs-lookup"><span data-stu-id="8edaa-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="8edaa-298">Detta görs av systemet när uppgifter associeras.</span><span class="sxs-lookup"><span data-stu-id="8edaa-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-299">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-300">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-301">QL2</span><span class="sxs-lookup"><span data-stu-id="8edaa-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-302">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-303">Endast valda uppgifter</span><span class="sxs-lookup"><span data-stu-id="8edaa-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-304">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-305">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-306">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-307">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-307">Yes</span></span> </p>
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
<span data-ttu-id="8edaa-308">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-309">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-310">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-311">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-312">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="8edaa-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-313">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-314">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-315">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-316">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-317">Giltig</span><span class="sxs-lookup"><span data-stu-id="8edaa-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-318">Per regel #5, Q1 och Q2 är två offerter på samma möjlighet, så de kan båda uppskatta för samma delar av ett projekt.</span><span class="sxs-lookup"><span data-stu-id="8edaa-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-319">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-320">K2</span><span class="sxs-lookup"><span data-stu-id="8edaa-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-321">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-322">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-323">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="8edaa-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-324">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-325">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-326">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-327">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-327">Yes</span></span> </p>
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
<span data-ttu-id="8edaa-328">O1</span><span class="sxs-lookup"><span data-stu-id="8edaa-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-329">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-330">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-331">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-332">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="8edaa-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-333">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-334">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-335">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-336">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-337">Ogiltigt</span><span class="sxs-lookup"><span data-stu-id="8edaa-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8edaa-338">Per regel #4, Q1 och Q2 är två offerter på olika möjligheter, så de kan båda uppskatta för samma delar av samma projekt.</span><span class="sxs-lookup"><span data-stu-id="8edaa-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="8edaa-339">O2</span><span class="sxs-lookup"><span data-stu-id="8edaa-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="8edaa-340">K1</span><span class="sxs-lookup"><span data-stu-id="8edaa-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="8edaa-341">QL1</span><span class="sxs-lookup"><span data-stu-id="8edaa-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-342">P1</span><span class="sxs-lookup"><span data-stu-id="8edaa-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="8edaa-343">Alla projektuppgifter eller tomt</span><span class="sxs-lookup"><span data-stu-id="8edaa-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="8edaa-344">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="8edaa-345">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8edaa-346">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8edaa-347">Ja</span><span class="sxs-lookup"><span data-stu-id="8edaa-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
