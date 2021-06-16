---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 30, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852899"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="cce6c-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 30, version 3</span><span class="sxs-lookup"><span data-stu-id="cce6c-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cce6c-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cce6c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cce6c-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="cce6c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cce6c-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cce6c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cce6c-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="cce6c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cce6c-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cce6c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cce6c-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 30.</span><span class="sxs-lookup"><span data-stu-id="cce6c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="cce6c-110">Den här versionen har ett versionsnummer på V3.10.51.61 och är allmänt tillgänglig via en självuppdatering i april 2021.</span><span class="sxs-lookup"><span data-stu-id="cce6c-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="cce6c-111">Uppdatering version 30</span><span class="sxs-lookup"><span data-stu-id="cce6c-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cce6c-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="cce6c-112">Bug fixes</span></span>

<span data-ttu-id="cce6c-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="cce6c-113">**Time and Expense**</span></span>

<span data-ttu-id="cce6c-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="cce6c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cce6c-115">Ett fel uppstår när du skapar och sparar en tidspost på sidan **Snabb skapa** om fältet **Roll** tas bort.</span><span class="sxs-lookup"><span data-stu-id="cce6c-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="cce6c-116">Med filtret Tidspost används fel filteroperator.</span><span class="sxs-lookup"><span data-stu-id="cce6c-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="cce6c-117">Kopierade tidsscheman visas inte automatiskt när du väljer **Kopiera vecka** i tidsinmatningskontrollen.</span><span class="sxs-lookup"><span data-stu-id="cce6c-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="cce6c-118">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="cce6c-118">**Resource Management**</span></span>

<span data-ttu-id="cce6c-119">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="cce6c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="cce6c-120">När du utökar en bokning blir den bokningsstatus som tilldelats den svåra bokningsstatusen felaktig.</span><span class="sxs-lookup"><span data-stu-id="cce6c-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="cce6c-121">Om en bokning utökas gäller den bokningsstatus som har definierats som **Genomförd** i metadata för bokningskonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="cce6c-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="cce6c-122">När en giltig bokningsstatus inte anges lokaliseras inte felmeddelandet korrekt.</span><span class="sxs-lookup"><span data-stu-id="cce6c-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="cce6c-123">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="cce6c-123">**Project Management**</span></span>

<span data-ttu-id="cce6c-124">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="cce6c-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="cce6c-125">Projekt kan inte skapas i en valuta och omfattar relaterade uppgifter i en annan valuta.</span><span class="sxs-lookup"><span data-stu-id="cce6c-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="cce6c-126">**Försäljning**</span><span class="sxs-lookup"><span data-stu-id="cce6c-126">**Sales**</span></span>

<span data-ttu-id="cce6c-127">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="cce6c-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="cce6c-128">När en prislista kopieras uppdateras inte priserna.</span><span class="sxs-lookup"><span data-stu-id="cce6c-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="cce6c-129">Det går inte att stänga en offert som den har vunnit när kostnadsdetaljen har ett ursprungsvärde.</span><span class="sxs-lookup"><span data-stu-id="cce6c-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="cce6c-130">I entiteten **Projektuppgift**, **Beräknad kostnad** har bytt namn till **Planerad kostnad (bas)**.</span><span class="sxs-lookup"><span data-stu-id="cce6c-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="cce6c-131">Ett null-referensfel skapas när fakturor skapas eller tas bort.</span><span class="sxs-lookup"><span data-stu-id="cce6c-131">A null reference exception is generated when invoices are created or deleted.</span></span>