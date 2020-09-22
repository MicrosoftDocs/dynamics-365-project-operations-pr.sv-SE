---
title: Startsida för prissättnings- och kostnadsdimensioner
description: I det här ämnet finns en översikt över prissättningsdimensioner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756197"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="ee3a4-103">Startsida för prissättnings- och kostnadsdimensioner</span><span class="sxs-lookup"><span data-stu-id="ee3a4-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="ee3a4-104">Dimensionerna som används i personal för att ställa in priser och kostnader faller i två kategorier:</span><span class="sxs-lookup"><span data-stu-id="ee3a4-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="ee3a4-105">Personer</span><span class="sxs-lookup"><span data-stu-id="ee3a4-105">People</span></span>
- <span data-ttu-id="ee3a4-106">Planerat arbete</span><span class="sxs-lookup"><span data-stu-id="ee3a4-106">Planned work</span></span>

<span data-ttu-id="ee3a4-107">Därför finns det två typer av dimensionsvärden för prissättning tillgängliga i PSA (Project Service Automation):</span><span class="sxs-lookup"><span data-stu-id="ee3a4-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="ee3a4-108">**Alternativuppsättningar** - dimensioner som är fasta uppräkningar för en uppsättning värden.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="ee3a4-109">**Entitetsbaserade värden** – dimensioner som kan vara en varierad uppsättning värden.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="ee3a4-110">Prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="ee3a4-110">Pricing dimensions</span></span>

<span data-ttu-id="ee3a4-111">PSA levererar en standarduppsättning med prisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="ee3a4-112">Du kan visa dessa genom att gå till **Project Service** > **parametrar**.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="ee3a4-113">I parameterposten, på fliken **Beloppsbaserad prissättningsdimension** ska du kontrollera att rollen **msdyn_resourcecategory** och resursorganisationsenheten **msdyn_organizationalunit** har fälten **Gäller för försäljning** och **Gäller för kostnad** inställd på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="ee3a4-114">På så sätt kan du ange pris och kostnad för varje kombination av roll och organisationsenheter.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Skärmbild av parametrar för Project Service med "gäller för försäljning" markerad](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="ee3a4-116">Om du har använt de här fälten som roll- och organisationsenhet som prissättningsdimensioner före version 3 av PSA-versionen kommer det inte att finnas någon observerbar förändring.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="ee3a4-117">Du kan fortsätta att använda Project Service som vanligt.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="ee3a4-118">Om du behöver pris eller kostnad för dina resurser med hjälp av ytterligare attribut kan du skapa anpassade fält, entiteter och dimensioner.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="ee3a4-119">Mer information finns i följande avsnitt: Tänk dock på att du måste genomföra procedurerna i nedanstående ordning:</span><span class="sxs-lookup"><span data-stu-id="ee3a4-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="ee3a4-120">Skapa anpassade fält och entiteter</span><span class="sxs-lookup"><span data-stu-id="ee3a4-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="ee3a4-121">Lägg till anpassade fält i prisinställning och transaktionella entiteter</span><span class="sxs-lookup"><span data-stu-id="ee3a4-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="ee3a4-122">Konfigurera anpassade fält som prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="ee3a4-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="ee3a4-123">Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="ee3a4-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="ee3a4-124">Prissättning av mänsklig resurs</span><span class="sxs-lookup"><span data-stu-id="ee3a4-124">Pricing human resource time</span></span>
<span data-ttu-id="ee3a4-125">Hur en organisation prissätter mänsklig resurs är ofta ett viktigt strategiskt övervägande som påverkar organisationens lönsamhet direkt.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="ee3a4-126">Arbeta med ekonomiteamen och övningsrubriker när organisationen är klar att identifiera hur fakturering och kostnader för personaltid ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="ee3a4-127">Andra faktorer för prissättningen är om återanvända fält eller entiteter som inte för närvarande är prissättningsdimensioner men som används som prissättningsdimensioner för organisationen.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="ee3a4-128">Fält som **transaktionskategori** (**msdyn_transactioncategory**) och **bokningsbar resurs** (**bookableresource**) är exempel på sökande dimensioner.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="ee3a4-129">Du bör också fundera över om prissättningsdimensionen ska vara en tabell eller en alternativuppsättning.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="ee3a4-130">Om du förväntar dig ändringar av värden i en dimension som blir större än 10 eller 12 och du behöver ytterligare attribut för dessa värden kan du skapa en entitet i stället för en alternativuppsättning.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="ee3a4-131">Om du underhåller en alternativuppsättning, t.ex. lägga till eller ta bort värden, krävs en administratör eller utvecklare för att kunna lägga till nya rader i en tabell kan utföras av de flesta användare.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="ee3a4-132">I följande exempel visas faktureringskostnader som är inställda utifrån den roll och den resursorganisationsenhet som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="ee3a4-133">Kostnadstariffer är vanligtvis baserade på den anställdes löneområde och den organisationsenhet de tillhör.</span><span class="sxs-lookup"><span data-stu-id="ee3a4-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="ee3a4-134">I det här exemplet ser faktureringskursen och kostnadstabellerna ut på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="ee3a4-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="ee3a4-135">**Exempel på faktureringskostnader**</span><span class="sxs-lookup"><span data-stu-id="ee3a4-135">**Sample bill rates**</span></span>

| <span data-ttu-id="ee3a4-136">Roll</span><span class="sxs-lookup"><span data-stu-id="ee3a4-136">Role</span></span>        | <span data-ttu-id="ee3a4-137">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="ee3a4-137">Org Unit</span></span>    |<span data-ttu-id="ee3a4-138">Enhet</span><span class="sxs-lookup"><span data-stu-id="ee3a4-138">Unit</span></span>      |<span data-ttu-id="ee3a4-139">Pris</span><span class="sxs-lookup"><span data-stu-id="ee3a4-139">Price</span></span>      |<span data-ttu-id="ee3a4-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="ee3a4-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="ee3a4-141">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="ee3a4-141">Developer</span></span>   | <span data-ttu-id="ee3a4-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ee3a4-142">Contoso US</span></span>  |<span data-ttu-id="ee3a4-143">Hour</span><span class="sxs-lookup"><span data-stu-id="ee3a4-143">Hour</span></span> | <span data-ttu-id="ee3a4-144">200</span><span class="sxs-lookup"><span data-stu-id="ee3a4-144">200</span></span>|<span data-ttu-id="ee3a4-145">USD</span><span class="sxs-lookup"><span data-stu-id="ee3a4-145">USD</span></span>     |
| <span data-ttu-id="ee3a4-146">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="ee3a4-146">Developer</span></span>   | <span data-ttu-id="ee3a4-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="ee3a4-147">Contoso India</span></span> |<span data-ttu-id="ee3a4-148">Hour</span><span class="sxs-lookup"><span data-stu-id="ee3a4-148">Hour</span></span>|   <span data-ttu-id="ee3a4-149">112</span><span class="sxs-lookup"><span data-stu-id="ee3a4-149">112</span></span>|<span data-ttu-id="ee3a4-150">USD</span><span class="sxs-lookup"><span data-stu-id="ee3a4-150">USD</span></span>     |


<span data-ttu-id="ee3a4-151">**Exempelkostnadstariffer**</span><span class="sxs-lookup"><span data-stu-id="ee3a4-151">**Sample cost rates**</span></span>

| <span data-ttu-id="ee3a4-152">Löneband</span><span class="sxs-lookup"><span data-stu-id="ee3a4-152">Salary Band</span></span>     | <span data-ttu-id="ee3a4-153">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="ee3a4-153">Org Unit</span></span>    |<span data-ttu-id="ee3a4-154">Enhet</span><span class="sxs-lookup"><span data-stu-id="ee3a4-154">Unit</span></span>      |<span data-ttu-id="ee3a4-155">Pris</span><span class="sxs-lookup"><span data-stu-id="ee3a4-155">Price</span></span>      |<span data-ttu-id="ee3a4-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="ee3a4-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="ee3a4-157">Mitt företag_Band1</span><span class="sxs-lookup"><span data-stu-id="ee3a4-157">My company_Band1</span></span> | <span data-ttu-id="ee3a4-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ee3a4-158">Contoso US</span></span>  |<span data-ttu-id="ee3a4-159">Hour</span><span class="sxs-lookup"><span data-stu-id="ee3a4-159">Hour</span></span> | <span data-ttu-id="ee3a4-160">145</span><span class="sxs-lookup"><span data-stu-id="ee3a4-160">145</span></span>|<span data-ttu-id="ee3a4-161">USD</span><span class="sxs-lookup"><span data-stu-id="ee3a4-161">USD</span></span>     |
| <span data-ttu-id="ee3a4-162">Mitt företag_Band2</span><span class="sxs-lookup"><span data-stu-id="ee3a4-162">My company_Band2</span></span> | <span data-ttu-id="ee3a4-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="ee3a4-163">Contoso India</span></span> |<span data-ttu-id="ee3a4-164">Hour</span><span class="sxs-lookup"><span data-stu-id="ee3a4-164">Hour</span></span>|   <span data-ttu-id="ee3a4-165">67</span><span class="sxs-lookup"><span data-stu-id="ee3a4-165">67</span></span>|<span data-ttu-id="ee3a4-166">USD</span><span class="sxs-lookup"><span data-stu-id="ee3a4-166">USD</span></span>     |
