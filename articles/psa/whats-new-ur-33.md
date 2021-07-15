---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 33, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334608"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="16f89-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 33, version 3</span><span class="sxs-lookup"><span data-stu-id="16f89-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="16f89-104">Vi är glada att kunna presentera den senaste uppdateringen för Microsoft Dynamics 365 Project Service Automation-appen.</span><span class="sxs-lookup"><span data-stu-id="16f89-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="16f89-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="16f89-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="16f89-106">Den är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="16f89-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="16f89-107">Om du vill uppdatera till den här versionen går du till sidan Admin Center för Dynamics 365 Online Solutions och installerar uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="16f89-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="16f89-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="16f89-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="16f89-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 33.</span><span class="sxs-lookup"><span data-stu-id="16f89-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="16f89-110">Den här versionen har ett versionsnummer för V3.10.54.98 och är allmänt tillgänglig via en självuppdatering i juli 2021.</span><span class="sxs-lookup"><span data-stu-id="16f89-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="16f89-111">Uppdatering version 33</span><span class="sxs-lookup"><span data-stu-id="16f89-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="16f89-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="16f89-112">Bug fixes</span></span>

<span data-ttu-id="16f89-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="16f89-113">**Time and Expense**</span></span>

<span data-ttu-id="16f89-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="16f89-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="16f89-115">Två låsta fält, **msdyn_description** och **msdyn_externaldescription** redigerbara efter att de har skickas in.</span><span class="sxs-lookup"><span data-stu-id="16f89-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="16f89-116">Ett felmeddelande visas om en kostnad skapas som inte är relaterad till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="16f89-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="16f89-117">När en tidspost skapas blir resursrollen en inaktiv roll som standard.</span><span class="sxs-lookup"><span data-stu-id="16f89-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="16f89-118">Rader som hör till en förterad och borttagna utgifter tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="16f89-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="16f89-119">I **Snabbregistreringsformulär för tidspost**, uppdatera vyn **Projektuppgiftslista** för att ändra datumet som visas som standard till uppgiftens startdatum.</span><span class="sxs-lookup"><span data-stu-id="16f89-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="16f89-120">När du skapar en tidspost från fliken **Relaterade** för den bokningsbara resursen, skapas tidsposten felaktigt för den inloggade användaren i stället för den överordnat bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="16f89-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="16f89-121">Nya fält läggs till i dialogrutan **MDD för massgodkännande**.</span><span class="sxs-lookup"><span data-stu-id="16f89-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="16f89-122">**Projektplanering**</span><span class="sxs-lookup"><span data-stu-id="16f89-122">**Project planning**</span></span>

<span data-ttu-id="16f89-123">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="16f89-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="16f89-124">Gör projektgenereringen långsammare när mallar för projektarbete i timmen tillämpas med komplexa kalendrar.</span><span class="sxs-lookup"><span data-stu-id="16f89-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="16f89-125">När startdatum är större än slutdatumet visas ett fel i projektmallen för kopian på grund av skillnader i tidskomponenten för varje fält.</span><span class="sxs-lookup"><span data-stu-id="16f89-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="16f89-126">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="16f89-126">**Resource management**</span></span>

<span data-ttu-id="16f89-127">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="16f89-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="16f89-128">En felaktig parameter används i resursutnyttjandefrågan och XML-leadsen leder till felaktiga filterresultat i rutnätet **resursutnyttjande**.</span><span class="sxs-lookup"><span data-stu-id="16f89-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="16f89-129">Bekräftelsen **Utöka bokningar** visar felaktigt slutdatum för bokningar.</span><span class="sxs-lookup"><span data-stu-id="16f89-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="16f89-130">**Försäljning**</span><span class="sxs-lookup"><span data-stu-id="16f89-130">**Sales**</span></span>

<span data-ttu-id="16f89-131">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="16f89-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="16f89-132">Ett felmeddelande visas om ett kategoripris skapas med värden som saknas.</span><span class="sxs-lookup"><span data-stu-id="16f89-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="16f89-133">Ett felmeddelande visas om en kontraktradsmilstolpar skapas utan en orderrad.</span><span class="sxs-lookup"><span data-stu-id="16f89-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
