---
title: Integrering för Microsoft Project Client
description: Det kan vara komplicerat att planera och underhålla ett projekt. Det innebär att projektledarna måste använda verktyg som hjälper dem att hantera den här uppgiften. Integrering med Microsoft Project Client tillhandahåller stöd för att öppna och hantera en uppdelad arbetsstruktur för projekt.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289346"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="02924-104">Integrering för Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="02924-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02924-105">Det kan vara komplicerat att planera och underhålla ett projekt. Det innebär att projektledarna måste använda verktyg som hjälper dem att hantera den här uppgiften.</span><span class="sxs-lookup"><span data-stu-id="02924-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="02924-106">Integrering med Microsoft Project Client tillhandahåller stöd för att öppna och hantera en uppdelad arbetsstruktur för projekt.</span><span class="sxs-lookup"><span data-stu-id="02924-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="02924-107">Projektledaren kan publicera alla ändringar i Dynamics 365 Finance uppdelad arbetsstruktur för projekt.</span><span class="sxs-lookup"><span data-stu-id="02924-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="02924-108">Om du använder uppdateringen från juli (version 10.0.4) måste du installera KB 4054797 och 4055884.</span><span class="sxs-lookup"><span data-stu-id="02924-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="02924-109">Konfigurera tillägget Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="02924-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="02924-110">För att aktivera Microsoft Project Client krävs tillägg Microsoft Dynamics 365 krävs för att installeras i användarens klient Microsoft Project-appar.</span><span class="sxs-lookup"><span data-stu-id="02924-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="02924-111">Det gör du genom att öppna **arbetsytan projektledning**.</span><span class="sxs-lookup"><span data-stu-id="02924-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="02924-112">•   Klicka på **Konfigurera tillägg för projektklient** från avsnittet **Länkar** > **Konfiguration** på arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="02924-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="02924-113">•   Klicka på **Öppna** och sedan på **Kör** när du uppmanas till det.</span><span class="sxs-lookup"><span data-stu-id="02924-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="02924-114">Öppna och redigera ett befintligt utkast av uppdelad arbetsstruktur i Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="02924-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="02924-115">Om ett projekt Dynamics 365 Finance redan har en uppdelad arbetsstruktur kan du öppna arbetsstrukturen i Microsoft Project Client-appar om strukturen för arbete är i utkastform.</span><span class="sxs-lookup"><span data-stu-id="02924-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="02924-116">Om du vill öppna från **Projekt** klickar du på länken **Öppna i Microsoft Project** fliken **Plan**. Du kan även öppna den här sidan från Microsoft Project Client-appar genom att klicka på **Öppna** i fliken **Microsoft Dynamics 365**. Välj **juridisk person** och **projekt** i listan.</span><span class="sxs-lookup"><span data-stu-id="02924-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="02924-117">Om du använder Internet Explorer som webbläsare måste du klicka på **Spara** för att manuellt öppna från platsen där filen hämtas till.</span><span class="sxs-lookup"><span data-stu-id="02924-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="02924-118">Du kan också klicka på **Spara och öppna** för att öppna filen i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="02924-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="02924-119">Byt inte namn på filnamnet när du sparar.</span><span class="sxs-lookup"><span data-stu-id="02924-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="02924-120">Innan du gör några ändringar i filen med Microsoft Project Client måste du checka ut den. Klicka på **checka ut** på fliken **Microsoft Dynamics 365**. Detta gör att andra användare inte kan redigera uppdelad arbetsstruktur från Finance på samma gång.</span><span class="sxs-lookup"><span data-stu-id="02924-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="02924-121">Om du vill publicera uppdelad arbetsstrukturen när du har slutfört eventuella ändringar klickar du på **checka in** på fliken **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="02924-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="02924-122">Om ett projektteam redan har lagts till i projektet i Finance kommer resurslistan att fyllas i med teammedlemmarna.</span><span class="sxs-lookup"><span data-stu-id="02924-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="02924-123">Om ett projektteam ännu inte har lagts till i projektet kan du välja resurser och bygga teamet i Microsoft Project Client genom att klicka på knappen **Resurser** på fliken **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="02924-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="02924-124">Följande data kommer att synkroniseras tillbaka till Finance som en del av incheckningsprocessen:</span><span class="sxs-lookup"><span data-stu-id="02924-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="02924-125">•   Uppgiftsnamn</span><span class="sxs-lookup"><span data-stu-id="02924-125">•   Task name</span></span>

<span data-ttu-id="02924-126">•   Startdatum</span><span class="sxs-lookup"><span data-stu-id="02924-126">•   Start date</span></span>

<span data-ttu-id="02924-127">•   Slutdatum</span><span class="sxs-lookup"><span data-stu-id="02924-127">•   Finish date</span></span>

<span data-ttu-id="02924-128">•   Föregångare</span><span class="sxs-lookup"><span data-stu-id="02924-128">•   Predecessors</span></span>

<span data-ttu-id="02924-129">•   Resursnamn</span><span class="sxs-lookup"><span data-stu-id="02924-129">•   Resource names</span></span>

<span data-ttu-id="02924-130">•   Kategori</span><span class="sxs-lookup"><span data-stu-id="02924-130">•   Category</span></span>

<span data-ttu-id="02924-131">•   Resurskategori</span><span class="sxs-lookup"><span data-stu-id="02924-131">•   Resource category</span></span>

<span data-ttu-id="02924-132">•   Arbetstider</span><span class="sxs-lookup"><span data-stu-id="02924-132">•   Work hours</span></span>

<span data-ttu-id="02924-133">•   Anteckningar</span><span class="sxs-lookup"><span data-stu-id="02924-133">•   Notes</span></span>

<span data-ttu-id="02924-134">•   Prioritet</span><span class="sxs-lookup"><span data-stu-id="02924-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="02924-135">Om du lägger till några andra kolumner i Microsoft Project Client-filen sparas de inte i filen och kommer inte att visas när filen öppnas igen.</span><span class="sxs-lookup"><span data-stu-id="02924-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="02924-136">Skapa en uppdelad arbetsstruktur för ett befintligt projekt med hjälp av Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="02924-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="02924-137">För att skapa en ny uppdelad arbetsstruktur genom att använda Microsoft Project Client följ dessa steg:</span><span class="sxs-lookup"><span data-stu-id="02924-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="02924-138">Öppna Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="02924-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="02924-139">På fliken **Microsoft Dynamics 365** klicka på **Öppna**.</span><span class="sxs-lookup"><span data-stu-id="02924-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="02924-140">Välj **juridisk person** för projektet.</span><span class="sxs-lookup"><span data-stu-id="02924-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="02924-141">Välj **projektet**.</span><span class="sxs-lookup"><span data-stu-id="02924-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="02924-142">Klicka på **Prova** på fliken **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="02924-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="02924-143">När du är klar att publicera till Finance, klickar du på **Checka in** på fliken **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="02924-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="02924-144">Ersätt befintlig uppdelad arbetsstruktur för ett befintligt projekt med hjälp av Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="02924-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="02924-145">Gör så här om du vill skapa en ny uppdelad arbetsstruktur av Microsoft Project Client och ersätta en befintlig arbetsstruktur för ett befintligt projekt:</span><span class="sxs-lookup"><span data-stu-id="02924-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="02924-146">Öppna Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="02924-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="02924-147">Skapa schemat i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="02924-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="02924-148">På fliken **Microsoft Dynamics 365** klicka på **Spara ändringar** > **Ersätt befintligt projekt**.</span><span class="sxs-lookup"><span data-stu-id="02924-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="02924-149">Välj **juridisk person** för projektet.</span><span class="sxs-lookup"><span data-stu-id="02924-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="02924-150">Välj **projektet**.</span><span class="sxs-lookup"><span data-stu-id="02924-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="02924-151">Klicka på **OK**.</span><span class="sxs-lookup"><span data-stu-id="02924-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="02924-152">Skapa ett nytt projekt från Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="02924-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="02924-153">Öppna Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="02924-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="02924-154">Skapa schemat i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="02924-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="02924-155">På fliken **Microsoft Dynamics 365** klicka på **Spara ändringar** > **Spara till nytt projekt**.</span><span class="sxs-lookup"><span data-stu-id="02924-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="02924-156">Välj **juridisk person** för projektet.</span><span class="sxs-lookup"><span data-stu-id="02924-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="02924-157">Ange **Projekt-ID**, om nödvändigt.</span><span class="sxs-lookup"><span data-stu-id="02924-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="02924-158">Ange **produktnamnet**.</span><span class="sxs-lookup"><span data-stu-id="02924-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="02924-159">Välj **Projekttyp**, **Projektgruppen** och **Projektkontrakts-ID**.</span><span class="sxs-lookup"><span data-stu-id="02924-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="02924-160">Du kan också skapa ett nytt projektkontrakt genom att klicka på **nytt**.</span><span class="sxs-lookup"><span data-stu-id="02924-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="02924-161">Välj den **kalender** som ska användas för resurser.</span><span class="sxs-lookup"><span data-stu-id="02924-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="02924-162">Klicka på **OK**.</span><span class="sxs-lookup"><span data-stu-id="02924-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]