---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 16, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 16, version 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143655"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="44117-103">Project Service Automation uppdateringsversion 16, V3</span><span class="sxs-lookup"><span data-stu-id="44117-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="44117-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="44117-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="44117-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="44117-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="44117-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="44117-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="44117-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="44117-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="44117-108">Mer information finns i [Installera och uppdatera en prioriterad lösning](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="44117-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="44117-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 16.</span><span class="sxs-lookup"><span data-stu-id="44117-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="44117-110">Den här versionen har versionsnummer V3.10.6.34 och är allmänt tillgänglig via en självuppdatering i januari 2020.</span><span class="sxs-lookup"><span data-stu-id="44117-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="44117-111">Uppdatering version 16</span><span class="sxs-lookup"><span data-stu-id="44117-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="44117-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="44117-112">Bug fixes</span></span>

-   <span data-ttu-id="44117-113">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="44117-113">Time and Expense</span></span>

    -   <span data-ttu-id="44117-114">Åtgärdat: Användare som försöker skicka raderade tid- och utgiftsposter för godkännanden får nu relevanta felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="44117-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="44117-115">Projektledning</span><span class="sxs-lookup"><span data-stu-id="44117-115">Project Management</span></span>

    -   <span data-ttu-id="44117-116">Åtgärdat: De resursenheter som har definierats för teammedlemmar i mallar beaktas när mallarna tillämpas på ett nytt projekt.</span><span class="sxs-lookup"><span data-stu-id="44117-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="44117-117">Åtgärdat: Förbättrad hantering av omtilldelning av postägarskap.</span><span class="sxs-lookup"><span data-stu-id="44117-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="44117-118">Åtgärdat: Projekt som håller på att kopieras får inte kopieras förrän alla kopieringsåtgärder har slutförts.</span><span class="sxs-lookup"><span data-stu-id="44117-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="44117-119">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="44117-119">Resource Management</span></span>

    -   <span data-ttu-id="44117-120">Åtgärdat: Utökade bokningar hanterar nu korta varaktigheter korrekt och skapar inte längre noll timmar för utökade bokningar.</span><span class="sxs-lookup"><span data-stu-id="44117-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="44117-121">Åtgärdat: Vyn Avstämningen visas nu när projektets tidszon är + 5:30 GMT och användarens tidszon är annorlunda.</span><span class="sxs-lookup"><span data-stu-id="44117-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="44117-122">Sales</span><span class="sxs-lookup"><span data-stu-id="44117-122">Sales</span></span>

    -   <span data-ttu-id="44117-123">Åtgärdat: När ett projekt som har mappats till en kontraktrad tas bort och ett nytt projekt mappas, utvärderades inte de faktiska posterna i det nya projektet på nytt, detta grund val av de fakturerings- och prisregler som definierats på kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="44117-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="44117-124">Detta har åtgärdats i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="44117-124">This has been fixed in this release.</span></span> <span data-ttu-id="44117-125">Priser och faktiska poster för det nymappade projektet kommer att återföras och återskapas på rätt sätt utifrån pris och faktureringsregler för kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="44117-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="44117-126">Som en följd utvärderas ochså de faktiska posterna för det icke-mappade projektet på nytt.</span><span class="sxs-lookup"><span data-stu-id="44117-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="44117-127">Åtgärdat: Ytterligare validering har lagts till i fältet **Belopp** för en uppskattningsrad, detta för att se till att noll-värden inte sparas.</span><span class="sxs-lookup"><span data-stu-id="44117-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="44117-128">Åtgärdat: När faktiska värden har uppdaterats i ett projekt har en uppdateringsknapp lagts till i projektets huvudformulär så att användarna kan synkronisera de faktiska värdena på nytt.</span><span class="sxs-lookup"><span data-stu-id="44117-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="44117-129">åtgärdat: När användare uppgraderar från 2.X till 3. X tillåts projekt med ett NULL-värde för projektets namn.</span><span class="sxs-lookup"><span data-stu-id="44117-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

