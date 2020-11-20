---
title: Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter
description: I det här ämnet finns information om hur man bokar namngivna resurser till projektteam och tilldelar dem till uppgifter.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130195"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="9ad26-103">Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter</span><span class="sxs-lookup"><span data-stu-id="9ad26-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9ad26-104">Du kan lägga till en namngiven resurs i projektteamet genom att boka dem direkt på teamet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="9ad26-105">Följ stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="9ad26-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="9ad26-106">I Project Service Automation, gå till **projekt** och välj de öppna projekt du bokar för.</span><span class="sxs-lookup"><span data-stu-id="9ad26-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="9ad26-107">På sidan **Projekt** på fliken **Team**, klicka på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9ad26-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Lägga till en teammedlem från fliken team](media/RM-how-to-1.png)

3. <span data-ttu-id="9ad26-109">I dialogrutan **Snabbregistrering av projektteammedlem** väljer du den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="9ad26-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="9ad26-110">Fältet **Roll** fylls i med resursens standardroll om de har en tilldelad.</span><span class="sxs-lookup"><span data-stu-id="9ad26-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="9ad26-111">Du kan ändra rollen vid behov.</span><span class="sxs-lookup"><span data-stu-id="9ad26-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="9ad26-112">Välj de från- och till-datum som resursen behövs och välj allokeringsmetod för resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="9ad26-113">Om du vill att teammedlemmen ska vara en projektgodkännare väljer du **Ja** i fältet **projektgodkännare**.</span><span class="sxs-lookup"><span data-stu-id="9ad26-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="9ad26-114">Detta innebär att teammedlemmen kan godkänna skickade tid- och utgiftsposter för det här projektet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="9ad26-115">Klicka på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="9ad26-115">Click **Save**.</span></span>

![Lägga till en teammedlem i formuläret snabbregistrering](media/RM-how-to-2.png)


<span data-ttu-id="9ad26-117">Du kan nu tilldela den bokade resursen till aktiviteter i projektet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="9ad26-118">PÅ sidan **projekt** klickar du på fliken **schema** för att tilldela uppgifter till den nya resursen.</span><span class="sxs-lookup"><span data-stu-id="9ad26-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="9ad26-119">Resursväljaren som startas från fältet **resurser** i uppgiftsrutnätet visar de team medlemmar som du kan välja.</span><span class="sxs-lookup"><span data-stu-id="9ad26-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Tilldela en teammedlem till en uppgift på fliken schema](media/RM-how-to-3.png)

<span data-ttu-id="9ad26-121">I version 3 av Project Service Automation (PSA), är inte resursbokningar och uppgiftstilldelningar tätt kopplade.</span><span class="sxs-lookup"><span data-stu-id="9ad26-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="9ad26-122">Det innebär att när du använder resursväljaren i schemat kan du tilldela uppgifter till teammedlemmar så att de blir fler timmar än de som ingår i projektet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="9ad26-123">Du kan se skillnaderna mellan bokningar av teammedlemmar och tilldelningar på fliken **Team** eller på fliken **resursavstämningar**. Du kan även stämma av skillnaderna mellan bokningar och tilldelningar för resurser på en mer detaljerad nivå.</span><span class="sxs-lookup"><span data-stu-id="9ad26-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Fliken Resursavstämning](media/RM-how-to-4.png)

<span data-ttu-id="9ad26-125">Du kan även använda resursväljaren på fliken **schema** om du vill söka efter och välja bokningsbara resurser som inte redan ingår i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="9ad26-126">De visas i resursväljaren som **andra resurser**.</span><span class="sxs-lookup"><span data-stu-id="9ad26-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Tilldela en uppgift till en icke-teammedlemresurs](media/RM-how-to-5.png)

<span data-ttu-id="9ad26-128">När du gör detta läggs resursen till i projektteamet och tilldelas uppgiften, men inga bokningar skapas.</span><span class="sxs-lookup"><span data-stu-id="9ad26-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Teammedlem med tilldelningar och inga bokningar](media/RM-how-to-6.png)

<span data-ttu-id="9ad26-130">Du kan använda den utökade bokningsfunktionen på fliken **avstämning** eller **Schemaläggningstavla** för att boka resursens kapacitet på projektet.</span><span class="sxs-lookup"><span data-stu-id="9ad26-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Utöka bokningar för en teammedlem på fliken resursavstämning](media/RM-how-to-7.png)

<span data-ttu-id="9ad26-132">När en teammedlem är bokad i projektet kan du använda underhåll bokningar eller använda schemaläggningstavlan direkt för att hantera deras bokningar.</span><span class="sxs-lookup"><span data-stu-id="9ad26-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
