---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 28, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280240"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="49db1-103">Nyheter och ändringar i Project Service Automation, uppdateringsversion 28, version 3</span><span class="sxs-lookup"><span data-stu-id="49db1-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="49db1-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="49db1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="49db1-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="49db1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="49db1-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="49db1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="49db1-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="49db1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="49db1-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="49db1-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="49db1-109">I det här ämnet anges de funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdateringsutgåva 28. Denna version har versionsnummer V3.10.46.32 och är i allmänhet tillgänglig genom en självuppdatering i januari 2021.</span><span class="sxs-lookup"><span data-stu-id="49db1-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="49db1-110">Uppdatering version 28</span><span class="sxs-lookup"><span data-stu-id="49db1-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="49db1-111">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="49db1-111">Bug fixes</span></span>

<span data-ttu-id="49db1-112">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="49db1-112">**Time and Expense**</span></span>

<span data-ttu-id="49db1-113">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="49db1-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="49db1-114">Användare kan använda **Massredigering** för att uppdatera tidsposter som har godkänts och skickats.</span><span class="sxs-lookup"><span data-stu-id="49db1-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="49db1-115">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="49db1-115">**Project Management**</span></span>

<span data-ttu-id="49db1-116">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="49db1-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="49db1-117">I de fall där uppgiftens GUID tolkas som ett tal, kan aktiviteter inte öppnas för redigering med **Redigera aktivitet** i menyfliksområdet på sidan **Uppdelad arbetsstruktur**.</span><span class="sxs-lookup"><span data-stu-id="49db1-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="49db1-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="49db1-118">**Sales**</span></span>

<span data-ttu-id="49db1-119">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="49db1-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="49db1-120">Ett null-referensundantag genereras när plugin-programmet **GetEstimatesForProject** åberopas.</span><span class="sxs-lookup"><span data-stu-id="49db1-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="49db1-121">**Markera redo att fakturera** i milstolprutnätet uppdaterar attribut endast delvis, med undantag för attributet **InvoiceStatus**, som uppdateras.</span><span class="sxs-lookup"><span data-stu-id="49db1-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]