---
title: Hantera resurser
description: I det här ämnet finns information om hur du hanterar resurser.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275020"
---
# <a name="manage-resources"></a><span data-ttu-id="16c6d-103">Hantera resurser</span><span class="sxs-lookup"><span data-stu-id="16c6d-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="16c6d-104">Dynamics 365 Project Service Automation innehåller en instrumentpanel för resurshantering som ger en grafisk översikt över resursbehov och utnyttjande i hela organisationen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="16c6d-105">Du kan använda diagrammen på den här instrumentpanelen för att visualisera följande information:</span><span class="sxs-lookup"><span data-stu-id="16c6d-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="16c6d-106">**Resursbehov** – diagrammet **aktiva resursbegäran** innehåller resurser som har skickats in.</span><span class="sxs-lookup"><span data-stu-id="16c6d-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="16c6d-107">Resurserna aggregeras antingen efter roll eller projekt.</span><span class="sxs-lookup"><span data-stu-id="16c6d-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="16c6d-108">**Ej skickad resursbehov**  – diagrammet **Otilldelat resursbehov** visar alla resurskrav som inte har skickats.</span><span class="sxs-lookup"><span data-stu-id="16c6d-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="16c6d-109">Den hjälper resursansvariga att visa behov som inte är fast och kan skickas via en resursförfrågan.</span><span class="sxs-lookup"><span data-stu-id="16c6d-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="16c6d-110">**Fakturerbar tid för den senaste veckan** – diagrammet **användning efter roll** visar procentandelen av organisationens faktiska fakturerbara användning efter roll mot den faktiska fakturerbara användning efter roll.</span><span class="sxs-lookup"><span data-stu-id="16c6d-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="16c6d-111">Om du vill göra diagrammet **Användning efter roll** tillgänglig skapar du ett jobb som kör arbetsflödet UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="16c6d-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="16c6d-112">Detta återkommande jobb körs var sjunde dag för att beräkna fakturerbart utnyttjande för de föregående sju dagarna.</span><span class="sxs-lookup"><span data-stu-id="16c6d-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="16c6d-113">Resultatet aggregeras efter roll.</span><span class="sxs-lookup"><span data-stu-id="16c6d-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="16c6d-114">Hantera projektteammedlemmar</span><span class="sxs-lookup"><span data-stu-id="16c6d-114">Manage project team members</span></span>

<span data-ttu-id="16c6d-115">Projektledarna kan använda resurshanterarens instrumentpanel för att hantera resurser i projekt.</span><span class="sxs-lookup"><span data-stu-id="16c6d-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="16c6d-116">De kan till exempel lägga till en gruppmedlem direkt i ett projekt och boka en grupp medlem för att uppfylla de resurskrav som har samlats upp av en generisk resurs.</span><span class="sxs-lookup"><span data-stu-id="16c6d-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="16c6d-117">Lägga till en teammedlem direkt i ett projekt</span><span class="sxs-lookup"><span data-stu-id="16c6d-117">Add a team member directly to a project</span></span>

<span data-ttu-id="16c6d-118">Om du vill lägga till en teammedlem direkt i ett projekt väljer du **Projekt** på sidan **Team** och väljer **Ny**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="16c6d-119">Dialogrutan **Snabbregistrering: Projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="16c6d-120">I den här dialogrutan kan du utföra de här uppgifterna:</span><span class="sxs-lookup"><span data-stu-id="16c6d-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="16c6d-121">**Boka en namngiven resurs** – i fältet **Bokningsbar resurs** anger du namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="16c6d-122">Välj sedan rollen, ange period och välj en allokeringsmetod.</span><span class="sxs-lookup"><span data-stu-id="16c6d-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="16c6d-123">Den namngivna resursen som du har valt läggs till i projektet med hjälp av den valda allokeringsregeln och resurskalendern.</span><span class="sxs-lookup"><span data-stu-id="16c6d-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="16c6d-124">**Lägg till en generisk resurs** – Lämna fältet **Bokningsbar resurs** tomt och välj sedan rollen, ange perioden och välj önskad allokeringsmetod.</span><span class="sxs-lookup"><span data-stu-id="16c6d-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="16c6d-125">En generisk resurs läggs till i teamet som en platshållare för att hålla efterfrågemönstret som används för att boka namngivna resurser i teamet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="16c6d-126">Kravet ställs i enlighet med projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="16c6d-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="16c6d-127">**Lägg till en namngiven resurs i teamet utan förbrukningsresurskapacitet** – Välj en resurs i fältet **bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="16c6d-128">Välj sedan period och välj **Ingen** som allokeringsmetod.</span><span class="sxs-lookup"><span data-stu-id="16c6d-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="16c6d-129">Resursen läggs till i teamet, men resursens kapacitet förbrukas inte via en bokning.</span><span class="sxs-lookup"><span data-stu-id="16c6d-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="16c6d-130">Boka en teammedlem som uppfyller resurskraven för en generisk resurs</span><span class="sxs-lookup"><span data-stu-id="16c6d-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="16c6d-131">I PSA kan du boka en generisk resurs i ett projektteam och du kan ange vilken kapacitet som krävs samt hur kapaciteten ska fördelas.</span><span class="sxs-lookup"><span data-stu-id="16c6d-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="16c6d-132">Du kan ange attribut som är associerade med den allmänna resursen i resursbehovet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="16c6d-133">Dessa attribut innehåller obligatoriska kunskaper, den prioriterade organisationsenheten och önskade resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="16c6d-134">Följ stegen nedan för att ange vilka kunskaper som krävs på en generisk resurs för en utvecklare.</span><span class="sxs-lookup"><span data-stu-id="16c6d-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="16c6d-135">På sidan **projekt** på fliken **team** väljer du **ny** för att boka en generisk resurs.</span><span class="sxs-lookup"><span data-stu-id="16c6d-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Allmänna resurser bokade i teamet](media/Resource-Management-image9.png)

2. <span data-ttu-id="16c6d-137">I vyn **Alla teammedlemmar** i kolumnen **Resurskrav** väljer du länk om du vill lägga till obligatoriska kunskaper för den generiska resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Kravlänk](media/Resource-Management-image10.png)

3. <span data-ttu-id="16c6d-139">På sidan **Resurskrav** som visas i rutnätet **Färdigheter** välj sedan ellipsen (**...**) och sedan **Lägg till ny kravegenskap** för att lägga till nödvändiga färdigheter för din utvecklare.</span><span class="sxs-lookup"><span data-stu-id="16c6d-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Kommandot Lägg till ny kravegenskap](media/Resource-Management-image11.png)

4. <span data-ttu-id="16c6d-141">I dialogrutan **Snabbregistrering: Kravegenskap** som visas väljer du önskad färdighet i fältet **egenskap**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="16c6d-142">I fältet **värderingsvärde** väljer du sedan önskad kompetensnivå för den färdigheten.</span><span class="sxs-lookup"><span data-stu-id="16c6d-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="16c6d-143">Slutligen, i fältet **Resurskrav** anger du behovet av källresurser från organisationsenheter eller till och med namngivna resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="16c6d-144">När du är klar väljer du **Spara**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-144">When you've finished, select **Save**.</span></span>

    ![Snabbregistrering: dialogrutan kravegenskap](media/Resource-Management-image12.png)

5. <span data-ttu-id="16c6d-146">På sidan **Resurskrav**, välj **Boka** för att uppfylla resursbehovet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Knappen Boka på sidan Resurskrav](media/Resource-Management-image13.png)

    <span data-ttu-id="16c6d-148">Du kan också markera den allmänna resursen i rutnätet **alla teammedlemmar** och väljer sedan **boka**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Knappen Boka ovanför rutnätet Alla teammedlemmar](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="16c6d-150">I det här exemplet finns 40 obligatoriska timmar men inga egentliga timmar eftersom allmänna resurser inte har några bokningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="16c6d-151">Det finns inte heller några tilldelade timmar eftersom den allmänna resursen lades till direkt i teamet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="16c6d-152">Du lades inte till med hjälp av tilldelning av uppgifter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="16c6d-153">På sidan **schemaläggningsassistent** kan du filtrera tillgängliga resurser utifrån de krav som anges i resursbehovet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="16c6d-154">Resurserna sorteras enligt de sorteringsparametrar som anges på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="16c6d-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Sidan Schemaläggningsassistenten](media/Resource-Management-image15.png)

    <span data-ttu-id="16c6d-156">Här följer några filter som ofta används:</span><span class="sxs-lookup"><span data-stu-id="16c6d-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="16c6d-157">**Egenskaper tillsammans med en värdering** – filtrera efter kunskaper, certifieringar och andra resurser, samt bedömningar av kompetenser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="16c6d-158">**Roller** – filtrera efter de standardroller som tilldelas bokningsbara resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="16c6d-159">**Organisationsenheter** – filtrera bokningsbara resurser efter de organisationsenheter de är tilldelade till.</span><span class="sxs-lookup"><span data-stu-id="16c6d-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="16c6d-160">Om du inte är nöjd med resultatet av den första kravsökningen kan du ändra filtervillkoren.</span><span class="sxs-lookup"><span data-stu-id="16c6d-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="16c6d-161">Expandera rutan **filtervy** till vänster och välj sedan **Sök** efter ytterligare resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Fönstret Filtervy](media/Resource-Management-image16.png)

7. <span data-ttu-id="16c6d-163">Om du vill ändra hur resultatet sorteras väljer du **sortera**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Kommandot Sortera](media/Resource-Management-image17.png)

8. <span data-ttu-id="16c6d-165">Välj resurser enligt den begäran som anges på kravet, som anges längst upp på rutnätet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="16c6d-166">Du kan radera urvalet av celler i rutnätet och låta den öppna resurskapaciteten vara öppen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="16c6d-167">Det går bara att markera en resurs åt gången som bokad.</span><span class="sxs-lookup"><span data-stu-id="16c6d-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="16c6d-168">Välj **boka** om du vill boka den valda resursen och låta schemaläggningstavlan vara öppen så att du kan välja ytterligare resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="16c6d-169">Du kan också välja **Boka och avsluta** om du vill boka den valda resursen och stänga schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="16c6d-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Resurs att boka](media/Resource-Management-image19.png)

    <span data-ttu-id="16c6d-171">Du får ett meddelande om bokade timmar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="16c6d-172">Begäranindikatorerna illustrerar hur mycket av bokningskravet som är uppfyllt och hur mycket som återstår.</span><span class="sxs-lookup"><span data-stu-id="16c6d-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="16c6d-173">Du kan också se hur mycket av den valda resurskapaciteten som förbrukas.</span><span class="sxs-lookup"><span data-stu-id="16c6d-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="16c6d-174">Välj **expandera** om du vill visa mer information om resursbokningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="16c6d-175">Gå tillbaka till vyn **Alla teammedlemmar**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="16c6d-176">Observera att den allmänna resursen i rutnätet har ersatts av den namngivna resursen och 40 timmar har ställts in som bokad för resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Uppdaterat rutnätet för alla teammedlemmar](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="16c6d-178">Inga timmar visas eftersom de har bokats direkt i teamet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="16c6d-179">De har inte bokats med hjälp av tilldelning av uppgifter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="16c6d-180">Tilldela allmänna resurser till uppgifter och generera resurskrav</span><span class="sxs-lookup"><span data-stu-id="16c6d-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="16c6d-181">Du kan skapa uppgifter i PSA och sedan tilldela dem allmänna resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="16c6d-182">På det här sättet kan resursbehovet representeras av platshållare samtidigt som du uppskattar ditt schema och finansiell numrering.</span><span class="sxs-lookup"><span data-stu-id="16c6d-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="16c6d-183">Du kan sedan generera resurskrav för de allmänna resurserna och uppfylla dem.</span><span class="sxs-lookup"><span data-stu-id="16c6d-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="16c6d-184">På sidan **projekt** på fliken **schema** väljer du **lägg till** för att skapa en uppgift.</span><span class="sxs-lookup"><span data-stu-id="16c6d-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Ny uppgift skapad](media/Resource-Management-image21.png)

2. <span data-ttu-id="16c6d-186">I fältet **Resurser**, välj symbolen **Resursväljare**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="16c6d-187">Resursväljaren visas och visar befintliga teammedlemmar för projektet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Resursväljare](media/Resource-Management-image22.png)

3. <span data-ttu-id="16c6d-189">Ange namnet på den nya generiska resursen och välj sedan **skapa**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Namnet på en ny generisk resurs angavs](media/Resource-Management-image23.png)

4. <span data-ttu-id="16c6d-191">I dialogrutan **Snabbregistrering: Projektteammedlem** som visas väljer du roll för generisk resurs i fältet **roll**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="16c6d-192">I fältet **Resursenhet** väljer du organisationsenhet för den generiska resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="16c6d-193">Välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-193">Then select **Save**.</span></span>

    ![Snabbregistrering: dialogrutan Projektteammedlem.](media/Resource-Management-image24.png)

    <span data-ttu-id="16c6d-195">Den generiska teammedlemmen har nu tilldelats till aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="16c6d-195">The generic team member is now assigned to the task.</span></span>

    ![Den generiska teammedlemmen har tilldelats till aktiviteten.](media/Resource-Management-image25.png)

    <span data-ttu-id="16c6d-197">På fliken **team** visas den nya generiska teammedlemmen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="16c6d-198">Observera att det endast har tilldelats timmar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="16c6d-199">De här timmarna är summan av alla uppgifter som är tilldelade till den generiska teammedlemmen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="16c6d-200">Den generiska teammedlemmen har ännu inte krävt några timmar eller ett resurskrav.</span><span class="sxs-lookup"><span data-stu-id="16c6d-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Generisk teammedlem på fliken team](media/Resource-Management-image26.png)

5. <span data-ttu-id="16c6d-202">Du kan nu tilldela den generiska teammedlemmen till andra uppgifter med hjälp av resursväljaren.</span><span class="sxs-lookup"><span data-stu-id="16c6d-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Generisk team medlem i resursväljaren](media/Resource-Management-image27.png)

    <span data-ttu-id="16c6d-204">När du har tilldelat generisk resurs till uppgiften kan du skapa ett resurskrav för den generiska resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="16c6d-205">På fliken **Team**, välj den generiska resursen och välj sedan **generera krav**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Kommandot Generera krav](media/Resource-Management-image28.png)

    <span data-ttu-id="16c6d-207">När kravet skapas får den generiska teammedlemmen obligatoriska timmar och en länk för resurskravet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Länk för resurskrav](media/Resource-Management-image29.png)

    <span data-ttu-id="16c6d-209">När du har bokat en namngiven resurs tas den allmänna resursen bort från teamet och ersätts av den namngivna resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Den generiska resursen ersätts av den namngivna resursen](media/Resource-Management-image30.png)

    <span data-ttu-id="16c6d-211">På fliken **Schema** tas den generiska resurstilldelningar och ersätts av den namngivna resursen på fliken schema.</span><span class="sxs-lookup"><span data-stu-id="16c6d-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Generiska resurstilldelningar som ersätts av den namngivna resursen på fliken schema.](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="16c6d-213">Det här problemet uppstår endast när en namngiven resurs är helt bokad för generiska resurskrav.</span><span class="sxs-lookup"><span data-stu-id="16c6d-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="16c6d-214">När en namngiven resurs delvis ersätter det generiska resurs behovet eller flera namngivna resurser ersätter det allmänna resurs behovet, förblir den allmänna resursen tilldelad aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="16c6d-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="16c6d-215">I följande bild har en 80-timmars uppgift planerats för en varaktighet på fem dagar (16 timmar per dag över fem dagar) och tilldelats den generiska resurs som kallas **funktionell**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-timmars, fem dagars uppgift tilldelad till den funktionella generiska resursen](media/Resource-Management-image32.png)

    <span data-ttu-id="16c6d-217">När du genererar kravet är det för 80 timmar i fem dagar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Krav som genereras för 80 timmar i fem dagar](media/Resource-Management-image33.png)

    <span data-ttu-id="16c6d-219">Eftersom tillgängliga resurser endast arbetar åtta timmar per dag krävs det två resurser för att uppfylla kravet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Andra resursen](media/Resource-Management-image35.png)

    <span data-ttu-id="16c6d-221">På fliken **team** kan du nu se att den allmänna resursen inte har några obligatoriska timmar, men att de tilldelade timmarna fortfarande visas tillsammans med de två namngivna resurser som utgör uppfyllandet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Två namngivna resurser på fliken Team](media/Resource-Management-image36.png)

    <span data-ttu-id="16c6d-223">På fliken **schema** har den allmänna resursen fortfarande tilldelats uppgiften.</span><span class="sxs-lookup"><span data-stu-id="16c6d-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Generiska resurser på fliken Schema](media/Resource-Management-image37.png)

<span data-ttu-id="16c6d-225">PSA tilldelar inte båda resurserna till uppgiften eftersom det kan ge ett mindre förutsägbart schema.</span><span class="sxs-lookup"><span data-stu-id="16c6d-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="16c6d-226">I det här enkla exemplet är det enkelt att fördela timmarna lika mellan två resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="16c6d-227">I mer komplexa scenarier med flera uppgifter och flera resurser måste PSA emellertid göra antagandet om hur den bör allokera de bokningar som tas emot för flera resurser i flera olika uppgifter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="16c6d-228">Därför är projektledare är ansvarig för att analysera flera bokningar och tilldela dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="16c6d-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="16c6d-229">För att kunna allokera bokningarna tilldelas projektledaren uppgifterna från de allmänna resurserna till de namngivna resurserna och sedan används vyn **avstämning** för att se till att allokeringen fungerar med bokningarna.</span><span class="sxs-lookup"><span data-stu-id="16c6d-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="16c6d-230">Redigera ett resurskrav</span><span class="sxs-lookup"><span data-stu-id="16c6d-230">Edit a resource requirement</span></span>

<span data-ttu-id="16c6d-231">När ett resurskrav har skapats kan en projektledare eller en resursansvarig behöva redigera informationen för att förfina sökvillkoren när schemaläggningstavlan används.</span><span class="sxs-lookup"><span data-stu-id="16c6d-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="16c6d-232">Följ stegen nedan om du vill redigera resurskravet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="16c6d-233">På sidan **projekt** på fliken **team** väljer du länken till alla krav på en generisk resurs.</span><span class="sxs-lookup"><span data-stu-id="16c6d-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="16c6d-234">På sidan **resursbehov** som visas kan du uppdatera flera attribut.</span><span class="sxs-lookup"><span data-stu-id="16c6d-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="16c6d-235">Här följer några exempel:</span><span class="sxs-lookup"><span data-stu-id="16c6d-235">Here are some examples:</span></span>

    - <span data-ttu-id="16c6d-236">Namn</span><span class="sxs-lookup"><span data-stu-id="16c6d-236">Name</span></span>
    - <span data-ttu-id="16c6d-237">Från och med</span><span class="sxs-lookup"><span data-stu-id="16c6d-237">From Date</span></span>
    - <span data-ttu-id="16c6d-238">Hittills</span><span class="sxs-lookup"><span data-stu-id="16c6d-238">To Date</span></span>
    - <span data-ttu-id="16c6d-239">Varaktighet</span><span class="sxs-lookup"><span data-stu-id="16c6d-239">Duration</span></span>
    - <span data-ttu-id="16c6d-240">Resurstyp</span><span class="sxs-lookup"><span data-stu-id="16c6d-240">Resource Type</span></span>

<span data-ttu-id="16c6d-241">På sidan **resurskrav** kan projektledaren eller resursansvarig även ange följande information:</span><span class="sxs-lookup"><span data-stu-id="16c6d-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="16c6d-242">Kompetens</span><span class="sxs-lookup"><span data-stu-id="16c6d-242">Skills</span></span>
- <span data-ttu-id="16c6d-243">Roller</span><span class="sxs-lookup"><span data-stu-id="16c6d-243">Roles</span></span>
- <span data-ttu-id="16c6d-244">Resursinställningar</span><span class="sxs-lookup"><span data-stu-id="16c6d-244">Resource preferences</span></span>
- <span data-ttu-id="16c6d-245">Prioriterade organisationsenheter</span><span class="sxs-lookup"><span data-stu-id="16c6d-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="16c6d-246">Uppdatera resursbokningar efter att de har bokats i ett projekt</span><span class="sxs-lookup"><span data-stu-id="16c6d-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="16c6d-247">När du har lagt till en allmän eller namngiven resurs i ett projektteam kan du ändra resursens bokföring.</span><span class="sxs-lookup"><span data-stu-id="16c6d-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="16c6d-248">På sidan **Projekt** på fliken **Team** väljer du en teammedlem och sedan **Underhåll bokningar**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Schemaläggningstavlan öppnas för den valda teammedlemmen](media/Resource-Management-image40.png)

    <span data-ttu-id="16c6d-250">Schemaläggningstavla visas och visar projektmedlemmens bokningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="16c6d-251">Expandera teammedlemmens post om du vill visa vilka tider som har bokats i projektet och andra projekt som konsumerar teammedlemmens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="16c6d-252">Välj och dra bokningen för att utöka eller förkorta den.</span><span class="sxs-lookup"><span data-stu-id="16c6d-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="16c6d-253">Dialogrutan **Skapa resursbokning** öppnas där du kan justera bokningen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialogrutan Skapa resursbokning](media/Resource-Management-image41.png)

3. <span data-ttu-id="16c6d-255">Högerklicka på bokningen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-255">Right-click the booking.</span></span> <span data-ttu-id="16c6d-256">Sedan kan du använda snabbmenyn för att utföra följande åtgärder:</span><span class="sxs-lookup"><span data-stu-id="16c6d-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="16c6d-257">Ändra bokningsstatus.</span><span class="sxs-lookup"><span data-stu-id="16c6d-257">Change the booking status.</span></span>
    - <span data-ttu-id="16c6d-258">Redigera bokningen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-258">Edit the booking.</span></span>
    - <span data-ttu-id="16c6d-259">Ersätt en resurs i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="16c6d-260">Ändra bokningsstatus</span><span class="sxs-lookup"><span data-stu-id="16c6d-260">Change the booking status</span></span>

<span data-ttu-id="16c6d-261">Du kan ändra vilken status som helst för alla standard- eller anpassade bokningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-261">You can change any default or custom booking status.</span></span>

![Kommandot Ändra status](media/Resource-Management-image42.png)

<span data-ttu-id="16c6d-263">Följande statusar ingår i PSA:</span><span class="sxs-lookup"><span data-stu-id="16c6d-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="16c6d-264">**Annullerad** – den här statusen avbryter en resursbokning och frigör resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="16c6d-265">**Fast bokning** – den här statusen förbrukar en resurskapacitet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="16c6d-266">En bokning har vanligtvis denna status när du öppnar **Underhåll bokningar** från rutnätet **Alla teammedlemmar** på sidan **projekt**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="16c6d-267">**Preliminär bokning** – den här statusen lägger till en resurs i ett team, men förbrukar inte resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="16c6d-268">Den indikerar att resursen har reserverats för potentiellt arbete men fortfarande har kapacitet för andra jobb.</span><span class="sxs-lookup"><span data-stu-id="16c6d-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="16c6d-269">I vyn över övergripande resurstillgänglighet får preliminära bokningar annan status än fasta bokningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="16c6d-270">**Föreslagen** – denna status representerar resursansvariges eller projektledarens förslag för en resurs.</span><span class="sxs-lookup"><span data-stu-id="16c6d-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="16c6d-271">Förslag förbrukar inte resursens kapacitet och resursen läggs inte till i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="16c6d-272">Om du vill göra en fast bokning för resursen i teamet måste projektledaren godkänna förslaget.</span><span class="sxs-lookup"><span data-stu-id="16c6d-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="16c6d-273">Skicka resursbegäran</span><span class="sxs-lookup"><span data-stu-id="16c6d-273">Submit resource requests</span></span>

<span data-ttu-id="16c6d-274">Resursbegäran används för att bära en begäran (resurskrav) som måste uppfyllas av en resursansvarig.</span><span class="sxs-lookup"><span data-stu-id="16c6d-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="16c6d-275">För en generisk resurs som redan finns i teamet kan du skicka en resursbegäran direkt.</span><span class="sxs-lookup"><span data-stu-id="16c6d-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="16c6d-276">En resursbegäran kan uppfyllas på två sätt:</span><span class="sxs-lookup"><span data-stu-id="16c6d-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="16c6d-277">Resurshanteraren uppfyller direkt begäran.</span><span class="sxs-lookup"><span data-stu-id="16c6d-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="16c6d-278">I det här fallet ersätts den generiska resursen av en fast bokning med en namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="16c6d-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="16c6d-279">Resursansvarig föreslår en resurs för projektledaren och projektledaren godkänner eller avvisar den föreslagna resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="16c6d-280">Direkt uppfyllelse av resursbegäran</span><span class="sxs-lookup"><span data-stu-id="16c6d-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="16c6d-281">När ett resurskrav skapas kan en projektledare skicka en resursbegäran för en generisk resurs genom att välja resursen och sedan välja **skicka begäran**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Knappen Skicka begäran](media/Resource-Management-image45.png)

<span data-ttu-id="16c6d-283">Kommentarer om resursen kan ges till den resursansvarige som uppfyller begäran.</span><span class="sxs-lookup"><span data-stu-id="16c6d-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="16c6d-284">När begäran har skickats ändras fältet **status** för teammedlemmen till **skickad**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Ange valfria kommentarer](media/Resource-Management-image46.png)

<span data-ttu-id="16c6d-286">När resursansvarig fullföljer begäran ersätts den generiska teammedlemmen av den namngivna resursen i rutnätet **alla teammedlemmar**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![En generisk teammedlem som ersatts av den namngivna resursen i rutnätet alla teammedlemmar](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="16c6d-288">Använda ett resursförslag för resursbegäran</span><span class="sxs-lookup"><span data-stu-id="16c6d-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="16c6d-289">I stället för att direkt boka en resurs i en resursbegäran kan en resursansvarig föreslå projektresurs till projektledare.</span><span class="sxs-lookup"><span data-stu-id="16c6d-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="16c6d-290">En resursansvarig kan använda det här alternativet om en exakt matchning för kraven inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="16c6d-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="16c6d-291">När en resursansvarig föreslår en resurs ser projektledare fältet **status** för den allmänna teammedlemmen ändras till **Måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Den generiska teammedlemmens status ändras till Måste granskas](media/Resource-Management-image48.png)

<span data-ttu-id="16c6d-293">Om du vill visa den föreslagna resursen tillsammans med en visualisering av effekten av förslagets bokning, dubbelklickar du på den teammedlem som har statusvärdet **Måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="16c6d-294">Välj sedan fliken **föreslagna resurser**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-294">Then select the **Proposed Resources** tab.</span></span>

![Fliken Föreslagna resurser](media/Resource-Management-image49.png)

<span data-ttu-id="16c6d-296">Markera **acceptera alla förslag** för att acceptera alla föreslagna resurser eller **avvisa alla förslag** för att avvisa dem.</span><span class="sxs-lookup"><span data-stu-id="16c6d-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="16c6d-297">Om du accepterar de föreslagna resurserna är de fast bokade i projektet som teammedlemmar och ersätter generiska resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="16c6d-298">Du måste antingen acceptera eller avvisa alla föreslagna resurser.</span><span class="sxs-lookup"><span data-stu-id="16c6d-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="16c6d-299">Du kan inte delvis acceptera eller avvisa dem.</span><span class="sxs-lookup"><span data-stu-id="16c6d-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="16c6d-300">Ersätt en resurs i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="16c6d-301">Ibland måste en projektledare ersätta en teammedlem i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="16c6d-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="16c6d-302">På sidan **Projekt** på fliken **Team** väljer du den resurs som behöver en ersättning och sedan **Underhåll bokningar**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="16c6d-303">Expandera resursen om du vill visa de projekt som den är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="16c6d-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Resurs utökad för att visa tilldelade projekt](media/Resource-Management-image50.png)

3. <span data-ttu-id="16c6d-305">Högerklicka på projektet och välj sedan **Ersättningsresurs**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="16c6d-306">Om du känner till den resurs du vill ersätta den aktuella resursen med markerar du eller skriver namnet och väljer sedan **tilldela igen**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Ange en ersättningsresurs](media/Resource-Management-image51.png)

    <span data-ttu-id="16c6d-308">Du kan också söka efter en resurs genom att följa stegen nedan:</span><span class="sxs-lookup"><span data-stu-id="16c6d-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="16c6d-309">Välj **Sök ersättning**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-309">Select **Find Substitution**.</span></span>

        ![Söka efter en ersättningsresurs](media/Resource-Management-image52.png)

        <span data-ttu-id="16c6d-311">Schemaassistenten visar en lista över tillgängliga ersättningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="16c6d-312">I schemaläggningsassistenten kan du ytterligare filtrera tillgängliga resurser för att hitta en lämplig ersättare.</span><span class="sxs-lookup"><span data-stu-id="16c6d-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Lista över tillgängliga ersättare](media/Resource-Management-image53.png)

    2. <span data-ttu-id="16c6d-314">För att ersätta resursen, välj resursen och välj **ersättare**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Vald ersättningsresurs](media/Resource-Management-image54.png)

    <span data-ttu-id="16c6d-316">Bokningarna och tilldelningarna ersätts med den nya resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Bokningarna och tilldelningarna ersätts med den nya resursen.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="16c6d-318">Avstämning av bokningar och tilldelningar av teammedlemmar</span><span class="sxs-lookup"><span data-stu-id="16c6d-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="16c6d-319">För teammedlemmar kombineras inte bokningar och tilldelningar är löst kopplade.</span><span class="sxs-lookup"><span data-stu-id="16c6d-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="16c6d-320">Med andra ord kan resurser ha tilldelningar, men inga bokningar, eller så kan de inte ha bokningar men inga tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="16c6d-321">Vanligtvis justeras projektbokningar och tilldelningar så att resurserna har rätt kapacitet för att utföra sina aktivitetstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="16c6d-322">Bokningarna kan emellertid vara baserade på tillgänglighet, och tidsinställningar för aktiviteter kan ändras när projektet fortsätter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="16c6d-323">Därför är den fria kopplingen av bokningar och tilldelningar flexiblare.</span><span class="sxs-lookup"><span data-stu-id="16c6d-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="16c6d-324">PSA har fliken **avstämning** låter projektledarna avstämma teammedlemmarnas bokningar och deras tilldelningar för sina projektteam.</span><span class="sxs-lookup"><span data-stu-id="16c6d-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Fliken Avstämning](media/Resource-Management-image56.png)

<span data-ttu-id="16c6d-326">Fliken **avstämning** visar bokningar och tilldelningar ned till nivån för enskilda uppgiftstilldelningen för varje teammedlem.</span><span class="sxs-lookup"><span data-stu-id="16c6d-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="16c6d-327">Den visar antalet timmar i celler som kan representera tidsperioder från månader ned till dagar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="16c6d-328">Fliken visar även en total nettosumma för projektet tillsammans med en total kolumn.</span><span class="sxs-lookup"><span data-stu-id="16c6d-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="16c6d-329">För varje resurs beräknar fliken en skillnad mellan en teammedlems bokningar och sammanslagningen av teammedlemmens aktivitetstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="16c6d-330">Vi rekommenderar att skillnaden är 0 (noll).</span><span class="sxs-lookup"><span data-stu-id="16c6d-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="16c6d-331">Det bör alltså inte finnas någon skillnad mellan bokningar och tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="16c6d-332">Skillnader är färgade och tonade för att framhäva två villkor:</span><span class="sxs-lookup"><span data-stu-id="16c6d-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="16c6d-333">**Underskott för bokning** – Underskott för bokning uppstår om en resurs har fler tilldelningar än bokningar.</span><span class="sxs-lookup"><span data-stu-id="16c6d-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="16c6d-334">Eftersom denna kapacitet inte har reserverats kan en projektledare korrigera problemet genom att utöka resursens bokningar så att underskottet täcks.</span><span class="sxs-lookup"><span data-stu-id="16c6d-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="16c6d-335">**Överflödiga bokningar** – Överflödiga bokningar inträffar när en resurs har bokats i projektet men inte tilldelats aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="16c6d-336">Det här tillståndet kan vara acceptabelt i de fall då resursen togs i projektet före tilldelning av uppgifter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="16c6d-337">I andra fall är inte resursen planerad att tilldelas till uppgifter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="16c6d-338">I så fall bör projektledaren överväga att annullera resursbokningarna så att kapaciteten kan användas för ett annat projekt.</span><span class="sxs-lookup"><span data-stu-id="16c6d-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="16c6d-339">I vissa fall kan du se en nettoskillnad i noll för en resurs (t.ex. månadsnivån) när du visar tid på en högre nivå än dag nivå (till exempel månadsnivån).</span><span class="sxs-lookup"><span data-stu-id="16c6d-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="16c6d-340">Om du visar tid på veckonivån kan du se att det finns tilldelningar på noll timmar och bokningar på 40 timmar under den första veckan men tilldelningar på 40 timmar och bokningar på noll timmar i den andra veckan i månaden.</span><span class="sxs-lookup"><span data-stu-id="16c6d-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="16c6d-341">Generellt synkroniseras bokningarna och tilldelningarna, men de skiljer sig från en vecka till nästa.</span><span class="sxs-lookup"><span data-stu-id="16c6d-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="16c6d-342">När du visar högre tidsnivåer visar har celler i fliken **avstämning** har en indikator som meddelar att det finns olikheter på lägre nivåer.</span><span class="sxs-lookup"><span data-stu-id="16c6d-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="16c6d-343">Genom att dubbelklicka i en cell kan du zooma in för att visa skillnaden.</span><span class="sxs-lookup"><span data-stu-id="16c6d-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="16c6d-344">Du kan sedan högerklicka för att zooma ut. Genom att välja en resurs och sedan använda kontrollen **nästa skillnad** i verktygsfältet i rutnätet kan du gå vidare till nästa skillnad mellan bokningar och tilldelningar för resursen.</span><span class="sxs-lookup"><span data-stu-id="16c6d-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="16c6d-345">Därefter kan du använda kontrollen **föregående skillnad** för att gå tillbaka.</span><span class="sxs-lookup"><span data-stu-id="16c6d-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="16c6d-346">Du kan också inaktivera skillnadsindikator och navigeringsbeteende under **inställningar**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Skillnadsindikator](media/Resource-Management-image57.png)

<span data-ttu-id="16c6d-348">I situationer där du har aktivitetstilldelningar för en resurs men inga bokningar, på sidan **Projekt** på fliken **Avstämning**, välj underskott för bokningen och sedan **utöka bokning**.</span><span class="sxs-lookup"><span data-stu-id="16c6d-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="16c6d-349">I dialogrutan **utöka bokning** visas och visar den bokning som behövs för att lösa resursens underskott.</span><span class="sxs-lookup"><span data-stu-id="16c6d-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="16c6d-350">Den visar även resursens befintliga bokningar för alla projekt eller andra schemalagda entiteter.</span><span class="sxs-lookup"><span data-stu-id="16c6d-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="16c6d-351">Om du väljer **OK** för att skapa bokningen för resursen, oavsett resursens tillgänglighet, kan det leda till överbokning.</span><span class="sxs-lookup"><span data-stu-id="16c6d-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialogrutan utöka bokning](media/Resource-Management-image58.png)

<span data-ttu-id="16c6d-353">Projektledaren eller resursansvarig kan sedan använda schemaläggningstavlan för att hantera alla situationer där en resurs har blivit överbokad utanför sin kapacitet.</span><span class="sxs-lookup"><span data-stu-id="16c6d-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]