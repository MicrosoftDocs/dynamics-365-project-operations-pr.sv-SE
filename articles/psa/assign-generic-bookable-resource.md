---
title: Tilldela allmänna bokningsbara resurser till en uppgift och ett projektteam
description: I det här ämnet finns information om bokning av generiska resurser till aktivitets- och projektgrupper.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085555"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="7e751-103">Tilldela allmänna bokningsbara resurser till en uppgift och generera resurskrav</span><span class="sxs-lookup"><span data-stu-id="7e751-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7e751-104">Utöver att boka och tilldela namngivna och verkliga resurser i projektet kan du tilldela allmänna resurser till projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="7e751-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="7e751-105">Dessa resurser kan användas som platshållare för namngivna resurser tills du är klar att bemanna projektet med namngivna resurser.</span><span class="sxs-lookup"><span data-stu-id="7e751-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="7e751-106">I Project Service Automation (PSA), öppna sidan **projekt** och på fliken **schema** anger du positionsnamnet för den generiska resursen i cellen **Resurs** i schemat.</span><span class="sxs-lookup"><span data-stu-id="7e751-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="7e751-107">Du kan också klicka på **Resurs** i cellen för att öppna resursväljaren och sedan ange namnet på den generiska resurs som du vill skapa.</span><span class="sxs-lookup"><span data-stu-id="7e751-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Skapa och tilldela en generisk teammedlem](media/RM-how-to-9.png)

<span data-ttu-id="7e751-109">Detta öppnar panelen **Snabbregistrering: Projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="7e751-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="7e751-110">Ange roll och organisationsenhet för den allmänna resursteammedlemmen och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="7e751-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Snabb skapande av generisk teammedlem](media/RM-how-to-10.png)

3. <span data-ttu-id="7e751-112">När du har skapat en ny generisk resursteammedlem tilldelas den aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="7e751-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="7e751-113">Du kan fortsätta att tilldela den allmänna resursen till andra uppgifter i aktivitetsschemat.</span><span class="sxs-lookup"><span data-stu-id="7e751-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Tilldela befintlig generisk teammedlem till uppgifter](media/RM-how-to-11.png)

4. <span data-ttu-id="7e751-115">När du har tilldelat den generiska resursen kan du skapa ett resurskrav och utföra den genom att direkt boka eller skicka en resursförfrågan till en resursansvarig.</span><span class="sxs-lookup"><span data-stu-id="7e751-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Skapa ett krav för en generisk teammedlem](media/RM-how-to-12.png)

<span data-ttu-id="7e751-117">Förutom att använda resursväljaren som nämnts ovan kan du lägga till allmänna resurser direkt i rutnätet med den generiska teammedlemmen.</span><span class="sxs-lookup"><span data-stu-id="7e751-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="7e751-118">Resurserna läggs till med ett resurskrav som baseras på start- och slutdatumen och allokeringsmetoden som anges i panelen **Snabbregistrering: Projektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="7e751-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="7e751-119">Du kan se en skillnad om du lägger till den allmänna teammedlemmen direkt och sedan tilldelar fler uppgifter till den allmänna resursen än de som krävs för att täcka antalet timmar.</span><span class="sxs-lookup"><span data-stu-id="7e751-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="7e751-120">Klicka **Generera krav** om du vill generera om behovet för att balansera de timmar som krävs för tilldelningarna.</span><span class="sxs-lookup"><span data-stu-id="7e751-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="7e751-121">Du kan också klicka på länken **resurskrav** i teamets rutnät för att öppna kravet och lägga till kunskaper, önskade resurser etc.</span><span class="sxs-lookup"><span data-stu-id="7e751-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Resurskrav](media/RM-how-to-13.png)

