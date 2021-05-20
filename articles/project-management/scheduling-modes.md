---
title: Schemaläggningslägen
description: I det här ämnet finns information om schemaläggningslägen.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981457"
---
# <a name="scheduling-modes"></a><span data-ttu-id="b5080-103">Schemaläggningslägen</span><span class="sxs-lookup"><span data-stu-id="b5080-103">Scheduling modes</span></span>

<span data-ttu-id="b5080-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b5080-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b5080-105">Dynamics 365 Project Operations gör att organisationer kan definiera hur de hanterar ändringar av nyckelvariabler i uppgifter inom den uppdelade arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="b5080-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="b5080-106">Utifrån organisationens specifika behov kan projektansvariga ändra schemaläggningsläget när ett projekt skapas.</span><span class="sxs-lookup"><span data-stu-id="b5080-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="b5080-107">Det finns tre tillgängliga schemaläggningslägen i Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b5080-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="b5080-108">Fast varaktighet (det här är standardläget)</span><span class="sxs-lookup"><span data-stu-id="b5080-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="b5080-109">Fast arbete</span><span class="sxs-lookup"><span data-stu-id="b5080-109">Fixed work</span></span>
  - <span data-ttu-id="b5080-110">Fasta enheter</span><span class="sxs-lookup"><span data-stu-id="b5080-110">Fixed units</span></span>

<span data-ttu-id="b5080-111">Värdena som påverkas av definitionen i ett visst schemaläggningsläge bestäms av följande formel:</span><span class="sxs-lookup"><span data-stu-id="b5080-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="b5080-112">Insats (*Arbete*) = Varaktighet x enheter</span><span class="sxs-lookup"><span data-stu-id="b5080-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="b5080-113">När du definierar ett projekts schemaläggningsläge ställer du in ett av dessa värden som sedan inte kan ändras.</span><span class="sxs-lookup"><span data-stu-id="b5080-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="b5080-114">Om du har värdet som en konstant prioriteras det, vilket meddelar systemet att det inte ska ändras när de två andra värdena ändras.</span><span class="sxs-lookup"><span data-stu-id="b5080-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="b5080-115">Följande tabell innehåller information om effekten av att välja ett visst läge.</span><span class="sxs-lookup"><span data-stu-id="b5080-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="b5080-116">**I denna uppgift**</span><span class="sxs-lookup"><span data-stu-id="b5080-116">**In this task**</span></span>             | <span data-ttu-id="b5080-117">**Om du reviderar enheter**</span><span class="sxs-lookup"><span data-stu-id="b5080-117">**If you revise units**</span></span>   | <span data-ttu-id="b5080-118">**Om du reviderar varaktighet**</span><span class="sxs-lookup"><span data-stu-id="b5080-118">**If you revise duration**</span></span> | <span data-ttu-id="b5080-119">**Om du reviderar insats**</span><span class="sxs-lookup"><span data-stu-id="b5080-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="b5080-120">Uppgift med fasta enheter</span><span class="sxs-lookup"><span data-stu-id="b5080-120">Fixed units task</span></span>     | <span data-ttu-id="b5080-121">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-121">Duration is recalculated.</span></span> | <span data-ttu-id="b5080-122">Insats beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-122">Effort is recalculated.</span></span>    | <span data-ttu-id="b5080-123">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="b5080-124">Uppgift med fast insats</span><span class="sxs-lookup"><span data-stu-id="b5080-124">Fixed effort task</span></span>    | <span data-ttu-id="b5080-125">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-125">Duration is recalculated.</span></span> | <span data-ttu-id="b5080-126">Enheter beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-126">Units are recalculated.</span></span>    | <span data-ttu-id="b5080-127">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="b5080-128">Uppgift med fast varaktighet</span><span class="sxs-lookup"><span data-stu-id="b5080-128">Fixed duration task</span></span>  | <span data-ttu-id="b5080-129">Insats beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-129">Effort is recalculated.</span></span>   | <span data-ttu-id="b5080-130">Insats beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-130">Effort is recalculated.</span></span>    | <span data-ttu-id="b5080-131">Enheter beräknas om.</span><span class="sxs-lookup"><span data-stu-id="b5080-131">Units are recalculated.</span></span>   |

<span data-ttu-id="b5080-132">Mer information om vad ett visst läge innebär finns i [Ändra uppgiftstyp för bättre schemaläggning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="b5080-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="b5080-133">I ämnet används termen **Arbete** i stället för **Insats**.</span><span class="sxs-lookup"><span data-stu-id="b5080-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="b5080-134">Ändra organisationens schemaläggningsläge</span><span class="sxs-lookup"><span data-stu-id="b5080-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="b5080-135">Definiera en organisations schemaläggningsläge genom att följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="b5080-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="b5080-136">Gå till **Inställningar** \> **Allmänt** \> **Parametrar** och välj projektparametern.</span><span class="sxs-lookup"><span data-stu-id="b5080-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="b5080-137">På sidan **Projektparametrar** väljer du standardschemaläggningsläget för organisationen och definierar om projektansvarig kan åsidosätta inställningen när ett nytt projekt skapas.</span><span class="sxs-lookup"><span data-stu-id="b5080-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="b5080-138">Ändra inställningen för schemaläggningsläge för ett projekt</span><span class="sxs-lookup"><span data-stu-id="b5080-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="b5080-139">Om en organisation tillåter att projektansvarig åsidosätter standardschemaläggningsläget kan projektansvarig göra ändringen när hen skapar ett nytt projekt.</span><span class="sxs-lookup"><span data-stu-id="b5080-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="b5080-140">När projektet har sparats går det dock inte att ändra schemaläggningsläget.</span><span class="sxs-lookup"><span data-stu-id="b5080-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="b5080-141">Kopierade projekt</span><span class="sxs-lookup"><span data-stu-id="b5080-141">Copied projects</span></span>

<span data-ttu-id="b5080-142">Eftersom ett projekt skapas när åtgärden kopiera projekt vidtas kan inte projektansvarig ställa in schemaläggningsläge.</span><span class="sxs-lookup"><span data-stu-id="b5080-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="b5080-143">Målprojektet använder som standard alltid det läge som har definierats på organisationsnivå.</span><span class="sxs-lookup"><span data-stu-id="b5080-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="b5080-144">Kopierade uppgifter</span><span class="sxs-lookup"><span data-stu-id="b5080-144">Copied tasks</span></span>

<span data-ttu-id="b5080-145">När en uppgift kopieras från ett projekt till ett annat, ärver uppgiften schemaläggningsläget för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="b5080-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
