---
title: Bekräfta en proforma projektfaktura
description: Den ämne information om hur du bekräftar projektbaserade proforma-fakturor i Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867109"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="1c0e7-103">Bekräfta en proforma projektfaktura</span><span class="sxs-lookup"><span data-stu-id="1c0e7-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="1c0e7-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="1c0e7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1c0e7-105">När en proforma-faktura har bekräftats uppdateras statusen på projektfakturan till **Bekräftad**.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="1c0e7-106">När en faktura har bekräftats blir den skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="1c0e7-107">Framöver kan fakturan endast korrigeras om det finns några korrigeringar eller krediter som initierats av kunden.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="1c0e7-108">I följande tabell visas de faktiska värden som har skapats av systemet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="1c0e7-109">Dessa faktiska värden skapas när vissa operationer utförs i utkastet av projektfakturan innan den bekräftas.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="1c0e7-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1c0e7-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="1c0e7-111">
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1c0e7-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-112">Fakturera ett förskott eller ett arvode</span><span class="sxs-lookup"><span data-stu-id="1c0e7-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-113">Ett fakturerat faktiskt värde för försäljning av typen <strong>Arvode</strong> skapas för beloppet på förskottet eller arvodet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-114">Ett icke fakturerat faktiskt värde för försäljning av ett negativt belopp av arvodet eller förskottet som ska användas för avstämning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-115">När du har stämt av ett arvode eller ett förskott på en faktura.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-116">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1c0e7-117">Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-118">Ett fakturerat faktiskt värde för försäljning för beloppet på den här fakturan.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1c0e7-119">När du har delvis stämt av ett arvode eller ett förskott på en faktura.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-120">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1c0e7-121">Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-122">Ett fakturerat faktiskt värde för försäljning för beloppet på den här fakturan.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-123">Ett negativt icke fakturerat faktiskt värde för försäljning av det kvarstående beloppet av arvodet eller förskottet som ska användas för avstämning på framtida fakturor.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-124">Fakturering av en tidtransaktion utan några ändringar i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-125">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-126">Ett fakturerat faktiskt värde för försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1c0e7-127">Fakturering av en tidstransaktion som redigerades för att minska antalet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-128">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-129">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-130">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för de återstående timmarna och det återstående beloppet efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-131">Fakturering av en tidstransaktion som redigerades för att öka antalet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-132">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-133">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-134">Fakturering av en utgiftstransaktion utan några ändringar i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-135">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-136">Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet</span><span class="sxs-lookup"><span data-stu-id="1c0e7-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1c0e7-137">Fakturering av en utgiftstransaktion som redigerades för att minska antalet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-138">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-139">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-140">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för återstående kvantitet och belopp efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-141">Fakturering av en utgiftstransaktion som redigerades för att öka antalet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-142">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-143">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för återstående kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-144">Fakturera en materialtransaktion utan att redigera utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-145">En ofakturerad försäljning för kvantitet och belopp på det ursprungliga godkännandet av materialanvändningen.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-146">En fakturerad faktisk försäljning för kvantitet och belopp på det ursprungliga godkännandet av materialanvändningen.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1c0e7-147">Fakturera en materialtransaktion som redigerats för att minska kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-148">En ofakturerad försäljning för kvantitet och belopp på det ursprungliga godkännandet av tidsanvändningen.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-149">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-150">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för återstående kvantitet och belopp efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-151">Fakturera en materialtransaktion som redigerats för att öka kvantiteten.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-152">En ofakturerad försäljning för kvantitet och belopp på det ursprungliga godkännandet av materialanvändningen.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-153">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1c0e7-154">Fakturering av en avgift.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-155">Återförande av en ofakturerad försäljning som gäller avgiftbeloppet på den ursprungliga journalraden.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-156">Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga journalraden för avgift.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1c0e7-157">Fakturera en milstolpe.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-158">Ett fakturerat faktiskt värde för försäljning för milstolpens belopp på den ursprungliga milstolpen på projektkontraktraden.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1c0e7-159">Fakturera en produktbaserad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1c0e7-160">Ett fakturerat faktiskt värde för försäljning för produktraden med kvantitet och belopp som kommer från den produktbaserade kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="1c0e7-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
