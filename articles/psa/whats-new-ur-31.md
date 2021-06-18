---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 31, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999153"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="f4a4c-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 31, V3</span><span class="sxs-lookup"><span data-stu-id="f4a4c-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f4a4c-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f4a4c-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f4a4c-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f4a4c-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f4a4c-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f4a4c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f4a4c-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 31.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="f4a4c-110">Den här versionen har ett versionsnummer på V3.10.52.77 och är allmänt tillgänglig via en självuppdatering i maj 2021.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="f4a4c-111">Uppdatering version 31</span><span class="sxs-lookup"><span data-stu-id="f4a4c-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f4a4c-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="f4a4c-112">Bug fixes</span></span>

<span data-ttu-id="f4a4c-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="f4a4c-113">**Time and Expense**</span></span>

<span data-ttu-id="f4a4c-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f4a4c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f4a4c-115">Knapparna för tidsinmatningskontroll på sidan **Bokningsbar resurs** var förvirrande.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="f4a4c-116">Ett null-referensundantag skapades i **Project.SetTrackingFields** när en tidspost godkändes.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="f4a4c-117">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="f4a4c-117">**Resource Management**</span></span>

<span data-ttu-id="f4a4c-118">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f4a4c-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="f4a4c-119">**Skapa teammedlem** visar inte korrekt metadatainställning för bokning för **Standardstatus för bekräftad bokning**.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="f4a4c-120">Vid uppgradering från PSA 1.X till 3.X misslyckas uppgraderingsprocessen vid **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="f4a4c-121">**Försäljning**</span><span class="sxs-lookup"><span data-stu-id="f4a4c-121">**Sales**</span></span>

<span data-ttu-id="f4a4c-122">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f4a4c-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="f4a4c-123">Faktisk intäkt konverterar beloppen till projektvaluta i spårningsrutnätet.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="f4a4c-124">Standardvalutan skiljer sig när journalrader, offertrader och kontraktrader skapas i scenarier där företagets basvaluta skiljer sig från projektvalutan.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="f4a4c-125">Förfrågan **Väntar på validering av korrigeringsjournal** filtreras inte per projekt.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="f4a4c-126">Återstående försäljning beräknas felaktigt på ett projekt.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="f4a4c-127">Offerter baserade på en kontakt misslyckas när de skapas utan en prislista.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="f4a4c-128">Det visas inget bearbetningsfält när du väljer **Bekräfta faktura**.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="f4a4c-129">Det visas inget bearbetningsfält när du väljer **Skapa faktura**.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="f4a4c-130">Om du stänger en offert som förlorad annulleras inte bokningar.</span><span class="sxs-lookup"><span data-stu-id="f4a4c-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







