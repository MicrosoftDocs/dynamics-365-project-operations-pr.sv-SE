---
title: Inaktivera en prissättningsdimension
description: I det här ämnet finns information om hur du inaktiverar prissättningsdimensioner.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274750"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="425ec-103">Inaktivera en prissättningsdimension</span><span class="sxs-lookup"><span data-stu-id="425ec-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="425ec-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="425ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="425ec-105">Du kan behöva granska och uppdatera din prissättningsstrategi med några års intervall.</span><span class="sxs-lookup"><span data-stu-id="425ec-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="425ec-106">Alla uppdateringar du gör kanske kräver att du stänger av en befintlig prissättningsdimension och skapar en ny.</span><span class="sxs-lookup"><span data-stu-id="425ec-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="425ec-107">Du kan till exempel ha tidigare prissättning via **Roll**, men nu har du bestämt dig för att få priset via **Arbetserfarenhet**.</span><span class="sxs-lookup"><span data-stu-id="425ec-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="425ec-108">Detta kan medföra att du måste stänga **Roll** som en prissättningsdimension och skapa **arbetserfarenhet** som en ny prissättningsdimension.</span><span class="sxs-lookup"><span data-stu-id="425ec-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="425ec-109">Inaktivera en prissättningsmodell, oavsett om den är slut eller anpassad kan göras genom att ange fälten **Gäller för kostnad** och **Gäller för försäljning** i prissättningsdimensionen till **nej**.</span><span class="sxs-lookup"><span data-stu-id="425ec-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="425ec-110">Men när du gör detta kan felmeddelandet visas, **prisdimensionen kan inte uppdateras eller tas bort om det finns associerade prisposter.**</span><span class="sxs-lookup"><span data-stu-id="425ec-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Affärsprocessfel som uppstår när en prissättningsdimension stängs av](media/Business-Process-Error.png)

<span data-ttu-id="425ec-112">Det här felmeddelandet anger att det finns prissättningsposter som har ställts in tidigare för den dimension som ska stängas av.</span><span class="sxs-lookup"><span data-stu-id="425ec-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="425ec-113">Alla poster för **Rollpris** och **Pålägg för rollpris** som refererar till en dimension måste tas bort innan dimensionens tillämpbarhet kan ställas in på **Nej**.</span><span class="sxs-lookup"><span data-stu-id="425ec-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="425ec-114">Den här regeln gäller både för medföljande prissättningsdimensioner och för de prissättningsdimensioner som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="425ec-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="425ec-115">Anledningen till att validera är att varje post för **rollpris** måste ha en unik kombination av dimensioner.</span><span class="sxs-lookup"><span data-stu-id="425ec-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="425ec-116">Till exempel en prislista med namnet **amerikansk kostnadstaxan 2018** har du följande rader för **rollpris**.</span><span class="sxs-lookup"><span data-stu-id="425ec-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="425ec-117">Standardrubrik</span><span class="sxs-lookup"><span data-stu-id="425ec-117">Standard Title</span></span>         | <span data-ttu-id="425ec-118">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="425ec-118">Org Unit</span></span>    |<span data-ttu-id="425ec-119">Enhet</span><span class="sxs-lookup"><span data-stu-id="425ec-119">Unit</span></span>   |<span data-ttu-id="425ec-120">Pris</span><span class="sxs-lookup"><span data-stu-id="425ec-120">Price</span></span>  |<span data-ttu-id="425ec-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="425ec-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="425ec-122">Systemtekniker</span><span class="sxs-lookup"><span data-stu-id="425ec-122">Systems Engineer</span></span>|<span data-ttu-id="425ec-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="425ec-123">Contoso US</span></span>|<span data-ttu-id="425ec-124">Timme</span><span class="sxs-lookup"><span data-stu-id="425ec-124">Hour</span></span>| <span data-ttu-id="425ec-125">100</span><span class="sxs-lookup"><span data-stu-id="425ec-125">100</span></span>|<span data-ttu-id="425ec-126">USD</span><span class="sxs-lookup"><span data-stu-id="425ec-126">USD</span></span>|
| <span data-ttu-id="425ec-127">Senior systemtekniker</span><span class="sxs-lookup"><span data-stu-id="425ec-127">Senior Systems Engineer</span></span>|<span data-ttu-id="425ec-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="425ec-128">Contoso US</span></span>|<span data-ttu-id="425ec-129">Timme</span><span class="sxs-lookup"><span data-stu-id="425ec-129">Hour</span></span>| <span data-ttu-id="425ec-130">150</span><span class="sxs-lookup"><span data-stu-id="425ec-130">150</span></span>| <span data-ttu-id="425ec-131">USD</span><span class="sxs-lookup"><span data-stu-id="425ec-131">USD</span></span>|


<span data-ttu-id="425ec-132">När du stänger av **Standardrubrik** som prissättningsdimension och prissättningsmotor söker efter ett pris används endast värdet för **organisationsenhet** från inmatningskontexten.</span><span class="sxs-lookup"><span data-stu-id="425ec-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="425ec-133">Om **organisationsenhet** i inmatningskontexten är "Contoso US" är resultatet inte entydigt eftersom båda raderna överensstämmer.</span><span class="sxs-lookup"><span data-stu-id="425ec-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="425ec-134">För att undvika det här scenariot när du skapar posten **Rollpris** bekräftar systemet att kombinationen av dimensioner är unik.</span><span class="sxs-lookup"><span data-stu-id="425ec-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="425ec-135">Om dimensionen inaktiveras efter att posten **Rollpris** har skapats kan den här begränsningen brytas.</span><span class="sxs-lookup"><span data-stu-id="425ec-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="425ec-136">Därför är det nödvändigt att innan du stänger av en dimension, tar bort alla rader för **Rollpris** och **Rollprispålägg** som har det dimensionsvärdet ifyllt.</span><span class="sxs-lookup"><span data-stu-id="425ec-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]