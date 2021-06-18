---
title: Preliminärboka krav
description: I det här ämnet finns information om hur du preliminärbokar krav.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997938"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="2f8ba-103">Preliminärboka krav</span><span class="sxs-lookup"><span data-stu-id="2f8ba-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2f8ba-104">Ett resurskrav kan vara en fast bokning.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="2f8ba-105">En fast bokning skapar ett förslag som förbrukar resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="2f8ba-106">Förslaget skickas sedan tillbaka till användaren som skapade begäran för godkännande.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="2f8ba-107">En preliminär bokning lägger till en resurs i ett projektteam och har en annan status på schemaläggningstavlan, men den förbrukar inte resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="2f8ba-108">Om du vill preliminärboka en resurs från schemaläggingstavlan anger du fältet **bokningsstatus** fältet boknings status till **preliminär**.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Bokningsstatusen är inställd på preliminär](media/Resource-Management-image77.png)

<span data-ttu-id="2f8ba-110">När fliken **Team** finns i vyn **Namngivna teammedlemmar** visas resursen där.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="2f8ba-111">De preliminärbokade timmarna rapporteras i kolumnen **preliminärbokade timmar**.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Preliminärbokade timmar i vyn Namngivna teammedlemmar](media/Resource-Management-image78.png)

<span data-ttu-id="2f8ba-113">Preliminärbokade teammedlemmar kan tilldelas uppgifter.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-113">Soft-booked team members can be assigned to tasks.</span></span>

![Preliminärbokade teammedlemmar tilldelade till en uppgift.](media/Resource-Management-image79.png)

<span data-ttu-id="2f8ba-115">På fliken **avstämning** visas inga bokningar för en preliminärbokad resurs eftersom fliken **avstämning** endast betraktar fasta bokningar.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Preliminärbokad resurs utan bokningar på fliken avstämning](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="2f8ba-117">Du kan inte preliminärboka en resurs från ett krav som har genererats från en allmän teammedlem.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="2f8ba-118">På schemaläggningstavlan används olika färger för preliminärbokningar för en resurs.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Preliminärbokningar på schemaläggningstavlan](media/Resource-Management-image81.png)

<span data-ttu-id="2f8ba-120">Om du vill konvertera en preliminärbokning till en fast bokning högerklickar du på preliminärbokningen och väljer sedan **ändra status** \> **fast bokning** \> **fast**.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Ändra bokningsstatus till fast](media/Resource-Management-image82.png)

<span data-ttu-id="2f8ba-122">Bokningen ändras och status ändras på Schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="2f8ba-123">Eftersom bokningsstatusen är **hård** visas resursen som bokad och dess kapacitet och tillgänglighet justeras.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="2f8ba-124">Du kan använda samma metod för att annullera en fast bokning eller en preliminär bokning från Schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="2f8ba-125">Om du vill konvertera en preliminär bokning till en fast bokad på projektets flik **Team** klickar du på resursen och väljer **bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="2f8ba-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Bekräfta kommando](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]