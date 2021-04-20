---
title: Hantera projektprislistor i projektkontrakt
description: I det här ämnet finns information om hur du hanterar projektprislistor i projektkontrakt.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858585"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="af6a6-103">Hantera projektprislistor i projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="af6a6-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="af6a6-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="af6a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af6a6-105">Projektkontrakt i Dynamics 365 Project Operations är utformade för att stödja flera prislistor för försäljningsdatum i ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="af6a6-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="af6a6-106">I Project Operations finns det en ny associerad entitet som kallas **projektprislistor**.</span><span class="sxs-lookup"><span data-stu-id="af6a6-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="af6a6-107">Entiteten har en 1:n-relation till ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="af6a6-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="af6a6-108">Projektprislistor används för pristransaktioner med tid, material och utgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="af6a6-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="af6a6-109">När ett kontrakt offert har en eller flera projektprislistor används dessa prislistor för pristid, material, kostnader och faktiska värden för projekt som är associerade med kontraktet via kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="af6a6-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="af6a6-110">När det inte finns några projektprislistor på ett projektavtal ser du ett varningsmeddelande om att det inte finns några projektprislistor och dina uppskattningar, faktiska projektarbete, material och inloggade kostnader kommer inte att prissättas.</span><span class="sxs-lookup"><span data-stu-id="af6a6-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="af6a6-111">Det kommer inte att finnas något pris för försäljningsvärden.</span><span class="sxs-lookup"><span data-stu-id="af6a6-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="af6a6-112">Associera eller ta bort associationen för en projekt prislista till ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="af6a6-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="af6a6-113">Skapa eller associera en specifik prislista för projektbaserat arbete, material och utgifter</span><span class="sxs-lookup"><span data-stu-id="af6a6-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="af6a6-114">I projektkontraktet, välj fliken **Projektprislistor**.</span><span class="sxs-lookup"><span data-stu-id="af6a6-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="af6a6-115">Välj i delnätet **+ Lägg till ny projektprislista**.</span><span class="sxs-lookup"><span data-stu-id="af6a6-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="af6a6-116">I skjutreglaget **Snabbregistrering** välj en prislista.</span><span class="sxs-lookup"><span data-stu-id="af6a6-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="af6a6-117">I den nedrullningsbara listan visas alla prislistor som har kontexten inställd på **försäljning**, där valutan i prislistan överensstämmer med valutan i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="af6a6-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="af6a6-118">Ange en beskrivning av kopplingen till prislistan för projekt, välj **Spara** och stäng sedan reglaget **Snabbregistrering**.</span><span class="sxs-lookup"><span data-stu-id="af6a6-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="af6a6-119">En koppling till projektprislistan skapas.</span><span class="sxs-lookup"><span data-stu-id="af6a6-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="af6a6-120">Upprepa steg 1-4 om du vill associera fler än en projektprislista till projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="af6a6-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="af6a6-121">Skapa endast flera projektprislistor om du har olika giltighetsdatum för de associerade projektprislistorna.</span><span class="sxs-lookup"><span data-stu-id="af6a6-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="af6a6-122">Project Operations stöder inte överlappande giltighetsdatum för projektprislistorna.</span><span class="sxs-lookup"><span data-stu-id="af6a6-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="af6a6-123">Om det finns flera projektprislistor för en transaktion med ett visst datum blir priset på den transaktionen standard till noll.</span><span class="sxs-lookup"><span data-stu-id="af6a6-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="af6a6-124">Ta bort en association för projektprislista</span><span class="sxs-lookup"><span data-stu-id="af6a6-124">Remove a project price list association</span></span>

- <span data-ttu-id="af6a6-125">Markera projektprislistan och välj sedan **ta bort kontraktprojekt prislista** i underrutnätet.</span><span class="sxs-lookup"><span data-stu-id="af6a6-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="af6a6-126">Prislistan tas bort från projekt prislistorna för kontraktet.</span><span class="sxs-lookup"><span data-stu-id="af6a6-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="af6a6-127">Själva prislistan tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="af6a6-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="af6a6-128">Endast associationen till kontraktet kommer att tas bort.</span><span class="sxs-lookup"><span data-stu-id="af6a6-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="af6a6-129">Ange automatisk standard av projekt prislistor för ett kontrakt</span><span class="sxs-lookup"><span data-stu-id="af6a6-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="af6a6-130">En projektprislista kan anges som standardprislista för projekt.</span><span class="sxs-lookup"><span data-stu-id="af6a6-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="af6a6-131">Med den här inställningen kan du se till att alla kontrakt i organisationen alltid börjar med en standardprislista för projekt för den prisperioden.</span><span class="sxs-lookup"><span data-stu-id="af6a6-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="af6a6-132">Konfigurera organisationens standard för projekt prislistor</span><span class="sxs-lookup"><span data-stu-id="af6a6-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="af6a6-133">Gå till **Inställningar** > **Allmän** och välj sedan **Parametrar**.</span><span class="sxs-lookup"><span data-stu-id="af6a6-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="af6a6-134">I listsida **Aktiva parametrar**, välj och dubbelklicka på posten för att öppna den.</span><span class="sxs-lookup"><span data-stu-id="af6a6-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="af6a6-135">Kontrollera att du inte klickar på ett fältvärde som är hyperlänk medan du dubbelklickar på.</span><span class="sxs-lookup"><span data-stu-id="af6a6-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="af6a6-136">På sidan **aktiva parametrar** välj fliken **prislista**. I ett underrutnät visas en lista över standardprislistor.</span><span class="sxs-lookup"><span data-stu-id="af6a6-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="af6a6-137">Det här är en lista över standardkostnads- och försäljningsprislistor.</span><span class="sxs-lookup"><span data-stu-id="af6a6-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="af6a6-138">Att ha en prislista för **Försäljning** här för varje valuta som du säljer i ser till att försäljningsprislistan är standard på alla kontrakt som du skapar för kunder som handlar i den här valutan.</span><span class="sxs-lookup"><span data-stu-id="af6a6-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="af6a6-139">Ställ in en kundspecifik projektprislista</span><span class="sxs-lookup"><span data-stu-id="af6a6-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="af6a6-140">Du kan också skapa kundspecifika projektprislistor när du har förhandlat fram ett huvudprisavtal med kunderna.</span><span class="sxs-lookup"><span data-stu-id="af6a6-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="af6a6-141">Gå till **Försäljning** > **Kunder**.</span><span class="sxs-lookup"><span data-stu-id="af6a6-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="af6a6-142">Välj den kund som har en särskild prislista i listan med aktiva konton.</span><span class="sxs-lookup"><span data-stu-id="af6a6-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="af6a6-143">Markera kundposten och öppna den och välj sedan fliken **projektprislistor**. I ett underrutnät visas en lista över projektprislistor som är specifika för kunden.</span><span class="sxs-lookup"><span data-stu-id="af6a6-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="af6a6-144">Skapa en ny association av prislista här om du vill ha en specifik projektprislista för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="af6a6-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="af6a6-145">Anpassad prissättning på ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="af6a6-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="af6a6-146">När du har skapat organisations- och kundspecifika standard prislistor skapas projektkontrakten automatiskt med de här kopplingarna av prislistorna i projekt.</span><span class="sxs-lookup"><span data-stu-id="af6a6-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="af6a6-147">Projektkontraktslistor i ett projektkontrakt kopieras dock alltid med datum- och kontraktnamn som bifogas till dem.</span><span class="sxs-lookup"><span data-stu-id="af6a6-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="af6a6-148">Konto- och projektledarna kan sedan göra ändringar i priser för kopiorna.</span><span class="sxs-lookup"><span data-stu-id="af6a6-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="af6a6-149">Dessa ändrade priser gäller endast för detta projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="af6a6-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
