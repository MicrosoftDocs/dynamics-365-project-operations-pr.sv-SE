---
title: Översikt över prissättningsdimensioner
description: I det här ämnet finns information om prissättningsdimensioner i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898238"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="8c831-103">Översikt över prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="8c831-103">Pricing dimensions overview</span></span>

<span data-ttu-id="8c831-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="8c831-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c831-105">Dimensionerna som används i personal för att ställa in priser och kostnader faller i två kategorier:</span><span class="sxs-lookup"><span data-stu-id="8c831-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="8c831-106">Personer</span><span class="sxs-lookup"><span data-stu-id="8c831-106">People</span></span>
- <span data-ttu-id="8c831-107">Planerat arbete</span><span class="sxs-lookup"><span data-stu-id="8c831-107">Planned work</span></span>

<span data-ttu-id="8c831-108">Därför finns det två typer av dimensionsvärden för prissättning tillgängliga:</span><span class="sxs-lookup"><span data-stu-id="8c831-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="8c831-109">**Alternativuppsättningar**: dimensioner som är fasta uppräkningar för en uppsättning värden.</span><span class="sxs-lookup"><span data-stu-id="8c831-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="8c831-110">**Entitetsbaserade värden**: dimensioner som kan vara en varierad uppsättning värden.</span><span class="sxs-lookup"><span data-stu-id="8c831-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="8c831-111">Prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="8c831-111">Pricing dimensions</span></span>

<span data-ttu-id="8c831-112">Dynamics 365 Project Operations levereras med en standarduppsättning med prissättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="8c831-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="8c831-113">Du kan visa dessa prissättningsdimensioner genom att gå till **Project Operations** > **parametrar**.</span><span class="sxs-lookup"><span data-stu-id="8c831-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="8c831-114">I parameterposten, på fliken **Beloppsbaserad prissättningsdimension** ska du kontrollera att rollen **msdyn_resourcecategory** och resursorganisationsenheten **msdyn_organizationalunit** har fälten **Gäller för försäljning** och **Gäller för kostnad** inställd på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8c831-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="8c831-115">Med dessa fält aktiverade kan du ange pris och kostnad för varje kombination av roll och organisationsenheter.</span><span class="sxs-lookup"><span data-stu-id="8c831-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="8c831-116">Om du behöver pris eller kostnad för dina resurser med hjälp av ytterligare attribut kan du skapa anpassade fält, entiteter och dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8c831-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="8c831-117">Prissättning av mänsklig resurs</span><span class="sxs-lookup"><span data-stu-id="8c831-117">Pricing human resource time</span></span>
<span data-ttu-id="8c831-118">Hur en organisation prissätter mänsklig resurs är ofta ett viktigt strategiskt övervägande som påverkar organisationens lönsamhet direkt.</span><span class="sxs-lookup"><span data-stu-id="8c831-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="8c831-119">Arbeta med ekonomiteamen och övningsrubriker när organisationen är klar att identifiera hur fakturering och kostnader för personaltid ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="8c831-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="8c831-120">Andra faktorer för prissättningen är om återanvända fält eller entiteter som inte för närvarande är prissättningsdimensioner men som används som prissättningsdimensioner för organisationen.</span><span class="sxs-lookup"><span data-stu-id="8c831-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="8c831-121">Fält som **transaktionskategori** (**msdyn_transactioncategory**) och **bokningsbar resurs** (**bookableresource**) är exempel på sökande dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8c831-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="8c831-122">Fundera över om prissättningsdimensionen ska vara en tabell eller en alternativuppsättning.</span><span class="sxs-lookup"><span data-stu-id="8c831-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="8c831-123">Om du förväntar dig ändringar av värden i en dimension som blir större än 10 eller 12 och du behöver ytterligare attribut för dessa värden kan du skapa en entitet i stället för en alternativuppsättning.</span><span class="sxs-lookup"><span data-stu-id="8c831-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="8c831-124">Om du underhåller en alternativuppsättning, t.ex. lägga till eller ta bort värden, krävs en administratör eller utvecklare för att kunna lägga till nya rader i en tabell kan utföras av de flesta användare.</span><span class="sxs-lookup"><span data-stu-id="8c831-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="8c831-125">I följande exempel visas faktureringskostnader som är inställda utifrån den roll och den resursorganisationsenhet som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="8c831-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="8c831-126">Kostnadstariffer är vanligtvis baserade på den anställdes löneområde och den organisationsenhet de tillhör.</span><span class="sxs-lookup"><span data-stu-id="8c831-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="8c831-127">I det här exemplet ser faktureringskursen och kostnadstabellerna ut på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="8c831-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="8c831-128">**Exempel på faktureringskostnader**</span><span class="sxs-lookup"><span data-stu-id="8c831-128">**Sample bill rates**</span></span>

| <span data-ttu-id="8c831-129">Roll</span><span class="sxs-lookup"><span data-stu-id="8c831-129">Role</span></span>        | <span data-ttu-id="8c831-130">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="8c831-130">Org Unit</span></span>    |<span data-ttu-id="8c831-131">Enhet</span><span class="sxs-lookup"><span data-stu-id="8c831-131">Unit</span></span>      |<span data-ttu-id="8c831-132">Pris</span><span class="sxs-lookup"><span data-stu-id="8c831-132">Price</span></span>      |<span data-ttu-id="8c831-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="8c831-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8c831-134">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="8c831-134">Developer</span></span>   | <span data-ttu-id="8c831-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8c831-135">Contoso US</span></span>  |<span data-ttu-id="8c831-136">Hour</span><span class="sxs-lookup"><span data-stu-id="8c831-136">Hour</span></span> | <span data-ttu-id="8c831-137">200</span><span class="sxs-lookup"><span data-stu-id="8c831-137">200</span></span>|<span data-ttu-id="8c831-138">USD</span><span class="sxs-lookup"><span data-stu-id="8c831-138">USD</span></span>     |
| <span data-ttu-id="8c831-139">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="8c831-139">Developer</span></span>   | <span data-ttu-id="8c831-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="8c831-140">Contoso India</span></span> |<span data-ttu-id="8c831-141">Hour</span><span class="sxs-lookup"><span data-stu-id="8c831-141">Hour</span></span>|   <span data-ttu-id="8c831-142">112</span><span class="sxs-lookup"><span data-stu-id="8c831-142">112</span></span>|<span data-ttu-id="8c831-143">USD</span><span class="sxs-lookup"><span data-stu-id="8c831-143">USD</span></span>     |


<span data-ttu-id="8c831-144">**Exempelkostnadstariffer**</span><span class="sxs-lookup"><span data-stu-id="8c831-144">**Sample cost rates**</span></span>

| <span data-ttu-id="8c831-145">Löneband</span><span class="sxs-lookup"><span data-stu-id="8c831-145">Salary Band</span></span>     | <span data-ttu-id="8c831-146">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="8c831-146">Org Unit</span></span>    |<span data-ttu-id="8c831-147">Enhet</span><span class="sxs-lookup"><span data-stu-id="8c831-147">Unit</span></span>      |<span data-ttu-id="8c831-148">Pris</span><span class="sxs-lookup"><span data-stu-id="8c831-148">Price</span></span>      |<span data-ttu-id="8c831-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="8c831-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8c831-150">Mitt företag_Band1</span><span class="sxs-lookup"><span data-stu-id="8c831-150">My company_Band1</span></span> | <span data-ttu-id="8c831-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8c831-151">Contoso US</span></span>  |<span data-ttu-id="8c831-152">Hour</span><span class="sxs-lookup"><span data-stu-id="8c831-152">Hour</span></span> | <span data-ttu-id="8c831-153">145</span><span class="sxs-lookup"><span data-stu-id="8c831-153">145</span></span>|<span data-ttu-id="8c831-154">USD</span><span class="sxs-lookup"><span data-stu-id="8c831-154">USD</span></span>     |
| <span data-ttu-id="8c831-155">Mitt företag_Band2</span><span class="sxs-lookup"><span data-stu-id="8c831-155">My company_Band2</span></span> | <span data-ttu-id="8c831-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="8c831-156">Contoso India</span></span> |<span data-ttu-id="8c831-157">Hour</span><span class="sxs-lookup"><span data-stu-id="8c831-157">Hour</span></span>|   <span data-ttu-id="8c831-158">67</span><span class="sxs-lookup"><span data-stu-id="8c831-158">67</span></span>|<span data-ttu-id="8c831-159">USD</span><span class="sxs-lookup"><span data-stu-id="8c831-159">USD</span></span>     |
