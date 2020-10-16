---
title: Distributionstyper
description: I det här ämnet finns information som gör det lättare för dig att fastställa korrekt distributionstyp av Project Operations för ditt företag.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949098"
---
# <a name="deployment-types"></a><span data-ttu-id="6f6d8-103">Distributionstyper</span><span class="sxs-lookup"><span data-stu-id="6f6d8-103">Deployment types</span></span>

<span data-ttu-id="6f6d8-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="6f6d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f6d8-105">När du har köpt licensen startar du här för att fastställa den bästa distributionsmodellen för Dynamics 365 Project Operations med hjälp av [Guidat installationsflöde](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6f6d8-106">När du har slutfört flödet i den guidade installationen dirigeras du till rätt hanteringsportal för att slutföra installationen.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6f6d8-107">Se distributionsinformationen nedan för att slutföra installationen.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6f6d8-108">Befintliga kunder av Dynamics som använder Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6f6d8-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6f6d8-109">Project Operations inkluderar de funktioner som levererades med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6f6d8-110">En uppgraderingssökväg publiceras för de här kunderna i framtiden.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6f6d8-111">Befintliga kunder av Dynamics 365 Finance som använder projekthantering och redovisning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6f6d8-112">Befintliga kunder av Finance som använder projektlednings- och redovisningsfunktionerna kan fortsätta använda dessa funktioner.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="6f6d8-113">Se [Project Operations för lagerbaserade/produktionsorderbaserade scenarier](#pma).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="6f6d8-114">Project Operations har stöd för flera distributionsalternativ för att uppfylla dina krav.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6f6d8-115">Oavsett om du är en ny eller befintlig Dynamics 365-kund kan Project Operations tillgodose dina behov.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6f6d8-116">Vår [distributionsenkät](https://aka.ms/provisionprojectoperations) hjälper dig att fastställa rätt distribution.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6f6d8-117">Resultatet vägleder dig mot någon av följande distributionstyper:</span><span class="sxs-lookup"><span data-stu-id="6f6d8-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6f6d8-118">Mindre distribution – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6f6d8-119">Project Operations för resursscenarier/icke lagerbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="6f6d8-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6f6d8-120">Project Operations för lagerbaserade/produktionsorderbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="6f6d8-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6f6d8-121">Project Operations har stöd för lagerbaserade/produktionsorderbaserade scenarier och icke lagerbaserade/resursbaserade scenarier i samma miljö via konfigurationer på en juridisk enhetsnivå.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6f6d8-122">Till exempel kan Contoso utnyttja lagerbaserade/produktionsorderbaserade funktioner i den amerikanska produktionsanläggningen (juridisk entitet = Contoso Manufacturing United States) och icke lagerbaserade/resursbaserade funktioner i Contosos anläggning för service av robotarmar i Storbritannien (juridisk entitet = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="6f6d8-123"><a name="lite"><a/>Enkel distribution – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="6f6d8-124">Den enkla distributionen omfattar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="6f6d8-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6f6d8-125">Planera projekt med hjälp av Microsoft Project för webben</span><span class="sxs-lookup"><span data-stu-id="6f6d8-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6f6d8-126">Flerdimensionell prissättning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6f6d8-127">Enhetlig resurshantering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-127">Unified Resource Management</span></span>
- <span data-ttu-id="6f6d8-128">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-128">Time Tracking</span></span>
- <span data-ttu-id="6f6d8-129">Grundläggande utgifter</span><span class="sxs-lookup"><span data-stu-id="6f6d8-129">Basic Expense</span></span>
- <span data-ttu-id="6f6d8-130">Fakturaförslag</span><span class="sxs-lookup"><span data-stu-id="6f6d8-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6f6d8-131">Instruktioner för distribution:</span><span class="sxs-lookup"><span data-stu-id="6f6d8-131">Deployment steps:</span></span>
<span data-ttu-id="6f6d8-132">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6f6d8-133">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](lite-preview-subscription-sign-up.md) och [Etablera en ny miljö](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="6f6d8-134"><a name="integrated"><a/>Project Operations för resursscenarier/icke lagerbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="6f6d8-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6f6d8-135">Project Operations för resursbaserade/icke lagerbaserade scenarier omfattar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="6f6d8-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6f6d8-136">Planera projekt med hjälp av Microsoft Project för webben</span><span class="sxs-lookup"><span data-stu-id="6f6d8-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6f6d8-137">Flerdimensionell prissättning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6f6d8-138">Enhetlig resurshantering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-138">Unified Resource Management</span></span>
- <span data-ttu-id="6f6d8-139">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-139">Time Tracking</span></span>
- <span data-ttu-id="6f6d8-140">Grundläggande utgifter</span><span class="sxs-lookup"><span data-stu-id="6f6d8-140">Basic Expense</span></span>
- <span data-ttu-id="6f6d8-141">Fullständig utgift</span><span class="sxs-lookup"><span data-stu-id="6f6d8-141">Full Expense</span></span>
- <span data-ttu-id="6f6d8-142">OCR på kvitto</span><span class="sxs-lookup"><span data-stu-id="6f6d8-142">Receipt OCR</span></span>
- <span data-ttu-id="6f6d8-143">Fullständig fakturering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-143">Full Invoicing</span></span>
- <span data-ttu-id="6f6d8-144">Intäktsredovisning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6f6d8-145">Instruktioner för distribution:</span><span class="sxs-lookup"><span data-stu-id="6f6d8-145">Deployment steps:</span></span>
<span data-ttu-id="6f6d8-146">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6f6d8-147">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](resource-sign-up-preview-subscription.md) och [Etablera en ny miljö](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6f6d8-148">Project Operations för lagerbaserade/produktionsorderbaserade scenarier</span><span class="sxs-lookup"><span data-stu-id="6f6d8-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6f6d8-149">Projektplanering med hjälp av WBS</span><span class="sxs-lookup"><span data-stu-id="6f6d8-149">Project planning using WBS</span></span>
- <span data-ttu-id="6f6d8-150">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-150">Resource Management</span></span>
- <span data-ttu-id="6f6d8-151">Tidsspårning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-151">Time Tracking</span></span>
- <span data-ttu-id="6f6d8-152">Fullständig utgift</span><span class="sxs-lookup"><span data-stu-id="6f6d8-152">Full Expense</span></span>
- <span data-ttu-id="6f6d8-153">OCR på kvitto</span><span class="sxs-lookup"><span data-stu-id="6f6d8-153">Receipt OCR</span></span>
- <span data-ttu-id="6f6d8-154">Fullständig fakturering</span><span class="sxs-lookup"><span data-stu-id="6f6d8-154">Full Invoicing</span></span>
- <span data-ttu-id="6f6d8-155">Intäktsredovisning</span><span class="sxs-lookup"><span data-stu-id="6f6d8-155">Revenue Recognition</span></span>
- <span data-ttu-id="6f6d8-156">Produktionsorder</span><span class="sxs-lookup"><span data-stu-id="6f6d8-156">Production Orders</span></span>
- <span data-ttu-id="6f6d8-157">Stöd för material</span><span class="sxs-lookup"><span data-stu-id="6f6d8-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6f6d8-158">Instruktioner för distribution:</span><span class="sxs-lookup"><span data-stu-id="6f6d8-158">Deployment steps:</span></span>
<span data-ttu-id="6f6d8-159">Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6f6d8-160">Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) och [Etablera en ny miljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



