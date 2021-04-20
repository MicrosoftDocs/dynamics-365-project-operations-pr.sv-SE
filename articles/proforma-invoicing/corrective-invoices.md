---
title: Projektbaserade fakturor för korrigering
description: Detta ämne ger information om hur du skapar och bekräftar projektbaserade fakturor för korrigering i Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867063"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="f33d8-103">Projektbaserade fakturor för korrigering</span><span class="sxs-lookup"><span data-stu-id="f33d8-103">Corrective project-based invoices</span></span>

<span data-ttu-id="f33d8-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="f33d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f33d8-105">En bekräftad projektfaktura kan korrigeras för att bearbeta förändringar eller krediter som har förhandlats med kunden och projektledaren.</span><span class="sxs-lookup"><span data-stu-id="f33d8-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f33d8-106">Om du vill göra ändringar i en bekräftad faktura öppnar du den bekräftade fakturan och väljer **Korrigera den här fakturan**.</span><span class="sxs-lookup"><span data-stu-id="f33d8-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f33d8-107">Detta val är inte tillgängligt om inte en projektfaktura bekräftas eller om den projektbaserade fakturan har förskott eller arvode eller avstämningar av förskott eller arvode.</span><span class="sxs-lookup"><span data-stu-id="f33d8-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="f33d8-108">Ett nytt utkast till faktura skapas från den bekräftade fakturan.</span><span class="sxs-lookup"><span data-stu-id="f33d8-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f33d8-109">All fakturaradsinformation från den tidigare bekräftade fakturan kopieras till det nya utkastet.</span><span class="sxs-lookup"><span data-stu-id="f33d8-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f33d8-110">Nedan följer några av de viktigaste begreppen som du bör förstå om radinformation på den nya korrigerade fakturan:</span><span class="sxs-lookup"><span data-stu-id="f33d8-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f33d8-111">Alla kvantiteter uppdateras till noll.</span><span class="sxs-lookup"><span data-stu-id="f33d8-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f33d8-112">Dynamics 365 Project Operations förutsätter att alla fakturerade objekt krediteras helt.</span><span class="sxs-lookup"><span data-stu-id="f33d8-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f33d8-113">Om det behövs kan du manuellt uppdatera dessa kvantiteter för att återspegla den kvantitet som faktureras och inte den kvantitet som krediteras.</span><span class="sxs-lookup"><span data-stu-id="f33d8-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f33d8-114">Beroende på vilken kvantitet du anger beräknar programmet det krediterade antalet.</span><span class="sxs-lookup"><span data-stu-id="f33d8-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f33d8-115">Det här beloppet återspeglas i de faktiska värdena som skapas när den korrigerade fakturan bekräftas.</span><span class="sxs-lookup"><span data-stu-id="f33d8-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f33d8-116">Om du gör ändringar i momsbeloppet måste du ange rätt momsbelopp och inte det momsbelopp som ska krediteras.</span><span class="sxs-lookup"><span data-stu-id="f33d8-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f33d8-117">Ändringar av milstolpar bearbetas alltid som fulla krediter.</span><span class="sxs-lookup"><span data-stu-id="f33d8-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="f33d8-118">För fakturaradsinformation som är korrigeringar för andra redan fakturerade debiteringar har fältet **Korrigering** angett till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f33d8-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="f33d8-119">För fakturor som har korrigerat fakturaradinformation har fältet **Har korrigeringar** angett till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f33d8-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="f33d8-120">Fakta som skapas när en korrigerande faktura bekräftas</span><span class="sxs-lookup"><span data-stu-id="f33d8-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="f33d8-121">I följande tabell visas de faktiska värden som skapas när en korrigeringsfaktura bekräftas.</span><span class="sxs-lookup"><span data-stu-id="f33d8-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f33d8-122">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f33d8-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f33d8-123">
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f33d8-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f33d8-124">Fakturering av hela krediten för en tidigare fakturerad tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-125">Återförande av en fakturerad försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="f33d8-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-126">Ett nytt fakturerat faktiskt värde för försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="f33d8-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f33d8-127">Fakturering av delkrediten för en tidstransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-128">Återförande av en fakturerad försäljning som gäller timmar och belopp som fakturerats på den ursprungliga fakturaradsinformationen för tid.</span><span class="sxs-lookup"><span data-stu-id="f33d8-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-129">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f33d8-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-130">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående timmar och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="f33d8-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f33d8-131">Fakturering av hela krediten för en tidigare fakturerad utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-132">Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.</span><span class="sxs-lookup"><span data-stu-id="f33d8-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-133">Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.</span><span class="sxs-lookup"><span data-stu-id="f33d8-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f33d8-134">Fakturering av delkrediten för en tidigare fakturerad utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-135">Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för en utgift.</span><span class="sxs-lookup"><span data-stu-id="f33d8-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-136">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f33d8-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-137">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående kvantitet och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="f33d8-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f33d8-138">Fakturera hela krediten för en tidigare fakturerad materialtransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-139">En fakturerad försäljning för kvantitet och belopp på det ursprungliga fakturadetalj för material.</span><span class="sxs-lookup"><span data-stu-id="f33d8-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-140">En ny ofakturerad faktisk försäljning för kvantitet och belopp på det ursprungliga fakturadetalj för material.</span><span class="sxs-lookup"><span data-stu-id="f33d8-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f33d8-141">Fakturera delkrediten för en materialtransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-142">En fakturerad försäljning för kvantitet och fakturerat belopp på det ursprungliga fakturadetalj för material.</span><span class="sxs-lookup"><span data-stu-id="f33d8-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-143">En ny faktisk ofakturerad försäljning som är debiterbar för kvantitet och belopp på den redigerade fakturaradsdetaljen, en siffra som motsvarar den faktiska faktureringen.</span><span class="sxs-lookup"><span data-stu-id="f33d8-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-144">Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående kvantitet och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.</span><span class="sxs-lookup"><span data-stu-id="f33d8-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f33d8-145">Fakturering av hela krediten för en tidigare fakturerad avgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-146">Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="f33d8-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-147">Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="f33d8-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f33d8-148">Fakturering av delkrediten för en tidigare fakturerad avgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="f33d8-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-149">Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för avgift.</span><span class="sxs-lookup"><span data-stu-id="f33d8-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-150">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f33d8-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f33d8-151">Fakturering av hela krediten för en tidigare fakturerad milstolpe.</span><span class="sxs-lookup"><span data-stu-id="f33d8-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-152">Återförande av en fakturerad försäljning som gäller belopp på den ursprungliga fakturaradsinformationen för milstolpen.</span><span class="sxs-lookup"><span data-stu-id="f33d8-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f33d8-153">Fakturastatus för milstolpen uppdateras från det att <b>Bokförd kundfaktura</b> till <b>Klar att fakturera</b>.</span><span class="sxs-lookup"><span data-stu-id="f33d8-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f33d8-154">Fakturering av delkrediten för en tidigare fakturerad milstolpe.</span><span class="sxs-lookup"><span data-stu-id="f33d8-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f33d8-155">Det här scenariot stöds inte.</span><span class="sxs-lookup"><span data-stu-id="f33d8-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
