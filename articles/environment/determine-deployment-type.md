---
title: Fastställa din distributionstyp
description: I det här ämnet finns information som gör det lättare för dig att fastställa korrekt distributionstyp av Project Operations för ditt företag.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085544"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="58b08-103">Fastställa din distributionstyp</span><span class="sxs-lookup"><span data-stu-id="58b08-103">Determine your deployment type</span></span>

<span data-ttu-id="58b08-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="58b08-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58b08-105">När du har köpt licensen startar du här för att fastställa den bästa distributionsmodellen för Dynamics 365 Project Operations med hjälp av [Guidat installationsflöde](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="58b08-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="58b08-106">När du har slutfört flödet i den guidade installationen dirigeras du till rätt hanteringsportal för att slutföra installationen.</span><span class="sxs-lookup"><span data-stu-id="58b08-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="58b08-107">Se distributionsinformationen för att slutföra installationen.</span><span class="sxs-lookup"><span data-stu-id="58b08-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="58b08-108">Befintliga kunder av Dynamics som använder Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="58b08-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="58b08-109">Project Operations inkluderar de funktioner som levererades med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="58b08-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="58b08-110">En uppgraderingssökväg publiceras för de här kunderna i framtiden.</span><span class="sxs-lookup"><span data-stu-id="58b08-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="58b08-111">Befintliga kunder av Dynamics 365 Finance som använder projekthantering och redovisning</span><span class="sxs-lookup"><span data-stu-id="58b08-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="58b08-112">Befintliga kunder av Finance som använder projektlednings- och redovisningsfunktionerna kan fortsätta använda dessa funktioner.</span><span class="sxs-lookup"><span data-stu-id="58b08-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="58b08-113">Se [Project Operations för lagerbaserade/produktionsorderbaserade scenarier](#pma).</span><span class="sxs-lookup"><span data-stu-id="58b08-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="58b08-114">Distributionstyper</span><span class="sxs-lookup"><span data-stu-id="58b08-114">Deployment types</span></span>
<span data-ttu-id="58b08-115">Project Operations har stöd för flera distributionsalternativ för att uppfylla dina krav.</span><span class="sxs-lookup"><span data-stu-id="58b08-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="58b08-116">Oavsett om du är en ny eller befintlig Dynamics 365-kund kan Project Operations tillgodose dina behov.</span><span class="sxs-lookup"><span data-stu-id="58b08-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="58b08-117">Vår [distributionsenkät](https://aka.ms/provisionprojectoperations) hjälper dig att fastställa rätt distribution.</span><span class="sxs-lookup"><span data-stu-id="58b08-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="58b08-118">Resultatet vägleder dig mot någon av följande distributionstyper:</span><span class="sxs-lookup"><span data-stu-id="58b08-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="58b08-119">Mindre distribution – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="58b08-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="58b08-120">Project Operations för resursscenarier/icke lagerbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="58b08-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="58b08-121">Project Operations för lagerbaserade/produktionsorderbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="58b08-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="58b08-122">Project Operations har stöd för lagerbaserade/produktionsorderbaserade scenarier och icke lagerbaserade/resursbaserade scenarier i samma miljö via konfigurationer på en juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="58b08-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="58b08-123">Contoso kan t. ex. använda funktionerna för lager-/produktionsorder i en amerikansk tillverkningsanläggning (juridisk person = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="58b08-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="58b08-124">Contoso kan använda icke-lagerförda och resursbaserade funktioner i Contoso Robotics Arms serviceanläggning i Storbritannien (juridisk person = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="58b08-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="58b08-125">Enkel distribution – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="58b08-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="58b08-126">Den enkla distributionen omfattar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="58b08-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="58b08-127">Planera projekt med hjälp av Microsoft Project för webben</span><span class="sxs-lookup"><span data-stu-id="58b08-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="58b08-128">Flerdimensionell prissättning</span><span class="sxs-lookup"><span data-stu-id="58b08-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="58b08-129">Enhetlig resurshantering</span><span class="sxs-lookup"><span data-stu-id="58b08-129">Unified Resource Management</span></span>
- <span data-ttu-id="58b08-130">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="58b08-130">Time Tracking</span></span>
- <span data-ttu-id="58b08-131">Grundläggande utgifter</span><span class="sxs-lookup"><span data-stu-id="58b08-131">Basic Expense</span></span>
- <span data-ttu-id="58b08-132">Fakturaförslag</span><span class="sxs-lookup"><span data-stu-id="58b08-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="58b08-133">Instruktioner för distribution</span><span class="sxs-lookup"><span data-stu-id="58b08-133">Deployment steps</span></span>
<span data-ttu-id="58b08-134">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="58b08-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="58b08-135">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](lite-preview-subscription-sign-up.md) och [Etablera en ny miljö](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="58b08-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="58b08-136">Project Operations för resursscenarier/icke lagerbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="58b08-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="58b08-137">Project Operations för resursbaserade/icke lagerbaserade scenarier omfattar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="58b08-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="58b08-138">Planera projekt med hjälp av Microsoft Project för webben</span><span class="sxs-lookup"><span data-stu-id="58b08-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="58b08-139">Flerdimensionell prissättning</span><span class="sxs-lookup"><span data-stu-id="58b08-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="58b08-140">Enhetlig resurshantering</span><span class="sxs-lookup"><span data-stu-id="58b08-140">Unified Resource Management</span></span>
- <span data-ttu-id="58b08-141">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="58b08-141">Time Tracking</span></span>
- <span data-ttu-id="58b08-142">Grundläggande utgifter</span><span class="sxs-lookup"><span data-stu-id="58b08-142">Basic Expense</span></span>
- <span data-ttu-id="58b08-143">Fullständig utgift</span><span class="sxs-lookup"><span data-stu-id="58b08-143">Full Expense</span></span>
- <span data-ttu-id="58b08-144">OCR på kvitto</span><span class="sxs-lookup"><span data-stu-id="58b08-144">Receipt OCR</span></span>
- <span data-ttu-id="58b08-145">Fullständig fakturering</span><span class="sxs-lookup"><span data-stu-id="58b08-145">Full Invoicing</span></span>
- <span data-ttu-id="58b08-146">Intäktsredovisning</span><span class="sxs-lookup"><span data-stu-id="58b08-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="58b08-147">Instruktioner för distribution</span><span class="sxs-lookup"><span data-stu-id="58b08-147">Deployment steps</span></span>
<span data-ttu-id="58b08-148">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="58b08-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="58b08-149">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](resource-sign-up-preview-subscription.md) och [Etablera en ny miljö](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="58b08-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="58b08-150">Project Operations för lagerbaserade/produktionsorderbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="58b08-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="58b08-151">Projektplanering med hjälp av WBS</span><span class="sxs-lookup"><span data-stu-id="58b08-151">Project planning using WBS</span></span>
- <span data-ttu-id="58b08-152">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="58b08-152">Resource Management</span></span>
- <span data-ttu-id="58b08-153">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="58b08-153">Time Tracking</span></span>
- <span data-ttu-id="58b08-154">Fullständig utgift</span><span class="sxs-lookup"><span data-stu-id="58b08-154">Full Expense</span></span>
- <span data-ttu-id="58b08-155">OCR på kvitto</span><span class="sxs-lookup"><span data-stu-id="58b08-155">Receipt OCR</span></span>
- <span data-ttu-id="58b08-156">Fullständig fakturering</span><span class="sxs-lookup"><span data-stu-id="58b08-156">Full Invoicing</span></span>
- <span data-ttu-id="58b08-157">Intäktsredovisning</span><span class="sxs-lookup"><span data-stu-id="58b08-157">Revenue Recognition</span></span>
- <span data-ttu-id="58b08-158">Produktionsorder</span><span class="sxs-lookup"><span data-stu-id="58b08-158">Production Orders</span></span>
- <span data-ttu-id="58b08-159">Stöd för material</span><span class="sxs-lookup"><span data-stu-id="58b08-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="58b08-160">Instruktioner för distribution</span><span class="sxs-lookup"><span data-stu-id="58b08-160">Deployment steps</span></span>
<span data-ttu-id="58b08-161">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="58b08-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="58b08-162">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) och [Etablera en ny miljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="58b08-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

