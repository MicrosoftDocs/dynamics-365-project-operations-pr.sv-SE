---
title: Översikt över schemaläggningsassistenten
description: I det här ämnet finns information om hur du arbetar med schemaläggningsassistenten för att boka resurser.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125650"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="cc506-103">Översikt över schemaläggningsassistenten</span><span class="sxs-lookup"><span data-stu-id="cc506-103">Schedule assistant overview</span></span>

<span data-ttu-id="cc506-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="cc506-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc506-105">Schemaläggningsassistenten används för att boka resurser baserat på de krav som projektledaren har definierat.</span><span class="sxs-lookup"><span data-stu-id="cc506-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="cc506-106">Schemaläggningsassistenten använder de parametrar som ges i resurskravet för att hitta resursen.</span><span class="sxs-lookup"><span data-stu-id="cc506-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="cc506-107">Schemaläggningsassistenten rekommenderar resurser som uppfyller relevanta krav, t.ex. vilka tidsfönster eller kunskaper som behövs.</span><span class="sxs-lookup"><span data-stu-id="cc506-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="cc506-108">När lämpliga resurser identifieras kan resursen eller projektledaren boka resursen för arbetet.</span><span class="sxs-lookup"><span data-stu-id="cc506-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cc506-109">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="cc506-109">Prerequisites</span></span>

<span data-ttu-id="cc506-110">Schemaläggningsassistenten ingår i lösningen Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="cc506-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="cc506-111">Lösningen ingår i och installeras med Dynamics 365 Project Operations, Dynamics 365 Field Service och Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="cc506-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="cc506-112">Matchningskrav och resurser</span><span class="sxs-lookup"><span data-stu-id="cc506-112">Matching requirements and resources</span></span>

<span data-ttu-id="cc506-113">Ett genererat resurskrav bygger på information som:</span><span class="sxs-lookup"><span data-stu-id="cc506-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="cc506-114">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="cc506-114">Characteristics</span></span>
-   <span data-ttu-id="cc506-115">Roller</span><span class="sxs-lookup"><span data-stu-id="cc506-115">Roles</span></span>
-   <span data-ttu-id="cc506-116">Affärsenheter</span><span class="sxs-lookup"><span data-stu-id="cc506-116">Business units</span></span>
-   <span data-ttu-id="cc506-117">Resursinställningar</span><span class="sxs-lookup"><span data-stu-id="cc506-117">Resource preferences</span></span>
-   <span data-ttu-id="cc506-118">Insatsprofiler</span><span class="sxs-lookup"><span data-stu-id="cc506-118">Effort contours</span></span>
-   <span data-ttu-id="cc506-119">Tidszon</span><span class="sxs-lookup"><span data-stu-id="cc506-119">Time zone</span></span>

<span data-ttu-id="cc506-120">I schemaläggningsassistenten används dessa uppgifter för att filtrera resurser.</span><span class="sxs-lookup"><span data-stu-id="cc506-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="cc506-121">Öppna schemaläggningsassistenten</span><span class="sxs-lookup"><span data-stu-id="cc506-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="cc506-122">Det finns två sätt att starta schemaläggningsassistenten.</span><span class="sxs-lookup"><span data-stu-id="cc506-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="cc506-123">Om du använder hybridläget kan du välja valfri teammedlem i rutnätet med teammedlemmar med ett resurskrav som inte har uppfyllts och sedan välja **Boka**.</span><span class="sxs-lookup"><span data-stu-id="cc506-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="cc506-124">Om du använder centralläget söker resurshanteraren efter och väljer resursen.</span><span class="sxs-lookup"><span data-stu-id="cc506-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="cc506-125">Filter för schemaläggningsassistenten</span><span class="sxs-lookup"><span data-stu-id="cc506-125">Schedule assistant filters</span></span>

<span data-ttu-id="cc506-126">När schemaläggningsassistenten har körts visas informationen från resurskravet som filtrerade värden i den vänstra rutan.</span><span class="sxs-lookup"><span data-stu-id="cc506-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="cc506-127">Resurshanteraren eller projektledaren kan finjustera resultaten genom att justera filter så att det motsvarar schemaläggningsbehoven.</span><span class="sxs-lookup"><span data-stu-id="cc506-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="cc506-128">I filterrutan visas alternativen för arbete, t.ex.:</span><span class="sxs-lookup"><span data-stu-id="cc506-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="cc506-129">Arbetets start och slut</span><span class="sxs-lookup"><span data-stu-id="cc506-129">Work start and end</span></span>
-   <span data-ttu-id="cc506-130">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="cc506-130">Characteristics</span></span>
-   <span data-ttu-id="cc506-131">Roller</span><span class="sxs-lookup"><span data-stu-id="cc506-131">Roles</span></span>
-   <span data-ttu-id="cc506-132">Organisationsenheter</span><span class="sxs-lookup"><span data-stu-id="cc506-132">Organizational units</span></span>
-   <span data-ttu-id="cc506-133">Resursföretag</span><span class="sxs-lookup"><span data-stu-id="cc506-133">Resourcing company</span></span>
-   <span data-ttu-id="cc506-134">Resurstyper</span><span class="sxs-lookup"><span data-stu-id="cc506-134">Resource types</span></span>
-   <span data-ttu-id="cc506-135">Prioriterade resurser</span><span class="sxs-lookup"><span data-stu-id="cc506-135">Preferred resources</span></span>
