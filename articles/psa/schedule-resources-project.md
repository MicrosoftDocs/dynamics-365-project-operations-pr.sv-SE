---
title: Schemalägg resurser för ett projekt.
description: Schemalägga resurser för ett projekt i Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150465"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="dc585-103">Schemalägg resurser för ett projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dc585-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dc585-104">Du kan kontrollera resurstillgänglighet för att få en övergripande bild av hur bokade resurser är, eller du kan filtrera vyn efter färdigheter, team, plats och andra alternativ.</span><span class="sxs-lookup"><span data-stu-id="dc585-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="dc585-105">Schematavlan visar en lista över resurser och deras tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="dc585-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="dc585-106">Välj ett visningsläge för att visa tillgänglighet efter **Timmar**, **Dag**, **Vecka** eller **Månad**.</span><span class="sxs-lookup"><span data-stu-id="dc585-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="dc585-107">Det är viktigt att ställa in schematavlan innan du använder den.</span><span class="sxs-lookup"><span data-stu-id="dc585-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="dc585-108">Mer information finns i [Konfigurera schemaläggningstavlan (Field Service eller Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="dc585-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="dc585-109">Om du använder en äldre version och vill se resurstillgängligheten, se då [Visa resurstillgänglighet](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="dc585-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="dc585-110">Om du vill använda funktionen för schemaläggningstavla, geocoding och platstjänster, måste du aktivera kartor.</span><span class="sxs-lookup"><span data-stu-id="dc585-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="dc585-111">I huvudmenyn väljer du **Schemaläggning av resurs** > **Administration**.</span><span class="sxs-lookup"><span data-stu-id="dc585-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="dc585-112">Klicka på **Schemaläggningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="dc585-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="dc585-113">Öppna post och bläddra ned till avsnittet **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="dc585-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="dc585-114">I fältet **Anslut till kartor** väljer du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dc585-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="dc585-115">Godkänn villkoren och spara posten.</span><span class="sxs-lookup"><span data-stu-id="dc585-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="dc585-116">I huvudmenyn väljer du **Project Service** > **Schemaläggningstavla**.</span><span class="sxs-lookup"><span data-stu-id="dc585-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="dc585-117">Härifrån finns det flera sätt att schemalägga ett bokningskrav.</span><span class="sxs-lookup"><span data-stu-id="dc585-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="dc585-118">Välj den metod som fungerar för dig.</span><span class="sxs-lookup"><span data-stu-id="dc585-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="dc585-119">Hitta tillgängliga resurser</span><span class="sxs-lookup"><span data-stu-id="dc585-119">Find available resources</span></span>

1.  <span data-ttu-id="dc585-120">I listan **Bokningskrav** högerklickar du på en oplanerad bokning och välj något av följande:</span><span class="sxs-lookup"><span data-stu-id="dc585-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="dc585-121">Välj **Sök tillgänglighet - Aktuella resurser** för att hitta tillgängliga resurser i listan över resurser på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="dc585-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="dc585-122">Välj **Sök tillgänglighet - Aktuella resurser** för att hitta tillgängliga resurser bland resurserna i systemet</span><span class="sxs-lookup"><span data-stu-id="dc585-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="dc585-123">När du gör detta visar filtren alternativ för det valda bokningskravet.</span><span class="sxs-lookup"><span data-stu-id="dc585-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="dc585-124">När du ser en tillgänglig lucka högerklickar du på tidsluckan på schemaläggningstavlan och väljer **Boka här**.</span><span class="sxs-lookup"><span data-stu-id="dc585-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="dc585-125">Eller också kan du dra och släpp bokningskravet till den tillgängliga tidsluckan.</span><span class="sxs-lookup"><span data-stu-id="dc585-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="dc585-126">Boka en resurs med hjälp av den dagliga vyn och se vem som är underbokad</span><span class="sxs-lookup"><span data-stu-id="dc585-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="dc585-127">På schematavlan väljer du **Visa läge** och sedan **Dagar**.</span><span class="sxs-lookup"><span data-stu-id="dc585-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="dc585-128">Här visas en rutnätsvy över hur många timmar en resurs är bokad per dag och vilka dagar de är gratis.</span><span class="sxs-lookup"><span data-stu-id="dc585-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="dc585-129">Klicka på namnet på den resurs som du vill boka, och markera sedan **Boka**.</span><span class="sxs-lookup"><span data-stu-id="dc585-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="dc585-130">I dialogrutan **Resursbokning (skapa)** väljer du det projekt som du vill boka resursen för, tillsammans med bokningsmetod och start- och sluttider.</span><span class="sxs-lookup"><span data-stu-id="dc585-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="dc585-131">När du är klar väljer du **Boka**.</span><span class="sxs-lookup"><span data-stu-id="dc585-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="dc585-132">Visa i schemaläggningstavlan</span><span class="sxs-lookup"><span data-stu-id="dc585-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="dc585-133">Välj en ej schemalagd bokningskrav från listan längst ned.</span><span class="sxs-lookup"><span data-stu-id="dc585-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="dc585-134">Dra bokningskravet till en tillgänglig resurs/tidslucka på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="dc585-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="dc585-135">När du är klar väljer du **Boka**.</span><span class="sxs-lookup"><span data-stu-id="dc585-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="dc585-136">Ytterligare resurser</span><span class="sxs-lookup"><span data-stu-id="dc585-136">Additional resources</span></span>  
 [<span data-ttu-id="dc585-137">Guide för resurshanteraren</span><span class="sxs-lookup"><span data-stu-id="dc585-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
