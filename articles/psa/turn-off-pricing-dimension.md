---
title: Inaktivera en prissättningsdimension
description: I det här ämnet visas hur du ställer in prissättningsdimensioner i Project Service-lösningen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085625"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="017f2-103">Inaktivera en prissättningsdimension</span><span class="sxs-lookup"><span data-stu-id="017f2-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="017f2-104">Du kan behöva granska och uppdatera din prissättningsstrategi med några års intervall.</span><span class="sxs-lookup"><span data-stu-id="017f2-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="017f2-105">Alla uppdateringar du gör kanske kräver att du stänger av en befintlig prissättningsdimension och skapar en ny.</span><span class="sxs-lookup"><span data-stu-id="017f2-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="017f2-106">Du kan till exempel ha tidigare prissättning via **Roll** , men nu har du bestämt dig för att få priset via **Arbetserfarenhet**.</span><span class="sxs-lookup"><span data-stu-id="017f2-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="017f2-107">Detta kan medföra att du måste stänga **Roll** som en prissättningsdimension och skapa **arbetserfarenhet** som en ny prissättningsdimension.</span><span class="sxs-lookup"><span data-stu-id="017f2-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="017f2-108">Inaktivera en prissättningsmodell, oavsett om den är slut eller anpassad kan göras genom att ange fälten **Gäller för kostnad** och **Gäller för försäljning** i prissättningsdimensionen till **nej**.</span><span class="sxs-lookup"><span data-stu-id="017f2-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="017f2-109">När du gör detta kan det emellertid hända att följande felmeddelande visas.</span><span class="sxs-lookup"><span data-stu-id="017f2-109">However, when you do this, you might receive the following error message.</span></span>

![Affärsprocessfel som uppstår när en prissättningsdimension stängs av](media/Business-Process-Error.png)


<span data-ttu-id="017f2-111">Det här felmeddelandet anger att det finns prissättningsposter som har ställts in tidigare för den dimension som ska stängas av.</span><span class="sxs-lookup"><span data-stu-id="017f2-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="017f2-112">Alla poster för **Rollpris** och **Pålägg för rollpris** som refererar till en dimension måste tas bort innan dimensionens tillämpbarhet kan ställas in på **Nej**.</span><span class="sxs-lookup"><span data-stu-id="017f2-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="017f2-113">Den här regeln gäller både för medföljande prissättningsdimensioner och för de prissättningsdimensioner som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="017f2-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="017f2-114">Anledningen till att validera är att Project Service har ett villkor som varje post för **rollpris** måste ha en unik kombination av dimensioner.</span><span class="sxs-lookup"><span data-stu-id="017f2-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="017f2-115">Till exempel en prislista med namnet **amerikansk kostnadstaxan 2018** har du följande rader för **rollpris**.</span><span class="sxs-lookup"><span data-stu-id="017f2-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="017f2-116">Standardrubrik</span><span class="sxs-lookup"><span data-stu-id="017f2-116">Standard Title</span></span>         | <span data-ttu-id="017f2-117">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="017f2-117">Org Unit</span></span>    |<span data-ttu-id="017f2-118">Enhet</span><span class="sxs-lookup"><span data-stu-id="017f2-118">Unit</span></span>   |<span data-ttu-id="017f2-119">Pris</span><span class="sxs-lookup"><span data-stu-id="017f2-119">Price</span></span>  |<span data-ttu-id="017f2-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="017f2-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="017f2-121">Systemtekniker</span><span class="sxs-lookup"><span data-stu-id="017f2-121">Systems Engineer</span></span>|<span data-ttu-id="017f2-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="017f2-122">Contoso US</span></span>|<span data-ttu-id="017f2-123">Hour</span><span class="sxs-lookup"><span data-stu-id="017f2-123">Hour</span></span>| <span data-ttu-id="017f2-124">100</span><span class="sxs-lookup"><span data-stu-id="017f2-124">100</span></span>|<span data-ttu-id="017f2-125">USD</span><span class="sxs-lookup"><span data-stu-id="017f2-125">USD</span></span>|
| <span data-ttu-id="017f2-126">Senior systemtekniker</span><span class="sxs-lookup"><span data-stu-id="017f2-126">Senior Systems Engineer</span></span>|<span data-ttu-id="017f2-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="017f2-127">Contoso US</span></span>|<span data-ttu-id="017f2-128">Hour</span><span class="sxs-lookup"><span data-stu-id="017f2-128">Hour</span></span>| <span data-ttu-id="017f2-129">150</span><span class="sxs-lookup"><span data-stu-id="017f2-129">150</span></span>| <span data-ttu-id="017f2-130">USD</span><span class="sxs-lookup"><span data-stu-id="017f2-130">USD</span></span>|


<span data-ttu-id="017f2-131">När du stänger av **Standardrubrik** som prissättningsdimension och Project Service prissättningsmotor söker efter ett pris används endast värdet för **organisationsenhet** från inmatningskontexten.</span><span class="sxs-lookup"><span data-stu-id="017f2-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="017f2-132">Om **organisationsenhet** i inmatningskontexten är "Contoso US" är resultatet inte entydigt eftersom båda raderna överensstämmer.</span><span class="sxs-lookup"><span data-stu-id="017f2-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="017f2-133">För att undvika det här scenariot när du skapar posten **Rollpris** bekräftar Project Service att kombinationen av dimensioner är unik.</span><span class="sxs-lookup"><span data-stu-id="017f2-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="017f2-134">Om dimensionen inaktiveras efter att posten **Rollpris** har skapats kan den här begränsningen brytas.</span><span class="sxs-lookup"><span data-stu-id="017f2-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="017f2-135">Därför är det nödvändigt att innan du stänger av en dimension, tar bort alla rader för **Rollpris** och **Rollprispålägg** som har det dimensionsvärdet ifyllt.</span><span class="sxs-lookup"><span data-stu-id="017f2-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

