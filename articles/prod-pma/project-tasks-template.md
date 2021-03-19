---
title: Synkronisera projektuppgifter direkt från Project Service Automation till Finance and Operations
description: I det här ämne beskrivs den mall och underliggande uppgift som används för att synkronisera projektaktiviteter direkt från Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288941"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="4b4ba-103">Synkronisera projektuppgifter direkt från Project Service Automation till Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b4ba-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4b4ba-104">I det här ämne beskrivs den mall och underliggande uppgift som används för att synkronisera projektaktiviteter direkt från Dynamics 365 Project Service Automation till Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="4b4ba-105">OProjektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="4b4ba-106">Om du använder Enterprise Edition 7.3.0 kan du, efter att du har installerat KB 4132657 och KB 4132660, använda mallarna för att integrera projektuppgifter, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och faktiska värden samt för att konfigurera låsning av funktioner.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="4b4ba-107">Om du måste återställa redovisningsfördelningarna bör du även installera KB-4131710.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="4b4ba-108">Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="4b4ba-109">Dataflöde för Project Service Automation till Finance</span><span class="sxs-lookup"><span data-stu-id="4b4ba-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="4b4ba-110">Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="4b4ba-111">Integreringsmallen som är tillgänglig med funktionen för dataintegrering gör det möjligt för dataflöde om projektuppgifter från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4b4ba-112">Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="4b4ba-113">[![Dataflöde för Project Service Automation-integrering med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4b4ba-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4b4ba-114">Mall och uppgift</span><span class="sxs-lookup"><span data-stu-id="4b4ba-114">Template and task</span></span>

<span data-ttu-id="4b4ba-115">Om du vill öppna mallen går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4b4ba-116">Följande mall och underliggande uppgift som används för att synkronisera projektaktiviteter direkt från Project Service Automation till Finance:</span><span class="sxs-lookup"><span data-stu-id="4b4ba-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="4b4ba-117">**Namn på mallen i dataintegrering:** projektuppgifter (PSA till Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4b4ba-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="4b4ba-118">**Namn på aktiviteten i projektet:** projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="4b4ba-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="4b4ba-119">Innan du kan utföra synkronisering av projektuppgifter måste du synkronisera projektkontrakt och projekt.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="4b4ba-120">Entitetsuppsättning</span><span class="sxs-lookup"><span data-stu-id="4b4ba-120">Entity set</span></span>

| <span data-ttu-id="4b4ba-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4b4ba-121">Project Service Automation</span></span> | <span data-ttu-id="4b4ba-122">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="4b4ba-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="4b4ba-123">Projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="4b4ba-123">Project Tasks</span></span>              | <span data-ttu-id="4b4ba-124">Integrationsentitet för projektuppgift</span><span class="sxs-lookup"><span data-stu-id="4b4ba-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="4b4ba-125">Entitetsflöde</span><span class="sxs-lookup"><span data-stu-id="4b4ba-125">Entity flow</span></span>

<span data-ttu-id="4b4ba-126">Projektaktiviteter hanteras i Project Service Automation och synkroniseras med att Finance som projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4b4ba-127">Krav och mappningsinställningar</span><span class="sxs-lookup"><span data-stu-id="4b4ba-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="4b4ba-128">Innan du kan utföra synkronisering av projektuppgifter måste du synkronisera projektkontrakt och projekt.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="4b4ba-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="4b4ba-129">Power Query</span></span>

<span data-ttu-id="4b4ba-130">Du måste använda Microsoft Power Query för Excel för att filtrera data om villkoret uppfylls:</span><span class="sxs-lookup"><span data-stu-id="4b4ba-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="4b4ba-131">Du har resursspecifika poster i en projektaktivitet.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="4b4ba-132">Om du måste använda Power Query följer du den här riktlinjen:</span><span class="sxs-lookup"><span data-stu-id="4b4ba-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="4b4ba-133">Mallen projektaktiviteter (PSA till Fin and Ops) har ett standardfilter som inte innehåller några datorspecifika poster från en projektuppgift genom att ange filtret för **IsLineTask** till **false**.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="4b4ba-134">Om du skapar en egen mall måste du lägga till filtret.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4b4ba-135">Mallgrupp i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="4b4ba-135">Template mapping in Data integration</span></span>

<span data-ttu-id="4b4ba-136">I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="4b4ba-137">Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="4b4ba-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4b4ba-138">[![Mallmappning](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="4b4ba-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]