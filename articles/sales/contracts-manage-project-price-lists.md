---
title: Hantera projektprislistor i projektkontrakt
description: I det här ämnet finns information om hur du hanterar projektprislistor i projektkontrakt.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278620"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="9f8a4-103">Hantera projektprislistor i projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="9f8a4-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="9f8a4-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="9f8a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9f8a4-105">Projektkontrakt i Dynamics 365 Project Operations är utformade för att stödja flera prislistor för försäljningsdatum i ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="9f8a4-106">I Project Operations finns det en ny associerad entitet som kallas **projektprislistor**.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="9f8a4-107">Entiteten har en 1:n-relation till ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="9f8a4-108">Projektprislistor används för att visa pris-, tids- och utgiftstransaktioner för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="9f8a4-109">När ett kontrakt har en eller flera projekt prislistor används de här prislistorna som priser för uppskattningar av tid och utgifter och faktiska värden för projekt som är associerade med kontraktet via kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="9f8a4-110">Om det inte finns några projekt prislistor i ett projektkontrakt visas ett varnings meddelande om att det inte finns några projektprislistor och att uppskattningar, projektarbete och utgifter inte ska vara prissatta.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="9f8a4-111">Det kommer inte att finnas något pris för försäljningsvärden.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="9f8a4-112">Associera eller ta bort associationen för en projekt prislista till ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="9f8a4-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="9f8a4-113">Skapa eller associera en specifik prislista för uppskattning av projektbaserade resurser och utgifter</span><span class="sxs-lookup"><span data-stu-id="9f8a4-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="9f8a4-114">I projektkontraktet, välj fliken **Projektprislistor**.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="9f8a4-115">Välj i delnätet **+ Lägg till ny projektprislista**.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="9f8a4-116">I skjutreglaget **Snabbregistrering** välj en prislista.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="9f8a4-117">I den nedrullningsbara listan visas alla prislistor som har kontexten inställd på **försäljning**, där valutan i prislistan överensstämmer med valutan i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="9f8a4-118">Ange en beskrivning av kopplingen till prislistan för projekt, välj **Spara** och stäng sedan reglaget **Snabbregistrering**.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="9f8a4-119">En koppling till projektprislistan skapas.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="9f8a4-120">Upprepa steg 1-4 om du vill associera fler än en projektprislista till projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="9f8a4-121">Skapa endast flera projektprislistor om du har olika giltighetsdatum för de associerade projektprislistorna.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="9f8a4-122">Project Operations stöder inte överlappande giltighetsdatum för projektprislistorna.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="9f8a4-123">Om det finns flera projektprislistor för en transaktion med ett visst datum blir priset på den transaktionen standard till noll.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="9f8a4-124">Ta bort en association för projektprislista</span><span class="sxs-lookup"><span data-stu-id="9f8a4-124">Remove a project price list association</span></span>

- <span data-ttu-id="9f8a4-125">Markera projektprislistan och välj sedan **ta bort kontraktprojekt prislista** i underrutnätet.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="9f8a4-126">Prislistan tas bort från projekt prislistorna för kontraktet.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="9f8a4-127">Själva prislistan tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="9f8a4-128">Endast associationen till kontraktet kommer att tas bort.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="9f8a4-129">Ange automatisk standard av projekt prislistor för ett kontrakt</span><span class="sxs-lookup"><span data-stu-id="9f8a4-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="9f8a4-130">Du kan ställa in en projekt prislista som standardlista i ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="9f8a4-131">Med hjälp av den här installationen kan du se till att alla kontrakt i organisationen alltid startas med en standard prislista för den prisperioden.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="9f8a4-132">Konfigurera organisationens standard för projekt prislistor</span><span class="sxs-lookup"><span data-stu-id="9f8a4-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="9f8a4-133">Gå till **Inställningar** > **Allmän** och välj sedan **Parametrar**.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="9f8a4-134">I listsida **Aktiva parametrar**, välj och dubbelklicka på posten för att öppna den.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="9f8a4-135">Kontrollera att du inte klickar på ett fältvärde som är hyperlänk medan du dubbelklickar på.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="9f8a4-136">På sidan **aktiva parametrar** välj fliken **prislista**. I ett underrutnät visas en lista över standardprislistor.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="9f8a4-137">Det här är en lista över standardkostnads- och försäljningsprislistor.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="9f8a4-138">Att ha en prislista för **Försäljning** här för varje valuta som du säljer i ser till att försäljningsprislistan är standard på alla kontrakt som du skapar för kunder som handlar i den här valutan.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="9f8a4-139">Ställ in en kundspecifik projektprislista</span><span class="sxs-lookup"><span data-stu-id="9f8a4-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="9f8a4-140">Du kan också skapa kundspecifika projektprislistor när du har förhandlat fram ett huvudprisavtal med kunderna.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="9f8a4-141">Gå till **Försäljning** > **Kunder**.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="9f8a4-142">Välj den kund som har en särskild prislista i listan med aktiva konton.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="9f8a4-143">Markera kundposten och öppna den och välj sedan fliken **projektprislistor**. I ett underrutnät visas en lista över projektprislistor som är specifika för kunden.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="9f8a4-144">Skapa en ny association av prislista här om du vill ha en specifik projektprislista för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="9f8a4-145">Anpassad prissättning på ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="9f8a4-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="9f8a4-146">När du har skapat organisations- och kundspecifika standard prislistor skapas projektkontrakten automatiskt med de här kopplingarna av prislistorna i projekt.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="9f8a4-147">Projektkontraktslistor i ett projektkontrakt kopieras dock alltid med datum- och kontraktnamn som bifogas till dem.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="9f8a4-148">Konto- och projektledarna kan sedan göra ändringar i priser för kopiorna.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="9f8a4-149">Dessa ändrade priser gäller endast för detta projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="9f8a4-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]