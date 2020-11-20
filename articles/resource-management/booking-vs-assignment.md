---
title: Bokningar kontra tilldelningar
description: I det här ämnet finns information om skillnaderna mellan resursbokningar och resurstilldelningar.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130240"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="32462-103">Bokningar kontra tilldelningar</span><span class="sxs-lookup"><span data-stu-id="32462-103">Bookings vs assignments</span></span>

<span data-ttu-id="32462-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="32462-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="32462-105">Bokningar är en fast eller preliminär allokering av resurser till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="32462-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="32462-106">Fasta bokningar förbrukar en resurs kapacitet.</span><span class="sxs-lookup"><span data-stu-id="32462-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="32462-107">Bokningar representerar organisationskoncept för grupper så att de kan förstå hur resurser ska engageras mellan olika projekt.</span><span class="sxs-lookup"><span data-stu-id="32462-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="32462-108">Dynamics 365 Project Operations beaktar bokningar som ett koncept på projektnivå.</span><span class="sxs-lookup"><span data-stu-id="32462-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="32462-109">Till skillnad från bokningar är tilldelningar åtagande av resurser till projektuppgifter i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="32462-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="32462-110">Resurserna kan vara namngivna eller generiska.</span><span class="sxs-lookup"><span data-stu-id="32462-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="32462-111">Vanligtvis är summan av bokningarna för en resurs lika med summan av resursens tilldelningar för en eller flera uppgifter.</span><span class="sxs-lookup"><span data-stu-id="32462-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="32462-112">Project Operations verkställer emellertid inte detta avtal.</span><span class="sxs-lookup"><span data-stu-id="32462-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="32462-113">I vyn **avstämning** visas en projektledare där resursens bokningar och tilldelningar inte godkänner varandra.</span><span class="sxs-lookup"><span data-stu-id="32462-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
