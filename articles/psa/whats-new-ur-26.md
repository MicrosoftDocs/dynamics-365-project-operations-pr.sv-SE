---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 26, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948846"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="5d3a9-103">Project Service Automation uppdateringsversion 26, V3</span><span class="sxs-lookup"><span data-stu-id="5d3a9-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5d3a9-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5d3a9-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5d3a9-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5d3a9-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5d3a9-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5d3a9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5d3a9-109">I det här ämnet finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation, uppdateringsversion 26, version 3.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="5d3a9-110">Denna version har versionsnummer V3.10.44.59 och är allmänt tillgänglig via en självuppdatering i december 2020.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="5d3a9-111">Uppdatering version 26</span><span class="sxs-lookup"><span data-stu-id="5d3a9-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5d3a9-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="5d3a9-112">Bug fixes</span></span>

<span data-ttu-id="5d3a9-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-113">**Time and Expense**</span></span>

<span data-ttu-id="5d3a9-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5d3a9-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="5d3a9-115">Användare har möjlighet att ändra uppgiften på en tidspost som har godkänts/skickats.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="5d3a9-116">"Object Reference Not Set"-fel när du sparar tidspost.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="5d3a9-117">Tidspostimport från resurstilldelningar skapar tidsposter med de felaktiga DateTime-värdena.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="5d3a9-118">När Project Service Automation och Field Service-appen båda är installerade visas knappen **Nytt** två gånger i kommandofältet för tidsposter i Field Service-appen.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="5d3a9-119">Celluppdateringarna **Tillåt enhet** och **Enhetsgrupp** fungerar nu för rutnätet **Utgiftsuppskattningar**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="5d3a9-120">Formuläret **Uppdatera tidspost** innehåller **Tidslinje**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="5d3a9-121">Tidsgodkännande för icke-projekttidsposter blockerar systemet vid sökning efter en godkännar-roll för projektet.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="5d3a9-122">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-122">**Resource Management**</span></span>

<span data-ttu-id="5d3a9-123">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5d3a9-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="5d3a9-124">Lade till validering i plugin-programmet **PostProjectCreate** för att kontrollera om det finns ett primärt krav innan ett sådant skapas.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="5d3a9-125">Snabbformuläret **Medlem i projektteam** avger ett nollreferensundantag om fält tas bort från formuläret.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="5d3a9-126">Genererande av krav för 12 timmar över 1 år kommer att misslyckas.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="5d3a9-127">Förbättrat nollreferensundantag för felmeddelande vid skapande av resurskrav.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="5d3a9-128">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-128">**Project Management**</span></span>

<span data-ttu-id="5d3a9-129">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5d3a9-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="5d3a9-130">Förbättrad validering för att adressera nollreferensundantag som genereras i plugin-programmet **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="5d3a9-131">Projekt som publiceras av det stationära Microsoft Project-tillägget tar bort ej tilldelade tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="5d3a9-132">Lade till ny validering när en uppgifts projektreferens är ogiltig på grund av nollreferensundantag i plugin-programmet **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="5d3a9-133">Rutnätet gruppmedlem visar inte distinkta tilldelningar i gruppmedlemsposten.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="5d3a9-134">Lade till nya verifierings- och felmeddelanden på grund av nollreferensundantag i plugin-programmet **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="5d3a9-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-135">**Sales**</span></span>

<span data-ttu-id="5d3a9-136">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5d3a9-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="5d3a9-137">Vid val av en projektbaserad rad inom en offert eller ett kontrakt ska knappen **Förslag** endast vara synlig när du väljer en produktbaserad rad som är kopplad till en befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="5d3a9-138">Spearera privilegiet **Skapa_produkt** från privilegiet **Skapa_projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="5d3a9-139">Om du tar bort en fakturarad orsakas ett nollreferensfel i **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]