---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 14, version 3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 14 V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124840"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="156e1-103">Project Service Automation uppdateringsversion 14, V3</span><span class="sxs-lookup"><span data-stu-id="156e1-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="156e1-104">Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="156e1-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="156e1-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="156e1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="156e1-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="156e1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="156e1-107">Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="156e1-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="156e1-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="156e1-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="156e1-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 14.</span><span class="sxs-lookup"><span data-stu-id="156e1-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="156e1-110">Den här versionen har versionsnumret för V-3.10.4.21 och är tillgängligt enligt följande schema:</span><span class="sxs-lookup"><span data-stu-id="156e1-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="156e1-111">**Allmän tillgänglighet (självuppdatering):** 2020 januari</span><span class="sxs-lookup"><span data-stu-id="156e1-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="156e1-112">**Automatisk uppdatering:** 2020 februari</span><span class="sxs-lookup"><span data-stu-id="156e1-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="156e1-113">Uppdatering version 14</span><span class="sxs-lookup"><span data-stu-id="156e1-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="156e1-114">Förbättringar</span><span class="sxs-lookup"><span data-stu-id="156e1-114">Enhancements</span></span>

- <span data-ttu-id="156e1-115">Sales</span><span class="sxs-lookup"><span data-stu-id="156e1-115">Sales</span></span>

     - <span data-ttu-id="156e1-116">Anpassade fältvärden från **Information om offertrad** kopieras till **Projektkontraktradens detaljer** när en offert uppdateras till **stängd som vunnen**.</span><span class="sxs-lookup"><span data-stu-id="156e1-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="156e1-117">Bekräftade projekt kan **stängas som förlorade**.</span><span class="sxs-lookup"><span data-stu-id="156e1-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="156e1-118">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="156e1-118">Resource Management</span></span>

     - <span data-ttu-id="156e1-119">När du utökar bokningarna visas en dialogruta där du bekräftar bokningsresultat och skapar en länk för att underhålla bokningar.</span><span class="sxs-lookup"><span data-stu-id="156e1-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="156e1-120">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="156e1-120">Bug fixes</span></span>

- <span data-ttu-id="156e1-121">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="156e1-121">Time and Expense</span></span>

     - <span data-ttu-id="156e1-122">Fast: bättre användarupplevelse när användaren inte har valt några poster som ska rättas till.</span><span class="sxs-lookup"><span data-stu-id="156e1-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="156e1-123">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="156e1-123">Resource Management</span></span>

     - <span data-ttu-id="156e1-124">Fast: boka en resurs flera gånger flödar från namnet på den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="156e1-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="156e1-125">Sales</span><span class="sxs-lookup"><span data-stu-id="156e1-125">Sales</span></span>

     - <span data-ttu-id="156e1-126">Fast: det totala försäljningspriset beräknas inte förrän användaren även försummar en självkostnad för utgiftsuppskattningar i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="156e1-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="156e1-127">Fixat: Stängning av en offert som **vunnen** misslyckas om det associerade projektavtalet inte har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="156e1-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

