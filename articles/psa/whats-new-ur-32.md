---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 32, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129688"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="57555-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 32, version 3</span><span class="sxs-lookup"><span data-stu-id="57555-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="57555-104">Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen.</span><span class="sxs-lookup"><span data-stu-id="57555-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="57555-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="57555-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="57555-106">Den är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="57555-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="57555-107">Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="57555-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="57555-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="57555-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="57555-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 32.</span><span class="sxs-lookup"><span data-stu-id="57555-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="57555-110">Den här versionen har versionsnummer V3.10.53.108 och är allmänt tillgänglig via en självuppdatering i juni 2021.</span><span class="sxs-lookup"><span data-stu-id="57555-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="57555-111">Uppdatering version 32</span><span class="sxs-lookup"><span data-stu-id="57555-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="57555-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="57555-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="57555-113">Allmänt</span><span class="sxs-lookup"><span data-stu-id="57555-113">General</span></span>

- <span data-ttu-id="57555-114">Om en större uppgradering misslyckas bör endast huvudprogrammets ingångspunkter blockeras för att se till att delade entiteter fortfarande är tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="57555-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="57555-115">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="57555-115">Time and Expense</span></span>

<span data-ttu-id="57555-116">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="57555-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="57555-117">**TimeEntriesImportFromResourceAssignment** upprätthåller inte start- och sluttiderna för resurstilldelningsutsnittet.</span><span class="sxs-lookup"><span data-stu-id="57555-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="57555-118">Om du väljer **Öppna post** i rutnätet **Tidspost** kan det hända att du inte kan välja andra formulär.</span><span class="sxs-lookup"><span data-stu-id="57555-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="57555-119">När du importerar tilldelningar till tidsposter kan klientkodsfrågan skapa en lång URL som misslyckas.</span><span class="sxs-lookup"><span data-stu-id="57555-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="57555-120">I rutnätet **Tidspost**, när ett värde har tagits bort från en cell, förblir inte fokus i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="57555-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="57555-121">Knappen **Avvisa** har tagits bort från vyn **Bearbetar godkännanden** för moderna godkännanden.</span><span class="sxs-lookup"><span data-stu-id="57555-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="57555-122">Stabilitet och prestanda för godkännande av tidsposter i bulk påverkas av deadlock och ett fel i att korrekt hantera anpassningar som är relaterade till entiteten **Tidspost**.</span><span class="sxs-lookup"><span data-stu-id="57555-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="57555-123">Projektplanering</span><span class="sxs-lookup"><span data-stu-id="57555-123">Project Planning</span></span>

- <span data-ttu-id="57555-124">Ett null-referensundantag skapas när du uppdaterar ett projekt som har ett null-värde i fältet **Upphandlande enhet**.</span><span class="sxs-lookup"><span data-stu-id="57555-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="57555-125">**Uppdatera projektsummor** beräknar felaktigt den återstående kostnaden och återstående försäljning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="57555-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="57555-126">Överflödiga prisberäkningar påverkar prestanda för uppdateringar av resurstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="57555-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="57555-127">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="57555-127">Resource Management</span></span>

<span data-ttu-id="57555-128">Följande problem har korrigerats:</span><span class="sxs-lookup"><span data-stu-id="57555-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="57555-129">När en bokningsbar resurs kalenderkapacitet är fler än 1 identifierar Project Service Automation felaktigt kapaciteten som 0 (noll).</span><span class="sxs-lookup"><span data-stu-id="57555-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="57555-130">Därför uppstår en oändlig loop i schemavyn.</span><span class="sxs-lookup"><span data-stu-id="57555-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="57555-131">Försäljning</span><span class="sxs-lookup"><span data-stu-id="57555-131">Sales</span></span>

<span data-ttu-id="57555-132">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="57555-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="57555-133">När en journalrad skapas som har en anpassad transaktionstyp sker följande nullreferensundantag: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="57555-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="57555-134">Roller och kategorier som inaktiveras innan en offert kopieras ska inte läggas till i debiterbara roller och kategorier för den nyligen kopierade offerten.</span><span class="sxs-lookup"><span data-stu-id="57555-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="57555-135">Dokumentdatum och redovisningsdatum justeras inte mot startdatumet som anges på en fakturaradsdetalj som skapas direkt på en utkastfaktura.</span><span class="sxs-lookup"><span data-stu-id="57555-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="57555-136">Null-referensundantag skapas i scenarier som är relaterade till inaktivering av roller och kategorier innan en offert kopieras.</span><span class="sxs-lookup"><span data-stu-id="57555-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="57555-137">Åtgärden **Uppdatera priser** på sidan **Projekt** uppdaterar inte utgiftsberäkningar och materialberäkningar.</span><span class="sxs-lookup"><span data-stu-id="57555-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
