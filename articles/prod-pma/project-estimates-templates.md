---
title: Synkronisera projektberäkningar direkt från Project Service Automation till Finance and Operations
description: I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera uppskattning av projekttid och uppskattning av projektutgift direkt från Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Finance.
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
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085668"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="459dd-103">Synkronisera projektberäkningar direkt från Project Service Automation till Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="459dd-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="459dd-104">I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera uppskattning av projekttid och uppskattning av projektutgift direkt från Dynamics 365 Project Service Automation till Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="459dd-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="459dd-105">Projektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="459dd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="459dd-106">Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.</span><span class="sxs-lookup"><span data-stu-id="459dd-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="459dd-107">Dataflöde för Project Service Automation till Finance</span><span class="sxs-lookup"><span data-stu-id="459dd-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="459dd-108">Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="459dd-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="459dd-109">Integreringsmallar som är tillgänglig med funktionen för dataintegrering gör det möjligt för dataflöde timberäkningar och projektutgiftsberäkningar från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="459dd-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="459dd-110">Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="459dd-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="459dd-111">[![Dataflöde för Project Service Automation-integrering med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="459dd-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="459dd-112">Projekttimberäkningar</span><span class="sxs-lookup"><span data-stu-id="459dd-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="459dd-113">Mall och uppgifter</span><span class="sxs-lookup"><span data-stu-id="459dd-113">Template and tasks</span></span>

<span data-ttu-id="459dd-114">Om du vill öppna tillgängligare mallar går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.</span><span class="sxs-lookup"><span data-stu-id="459dd-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="459dd-115">Följande mall och underliggande uppgift som används för att synkronisera uppskattning av projekttid direkt från Project Service Automation till Finance:</span><span class="sxs-lookup"><span data-stu-id="459dd-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="459dd-116">**Namn på mallen i dataintegrering:** projekttimberäkningar (PSA till Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="459dd-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="459dd-117">**Namn på aktiviteterna i projektet:**</span><span class="sxs-lookup"><span data-stu-id="459dd-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="459dd-118">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="459dd-118">Transaction relationships</span></span>
    - <span data-ttu-id="459dd-119">Utgiftsberäkningar</span><span class="sxs-lookup"><span data-stu-id="459dd-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="459dd-120">Entitetsuppsättning</span><span class="sxs-lookup"><span data-stu-id="459dd-120">Entity set</span></span>

| <span data-ttu-id="459dd-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="459dd-121">Project Service Automation</span></span> | <span data-ttu-id="459dd-122">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="459dd-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="459dd-123">Projektuppgifter</span><span class="sxs-lookup"><span data-stu-id="459dd-123">Project tasks</span></span>              | <span data-ttu-id="459dd-124">Integreringsentitet för uppskattning av projekttid</span><span class="sxs-lookup"><span data-stu-id="459dd-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="459dd-125">Entitetsflöde</span><span class="sxs-lookup"><span data-stu-id="459dd-125">Entity flow</span></span>

<span data-ttu-id="459dd-126">Projekttimberäkningar i Project Service Automation och synkroniseras med att Finance som prognosen för projekttid.</span><span class="sxs-lookup"><span data-stu-id="459dd-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="459dd-127">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="459dd-127">Prerequisites</span></span>

<span data-ttu-id="459dd-128">Innan du kan utföra en synkronisering av uppskattningar av projekttimmar måste du synkronisera projekt, projektaktiviteter och transaktionskategorier för projektutgifter.</span><span class="sxs-lookup"><span data-stu-id="459dd-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="459dd-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="459dd-129">Power Query</span></span>

<span data-ttu-id="459dd-130">I mallen uppskattning av projekttid måste du använda Microsoft Power Query för Excel för att utföra de här uppgifterna:</span><span class="sxs-lookup"><span data-stu-id="459dd-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="459dd-131">Ange standard prognosmodell-ID som används när integreringen skapar nya timprognoser.</span><span class="sxs-lookup"><span data-stu-id="459dd-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="459dd-132">Filtrera bort eventuella resursspecifika poster i den aktivitet som inte ska integreras i timprognoser.</span><span class="sxs-lookup"><span data-stu-id="459dd-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="459dd-133">Filtrera bort tomma rader för transaktionskategori.</span><span class="sxs-lookup"><span data-stu-id="459dd-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="459dd-134">Om du inte slutför den här uppgiften kan timprognoser bli ogiltiga.</span><span class="sxs-lookup"><span data-stu-id="459dd-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="459dd-135">Ange standard modell-ID för prognos</span><span class="sxs-lookup"><span data-stu-id="459dd-135">Set the default forecast model ID</span></span>

<span data-ttu-id="459dd-136">Du uppdaterar standard modell-ID för prognos genom att klicka på pilen **mappning** för att öppna mappningen.</span><span class="sxs-lookup"><span data-stu-id="459dd-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="459dd-137">Välj sedan länken **Avancerad fråga och filtrering**.</span><span class="sxs-lookup"><span data-stu-id="459dd-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="459dd-138">Om du använder standardmallen projekttimberäkningar (PSA till Fin and Ops) välj **Infogade villkoret** i listan **Använda steg**.</span><span class="sxs-lookup"><span data-stu-id="459dd-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="459dd-139">I inmatningen **Funktion** ersätt **O\_prognos** med namnet på det modell-ID för prognos som ska användas tillsammans med integrationen.</span><span class="sxs-lookup"><span data-stu-id="459dd-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="459dd-140">Standardmallen har ett prognosmodell-ID från demonstrationsdata.</span><span class="sxs-lookup"><span data-stu-id="459dd-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="459dd-141">Om du skapar en ny mall måste du lägga till den här kolumnen.</span><span class="sxs-lookup"><span data-stu-id="459dd-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="459dd-142">I Power Query, välj **Lägg till villkorlig kolumn** och ange ett namn för den nya kolumnen, t.ex. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="459dd-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="459dd-143">Ange villkoret för kolumnen där, om projektuppgiften inte är null, så \<enter the forecast model ID\>, annars null.</span><span class="sxs-lookup"><span data-stu-id="459dd-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="459dd-144">Filtrera bort specifika resursposter</span><span class="sxs-lookup"><span data-stu-id="459dd-144">Filter out resource-specific records</span></span>

<span data-ttu-id="459dd-145">Mallen projekttimberäkningar (PSA till Fin and Ops) har ett standardfilter som tar bort eventuella resursbaserade poster.</span><span class="sxs-lookup"><span data-stu-id="459dd-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="459dd-146">Om du skapar en egen mall måste du lägga till filtret.</span><span class="sxs-lookup"><span data-stu-id="459dd-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="459dd-147">Välj den länken **avancerade frågan och filtrering** för att filtrera kolumnen **msdyn\_islinetask** så att endast **falska** poster tas med.</span><span class="sxs-lookup"><span data-stu-id="459dd-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="459dd-148">Filtrera bort tomma rader för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="459dd-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="459dd-149">Du måste lägga till ett filter om du vill ta bort rader som har tomma transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="459dd-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="459dd-150">Den här uppgiften krävs oavsett om du använder standardmallen eller skapar en egen mall.</span><span class="sxs-lookup"><span data-stu-id="459dd-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="459dd-151">Det här filtret tar bort sammanfattningsrader från Project Service Automation som kan resultera i att timuppskattningarna i Finance blir felaktiga.</span><span class="sxs-lookup"><span data-stu-id="459dd-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="459dd-152">Välj länken **Avancerad fråga och filter** om du vill filtrera bort null-poster i kolumnen **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="459dd-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="459dd-153">Mallgrupp i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="459dd-153">Template mapping in Data integration</span></span>

<span data-ttu-id="459dd-154">I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="459dd-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="459dd-155">Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="459dd-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="459dd-156">[![Malluppgiftsmappning i dataintegration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="459dd-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="459dd-157">Beräkning av projektutgifter</span><span class="sxs-lookup"><span data-stu-id="459dd-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="459dd-158">Mall och uppgifter</span><span class="sxs-lookup"><span data-stu-id="459dd-158">Template and tasks</span></span>

<span data-ttu-id="459dd-159">Följande mall och underliggande uppgift som används för att synkronisera uppskattning av projektutgifter direkt från Project Service Automation till Finance:</span><span class="sxs-lookup"><span data-stu-id="459dd-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="459dd-160">**Namn på mallen i dataintegrering:** uppskattning av projektutgifter (PSA till Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="459dd-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="459dd-161">**Namn på aktiviteterna i projektet:**</span><span class="sxs-lookup"><span data-stu-id="459dd-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="459dd-162">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="459dd-162">Transaction relationships</span></span> 
    - <span data-ttu-id="459dd-163">Utgiftsberäkningar</span><span class="sxs-lookup"><span data-stu-id="459dd-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="459dd-164">Entitetsuppsättning</span><span class="sxs-lookup"><span data-stu-id="459dd-164">Entity set</span></span>

| <span data-ttu-id="459dd-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="459dd-165">Project Service Automation</span></span> | <span data-ttu-id="459dd-166">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="459dd-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="459dd-167">Transaktionskopplingar</span><span class="sxs-lookup"><span data-stu-id="459dd-167">Transaction Connections</span></span>    | <span data-ttu-id="459dd-168">Integrationsentitet för projekttransaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="459dd-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="459dd-169">Beräkningsrader</span><span class="sxs-lookup"><span data-stu-id="459dd-169">Estimate Lines</span></span>             | <span data-ttu-id="459dd-170">Integreringsentitet för uppskattning av projektutgifter</span><span class="sxs-lookup"><span data-stu-id="459dd-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="459dd-171">Entitetsflöde</span><span class="sxs-lookup"><span data-stu-id="459dd-171">Entity flow</span></span>

<span data-ttu-id="459dd-172">Uppskattning av projektutgifter i Project Service Automation och synkroniseras med att Finance som uppskattning av projektutgifter.</span><span class="sxs-lookup"><span data-stu-id="459dd-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="459dd-173">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="459dd-173">Prerequisites</span></span>

<span data-ttu-id="459dd-174">Innan du kan utföra en synkronisering av uppskattning av projektutgifter måste du synkronisera projekt, projektaktiviteter och transaktionskategorier för projektutgifter.</span><span class="sxs-lookup"><span data-stu-id="459dd-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="459dd-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="459dd-175">Power Query</span></span>

<span data-ttu-id="459dd-176">I mallen uppskattning av projektutgifter av verkliga värden måste du använda Power Query för att utföra följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="459dd-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="459dd-177">Filtrera så att endast radposter för uppskattning av projekt.</span><span class="sxs-lookup"><span data-stu-id="459dd-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="459dd-178">Ange standard prognosmodell-ID som används när integreringen skapar nya timprognoser.</span><span class="sxs-lookup"><span data-stu-id="459dd-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="459dd-179">Omvandla faktureringstyperna.</span><span class="sxs-lookup"><span data-stu-id="459dd-179">Transform the billing types.</span></span>
- <span data-ttu-id="459dd-180">Omvandla transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="459dd-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="459dd-181">Filtrera så att endast för uppskattning av utgiftsrader</span><span class="sxs-lookup"><span data-stu-id="459dd-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="459dd-182">Mallen beräkning av projektutgifter (PSA till Fin and Ops) har ett standardfilter som endast innehåller utgiftsrader i integrationen.</span><span class="sxs-lookup"><span data-stu-id="459dd-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="459dd-183">Om du skapar en egen mall måste du lägga till filtret.</span><span class="sxs-lookup"><span data-stu-id="459dd-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="459dd-184">Välj uppgiften **transaktionsrelationer** och klicka sedan på pilen **Mappning**.</span><span class="sxs-lookup"><span data-stu-id="459dd-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="459dd-185">Välj länken **Avancerad fråga och filtrering**.</span><span class="sxs-lookup"><span data-stu-id="459dd-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="459dd-186">Filtrera kolumnen **msdyn\_transactiontype1** så att den endast innehåller **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="459dd-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="459dd-187">Ange standard modell-ID för prognos</span><span class="sxs-lookup"><span data-stu-id="459dd-187">Set the default forecast model ID</span></span>

<span data-ttu-id="459dd-188">Du uppdaterar standard modell-ID för prognos genom att välja uppgiften **Utgiftsberäkningar** och klicka sedan pilen **Mappning** för att öppna mappningen.</span><span class="sxs-lookup"><span data-stu-id="459dd-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="459dd-189">Välj länken **Avancerad fråga och filtrering**.</span><span class="sxs-lookup"><span data-stu-id="459dd-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="459dd-190">Om du använder mallen uppskattning av projektutgifter (PSA till Fin and Ops) i Power Query, välj det första **Infogade villkoret** från **Använda steg**.</span><span class="sxs-lookup"><span data-stu-id="459dd-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="459dd-191">I inmatningen **Funktion** ersätt **O\_prognos** med namnet på det modell-ID för prognos som ska användas tillsammans med integrationen.</span><span class="sxs-lookup"><span data-stu-id="459dd-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="459dd-192">Standardmallen har ett prognosmodell-ID från demonstrationsdata.</span><span class="sxs-lookup"><span data-stu-id="459dd-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="459dd-193">Om du skapar en ny mall måste du lägga till den här kolumnen.</span><span class="sxs-lookup"><span data-stu-id="459dd-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="459dd-194">I Power Query, välj **Lägg till villkorlig kolumn** och ange ett namn för den nya kolumnen, t.ex. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="459dd-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="459dd-195">Ange villkoret för kolumnen där, om ID för uppskattningsrad inte är null, så \<enter the forecast model ID\>, annars null.</span><span class="sxs-lookup"><span data-stu-id="459dd-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="459dd-196">Omvandla faktureringstyperna</span><span class="sxs-lookup"><span data-stu-id="459dd-196">Transform the billing types</span></span>

<span data-ttu-id="459dd-197">Mallen beräkning av projektutgifter (PSA till Fin and Ops) innehåller en villkorlig kolumn som används för att omvandla de faktureringstyper som tas emot från Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="459dd-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="459dd-198">Om du skapar en egen mall måste du lägga till villkorlig kolumn.</span><span class="sxs-lookup"><span data-stu-id="459dd-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="459dd-199">Välj länken **Avancerad fråga och filtrering** och välj sedan **Lägg till villkorlig kolumn**.</span><span class="sxs-lookup"><span data-stu-id="459dd-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="459dd-200">Ange ett namn för den nya kolumnen t.ex. **Faktureringstyp**.</span><span class="sxs-lookup"><span data-stu-id="459dd-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="459dd-201">Ange därefter följande villkor:</span><span class="sxs-lookup"><span data-stu-id="459dd-201">Then enter the following condition:</span></span>

<span data-ttu-id="459dd-202">Om **msdyn\_billingtype** = 192350000, sedan **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="459dd-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="459dd-203">else if **msdyn\_billingtype** = 192350001, sedan **Debiterbar**</span><span class="sxs-lookup"><span data-stu-id="459dd-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="459dd-204">else if **msdyn\_billingtype** = 192350002, sedan **Kostnadsfri**</span><span class="sxs-lookup"><span data-stu-id="459dd-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="459dd-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="459dd-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="459dd-206">Omvandla transaktionstyper</span><span class="sxs-lookup"><span data-stu-id="459dd-206">Transform the transaction types</span></span>

<span data-ttu-id="459dd-207">Mallen beräkning av projektutgifter (PSA till Fin and Ops) innehåller en villkorlig kolumn som används för att omvandla de transaktionstyper som tas emot från Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="459dd-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="459dd-208">Om du skapar en egen mall måste du lägga till villkorlig kolumn.</span><span class="sxs-lookup"><span data-stu-id="459dd-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="459dd-209">Välj länken **Avancerad fråga och filtrering** och välj sedan **Lägg till villkorlig kolumn**.</span><span class="sxs-lookup"><span data-stu-id="459dd-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="459dd-210">Ange ett namn för den nya kolumnen t.ex. **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="459dd-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="459dd-211">Ange därefter följande villkor:</span><span class="sxs-lookup"><span data-stu-id="459dd-211">Then enter the following condition:</span></span>

<span data-ttu-id="459dd-212">Om **msdyn\_transactiontypecode** = 192350000, sedan **Kostnad**</span><span class="sxs-lookup"><span data-stu-id="459dd-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="459dd-213">else if **msdyn\_transactiontypecode** = 192350005, sedan **Försäljning**</span><span class="sxs-lookup"><span data-stu-id="459dd-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="459dd-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="459dd-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="459dd-215">Mallgrupp i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="459dd-215">Template mapping in Data integration</span></span>

<span data-ttu-id="459dd-216">I följande illustration visas exempel på hur du mappar malluppgifter i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="459dd-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="459dd-217">Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="459dd-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="459dd-218">[![Mallmappning av transaktioner av utgiftsuppskattning](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="459dd-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="459dd-219">[![Mallmappning av utgiftsuppskattningar](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="459dd-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
