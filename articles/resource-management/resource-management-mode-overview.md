---
title: Översikt över resurshanteringslägen
description: I det här ämnet finns information om funktionen för projekthantering i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279475"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="e6ac2-103">Resurshanteringslägen – Översikt</span><span class="sxs-lookup"><span data-stu-id="e6ac2-103">Resource management modes overview</span></span>

<span data-ttu-id="e6ac2-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="e6ac2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e6ac2-105">Dynamics 365 Project Operations har stöd för två lägen för att du ska kunna utföra det övergripande bokningsflödet.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="e6ac2-106">Hanteringsläget definieras som en projektparameter och kan ändras om företagets behov ändras.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="e6ac2-107">Centralt läge</span><span class="sxs-lookup"><span data-stu-id="e6ac2-107">Central mode</span></span>
<span data-ttu-id="e6ac2-108">För organisationer som centraliserar tilldelningen för resurser till projekt, kan du med hjälp av centralläget se till att projektledarna kan definiera resurskrav på projektnivå.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="e6ac2-109">Uppfyllelse av resurskraven delegeras till en resursansvarig.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="e6ac2-110">Projektledarna kan acceptera eller avvisa resurser som föreslås av den resursansvariga.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centralt läge](./media/resource-management-central.png)

<span data-ttu-id="e6ac2-112">Information om hur du hanterar resurser med centralt läge finns i:</span><span class="sxs-lookup"><span data-stu-id="e6ac2-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="e6ac2-113">Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov</span><span class="sxs-lookup"><span data-stu-id="e6ac2-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e6ac2-114">Boka namngivna resurser från resurskrav</span><span class="sxs-lookup"><span data-stu-id="e6ac2-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="e6ac2-115">Skicka en resursbegäran</span><span class="sxs-lookup"><span data-stu-id="e6ac2-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="e6ac2-116">Uppfyll en resursförfrågning</span><span class="sxs-lookup"><span data-stu-id="e6ac2-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="e6ac2-117">Acceptera eller avvisa en föreslagen projektresurs från en resursförfrågan</span><span class="sxs-lookup"><span data-stu-id="e6ac2-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="e6ac2-118">Hybridläge</span><span class="sxs-lookup"><span data-stu-id="e6ac2-118">Hybrid mode</span></span>
<span data-ttu-id="e6ac2-119">För organisationer som behöver flexibilitet i tilldelningen av resurser innebär hybridläget att både projektledarna och resursansvariga kan boka resurser.</span><span class="sxs-lookup"><span data-stu-id="e6ac2-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridläge](./media/resource-management-hybrid.png)

<span data-ttu-id="e6ac2-121">Utöver den centrallägesprocess som stöds, se följande avsnitt för att hantera alla andra bokningsflöden som stöds i hybridläget:</span><span class="sxs-lookup"><span data-stu-id="e6ac2-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="e6ac2-122">Boka en resurs direkt till ett projekt:</span><span class="sxs-lookup"><span data-stu-id="e6ac2-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="e6ac2-123">Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter</span><span class="sxs-lookup"><span data-stu-id="e6ac2-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="e6ac2-124">Boka en resurs från ett resurskrav:</span><span class="sxs-lookup"><span data-stu-id="e6ac2-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="e6ac2-125">Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov</span><span class="sxs-lookup"><span data-stu-id="e6ac2-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e6ac2-126">Boka namngivna resurser från resurskrav</span><span class="sxs-lookup"><span data-stu-id="e6ac2-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]