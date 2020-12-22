---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 26, version 3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643285"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="34ec9-102">Project Service Automation uppdateringsversion 26, V3</span><span class="sxs-lookup"><span data-stu-id="34ec9-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="34ec9-103">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="34ec9-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="34ec9-104">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="34ec9-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="34ec9-105">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="34ec9-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="34ec9-106">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="34ec9-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="34ec9-107">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="34ec9-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="34ec9-108">I det här ämnet finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation, uppdateringsversion 26, version 3.</span><span class="sxs-lookup"><span data-stu-id="34ec9-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="34ec9-109">Denna version har versionsnummer V3.10.44.59 och är allmänt tillgänglig via en självuppdatering i december 2020.</span><span class="sxs-lookup"><span data-stu-id="34ec9-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="34ec9-110">Uppdatering version 26</span><span class="sxs-lookup"><span data-stu-id="34ec9-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="34ec9-111">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="34ec9-111">Bug fixes</span></span>

<span data-ttu-id="34ec9-112">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="34ec9-112">**Time and Expense**</span></span>

<span data-ttu-id="34ec9-113">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="34ec9-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="34ec9-114">Användare har möjlighet att ändra uppgiften på en tidspost som har godkänts/skickats.</span><span class="sxs-lookup"><span data-stu-id="34ec9-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="34ec9-115">"Object Reference Not Set"-fel när du sparar tidspost.</span><span class="sxs-lookup"><span data-stu-id="34ec9-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="34ec9-116">Tidspostimport från resurstilldelningar skapar tidsposter med de felaktiga DateTime-värdena.</span><span class="sxs-lookup"><span data-stu-id="34ec9-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="34ec9-117">När Project Service Automation och Field Service-appen båda är installerade visas knappen **Nytt** två gånger i kommandofältet för tidsposter i Field Service-appen.</span><span class="sxs-lookup"><span data-stu-id="34ec9-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="34ec9-118">Celluppdateringarna **Tillåt enhet** och **Enhetsgrupp** fungerar nu för rutnätet **Utgiftsuppskattningar**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="34ec9-119">Formuläret **Uppdatera tidspost** innehåller **Tidslinje**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="34ec9-120">Tidsgodkännande för icke-projekttidsposter blockerar systemet vid sökning efter en godkännar-roll för projektet.</span><span class="sxs-lookup"><span data-stu-id="34ec9-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="34ec9-121">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="34ec9-121">**Resource Management**</span></span>

<span data-ttu-id="34ec9-122">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="34ec9-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="34ec9-123">Lade till validering i plugin-programmet **PostProjectCreate** för att kontrollera om det finns ett primärt krav innan ett sådant skapas.</span><span class="sxs-lookup"><span data-stu-id="34ec9-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="34ec9-124">Snabbformuläret **Medlem i projektteam** avger ett nollreferensundantag om fält tas bort från formuläret.</span><span class="sxs-lookup"><span data-stu-id="34ec9-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="34ec9-125">Genererande av krav för 12 timmar över 1 år kommer att misslyckas.</span><span class="sxs-lookup"><span data-stu-id="34ec9-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="34ec9-126">Förbättrat nollreferensundantag för felmeddelande vid skapande av resurskrav.</span><span class="sxs-lookup"><span data-stu-id="34ec9-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="34ec9-127">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="34ec9-127">**Project Management**</span></span>

<span data-ttu-id="34ec9-128">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="34ec9-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="34ec9-129">Förbättrad validering för att adressera nollreferensundantag som genereras i plugin-programmet **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="34ec9-130">Projekt som publiceras av det stationära Microsoft Project-tillägget tar bort ej tilldelade tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="34ec9-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="34ec9-131">Lade till ny validering när en uppgifts projektreferens är ogiltig på grund av nollreferensundantag i plugin-programmet **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="34ec9-132">Rutnätet gruppmedlem visar inte distinkta tilldelningar i gruppmedlemsposten.</span><span class="sxs-lookup"><span data-stu-id="34ec9-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="34ec9-133">Lade till nya verifierings- och felmeddelanden på grund av nollreferensundantag i plugin-programmet **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="34ec9-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="34ec9-134">**Sales**</span></span>

<span data-ttu-id="34ec9-135">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="34ec9-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="34ec9-136">Vid val av en projektbaserad rad inom en offert eller ett kontrakt ska knappen **Förslag** endast vara synlig när du väljer en produktbaserad rad som är kopplad till en befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="34ec9-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="34ec9-137">Spearera privilegiet **Skapa_produkt** från privilegiet **Skapa_projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="34ec9-138">Om du tar bort en fakturarad orsakas ett nollreferensfel i **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="34ec9-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
