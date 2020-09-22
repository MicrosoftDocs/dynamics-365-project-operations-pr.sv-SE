---
title: Mobil arbetsyta för projektets tidspost
description: I den här ämne finns information om hur du använder mobil arbetsyta för projektets tidspost. På den här arbetsytan kan användare ange och spara tid för ett projekt med hjälp av deras mobila enheter.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756228"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="9f64a-104">Mobil arbetsyta för projektets tidspost</span><span class="sxs-lookup"><span data-stu-id="9f64a-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f64a-105">I den här ämne finns information om hur du använder mobil arbetsyta för **projektets tidspost**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="9f64a-106">På den här arbetsytan kan användare ange och spara tid för ett projekt med hjälp av deras mobila enheter.</span><span class="sxs-lookup"><span data-stu-id="9f64a-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="9f64a-107">Den här mobila arbetsytan är avsedd att användas tillsammans med Dynamics 365 Unified Ops-mobilapp.</span><span class="sxs-lookup"><span data-stu-id="9f64a-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="9f64a-108">Översikt</span><span class="sxs-lookup"><span data-stu-id="9f64a-108">Overview</span></span>
<span data-ttu-id="9f64a-109">Som en del av det dagliga arbetet är projektresurserna ofta på plats eller på resande fot.</span><span class="sxs-lookup"><span data-stu-id="9f64a-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="9f64a-110">**Projektets tidsinmatning** mobil arbetsyta kan användarna ange sin fakturerbara eller ej fakturerbar tid för ett projekt på den mobila enheten som de väljer.</span><span class="sxs-lookup"><span data-stu-id="9f64a-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="9f64a-111">Projektresurser kan därför registrera tidstransaktioner när som helst och var som helst.</span><span class="sxs-lookup"><span data-stu-id="9f64a-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="9f64a-112">De kan också visa tidtransaktioner som redan har registrerats.</span><span class="sxs-lookup"><span data-stu-id="9f64a-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="9f64a-113">Specifikt i **Projektets tidspost** kan mobil arbetsyta användarna utföra de här uppgifterna:</span><span class="sxs-lookup"><span data-stu-id="9f64a-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="9f64a-114">Ange antalet timmar som du har tillbringat för en viss uppgift för alla valda datum.</span><span class="sxs-lookup"><span data-stu-id="9f64a-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="9f64a-115">Sök efter projektnamn eller kund för att hitta projektet för att ange tid för.</span><span class="sxs-lookup"><span data-stu-id="9f64a-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="9f64a-116">Ange kategori och aktivitet för den tid du tillbringar.</span><span class="sxs-lookup"><span data-stu-id="9f64a-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="9f64a-117">Registrera tiden som fakturerbar eller ej fakturerbar för projektet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="9f64a-118">Ange eventuella externa eller interna kommentarer.</span><span class="sxs-lookup"><span data-stu-id="9f64a-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9f64a-119">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="9f64a-119">Prerequisites</span></span>
<span data-ttu-id="9f64a-120">Förutsättningarna varierar beroende på vilken version av Microsoft Dynamics 365 som har distribuerats för organisationen.</span><span class="sxs-lookup"><span data-stu-id="9f64a-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="9f64a-121">Krav om du använder Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9f64a-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="9f64a-122">Om Finance har distribuerats för organisationen måste systemadministratör publicera mobil arbetsytan **Projektets tidspost**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="9f64a-123">Instruktioner om hur du [publicerar en mobil arbetsyta](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="9f64a-124">Förutsättningar om du använder version 1611 med plattformsuppdatering 3 eller senare</span><span class="sxs-lookup"><span data-stu-id="9f64a-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="9f64a-125">Om version 1611 med plattformsuppdatering 3 eller senare har distribuerats för organisationen måste systemadministratör uppfylla följande krav.</span><span class="sxs-lookup"><span data-stu-id="9f64a-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9f64a-126">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="9f64a-126">Prerequisite</span></span></th>
<th><span data-ttu-id="9f64a-127">Roll</span><span class="sxs-lookup"><span data-stu-id="9f64a-127">Role</span></span></th>
<th><span data-ttu-id="9f64a-128">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9f64a-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="9f64a-129">Implementera KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="9f64a-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="9f64a-130">Systemadministratör</span><span class="sxs-lookup"><span data-stu-id="9f64a-130">System administrator</span></span></td>
<td><span data-ttu-id="9f64a-131">KB 4018050 är en X++ uppdatering eller en snabb korrigering för mobil arbetsyta <strong>projekttidsinmatning</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f64a-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="9f64a-132">Innan du implementerar KB 4018050 måste systemadministratör följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="9f64a-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="9f64a-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Hämta snabb korrigeringen för metadata från Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="9f64a-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="9f64a-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installera snabbkorrigeringen för metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="9f64a-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="9f64a-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Skapa ett distribuerbart paket</a> som innehåller modellerna <strong>ApplicationSuite</strong> och <strong>ProjectMobile</strong> och överför sedan det distributionsbara paketet till LCS.</span><span class="sxs-lookup"><span data-stu-id="9f64a-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="9f64a-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Använd det distributionsbara paketet</a>.</span><span class="sxs-lookup"><span data-stu-id="9f64a-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f64a-137">Publicera arbetsytan <strong>Projektets tidspost</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f64a-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="9f64a-138">Systemadministratör</span><span class="sxs-lookup"><span data-stu-id="9f64a-138">System administrator</span></span></td>
<td><span data-ttu-id="9f64a-139">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">publicerar en mobil arbetsyta</a>.</span><span class="sxs-lookup"><span data-stu-id="9f64a-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="9f64a-140">Ladda ned och installera en mobilapp</span><span class="sxs-lookup"><span data-stu-id="9f64a-140">Download and install the mobile app</span></span>

<span data-ttu-id="9f64a-141">Ladda ned och installera mobilappen Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="9f64a-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="9f64a-142">För Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="9f64a-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="9f64a-143">För iPhones</span><span class="sxs-lookup"><span data-stu-id="9f64a-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="9f64a-144">Logga in på mobilappen</span><span class="sxs-lookup"><span data-stu-id="9f64a-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="9f64a-145">Starta appen på din mobila enhet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="9f64a-146">Ange din Dynamics 365 URL</span><span class="sxs-lookup"><span data-stu-id="9f64a-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="9f64a-147">Första gången du loggar in ombeds du ange ditt användarnamn och lösenord.</span><span class="sxs-lookup"><span data-stu-id="9f64a-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="9f64a-148">Ange dina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="9f64a-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="9f64a-149">När du har loggat in visas de tillgängliga arbetsytorna för ditt företag.</span><span class="sxs-lookup"><span data-stu-id="9f64a-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="9f64a-150">Observera att om systemadministratören publicerar en ny arbetsyta senare måste du uppdatera listan med mobila arbetsytor.</span><span class="sxs-lookup"><span data-stu-id="9f64a-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="9f64a-151">[![Dra nedåt för att uppdatera](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="9f64a-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="9f64a-152">Ange tid genom att använda mobil arbetsyta för projektets tidsinmatning</span><span class="sxs-lookup"><span data-stu-id="9f64a-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="9f64a-153">På din mobila enhet, välj arbetsytan **Projektets tidspost**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="9f64a-154">Välj **Tidspost**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-154">Select **Time entry**.</span></span> <span data-ttu-id="9f64a-155">Kalenderdatumen för den aktuella veckan visas.</span><span class="sxs-lookup"><span data-stu-id="9f64a-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="9f64a-156">För ett valt datum, välj **Åtgärder** &gt; **Ny inmatning**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="9f64a-157">Ange hur många objekt som ska registreras.</span><span class="sxs-lookup"><span data-stu-id="9f64a-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="9f64a-158">Välj projekt för tidsposten.</span><span class="sxs-lookup"><span data-stu-id="9f64a-158">Select the project for the time entry.</span></span> <span data-ttu-id="9f64a-159">En lista visar de projekt som har lästs in i din app för användning offline.</span><span class="sxs-lookup"><span data-stu-id="9f64a-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="9f64a-160">Som standard laddas 50 objekt, men en utvecklare kan ändra antalet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="9f64a-161">Mer information finns i [mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="9f64a-162">Om projektet inte finns med i listan väljer du **Sök**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="9f64a-163">Sök efter namn eller växla till sökning efter projektnamn eller kund.</span><span class="sxs-lookup"><span data-stu-id="9f64a-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="9f64a-164">Välj en kategori.</span><span class="sxs-lookup"><span data-stu-id="9f64a-164">Select a category.</span></span> <span data-ttu-id="9f64a-165">En lista visar de kategorier som har lästs in i din app för användning offline.</span><span class="sxs-lookup"><span data-stu-id="9f64a-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="9f64a-166">Som standard laddas 50 objekt, men en utvecklare kan ändra antalet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="9f64a-167">Mer information finns i [mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="9f64a-168">Om kategorin inte finns med i listan väljer du **Sök**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="9f64a-169">Sök efter kategori eller växla till att söka efter kategorinamn.</span><span class="sxs-lookup"><span data-stu-id="9f64a-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="9f64a-170">Välj en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-170">Select an activity.</span></span> <span data-ttu-id="9f64a-171">En lista visar de aktiviteter som har lästs in i din app för användning offline.</span><span class="sxs-lookup"><span data-stu-id="9f64a-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="9f64a-172">Som standard laddas 50 objekt, men en utvecklare kan ändra antalet.</span><span class="sxs-lookup"><span data-stu-id="9f64a-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="9f64a-173">Mer information finns i [mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="9f64a-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="9f64a-174">Om din aktivitet inte finns med i listan väljer du **Sök**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="9f64a-175">Sök efter aktivitetsnummer eller växla till sök efter syfte.</span><span class="sxs-lookup"><span data-stu-id="9f64a-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="9f64a-176">Välj radegenskapen.</span><span class="sxs-lookup"><span data-stu-id="9f64a-176">Select the line property.</span></span>
12. <span data-ttu-id="9f64a-177">Valfritt: Ange eventuella externa och interna kommentarer.</span><span class="sxs-lookup"><span data-stu-id="9f64a-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="9f64a-178">Välj **Utfört**.</span><span class="sxs-lookup"><span data-stu-id="9f64a-178">Select **Done**.</span></span>
