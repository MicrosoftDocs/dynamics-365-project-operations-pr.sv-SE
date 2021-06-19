---
title: Bokningar kontra tilldelningar
description: I det här ämnet finns information om skillnaderna mellan resursbokningar och resurstilldelningar.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012788"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="7d11a-103">Bokningar kontra tilldelningar</span><span class="sxs-lookup"><span data-stu-id="7d11a-103">Bookings vs assignments</span></span>

<span data-ttu-id="7d11a-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="7d11a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d11a-105">Bokningar är en fast eller preliminär allokering av resurser till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="7d11a-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7d11a-106">Fasta bokningar förbrukar en resurs kapacitet.</span><span class="sxs-lookup"><span data-stu-id="7d11a-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="7d11a-107">Bokningar representerar organisationskoncept för grupper så att de kan förstå hur resurser ska engageras mellan olika projekt.</span><span class="sxs-lookup"><span data-stu-id="7d11a-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="7d11a-108">Dynamics 365 Project Operations betraktar bokningar som ett koncept på projektnivå.</span><span class="sxs-lookup"><span data-stu-id="7d11a-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="7d11a-109">Till skillnad från bokningar är tilldelningar åtagande av resurser till projektuppgifter i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="7d11a-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7d11a-110">Resurserna kan vara namngivna eller generiska.</span><span class="sxs-lookup"><span data-stu-id="7d11a-110">The resources can be named or generic.</span></span>  <span data-ttu-id="7d11a-111">När ett resurskrav härleds från projektuppgiftstilldelningarna använder Project Operations insatsprofilerna från resurstilldelningen för att skapa informationsprofiler om resurskrav.</span><span class="sxs-lookup"><span data-stu-id="7d11a-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="7d11a-112">En referens till resurstilldelningarna bibehålls emellertid inte.</span><span class="sxs-lookup"><span data-stu-id="7d11a-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="7d11a-113">Uppdateringar av de bokningar som härleds från resurskravet uppdaterar inga resurstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="7d11a-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="7d11a-114">Vanligtvis är summan av bokningarna för en resurs lika med summan av resursens tilldelningar för en eller flera uppgifter.</span><span class="sxs-lookup"><span data-stu-id="7d11a-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="7d11a-115">Project Operations verkställer emellertid inte detta avtal.</span><span class="sxs-lookup"><span data-stu-id="7d11a-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="7d11a-116">I vyn **avstämning** visas en projektledare där resursens bokningar och tilldelningar inte godkänner varandra.</span><span class="sxs-lookup"><span data-stu-id="7d11a-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]