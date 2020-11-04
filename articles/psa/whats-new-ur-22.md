---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 22, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085488"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="84798-103">Project Service Automation uppdateringsversion 22, V3</span><span class="sxs-lookup"><span data-stu-id="84798-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="84798-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="84798-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="84798-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="84798-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="84798-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="84798-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="84798-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="84798-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="84798-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="84798-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="84798-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 22.</span><span class="sxs-lookup"><span data-stu-id="84798-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="84798-110">Den här versionen har ett versionsnummer på V 3.10.33.48 och är allmänt tillgänglig via en självuppdatering i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="84798-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="84798-111">Uppdatering version 22</span><span class="sxs-lookup"><span data-stu-id="84798-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="84798-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="84798-112">Bug fixes</span></span>



<span data-ttu-id="84798-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="84798-113">**Time and Expense**</span></span>

<span data-ttu-id="84798-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="84798-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="84798-115">**Tidsposter** läggs inte till automatiskt i tidspostschemat efter import.</span><span class="sxs-lookup"><span data-stu-id="84798-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="84798-116">Rutnätet för datumväljaren **Tidspost** känner inte igen en användares nationella inställningar.</span><span class="sxs-lookup"><span data-stu-id="84798-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="84798-117">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="84798-117">**Resource Management**</span></span>

<span data-ttu-id="84798-118">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="84798-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="84798-119">I manuellt läge identifieras inte ändringar i profiler för **resurstilldelningar** när de genererar **resurskrav**.</span><span class="sxs-lookup"><span data-stu-id="84798-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="84798-120">**Resursförfrågningar** stöder inte status för anpassade begäranden.</span><span class="sxs-lookup"><span data-stu-id="84798-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="84798-121">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="84798-121">**Project Management**</span></span>

<span data-ttu-id="84798-122">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="84798-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="84798-123">Om du använder dubbel klickning på EstimateGridControl tolkas inte holländska formatnummer korrekt.</span><span class="sxs-lookup"><span data-stu-id="84798-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="84798-124">Tilldelade timmar uppdateras inte korrekt när tilldelningar ändras med hjälp av Microsoft Project-tillägget för klient på stationär dator.</span><span class="sxs-lookup"><span data-stu-id="84798-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="84798-125">Rutnät för projektuppföljning och uppskattning visar fel försäljningsvalutakod när kontraktsvalutan är annorlunda än kundvalutan och organisationen är konfigurerad att visa valutakoder i stället för valutasymboler.</span><span class="sxs-lookup"><span data-stu-id="84798-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="84798-126">En teammedlems slutdatum lägger till en dag om arbetskalenderns schema är 24 timmar per dag.</span><span class="sxs-lookup"><span data-stu-id="84798-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="84798-127">Om du lägger till en transaktionskategori i en aktivitet i projektschemat utlöses inte spara automatiskt.</span><span class="sxs-lookup"><span data-stu-id="84798-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="84798-128">Följande fel visas när du lägger till en teammedlem i projektmallen: "resurskrav kan inte associeras med projektmallar".</span><span class="sxs-lookup"><span data-stu-id="84798-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="84798-129">Regelskript för menyfliksområdet "msdyn. Approval. CanApproveOrReject" visar timeout-fel.</span><span class="sxs-lookup"><span data-stu-id="84798-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="84798-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="84798-130">**Sales**</span></span>

<span data-ttu-id="84798-131">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="84798-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="84798-132">Meddelande om valideringsfel visas inte när en kostnadsprislista väljs i prislistesökning i formulär/entitet "Ny prislista för offertprojekt".</span><span class="sxs-lookup"><span data-stu-id="84798-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="84798-133">När du stänger offerten som vunnen navigerar den inte till det skapade kontraktet om en BPF som är kopplad till offerten är den sista fasen.</span><span class="sxs-lookup"><span data-stu-id="84798-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="84798-134">Återföring av **Fakturerad försäljning** är länkat till den ursprungliga kostnaden när en tidspost återkallas.</span><span class="sxs-lookup"><span data-stu-id="84798-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="84798-135">När du väljer knappen **Bekräfta** ändras inte faktura statusen till **Bekräftad** om inte fakturan uppdateras.</span><span class="sxs-lookup"><span data-stu-id="84798-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
