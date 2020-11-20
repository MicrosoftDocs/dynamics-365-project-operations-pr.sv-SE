---
title: Tilldela en resurs till en uppgift
description: I det här ämnet finns information om hur du tilldelar resurser till uppgifter.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b7aef799ec4b90d602a6f3641cbac06264664f00
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125155"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="0258c-103">Tilldela en resurs till en uppgift</span><span class="sxs-lookup"><span data-stu-id="0258c-103">Assign a resource to a task</span></span>

<span data-ttu-id="0258c-104">Det finns tre sätt att tilldela en resurs till en aktivitet i Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0258c-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="0258c-105">Boka en resurs som en teammedlem och tilldela sedan resursen till en aktivitet</span><span class="sxs-lookup"><span data-stu-id="0258c-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="0258c-106">Du kan lägga till en resurs i projektteamet och sedan tilldela resursen till uppgifter i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="0258c-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="0258c-107">På fliken **teammedlem** lägger du till en ny teammedlem genom att välja **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="0258c-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="0258c-108">Då öppnas panelen för **snabbregistrering av teammedlem** där du kan markera bokningsbar resurs och ange en roll.</span><span class="sxs-lookup"><span data-stu-id="0258c-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="0258c-109">Välj en av följande tilldelningsmetoder för bokning av resursen:</span><span class="sxs-lookup"><span data-stu-id="0258c-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="0258c-110">**Full kapacitet** bokar resursens fulla kapacitet för angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="0258c-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="0258c-111">**Procentandelskapacitet** bokar resursen under en viss procentandel av resursens kapacitet för angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="0258c-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="0258c-112">**Efter timmar - fördela jämnt** bokar resursen under ett angivet antal timmar och fördelar dessa jämnt per dag under angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="0258c-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="0258c-113">**Efter timmar - Tidigareläggning** bokar resursen under ett angivet antal timmar och tidigarelägger timmarna per dag under angivna från- och till-datum.</span><span class="sxs-lookup"><span data-stu-id="0258c-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="0258c-114">**Ingen** lägger till resursen i teamet men skapar inga bokningar som tar upp kapacitet.</span><span class="sxs-lookup"><span data-stu-id="0258c-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="0258c-115">På rutnätet **Schemalägg** välj ikonen **Resurs** i resurscellen och under **teammedlem** markerar du den teammedlem du precis har lagt till.</span><span class="sxs-lookup"><span data-stu-id="0258c-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="0258c-116">På flikarna **Teammedlem** och **Avstämning** visar resursen bokade timmar och tilldelade timmar.</span><span class="sxs-lookup"><span data-stu-id="0258c-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="0258c-117">Timmarna bör vara desamma men behöver inte vara det, detta eftersom bokningar och tilldelningar inte är nära sammankopplade.</span><span class="sxs-lookup"><span data-stu-id="0258c-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="0258c-118">Fliken **Avstämning** ger dig information om huruvida de varierar, till exempel när du tilldelar en resurs fler timmar än du har bokat.</span><span class="sxs-lookup"><span data-stu-id="0258c-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="0258c-119">Om det behövs kan du korrigera denna information för att vidta korrigeringsåtgärder, antingen genom att utöka resursens bokningar eller ändra tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="0258c-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="0258c-120">Skapa en generisk teammedlem genom tilldelning av aktiveter</span><span class="sxs-lookup"><span data-stu-id="0258c-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="0258c-121">När du skapar en generisk teammedlem genom uppgiftstilldelning måste du skapa en platshållare eller generisk resurs som beskriver egenskaperna för den namngivna resurs du i slutändan vill ska arbeta med uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="0258c-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="0258c-122">Därefter skapar du ett krav (eller skickar in en begäran med hjälp av kravet) som används för att söka och boka den namngivna resursen.</span><span class="sxs-lookup"><span data-stu-id="0258c-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="0258c-123">I rutnätet **Schema** för en uppgift markerar du **Resurs** i resurscellen.</span><span class="sxs-lookup"><span data-stu-id="0258c-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="0258c-124">Ange ett namn som utgör resursnamnet för platshållaren.</span><span class="sxs-lookup"><span data-stu-id="0258c-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="0258c-125">Till exempel Programhanterare.</span><span class="sxs-lookup"><span data-stu-id="0258c-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="0258c-126">Välj **skapa** och ange rollen för den generiska resursen i fältet **Snabbregistering av projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="0258c-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="0258c-127">Du kan fortsätta att tilldela aktiviteter till denna platshållarresurs genom att välja resursen i aktivitetens **resursväljare**.</span><span class="sxs-lookup"><span data-stu-id="0258c-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="0258c-128">De är listade under **Teammedlemmar**.</span><span class="sxs-lookup"><span data-stu-id="0258c-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="0258c-129">När du är klar med att tilldela den generiska resursen markerar du den generiska resursen i **Team** och sedan **Generera krav** för att skapa ett resurskrav för den generiska resursen.</span><span class="sxs-lookup"><span data-stu-id="0258c-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="0258c-130">Välj **Boka** för den generiska resursen.</span><span class="sxs-lookup"><span data-stu-id="0258c-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="0258c-131">Du kan sedan använda schemaläggningstavlan för att hitta och boka en verklig resurs.</span><span class="sxs-lookup"><span data-stu-id="0258c-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="0258c-132">Du kan också skicka in kravet för expediering genom en resursansvarig.</span><span class="sxs-lookup"><span data-stu-id="0258c-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="0258c-133">Om den generiska resursen har kompletterats med en namngiven resurs tas den generiska resursen bort från teamet, och aktivitetstilldelningarna för den generiska resursen tilldelas den namngivna resurs som uppfyllt den generiska resursens resurskrav.</span><span class="sxs-lookup"><span data-stu-id="0258c-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="0258c-134">Tilldela en namngiven resurs från listan över alla bokningsbara resurser</span><span class="sxs-lookup"><span data-stu-id="0258c-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="0258c-135">Du kan använda sökrutan i **resursväljaren** för att söka efter alla bokningsbara resurser och tilldela dem till en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="0258c-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="0258c-136">Resurser som är tilldelade detta sätt läggs till i teamet utan att behöva boka.</span><span class="sxs-lookup"><span data-stu-id="0258c-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="0258c-137">Detta påminner om att lägga till en teammedlem och välja ingen som allokeringsmetod.</span><span class="sxs-lookup"><span data-stu-id="0258c-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="0258c-138">Resursen visas på flikarna **Team** och **Avstämning** som resurser med endast tilldelningar och ett bokningsunderskott.</span><span class="sxs-lookup"><span data-stu-id="0258c-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="0258c-139">Schemalägg dem om du vill använda deras tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="0258c-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="0258c-140">I rutnätet **Schema** för en uppgift markerar du **Resurs** i resurscellen.</span><span class="sxs-lookup"><span data-stu-id="0258c-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="0258c-141">Börja skriva ett namn.</span><span class="sxs-lookup"><span data-stu-id="0258c-141">Start typing a name.</span></span> <span data-ttu-id="0258c-142">Sökresultaten för namnet visas i resursväljaren under **resursväljaren** under **andra resurser**.</span><span class="sxs-lookup"><span data-stu-id="0258c-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="0258c-143">Välj resursen som du vill tilldela uppgiften.</span><span class="sxs-lookup"><span data-stu-id="0258c-143">Select the resource that you want to assign to the task.</span></span>

