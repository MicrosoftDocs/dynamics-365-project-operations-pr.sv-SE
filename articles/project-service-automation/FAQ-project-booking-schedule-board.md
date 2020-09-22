---
title: Skapa en projektbokning från schemaläggningstavlan
description: I det här ämnet finns information om hur du skapar en projektbokning från schemaläggningstavlan.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756275"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="a51a2-103">Skapa en projektbokning från schemaläggningstavlan</span><span class="sxs-lookup"><span data-stu-id="a51a2-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="a51a2-104">Du kan boka en resurs för ett projekt direkt från fliken **Team** på projektet eller genom att skapa ett resurskrav från en tilldelning av en allmän teammedlem och sedan uppfylla det genererade kravet med en projektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="a51a2-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="a51a2-105">Du kan också boka en resurs till ett projekt direkt från schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="a51a2-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="a51a2-106">Det finns tre sätt att göra det:</span><span class="sxs-lookup"><span data-stu-id="a51a2-106">There are three ways to do this:</span></span>

- <span data-ttu-id="a51a2-107">**Boka från ett genererat resurskrav:** du kan skapa ett resurskrav efter att du har skapat en generisk resurs och tilldelning av uppgifter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="a51a2-108">**Boka från det primära kravet:** de primära kraven visas på schemaläggningstavlan på fliken **projekt**.</span><span class="sxs-lookup"><span data-stu-id="a51a2-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="a51a2-109">**Boka från ett nytt resurskrav:** du kan skapa ett resurskrav från grunden och associera det med ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="a51a2-110">Resurskravet visas i fliken **Öppna krav** på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="a51a2-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="a51a2-111">Boka från ett genererat resurskrav</span><span class="sxs-lookup"><span data-stu-id="a51a2-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="a51a2-112">Du kan skapa en generisk resurs och tilldela den en eller flera aktiviteter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="a51a2-113">Du kan sedan generera ett resurskrav från den generiske teammedlemmen.</span><span class="sxs-lookup"><span data-stu-id="a51a2-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="a51a2-114">På schemaläggningstavlan visas denna resurs i fliken **Öppna krav** fliken. Du kan behöva använda kolumnfilter i rutnätet om du har många öppna krav.</span><span class="sxs-lookup"><span data-stu-id="a51a2-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="a51a2-115">![Öppna en kravflik på schemaläggningstavlan](media/FAQ-Project-Booking-Schedule-Board-1.png "Skärmbild på tabell för bokningar och tilldelningar")</span><span class="sxs-lookup"><span data-stu-id="a51a2-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="a51a2-116">Välj krav.</span><span class="sxs-lookup"><span data-stu-id="a51a2-116">Select the requirement.</span></span> <span data-ttu-id="a51a2-117">Fliken **Sök tillgänglighet** visas högst upp på den valda raden.</span><span class="sxs-lookup"><span data-stu-id="a51a2-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="a51a2-118">När du sedan väljer fliken öppnas schemaläggningstavlans läge för schemaläggningshjälp, och tillgängliga resurser som uppfyller kraven för resursen filtreras.</span><span class="sxs-lookup"><span data-stu-id="a51a2-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="a51a2-119">Därifrån kan du boka en resurs.</span><span class="sxs-lookup"><span data-stu-id="a51a2-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="a51a2-120">Du kan också dra och släppa den markerade raden från botten av schemaläggningstavlan till en resurscell i rutnätet ovan.</span><span class="sxs-lookup"><span data-stu-id="a51a2-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="a51a2-121">När du släpper öppnas panelen **Skapa resursbokning** till höger.</span><span class="sxs-lookup"><span data-stu-id="a51a2-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="a51a2-122">Om du väljer **Boka** bokas resursen till projektteamet.</span><span class="sxs-lookup"><span data-stu-id="a51a2-122">Selecting **Book** books the resource onto the project team.</span></span>

![Skapa resursbokningspanel](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="a51a2-124">Boka från primärt krav</span><span class="sxs-lookup"><span data-stu-id="a51a2-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="a51a2-125">Om du skapar ett projekt i Project Service skapas automatiskt ett resurskrav kallat "primärt krav".</span><span class="sxs-lookup"><span data-stu-id="a51a2-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="a51a2-126">Detta är ett tomt krav som används för att snabbt boka en resurs via schemaläggningstavlan utan att generera ett krav eller skapa ett helt nytt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="a51a2-127">Eftersom kravet är tomt måste du ange datum samt tilldelning och arbetstimmar (om tillämpligt).</span><span class="sxs-lookup"><span data-stu-id="a51a2-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="a51a2-128">För att boka en resurs med det primära kravet markerar du fliken **Projekt** på schemaläggningstavlan. Du kan komma att behöva använda kolumnfiltret på kolumnen **Projekt** om du har många projekt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="a51a2-129">![Kolumnfilter på schemaläggningstavlan](media/FAQ-Project-Booking-Schedule-Board-2.png "Skärmbild på tabell för bokningar och tilldelningar")</span><span class="sxs-lookup"><span data-stu-id="a51a2-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="a51a2-130">Välj det krav som bara har projektnamnet som namn och som har en varaktighet på noll (0).</span><span class="sxs-lookup"><span data-stu-id="a51a2-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="a51a2-131">Markera fliken **Sök tillgänglighet** som visas högst upp på raden.</span><span class="sxs-lookup"><span data-stu-id="a51a2-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="a51a2-132">Detta placerar schemaläggningstavlan i läget för schemaläggningshjälpen och visar tillgängliga resurser som kan bokas för projektet.</span><span class="sxs-lookup"><span data-stu-id="a51a2-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="a51a2-133">Eftersom ett **primärt krav** är ett tomt krav med zero (0) i varaktighet måste du ange en varaktighet på panelen **Skapa Resursbokning** när du väljer och bokar en resurs.</span><span class="sxs-lookup"><span data-stu-id="a51a2-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="a51a2-134">Du kan också välja **primärt krav för projektet** längst ned i schemaläggningstavlan och dra och släppa det på en resurs för att schemalägga det.</span><span class="sxs-lookup"><span data-stu-id="a51a2-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="a51a2-135">Eftersom ett **primärt krav** är ett tomt krav med zero (0) i varaktighet måste du ange en varaktighet på panelen **Skapa Resursbokning** när du väljer och bokar en resurs.</span><span class="sxs-lookup"><span data-stu-id="a51a2-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="a51a2-136">När du bokar en resurs via **primärt krav** på schemaläggningstavlan lägger du till den i projektteamet utan några tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="a51a2-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="a51a2-137">Boka från ett nytt resurskrav</span><span class="sxs-lookup"><span data-stu-id="a51a2-137">Book from a new resource requirement</span></span>
<span data-ttu-id="a51a2-138">Följ stegen nedan om du vill boka från ett nytt resurskrav.</span><span class="sxs-lookup"><span data-stu-id="a51a2-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="a51a2-139">Gå till **Resurskrav** och markera **Nytt** för att skapa ett nytt resurskrav.</span><span class="sxs-lookup"><span data-stu-id="a51a2-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="a51a2-140">Välj ett **projekt** på fliken projekt som du vill associera kravet med projektet.</span><span class="sxs-lookup"><span data-stu-id="a51a2-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="a51a2-141">PÅ schemaläggningstavlan visas detta nya krav som **Öppet krav** som du kan uppfylla.</span><span class="sxs-lookup"><span data-stu-id="a51a2-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="a51a2-142">Boka resursen för att lägga till den i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="a51a2-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="a51a2-143">Nu när resursen har bokats måste du tilldela uppgifter manuellt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-143">Now that the resource is booked, you must assign tasks manually.</span></span>

