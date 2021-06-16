---
title: Project Operations mappningsversioner för dubbelriktad skrivning
description: Detta ämne innehåller listan med mappningar med dubbelriktad skrivning som krävs för Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939052"
---
# <a name="project-operations-dual-write-map-versions"></a><span data-ttu-id="39e58-103">Project Operations mappningsversioner för dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="39e58-103">Project Operations dual-write map versions</span></span>

<span data-ttu-id="39e58-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="39e58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="39e58-105">För att använda Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier krävs att en uppsättning mappningar med dubbelriktad skrivning körs i miljön.</span><span class="sxs-lookup"><span data-stu-id="39e58-105">Using Dynamics 365 Project Operations for resource/non-stocked scenarios requires a set of dual-write maps to be running in the environment.</span></span> 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a><span data-ttu-id="39e58-106">Obligatoriska mappningar: Orkestreringslösning för dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="39e58-106">Prerequisite maps: Dual-write orchestration solution</span></span>

<span data-ttu-id="39e58-107">Följande mappningar är obligatoriska för lösningen Project Operations.</span><span class="sxs-lookup"><span data-stu-id="39e58-107">The following maps are required prerequisites for the Project Operations solution.</span></span> <span data-ttu-id="39e58-108">Kör de mappningar som visas i följande tabell och relaterade tabellmappningar i miljön.</span><span class="sxs-lookup"><span data-stu-id="39e58-108">Make sure to run the maps listed in the following table and any related table maps in your environment.</span></span>

| <span data-ttu-id="39e58-109">Tabellmappning</span><span class="sxs-lookup"><span data-stu-id="39e58-109">Table map</span></span> | <span data-ttu-id="39e58-110">Initial synkronisering</span><span class="sxs-lookup"><span data-stu-id="39e58-110">Initial sync</span></span> |
| --- | --- |
| <span data-ttu-id="39e58-111">Huvudbok (msdyn_ledgers)</span><span class="sxs-lookup"><span data-stu-id="39e58-111">Ledger (msdyn_ledgers)</span></span> | <span data-ttu-id="39e58-112">Kräver inledande synkning för tabellmappningen och alla förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="39e58-112">Requires initial sync for the table map and all prerequisites.</span></span> <span data-ttu-id="39e58-113">Master för initial synkning är Finance and Operations-apparna.</span><span class="sxs-lookup"><span data-stu-id="39e58-113">Master for initial sync is Finance and Operations apps.</span></span> |
| <span data-ttu-id="39e58-114">Juridiska entiteter (cdm_companies)</span><span class="sxs-lookup"><span data-stu-id="39e58-114">Legal entities (cdm_companies)</span></span> | <span data-ttu-id="39e58-115">Krävs inte.</span><span class="sxs-lookup"><span data-stu-id="39e58-115">Not required.</span></span> <span data-ttu-id="39e58-116">Systemet fyller automatiskt i den här entiteten när miljöer länkas med dubbelriktad skrivning.</span><span class="sxs-lookup"><span data-stu-id="39e58-116">The system populates this entity automatically when environments are linked using dual-write.</span></span> |
| <span data-ttu-id="39e58-117">Kunder V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="39e58-117">Customers V3 (accounts)</span></span> | <span data-ttu-id="39e58-118">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-118">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-119">Leverantörer V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="39e58-119">Vendors V2 (msdyn_vendors)</span></span> | <span data-ttu-id="39e58-120">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-120">Not required for provisioning.</span></span> |

1. <span data-ttu-id="39e58-121">I mappningslistan väljer du mappningen Huvudbok **(msdyn\_ledgers)** med alla obligatoriska delar och väljer sedan kryssrutan **Initial synkning**.</span><span class="sxs-lookup"><span data-stu-id="39e58-121">From the list of maps, select the Ledger **(msdyn\_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> <span data-ttu-id="39e58-122">I fältet **Master för initial synkning** väljer du **Finance and Operations-appar** för både huvudboksmappning och obligatoriska mappningar.</span><span class="sxs-lookup"><span data-stu-id="39e58-122">In the **Master for initial sync** field, select **Finance and Operations apps** for both ledger map and all prerequisite maps.</span></span> <span data-ttu-id="39e58-123">Markera **Kör**.</span><span class="sxs-lookup"><span data-stu-id="39e58-123">Select **Run**.</span></span>

![Synkronisering av huvudboksmappning](media/DW6.png)

1. <span data-ttu-id="39e58-125">Följ samma steg för alla återstående tabellmappningar som visas i tabellen ovan.</span><span class="sxs-lookup"><span data-stu-id="39e58-125">Follow the same steps for all remaining table maps listed in the above table.</span></span> <span data-ttu-id="39e58-126">Markera inte kryssrutan **Initial synkning** när dessa mappningar körs.</span><span class="sxs-lookup"><span data-stu-id="39e58-126">Do not select the **Initial sync** check box when running those maps.</span></span>

## <a name="project-operations-dual-write-maps"></a><span data-ttu-id="39e58-127">Project Operations mappningar med dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="39e58-127">Project Operations dual-write maps</span></span>

<span data-ttu-id="39e58-128">Följande mappningar krävs för en Project Operations-lösning.</span><span class="sxs-lookup"><span data-stu-id="39e58-128">The following maps are required for a Project Operations solution.</span></span>

| <span data-ttu-id="39e58-129">**Entitetsmappning**</span><span class="sxs-lookup"><span data-stu-id="39e58-129">**Entity map**</span></span> | <span data-ttu-id="39e58-130">**Senaste versionen**</span><span class="sxs-lookup"><span data-stu-id="39e58-130">**Latest version**</span></span> | <span data-ttu-id="39e58-131">**Initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="39e58-131">**Initial sync**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="39e58-132">Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections)</span><span class="sxs-lookup"><span data-stu-id="39e58-132">Integration entity for project transaction relationships (msdyn\_transactionconnections)</span></span> | <span data-ttu-id="39e58-133">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="39e58-133">1.0.0.0</span></span> | <span data-ttu-id="39e58-134">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-134">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-135">Projektkontraktrubriker (sales orders)</span><span class="sxs-lookup"><span data-stu-id="39e58-135">Project contract headers (sales orders)</span></span> | <span data-ttu-id="39e58-136">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="39e58-136">1.0.0.1</span></span> | <span data-ttu-id="39e58-137">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-137">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-138">Projektkontraktrader (salesorderdetails)</span><span class="sxs-lookup"><span data-stu-id="39e58-138">Project contract lines (salesorderdetails)</span></span> | <span data-ttu-id="39e58-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="39e58-139">1.0.0.0</span></span> | <span data-ttu-id="39e58-140">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-140">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-141">Källa för projektfinansiering (msdyn_projectcontractsplitbillingrules)</span><span class="sxs-lookup"><span data-stu-id="39e58-141">Project funding source (msdyn_projectcontractsplitbillingrules)</span></span> | <span data-ttu-id="39e58-142">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="39e58-142">1.0.0.1</span></span> | <span data-ttu-id="39e58-143">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-143">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-144">Project Operations integrationstabell för materialberäkningar (msdyn\_estimatelines)</span><span class="sxs-lookup"><span data-stu-id="39e58-144">Project Operations integration table for material estimates (msdyn\_estimatelines)</span></span> | <span data-ttu-id="39e58-145">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="39e58-145">1.0.0.0</span></span> | <span data-ttu-id="39e58-146">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-146">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-147">Projektfakturaförslag V2 (invoices)</span><span class="sxs-lookup"><span data-stu-id="39e58-147">Project invoice proposals V2 (invoices)</span></span> | <span data-ttu-id="39e58-148">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="39e58-148">1.0.0.2</span></span> | <span data-ttu-id="39e58-149">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-149">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-150">Faktiska värden för Project Operations-integration (msdyn_actuals)</span><span class="sxs-lookup"><span data-stu-id="39e58-150">Project Operations integration actuals (msdyn_actuals)</span></span> | <span data-ttu-id="39e58-151">1.0.0.14</span><span class="sxs-lookup"><span data-stu-id="39e58-151">1.0.0.14</span></span> | <span data-ttu-id="39e58-152">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-152">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-153">Milstolpar för kontraktrad för Project Operations-integration (msdyn_contractlinesscheduleofvalues)</span><span class="sxs-lookup"><span data-stu-id="39e58-153">Project Operations integration contract line milestones (msdyn_contractlinesscheduleofvalues)</span></span> | <span data-ttu-id="39e58-154">1.0.0.4</span><span class="sxs-lookup"><span data-stu-id="39e58-154">1.0.0.4</span></span> | <span data-ttu-id="39e58-155">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-155">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-156">Entitet för Project Operations-integration för utgiftsuppskattningar (msdyn_estimateslines)</span><span class="sxs-lookup"><span data-stu-id="39e58-156">Project Operations integration entity for expense estimates (msdyn_estimateslines)</span></span> | <span data-ttu-id="39e58-157">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="39e58-157">1.0.0.2</span></span> | <span data-ttu-id="39e58-158">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-158">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-159">Entitet för Project Operations-integration för tidsuppskattningar (msdyn_resourceassignments)</span><span class="sxs-lookup"><span data-stu-id="39e58-159">Project Operations integration entity for hour estimates (msdyn_resourceassignments)</span></span> | <span data-ttu-id="39e58-160">1.0.0.5</span><span class="sxs-lookup"><span data-stu-id="39e58-160">1.0.0.5</span></span> | <span data-ttu-id="39e58-161">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-161">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-162">Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_expensecategories)</span><span class="sxs-lookup"><span data-stu-id="39e58-162">Project Operations integration project expense categories export entity (msdyn_expensecategories)</span></span> | <span data-ttu-id="39e58-163">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="39e58-163">1.0.0.2</span></span> | <span data-ttu-id="39e58-164">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-164">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-165">Entitet för export av projektutgifter i Project Operations-integration (msdyn_expenses)</span><span class="sxs-lookup"><span data-stu-id="39e58-165">Project Operations integration project expenses export entity (msdyn_expenses)</span></span> | <span data-ttu-id="39e58-166">1.0.0.2</span><span class="sxs-lookup"><span data-stu-id="39e58-166">1.0.0.2</span></span> | <span data-ttu-id="39e58-167">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-167">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-168">Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices)</span><span class="sxs-lookup"><span data-stu-id="39e58-168">Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)</span></span> | <span data-ttu-id="39e58-169">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="39e58-169">1.0.0.0</span></span> | <span data-ttu-id="39e58-170">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-170">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-171">Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn_projectvendorinvoicelines)</span><span class="sxs-lookup"><span data-stu-id="39e58-171">Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)</span></span> | <span data-ttu-id="39e58-172">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="39e58-172">1.0.0.0</span></span> | <span data-ttu-id="39e58-173">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-173">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-174">Projektresursroller för alla företag (bookableresourcecategories)</span><span class="sxs-lookup"><span data-stu-id="39e58-174">Project resource roles for all companies (bookableresourcecategories)</span></span> | <span data-ttu-id="39e58-175">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="39e58-175">1.0.0.1</span></span> | <span data-ttu-id="39e58-176">Kräver en initial synkronisering av tabellmappningen för att synkronisera resursrollerna Projektledare och Teammedlem som fylls i i Dynamics 365 Dataverse-miljön under etableringen.</span><span class="sxs-lookup"><span data-stu-id="39e58-176">Requires an initial sync for the table map to synchronize the Project Manager and Team member resource roles that are populated in the Dynamics 365 Dataverse environment during provisioning.</span></span> <span data-ttu-id="39e58-177">Dataverse är huvudkällan för den första synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="39e58-177">Dataverse is the main source for the initial synchronization.</span></span> |
| <span data-ttu-id="39e58-178">Projektuppgifter (msdyn_projecttasks)</span><span class="sxs-lookup"><span data-stu-id="39e58-178">Project tasks (msdyn_projecttasks)</span></span> | <span data-ttu-id="39e58-179">1.0.0.4</span><span class="sxs-lookup"><span data-stu-id="39e58-179">1.0.0.4</span></span> | <span data-ttu-id="39e58-180">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-180">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-181">Projekttransaktionskategorier (msdyn_transactioncategories)</span><span class="sxs-lookup"><span data-stu-id="39e58-181">Project transaction categories (msdyn_transactioncategories)</span></span> | <span data-ttu-id="39e58-182">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="39e58-182">1.0.0.0</span></span> | <span data-ttu-id="39e58-183">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-183">Not required for provisioning.</span></span> |
| <span data-ttu-id="39e58-184">Projekt V2 (msdyn_projects)</span><span class="sxs-lookup"><span data-stu-id="39e58-184">Projects V2 (msdyn_projects)</span></span> | <span data-ttu-id="39e58-185">1.0.0.1</span><span class="sxs-lookup"><span data-stu-id="39e58-185">1.0.0.1</span></span> | <span data-ttu-id="39e58-186">Krävs inte för etablering.</span><span class="sxs-lookup"><span data-stu-id="39e58-186">Not required for provisioning.</span></span> |

<span data-ttu-id="39e58-187">Kör de listade mappningar genom att följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="39e58-187">Complete the following steps to run the listed maps.</span></span>

1. <span data-ttu-id="39e58-188">Aktivera projektresursrollerna för tabellmappningen **Alla företag (bookableresourcecategories)** eftersom denna mappning kräver första synkronisering. I fältet **Master för första synkning** väljer du **Gemensam datatjänst**.</span><span class="sxs-lookup"><span data-stu-id="39e58-188">Enable the Project resource roles for **all companies (bookableresourcecategories)** table map as this map requires the initial sync. In the **Master for initial sync** field, select **Common data service**.</span></span> 

 ![Mappningssynkning av resursrolltabell](media/6ResourceInitialSync.jpg)

 <span data-ttu-id="39e58-190">Vänta tills mappningen status är **Körs** innan du tar nästa steg.</span><span class="sxs-lookup"><span data-stu-id="39e58-190">Wait until the status of the map is **Running** before you move to the next step.</span></span>

2. <span data-ttu-id="39e58-191">Markera alla återstående obligatoriska mappningar.</span><span class="sxs-lookup"><span data-stu-id="39e58-191">Select all of the remaining required maps.</span></span> <span data-ttu-id="39e58-192">Du kan filtrera dem i listan med mappningar med dubbelriktad skrivning med nyckelordet **Projekt** i sökfunktionen längst upp till höger.</span><span class="sxs-lookup"><span data-stu-id="39e58-192">You can filter them in the dual-write map list using the keyword, **Project** in search in the upper-right corner.</span></span> <span data-ttu-id="39e58-193">Du kan göra flerval av alla mappningar och sedan köra dem.</span><span class="sxs-lookup"><span data-stu-id="39e58-193">You can multi-select all maps and then run.</span></span> <span data-ttu-id="39e58-194">Mer information finns i [Hantera flera tabellmappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps).</span><span class="sxs-lookup"><span data-stu-id="39e58-194">For more information, see [Manage multiple table maps](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps).</span></span> <span data-ttu-id="39e58-195">Se till att du även aktiverar och kör relaterade entitetsmappningar.</span><span class="sxs-lookup"><span data-stu-id="39e58-195">Make sure to also enable and run related entity maps.</span></span>

### <a name="project-operations-dual-write-map-versions"></a><span data-ttu-id="39e58-196">Project Operations mappningsversioner för dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="39e58-196">Project Operations dual-write map versions</span></span>

<span data-ttu-id="39e58-197">Kör alltid den senaste versionen av mappningen i miljön.</span><span class="sxs-lookup"><span data-stu-id="39e58-197">Always run the latest version of the map in your environment.</span></span> <span data-ttu-id="39e58-198">Vissa funktioner kanske inte fungerar korrekt om något av följande villkor finns:</span><span class="sxs-lookup"><span data-stu-id="39e58-198">Certain features and capabilities might not work correctly if any of the following conditions exist:</span></span>

- <span data-ttu-id="39e58-199">En mappning har inte aktiverats.</span><span class="sxs-lookup"><span data-stu-id="39e58-199">A map isn't activated.</span></span>
- <span data-ttu-id="39e58-200">Den senaste versionen av mappningen har inte aktiverats.</span><span class="sxs-lookup"><span data-stu-id="39e58-200">The latest version of the map isn't activated.</span></span> 
- <span data-ttu-id="39e58-201">Relaterade tabellmappningar har inte aktiverats.</span><span class="sxs-lookup"><span data-stu-id="39e58-201">Related table maps aren't activated.</span></span>

<span data-ttu-id="39e58-202">Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**.</span><span class="sxs-lookup"><span data-stu-id="39e58-202">You can view the active version of the map in the **Version** column on the **Dual-write** page.</span></span> <span data-ttu-id="39e58-203">Du kan aktivera en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen.</span><span class="sxs-lookup"><span data-stu-id="39e58-203">You can activate a new version of the map by selecting **Table map versions**, selecting the latest version, and then saving the selected version.</span></span> <span data-ttu-id="39e58-204">Om du har anpassat en "out-of-the-box"-tabellmappning måste du tillämpa ändringarna på nytt.</span><span class="sxs-lookup"><span data-stu-id="39e58-204">If you have customized an out-of-the-box table map, you will need reapply the changes.</span></span> <span data-ttu-id="39e58-205">Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).</span><span class="sxs-lookup"><span data-stu-id="39e58-205">For more information, see [Application lifecycle management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).</span></span>