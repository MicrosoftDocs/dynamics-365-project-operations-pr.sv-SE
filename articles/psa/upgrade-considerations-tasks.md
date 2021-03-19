---
title: Uppgraderingshänsyn för uppdelad arbetsstruktur
description: I det här ämnet finns information om hur du uppgraderar uppdelad arbetsstruktur från Project Service Automation 2.x till 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281770"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="95116-103">Uppgraderingshänsyn för uppdelad arbetsstruktur</span><span class="sxs-lookup"><span data-stu-id="95116-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="95116-104">I det här ämnet finns information om hur du uppgraderar uppdelad arbetsstruktur från Project Service Automation 2.x till 3.x.</span><span class="sxs-lookup"><span data-stu-id="95116-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="95116-105">I det här ämnet anges hälsotillståndet för ett projekt i Project Service Automation (PSA) som krävs för en lyckad uppgradering.</span><span class="sxs-lookup"><span data-stu-id="95116-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="95116-106">Det finns också information om de vanligaste spärrningsförhållanden som gör att uppgraderingen misslyckas.</span><span class="sxs-lookup"><span data-stu-id="95116-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="95116-107">Mer information om hur du definierar projektuppgifter och deras funktioner i ett projektschema finns i [projektscheman](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="95116-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="95116-108">Nyckelentiteter</span><span class="sxs-lookup"><span data-stu-id="95116-108">Key entities</span></span>
<span data-ttu-id="95116-109">Följande entiteter krävs för att du ska kunna utföra en korrekt uppdelad arbetsstruktur som redan har laddats med resurser:</span><span class="sxs-lookup"><span data-stu-id="95116-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="95116-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="95116-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="95116-111">Projektteam</span><span class="sxs-lookup"><span data-stu-id="95116-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="95116-112">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="95116-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="95116-113">Resurstilldelningar</span><span class="sxs-lookup"><span data-stu-id="95116-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="95116-114">Beroende för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="95116-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="95116-115">Bokningsbara resurser</span><span class="sxs-lookup"><span data-stu-id="95116-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="95116-116">Om du vill definiera en resursinläst uppdelad arbetsstruktur som ska användas måste du utföra följande steg:</span><span class="sxs-lookup"><span data-stu-id="95116-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="95116-117">Skapa ett nytt projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-117">Create a new project.</span></span> <span data-ttu-id="95116-118">Mer information om hur du skapar ett nytt projekt finns i [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="95116-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="95116-119">Skapa en eller flera uppgifter.</span><span class="sxs-lookup"><span data-stu-id="95116-119">Create one or more tasks.</span></span> <span data-ttu-id="95116-120">Mer information om hur du skapar en ny uppgift finns i [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="95116-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="95116-121">Definiera uppgiftberoenden</span><span class="sxs-lookup"><span data-stu-id="95116-121">Define the task dependencies.</span></span> <span data-ttu-id="95116-122">Mer information finns i [Beroende för projektuppgift](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="95116-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="95116-123">Tilldela projektets teammedlemmar till projektet.</span><span class="sxs-lookup"><span data-stu-id="95116-123">Assign project team members to the project.</span></span> <span data-ttu-id="95116-124">Mer information finns i [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="95116-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="95116-125">Tilldela projektets teammedlemmar till uppgifter.</span><span class="sxs-lookup"><span data-stu-id="95116-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="95116-126">Mer information finns i [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="95116-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="95116-127">Projektteamrelationer</span><span class="sxs-lookup"><span data-stu-id="95116-127">Project team relationships</span></span>

<span data-ttu-id="95116-128">För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:</span><span class="sxs-lookup"><span data-stu-id="95116-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="95116-129">Alla projektmedlemmar i teamet måste associeras med en bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="95116-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="95116-130">Alla projektmedlemmar i teamet måste associeras med samma projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="95116-131">Projektuppgiftsrelationer</span><span class="sxs-lookup"><span data-stu-id="95116-131">Project task relationships</span></span>
<span data-ttu-id="95116-132">För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:</span><span class="sxs-lookup"><span data-stu-id="95116-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="95116-133">Alla relaterade uppgifter måste associeras med samma projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="95116-134">Varje raduppgift måste ha en överordnad uppgift.</span><span class="sxs-lookup"><span data-stu-id="95116-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="95116-135">Varje uppgift måste ha ett överordnat projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="95116-136">Giltiga villkor</span><span class="sxs-lookup"><span data-stu-id="95116-136">Valid conditions</span></span>

- <span data-ttu-id="95116-137">Alla uppgiftsvaraktigheter måste vara större än eller lika med (>=) en timme och mindre än 1 800 000 minuter (1 250 dagar).\*</span><span class="sxs-lookup"><span data-stu-id="95116-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="95116-138">Alla uppgifter måste ha ett startdatum som inte är tidigare än 2000-01-01.\*</span><span class="sxs-lookup"><span data-stu-id="95116-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="95116-139">Alla uppgifter måste vara ett startdatum som inte är längre än 17 år från och med idag.\*</span><span class="sxs-lookup"><span data-stu-id="95116-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="95116-140">Alla uppgifter måste ha ett startdatum som är tidigare eller lika med deras slutdatum.</span><span class="sxs-lookup"><span data-stu-id="95116-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="95116-141">Alla transaktionstyper för klassificeringar (utgift, material, skatt och tid) måste ha värden för **standardenhet** och **enhetsgrupp**.</span><span class="sxs-lookup"><span data-stu-id="95116-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="95116-142">Datumformat med bokstäver bör undvikas.</span><span class="sxs-lookup"><span data-stu-id="95116-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="95116-143">Potentiella åtgärdssteg</span><span class="sxs-lookup"><span data-stu-id="95116-143">Potential mitigation steps</span></span>
- <span data-ttu-id="95116-144">Använd avancerad sökning för att identifiera projektaktiviteter som inte innehåller projekt-ID.</span><span class="sxs-lookup"><span data-stu-id="95116-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="95116-145">Använd avancerad sökning för att identifiera projektaktiviteter där den schemalagda varaktigheten är större än > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="95116-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="95116-146">Innan du gör några dataändringar bör du undersöka alla anpassningar som har associerats med den entitet som kan ha lett till ett dåligt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="95116-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="95116-147">De här anpassningarna ska åtgärdas innan du fortsätter med några databaserade uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="95116-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="95116-148">Om du har identifierat vilka uppgifter som har överbliven åtgärd kan du överväga att ta bort de här uppgifterna om de inte behövs eller om de ska associeras med rätt överordnat projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="95116-149">Om det är möjligt kan du lägga till flera uppgifter som representerar den totala varaktigheten för aktiviteter där varaktigheten är mer än 1 250 dagar.</span><span class="sxs-lookup"><span data-stu-id="95116-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="95116-150">Objekt som anges med en asterisk (\*) har gränser som beror på att CRM (Customer Relationship Management) bara stöder av 7 320 upprepade utvidgningar.</span><span class="sxs-lookup"><span data-stu-id="95116-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="95116-151">Du måste stanna kvar under den här gränsen.</span><span class="sxs-lookup"><span data-stu-id="95116-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="95116-152">Resurstilldelningsrelationer</span><span class="sxs-lookup"><span data-stu-id="95116-152">Resource Assignment relationships</span></span>
<span data-ttu-id="95116-153">För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:</span><span class="sxs-lookup"><span data-stu-id="95116-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="95116-154">Alla resurstilldelningar i en uppdelad arbetsstruktur måste relateras till samma projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="95116-155">Alla resurstilldelningar i en uppdelad arbetsstruktur måste kopplas till projektteammedlemmar i samma projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="95116-156">Potentiella åtgärdssteg</span><span class="sxs-lookup"><span data-stu-id="95116-156">Potential mitigation steps</span></span>
- <span data-ttu-id="95116-157">Identifiera alla uppgifter som faller utanför villkoren som beskrivs ovan.</span><span class="sxs-lookup"><span data-stu-id="95116-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="95116-158">Alla resurstilldelningar som inte längre är giltiga ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="95116-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="95116-159">Projektuppgiftsberoende relationer</span><span class="sxs-lookup"><span data-stu-id="95116-159">Project task dependency relationships</span></span>
<span data-ttu-id="95116-160">För att uppgraderingen ska genomföras korrekt måste följande relationer upprätthållas på rätt sätt:</span><span class="sxs-lookup"><span data-stu-id="95116-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="95116-161">Alla beroende av projektuppgifter måste vara relaterade till samma projekt.</span><span class="sxs-lookup"><span data-stu-id="95116-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="95116-162">En uppgift får inte ha samma beroendereferens mer än en gång.</span><span class="sxs-lookup"><span data-stu-id="95116-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]