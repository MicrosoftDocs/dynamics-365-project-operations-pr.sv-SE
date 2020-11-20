---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 25, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183565"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="fc479-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 25, version 3</span><span class="sxs-lookup"><span data-stu-id="fc479-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="fc479-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fc479-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fc479-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="fc479-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fc479-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fc479-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fc479-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="fc479-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fc479-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fc479-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fc479-109">I det här ämnet anges de funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdateringsutgåva 25. Denna version har versionsnumret V 3.10.43.76 och är i allmänhet tillgänglig genom en självuppdatering i oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="fc479-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="fc479-110">Uppdatering version 25</span><span class="sxs-lookup"><span data-stu-id="fc479-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fc479-111">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="fc479-111">Bug fixes</span></span>

<span data-ttu-id="fc479-112">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="fc479-112">**Time and Expense**</span></span>

<span data-ttu-id="fc479-113">Följande problem har korrigerats:</span><span class="sxs-lookup"><span data-stu-id="fc479-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="fc479-114">Tidstransaktionsdiagram som visar ytterligare data baserat på för stort för ett intervall som hämtas.</span><span class="sxs-lookup"><span data-stu-id="fc479-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="fc479-115">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="fc479-115">**Resource Management**</span></span>

<span data-ttu-id="fc479-116">Följande problem har korrigerats:</span><span class="sxs-lookup"><span data-stu-id="fc479-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="fc479-117">Lägger till Package Deployer-kod för att hoppa över Universal Resource Scheduling korrigeringsfilen om det redan finns en korrigeringsfil för versionen.</span><span class="sxs-lookup"><span data-stu-id="fc479-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="fc479-118">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="fc479-118">**Project Management**</span></span>

<span data-ttu-id="fc479-119">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="fc479-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="fc479-120">Korrigerade skillnader i avrundning och valutakurser resulterar i felaktiga planerade kostnader i rutnätet för projektspårning.</span><span class="sxs-lookup"><span data-stu-id="fc479-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="fc479-121">Stödja möjligheten att visa två eller flera reagera rutnät i formuläret **projekt**.</span><span class="sxs-lookup"><span data-stu-id="fc479-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="fc479-122">Med den här valideringen kan du adressera möjligheten att tilldela en uppgift förbi kalenderns slutdatum, vilket resulterar i en misslyckad resurstilldelning.</span><span class="sxs-lookup"><span data-stu-id="fc479-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="fc479-123">Förbättrad felhantering i adress nollreferens undantag genererat från följande:</span><span class="sxs-lookup"><span data-stu-id="fc479-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="fc479-124">**PreValidateProjectTeamMemberCreate** plugin</span><span class="sxs-lookup"><span data-stu-id="fc479-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="fc479-125">**PreValidateProjectTaskCreate** när en projektuppgift skapas utan ett associerat projekt</span><span class="sxs-lookup"><span data-stu-id="fc479-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="fc479-126">**PreProjectTeamMemberCreate** plugin</span><span class="sxs-lookup"><span data-stu-id="fc479-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="fc479-127">**PostProjectTeamMemberDelete** plugin</span><span class="sxs-lookup"><span data-stu-id="fc479-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="fc479-128">**PreValidateProjectTaskDelete** plugin</span><span class="sxs-lookup"><span data-stu-id="fc479-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="fc479-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="fc479-129">**Sales**</span></span>

<span data-ttu-id="fc479-130">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="fc479-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="fc479-131">Förbättrad felhantering för att adressera nollreferens undantag som genererats från **Kopiera projekt: uppskattning av HelperResource-hantering**.</span><span class="sxs-lookup"><span data-stu-id="fc479-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="fc479-132">**Inte redo att fakturera** på en **Eftersläpning av tids- och materialfakturering** rensar inte faktureringsstatus.</span><span class="sxs-lookup"><span data-stu-id="fc479-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="fc479-133">Korrigerade felmärkta knappar **Priser** i **Rollpris** och **Katalogobjekt**.</span><span class="sxs-lookup"><span data-stu-id="fc479-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
