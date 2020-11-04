---
title: Synkronisera projektutgiftskategorier mellan Finance and Operations och Project Service Automation
description: I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera projektets utgiftskategorier mellan från Microsoft Dynamics 365 Finance och Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085679"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="59f59-103">Synkronisera projektutgiftskategorier mellan Finance and Operations och Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59f59-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="59f59-104">I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera projektets utgiftskategorier mellan från Dynamics 365 Finance och Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59f59-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="59f59-105">OProjektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="59f59-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="59f59-106">Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.</span><span class="sxs-lookup"><span data-stu-id="59f59-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="59f59-107">Om du använder Enterprise Edition 7.3.0 kan du, efter att du har installerat KB 4132657 och KB 4132660, använda mallarna för att integrera projektuppgifter, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och faktiska värden samt för att konfigurera låsning av funktioner.</span><span class="sxs-lookup"><span data-stu-id="59f59-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="59f59-108">Om du måste återställa redovisningsfördelningarna bör du även installera KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="59f59-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="59f59-109">Dataflöde för Project Service Automation och Finance</span><span class="sxs-lookup"><span data-stu-id="59f59-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="59f59-110">Project Service Automation och Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="59f59-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="59f59-111">Integreringsmallar som är tillgänglig med funktionen för dataintegrering gör det möjligt för dataflöde om kategorier för utgiftstransaktioner för projekt mellan Finance och Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59f59-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="59f59-112">Om projektutgiftskategorierna är sammanställda i Finance är integrationsflödet först inställt på Finance till Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59f59-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="59f59-113">Integrerings-ID för projektutgiftskategorierna uppdateras sedan med synkroniseringen från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="59f59-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="59f59-114">Om projektutgiftskategorierna är sammanställda i Project Service Automation är integrationsflödet först inställt på Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="59f59-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="59f59-115">Projektkategorierna måste redan vara konfigurerade i Finance innan synkroniseringen mellan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59f59-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="59f59-116">Synkronisera från Finance tillbaka till Project Service Automation och sedan från Project Service Automation till Finance igen.</span><span class="sxs-lookup"><span data-stu-id="59f59-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="59f59-117">På det här sättet kan du garantera att kategorierna är länkade och att inga dubbletter skapas.</span><span class="sxs-lookup"><span data-stu-id="59f59-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="59f59-118">Projektutgiftskategorierna hanteras vanligtvis hanterade i Finance.</span><span class="sxs-lookup"><span data-stu-id="59f59-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="59f59-119">Om de inte är det, eller om utgiftskategorier redan har skapats i Project Service Automation, måste du först synkronisera med hjälp av transaktionskategorier för projektutgifter (PSA till Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="59f59-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="59f59-120">Synkronisera sedan med hjälp av mallen för transaktionskategorier för projektutgifter (Fin and Ops till PSA).</span><span class="sxs-lookup"><span data-stu-id="59f59-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="59f59-121">Kör sedan synkroniseringen från Project Service Automation till Finance en gång till.</span><span class="sxs-lookup"><span data-stu-id="59f59-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="59f59-122">Om du synkroniserar först från Project Service Automation måste följande krav uppfyllas i Finance innan synkroniseringen körs:</span><span class="sxs-lookup"><span data-stu-id="59f59-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="59f59-123">Den delade kategorin som överensstämmer med projektkategorin som är inställd i Project Service Automation måste finnas och måste vara aktiverad för både **projekt** och **utgift**.</span><span class="sxs-lookup"><span data-stu-id="59f59-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="59f59-124">För varje juridisk person i Finance som måste vara integrerad med måste följande projektkategorier finnas:</span><span class="sxs-lookup"><span data-stu-id="59f59-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="59f59-125">**Projektkategorin** finns.</span><span class="sxs-lookup"><span data-stu-id="59f59-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="59f59-126">**Användning i utgift** har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="59f59-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="59f59-127">**Aktiv i journal** har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="59f59-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="59f59-128">**Transaktionstyp** har värdet **utgift**.</span><span class="sxs-lookup"><span data-stu-id="59f59-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="59f59-129">Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.</span><span class="sxs-lookup"><span data-stu-id="59f59-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="59f59-130">[![Dataflöde för Project Service Automation-integrering med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="59f59-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="59f59-131">Synkronisering av projektutgiftskategorier från Finance till Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59f59-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="59f59-132">Mall och uppgift</span><span class="sxs-lookup"><span data-stu-id="59f59-132">Template and task</span></span>

<span data-ttu-id="59f59-133">Om du vill öppna mallen går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.</span><span class="sxs-lookup"><span data-stu-id="59f59-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="59f59-134">Följande mall och underliggande uppgift som används för att synkronisera projektutgiftskategorier från Finance till Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="59f59-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="59f59-135">**Namn på mallen i dataintegrering:** transaktionskategorier för projektutgifter (Fin and Ops till PSA)</span><span class="sxs-lookup"><span data-stu-id="59f59-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="59f59-136">**Namn på uppgiften i projektet:** synkroniserar kategorier till PSA</span><span class="sxs-lookup"><span data-stu-id="59f59-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="59f59-137">Entitetsuppsättning</span><span class="sxs-lookup"><span data-stu-id="59f59-137">Entity set</span></span>

| <span data-ttu-id="59f59-138">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="59f59-138">Finance</span></span>                           | <span data-ttu-id="59f59-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59f59-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="59f59-140">Integreringsentitet för kategorier</span><span class="sxs-lookup"><span data-stu-id="59f59-140">Integration entity for categories</span></span> | <span data-ttu-id="59f59-141">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="59f59-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="59f59-142">Entitetsflöde</span><span class="sxs-lookup"><span data-stu-id="59f59-142">Entity flow</span></span>

<span data-ttu-id="59f59-143">Projektutgiftskategorier hanteras i Finance och synkroniseras till Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="59f59-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="59f59-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="59f59-144">Power Query</span></span>

<span data-ttu-id="59f59-145">När du synkroniserar med Project Service Automation måste du använda Microsoft Power Query for Excel för att ange faktureringstyp i transaktionskategorin.</span><span class="sxs-lookup"><span data-stu-id="59f59-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="59f59-146">Kategorierna för projektutgiftstransaktioner mallen (Fin och Ops to PSA) tillhandahåller en standardkolumn och mappning.</span><span class="sxs-lookup"><span data-stu-id="59f59-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="59f59-147">Om du skapar en egen mall måste du lägga till en villkorskolumn i Power Query.</span><span class="sxs-lookup"><span data-stu-id="59f59-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="59f59-148">Följ stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="59f59-148">Follow these steps.</span></span>

1. <span data-ttu-id="59f59-149">Klicka på pilen om du vill öppna mappningen av aktiviteten projektutgiftskategorier i mallen Projektutgiftskategorier (Fin and Ops till PSA).</span><span class="sxs-lookup"><span data-stu-id="59f59-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="59f59-150">Klicka på länken **Avancerad fråga och filtrering** för att öppna Power Query.</span><span class="sxs-lookup"><span data-stu-id="59f59-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="59f59-151">Välj **Lägg till villkorlig kolumn**.</span><span class="sxs-lookup"><span data-stu-id="59f59-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="59f59-152">Ange ett namn för den nya kolumnen t.ex. **Faktureringstyp**.</span><span class="sxs-lookup"><span data-stu-id="59f59-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="59f59-153">Ange följande villkor: **om CATEGORYID inte är null 19235001, annars null**.</span><span class="sxs-lookup"><span data-stu-id="59f59-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="59f59-154">Klicka på **OK** i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="59f59-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="59f59-155">Kontrollera att du mappar den nya kolumnen på mappningssidan.</span><span class="sxs-lookup"><span data-stu-id="59f59-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="59f59-156">I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="59f59-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="59f59-157">Mappningen visar fältinformationen som ska synkroniseras från Finance till Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59f59-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="59f59-158">[![Projektutgiftskategori till mallmappning av Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="59f59-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="59f59-159">Synkronisering av projektutgiftskategorier från Project Service Automation till Finance</span><span class="sxs-lookup"><span data-stu-id="59f59-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="59f59-160">Mall och uppgift</span><span class="sxs-lookup"><span data-stu-id="59f59-160">Template and task</span></span>

<span data-ttu-id="59f59-161">Följande mall och underliggande uppgift som används för att synkronisera projektutgiftskategorier från Project Service Automation till Finance:</span><span class="sxs-lookup"><span data-stu-id="59f59-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="59f59-162">**Namn på mallen i dataintegrering:** transaktionskategorier för projektutgifter (PSA till Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="59f59-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="59f59-163">**Namn på uppgiften i projektet:** synkroniserar kategorier till Fin Ops</span><span class="sxs-lookup"><span data-stu-id="59f59-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="59f59-164">Entitetsuppsättning</span><span class="sxs-lookup"><span data-stu-id="59f59-164">Entity set</span></span>

| <span data-ttu-id="59f59-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59f59-165">Project Service Automation</span></span> | <span data-ttu-id="59f59-166">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="59f59-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="59f59-167">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="59f59-167">Transaction categories</span></span>     | <span data-ttu-id="59f59-168">Integreringsentitet för kategorier</span><span class="sxs-lookup"><span data-stu-id="59f59-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="59f59-169">Entitetsflöde</span><span class="sxs-lookup"><span data-stu-id="59f59-169">Entity flow</span></span>

<span data-ttu-id="59f59-170">Projektutgiftskategorier hanteras i Finance och synkroniseras till Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="59f59-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="59f59-171">Synkroniseringen tillbaka till Finance uppdaterar projektkategorin i Finance med integrations-ID från Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59f59-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="59f59-172">Mallgrupp i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="59f59-172">Template mapping in Data integration</span></span>

<span data-ttu-id="59f59-173">I följande illustration visas ett exempel på hur du mappar malluppgifter i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="59f59-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="59f59-174">Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.</span><span class="sxs-lookup"><span data-stu-id="59f59-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="59f59-175">[![Project Service Automation till Finance-mallmappning](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="59f59-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
