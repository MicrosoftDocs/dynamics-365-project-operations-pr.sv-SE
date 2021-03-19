---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 23, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 379379ff643baa10417333b4be5e56d56eb5bc26
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280555"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="a1958-103">Project Service Automation uppdateringsversion 23, V3</span><span class="sxs-lookup"><span data-stu-id="a1958-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a1958-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a1958-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a1958-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="a1958-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a1958-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a1958-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a1958-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="a1958-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a1958-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a1958-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a1958-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 23.</span><span class="sxs-lookup"><span data-stu-id="a1958-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="a1958-110">Den här versionen har versionsnummer V 3.10.34.30 och är allmänt tillgänglig via en självuppdatering i augusti 2020.</span><span class="sxs-lookup"><span data-stu-id="a1958-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="a1958-111">Uppdatering version 23</span><span class="sxs-lookup"><span data-stu-id="a1958-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a1958-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="a1958-112">Bug fixes</span></span>

<span data-ttu-id="a1958-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="a1958-113">**Time and Expense**</span></span>

<span data-ttu-id="a1958-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="a1958-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="a1958-115">Hantera edge-ärende i **ta bort projektteammedlem** om du vill ge ett meningsfullt undantag.</span><span class="sxs-lookup"><span data-stu-id="a1958-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="a1958-116">Tilldelningsimporten resulterar i en tom borttagningssida.</span><span class="sxs-lookup"><span data-stu-id="a1958-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="a1958-117">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="a1958-117">**Resource Management**</span></span>

<span data-ttu-id="a1958-118">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="a1958-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a1958-119">**Resurskortet för rutnät för resursutnyttjande** visar felaktiga data när tidsskalan är längre än fem dagar.</span><span class="sxs-lookup"><span data-stu-id="a1958-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="a1958-120">När en kund skapar en bokningsbar resurs misslyckas plugin-programmet att automatiskt lägga till resursen i en Microsoft Office 365-grupp.</span><span class="sxs-lookup"><span data-stu-id="a1958-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="a1958-121">Vyn **avstämning** visar manuella guidade fel i vyerna **Vecka** eller **Månad**.</span><span class="sxs-lookup"><span data-stu-id="a1958-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="a1958-122">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="a1958-122">**Project Management**</span></span>

<span data-ttu-id="a1958-123">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="a1958-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="a1958-124">Ett alltför stort antal entiteter för **RetrieveMultiple för usersettings** orsakar försämrad prestanda för projektgodkännanden och andra operationer.</span><span class="sxs-lookup"><span data-stu-id="a1958-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="a1958-125">Rutnätet **Uppgiftsplanering** är begränsad till att endast visa upp till fem teammedlemmar från projektteamet.</span><span class="sxs-lookup"><span data-stu-id="a1958-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="a1958-126">Rutnätet **Uppgiftsplanering** resursuppslag filtrerar inte inaktiva resurser.</span><span class="sxs-lookup"><span data-stu-id="a1958-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="a1958-127">Manuellt läge fungerar inte som förväntat i uppdelad arbetsstruktur för projektplanering.</span><span class="sxs-lookup"><span data-stu-id="a1958-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="a1958-128">Rutnätet **Uppgiftsplanering** visar **Inaktiva transaktionskategorier**.</span><span class="sxs-lookup"><span data-stu-id="a1958-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="a1958-129">Rutnätet **resurstilldelningar** avrundar fel när en uppgift har flera tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="a1958-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="a1958-130">Avrundningsvärden skiljer sig mellan den planerade kostnaden och den faktiska kostnaden för en enskild aktivitet.</span><span class="sxs-lookup"><span data-stu-id="a1958-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="a1958-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a1958-131">**Sales**</span></span>

<span data-ttu-id="a1958-132">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="a1958-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a1958-133">**Hämta alla transaktionskategorier** dubbelklicka på skapar flera rader.</span><span class="sxs-lookup"><span data-stu-id="a1958-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]