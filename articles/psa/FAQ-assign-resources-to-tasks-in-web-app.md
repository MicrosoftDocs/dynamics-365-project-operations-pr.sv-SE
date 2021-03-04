---
title: Hur tilldelar jag en bokningsbar resurs till en uppgift i webbappen
description: En översikt över olika sätt att tilldela bokningsbara resurser.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146595"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="aa0be-103">Hur tilldelar jag en bokningsbar resurs till en aktivitet i webbappen (programmet Project Service v2.x)</span><span class="sxs-lookup"><span data-stu-id="aa0be-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="aa0be-104">Det finns två sätt att tilldela en resurs till en aktivitet i Project Service.</span><span class="sxs-lookup"><span data-stu-id="aa0be-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="aa0be-105">Du kan schemalägga en resurs som en teammedlem och sedan tilldela den till en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="aa0be-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="aa0be-106">Du kan också skapa en allmän teammedlem genom tilldelning av roller för uppgifter, skapa ett team och sedan uppfylla underlagskraven med en namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="aa0be-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="aa0be-107">Observera att om du vill tilldela en aktivitet en bokningsbar resurs så måste den bokningsbara teammedlemmen ha tillräckligt med tillgängliga bokningar.</span><span class="sxs-lookup"><span data-stu-id="aa0be-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="aa0be-108">Bokningsstatusen måste vara av bekräftelsetypen Fast bokning och med statusen Bekräftad.</span><span class="sxs-lookup"><span data-stu-id="aa0be-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="aa0be-109">Om det inte finns tillräckligt med bokningar för resursen kommer Project Service att ta bort tilldelningen och visa följande felmeddelande:</span><span class="sxs-lookup"><span data-stu-id="aa0be-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="aa0be-110">*Det gick inte att tilldela en resurs till aktiviteten - Följande resurs(er) har inte tillräckligt antal timmar bokade för projektet*</span><span class="sxs-lookup"><span data-stu-id="aa0be-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="aa0be-111">Boka en resurs som en teammedlem och tilldela sedan resursen till en aktivitet</span><span class="sxs-lookup"><span data-stu-id="aa0be-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="aa0be-112">Med den här metoden kan du lägga till en resurs i projektteamet och sedan tilldela uppgifter till resursen i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="aa0be-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="aa0be-113">Så här gör du detta:</span><span class="sxs-lookup"><span data-stu-id="aa0be-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="aa0be-114">Lägg till en ny teammedlem genom att välja **Nytt** i rutnätet för teammedlem.</span><span class="sxs-lookup"><span data-stu-id="aa0be-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="aa0be-115">Markera namnet på den bokningsbara resursen och ange en roll i fönstret Snabbregistrering av teammedlem.</span><span class="sxs-lookup"><span data-stu-id="aa0be-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="aa0be-116">Välj **Från**- och **Till**-datum.</span><span class="sxs-lookup"><span data-stu-id="aa0be-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="aa0be-117">![Skärmbild av lägga till teammedlem](media/FAQ-Resources-to-Tasks2-1.png "Skärmbild av lägga till teammedlem")</span><span class="sxs-lookup"><span data-stu-id="aa0be-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="aa0be-118">Välj en av följande tilldelningsmetoder för bokning av resursen:</span><span class="sxs-lookup"><span data-stu-id="aa0be-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="aa0be-119">**Full kapacitet** bokar resursens fulla kapacitet för angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="aa0be-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="aa0be-120">**Procentandelskapacitet** bokar resursen under en viss procentandel av resursens kapacitet för angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="aa0be-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="aa0be-121">**Efter timmar - fördela jämnt** bokar resursen under ett angivet antal timmar och fördelar tiden jämnt per dag under angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="aa0be-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="aa0be-122">**Efter timmar - Tidigareläggning** bokar resursen under ett angivet antal timmar och tidigarelägger timmarna per dag under angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="aa0be-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="aa0be-123">Välj inte **Ingen** eftersom detta lägger till resursen i teamet men inte skapar några bokningar som tar upp resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="aa0be-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="aa0be-124">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="aa0be-124">Select **Save**.</span></span>

    <span data-ttu-id="aa0be-125">Observera att tiderna för bokningen måste täcka insatstimmar och tidsintervall för de uppgifter som du tilldelar resursen till.</span><span class="sxs-lookup"><span data-stu-id="aa0be-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="aa0be-126">Om så inte är fallet kan du inte tilldela resursen till aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="aa0be-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="aa0be-127">Klicka på listrutan för resurscellen i uppgiftens uppdelade arbetsstruktur (WBS).</span><span class="sxs-lookup"><span data-stu-id="aa0be-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="aa0be-128">Därefter:</span><span class="sxs-lookup"><span data-stu-id="aa0be-128">Then:</span></span> 

    1. <span data-ttu-id="aa0be-129">Markera **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="aa0be-129">Select **Add**.</span></span>
    2. <span data-ttu-id="aa0be-130">Välj listrutan under **Resurser** och välj den teammedlem som du just skapade.</span><span class="sxs-lookup"><span data-stu-id="aa0be-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="aa0be-131">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa0be-131">Select **OK**.</span></span> <span data-ttu-id="aa0be-132">Teammedlemmen har nu tilldelats till aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="aa0be-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="aa0be-133">![Skärmbild av lägga till resurser med struktur](media/FAQ-Resources-to-Tasks2-2.png "Skärmbild av lägga till resurser med WBS")</span><span class="sxs-lookup"><span data-stu-id="aa0be-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="aa0be-134">I rutnätet för teammedlem visas summan av resursens tilldelade timmar under Tilldelade timmar.</span><span class="sxs-lookup"><span data-stu-id="aa0be-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="aa0be-135">Denna är mindre än eller lika med bokat antal timmar för resursen.</span><span class="sxs-lookup"><span data-stu-id="aa0be-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="aa0be-136">![Skärmbild av tilldelade timmar för en resurs](media/FAQ-Resources-to-Tasks2-3.png "Skärmbild av tilldelade timmar för en resurs")</span><span class="sxs-lookup"><span data-stu-id="aa0be-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="aa0be-137">Om den aktivitet som du försöker tilldela till resursen startas efter resursbokningarnas slutdatum kommer resursen inte att visas i listrutan.</span><span class="sxs-lookup"><span data-stu-id="aa0be-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="aa0be-138">Observera att du kan tilldela en resurs till fler timmar än deras bokade timmar om resursen har viss återstående, icke-tilldelad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="aa0be-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="aa0be-139">I det fallet kopplas resursen endast delvis till deras bokningar.</span><span class="sxs-lookup"><span data-stu-id="aa0be-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="aa0be-140">Du kan se dessa återstående, icke-tilldelade uppgiftstimmar genom att lägga till kolumnen Obemannade timmar i den uppdelade arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="aa0be-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="aa0be-141">Om resurser har tilldelats till deras bokade timmar (deras bokade timmar är lika med deras tilldelade timmar) visas följande felmeddelande när du försöker tilldela dem ytterligare uppgifter:</span><span class="sxs-lookup"><span data-stu-id="aa0be-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="aa0be-142">*Det gick inte att tilldela en resurs till aktiviteten - Följande resurs(er) har inte tillräckligt antal timmar bokade för projektet.*</span><span class="sxs-lookup"><span data-stu-id="aa0be-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="aa0be-143">Dessutom läggs den teammedlem som utgör förvald projektledare till i teamet utan bokningar när du skapar projektet, och kan heller inte tilldelas till en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="aa0be-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="aa0be-144">De visas inte i resurslistrutan för aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="aa0be-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="aa0be-145">Om du vill tilldela den här resursen måste du ta bort dem från teamet och sedan lägga till dem igen med en tilldelningsmetod som inte är "Ingen".</span><span class="sxs-lookup"><span data-stu-id="aa0be-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="aa0be-146">Orsaken till att de läggs till i teamet när projektet skapas är så att ett projekt har minst en projektgodkännare som standard.</span><span class="sxs-lookup"><span data-stu-id="aa0be-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="aa0be-147">Skapa en allmän teammedlem genom tilldelning av roller för uppgifter</span><span class="sxs-lookup"><span data-stu-id="aa0be-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="aa0be-148">Denna metod garanterar att resurser har tillräckligt med bokningar för aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="aa0be-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="aa0be-149">Först måste du skapa en platshållare eller generisk resurs som beskriver egenskaperna för den namngivna resurs du i slutändan vill ska arbeta med uppgifterna genom att skapa ett team efter tilldelning av roller till uppgifter.</span><span class="sxs-lookup"><span data-stu-id="aa0be-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="aa0be-150">Så här gör du detta:</span><span class="sxs-lookup"><span data-stu-id="aa0be-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="aa0be-151">Välj en uppgift i den uppdelade arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="aa0be-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="aa0be-152">Välj ikonen för listruta för **Tilldelad roll** i resurscellen.</span><span class="sxs-lookup"><span data-stu-id="aa0be-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="aa0be-153">Välj listrutan **Roll** och markera rollen för den generiska resursen.</span><span class="sxs-lookup"><span data-stu-id="aa0be-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="aa0be-154">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa0be-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="aa0be-155">![Skärmbild av använda WBS för att lägga till resurser](media/FAQ-Resources-to-Tasks2-4.png "Skärmbild av använda WBS för att lägga till resurser")</span><span class="sxs-lookup"><span data-stu-id="aa0be-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="aa0be-156">När du är klar med att tilldela roller för aktiviteterna i WBS markerar du **Skapa projektteam**.</span><span class="sxs-lookup"><span data-stu-id="aa0be-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="aa0be-157">Project Service skapar det lägsta antalet generiske teammedlemmar utifrån rollerna, söker organisationsenheter och organiserar projektkalendern genom att samla in aktivitetens tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="aa0be-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="aa0be-158">![Skärmbild på hur du skapar ett projektteam](media/FAQ-Resources-to-Tasks2-5.png "Skärmbild på hur du skapar ett projektteam")</span><span class="sxs-lookup"><span data-stu-id="aa0be-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="aa0be-159">I rutnätet Teammedlem ser du resurser av typen Allmän resurs, med namn på roll och befattning.</span><span class="sxs-lookup"><span data-stu-id="aa0be-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="aa0be-160">Om två resurser behövs för att en roll ska kunna slutföra arbetet skapar funktionen Skapa team två teammedlemmar och avgränsar dessa med hjälp av befattningens namn.</span><span class="sxs-lookup"><span data-stu-id="aa0be-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="aa0be-161">![Skärmbild av att lägga till två allmänna resurser](media/FAQ-Resources-to-Tasks2-6.png "Skärmbild av att lägga till två allmänna resurser")</span><span class="sxs-lookup"><span data-stu-id="aa0be-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="aa0be-162">Du kan öppna kravet på underliggande resurs för allmän teammedlem genom att välja länken under Resurskrav.</span><span class="sxs-lookup"><span data-stu-id="aa0be-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="aa0be-163">![Skärmbild av öppna krav för underliggande resurs](media/FAQ-Resources-to-Tasks2-7.png "Skärmbild av öppna krav för underliggande resurs")</span><span class="sxs-lookup"><span data-stu-id="aa0be-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="aa0be-164">Välj **Boka** för den generiska resursen. Du kan sedan använda schemaläggningstavlan för att söka efter och boka en riktig resurs.</span><span class="sxs-lookup"><span data-stu-id="aa0be-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="aa0be-165">Du kan också skicka in kravet för expediering av resursansvarig genom att välja **Skicka begäran**.</span><span class="sxs-lookup"><span data-stu-id="aa0be-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="aa0be-166">Om den generiska resursen har kompletterats med en namngiven resurs tas den generiska resursen bort från teamet, och aktivitetstilldelningarna för den generiska resursen tilldelas den namngivna resurs som uppfyllt den generiska resursens resurskrav.</span><span class="sxs-lookup"><span data-stu-id="aa0be-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

