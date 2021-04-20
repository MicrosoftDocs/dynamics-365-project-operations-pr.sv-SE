---
title: Skapa projektbaserade fakturor för korrigering
description: Detta ämne ger information om korrigeringsfakturor i Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788902"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="0d13b-103">Skapa projektbaserade fakturor för korrigering</span><span class="sxs-lookup"><span data-stu-id="0d13b-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="0d13b-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="0d13b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d13b-105">En bekräftad projektfaktura kan korrigeras för att bearbeta förändringar eller krediter som har förhandlats med kunden och projektledaren.</span><span class="sxs-lookup"><span data-stu-id="0d13b-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="0d13b-106">Om du vill göra ändringar i en bekräftad faktura öppnar du den bekräftade fakturan och väljer **Korrigera den här fakturan**.</span><span class="sxs-lookup"><span data-stu-id="0d13b-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0d13b-107">Det här alternativet är endast tillgängligt om projektfakturan är bekräftad.</span><span class="sxs-lookup"><span data-stu-id="0d13b-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="0d13b-108">Ett nytt utkast till faktura skapas från den bekräftade fakturan.</span><span class="sxs-lookup"><span data-stu-id="0d13b-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="0d13b-109">All fakturaradsinformation från den tidigare bekräftade fakturan kopieras till det nya utkastet.</span><span class="sxs-lookup"><span data-stu-id="0d13b-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="0d13b-110">Nedan följer några viktiga punkter som hjälper dig att förstå mer om radinformationen för den nya korrigerade fakturan:</span><span class="sxs-lookup"><span data-stu-id="0d13b-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="0d13b-111">Alla kvantiteter uppdateras till noll.</span><span class="sxs-lookup"><span data-stu-id="0d13b-111">All quantities are updated to zero.</span></span> <span data-ttu-id="0d13b-112">Detta förutsätter att alla fakturerade objekt krediteras helt.</span><span class="sxs-lookup"><span data-stu-id="0d13b-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="0d13b-113">Om det behövs kan du manuellt uppdatera dessa kvantiteter för att återspegla den kvantitet som faktureras och inte den kvantitet som krediteras.</span><span class="sxs-lookup"><span data-stu-id="0d13b-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="0d13b-114">Beroende på vilken kvantitet du anger beräknar programmet det krediterade antalet.</span><span class="sxs-lookup"><span data-stu-id="0d13b-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="0d13b-115">Det här beloppet återspeglas i de faktiska värdena som skapas när den korrigerade fakturan bekräftas.</span><span class="sxs-lookup"><span data-stu-id="0d13b-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="0d13b-116">Om du gör ändringar i momsbeloppet måste du ange rätt momsbelopp och inte det momsbelopp som ska krediteras.</span><span class="sxs-lookup"><span data-stu-id="0d13b-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="0d13b-117">Ändringar av milstolpar bearbetas alltid som fulla krediter.</span><span class="sxs-lookup"><span data-stu-id="0d13b-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="0d13b-118">Behållare eller förskott kan korrigeras om kunden fakturerades för ett felaktigt belopp.</span><span class="sxs-lookup"><span data-stu-id="0d13b-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="0d13b-119">Det går att korrigera avstämningar av behållare och förskott om ett felaktigt belopp användes för att stämma av mot avgifterna på en tidigare bekräftad faktura.</span><span class="sxs-lookup"><span data-stu-id="0d13b-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d13b-120">Fakturaradsinformation som är korrigeringar för andra redan fakturerade debiteringar har fältet **Korrigering** angett till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0d13b-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="0d13b-121">Fakturor med korrigerad fakturaradsinformation har ett fält med namnet **Har korrigeringar** som också har värdet **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0d13b-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="0d13b-122">Faktiska värden som skapas vid bekräftelse av en korrigeringsfaktura</span><span class="sxs-lookup"><span data-stu-id="0d13b-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="0d13b-123">I följande tabell visas de faktiska värden som skapas när en korrigeringsfaktura bekräftas.</span><span class="sxs-lookup"><span data-stu-id="0d13b-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0d13b-124">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d13b-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0d13b-125">
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d13b-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0d13b-126">Bekräfta korrigeringen av ett fakturerat förskott eller en behållare.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d13b-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-127">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="0d13b-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0d13b-128">Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.</span><span class="sxs-lookup"><span data-stu-id="0d13b-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-129">Ett fakturerat faktiskt värde för försäljning skapas för beloppet på arvodet eller förskottet för att återföra den ursprungliga fakturerade försäljningen.</span><span class="sxs-lookup"><span data-stu-id="0d13b-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-130">Ett nytt fakturerat faktiskt värde för försäljning skapas för det korrigerade beloppet på behållaren eller den förskottsbaserade korrigerade fakturaraden.</span><span class="sxs-lookup"><span data-stu-id="0d13b-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-131">Ett icke fakturerat faktiskt värde för försäljning av ett negativt belopp av arvodet eller den förskottsbaserade fakturaraden, som ska användas för avstämning.</span><span class="sxs-lookup"><span data-stu-id="0d13b-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0d13b-132">En bekräftelse av korrigeringen av ett tidigare avstämt arvode eller förskott.</span><span class="sxs-lookup"><span data-stu-id="0d13b-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-133">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="0d13b-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0d13b-134">Det här beloppet är positivt och är avsett att ta bort det negativ som skapades när den tidigare avstämningen gjordes.</span><span class="sxs-lookup"><span data-stu-id="0d13b-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-135">Återföring av ett fakturerat faktiskt värde för försäljning för beloppet på föregående faktura.</span><span class="sxs-lookup"><span data-stu-id="0d13b-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-136">Ett nytt fakturerat faktiskt värde för försäljning för det korrigerade kvarhållarbeloppet som tillämpas på den korrigerade fakturan.</span><span class="sxs-lookup"><span data-stu-id="0d13b-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-137">Ett icke fakturerat faktiskt värde för försäljning med ett negativt belopp från den överblivna arvodet eller förskottet, som ska användas för avstämning på senare fakturor.</span><span class="sxs-lookup"><span data-stu-id="0d13b-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d13b-138">Fakturering av hela krediten för en tidigare fakturerad tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="0d13b-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-139">Återförande av en fakturerad försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="0d13b-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-140">Ett nytt fakturerat faktiskt värde för försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="0d13b-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0d13b-141">Fakturering av delkrediten för en tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="0d13b-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-142">Återförande av en fakturerad försäljning som gäller timmar och belopp som fakturerats på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="0d13b-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-143">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="0d13b-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-144">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående timmar och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="0d13b-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d13b-145">Fakturering av hela krediten för en tidigare fakturerad utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="0d13b-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-146">Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.</span><span class="sxs-lookup"><span data-stu-id="0d13b-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-147">Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.</span><span class="sxs-lookup"><span data-stu-id="0d13b-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0d13b-148">Fakturering av delkrediten för en tidigare fakturerad utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="0d13b-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-149">Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för en utgift.</span><span class="sxs-lookup"><span data-stu-id="0d13b-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-150">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="0d13b-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-151">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående kvantitet och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="0d13b-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d13b-152">Fakturering av hela krediten för en tidigare fakturerad avgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="0d13b-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-153">Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="0d13b-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-154">Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="0d13b-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d13b-155">Fakturering av delkrediten för en tidigare fakturerad avgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="0d13b-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-156">Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="0d13b-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-157">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="0d13b-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0d13b-158">Fakturering av hela krediten för en tidigare fakturerad milstolpe.</span><span class="sxs-lookup"><span data-stu-id="0d13b-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-159">Återförande av en fakturerad försäljning som gäller belopp på den ursprungliga fakturaradsinformationen för milstolpen.</span><span class="sxs-lookup"><span data-stu-id="0d13b-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="0d13b-160">Fakturastatus för milstolpen uppdateras från det att <b>Bokförd kundfaktura</b> till <b>Klar att fakturera</b>.</span><span class="sxs-lookup"><span data-stu-id="0d13b-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0d13b-161">Fakturering av delkrediten för en tidigare fakturerad milstolpe.</span><span class="sxs-lookup"><span data-stu-id="0d13b-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d13b-162">Stöds inte</span><span class="sxs-lookup"><span data-stu-id="0d13b-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
