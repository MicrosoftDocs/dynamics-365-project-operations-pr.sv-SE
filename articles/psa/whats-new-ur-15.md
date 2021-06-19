---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 15, version 3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 86aadca637939120d0ccd839e7c425e9e8d38aec
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006848"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="2b26b-103">Project Service Automation uppdateringsversion 15, V3</span><span class="sxs-lookup"><span data-stu-id="2b26b-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2b26b-104">Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="2b26b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="2b26b-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="2b26b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2b26b-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2b26b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2b26b-107">Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="2b26b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="2b26b-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2b26b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2b26b-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 15.</span><span class="sxs-lookup"><span data-stu-id="2b26b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="2b26b-110">Den här versionen har ett versionsnummer på V-3.10.5.28 och är allmänt tillgänglig via en självuppdatering i januari 2020.</span><span class="sxs-lookup"><span data-stu-id="2b26b-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="2b26b-111">Uppdatering version 15</span><span class="sxs-lookup"><span data-stu-id="2b26b-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="2b26b-112">Förbättringar</span><span class="sxs-lookup"><span data-stu-id="2b26b-112">Enhancements</span></span>

- <span data-ttu-id="2b26b-113">Projektledning</span><span class="sxs-lookup"><span data-stu-id="2b26b-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2b26b-114">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="2b26b-114">Bug fixes</span></span>

- <span data-ttu-id="2b26b-115">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="2b26b-115">Time and Expense</span></span>

  - <span data-ttu-id="2b26b-116">Fast: Lägg till felhantering vid laddning i vyn avstämning.</span><span class="sxs-lookup"><span data-stu-id="2b26b-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="2b26b-117">Fast: projektresursnav: Byt namn **Belopp** för att minska tvetydighet.</span><span class="sxs-lookup"><span data-stu-id="2b26b-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="2b26b-118">Fast: justera vyn **Kopiera kolumner för tidspost** så att de inkluderar typen.</span><span class="sxs-lookup"><span data-stu-id="2b26b-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="2b26b-119">Fast: när du redigerar tid i rutnätsvy med decimaltal uppstår ett okänt fel för vissa tal.</span><span class="sxs-lookup"><span data-stu-id="2b26b-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="2b26b-120">Projektledning</span><span class="sxs-lookup"><span data-stu-id="2b26b-120">Project Management</span></span>

  - <span data-ttu-id="2b26b-121">Fast: den nedrullningsbara menyn för **används i spårningsvy** expanderas nu baserat på alternativets bredd.</span><span class="sxs-lookup"><span data-stu-id="2b26b-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="2b26b-122">Fast: när du hanterar projekt i + 13 tidszon kan du visa felaktiga resultat i aktivitetsberäkningar.</span><span class="sxs-lookup"><span data-stu-id="2b26b-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="2b26b-123">Fast: **Sluttid för teammedlem** har inte korrigerats när 24-timmarsformat används.</span><span class="sxs-lookup"><span data-stu-id="2b26b-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="2b26b-124">Fast: återaktiverade **BPF** i huvudformuläret **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="2b26b-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="2b26b-125">Fast: beräkningen av tilldelningar ignorerar inte längre en dag.</span><span class="sxs-lookup"><span data-stu-id="2b26b-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="2b26b-126">Fast: ett nytt meddelandebanderoll har lagts till i projektformuläret när tidszonen skiljer sig mellan användare och projekt.</span><span class="sxs-lookup"><span data-stu-id="2b26b-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="2b26b-127">Sales</span><span class="sxs-lookup"><span data-stu-id="2b26b-127">Sales</span></span>

  - <span data-ttu-id="2b26b-128">Fast: sökning efter utgiftskategori för utgiftsbedömning kan användas för att filtrera dubbletter.</span><span class="sxs-lookup"><span data-stu-id="2b26b-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="2b26b-129">Fast: kod i **PluginDomain.ExecuteInTryCatchBlock(..)** döljer inte längre undantagets ursprung.</span><span class="sxs-lookup"><span data-stu-id="2b26b-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="2b26b-130">Fast: får inte längre ett felmeddelande i **projektsökning** i formuläret **offertrad** när det finns fler än 1000 projekt.</span><span class="sxs-lookup"><span data-stu-id="2b26b-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="2b26b-131">Fast: **uppskattning** rutnät för arbetsuppskattningar och utgiftsuppskattningar visar nu rätt valutasymbol.</span><span class="sxs-lookup"><span data-stu-id="2b26b-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="2b26b-132">Fast: när en organisation uppdaterar PSA från uppdatering version 14 till uppdatering version 15 visas inte längre fliken **schema** som tom i formuläret **projekt**.</span><span class="sxs-lookup"><span data-stu-id="2b26b-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]