---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 17.5, snabbkorrigering, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 17.5, version 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085495"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="1932c-103">Project Service Automation uppdateringsversion 17.5, V3</span><span class="sxs-lookup"><span data-stu-id="1932c-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="1932c-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1932c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1932c-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="1932c-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="1932c-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1932c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1932c-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="1932c-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="1932c-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1932c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1932c-109">I detta ämne anges de funktioner och snabbkorrigeringar som är nya eller som har ändrats för, version 3, uppdateringsversion 17.5.</span><span class="sxs-lookup"><span data-stu-id="1932c-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="1932c-110">Den här versionen har versionsnummer på, version 3.10.7.32 och är allmänt tillgänglig via en självuppdatering i mars 2020.</span><span class="sxs-lookup"><span data-stu-id="1932c-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="1932c-111">Uppdatering version 17.5</span><span class="sxs-lookup"><span data-stu-id="1932c-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1932c-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="1932c-112">Bug fixes</span></span>


<span data-ttu-id="1932c-113">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="1932c-113">**Project Management**</span></span>

- <span data-ttu-id="1932c-114">Åtgärdat: synkroniseringsproblem på serversidan som inträffar tillsammans med aktiviteter med lång varaktighet.</span><span class="sxs-lookup"><span data-stu-id="1932c-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="1932c-115">Åtgärdat: Dygnet runt-arbetstidsmallar som felaktigt lägger till ytterligare en dag i aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="1932c-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="1932c-116">Åtgärdat: Arbetstidsmallar för 13 GMT som felaktigt byter uppgift en dag i förväg.</span><span class="sxs-lookup"><span data-stu-id="1932c-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

