---
title: Skapa tidsposter
description: I det här ämnet finns information om hur du skapar tidsposter.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756258"
---
# <a name="create-time-entries"></a><span data-ttu-id="29207-103">Skapa tidsposter</span><span class="sxs-lookup"><span data-stu-id="29207-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="29207-104">I tidigare versioner av Dynamics 365 Project Service Automation angavs tidsposter veckovis.</span><span class="sxs-lookup"><span data-stu-id="29207-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="29207-105">I version 3 av Project Service Automation anges tidsposter som dagliga uppgifter.</span><span class="sxs-lookup"><span data-stu-id="29207-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="29207-106">När du har skapat några tidsposter kan du dock skapa eller kopiera dem.</span><span class="sxs-lookup"><span data-stu-id="29207-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="29207-107">Skapa en tidspost</span><span class="sxs-lookup"><span data-stu-id="29207-107">Create a time entry</span></span>

<span data-ttu-id="29207-108">Följ dessa steg för att skapa en tidspost.</span><span class="sxs-lookup"><span data-stu-id="29207-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="29207-109">På sidan **Tidspost** klicka på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="29207-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="29207-110">I dialogrutan **Snabbregistrering: tidspost** ange varaktigheten av tidsposten i minuter, timmar eller dagar.</span><span class="sxs-lookup"><span data-stu-id="29207-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="29207-111">Varaktigheten måste anges i följande format: *x* minuter, *x* timmar eller *x* dagar.</span><span class="sxs-lookup"><span data-stu-id="29207-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="29207-112">Timmar och dagar kan även anges som decimalvärden, till exempel *x.x* timmar eller *x.x* dagar.</span><span class="sxs-lookup"><span data-stu-id="29207-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="29207-113">Välj vilken typ av tidsposten och projektet som du vill registrera tidsposten för.</span><span class="sxs-lookup"><span data-stu-id="29207-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="29207-114">I fältet **projektuppgift** letar du upp uppgiften för den här tidsposten.</span><span class="sxs-lookup"><span data-stu-id="29207-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29207-115">Om du skapar en tid för en uppgift som inte är tilldelad en användare kan du välja fältet **projektuppgift**, välj knappen **Sök**, välj **Ändra vy** och välj sedan **Alla aktiva projektuppgifter** för att ange alla uppgifter.</span><span class="sxs-lookup"><span data-stu-id="29207-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="29207-116">Ange en beskrivning, om det behövs en beskrivning, och välj sedan **Spara och stäng**.</span><span class="sxs-lookup"><span data-stu-id="29207-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="29207-117">När du har skapat och sparat tidsposten kan du redigera den i rutnätet för tidsposten.</span><span class="sxs-lookup"><span data-stu-id="29207-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="29207-118">Rutnätet för tidsposten stöder två format:</span><span class="sxs-lookup"><span data-stu-id="29207-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="29207-119">Du kan ange tidsposter i formatet **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="29207-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="29207-120">Formatet konverteras sedan till timmar och bråktal.</span><span class="sxs-lookup"><span data-stu-id="29207-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="29207-121">Du kan ange timmar och bråktal direkt.</span><span class="sxs-lookup"><span data-stu-id="29207-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="29207-122">Observera att bråkdelen av en timme inte är några minuter.</span><span class="sxs-lookup"><span data-stu-id="29207-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="29207-123">Därför motsvarar 1,5 timmar 1 timme och 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="29207-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="29207-124">Samma regel gäller för bråkdelar av en dag.</span><span class="sxs-lookup"><span data-stu-id="29207-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="29207-125">En dag är 24 timmar och 0,5 dagar motsvarar 12 timmar.</span><span class="sxs-lookup"><span data-stu-id="29207-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="29207-126">Masskapa tidsposter</span><span class="sxs-lookup"><span data-stu-id="29207-126">Bulk create time entries</span></span>

<span data-ttu-id="29207-127">När du har skapat några tidsposter kan du kopiera dem för att skapa ytterligare många tidsposter samtidigt.</span><span class="sxs-lookup"><span data-stu-id="29207-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="29207-128">På sidan **Tidspost** klicka på **Kopiera vecka**.</span><span class="sxs-lookup"><span data-stu-id="29207-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="29207-129">I fältgruppen **från period** i fälten **Startdatum** och **Slutdatum** definierar du datumintervallet för att kopiera tidsposter från.</span><span class="sxs-lookup"><span data-stu-id="29207-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="29207-130">I fältgruppen **Till period** i fältet **Startdatum**, ange datumet att skapa tidsposter för.</span><span class="sxs-lookup"><span data-stu-id="29207-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="29207-131">Välj **kopiera** om du vill skapa en kopia av de tidsposter som motsvarar den veckodag som anges i fältgruppen **till period**.</span><span class="sxs-lookup"><span data-stu-id="29207-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="29207-132">Exempelvis kopieras tidsposten för måndagen i den senaste veckan till måndagen i veckan som anges i fältgruppen **till period**.</span><span class="sxs-lookup"><span data-stu-id="29207-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="29207-133">Importera data för tidsposter</span><span class="sxs-lookup"><span data-stu-id="29207-133">Import data for time entries</span></span>

<span data-ttu-id="29207-134">Du kan importera data från projektbokningar och tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="29207-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="29207-135">När du importerar data kan du ange datumintervallet för de bokningar som ska importeras och sedan uttryckligen välja de bokningar som ska skapas som **utkast** tidsposter.</span><span class="sxs-lookup"><span data-stu-id="29207-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="29207-136">Gruppera efter, sortera, söka och filtrera funktioner</span><span class="sxs-lookup"><span data-stu-id="29207-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="29207-137">Du kan gruppera och filtrera tidsposter efter de dimensioner som anges i kolumnerna.</span><span class="sxs-lookup"><span data-stu-id="29207-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="29207-138">I fältet **gruppera efter** väljer du den dimension som ska användas för att filtrera tidsposter.</span><span class="sxs-lookup"><span data-stu-id="29207-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="29207-139">Du kan också sortera tidsposter i stigande eller fallande ordning med hjälp av pilen sortera i kolumnrubrikerna.</span><span class="sxs-lookup"><span data-stu-id="29207-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="29207-140">Du kan även visa eller dölja poster genom att välja knappen **Filter** i kolumnrubrikerna och i rutan **Sök** ange den text som ska användas för att söka efter tidsposter efter projektnamn, projektuppgift, tidspost eller resurs.</span><span class="sxs-lookup"><span data-stu-id="29207-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
