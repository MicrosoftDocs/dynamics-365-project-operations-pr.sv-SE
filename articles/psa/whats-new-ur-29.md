---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 29, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010493"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="61573-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 29, version 3</span><span class="sxs-lookup"><span data-stu-id="61573-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="61573-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="61573-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="61573-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="61573-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="61573-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="61573-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="61573-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="61573-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="61573-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="61573-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="61573-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 29.</span><span class="sxs-lookup"><span data-stu-id="61573-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="61573-110">Denna version har versionsnummer V3.10.47.7 och är allmänt tillgänglig via en självuppdatering i februari 2021.</span><span class="sxs-lookup"><span data-stu-id="61573-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="61573-111">Uppdatering version 29</span><span class="sxs-lookup"><span data-stu-id="61573-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="61573-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="61573-112">Bug fixes</span></span>

<span data-ttu-id="61573-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="61573-113">**Time and Expense**</span></span>

<span data-ttu-id="61573-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="61573-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="61573-115">Användare kan inte se arbetstimmar som är inloggade på icke-arbetsdagar i tidsinmatningsrutnätet.</span><span class="sxs-lookup"><span data-stu-id="61573-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="61573-116">Godkända utgiftsposter kan redigeras i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="61573-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="61573-117">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="61573-117">**Project Management**</span></span>

<span data-ttu-id="61573-118">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="61573-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="61573-119">Valideringslogik saknas för att säkerställa att arbetstimmarna för resurstilldelning inte kan vara negativa.</span><span class="sxs-lookup"><span data-stu-id="61573-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="61573-120">Den anpassade åtgärden **AssignResourcesForTask** uppdaterar alla fält i stället för att endast ändrade fält.</span><span class="sxs-lookup"><span data-stu-id="61573-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="61573-121">När du kopierar ett projekt i en miljö med plugin-program eller arbetsflöden som är registrerade på händelsen **CreateProject** uppdateras inte attributet **msdyn_bulkgenerationstatus** om **CopyWBSToProject** misslyckas.</span><span class="sxs-lookup"><span data-stu-id="61573-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="61573-122">När du expanderar projektkalendern sorteras inte arbetsdagarna i stigande ordning vilket gör att vissa uppdateringar av projektuppgiften misslyckas.</span><span class="sxs-lookup"><span data-stu-id="61573-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="61573-123">Om du ändrar projektledaren för ett befintligt projekt utlöses standardlogiken för organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="61573-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="61573-124">**Försäljning**</span><span class="sxs-lookup"><span data-stu-id="61573-124">**Sales**</span></span>

<span data-ttu-id="61573-125">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="61573-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="61573-126">Fliken **Kontraktresultat** på sidan **Kontrakt** misslyckas i bakgrunden under initiering när inga kontraktrader finns.</span><span class="sxs-lookup"><span data-stu-id="61573-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>