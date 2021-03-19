---
title: Schemalägg ett projekt med en uppdelad arbetsstruktur
description: Schemalägga ett projekt med uppdelad arbetsstruktur i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282715"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="1307a-103">Schemalägg ett projekt med en uppdelad arbetsstruktur (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1307a-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1307a-104">Ett projektschema kommunicerar vad som behöver göras, vilka resurser som ska utföra arbetet och tidsramen inom vilken arbetet behöver slutföras.</span><span class="sxs-lookup"><span data-stu-id="1307a-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="1307a-105">Projektschemat återspeglar det arbete som är associerat med att leverera projektet i tid.</span><span class="sxs-lookup"><span data-stu-id="1307a-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="1307a-106">Ett av de första stegen i projektets inledande fas är att skapa ett projektschema.</span><span class="sxs-lookup"><span data-stu-id="1307a-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="1307a-107">Om du vill upprätta ett projektschema måste du skapa en mall för uppdelad arbetsstruktur.</span><span class="sxs-lookup"><span data-stu-id="1307a-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="1307a-108">Skapa en projektstruktur med en uppdelad arbetsstruktur, som hjälper dig att:</span><span class="sxs-lookup"><span data-stu-id="1307a-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="1307a-109">Dela upp arbetet i hanterbara uppgifter</span><span class="sxs-lookup"><span data-stu-id="1307a-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="1307a-110">Uppskatta den tid som krävs för att slutföra en uppgift</span><span class="sxs-lookup"><span data-stu-id="1307a-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="1307a-111">Ange uppgiftssamband och uppgifters varaktighet</span><span class="sxs-lookup"><span data-stu-id="1307a-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="1307a-112">Fastställa roller som krävs för att slutföra varje uppgift</span><span class="sxs-lookup"><span data-stu-id="1307a-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="1307a-113">Projektschemat i den uppdelade arbetsstrukturen har ett välbekant utseende, komplett med ett interaktivt Gantt-schema.</span><span class="sxs-lookup"><span data-stu-id="1307a-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="1307a-114">Skapa en uppdelad arbetsstruktur för ett projekt</span><span class="sxs-lookup"><span data-stu-id="1307a-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="1307a-115">Skapa en uppdelad arbetsstruktur för att representera ordningen för uppgifter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="1307a-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="1307a-116">Uppdelad arbetsstruktur innehåller uppgifter, krav för varje uppgift och information om intäkter och utgifter.</span><span class="sxs-lookup"><span data-stu-id="1307a-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="1307a-117">I en uppdelad arbetsstruktur kan du lägga till:</span><span class="sxs-lookup"><span data-stu-id="1307a-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="1307a-118">Sekvens av uppgifter i en hierarki</span><span class="sxs-lookup"><span data-stu-id="1307a-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="1307a-119">Andra uppgifter, om det finns någon som måste slutföras innan du kan starta en uppgift</span><span class="sxs-lookup"><span data-stu-id="1307a-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="1307a-120">Startdatum, slutdatum och varaktighet för en uppgift</span><span class="sxs-lookup"><span data-stu-id="1307a-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="1307a-121">Antal timmar som krävs för en uppgift</span><span class="sxs-lookup"><span data-stu-id="1307a-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="1307a-122">Alla nödvändiga färdigheter och utbildning för arbetare</span><span class="sxs-lookup"><span data-stu-id="1307a-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="1307a-123">De arbetstagare som har tilldelats till en uppgift</span><span class="sxs-lookup"><span data-stu-id="1307a-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="1307a-124">Beräknad intäkt och utgifter</span><span class="sxs-lookup"><span data-stu-id="1307a-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="1307a-125">Uppgiftstyper</span><span class="sxs-lookup"><span data-stu-id="1307a-125">Task types</span></span>  
<span data-ttu-id="1307a-126">Du ska använda följande typer av uppgifter när du skapar en mall för uppdelad arbetsstruktur:</span><span class="sxs-lookup"><span data-stu-id="1307a-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="1307a-127">**Rotnoden för projektet**.</span><span class="sxs-lookup"><span data-stu-id="1307a-127">**Project root node**</span></span> | <span data-ttu-id="1307a-128">Översta sammanfattningsuppgiften för projektet.</span><span class="sxs-lookup"><span data-stu-id="1307a-128">The top-level summary task for the project.</span></span> <span data-ttu-id="1307a-129">Alla andra projektuppgifter som skapas under den.</span><span class="sxs-lookup"><span data-stu-id="1307a-129">All other project tasks are created under it.</span></span> <span data-ttu-id="1307a-130">Namnet på rotuppgiften är projektnamnet.</span><span class="sxs-lookup"><span data-stu-id="1307a-130">The name of the root task is the project name.</span></span> <span data-ttu-id="1307a-131">Insats, datum och varaktighet för rotnoden baseras på värden i hierarkin under den.</span><span class="sxs-lookup"><span data-stu-id="1307a-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="1307a-132">Du kan inte redigera egenskaper för rotnod eller ta bort rotnoden.</span><span class="sxs-lookup"><span data-stu-id="1307a-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="1307a-133">**Sammanfattning- eller behållaruppgifter**.</span><span class="sxs-lookup"><span data-stu-id="1307a-133">**Summary or container tasks**</span></span> | <span data-ttu-id="1307a-134">En sammanfattningsuppgift är en uppgift som har underordnade uppgifter under den.</span><span class="sxs-lookup"><span data-stu-id="1307a-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="1307a-135">En sammanfattningsuppgift har inte någon egen arbetsinsats eller utgift.</span><span class="sxs-lookup"><span data-stu-id="1307a-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="1307a-136">Dess arbetsinsats och utgift är en sammanslagning av dess underuppgifter.</span><span class="sxs-lookup"><span data-stu-id="1307a-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="1307a-137">Du kan ändra namnet på en sammanfattningsuppgift, men du kan inte ändra insats, datum eller tid, eftersom de beräknas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="1307a-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="1307a-138">Om du tar bort en sammanfattningsuppgift tas uppgiften och alla dess underordnade uppgifter bort.</span><span class="sxs-lookup"><span data-stu-id="1307a-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="1307a-139">**Lövnodsuppgifter**.</span><span class="sxs-lookup"><span data-stu-id="1307a-139">**Leaf node tasks**</span></span> | <span data-ttu-id="1307a-140">En lövnodsuppgift representerar det mest detaljerade arbetet i projektet.</span><span class="sxs-lookup"><span data-stu-id="1307a-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="1307a-141">Den har en uppskattad insats, ett planerat antal resurser, planerade start- och slutdatum och en tid.</span><span class="sxs-lookup"><span data-stu-id="1307a-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="1307a-142">Uppgiftshierarki</span><span class="sxs-lookup"><span data-stu-id="1307a-142">Task hierarchy</span></span>  
 <span data-ttu-id="1307a-143">När du skapar en uppgiftshierarki har du följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="1307a-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="1307a-144">**Lägg till uppgift**.</span><span class="sxs-lookup"><span data-stu-id="1307a-144">**Add task**.</span></span>   <span data-ttu-id="1307a-145">Du kan lägga till en uppgift på en plats som du väljer i uppgiftshierarkin.</span><span class="sxs-lookup"><span data-stu-id="1307a-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="1307a-146">Om du inte väljer en plats visas den nya uppgiften i slutet.</span><span class="sxs-lookup"><span data-stu-id="1307a-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="1307a-147">**Dra in uppgift**.</span><span class="sxs-lookup"><span data-stu-id="1307a-147">**Indent task**.</span></span>   <span data-ttu-id="1307a-148">Dra in en uppgift så att den blir underordnad uppgiften direkt ovanför.</span><span class="sxs-lookup"><span data-stu-id="1307a-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="1307a-149">**Dra ut uppgift**.</span><span class="sxs-lookup"><span data-stu-id="1307a-149">**Outdent task**.</span></span>   <span data-ttu-id="1307a-150">Dra ut en uppgift så att den inte längre är en underuppgift till dess ursprungliga överordnade uppgift.</span><span class="sxs-lookup"><span data-stu-id="1307a-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="1307a-151">**Flytta upp och flytta ned**.</span><span class="sxs-lookup"><span data-stu-id="1307a-151">**Move up and Move down**.</span></span>   <span data-ttu-id="1307a-152">Flytta uppgifter upp och ned i hierarkin för den överordnade uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="1307a-153">Om du flyttar en uppgift uppåt eller nedåt påverkar inte dess insats, utgift, datum eller tid.</span><span class="sxs-lookup"><span data-stu-id="1307a-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="1307a-154">Uppgiftsattribut</span><span class="sxs-lookup"><span data-stu-id="1307a-154">Task attributes</span></span>  
 <span data-ttu-id="1307a-155">En uppgifts namn beskriver det arbete som måste utföras.</span><span class="sxs-lookup"><span data-stu-id="1307a-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="1307a-156">Olika uppgiftsattribut används för att beskriva schemat och bemanningsbehov för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="1307a-157">Schemalägg attribut</span><span class="sxs-lookup"><span data-stu-id="1307a-157">Schedule attributes</span></span>

 - <span data-ttu-id="1307a-158">Tilldela värden till **Insatstimmar**, **Antal resurser**, **Startdatum**, **Slutdatum** och **Tid** för att fastställa schemat för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="1307a-159">**Insats** är en uppskattning av antalet timmar som det tar för att slutföra uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="1307a-160">**Antalet resurser** är en uppskattning som projektledaren placerar i uppgiften för att få bästa möjliga schema.</span><span class="sxs-lookup"><span data-stu-id="1307a-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="1307a-161">**Tid** (i dagar) anger antalet dagar det tar att slutföra uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="1307a-162">Bemanningsattribut</span><span class="sxs-lookup"><span data-stu-id="1307a-162">Staffing attributes</span></span>

 - <span data-ttu-id="1307a-163">**Roll**, **Organisationsenhet för resurs**, **Antal resurser** och **Resurser** beskriver bemanningsbehovet för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="1307a-164">**Roll** beskriver typen av resurs som behövs för att utföra uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="1307a-165">**Organisationsenhet för resursen** anger den organisationsenhet från vilken resurser ska bemannas för uppgiften. Detta påverkar också utgift- och försäljningsuppskattningen för uppgiften, eftersom det redovisas vid bestämning av enhetsförsäljningspriset för resursen.</span><span class="sxs-lookup"><span data-stu-id="1307a-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="1307a-166">**Resurser** innehåller en allmän eller namngiven resurs när någon hittas.</span><span class="sxs-lookup"><span data-stu-id="1307a-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="1307a-167">Beroenden mellan uppgifter</span><span class="sxs-lookup"><span data-stu-id="1307a-167">Task dependencies</span></span>  
 <span data-ttu-id="1307a-168">Du kan skapa relationer till föregångare mellan en eller flera uppgifter i den uppdelad arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="1307a-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="1307a-169">Du kan ange ett eller flera värden för föregångarfältet för uppgifter om du vill ange vilka uppgifter den är beroende av.</span><span class="sxs-lookup"><span data-stu-id="1307a-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="1307a-170">När du tilldelar en uppgift ett föregångarvärde kan uppgiften starta först när alla föregående uppgifter har slutförts.</span><span class="sxs-lookup"><span data-stu-id="1307a-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="1307a-171">Om du anger detta beroende för en uppgift leder det till omberäkning av det planerade startdatumet för uppgiften till det senaste slutet för alla dess föregående uppgifter.</span><span class="sxs-lookup"><span data-stu-id="1307a-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="1307a-172">Föregångarrelaterad påverkan på ett schema är inte begränsad av uppgiftsläget som definieras för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="1307a-173">Uppgiftsläge</span><span class="sxs-lookup"><span data-stu-id="1307a-173">Task mode</span></span>  
 <span data-ttu-id="1307a-174">Uppgiftsläget är en av de viktiga faktorer som fastställer schemaläggningen av lövnodsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="1307a-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="1307a-175">Det finns två uppgiftslägen för varje uppgift: automatiskt schemaläggningsläge och manuellt schemaläggningsläge.</span><span class="sxs-lookup"><span data-stu-id="1307a-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="1307a-176">**Automatisk schemaläggning**.</span><span class="sxs-lookup"><span data-stu-id="1307a-176">**Auto scheduling**.</span></span>   <span data-ttu-id="1307a-177">När du anger uppgiftsläget till Automatiskt schemalagt använder schemaläggningsmotorn schemaläggningsreglerna på följande uppgiftsattribut för att fastställa schemat för en uppgift:</span><span class="sxs-lookup"><span data-stu-id="1307a-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="1307a-178">Föregångare</span><span class="sxs-lookup"><span data-stu-id="1307a-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="1307a-179">Insats</span><span class="sxs-lookup"><span data-stu-id="1307a-179">Effort</span></span>  
  
    -   <span data-ttu-id="1307a-180">Antal resurser</span><span class="sxs-lookup"><span data-stu-id="1307a-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="1307a-181">Start- och slutdatum</span><span class="sxs-lookup"><span data-stu-id="1307a-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="1307a-182">**Schemaläggningsregler**.</span><span class="sxs-lookup"><span data-stu-id="1307a-182">**Scheduling rules**.</span></span>   <span data-ttu-id="1307a-183">Startdatumet för en lövnodsuppgift som saknar föregångare blir som standard projektets planeringsstartdatum.</span><span class="sxs-lookup"><span data-stu-id="1307a-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="1307a-184">En lövnodsuppgifts tid beräknas alltid som antalet arbetsdagar mellan dess start- och slutdatum.</span><span class="sxs-lookup"><span data-stu-id="1307a-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="1307a-185">När en uppgift schemaläggs automatiskt, följer schemaläggningsmotorn reglerna nedan:</span><span class="sxs-lookup"><span data-stu-id="1307a-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="1307a-186">Start- och slutdatumen för en uppgift måste alltid vara arbetsdagar enligt projektets schemaläggningskalender</span><span class="sxs-lookup"><span data-stu-id="1307a-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="1307a-187">Startdatum för en uppgift med föregångare har som standard det senaste slutdatumet för föregående uppgifter</span><span class="sxs-lookup"><span data-stu-id="1307a-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="1307a-188">Insats = antal personer \* tid \* timmar i en standardarbetsdag i projektkalendern</span><span class="sxs-lookup"><span data-stu-id="1307a-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="1307a-189">**Manuell schemaläggning**.</span><span class="sxs-lookup"><span data-stu-id="1307a-189">**Manual scheduling**.</span></span>   <span data-ttu-id="1307a-190">I vissa fall kanske du vill avvika från dessa regler.</span><span class="sxs-lookup"><span data-stu-id="1307a-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="1307a-191">I dessa fall kan du ange uppgiftsläget för manuell tidsplanering för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="1307a-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="1307a-192">Detta stoppar schemaläggningsmotorn från att beräkna värdena för andra schemaläggningsattribut.</span><span class="sxs-lookup"><span data-stu-id="1307a-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="1307a-193">Att ange föregående uppgifter påverkar alltid den beroende uppgiftens startdatum.</span><span class="sxs-lookup"><span data-stu-id="1307a-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="1307a-194">Skapa en uppdelad arbetsstruktur</span><span class="sxs-lookup"><span data-stu-id="1307a-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="1307a-195">Gå till **Project Service > Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1307a-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="1307a-196">Klicka på projektet du vill arbeta med.</span><span class="sxs-lookup"><span data-stu-id="1307a-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="1307a-197">Välj nedpilen bredvid projektnamnet i fältet överst på skärmen och klicka på Uppdelad arbetsstruktur.</span><span class="sxs-lookup"><span data-stu-id="1307a-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="1307a-198">Om du vill lägga till en uppgift klickar du på **Lägg till uppgift**.</span><span class="sxs-lookup"><span data-stu-id="1307a-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="1307a-199">Fyll i fälten för uppgiften och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="1307a-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="1307a-200">Fortsätt lägga till uppgifter tills din uppdelade arbetsstruktur är klar.</span><span class="sxs-lookup"><span data-stu-id="1307a-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="1307a-201">När du skapar en uppdelad arbetsstruktur, kan du göra följande för att organisera dina uppgifter:</span><span class="sxs-lookup"><span data-stu-id="1307a-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="1307a-202">Markera en uppgift och klicka på **Dra in** för att flytta den under en annan uppgift, eller klicka på Minska indrag för att flytta ut den en nivå.</span><span class="sxs-lookup"><span data-stu-id="1307a-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="1307a-203">Markera en uppgift och klicka på **Flytta upp** eller **Flytta ned** för att flytta den uppåt eller nedåt i listan.</span><span class="sxs-lookup"><span data-stu-id="1307a-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="1307a-204">Klicka på **Dölj Gantt-schema** för att dölja Gantt-schemat och klicka på **Visa Gantt-schema** för att visa det igen.</span><span class="sxs-lookup"><span data-stu-id="1307a-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="1307a-205">Välj en annan tidsperiod för Gantt-schemat i **Tidsskala**.</span><span class="sxs-lookup"><span data-stu-id="1307a-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="1307a-206">In du vill lägga till de roller som du har angett i den uppdelade arbetsstrukturen till projektets gruppmedlemmar klickar du på **Generera projektteam**.</span><span class="sxs-lookup"><span data-stu-id="1307a-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="1307a-207">Klicka på **Spara** i skärmens nedre högra hörn när du är klar med ändringarna.</span><span class="sxs-lookup"><span data-stu-id="1307a-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1307a-208">Se även</span><span class="sxs-lookup"><span data-stu-id="1307a-208">See Also</span></span>  
 [<span data-ttu-id="1307a-209">Guide för projektansvarig</span><span class="sxs-lookup"><span data-stu-id="1307a-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]