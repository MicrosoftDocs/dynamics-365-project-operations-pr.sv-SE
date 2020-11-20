---
title: Hantera flera tidszoner
description: När ett projekt skapas baseras tidszonen på den tidszon som har angetts i mallen för arbetstid.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119845"
---
# <a name="manage-time-zones"></a><span data-ttu-id="284e7-103">Hantera flera tidszoner</span><span class="sxs-lookup"><span data-stu-id="284e7-103">Manage time zones</span></span>

<span data-ttu-id="284e7-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="284e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="284e7-105">Projekt</span><span class="sxs-lookup"><span data-stu-id="284e7-105">Projects</span></span>

<span data-ttu-id="284e7-106">När ett projekt skapas baseras tidszonen på den tidszon som har angetts i mallen för arbetstid.</span><span class="sxs-lookup"><span data-stu-id="284e7-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="284e7-107">I formuläret **Projektet** är datumen alltid relativa till tidszonen för den användare som är inloggad på varje flik, med undantag för fliken **Uppgift**. När du visar uppdelad arbetsstruktur visas alltid datumen i projektets tidszon.</span><span class="sxs-lookup"><span data-stu-id="284e7-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="284e7-108">Aktiviteter</span><span class="sxs-lookup"><span data-stu-id="284e7-108">Tasks</span></span>

<span data-ttu-id="284e7-109">När en uppgift skapas styrs starttid, sluttid och timmar/dag av arbetstiderna för projektet.</span><span class="sxs-lookup"><span data-stu-id="284e7-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="284e7-110">Om en uppgift till exempel skapas med ett projekt vars tidszon är -8 PST och har följande arbetstider: 9:00 till 17:00 måndag till fredag. Uppgifter som skapas utan en tilldelning håller sig till starttiden och sluttiden i projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="284e7-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="284e7-111">Hantera resurser med tidszoner</span><span class="sxs-lookup"><span data-stu-id="284e7-111">Manage resources with time zones</span></span>

<span data-ttu-id="284e7-112">För korrekta och förutsägbara resultat när du använder **Utöka bokning** finns två viktiga förutsättningar som måste uppfyllas:</span><span class="sxs-lookup"><span data-stu-id="284e7-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="284e7-113">Användaren måste konfigurera tidszonen för sina enheter så att den motsvarar den tidszon som har angetts i systemets **anpassningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="284e7-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Tidszonsinställningar i Windows 10](media/reconcile-assignments-03.png)

  ![Tidszonsinställningar i inställningar för personliga alternativ](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="284e7-116">Den bokningsbara resursen måste innehålla minst en minuts arbetstid som överlappar med de profiler som används för att definiera det begärda tillägget.</span><span class="sxs-lookup"><span data-stu-id="284e7-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="284e7-117">Till exempel följande resurser med arbetstider som faller mellan 9:00 och 19:00.</span><span class="sxs-lookup"><span data-stu-id="284e7-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Jämförelse av resursprofiler](media/reconcile-assignments-05.png)

<span data-ttu-id="284e7-119">Följande tabell visar:</span><span class="sxs-lookup"><span data-stu-id="284e7-119">The following table shows:</span></span>

- <span data-ttu-id="284e7-120">En projektkalendermall</span><span class="sxs-lookup"><span data-stu-id="284e7-120">A project calendar template</span></span>
- <span data-ttu-id="284e7-121">Resurs A: den här resursen har samma kalender och finns i samma tidszon som i projektet.</span><span class="sxs-lookup"><span data-stu-id="284e7-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="284e7-122">Starttiden för bokningarna blir 9:00.</span><span class="sxs-lookup"><span data-stu-id="284e7-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="284e7-123">Resurs B: den här resursen finns i en annan tidszon än projektet och startar klockan 7:00 i sin tidszon.</span><span class="sxs-lookup"><span data-stu-id="284e7-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="284e7-124">Bokningarna kan emellertid börja klockan 9:00 eftersom det är den tidigaste starttiden för tilldelningens profil.</span><span class="sxs-lookup"><span data-stu-id="284e7-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="284e7-125">Resurser C och D: resurserna finns i olika tidszoner, de skiljer sig från varandra och projektet och deras bokningar startas inte tidigare än deras respektive tillgängliga starttider.</span><span class="sxs-lookup"><span data-stu-id="284e7-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="284e7-126">Entitet</span><span class="sxs-lookup"><span data-stu-id="284e7-126">Entity</span></span>  |<span data-ttu-id="284e7-127">Kalender</span><span class="sxs-lookup"><span data-stu-id="284e7-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="284e7-128">Projektkalendermall</span><span class="sxs-lookup"><span data-stu-id="284e7-128">Project calendar template</span></span>   | ![projektkalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="284e7-130">Resurs A</span><span class="sxs-lookup"><span data-stu-id="284e7-130">Resource A</span></span>  | ![Resurs A kalendern](media/reconcile-assignments-06.png) |
|<span data-ttu-id="284e7-132">Resurs B</span><span class="sxs-lookup"><span data-stu-id="284e7-132">Resource B</span></span>  |  ![Resurs B kalendern](media/reconcile-assignments-07.png) |
|<span data-ttu-id="284e7-134">Resurs C</span><span class="sxs-lookup"><span data-stu-id="284e7-134">Resource C</span></span>  |  ![Resurs C kalendern](media/reconcile-assignments-08.png) |
|<span data-ttu-id="284e7-136">Resurs D</span><span class="sxs-lookup"><span data-stu-id="284e7-136">Resource D</span></span>  | ![Resurs D kalendern](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="284e7-138">När du navigerar till vyn **Avstämning** visas resurstilldelningarna och tillhörande bokningsunderskott.</span><span class="sxs-lookup"><span data-stu-id="284e7-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vyn avstämning före tillägg](media/reconcile-assignments-10.png)

<span data-ttu-id="284e7-140">När funktionen för att utöka bokning har använts för varje resurs utökas bokningarna för varje resurs eftersom arbetstiderna för varje resurs överlappar profilen för underskottet.</span><span class="sxs-lookup"><span data-stu-id="284e7-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vyn avstämning efter bokningstillägget](media/reconcile-assignments-11.png) 

<span data-ttu-id="284e7-142">Observera att informationen i bokningarna visar olikheter i starttiden för bokningarna.</span><span class="sxs-lookup"><span data-stu-id="284e7-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="284e7-143">Bokningarna börjar inte tidigare än starttiden för tilldelningens profil och tidigast den tillgängliga starttiden för resursen.</span><span class="sxs-lookup"><span data-stu-id="284e7-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nya bokningar av de resurser som har schemaläggningstavlan](media/reconcile-assignments-12.png)
