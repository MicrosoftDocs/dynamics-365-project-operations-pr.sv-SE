---
title: Nyheter i Project Service Automation uppdatering version 12, v3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756216"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="0c64f-103">Project Service Automation V3, uppdatering version 12</span><span class="sxs-lookup"><span data-stu-id="0c64f-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="0c64f-104">Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="0c64f-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0c64f-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="0c64f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0c64f-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0c64f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0c64f-107">Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="0c64f-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0c64f-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0c64f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0c64f-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 12.</span><span class="sxs-lookup"><span data-stu-id="0c64f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="0c64f-110">Den här versionen har ett versionsnummer på V3.10.2.34 och är allmänt tillgänglig via en självuppdatering i oktober 2019.</span><span class="sxs-lookup"><span data-stu-id="0c64f-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="0c64f-111">Uppdatering version 12</span><span class="sxs-lookup"><span data-stu-id="0c64f-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0c64f-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="0c64f-112">Bug fixes</span></span>

- <span data-ttu-id="0c64f-113">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="0c64f-113">Time and Expense</span></span>

    - <span data-ttu-id="0c64f-114">Fast: meddelande om tidsinmatningsfel har uppdaterats med en mer relevant kontext.</span><span class="sxs-lookup"><span data-stu-id="0c64f-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="0c64f-115">Fast: rutnätet för tidsinmatning och schema visar den lodräta rullningslisten på rätt sätt vid behov.</span><span class="sxs-lookup"><span data-stu-id="0c64f-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="0c64f-116">Fast: Skickade kostnads- och tidsposter kan godkännas.</span><span class="sxs-lookup"><span data-stu-id="0c64f-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="0c64f-117">Fast: dialogrutan för bekräftelse av annullering av godkännande har korrigerats för att återspegla statusen för godkännandet när det ändrades från **godkänd** till **skickad**.</span><span class="sxs-lookup"><span data-stu-id="0c64f-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="0c64f-118">Fast: **pris**, **enhet** och **antal** är nu låsta i utgiftsposten efter att den har godkänts.</span><span class="sxs-lookup"><span data-stu-id="0c64f-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="0c64f-119">Projektledning</span><span class="sxs-lookup"><span data-stu-id="0c64f-119">Project Management</span></span>

    - <span data-ttu-id="0c64f-120">Fast: **ny** åtgärd i huvudformuläret **teammedlem** har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="0c64f-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="0c64f-121">Fast: resurstilldelningar har uppdaterats till att utgöra ett felaktigt avrundningsfel som leder till en ändring i uppgiftens slutdatum.</span><span class="sxs-lookup"><span data-stu-id="0c64f-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="0c64f-122">Fast: relevanta serverfel visas i aktivitetsrutnätet för användaren.</span><span class="sxs-lookup"><span data-stu-id="0c64f-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="0c64f-123">Fast: namnet på teammedlemmen återges nu i väljaren för aktivitetens personväljare i stället för befattningens namn.</span><span class="sxs-lookup"><span data-stu-id="0c64f-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="0c64f-124">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="0c64f-124">Resource Management</span></span>

    - <span data-ttu-id="0c64f-125">Fast: information om resurskrav för projekt som skapats från en mall använder nu projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="0c64f-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="0c64f-126">Fast: nu förvalda kunskaper och kompetenser från rollhuvuddata till resurskravet som skapats för rollen.</span><span class="sxs-lookup"><span data-stu-id="0c64f-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="0c64f-127">Sales</span><span class="sxs-lookup"><span data-stu-id="0c64f-127">Sales</span></span>

    - <span data-ttu-id="0c64f-128">Fast: dubbletter av objekt-ID hittas i huvudformuläret **Kontrakt**.</span><span class="sxs-lookup"><span data-stu-id="0c64f-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="0c64f-129">Fast: logiken har uppdaterats för att fliken **Offertanalys** ska visas så att flikens metadata visas.</span><span class="sxs-lookup"><span data-stu-id="0c64f-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="0c64f-130">Fast: bokföringsdatumet på den faktiska posten kommer nu från datumet då datum för tid/utgiftspost skapades, inte datumet för godkännandet.</span><span class="sxs-lookup"><span data-stu-id="0c64f-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
