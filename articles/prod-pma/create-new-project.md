---
title: Skapa ett nytt projekt
description: I det här ämnet finns information om hur du skapar ett nytt projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085675"
---
# <a name="create-a-new-project"></a><span data-ttu-id="bce71-103">Skapa ett nytt projekt</span><span class="sxs-lookup"><span data-stu-id="bce71-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bce71-104">Följ stegen nedan om du vill skapa ett nytt projekt.</span><span class="sxs-lookup"><span data-stu-id="bce71-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="bce71-105">På sidan **Projekthantering** välj **Ny projekt** och ange följande värden:</span><span class="sxs-lookup"><span data-stu-id="bce71-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="bce71-106">**Projekttyp:** tid och material</span><span class="sxs-lookup"><span data-stu-id="bce71-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="bce71-107">**Projektnamn:** XYZ uppgraderingsfas 2</span><span class="sxs-lookup"><span data-stu-id="bce71-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="bce71-108">**Projektgrupp:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="bce71-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="bce71-109">**Projektkontrakt-ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="bce71-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="bce71-110">Välj **Skapa projekt**.</span><span class="sxs-lookup"><span data-stu-id="bce71-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="bce71-111">Tilldela en resurs en projekt</span><span class="sxs-lookup"><span data-stu-id="bce71-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="bce71-112">På sidan **arbetare** i listan **arbetare** välj posten för den arbetare som du tidigare har ställt in kompetenser för och öppna arbetarposten.</span><span class="sxs-lookup"><span data-stu-id="bce71-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="bce71-113">I åtgärdsfönstret på fliken **Projekt** i gruppen **Inställning** välj **Tilldela projekt**.</span><span class="sxs-lookup"><span data-stu-id="bce71-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="bce71-114">På sidan **Tilldelning av resursvalideringsprojekt** på fliken **Projekt** i fältet **Lägg till projektet i utvalda projekt** i projektet **XYZ uppgradering fas 2**.</span><span class="sxs-lookup"><span data-stu-id="bce71-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="bce71-115">I fönstret **Återstående projekt** , välj ett projekt och välj sedan pilknappen för att lägga till det i rutan **Valda projekt**.</span><span class="sxs-lookup"><span data-stu-id="bce71-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="bce71-116">Du kan även tilldela kategorier för en resurs som du behöver.</span><span class="sxs-lookup"><span data-stu-id="bce71-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="bce71-117">Kategoritypen är antingen **kostnad** eller **intäkt**.</span><span class="sxs-lookup"><span data-stu-id="bce71-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="bce71-118">Kategoritypen bestäms av din organisation.</span><span class="sxs-lookup"><span data-stu-id="bce71-118">The category type is determined by your organization.</span></span> <span data-ttu-id="bce71-119">Om du inte har tilldelats några kategorier för en resurs slår Finance upp kategorin som standard för timkostnader för kostnader och intäkter.</span><span class="sxs-lookup"><span data-stu-id="bce71-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="bce71-120">Ange egenskaper för projektresurser och roller</span><span class="sxs-lookup"><span data-stu-id="bce71-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="bce71-121">En projektledare kan använda projektets källfunktioner för att skapa de roller som krävs för projektet.</span><span class="sxs-lookup"><span data-stu-id="bce71-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="bce71-122">Roller kan användas om bekräftade resurser fortfarande är okända när resurser reserveras.</span><span class="sxs-lookup"><span data-stu-id="bce71-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="bce71-123">Roller kan tillfälligt reserveras som planerade resurser så att du kan fortsätta med projektplaneringsfaserna.</span><span class="sxs-lookup"><span data-stu-id="bce71-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="bce71-124">[![Exempel på en roll](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="bce71-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="bce71-125">**Scenario:** Contoso anställdes för att slutföra ett tids- och materialprojekt som har en godkänd projektstadgar.</span><span class="sxs-lookup"><span data-stu-id="bce71-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="bce71-126">Juniorprojektledaren håller fortfarande på att slutföra projektets omfattning.</span><span class="sxs-lookup"><span data-stu-id="bce71-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="bce71-127">Resurshanteraren identifierar just nu specifika resurser som ska reserveras för att fungera i det nya projektet.</span><span class="sxs-lookup"><span data-stu-id="bce71-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="bce71-128">På grund av projektets kritiska karaktär begärde projektsponsor chefsprojektledare som en av rollerna.</span><span class="sxs-lookup"><span data-stu-id="bce71-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="bce71-129">Resurshanteraren måste skaffa den nya resursen och definiera rollen i systemet om oerfarna projektledare kräver resursinformationen under projektplanering.</span><span class="sxs-lookup"><span data-stu-id="bce71-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="bce71-130">I följande steg visas hur resurshanteraren kan konfigurera rollen som ansvarig för projektchefen och associera resursegenskaper med den.</span><span class="sxs-lookup"><span data-stu-id="bce71-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="bce71-131">Senare kan rollen användas för att söka efter tillgängliga resurser som matchar de begärda resurskompetenserna.</span><span class="sxs-lookup"><span data-stu-id="bce71-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="bce71-132">På sidan **Konfigurera roller** välj **Ny** och ange följande värden:</span><span class="sxs-lookup"><span data-stu-id="bce71-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="bce71-133">**Roll-ID:** chefsprojektledare</span><span class="sxs-lookup"><span data-stu-id="bce71-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="bce71-134">**Beskrivning:** chefsprojektledare</span><span class="sxs-lookup"><span data-stu-id="bce71-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="bce71-135">Välj **Skapa**.</span><span class="sxs-lookup"><span data-stu-id="bce71-135">Select **Create**.</span></span>
3. <span data-ttu-id="bce71-136">Välj rollen **Chefsprojektledare** och välj sedan **Konfigurera egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="bce71-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="bce71-137">I fältet **Egenskapstyp** välj **Färdighet**.</span><span class="sxs-lookup"><span data-stu-id="bce71-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="bce71-138">I fältet **Tillgängliga egenskaper** anger du den färdighet du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="bce71-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="bce71-139">I fältet **Egenskapstyp** välj **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="bce71-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="bce71-140">I fältet **Tillgängliga egenskaper** anger du den certifikattyp du vill söka efter.</span><span class="sxs-lookup"><span data-stu-id="bce71-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="bce71-141">Tilldela en projektresurs en projekt</span><span class="sxs-lookup"><span data-stu-id="bce71-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="bce71-142">På sidan **Alla projekt** välj **XYZ uppgradera fas 2** projekt.</span><span class="sxs-lookup"><span data-stu-id="bce71-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="bce71-143">På sidan **Projektgrupp och schemaläggning** välj **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="bce71-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="bce71-144">I fält **Roll** välj **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="bce71-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="bce71-145">Välj **Boka från kalendern**.</span><span class="sxs-lookup"><span data-stu-id="bce71-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="bce71-146">På sidan **Resurstillgänglighet** väljer du **Vyinställningar**.</span><span class="sxs-lookup"><span data-stu-id="bce71-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="bce71-147">På sida **Justera vyinställningarna** ange följande värden:</span><span class="sxs-lookup"><span data-stu-id="bce71-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="bce71-148">**Format för datumintervall:** dag</span><span class="sxs-lookup"><span data-stu-id="bce71-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="bce71-149">**Visa tillgänglighetsbeskrivningar:** Ja</span><span class="sxs-lookup"><span data-stu-id="bce71-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="bce71-150">**Visa resterande kapacitet:** Ja</span><span class="sxs-lookup"><span data-stu-id="bce71-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="bce71-151">Välj en resurs i listan över resurser.</span><span class="sxs-lookup"><span data-stu-id="bce71-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="bce71-152">Välj **Fast bokning** och **Full kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="bce71-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="bce71-153">Tilldela en resurs till en standardroll</span><span class="sxs-lookup"><span data-stu-id="bce71-153">Assign a resource to a default role</span></span>

<span data-ttu-id="bce71-154">Om du vill att projekt eller resurshanterare ska kunna öka detaljnivån ytterligare information om vilka resurser som kan reserveras för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="bce71-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="bce71-155">Du kan associera en standardroll med en befintlig resurs eller en nyligen hämtad resurs.</span><span class="sxs-lookup"><span data-stu-id="bce71-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="bce71-156">När till exempel Daniel har anställts har han erfarenheten och färdigheterna för rollen affärsanalytiker.</span><span class="sxs-lookup"><span data-stu-id="bce71-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="bce71-157">Resurshanteraren har tilldelat rollen som Daniels standardroll.</span><span class="sxs-lookup"><span data-stu-id="bce71-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="bce71-158">Därför lade resurshanteraren Daniel till i en pool av affärsanalytiker som är tillgängliga för att arbeta med projekt.</span><span class="sxs-lookup"><span data-stu-id="bce71-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="bce71-159">Vid resursreservationen kan projektledarna filtrera de rollresurser som är tillgängliga för arbete i projekt.</span><span class="sxs-lookup"><span data-stu-id="bce71-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="bce71-160">De kan använda den här informationen som ett kriterium när de utför beslutsanalys med flera villkor när resurser är uppfyllda.</span><span class="sxs-lookup"><span data-stu-id="bce71-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="bce71-161">De kan också lägga till andra resursegenskaper i filtret och söka efter resurser med specifika kunskaper, utbildning och erfarenheter för ett visst projekt.</span><span class="sxs-lookup"><span data-stu-id="bce71-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="bce71-162">**Scenario:** ett godkänt projekt har startats och rollen som chefsprojektledare reserverades som en planerad resurs under projektplaneringsfasen.</span><span class="sxs-lookup"><span data-stu-id="bce71-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="bce71-163">Resurshanteraren har nu skaffat en resurs för att kunna utföra rollen som chefsprojektledare.</span><span class="sxs-lookup"><span data-stu-id="bce71-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="bce71-164">På sidan **Resurslista** välj **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="bce71-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="bce71-165">På sidan **Resursroll** välj **Ny** och ange följande värden:</span><span class="sxs-lookup"><span data-stu-id="bce71-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="bce71-166">**Giltig från:** Ange aktuellt datum.</span><span class="sxs-lookup"><span data-stu-id="bce71-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="bce71-167">**Förfallodatum:** ange **aldrig**.</span><span class="sxs-lookup"><span data-stu-id="bce71-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="bce71-168">**Roll:** Ange **chefsprojektledare**.</span><span class="sxs-lookup"><span data-stu-id="bce71-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="bce71-169">Klicka på **Spara** och stäng sedan sidan.</span><span class="sxs-lookup"><span data-stu-id="bce71-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="bce71-170">På fliken **kompetenser** lägger du till kompetensen **ProjectMgmt** och **PMP** -intyg.</span><span class="sxs-lookup"><span data-stu-id="bce71-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
