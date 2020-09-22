---
title: Översikt över Project Service Automation
description: I det här ämnet finns information om Dynamics 365 Project Service Automation till Dynamics 365 Finance-lösningen.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756238"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="e271d-103">Översikt över Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e271d-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e271d-104">Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Dynamics 365 Finance och Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e271d-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="e271d-105">Med hjälp av integreringsmallarna som är tillgängliga med funktionen för dataintegrering kan du aktivera projekt-, projektkontrakt och projektkontraktrader, milstolpar i projekt, projektuppgifter, kategorier av utgiftstransaktioner, timuppskattningar och utgiftsuppskattningar från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e271d-106">Om du använder version 7.3.0 måste du installera KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="e271d-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="e271d-107">Du kan sedan integrera projekt med fast pris.</span><span class="sxs-lookup"><span data-stu-id="e271d-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="e271d-108">Om du använder version 7.3.0 och kopplar avgiftstransaktioner över från Project Service Automation måste du installera KB 4345320 för att kunna ta med avgifterna i projektfakturan.</span><span class="sxs-lookup"><span data-stu-id="e271d-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="e271d-109">Om du använder version 8.0 kan du använda integrering av projektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning.</span><span class="sxs-lookup"><span data-stu-id="e271d-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="e271d-110">Om du använder version 8.0.1 eller senare kan du synkronisera verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="e271d-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="e271d-111">Innan du kan integrera Project Service Automation till Finance måste du konfigurera integreringsparametrarna för Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e271d-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="e271d-112">Mer information finns i [integreringsparametrar för Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e271d-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="e271d-113">Den här integreringslösningen möjliggör direkt synkronisering i följande situationer:</span><span class="sxs-lookup"><span data-stu-id="e271d-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="e271d-114">Underhåll projektkontrakt i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-115">Skapa projekt i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-116">Underhåll projektkontraktrader i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-117">Underhåll milstolpar för projektkontraktrader i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-118">Underhåll projektuppgifter i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-119">Underhåll kategorier för utgiftstransaktioner i Finance och synkronisera dem direkt från Finance till Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e271d-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="e271d-120">Skapa uppskattning av projekttid i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-121">Skapa uppskattning av projektutgift i Project Service Automation och synkronisera dem direkt från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="e271d-122">Skapa för projekttid, utgift och faktiska avgifter Project Service Automation och skapa projekttransaktion i Project Service Automation integreringsjournal så att de kan bokföras i Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="e271d-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="e271d-123">Data synchronization</span></span>

<span data-ttu-id="e271d-124">Följande illustration visar hur datasynkroniseras som en del av integrationen mellan Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="e271d-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="e271d-125">Alla mallar är inte tillgängliga för tillfället.</span><span class="sxs-lookup"><span data-stu-id="e271d-125">Not all templates are currently available.</span></span> <span data-ttu-id="e271d-126">Mallarna kommer att publiceras när de slutförts.</span><span class="sxs-lookup"><span data-stu-id="e271d-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="e271d-127">[![Project Service Automation-integrering med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="e271d-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="e271d-128">Systemkrav för Finance</span><span class="sxs-lookup"><span data-stu-id="e271d-128">System requirements for Finance</span></span>

<span data-ttu-id="e271d-129">Om du vill använda Project Service Automation till Finance integreringslösningen måste du installera Enterprise Edition 7.3 med plattformsuppdatering 12 eller senare.</span><span class="sxs-lookup"><span data-stu-id="e271d-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="e271d-130">Systemkrav för Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e271d-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="e271d-131">Om du vill använda integreringslösningen Project Service Automation till Finance måste du installera följande komponenter:</span><span class="sxs-lookup"><span data-stu-id="e271d-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="e271d-132">Dynamics 365 Project Service Automation version 9.0.0.0 eller senare</span><span class="sxs-lookup"><span data-stu-id="e271d-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="e271d-133">Lösningen potentiell kund till kontant för Dynamics 365 Sales, version 1.14.0.0 (v14) eller senare</span><span class="sxs-lookup"><span data-stu-id="e271d-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="e271d-134">Project Service Automation till Finance-lösning för Dynamics 365 Project Service Automation version 1.0.0.0 eller senare</span><span class="sxs-lookup"><span data-stu-id="e271d-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="e271d-135">Installera integreringslösningen Project Service Automation till Finance i Project Service Automation-instansen</span><span class="sxs-lookup"><span data-stu-id="e271d-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="e271d-136">Hämta integreringslösningen Project Service Automation till Finance från [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) och följ anvisningarna i lösningen.</span><span class="sxs-lookup"><span data-stu-id="e271d-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
