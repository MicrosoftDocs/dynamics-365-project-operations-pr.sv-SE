---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 19, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126864"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="956be-103">Project Service Automation uppdateringsversion 19, V3</span><span class="sxs-lookup"><span data-stu-id="956be-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="956be-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="956be-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="956be-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="956be-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="956be-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="956be-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="956be-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="956be-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="956be-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="956be-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="956be-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 19.</span><span class="sxs-lookup"><span data-stu-id="956be-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="956be-110">Den här versionen har ett versionsnummer på V3.10.30.41 och är allmänt tillgänglig via en självuppdatering i maj 2020.</span><span class="sxs-lookup"><span data-stu-id="956be-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="956be-111">Uppdatering version 19</span><span class="sxs-lookup"><span data-stu-id="956be-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="956be-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="956be-112">Bug fixes</span></span>

<span data-ttu-id="956be-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="956be-113">**Time and Expense**</span></span>

<span data-ttu-id="956be-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="956be-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="956be-115">Fel som härletts från import av tidspost visas inte korrekt.</span><span class="sxs-lookup"><span data-stu-id="956be-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="956be-116">Tidspostrutnätet stöder inte fältfunktionen **Endast datum**.</span><span class="sxs-lookup"><span data-stu-id="956be-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="956be-117">Projektresurser kan inte skapa en utgift med ett projekt.</span><span class="sxs-lookup"><span data-stu-id="956be-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="956be-118">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="956be-118">**Project Management**</span></span>

<span data-ttu-id="956be-119">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="956be-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="956be-120">Nästa underordnade aktivitet orsakar en felaktig beräkning av insatser under slutförande (EAC).</span><span class="sxs-lookup"><span data-stu-id="956be-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="956be-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="956be-121">**Sales**</span></span>

<span data-ttu-id="956be-122">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="956be-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="956be-123">Åtgärden **Omberäkna** fungerar inte med information om utgiftskontraktrader eller information om offertrader.</span><span class="sxs-lookup"><span data-stu-id="956be-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="956be-124">**Uppdatera priser** saknas för utgiftsuppskattningar.</span><span class="sxs-lookup"><span data-stu-id="956be-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="956be-125">Kunder kan inte välja anpassade kontraktstatusorsaker från sidan **projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="956be-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="956be-126">Kunder försämrar prestanda när de skapar en anpassad prislista från en offert.</span><span class="sxs-lookup"><span data-stu-id="956be-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="956be-127">Kunder är inkonsekventa med standardinställningen **enhet** på sidorna **Information om offertrad** och **Kontraktradsinformation**.</span><span class="sxs-lookup"><span data-stu-id="956be-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="956be-128">Om du lägger till icke debiterbara transaktionskategoriartiklar på en debiterbar kontraktrad respekteras inte faktureringstypen **Icke debiterbar** för transaktionskategorin.</span><span class="sxs-lookup"><span data-stu-id="956be-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="956be-129">Kunder kan inte använda de nyligen tillagda rollerna och kategorierna i tidigare skapade kontrakt.</span><span class="sxs-lookup"><span data-stu-id="956be-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="956be-130">Kunder upplever försämrad prestanda onödig hämtning i PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="956be-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="956be-131">Roller som har ställts in icke-debiterbara i listan **resurskategorier** bör läggas till på fliken **Debiterbara roller** som **Icke debiterbar** på kontraktraden för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="956be-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="956be-132">Kunderna kan få försämrade prestanda när de skapar ett projekt eftersom **GetBookableResourceIdFromUser** hämtar alla bokningsbara resurser i stället för bara det primära ID:t.</span><span class="sxs-lookup"><span data-stu-id="956be-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="956be-133">**TransactionType**-entiteten saknar plugin-programmet för valideringsuppdatering för att förhindra att användare anger **Enheter** och **UnitGroups** som inte är giltiga för transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="956be-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="956be-134">Steget **Ta bort** fungerar inte för import av tidsposter.</span><span class="sxs-lookup"><span data-stu-id="956be-134">The **Remove** step does not work for time entry import.</span></span>
