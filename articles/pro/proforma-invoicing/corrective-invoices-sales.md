---
title: Korrigeringsprojektfakturor
description: Detta ämne ger information om hur du skapar och bekräftar korrigeringsfakturor i Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866613"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="a640c-103">Korrigeringsprojektfakturor</span><span class="sxs-lookup"><span data-stu-id="a640c-103">Corrective project invoices</span></span>

<span data-ttu-id="a640c-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="a640c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a640c-105">En bekräftad projektfaktura kan korrigeras för att bearbeta förändringar eller krediter som har förhandlats med kunden och projektledaren.</span><span class="sxs-lookup"><span data-stu-id="a640c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="a640c-106">Om du vill göra ändringar i en bekräftad faktura öppnar du den bekräftade fakturan och väljer **Korrigera den här fakturan**.</span><span class="sxs-lookup"><span data-stu-id="a640c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a640c-107">Det här alternativet är endast tillgängligt om projektfakturan är bekräftad.</span><span class="sxs-lookup"><span data-stu-id="a640c-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="a640c-108">Ett nytt utkast till faktura skapas från den bekräftade fakturan.</span><span class="sxs-lookup"><span data-stu-id="a640c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="a640c-109">All fakturaradsinformation från den tidigare bekräftade fakturan kopieras till det nya utkastet.</span><span class="sxs-lookup"><span data-stu-id="a640c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="a640c-110">Nedan följer några av de viktigaste begreppen som du bör förstå om radinformation på den nya korrigerade fakturan:</span><span class="sxs-lookup"><span data-stu-id="a640c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="a640c-111">Alla kvantiteter uppdateras till noll.</span><span class="sxs-lookup"><span data-stu-id="a640c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="a640c-112">Programmet antar att alla fakturerade artiklar är helt krediterade.</span><span class="sxs-lookup"><span data-stu-id="a640c-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="a640c-113">Om det behövs kan du manuellt uppdatera dessa kvantiteter för att återspegla den kvantitet som faktureras och inte den kvantitet som krediteras.</span><span class="sxs-lookup"><span data-stu-id="a640c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="a640c-114">Beroende på vilken kvantitet du anger beräknar programmet det krediterade antalet.</span><span class="sxs-lookup"><span data-stu-id="a640c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="a640c-115">Det här beloppet återspeglas i de faktiska värdena som skapas när den korrigerade fakturan bekräftas.</span><span class="sxs-lookup"><span data-stu-id="a640c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="a640c-116">Om du gör ändringar i momsbeloppet måste du ange rätt momsbelopp och inte det momsbelopp som ska krediteras.</span><span class="sxs-lookup"><span data-stu-id="a640c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="a640c-117">Tidigare bekräftade produktbaserade kontraktrader kopieras inte över.</span><span class="sxs-lookup"><span data-stu-id="a640c-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="a640c-118">Bearbetning av korrigeringar på en produktbaserad projektfaktura stöds inte.</span><span class="sxs-lookup"><span data-stu-id="a640c-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="a640c-119">Ändringar av milstolpar bearbetas alltid som fulla krediter.</span><span class="sxs-lookup"><span data-stu-id="a640c-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="a640c-120">Behållare eller förskott kan korrigeras om kunden fakturerades för ett felaktigt belopp.</span><span class="sxs-lookup"><span data-stu-id="a640c-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="a640c-121">Det går att korrigera avstämningar av behållare och förskott om ett felaktigt belopp användes för att stämma av mot avgifterna på en tidigare bekräftad faktura.</span><span class="sxs-lookup"><span data-stu-id="a640c-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a640c-122">Fakturaradsinformation som är korrigeringar av andra redan fakturerade avgifter har fältet **Korrigering** värdet **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a640c-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="a640c-123">Fakturor med korrigerad fakturaradsinformation har ett fält med namnet **Har korrigeringar** som också har värdet **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a640c-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="a640c-124">Fakta som skapas när en korrigerande faktura bekräftas</span><span class="sxs-lookup"><span data-stu-id="a640c-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="a640c-125">I följande tabell visas de faktiska värden som skapas när en korrigeringsfaktura bekräftas.</span><span class="sxs-lookup"><span data-stu-id="a640c-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="a640c-126">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a640c-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="a640c-127">
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a640c-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="a640c-128">Bekräfta korrigeringen av ett fakturerat förskott eller en behållare.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a640c-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-129">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="a640c-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="a640c-130">Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.</span><span class="sxs-lookup"><span data-stu-id="a640c-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-131">Ett fakturerat faktiskt värde för försäljning skapas för beloppet på arvodet eller förskottet för att återföra den ursprungliga fakturerade försäljningen.</span><span class="sxs-lookup"><span data-stu-id="a640c-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-132">Ett nytt fakturerat faktiskt värde för försäljning skapas för det korrigerade beloppet på behållaren eller den förskottsbaserade korrigerade fakturaraden.</span><span class="sxs-lookup"><span data-stu-id="a640c-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-133">Ett icke fakturerat faktiskt värde för försäljning av ett negativt belopp av arvodet eller den förskottsbaserade fakturaraden, som ska användas för avstämning.</span><span class="sxs-lookup"><span data-stu-id="a640c-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="a640c-134">En bekräftelse av korrigeringen av ett tidigare avstämt arvode eller förskott.</span><span class="sxs-lookup"><span data-stu-id="a640c-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-135">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="a640c-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="a640c-136">Det här beloppet är positivt och är avsett att ta bort det negativ som skapades när den tidigare avstämningen gjordes.</span><span class="sxs-lookup"><span data-stu-id="a640c-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-137">Återföring av ett fakturerat faktiskt värde för försäljning för beloppet på föregående faktura.</span><span class="sxs-lookup"><span data-stu-id="a640c-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-138">Ett nytt fakturerat faktiskt värde för försäljning för det korrigerade kvarhållarbeloppet som tillämpas på den korrigerade fakturan.</span><span class="sxs-lookup"><span data-stu-id="a640c-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-139">Ett icke fakturerat faktiskt värde för försäljning med ett negativt belopp från den överblivna arvodet eller förskottet, som ska användas för avstämning på senare fakturor.</span><span class="sxs-lookup"><span data-stu-id="a640c-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a640c-140">Fakturering av hela krediten för en tidigare fakturerad tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-141">Återförande av en fakturerad försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="a640c-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-142">Ett nytt fakturerat faktiskt värde för försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="a640c-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a640c-143">Fakturering av delkrediten för en tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-144">Återförande av en fakturerad försäljning som gäller timmar och belopp som fakturerats på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="a640c-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-145">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="a640c-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-146">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående timmar och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="a640c-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a640c-147">Fakturering av hela krediten för en tidigare fakturerad utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-148">Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.</span><span class="sxs-lookup"><span data-stu-id="a640c-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-149">Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.</span><span class="sxs-lookup"><span data-stu-id="a640c-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a640c-150">Fakturering av delkrediten för en tidigare fakturerad utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-151">Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för en utgift.</span><span class="sxs-lookup"><span data-stu-id="a640c-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-152">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="a640c-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-153">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående kvantitet och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="a640c-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a640c-154">Fakturera hela krediten för en tidigare fakturerad materialtransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-155">En fakturerad försäljning för kvantitet och belopp på det ursprungliga fakturadetalj för material.</span><span class="sxs-lookup"><span data-stu-id="a640c-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-156">En ny ofakturerad faktisk försäljning för kvantitet och belopp på det ursprungliga fakturadetalj för material.</span><span class="sxs-lookup"><span data-stu-id="a640c-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a640c-157">Fakturera delkrediten för en materialtransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-158">En fakturerad försäljning för kvantitet och fakturerat belopp på det ursprungliga fakturadetalj för material.</span><span class="sxs-lookup"><span data-stu-id="a640c-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-159">En ny faktisk ofakturerad försäljning som är debiterbar för kvantitet och belopp på den redigerade fakturaradsdetaljen, en siffra som motsvarar den faktiska faktureringen.</span><span class="sxs-lookup"><span data-stu-id="a640c-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-160">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående kvantitet och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="a640c-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a640c-161">Fakturering av hela krediten för en tidigare fakturerad avgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-162">Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="a640c-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-163">Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="a640c-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a640c-164">Fakturering av delkrediten för en tidigare fakturerad avgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="a640c-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-165">Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="a640c-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-166">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="a640c-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a640c-167">Fakturering av hela krediten för en tidigare fakturerad milstolpe.</span><span class="sxs-lookup"><span data-stu-id="a640c-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-168">Återförande av en fakturerad försäljning som gäller belopp på den ursprungliga fakturaradsinformationen för milstolpen.</span><span class="sxs-lookup"><span data-stu-id="a640c-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="a640c-169">Fakturastatus för milstolpen uppdateras från det att <b>Bokförd kundfaktura</b> till <b>Klar att fakturera</b>.</span><span class="sxs-lookup"><span data-stu-id="a640c-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a640c-170">Fakturering av delkrediten för en tidigare fakturerad milstolpe.</span><span class="sxs-lookup"><span data-stu-id="a640c-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-171">Stöds inte</span><span class="sxs-lookup"><span data-stu-id="a640c-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a640c-172">Kredit och korrigeringar av en tidigare fakturerad produktbaserad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="a640c-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a640c-173">Stöds inte</span><span class="sxs-lookup"><span data-stu-id="a640c-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
