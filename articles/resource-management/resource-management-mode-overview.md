---
title: Översikt över resurshanteringslägen
description: I det här ämnet finns information om resurshanteringsfunktioner i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085428"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="e5ad6-103">Översikt över resurshanteringslägen</span><span class="sxs-lookup"><span data-stu-id="e5ad6-103">Resource management modes overview</span></span>

<span data-ttu-id="e5ad6-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="e5ad6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e5ad6-105">Dynamics 365 Project Operations stöder två lägen för att du ska kunna utföra hela bokningsflödet.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="e5ad6-106">Hanteringsläget definieras som en projektparameter och kan ändras om företagets behov ändras.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="e5ad6-107">Centralt läge</span><span class="sxs-lookup"><span data-stu-id="e5ad6-107">Central mode</span></span>
<span data-ttu-id="e5ad6-108">För organisationer som centraliserar tilldelningen för resurser till projekt, kan du med hjälp av centralläget se till att projektledarna kan definiera resurskrav på projektnivå.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="e5ad6-109">Uppfyllelse av resurskraven delegeras till en resursansvarig.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="e5ad6-110">Projektledarna kan acceptera eller avvisa resurser som föreslås av den resursansvariga.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centralt läge](./media/resource-management-central.png)

<span data-ttu-id="e5ad6-112">Information om hur du hanterar resurser med centralt läge finns i:</span><span class="sxs-lookup"><span data-stu-id="e5ad6-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="e5ad6-113">Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov</span><span class="sxs-lookup"><span data-stu-id="e5ad6-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e5ad6-114">Boka namngivna resurser från resurskrav</span><span class="sxs-lookup"><span data-stu-id="e5ad6-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="e5ad6-115">Skicka en resursbegäran</span><span class="sxs-lookup"><span data-stu-id="e5ad6-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="e5ad6-116">Uppfyll en resursförfrågning</span><span class="sxs-lookup"><span data-stu-id="e5ad6-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="e5ad6-117">Acceptera eller avvisa en föreslagen projektresurs från en resursförfrågan</span><span class="sxs-lookup"><span data-stu-id="e5ad6-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="e5ad6-118">Hybridläge</span><span class="sxs-lookup"><span data-stu-id="e5ad6-118">Hybrid mode</span></span>
<span data-ttu-id="e5ad6-119">För organisationer som behöver flexibilitet i tilldelningen av resurser innebär hybridläget att både projektledarna och resursansvariga kan boka resurser.</span><span class="sxs-lookup"><span data-stu-id="e5ad6-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridläge](./media/resource-management-hybrid.png)

<span data-ttu-id="e5ad6-121">Utöver den centrallägesprocess som stöds, se följande avsnitt för att hantera alla andra bokningsflöden som stöds i hybridläget:</span><span class="sxs-lookup"><span data-stu-id="e5ad6-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="e5ad6-122">Boka en resurs direkt till ett projekt:</span><span class="sxs-lookup"><span data-stu-id="e5ad6-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="e5ad6-123">Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter</span><span class="sxs-lookup"><span data-stu-id="e5ad6-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="e5ad6-124">Boka en resurs från ett resurskrav:</span><span class="sxs-lookup"><span data-stu-id="e5ad6-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="e5ad6-125">Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov</span><span class="sxs-lookup"><span data-stu-id="e5ad6-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e5ad6-126">Boka namngivna resurser från resurskrav</span><span class="sxs-lookup"><span data-stu-id="e5ad6-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
