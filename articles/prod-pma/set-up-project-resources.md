---
title: Konfigurera projektresurser
description: I det här ämnet finns information om hur du konfigurerar eller begär projektresurser.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085712"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="93505-103">Konfigurera projektresurser</span><span class="sxs-lookup"><span data-stu-id="93505-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93505-104">Du måste ange en kalender och associera den med en medarbetare eller arbetare.</span><span class="sxs-lookup"><span data-stu-id="93505-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="93505-105">Kalendern används för att schemalägga projektet och arbetstiden för de resurser som reserveras för projektet.</span><span class="sxs-lookup"><span data-stu-id="93505-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="93505-106">Under kalenderinstallationen kan projektledarna göra resursutjämning som en del av resursoptimeringen.</span><span class="sxs-lookup"><span data-stu-id="93505-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="93505-107">Begränsningar kan anges för resurser utifrån kalenderschemat.</span><span class="sxs-lookup"><span data-stu-id="93505-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="93505-108">Du kan skapa en kalender på sidan **kalendrar**.</span><span class="sxs-lookup"><span data-stu-id="93505-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="93505-109">När du konfigurerar en arbetare som en projektresurs kan du välja bland arbetare som arbetar i det företag som du konfigurerar resurser för.</span><span class="sxs-lookup"><span data-stu-id="93505-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="93505-110">Alternativt kan du välja arbetare från andra företag i organisationen.</span><span class="sxs-lookup"><span data-stu-id="93505-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="93505-111">Dessa arbetare kallas för koncerninterna resurser.</span><span class="sxs-lookup"><span data-stu-id="93505-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="93505-112">I följande procedurer förklaras hur du konfigurerar en arbetare som en projektresurs i företaget och hur du skapar en koncernintern projektresurs.</span><span class="sxs-lookup"><span data-stu-id="93505-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="93505-113">Konfigurera en arbetare som en projektresurs</span><span class="sxs-lookup"><span data-stu-id="93505-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="93505-114">På sidan **arbetare** i listan **arbetare** väljer du den arbetare som du vill lägga till som en projektresurs i listan arbetare och öppnar sedan arbetarens post.</span><span class="sxs-lookup"><span data-stu-id="93505-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="93505-115">I åtgärdsfönstret, välj **Projekt** &gt; **Inställning** &gt; **Projektinställningar**.</span><span class="sxs-lookup"><span data-stu-id="93505-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="93505-116">Välj en kalender och stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="93505-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="93505-117">Du kan även ange standardprojekt för en resurs som en typ av förtilldelning.</span><span class="sxs-lookup"><span data-stu-id="93505-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="93505-118">Förtilldelningar kan användas när resurs chefen eller projektledaren vet vilka projektresursen kommer att arbeta i förväg.</span><span class="sxs-lookup"><span data-stu-id="93505-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="93505-119">Förtilldelningar kan också baseras på en förfrågan från en projekt sponsor eller kund.</span><span class="sxs-lookup"><span data-stu-id="93505-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="93505-120">Om du vill förtilldela ett projekt fördelat på sidan **Tilldela projekt** på fliken **Projekt** i listan **Återstående projekt** välj lämpligt projekt.</span><span class="sxs-lookup"><span data-stu-id="93505-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="93505-121">Konfigurera en koncernintern resurs</span><span class="sxs-lookup"><span data-stu-id="93505-121">Set up an intercompany resource</span></span>

<span data-ttu-id="93505-122">När du konfigurerar en arbetare som en koncernintern resurs måste du fylla i inställningarna både i långivande bolaget och låntagande bolaget.</span><span class="sxs-lookup"><span data-stu-id="93505-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="93505-123">I långivande bolaget</span><span class="sxs-lookup"><span data-stu-id="93505-123">In the lending company</span></span>

1. <span data-ttu-id="93505-124">I Finance kontrollera att långivande bolaget är valt och slutför proceduren i det föregående avsnittet "Konfigurera en arbetare som projektresurs".</span><span class="sxs-lookup"><span data-stu-id="93505-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="93505-125">På sidan **Koncernintern redovisning** klicka på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="93505-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="93505-126">I fältet **juridisk person-ID** välj långivande bolag.</span><span class="sxs-lookup"><span data-stu-id="93505-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="93505-127">Fyll i de återstående fälten efter behov och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="93505-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="93505-128">På sidan **Överföringspris** klicka på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="93505-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="93505-129">I fältet **låntagande juridisk person** välj rätt bolag.</span><span class="sxs-lookup"><span data-stu-id="93505-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="93505-130">Om du vill låna ut till det låntagande bolaget endast till den resurs du skapade i början av det här avsnittet markerar du i fältet **resurs** namnet på den resurs som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="93505-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="93505-131">För att göra alla resurser i det långivande bolaget tillgängligt för det låntagande bolaget, lämna fältet **Resurs** tom.</span><span class="sxs-lookup"><span data-stu-id="93505-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="93505-132">På sidan **Projektledning och redovisningsparametrar** på fliken **Koncerninternt** ange alternativet **Aktivera koncernintern resursschemaläggning och tidrapport** till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="93505-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="93505-133">I låntagande bolaget</span><span class="sxs-lookup"><span data-stu-id="93505-133">In the borrowing company</span></span>

- <span data-ttu-id="93505-134">På sidan **Resurslista** i sökfiltret ange namnet på den resurs som du skapade för det långivande bolaget för att verifiera att namnet ingår i resurslistan för det långivande bolaget.</span><span class="sxs-lookup"><span data-stu-id="93505-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="93505-135">Begär projektresurser</span><span class="sxs-lookup"><span data-stu-id="93505-135">Request project resources</span></span>
<span data-ttu-id="93505-136">Med funktionerna för schemaläggning av projektresurser kan du bara distribuera personalresurser för åtaganden eller projekt.</span><span class="sxs-lookup"><span data-stu-id="93505-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="93505-137">Aktivera den här funktionen genom att utföra följande uppgifter eller kontrollera att de har slutförts:</span><span class="sxs-lookup"><span data-stu-id="93505-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="93505-138">Ställ in nummerserier.</span><span class="sxs-lookup"><span data-stu-id="93505-138">Set up number sequences.</span></span>
- <span data-ttu-id="93505-139">Ställ in arbetsflöden för projekthantering och redovisning.</span><span class="sxs-lookup"><span data-stu-id="93505-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="93505-140">Aktivera arbetsflöden för resursförfrågan.</span><span class="sxs-lookup"><span data-stu-id="93505-140">Enable resource request workflows.</span></span>

<span data-ttu-id="93505-141">När föregående aktiviteter har slutförts kan du utföra följande uppgifter som du behöver:</span><span class="sxs-lookup"><span data-stu-id="93505-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="93505-142">Skapa en resursförfrågan från en bemannad resurs med mjuka bokningar.</span><span class="sxs-lookup"><span data-stu-id="93505-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="93505-143">Övervaka resursförfrågningar.</span><span class="sxs-lookup"><span data-stu-id="93505-143">Monitor resource requests.</span></span>
- <span data-ttu-id="93505-144">Uppfyll resursförfrågningar.</span><span class="sxs-lookup"><span data-stu-id="93505-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="93505-145">Begära en personalresurs från en WBS.</span><span class="sxs-lookup"><span data-stu-id="93505-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="93505-146">Boka resurser i ett projekt utan att behöva begära en personalresurs.</span><span class="sxs-lookup"><span data-stu-id="93505-146">Book resources to a project without having a request for a staffed resource.</span></span>
