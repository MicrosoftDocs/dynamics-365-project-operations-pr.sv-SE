---
title: Översikt över schemaläggningsassistenten
description: I det här ämnet finns information om hur du arbetar med schemaläggningsassistenten för att boka resurser.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908640"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="1a634-103">Översikt över schemaläggningsassistenten</span><span class="sxs-lookup"><span data-stu-id="1a634-103">Schedule assistant overview</span></span>

<span data-ttu-id="1a634-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="1a634-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a634-105">Schemaläggningsassistenten används för att boka resurser baserat på de krav som projektledaren har definierat.</span><span class="sxs-lookup"><span data-stu-id="1a634-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="1a634-106">Schemaläggningsassistenten använder de parametrar som ges i resurskravet för att hitta resursen.</span><span class="sxs-lookup"><span data-stu-id="1a634-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="1a634-107">Schemaläggningsassistenten rekommenderar resurser som uppfyller relevanta krav, t.ex. vilka tidsfönster eller kunskaper som behövs.</span><span class="sxs-lookup"><span data-stu-id="1a634-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="1a634-108">När lämpliga resurser identifieras kan resursen eller projektledaren boka resursen för arbetet.</span><span class="sxs-lookup"><span data-stu-id="1a634-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a634-109">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="1a634-109">Prerequisites</span></span>

<span data-ttu-id="1a634-110">Schemaläggningsassistenten ingår i lösningen Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="1a634-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="1a634-111">Lösningen ingår i och installeras med Dynamics 365 Project Operations, Dynamics 365 Field Service och Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="1a634-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="1a634-112">Matchningskrav och resurser</span><span class="sxs-lookup"><span data-stu-id="1a634-112">Matching requirements and resources</span></span>

<span data-ttu-id="1a634-113">Ett genererat resurskrav bygger på information som:</span><span class="sxs-lookup"><span data-stu-id="1a634-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="1a634-114">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="1a634-114">Characteristics</span></span>
-   <span data-ttu-id="1a634-115">Roller</span><span class="sxs-lookup"><span data-stu-id="1a634-115">Roles</span></span>
-   <span data-ttu-id="1a634-116">Affärsenheter</span><span class="sxs-lookup"><span data-stu-id="1a634-116">Business units</span></span>
-   <span data-ttu-id="1a634-117">Resursinställningar</span><span class="sxs-lookup"><span data-stu-id="1a634-117">Resource preferences</span></span>
-   <span data-ttu-id="1a634-118">Insatsprofiler</span><span class="sxs-lookup"><span data-stu-id="1a634-118">Effort contours</span></span>
-   <span data-ttu-id="1a634-119">Tidszon</span><span class="sxs-lookup"><span data-stu-id="1a634-119">Time zone</span></span>

<span data-ttu-id="1a634-120">I schemaläggningsassistenten används dessa uppgifter för att filtrera resurser.</span><span class="sxs-lookup"><span data-stu-id="1a634-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="1a634-121">Öppna schemaläggningsassistenten</span><span class="sxs-lookup"><span data-stu-id="1a634-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="1a634-122">Det finns två sätt att starta schemaläggningsassistenten.</span><span class="sxs-lookup"><span data-stu-id="1a634-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="1a634-123">Om du använder hybridläget kan du välja valfri teammedlem i rutnätet med teammedlemmar med ett resurskrav som inte har uppfyllts och sedan välja **Boka**.</span><span class="sxs-lookup"><span data-stu-id="1a634-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="1a634-124">Om du använder centralläget söker resurshanteraren efter och väljer resursen.</span><span class="sxs-lookup"><span data-stu-id="1a634-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="1a634-125">Filter för schemaläggningsassistenten</span><span class="sxs-lookup"><span data-stu-id="1a634-125">Schedule assistant filters</span></span>

<span data-ttu-id="1a634-126">När schemaläggningsassistenten har körts visas informationen från resurskravet som filtrerade värden i den vänstra rutan.</span><span class="sxs-lookup"><span data-stu-id="1a634-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="1a634-127">Resurshanteraren eller projektledaren kan finjustera resultaten genom att justera filter så att det motsvarar schemaläggningsbehoven.</span><span class="sxs-lookup"><span data-stu-id="1a634-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="1a634-128">I filterrutan visas alternativen för arbete, t.ex.:</span><span class="sxs-lookup"><span data-stu-id="1a634-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="1a634-129">Arbetets start och slut</span><span class="sxs-lookup"><span data-stu-id="1a634-129">Work start and end</span></span>
-   <span data-ttu-id="1a634-130">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="1a634-130">Characteristics</span></span>
-   <span data-ttu-id="1a634-131">Roller</span><span class="sxs-lookup"><span data-stu-id="1a634-131">Roles</span></span>
-   <span data-ttu-id="1a634-132">Organisationsenheter</span><span class="sxs-lookup"><span data-stu-id="1a634-132">Organizational units</span></span>
-   <span data-ttu-id="1a634-133">Resursföretag</span><span class="sxs-lookup"><span data-stu-id="1a634-133">Resourcing company</span></span>
-   <span data-ttu-id="1a634-134">Resurstyper</span><span class="sxs-lookup"><span data-stu-id="1a634-134">Resource types</span></span>
-   <span data-ttu-id="1a634-135">Prioriterade resurser</span><span class="sxs-lookup"><span data-stu-id="1a634-135">Preferred resources</span></span>
