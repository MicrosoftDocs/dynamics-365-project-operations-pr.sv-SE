---
title: Fastställa din distributionstyp
description: I det här ämnet finns information som gör det lättare för dig att fastställa korrekt distributionstyp av Project Operations för ditt företag.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401240"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="bb44e-103">Fastställa din distributionstyp</span><span class="sxs-lookup"><span data-stu-id="bb44e-103">Determine your deployment type</span></span>

<span data-ttu-id="bb44e-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="bb44e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb44e-105">När du har köpt licensen startar du här för att fastställa den bästa distributionsmodellen för Dynamics 365 Project Operations med hjälp av [Guidat installationsflöde](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bb44e-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="bb44e-106">När du har slutfört flödet i den guidade installationen dirigeras du till rätt hanteringsportal för att slutföra installationen.</span><span class="sxs-lookup"><span data-stu-id="bb44e-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="bb44e-107">Se distributionsinformationen för att slutföra installationen.</span><span class="sxs-lookup"><span data-stu-id="bb44e-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="bb44e-108">Befintliga kunder av Dynamics som använder Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bb44e-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="bb44e-109">Project Operations inkluderar de funktioner som levererades med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bb44e-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="bb44e-110">En uppgraderingssökväg kommer att ges ut för dessa kunder i 2021 utgivningscykel 1.</span><span class="sxs-lookup"><span data-stu-id="bb44e-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="bb44e-111">Befintliga kunder av Dynamics 365 Finance som använder projekthantering och redovisning</span><span class="sxs-lookup"><span data-stu-id="bb44e-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="bb44e-112">Befintliga kunder av finans Finance som använder funktionerna för projektledning och redovisning kan fortsätta att använda dem som de är.</span><span class="sxs-lookup"><span data-stu-id="bb44e-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="bb44e-113">Se [Project Operations för lagerbaserade/produktionsorderbaserade scenarier](#pma).</span><span class="sxs-lookup"><span data-stu-id="bb44e-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="bb44e-114">Distributionstyper</span><span class="sxs-lookup"><span data-stu-id="bb44e-114">Deployment types</span></span>
<span data-ttu-id="bb44e-115">Project Operations har stöd för flera distributionsalternativ för att uppfylla dina krav.</span><span class="sxs-lookup"><span data-stu-id="bb44e-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="bb44e-116">Oavsett om du är en ny eller befintlig Dynamics 365-kund kan Project Operations tillgodose dina behov.</span><span class="sxs-lookup"><span data-stu-id="bb44e-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="bb44e-117">Vår [distributionsenkät](https://aka.ms/provisionprojectoperations) hjälper dig att fastställa rätt distribution.</span><span class="sxs-lookup"><span data-stu-id="bb44e-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="bb44e-118">Resultatet vägleder dig mot någon av följande distributionstyper:</span><span class="sxs-lookup"><span data-stu-id="bb44e-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="bb44e-119">Mindre distribution – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="bb44e-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="bb44e-120">Project Operations för resursscenarier/icke lagerbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="bb44e-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="bb44e-121">Project Operations för lagerbaserade/produktionsorderbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="bb44e-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="bb44e-122">Project Operations har stöd för lagerbaserade/produktionsorderbaserade scenarier och icke lagerbaserade/resursbaserade scenarier i samma miljö via konfigurationer på en juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="bb44e-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="bb44e-123">Contoso kan t. ex. använda funktionerna för lager-/produktionsorder i en amerikansk tillverkningsanläggning (juridisk person = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="bb44e-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="bb44e-124">Contoso kan använda icke-lagerförda och resursbaserade funktioner i Contoso Robotics Arms serviceanläggning i Storbritannien (juridisk person = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="bb44e-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="bb44e-125">Enkel distribution – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="bb44e-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="bb44e-126">Den enkla distributionen omfattar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="bb44e-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="bb44e-127">Försäljningsprocess för projekt som utökar Dynamics 365 Sales-appupplevelser</span><span class="sxs-lookup"><span data-stu-id="bb44e-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="bb44e-128">Planera projekt med hjälp av Microsoft Project för webben</span><span class="sxs-lookup"><span data-stu-id="bb44e-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="bb44e-129">Flerdimensionell prissättning</span><span class="sxs-lookup"><span data-stu-id="bb44e-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="bb44e-130">Enhetlig resurshantering</span><span class="sxs-lookup"><span data-stu-id="bb44e-130">Unified resource management</span></span>
- <span data-ttu-id="bb44e-131">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="bb44e-131">Time tracking</span></span>
- <span data-ttu-id="bb44e-132">Grundläggande utgift</span><span class="sxs-lookup"><span data-stu-id="bb44e-132">Basic expense</span></span>
- <span data-ttu-id="bb44e-133">Proforma och kundorienterade fakturering</span><span class="sxs-lookup"><span data-stu-id="bb44e-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="bb44e-134">Instruktioner för distribution</span><span class="sxs-lookup"><span data-stu-id="bb44e-134">Deployment steps</span></span>
<span data-ttu-id="bb44e-135">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bb44e-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="bb44e-136">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](lite-preview-subscription-sign-up.md) och [Etablera en ny miljö](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="bb44e-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="bb44e-137">Project Operations för resursscenarier/icke lagerbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="bb44e-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="bb44e-138">Project Operations för resursbaserade/icke lagerbaserade scenarier omfattar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="bb44e-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="bb44e-139">Försäljningsprocess för projekt som utökar Dynamics 365 Sales-app</span><span class="sxs-lookup"><span data-stu-id="bb44e-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="bb44e-140">Planera projekt med hjälp av Microsoft Project för webben</span><span class="sxs-lookup"><span data-stu-id="bb44e-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="bb44e-141">Flerdimensionell prissättning</span><span class="sxs-lookup"><span data-stu-id="bb44e-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="bb44e-142">Enhetlig resurshantering</span><span class="sxs-lookup"><span data-stu-id="bb44e-142">Unified resource management</span></span>
- <span data-ttu-id="bb44e-143">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="bb44e-143">Time tracking</span></span>
- <span data-ttu-id="bb44e-144">Grundläggande utgift</span><span class="sxs-lookup"><span data-stu-id="bb44e-144">Basic expense</span></span>
- <span data-ttu-id="bb44e-145">Fullständig utgift</span><span class="sxs-lookup"><span data-stu-id="bb44e-145">Full expense</span></span>
- <span data-ttu-id="bb44e-146">OCR på kvitto</span><span class="sxs-lookup"><span data-stu-id="bb44e-146">Receipt OCR</span></span>
- <span data-ttu-id="bb44e-147">Proforma och kundorienterade fakturering</span><span class="sxs-lookup"><span data-stu-id="bb44e-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="bb44e-148">Intäktsredovisning för projekt</span><span class="sxs-lookup"><span data-stu-id="bb44e-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="bb44e-149">Instruktioner för distribution</span><span class="sxs-lookup"><span data-stu-id="bb44e-149">Deployment steps</span></span>
<span data-ttu-id="bb44e-150">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bb44e-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="bb44e-151">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](resource-sign-up-preview-subscription.md) och [Etablera en ny miljö](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="bb44e-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="bb44e-152">Project Operations för lagerbaserade/produktionsorderbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="bb44e-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="bb44e-153">Projektplanering med hjälp av WBS</span><span class="sxs-lookup"><span data-stu-id="bb44e-153">Project planning using WBS</span></span>
- <span data-ttu-id="bb44e-154">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="bb44e-154">Resource Management</span></span>
- <span data-ttu-id="bb44e-155">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="bb44e-155">Time Tracking</span></span>
- <span data-ttu-id="bb44e-156">Fullständig utgift</span><span class="sxs-lookup"><span data-stu-id="bb44e-156">Full Expense</span></span>
- <span data-ttu-id="bb44e-157">OCR på kvitto</span><span class="sxs-lookup"><span data-stu-id="bb44e-157">Receipt OCR</span></span>
- <span data-ttu-id="bb44e-158">Fullständig fakturering</span><span class="sxs-lookup"><span data-stu-id="bb44e-158">Full Invoicing</span></span>
- <span data-ttu-id="bb44e-159">Intäktsredovisning</span><span class="sxs-lookup"><span data-stu-id="bb44e-159">Revenue Recognition</span></span>
- <span data-ttu-id="bb44e-160">Produktionsorder</span><span class="sxs-lookup"><span data-stu-id="bb44e-160">Production Orders</span></span>
- <span data-ttu-id="bb44e-161">Stöd för material</span><span class="sxs-lookup"><span data-stu-id="bb44e-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="bb44e-162">Instruktioner för distribution</span><span class="sxs-lookup"><span data-stu-id="bb44e-162">Deployment steps</span></span>
<span data-ttu-id="bb44e-163">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bb44e-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="bb44e-164">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) och [Etablera en ny miljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="bb44e-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

