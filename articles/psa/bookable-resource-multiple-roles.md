---
title: Uppskatta projektförsäljning och kostnader när en bokningsbar resurs fyller flera roller i ett projekt
description: I det här ämnet finns information om hur prissättningsdimensioner kan användas för att stödja prissättning och kostnadsberäkning för en resurs som fyller flera roller i ett projekt.
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
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085592"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="762b9-103">Uppskatta projektförsäljning och kostnader när en bokningsbar resurs fyller flera roller i ett projekt</span><span class="sxs-lookup"><span data-stu-id="762b9-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="762b9-104">Projektbaserade företag har ofta ett behov av att en resurs ska utföra flera roller i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="762b9-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="762b9-105">Var och en av dessa roller kan vara prissatta och utgiftsberäknade på olika sätt, vilket innebär att samma resurs tid i projektet kan få en särskild ekonomisk uppskattning beroende på fakturerings- och kostnadstaxor för varje roll.</span><span class="sxs-lookup"><span data-stu-id="762b9-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="762b9-106">Med Project Service Automation kan du konfigurera värden för teammedlemmens post för den namngivna resursen och tillåta olika åsidosättningar för varje uppgift som teammedlemmen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="762b9-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="762b9-107">I följande exempel förklaras hur en enkel åsidosättning av det här värdet tillåter en resurs att ha flera roller i ett projekt med olika kostnads- och faktureringstaxor.</span><span class="sxs-lookup"><span data-stu-id="762b9-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="762b9-108">Skapa uppgifter</span><span class="sxs-lookup"><span data-stu-id="762b9-108">Create tasks</span></span>
<span data-ttu-id="762b9-109">Skapa två projektuppgifter på 40 timmar var. Uppgift A och uppgift B. Välj uppgift A som en föregående uppgift till uppgift B.</span><span class="sxs-lookup"><span data-stu-id="762b9-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="762b9-110">Ställ in roll och organisationsenhet för en allmän projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="762b9-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="762b9-111">På sidan **schema** välj raden **uppgift** för uppgift A.</span><span class="sxs-lookup"><span data-stu-id="762b9-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="762b9-112">I fältet **Resurser** , välj **Skapa** i den nedrullningsbara listan.</span><span class="sxs-lookup"><span data-stu-id="762b9-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="762b9-113">På sidan **Snabbregistrering av teammedlem** anger du attributen för den allmänna teammedlemmen som kan utföra uppgiften.</span><span class="sxs-lookup"><span data-stu-id="762b9-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="762b9-114">Markera lämplig roll och organisationsenhet och välj sedan **Spara och stäng**.</span><span class="sxs-lookup"><span data-stu-id="762b9-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="762b9-115">En allmän teammedlem skapas och tilldelas den här uppgiften.</span><span class="sxs-lookup"><span data-stu-id="762b9-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="762b9-116">Upprepa stegen för uppgift B och kontrollera att rollen och organisationsenheterna i den allmänna teammedlemmen som har skapats för uppgift B skiljer sig från uppgift A.</span><span class="sxs-lookup"><span data-stu-id="762b9-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="762b9-117">Ställ in roll och organisationsenhet för en projektuppgift</span><span class="sxs-lookup"><span data-stu-id="762b9-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="762b9-118">När du har skapat uppgiften A markerar du uppgiften och väljer **Redigera uppgift**.</span><span class="sxs-lookup"><span data-stu-id="762b9-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="762b9-119">På sidan **uppgiftsinformation** hitta fälten **roll** och **organisationsenhet** och lägg till de värden som krävs för en resurs som skulle utföra denna uppgift.</span><span class="sxs-lookup"><span data-stu-id="762b9-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="762b9-120">Om du genomför de här scenarierna med hjälp av information om demonstrations data för Project Service Automation kan du välja **rådgivningslead** för rollen och **Fabrikam US** som organisationsenhet.</span><span class="sxs-lookup"><span data-stu-id="762b9-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="762b9-121">Välj uppgift B och välj sedan **redigera uppgift**.</span><span class="sxs-lookup"><span data-stu-id="762b9-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="762b9-122">På sidan **uppgiftsinformation** hitta fälten **roll** och **organisationsenhet** och lägg till de värden som krävs för en resurs som skulle utföra denna uppgift.</span><span class="sxs-lookup"><span data-stu-id="762b9-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="762b9-123">Kontrollera att värdena i fälten **roll** och **organisationsenhet** är olika i uppgift B från de för uppgift A.</span><span class="sxs-lookup"><span data-stu-id="762b9-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="762b9-124">Om du genomför de här scenarierna med hjälp av information om demonstrations data för Project Service Automation kan du välja **nätverkstekniker** för rollen och **Fabrikam US** som organisationsenhet.</span><span class="sxs-lookup"><span data-stu-id="762b9-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="762b9-125">Spara och stäng sidan **uppgiftsinformation**.</span><span class="sxs-lookup"><span data-stu-id="762b9-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="762b9-126">Teammedlem och uppskatta beteende</span><span class="sxs-lookup"><span data-stu-id="762b9-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="762b9-127">På sidan **uppgiftsinformation** i **teammedlem** välj de två generiska teammedlemmarna och välj sedan **generera krav**.</span><span class="sxs-lookup"><span data-stu-id="762b9-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="762b9-128">Detta kommer att generera resurskrav.</span><span class="sxs-lookup"><span data-stu-id="762b9-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="762b9-129">Välj en rad i teammedlemmen för **rådgivningslead** och välj sedan **boka**.</span><span class="sxs-lookup"><span data-stu-id="762b9-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="762b9-130">Schemaläggningstavlan öppnas och bokar en resurs för det kravet.</span><span class="sxs-lookup"><span data-stu-id="762b9-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="762b9-131">Välj en rad i teammedlemmen för **nätverkstekniker** och välj sedan **boka**.</span><span class="sxs-lookup"><span data-stu-id="762b9-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="762b9-132">Schemaläggningstavlan öppnas och bokar samma resurs öppnas på det kravet.</span><span class="sxs-lookup"><span data-stu-id="762b9-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="762b9-133">Rutnät för teammedlem</span><span class="sxs-lookup"><span data-stu-id="762b9-133">Team Member grid</span></span> 
<span data-ttu-id="762b9-134">I rutnätet **Teammedlem** märker du att de två generiska teammedlemsposterna tas bort och att de har ersatts med en resurs.</span><span class="sxs-lookup"><span data-stu-id="762b9-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="762b9-135">Det finns en uppsättning värden för den resursen som visar en standarduppsättning med värden för **roll** och **organisationsenhet**.</span><span class="sxs-lookup"><span data-stu-id="762b9-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="762b9-136">När du expanderar raden i den teammedlemmens post kan du se enskilda tilldelningar för de båda uppgifterna i teammedlemmen.</span><span class="sxs-lookup"><span data-stu-id="762b9-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="762b9-137">Varje tilldelningsrad har uppgifter om specifika värden för **roll** och **organisationsenhet**.</span><span class="sxs-lookup"><span data-stu-id="762b9-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="762b9-138">Beräkningsrutnät</span><span class="sxs-lookup"><span data-stu-id="762b9-138">Estimates grid</span></span> 
<span data-ttu-id="762b9-139">När du navigerar till rutnätet **beräkning** kommer du att lägga märke till att båda tilldelningarna för samma resurs är olika.</span><span class="sxs-lookup"><span data-stu-id="762b9-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="762b9-140">Tilldelningen för resursens uppgift A är prissatt med hjälp av attributvärdet för **Roll** för **Rådgivningslead**.</span><span class="sxs-lookup"><span data-stu-id="762b9-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="762b9-141">Tilldelningen för sanna resurs för uppgift B är prissatt med hjälp av attributvärdet för **Roll** för **nätverkstekniker**.</span><span class="sxs-lookup"><span data-stu-id="762b9-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





