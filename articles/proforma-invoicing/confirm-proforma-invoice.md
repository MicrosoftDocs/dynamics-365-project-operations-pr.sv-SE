---
title: Bekräfta en proforma-faktura
description: I det här ämne finns information om hur du bekräftar en proforma-faktura.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085385"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="f05aa-103">Bekräfta en proforma-faktura</span><span class="sxs-lookup"><span data-stu-id="f05aa-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="f05aa-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="f05aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f05aa-105">När en proforma-faktura har bekräftats uppdateras statusen på projektfakturan till **Bekräftad**.</span><span class="sxs-lookup"><span data-stu-id="f05aa-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="f05aa-106">När en faktura har bekräftats blir den skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="f05aa-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="f05aa-107">I framtiden går det bara att korrigera en faktura om korrigering eller kreditering har inletts av kunden, eller om fakturan har markerats som betald.</span><span class="sxs-lookup"><span data-stu-id="f05aa-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="f05aa-108">I följande tabell visas de faktiska värden som har skapats av systemet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="f05aa-109">Dessa faktiska värden skapas när vissa operationer utförs i utkastet av projektfakturan innan den bekräftas.</span><span class="sxs-lookup"><span data-stu-id="f05aa-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="f05aa-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f05aa-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="f05aa-111">
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f05aa-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f05aa-112">Fakturering av en tidtransaktion utan några ändringar i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="f05aa-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-113">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-114">Ett fakturerat faktiskt värde för försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f05aa-115">Fakturering av en tidstransaktion som redigerades för att minska antalet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-116">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-117">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f05aa-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-118">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för de återstående timmarna och det återstående beloppet efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f05aa-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f05aa-119">Fakturering av en tidstransaktion som redigerades för att öka antalet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-120">Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-121">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f05aa-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f05aa-122">Fakturering av en utgiftstransaktion utan några ändringar i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="f05aa-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-123">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-124">Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f05aa-125">Fakturering av en utgiftstransaktion som redigerades för att minska antalet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-126">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-127">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f05aa-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-128">Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för återstående kvantitet och belopp efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f05aa-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f05aa-129">Fakturering av en utgiftstransaktion som redigerades för att öka antalet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-130">Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.</span><span class="sxs-lookup"><span data-stu-id="f05aa-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-131">Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för återstående kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.</span><span class="sxs-lookup"><span data-stu-id="f05aa-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f05aa-132">Fakturering av en avgift.</span><span class="sxs-lookup"><span data-stu-id="f05aa-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-133">Återförande av en ofakturerad försäljning som gäller avgiftbeloppet på den ursprungliga journalraden.</span><span class="sxs-lookup"><span data-stu-id="f05aa-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-134">Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga journalraden för avgift.</span><span class="sxs-lookup"><span data-stu-id="f05aa-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f05aa-135">Fakturera en milstolpe.</span><span class="sxs-lookup"><span data-stu-id="f05aa-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f05aa-136">Ett fakturerat faktiskt värde för försäljning för milstolpens belopp på den ursprungliga milstolpen på projektkontraktraden.</span><span class="sxs-lookup"><span data-stu-id="f05aa-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
