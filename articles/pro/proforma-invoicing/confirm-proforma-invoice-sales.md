---
title: Bekräfta en proforma-faktura
description: I det här ämnet finns information om hur du bekräftar proforma-fakturor i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085448"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="be180-103">Bekräfta en proforma-faktura</span><span class="sxs-lookup"><span data-stu-id="be180-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="be180-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="be180-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="be180-105">När en proforma-faktura har bekräftats uppdateras statusen på projektfakturan till **Bekräftad**.</span><span class="sxs-lookup"><span data-stu-id="be180-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="be180-106">När en faktura har bekräftats blir den skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="be180-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="be180-107">I framtiden går det bara att korrigera en faktura om korrigering eller kreditering har inletts av kunden, eller om fakturan har markerats som betald.</span><span class="sxs-lookup"><span data-stu-id="be180-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="be180-108">I följande tabell visas de faktiska värden som har skapats av systemet.</span><span class="sxs-lookup"><span data-stu-id="be180-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="be180-109">Dessa faktiska värden skapas när vissa operationer utförs i utkastet av projektfakturan innan den bekräftas.</span><span class="sxs-lookup"><span data-stu-id="be180-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="be180-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be180-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="be180-111">
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be180-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-112">Fakturera ett förskott eller ett arvode</span><span class="sxs-lookup"><span data-stu-id="be180-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-113">Ett fakturerat faktiskt värde för försäljning av typen <strong>Arvode</strong> skapas för beloppet på förskottet eller arvodet.</span><span class="sxs-lookup"><span data-stu-id="be180-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-114">Ett icke fakturerat faktiskt värde för försäljning av ett negativt belopp av arvodet eller förskottet som ska användas för avstämning.</span><span class="sxs-lookup"><span data-stu-id="be180-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-115">När du har stämt av ett arvode eller ett förskott på en faktura.</span><span class="sxs-lookup"><span data-stu-id="be180-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-116">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="be180-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="be180-117">Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.</span><span class="sxs-lookup"><span data-stu-id="be180-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-118">Ett fakturerat faktiskt värde för försäljning för beloppet på den här fakturan.</span><span class="sxs-lookup"><span data-stu-id="be180-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be180-119">När du har delvis stämt av ett arvode eller ett förskott på en faktura.</span><span class="sxs-lookup"><span data-stu-id="be180-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-120">En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning.</span><span class="sxs-lookup"><span data-stu-id="be180-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="be180-121">Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.</span><span class="sxs-lookup"><span data-stu-id="be180-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-122">Ett fakturerat faktiskt värde för försäljning för beloppet på den här fakturan.</span><span class="sxs-lookup"><span data-stu-id="be180-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-123">Ett negativt icke fakturerat faktiskt värde för försäljning av det kvarstående beloppet av arvodet eller förskottet som ska användas för avstämning på framtida fakturor.</span><span class="sxs-lookup"><span data-stu-id="be180-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-124">Fakturering av en tidtransaktion utan några ändringar i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="be180-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-125">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-126">Ett fakturerat faktiskt värde för försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be180-127">Fakturering av en tidstransaktion som redigerades för att minska antalet.</span><span class="sxs-lookup"><span data-stu-id="be180-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-128">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-129">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="be180-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-130">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för de återstående timmarna och det återstående beloppet efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="be180-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-131">Fakturering av en tidstransaktion som redigerades för att öka antalet.</span><span class="sxs-lookup"><span data-stu-id="be180-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-132">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-133">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="be180-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-134">Fakturering av en utgiftstransaktion utan några ändringar i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="be180-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-135">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-136">Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet</span><span class="sxs-lookup"><span data-stu-id="be180-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be180-137">Fakturering av en utgiftstransaktion som redigerades för att minska antalet.</span><span class="sxs-lookup"><span data-stu-id="be180-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-138">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-139">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="be180-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-140">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för återstående kvantitet och belopp efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="be180-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-141">Fakturering av en utgiftstransaktion som redigerades för att öka antalet.</span><span class="sxs-lookup"><span data-stu-id="be180-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-142">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="be180-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-143">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för återstående kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="be180-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be180-144">Fakturering av en avgift.</span><span class="sxs-lookup"><span data-stu-id="be180-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-145">Återförande av en ofakturerad försäljning som gäller avgiftbeloppet på den ursprungliga journalraden.</span><span class="sxs-lookup"><span data-stu-id="be180-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-146">Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga journalraden för avgift.</span><span class="sxs-lookup"><span data-stu-id="be180-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="be180-147">Fakturera en milstolpe.</span><span class="sxs-lookup"><span data-stu-id="be180-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-148">Ett fakturerat faktiskt värde för försäljning för milstolpens belopp på den ursprungliga milstolpen på projektkontraktraden.</span><span class="sxs-lookup"><span data-stu-id="be180-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="be180-149">Fakturera en produktbaserad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="be180-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be180-150">Ett fakturerat faktiskt värde för försäljning för produktraden med kvantitet och belopp som kommer från den produktbaserade kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="be180-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
