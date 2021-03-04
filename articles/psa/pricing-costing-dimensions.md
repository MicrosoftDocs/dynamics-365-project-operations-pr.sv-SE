---
title: Startsida för prissättnings- och kostnadsdimensioner
description: I det här ämnet finns en översikt över prissättningsdimensioner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151320"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="f7f4d-103">Startsida för prissättnings- och kostnadsdimensioner</span><span class="sxs-lookup"><span data-stu-id="f7f4d-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f7f4d-104">De dimensioner som används för att ange lönesättning och kostnader i projektbaserade organisationer påverkas av följande attribut:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="f7f4d-105">Personer som utför arbete på ungefär samma sätt som deras erfarenheter, roll eller geografi</span><span class="sxs-lookup"><span data-stu-id="f7f4d-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="f7f4d-106">Arbete som utförs på samma sätt som komplexitet eller tid på dygnet</span><span class="sxs-lookup"><span data-stu-id="f7f4d-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="f7f4d-107">Med tanke på att de olika attrubuten av arbete och de personer som krävs för att utföra arbetet finns det två typer av prisdimensionsvärden tillgängliga i Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="f7f4d-108">**Alternativuppsättningar**: - Attribut som är fasta uppräkningar för en uppsättning värden.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f7f4d-109">**Entitetbaserade värden** - attribut som kan ha en varierad uppsättning värden som är begränsade men kan ändras med tiden.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f7f4d-110">Prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="f7f4d-110">Pricing dimensions</span></span>

<span data-ttu-id="f7f4d-111">PSA levererar en standarduppsättning med prisdimensioner.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f7f4d-112">Du kan visa dessa genom att gå till **Project Service** > **parametrar**.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="f7f4d-113">I parameterposten, på fliken **Beloppsbaserad prissättningsdimension** ska du kontrollera att rollen **msdyn_resourcecategory** och resursorganisationsenheten **msdyn_organizationalunit** har fälten **Gäller för försäljning** och **Gäller för kostnad** inställd på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f7f4d-114">På så sätt kan du ange pris och kostnad för varje kombination av roll och organisationsenheter.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Skärmbild av parametrar för Project Service med "gäller för försäljning" markerad](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="f7f4d-116">Om du har använt de här fälten som roll- och organisationsenhet som prissättningsdimensioner före version 3 av PSA-versionen kommer det inte att finnas någon observerbar förändring.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="f7f4d-117">Du kan fortsätta att använda Project Service som vanligt.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="f7f4d-118">Om du behöver pris eller kostnad för dina resurser med hjälp av ytterligare attribut kan du skapa anpassade fält, entiteter och dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f7f4d-119">Mer information finns i följande avsnitt: Tänk dock på att du måste genomföra procedurerna i nedanstående ordning:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="f7f4d-120">Skapa anpassade fält och entiteter</span><span class="sxs-lookup"><span data-stu-id="f7f4d-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="f7f4d-121">Lägg till anpassade fält i prisinställning och transaktionella entiteter</span><span class="sxs-lookup"><span data-stu-id="f7f4d-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="f7f4d-122">Konfigurera anpassade fält som prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="f7f4d-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="f7f4d-123">Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="f7f4d-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="f7f4d-124">Prissättning av mänsklig resurs</span><span class="sxs-lookup"><span data-stu-id="f7f4d-124">Pricing human resource time</span></span>
<span data-ttu-id="f7f4d-125">Hur en organisation prissätter mänsklig resurs är ofta ett viktigt strategiskt övervägande som påverkar organisationens lönsamhet direkt.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f7f4d-126">Arbeta med ekonomiteamen och övningsrubriker när organisationen är klar att identifiera hur fakturering och kostnader för personaltid ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f7f4d-127">Andra faktorer för prissättningen är om återanvända fält eller entiteter som inte för närvarande är prissättningsdimensioner men som används som prissättningsdimensioner för organisationen.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f7f4d-128">Fält som **transaktionskategori** (**msdyn_transactioncategory**) och **bokningsbar resurs** (**bookableresource**) är exempel på sökande dimensioner.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f7f4d-129">Fundera över om prissättningsdimensionen ska vara en tabell eller en alternativuppsättning.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f7f4d-130">Om du förväntar dig ändringar av värden i en dimension som blir större än 10 eller 12 och du behöver ytterligare attribut för dessa värden kan du skapa en entitet i stället för en alternativuppsättning.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="f7f4d-131">Om du underhåller en alternativuppsättning, t.ex. lägga till eller ta bort värden, krävs en administratör eller utvecklare för att kunna lägga till nya rader i en tabell kan utföras av de flesta företagsanvändare.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="f7f4d-132">I följande exempel visas faktureringskostnader som är inställda utifrån den roll och den resursorganisationsenhet som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f7f4d-133">Kostnadstariffer är vanligtvis baserade på den anställdes löneområde och den organisationsenhet de tillhör.</span><span class="sxs-lookup"><span data-stu-id="f7f4d-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f7f4d-134">I det här exemplet ser faktureringskursen och kostnadstabellerna ut på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="f7f4d-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f7f4d-135">**Exempel på faktureringskostnader**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-135">**Sample bill rates**</span></span>

| <span data-ttu-id="f7f4d-136">Roll</span><span class="sxs-lookup"><span data-stu-id="f7f4d-136">Role</span></span>        | <span data-ttu-id="f7f4d-137">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="f7f4d-137">Org Unit</span></span>    |<span data-ttu-id="f7f4d-138">Enhet</span><span class="sxs-lookup"><span data-stu-id="f7f4d-138">Unit</span></span>      |<span data-ttu-id="f7f4d-139">Pris</span><span class="sxs-lookup"><span data-stu-id="f7f4d-139">Price</span></span>      |<span data-ttu-id="f7f4d-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="f7f4d-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f7f4d-141">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="f7f4d-141">Developer</span></span>   | <span data-ttu-id="f7f4d-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f7f4d-142">Contoso US</span></span>  |<span data-ttu-id="f7f4d-143">Timme</span><span class="sxs-lookup"><span data-stu-id="f7f4d-143">Hour</span></span> | <span data-ttu-id="f7f4d-144">200</span><span class="sxs-lookup"><span data-stu-id="f7f4d-144">200</span></span>|<span data-ttu-id="f7f4d-145">USD</span><span class="sxs-lookup"><span data-stu-id="f7f4d-145">USD</span></span>     |
| <span data-ttu-id="f7f4d-146">Utvecklare</span><span class="sxs-lookup"><span data-stu-id="f7f4d-146">Developer</span></span>   | <span data-ttu-id="f7f4d-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f7f4d-147">Contoso India</span></span> |<span data-ttu-id="f7f4d-148">Timme</span><span class="sxs-lookup"><span data-stu-id="f7f4d-148">Hour</span></span>|   <span data-ttu-id="f7f4d-149">112</span><span class="sxs-lookup"><span data-stu-id="f7f4d-149">112</span></span>|<span data-ttu-id="f7f4d-150">USD</span><span class="sxs-lookup"><span data-stu-id="f7f4d-150">USD</span></span>     |


<span data-ttu-id="f7f4d-151">**Exempelkostnadstariffer**</span><span class="sxs-lookup"><span data-stu-id="f7f4d-151">**Sample cost rates**</span></span>

| <span data-ttu-id="f7f4d-152">Löneband</span><span class="sxs-lookup"><span data-stu-id="f7f4d-152">Salary Band</span></span>     | <span data-ttu-id="f7f4d-153">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="f7f4d-153">Org Unit</span></span>    |<span data-ttu-id="f7f4d-154">Enhet</span><span class="sxs-lookup"><span data-stu-id="f7f4d-154">Unit</span></span>      |<span data-ttu-id="f7f4d-155">Pris</span><span class="sxs-lookup"><span data-stu-id="f7f4d-155">Price</span></span>      |<span data-ttu-id="f7f4d-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="f7f4d-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f7f4d-157">Mitt företag_Band1</span><span class="sxs-lookup"><span data-stu-id="f7f4d-157">My company_Band1</span></span> | <span data-ttu-id="f7f4d-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f7f4d-158">Contoso US</span></span>  |<span data-ttu-id="f7f4d-159">Timme</span><span class="sxs-lookup"><span data-stu-id="f7f4d-159">Hour</span></span> | <span data-ttu-id="f7f4d-160">145</span><span class="sxs-lookup"><span data-stu-id="f7f4d-160">145</span></span>|<span data-ttu-id="f7f4d-161">USD</span><span class="sxs-lookup"><span data-stu-id="f7f4d-161">USD</span></span>     |
| <span data-ttu-id="f7f4d-162">Mitt företag_Band2</span><span class="sxs-lookup"><span data-stu-id="f7f4d-162">My company_Band2</span></span> | <span data-ttu-id="f7f4d-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f7f4d-163">Contoso India</span></span> |<span data-ttu-id="f7f4d-164">Timme</span><span class="sxs-lookup"><span data-stu-id="f7f4d-164">Hour</span></span>|   <span data-ttu-id="f7f4d-165">67</span><span class="sxs-lookup"><span data-stu-id="f7f4d-165">67</span></span>|<span data-ttu-id="f7f4d-166">USD</span><span class="sxs-lookup"><span data-stu-id="f7f4d-166">USD</span></span>     |
