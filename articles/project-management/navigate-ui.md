---
title: Navigera i användargränssnittet
description: I det här ämne finns information om projektledning i Dynamics 365 i projektåtgärder.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 715a8bdb9a1f38f71b4c42f5307ed4a5c7170ef6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014273"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="318b4-103">Navigera i användargränssnittet</span><span class="sxs-lookup"><span data-stu-id="318b4-103">Navigating the user interface</span></span>

<span data-ttu-id="318b4-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="318b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="318b4-105">Översikt</span><span class="sxs-lookup"><span data-stu-id="318b4-105">Overview</span></span>

<span data-ttu-id="318b4-106">Projektets huvudformulär är indelat på flera flikar.</span><span class="sxs-lookup"><span data-stu-id="318b4-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="318b4-107">Varje flik motsvarar en annan detaljnivå i projektet.</span><span class="sxs-lookup"><span data-stu-id="318b4-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="318b4-108">**Sammanfattning**: visar en beskrivning av projektet och aggregerar både planerat och faktiskt projektresultat.</span><span class="sxs-lookup"><span data-stu-id="318b4-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Fliken Sammanfattning och fält](media/navigation7.png)

- <span data-ttu-id="318b4-110">**Uppgifter**: innehåller information om uppdelad arbetsstruktur som representeras av en rutnätsvy, en trädvy och ett Gantt-schema.</span><span class="sxs-lookup"><span data-stu-id="318b4-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Fliken Uppgift och fält](media/navigation8.png)

- <span data-ttu-id="318b4-112">**Team**: ger information om projektdeltagarna.</span><span class="sxs-lookup"><span data-stu-id="318b4-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="318b4-113">Den tilldelade insatsen för varje teammedlem sammanfattas i den här vyn.</span><span class="sxs-lookup"><span data-stu-id="318b4-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Fliken Team och fält](media/navigation9.png)

- <span data-ttu-id="318b4-115">**Resurstilldelningar**: tillhandahåller en tidsfasad vy över arbetsinsatsen för varje resurs i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="318b4-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Fliken Resurstilldelningar och fält](media/navigation10.png)

- <span data-ttu-id="318b4-117">**Resursavstämning**: visar en tidsfasad vy över skillnaderna mellan tilldelningarna för varje namngiven resurs och deras bokningar.</span><span class="sxs-lookup"><span data-stu-id="318b4-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Fliken Resursavstämning och fält](media/navigation11.png)

- <span data-ttu-id="318b4-119">**Uppskattningar**: visar en tidsfasad vy över kostnads- och försäljningsuppskattningarna för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="318b4-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Fliken Uppskattningar och fält](media/navigation12.png)

- <span data-ttu-id="318b4-121">**Spårning**: en vy som visar förloppet för uppgifter i uppdelad arbetsstruktur för insats, kostnader och försäljning.</span><span class="sxs-lookup"><span data-stu-id="318b4-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Fliken Spårning och fält](media/navigation13.png)

- <span data-ttu-id="318b4-123">**Försäljning**: ger djupa länkar till offerter och kontrakt som är associerade med projektet.</span><span class="sxs-lookup"><span data-stu-id="318b4-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="318b4-124">**Utgiftsuppskattningar**: tillhandahåller ett rutnät som definierar projektutgifter baserat på organisationens utgiftskategorier.</span><span class="sxs-lookup"><span data-stu-id="318b4-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Fliken Utgiftsuppskattningar och fält](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="318b4-126">Rutnätskontroller</span><span class="sxs-lookup"><span data-stu-id="318b4-126">Grid controls</span></span>

<span data-ttu-id="318b4-127">Här följer en kortfattad översikt över de typiska kontroller som finns på flikarna för projektplanering.</span><span class="sxs-lookup"><span data-stu-id="318b4-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="318b4-128">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="318b4-128">Refresh</span></span>

<span data-ttu-id="318b4-129">**Uppdatera**: hämtar senaste data från servern om några ändringar gjordes efter att rutnätet lästes in.</span><span class="sxs-lookup"><span data-stu-id="318b4-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Knappen Uppdatera](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="318b4-131">Gruppera efter</span><span class="sxs-lookup"><span data-stu-id="318b4-131">Group by</span></span>

<span data-ttu-id="318b4-132">**Gruppera efter**: uppdaterar en grupp av rader i rutnätet så att den motsvarar antingen resurser, roller eller kategorier utifrån användarens behov.</span><span class="sxs-lookup"><span data-stu-id="318b4-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Gruppera efter knapp](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="318b4-134">Föregående/nästa</span><span class="sxs-lookup"><span data-stu-id="318b4-134">Previous/Next</span></span>

<span data-ttu-id="318b4-135">**Föregående**/**nästa**: uppdatera de synliga tidsperioderna för tidsfasade rutnät.</span><span class="sxs-lookup"><span data-stu-id="318b4-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Knapparna Föregående och Nästa](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="318b4-137">Tidsskala</span><span class="sxs-lookup"><span data-stu-id="318b4-137">Timescale</span></span>

<span data-ttu-id="318b4-138">**Tidsskala**: ändra sammansättningen av tidsfasdata mellan dagar, veckor, månader och år.</span><span class="sxs-lookup"><span data-stu-id="318b4-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Knappen Tidsskala](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="318b4-140">Utöka</span><span class="sxs-lookup"><span data-stu-id="318b4-140">Expand</span></span>

<span data-ttu-id="318b4-141">**Visa**: återger det synliga rutnätet på fullskärm så att fler roller kan visas.</span><span class="sxs-lookup"><span data-stu-id="318b4-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![knappen Visa detaljer](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="318b4-143">Tidsfas efter</span><span class="sxs-lookup"><span data-stu-id="318b4-143">Time-phase by</span></span>

<span data-ttu-id="318b4-144">**Tidsfas efter**: uppdatera grupperingen av raderna i rutnätet så att det visar kostnadsuppskattningar för försäljningsuppskattningar.</span><span class="sxs-lookup"><span data-stu-id="318b4-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="318b4-145">Den här kontrollen gäller även för uppskattningsskript och spårningsrutnät.</span><span class="sxs-lookup"><span data-stu-id="318b4-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Tidsfas efter knapp](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="318b4-147">Lägg till kolumn</span><span class="sxs-lookup"><span data-stu-id="318b4-147">Add column</span></span>

<span data-ttu-id="318b4-148">**Lägg till kolumn**: gör att användaren kan definiera de synliga kolumnerna i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="318b4-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="318b4-149">Endast kolumner som är färdiga kan läggas till i rutnäten i formuläret **Projektplanering**.</span><span class="sxs-lookup"><span data-stu-id="318b4-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Lägg till kolumnknapp](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]