---
title: Hur gör jag en ”preliminär bokning” av resurser i programversion 2.x?
description: Den här artikeln beskriver hur du kan preliminärboka teammedlemmar med Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286045"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="3f99b-103">Hur preliminärbokar jag resurser i webbappen (appen Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="3f99b-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3f99b-104">Du kan preliminärt schemalägga eller boka en resurs till ett projektteam i syfte att visa att du planerar att tilldela resursen till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="3f99b-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="3f99b-105">Preliminärbokningar förbrukar ingen tillgängliga kapacitet för en resurs.</span><span class="sxs-lookup"><span data-stu-id="3f99b-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="3f99b-106">Preliminärbokade teammedlemmar kan inte tilldelas projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="3f99b-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="3f99b-107">Endast resurser med statusen Fast bokning och bekräftelsetypen Bekräftad kan tilldelas uppgifter (förutsatt att de har tillräckligt med fasta bokningstimmar för att täcka tilldelningsinsatsen).</span><span class="sxs-lookup"><span data-stu-id="3f99b-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="3f99b-108">Preliminärbokade teammedlemmar för projektet visas i rutnätet Teammedlem tillsammans med sina preliminärbokade timmar som visas i kolumnen Preliminärbokning.</span><span class="sxs-lookup"><span data-stu-id="3f99b-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="3f99b-109">De visas också på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="3f99b-109">They also show up on the schedule board.</span></span> <span data-ttu-id="3f99b-110">De anger återigen ingen kapacitetsförbrukning, detta eftersom preliminärbokningar inte förbrukar någon kapacitet för en resurs.</span><span class="sxs-lookup"><span data-stu-id="3f99b-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="3f99b-111">Det finns tre sätt att preliminärboka en teammedlem för ett projekt med hjälp av Project Service-version 2.x.</span><span class="sxs-lookup"><span data-stu-id="3f99b-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="3f99b-112">Du kan preliminärboka via schemaläggningstavlan, använda funktionen Behåll bokningar eller genom att skapa en generisk resurs.</span><span class="sxs-lookup"><span data-stu-id="3f99b-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="3f99b-113">Dessa metoder beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="3f99b-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="3f99b-114">Preliminärboka med schemaläggningstavlan</span><span class="sxs-lookup"><span data-stu-id="3f99b-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="3f99b-115">Gör följande för att preliminärboka via schemaläggningstavlan:</span><span class="sxs-lookup"><span data-stu-id="3f99b-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="3f99b-116">Öppna schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="3f99b-116">Open the schedule board.</span></span>
2. <span data-ttu-id="3f99b-117">Använd projektfliken på den nedre panelen för bokningskrav på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="3f99b-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="3f99b-118">Hitta det projekt som du vill preliminärboka en resurs på.</span><span class="sxs-lookup"><span data-stu-id="3f99b-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="3f99b-119">Om du har många olika projekt, klicka då på kolumnrubriken för projekt och använd sedan filtret för att hitta projektet.</span><span class="sxs-lookup"><span data-stu-id="3f99b-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="3f99b-120">Klicka på projektet och dra och släpp det sedan på resursens tidsrutnät.</span><span class="sxs-lookup"><span data-stu-id="3f99b-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="3f99b-121">Då öppnas panelen Skapa resursbokning till höger.</span><span class="sxs-lookup"><span data-stu-id="3f99b-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="3f99b-122">Justera start-och slutdatum, välj bokningsstatusen "Preliminär" och ange arbetstimmar.</span><span class="sxs-lookup"><span data-stu-id="3f99b-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="3f99b-123">Klicka på Boka.</span><span class="sxs-lookup"><span data-stu-id="3f99b-123">Click Book.</span></span>
7. <span data-ttu-id="3f99b-124">Tillbaka i projektet anges resursen nu som en teammedlem med preliminärbokade timmar i kolumnen Preliminärbokat.</span><span class="sxs-lookup"><span data-stu-id="3f99b-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="3f99b-125">Tänk på att du inte kan tilldela dem till uppgifter på den uppdelade arbetsstrukturen (WBS), detta eftersom resurser måste ha fastbokats för teamet för att tilldelas.</span><span class="sxs-lookup"><span data-stu-id="3f99b-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="3f99b-126">Preliminärboka via funktionen Behåll bokningar</span><span class="sxs-lookup"><span data-stu-id="3f99b-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="3f99b-127">Gör följande för att preliminärboka via Behåll bokningar:</span><span class="sxs-lookup"><span data-stu-id="3f99b-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="3f99b-128">Klicka på Nytt i rutnätet för teammedlem.</span><span class="sxs-lookup"><span data-stu-id="3f99b-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="3f99b-129">Markera den bokningsbara resursrollen från/till.</span><span class="sxs-lookup"><span data-stu-id="3f99b-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="3f99b-130">Välj en fördelningsmetod annan än Ingen:</span><span class="sxs-lookup"><span data-stu-id="3f99b-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="3f99b-131">Full kapacitet</span><span class="sxs-lookup"><span data-stu-id="3f99b-131">Full Capacity</span></span>
- <span data-ttu-id="3f99b-132">Procentandelskapacitet</span><span class="sxs-lookup"><span data-stu-id="3f99b-132">Percentage Capacity</span></span>
- <span data-ttu-id="3f99b-133">Efter timmar - fördela jämnt</span><span class="sxs-lookup"><span data-stu-id="3f99b-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="3f99b-134">Efter timmar - tidigareläggning</span><span class="sxs-lookup"><span data-stu-id="3f99b-134">By Hours Front Load</span></span>
4. <span data-ttu-id="3f99b-135">Klicka på Spara.</span><span class="sxs-lookup"><span data-stu-id="3f99b-135">Click Save.</span></span> <span data-ttu-id="3f99b-136">Resursen visas i teamets rutnät och deras arbetstider anges som Fast.</span><span class="sxs-lookup"><span data-stu-id="3f99b-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="3f99b-137">Behåll resursens bokningar genom att klicka på Behåll bokningar.</span><span class="sxs-lookup"><span data-stu-id="3f99b-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="3f99b-138">Expandera resursen om du vill visa bokningar när schemaläggningstavlan öppnas.</span><span class="sxs-lookup"><span data-stu-id="3f99b-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="3f99b-139">Bokningen anges då som Fast.</span><span class="sxs-lookup"><span data-stu-id="3f99b-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="3f99b-140">Högerklicka på bokningen och - under Ändra Status - markera Preliminärboka och sedan Preliminär.</span><span class="sxs-lookup"><span data-stu-id="3f99b-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="3f99b-141">Bokningsstatusen är nu Preliminär.</span><span class="sxs-lookup"><span data-stu-id="3f99b-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="3f99b-142">När du stänger schemaläggningstavlan ser du att timmarna för resursen har ändrats från Fast till Preliminär i rutnätet för teammedlem.</span><span class="sxs-lookup"><span data-stu-id="3f99b-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="3f99b-143">Notera att om du fastbokar en resurs till teamet och sedan tilldelar dem uppgifter i WBS kommer detta, när du använder Behåll bokningar för att ändra statusen från Fast till Preliminär, att avlägsna tilldelningarna från aktiviteterna för den resursen, detta eftersom endast fastbokade resurser kan tilldelas till uppgifter.</span><span class="sxs-lookup"><span data-stu-id="3f99b-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="3f99b-144">Preliminärboka genom att skapa en generisk resurs</span><span class="sxs-lookup"><span data-stu-id="3f99b-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="3f99b-145">Du kan skapa en preliminärbokning genom att skapa en generisk resursteammedlem, komplettera med schemaläggningstavlan eller resursbegäran och ändra typen i samband med bokning.</span><span class="sxs-lookup"><span data-stu-id="3f99b-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="3f99b-146">I detta syfte, gör på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="3f99b-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="3f99b-147">Tilldela roller till de uppgifter som du vill skapa generiske teammedlemmar för i projektets WBS.</span><span class="sxs-lookup"><span data-stu-id="3f99b-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="3f99b-148">Klicka på Generera projektteam.</span><span class="sxs-lookup"><span data-stu-id="3f99b-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="3f99b-149">I rutnätet för projektteammedlem väljer du den generiska resursen och klickar sedan på Boka.</span><span class="sxs-lookup"><span data-stu-id="3f99b-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="3f99b-150">Välj den resurs som du vill boka i schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="3f99b-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="3f99b-151">Ändra bokningsstatusen till "Preliminär" i panelen Skapa resursbokning på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="3f99b-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="3f99b-152">Klicka på Boka eller Boka och avsluta.</span><span class="sxs-lookup"><span data-stu-id="3f99b-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="3f99b-153">När du har stängt schemaläggningstavlan visas den markerade resursen som tillagd i teamet med såväl preliminärbokade timmar som tilldelade timmar.</span><span class="sxs-lookup"><span data-stu-id="3f99b-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="3f99b-154">Du kan också se att den generiska resursen förblir i teamet som en indikator på att uppgifterna tilldelas en preliminärbokad teammedlem.</span><span class="sxs-lookup"><span data-stu-id="3f99b-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="3f99b-155">När du är redo att ändra en preliminärbokad teammedlemsresurs till en fastbokad teammedlem så att du kan tilldela dem till aktiviteter kan du göra följande:</span><span class="sxs-lookup"><span data-stu-id="3f99b-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="3f99b-156">Markera resursen och klicka på Behåll bokningar.</span><span class="sxs-lookup"><span data-stu-id="3f99b-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="3f99b-157">Expandera resursen om du vill visa bokningar när schemaläggningstavlan öppnas.</span><span class="sxs-lookup"><span data-stu-id="3f99b-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="3f99b-158">Bokningen markeras som Preliminär.</span><span class="sxs-lookup"><span data-stu-id="3f99b-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="3f99b-159">Högerklicka på bokningen och - under Ändra Status - markera Fastboka och sedan Fast.</span><span class="sxs-lookup"><span data-stu-id="3f99b-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="3f99b-160">Bokningsstatusen är nu Fast.</span><span class="sxs-lookup"><span data-stu-id="3f99b-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="3f99b-161">När du stänger schemaläggningstavlan ser du att timmarna för resursen har ändrats från Preliminär till Fast i rutnätet för teammedlem.</span><span class="sxs-lookup"><span data-stu-id="3f99b-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="3f99b-162">Du kan nu tilldela resursen till aktiviteter (förutsatt att det finns samstämmighet mellan fastbokade timmar och aktivitetens insatstimmar för tilldelningen).</span><span class="sxs-lookup"><span data-stu-id="3f99b-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="3f99b-163">Observera att om du har följt stegen för generisk resursexpediering i objekt #3 ovan, så kommer den generiske teammedlemmen att tas bort från teamet när du ändrar statusen för den preliminärbokade bokningsbara resursen till Fast.</span><span class="sxs-lookup"><span data-stu-id="3f99b-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]