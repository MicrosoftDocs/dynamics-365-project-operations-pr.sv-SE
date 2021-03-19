---
title: Skapa ett projektteam
description: I det här ämnet finns information om hur du skapar och hanterar projektteam.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270880"
---
# <a name="create-a-project-team"></a><span data-ttu-id="6366f-103">Skapa ett projektteam</span><span class="sxs-lookup"><span data-stu-id="6366f-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6366f-104">För att du ska kunna använda rollerna som har ställts in tidigare i ett projekt måste en projektledare associera rollerna med projektet.</span><span class="sxs-lookup"><span data-stu-id="6366f-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="6366f-105">Flera roller kan tilldelas för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="6366f-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="6366f-106">För att undvika förvirring märks rollerna automatiskt under reservation.</span><span class="sxs-lookup"><span data-stu-id="6366f-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="6366f-107">Om projektledaren t.ex. kräver tre programmerare är det tre programmerare som har **programmerare 1**, **programmerare 2** och **programmerare 3** när deras etiketter genereras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="6366f-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="6366f-108">Om rollegenskaperna tidigare har angetts för rollen används de som ett filter vid sökning efter en resurs.</span><span class="sxs-lookup"><span data-stu-id="6366f-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="6366f-109">Ytterligare kännetecken kan läggas till som krävs för att sökningen ska kunna förfinas ytterligare.</span><span class="sxs-lookup"><span data-stu-id="6366f-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="6366f-110">Vyinställningar kan också anpassas så att du får en bättre bild av resurstillgängligheten.</span><span class="sxs-lookup"><span data-stu-id="6366f-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="6366f-111">Det finns alternativ för att visa tim-, dygns-, vecko-, månads-, kvartals- och årstillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="6366f-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="6366f-112">Det finns även ett alternativ för att visa tillgänglig och återstående kapacitet för resurser.</span><span class="sxs-lookup"><span data-stu-id="6366f-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="6366f-113">Det här alternativet är användbart vid tidshantering när du uppskattar tillgänglig tid för aktiviteter eller resurstillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="6366f-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="6366f-114">Projektledaren kan välja en roll på sidan och om det finns en tillgänglig resurs som passar för kravet väljer du om du vill reservera en resurs som ska fylla rollen.</span><span class="sxs-lookup"><span data-stu-id="6366f-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="6366f-115">Observera att resurserna inte behöver reserveras vid den här tidpunkten i planeringsfasen.</span><span class="sxs-lookup"><span data-stu-id="6366f-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="6366f-116">När du skapar en struktur kan du ersätta roller med personalresurser för projektet.</span><span class="sxs-lookup"><span data-stu-id="6366f-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="6366f-117">Om roller ersätts med personalresurser i WBS uppdateras projektets teamlista och schemaläggning automatiskt i resursinställningarna.</span><span class="sxs-lookup"><span data-stu-id="6366f-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="6366f-118">[![Projektteamlistor som innehåller både roller och faktiska resurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="6366f-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="6366f-119">Projektledaren har olika alternativ för att boka en resurs för ett projekt, till exempel **återstående kapacitet**, **full kapacitet**, **kapacitetsprocent** och **ange timmar**.</span><span class="sxs-lookup"><span data-stu-id="6366f-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="6366f-120">De här bokningsalternativen kan när som helst annulleras om resurstilldelningar ändras.</span><span class="sxs-lookup"><span data-stu-id="6366f-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="6366f-121">Två typer av bokningar stöds:</span><span class="sxs-lookup"><span data-stu-id="6366f-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="6366f-122">**Fast bokning** – resursreservationen har godkänts och bekräftats för att arbeta med åtagandet för den angivna varaktigheten.</span><span class="sxs-lookup"><span data-stu-id="6366f-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="6366f-123">**Mjuk bokning** – resursreservationerna har godkänts och preliminärt angetts till att arbeta med åtagandet för den angivna varaktigheten.</span><span class="sxs-lookup"><span data-stu-id="6366f-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="6366f-124">Följande procedur förklarar hur du skapar ett projektteam.</span><span class="sxs-lookup"><span data-stu-id="6366f-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="6366f-125">Skapa ett projektteam</span><span class="sxs-lookup"><span data-stu-id="6366f-125">Create a project team</span></span>

1. <span data-ttu-id="6366f-126">På listsidan **Alla projekt** välj ett projekt och välj sedan **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="6366f-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="6366f-127">På fliken **Projektteam och schemaläggning** i fältet **Schemalägg slutdatum** ange startdatum för schemaläggning plus en månad.</span><span class="sxs-lookup"><span data-stu-id="6366f-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="6366f-128">Om exempelvis schemats startdatum är 24 juni 2017 (24/06/2017) anger du **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="6366f-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="6366f-129">Markera **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="6366f-129">Select **Add**.</span></span>
4. <span data-ttu-id="6366f-130">I fältet **Lägg till roller i projekt** i fältet **Roll** väljer du **chefsprojektledare**.</span><span class="sxs-lookup"><span data-stu-id="6366f-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="6366f-131">Välj **nödvändig kompetens**.</span><span class="sxs-lookup"><span data-stu-id="6366f-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="6366f-132">På sidan **Välj egenskaper** är de egenskaper som du tidigare angett för rollen chefsprojektledare markerad som standard.</span><span class="sxs-lookup"><span data-stu-id="6366f-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="6366f-133">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="6366f-133">Select **OK**.</span></span>
7. <span data-ttu-id="6366f-134">På sidan **Lägg till roller i projekt** i fältet **Antal resurser** ange **1**.</span><span class="sxs-lookup"><span data-stu-id="6366f-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="6366f-135">I fältet **resurs** visas alla resurser som har nödvändig kompetens i sökningen.</span><span class="sxs-lookup"><span data-stu-id="6366f-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="6366f-136">Välj **Daniel Goldschmidt** och välj sedan **Skapa**.</span><span class="sxs-lookup"><span data-stu-id="6366f-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="6366f-137">På sidan **Projekt** välj **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="6366f-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="6366f-138">I fältet **Lägg till roller i projekt** i fältet **Roll** väljer du **teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="6366f-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="6366f-139">Ange **5** i fältet **Antal resurser**.</span><span class="sxs-lookup"><span data-stu-id="6366f-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="6366f-140">Välj **Skapa**.</span><span class="sxs-lookup"><span data-stu-id="6366f-140">Select **Create**.</span></span>
12. <span data-ttu-id="6366f-141">På sidan **projekt** väljer du **uppfylla resurser**.</span><span class="sxs-lookup"><span data-stu-id="6366f-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="6366f-142">Övervaka projektteam</span><span class="sxs-lookup"><span data-stu-id="6366f-142">Monitor project teams</span></span>
1. <span data-ttu-id="6366f-143">På sidan **All projekt** välj länken **projekt-ID** för projekt **XYZ uppgradering fas 2**.</span><span class="sxs-lookup"><span data-stu-id="6366f-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="6366f-144">Snabbflik **Projektgrupp och schemaläggning**, verifiera att de projektresurser som anges är korrekta.</span><span class="sxs-lookup"><span data-stu-id="6366f-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]