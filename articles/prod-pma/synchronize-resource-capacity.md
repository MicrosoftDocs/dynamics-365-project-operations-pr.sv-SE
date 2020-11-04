---
title: Synkronisera resurskapacitet
description: I det här ämnet finns information om hur du synkroniserar en resurs kapacitet för kalendrar och projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085518"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="5d79f-103">Synkronisera resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="5d79f-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d79f-104">Med hjälp av processerna för synkronisering av resurser kan du garantera att informationen för kalendern och baskalendern rinner ned i projektresursens schemaläggning.</span><span class="sxs-lookup"><span data-stu-id="5d79f-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="5d79f-105">Om kalendern ändras gör processerna de nödvändiga uppdateringarna till schemaläggning av projektresurser.</span><span class="sxs-lookup"><span data-stu-id="5d79f-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="5d79f-106">Processerna bidrar också till att förbättra prestanda eftersom kalenderns resursinformation synkroniseras i förväg.</span><span class="sxs-lookup"><span data-stu-id="5d79f-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="5d79f-107">Uppdateringarna av resursplaneringsinformationen kan därför snabbare uppdateras.</span><span class="sxs-lookup"><span data-stu-id="5d79f-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="5d79f-108">Vi rekommenderar att du schemalägger processerna som en batch i stället för en i taget.</span><span class="sxs-lookup"><span data-stu-id="5d79f-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="5d79f-109">I annat fall kommer någon att glömma bort de ingående datumen när informationen senast synkroniserades.</span><span class="sxs-lookup"><span data-stu-id="5d79f-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="5d79f-110">Om ingående datum inte används kan luckor uppstå vid synkronisering av datum.</span><span class="sxs-lookup"><span data-stu-id="5d79f-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synkronisering av kalender](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="5d79f-112">Synkronisering av resurskapacitets sammanslagningar</span><span class="sxs-lookup"><span data-stu-id="5d79f-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="5d79f-113">Synkroniseringsprocessen synkroniserar all information i resurskalendern.</span><span class="sxs-lookup"><span data-stu-id="5d79f-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="5d79f-114">Den här informationen inkluderar baskalenderinformation om eventuella ändringar i tabellen resurskalenderkapacitet för projektet.</span><span class="sxs-lookup"><span data-stu-id="5d79f-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="5d79f-115">Om nya resurser läggs till i projektet hjälper synkroniseringen till att säkerställa att den uppdaterade kalenderinformationen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="5d79f-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="5d79f-116">Du kan utföra synkroniseringen när som helst.</span><span class="sxs-lookup"><span data-stu-id="5d79f-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="5d79f-117">Vi rekommenderar att du använder en batch.</span><span class="sxs-lookup"><span data-stu-id="5d79f-117">We recommend that you use a batch.</span></span> <span data-ttu-id="5d79f-118">Alternativen är tillgängliga under synkroniseringen av kapacitetsreservationer.</span><span class="sxs-lookup"><span data-stu-id="5d79f-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="5d79f-119">Välj **Projektledning och redovisning** &gt; **Periodisk** &gt; **Synkronisering av kapacitet** &gt; **Synkronisering av resurskapacitets sammanslagningar**.</span><span class="sxs-lookup"><span data-stu-id="5d79f-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="5d79f-120">Ange alternativen visas i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="5d79f-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="5d79f-121">Alternativ</span><span class="sxs-lookup"><span data-stu-id="5d79f-121">Option</span></span>      | <span data-ttu-id="5d79f-122">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5d79f-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="5d79f-123">Periodkod</span><span class="sxs-lookup"><span data-stu-id="5d79f-123">Period code</span></span> | <span data-ttu-id="5d79f-124">Alternativt kan du välja en intervallkod för räkenskapsåret för att ange start- och slutdatum för synkroniseringsprocessen för resurskapacitets sammanslagningar.</span><span class="sxs-lookup"><span data-stu-id="5d79f-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="5d79f-125">Startdatum</span><span class="sxs-lookup"><span data-stu-id="5d79f-125">Start date</span></span>  | <span data-ttu-id="5d79f-126">Ange startdatum för synkroniseringsprocessen för resurskapacitets sammanslagning.</span><span class="sxs-lookup"><span data-stu-id="5d79f-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="5d79f-127">Slutdatum</span><span class="sxs-lookup"><span data-stu-id="5d79f-127">End date</span></span>    | <span data-ttu-id="5d79f-128">Ange slutdatum för synkroniseringsprocessen för resurskapacitets sammanslagning.</span><span class="sxs-lookup"><span data-stu-id="5d79f-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="5d79f-129">[![Synkroniseringsprocess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d79f-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
