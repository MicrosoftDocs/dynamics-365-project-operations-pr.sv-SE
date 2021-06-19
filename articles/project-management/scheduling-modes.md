---
title: Schemaläggningslägen
description: I det här ämnet finns information om schemaläggningslägen.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116729"
---
# <a name="scheduling-modes"></a><span data-ttu-id="51e42-103">Schemaläggningslägen</span><span class="sxs-lookup"><span data-stu-id="51e42-103">Scheduling modes</span></span>

<span data-ttu-id="51e42-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="51e42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="51e42-105">Dynamics 365 Project Operations gör att organisationer kan definiera hur de hanterar ändringar av nyckelvariabler i uppgifter inom den uppdelade arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="51e42-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="51e42-106">Utifrån organisationens specifika behov kan projektansvariga ändra schemaläggningsläget när ett projekt skapas.</span><span class="sxs-lookup"><span data-stu-id="51e42-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="51e42-107">Det finns tre tillgängliga schemaläggningslägen i Project Operations:</span><span class="sxs-lookup"><span data-stu-id="51e42-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="51e42-108">Fast varaktighet (det här är standardläget)</span><span class="sxs-lookup"><span data-stu-id="51e42-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="51e42-109">Fast insats (*Arbete*)</span><span class="sxs-lookup"><span data-stu-id="51e42-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="51e42-110">Fasta enheter</span><span class="sxs-lookup"><span data-stu-id="51e42-110">Fixed units</span></span>

<span data-ttu-id="51e42-111">Värdena som påverkas av definitionen i ett visst schemaläggningsläge bestäms av följande formel:</span><span class="sxs-lookup"><span data-stu-id="51e42-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="51e42-112">Insats = Varaktighet x enheter</span><span class="sxs-lookup"><span data-stu-id="51e42-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="51e42-113">När du definierar ett projekts schemaläggningsläge ställer du in ett av dessa värden som sedan inte kan ändras.</span><span class="sxs-lookup"><span data-stu-id="51e42-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="51e42-114">Om du har värdet som en konstant prioriteras det, vilket meddelar systemet att det inte ska ändras när de två andra värdena ändras.</span><span class="sxs-lookup"><span data-stu-id="51e42-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="51e42-115">Följande tabell innehåller information om effekten av att välja ett visst läge.</span><span class="sxs-lookup"><span data-stu-id="51e42-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="51e42-116">**I denna uppgift**</span><span class="sxs-lookup"><span data-stu-id="51e42-116">**In this task**</span></span>             | <span data-ttu-id="51e42-117">**Om du reviderar enheter**</span><span class="sxs-lookup"><span data-stu-id="51e42-117">**If you revise units**</span></span>   | <span data-ttu-id="51e42-118">**Om du reviderar varaktighet**</span><span class="sxs-lookup"><span data-stu-id="51e42-118">**If you revise duration**</span></span> | <span data-ttu-id="51e42-119">**Om du reviderar insats**</span><span class="sxs-lookup"><span data-stu-id="51e42-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="51e42-120">Uppgift med fasta enheter</span><span class="sxs-lookup"><span data-stu-id="51e42-120">Fixed units task</span></span>     | <span data-ttu-id="51e42-121">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-121">Duration is recalculated.</span></span> | <span data-ttu-id="51e42-122">Insats beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-122">Effort is recalculated.</span></span>    | <span data-ttu-id="51e42-123">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="51e42-124">Uppgift med fast insats</span><span class="sxs-lookup"><span data-stu-id="51e42-124">Fixed effort task</span></span>    | <span data-ttu-id="51e42-125">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-125">Duration is recalculated.</span></span> | <span data-ttu-id="51e42-126">Enheter beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-126">Units are recalculated.</span></span>    | <span data-ttu-id="51e42-127">Varaktighet beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="51e42-128">Uppgift med fast varaktighet</span><span class="sxs-lookup"><span data-stu-id="51e42-128">Fixed duration task</span></span>  | <span data-ttu-id="51e42-129">Insats beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-129">Effort is recalculated.</span></span>   | <span data-ttu-id="51e42-130">Insats beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-130">Effort is recalculated.</span></span>    | <span data-ttu-id="51e42-131">Enheter beräknas om.</span><span class="sxs-lookup"><span data-stu-id="51e42-131">Units are recalculated.</span></span>   |

<span data-ttu-id="51e42-132">Mer information om vad ett visst läge innebär finns i [Ändra uppgiftstyp för bättre schemaläggning](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="51e42-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="51e42-133">I ämnet används termen **Arbete** i stället för **Insats**.</span><span class="sxs-lookup"><span data-stu-id="51e42-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="51e42-134">Ändra organisationens schemaläggningsläge</span><span class="sxs-lookup"><span data-stu-id="51e42-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="51e42-135">Definiera en organisations schemaläggningsläge genom att följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="51e42-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="51e42-136">Gå till **Inställningar** \> **Allmänt** \> **Parametrar** och välj projektparametern.</span><span class="sxs-lookup"><span data-stu-id="51e42-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="51e42-137">På sidan **Projektparametrar** väljer du standardschemaläggningsläget för organisationen och definierar om projektansvarig kan åsidosätta inställningen när ett nytt projekt skapas.</span><span class="sxs-lookup"><span data-stu-id="51e42-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="51e42-138">Ändra inställningen för schemaläggningsläge för ett projekt</span><span class="sxs-lookup"><span data-stu-id="51e42-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="51e42-139">Om en organisation tillåter att projektansvarig åsidosätter standardschemaläggningsläget kan projektansvarig göra ändringen när hen skapar ett nytt projekt.</span><span class="sxs-lookup"><span data-stu-id="51e42-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="51e42-140">När projektet har sparats går det dock inte att ändra schemaläggningsläget.</span><span class="sxs-lookup"><span data-stu-id="51e42-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="51e42-141">Kopierade projekt</span><span class="sxs-lookup"><span data-stu-id="51e42-141">Copied projects</span></span>

<span data-ttu-id="51e42-142">Eftersom ett projekt skapas när åtgärden kopiera projekt vidtas kan inte projektansvarig ställa in schemaläggningsläge.</span><span class="sxs-lookup"><span data-stu-id="51e42-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="51e42-143">Målprojektet använder som standard alltid det läge som har definierats på organisationsnivå.</span><span class="sxs-lookup"><span data-stu-id="51e42-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="51e42-144">Kopierade uppgifter</span><span class="sxs-lookup"><span data-stu-id="51e42-144">Copied tasks</span></span>

<span data-ttu-id="51e42-145">När en uppgift kopieras från ett projekt till ett annat, ärver uppgiften schemaläggningsläget för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="51e42-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
