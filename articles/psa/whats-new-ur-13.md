---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 13, version 3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 13, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085500"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="cb73b-103">Project Service Automation uppdateringsversion 13, V3</span><span class="sxs-lookup"><span data-stu-id="cb73b-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="cb73b-104">Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="cb73b-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cb73b-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cb73b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cb73b-107">Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="cb73b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="cb73b-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cb73b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cb73b-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 13.</span><span class="sxs-lookup"><span data-stu-id="cb73b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="cb73b-110">Den här versionen har versionsnumret för V3.10.3.18 och är tillgängligt enligt följande schema:</span><span class="sxs-lookup"><span data-stu-id="cb73b-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="cb73b-111">**Allmän tillgänglighet (självuppdatering):** 2019 november</span><span class="sxs-lookup"><span data-stu-id="cb73b-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="cb73b-112">**Automatisk uppdatering:** December 2019</span><span class="sxs-lookup"><span data-stu-id="cb73b-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="cb73b-113">Uppdatering version 13</span><span class="sxs-lookup"><span data-stu-id="cb73b-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="cb73b-114">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="cb73b-114">Bug fixes</span></span>

- <span data-ttu-id="cb73b-115">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="cb73b-115">Time and Expense</span></span>

     - <span data-ttu-id="cb73b-116">Fast: Sökfunktionen på sidan **utgiftsgodkännande** fungerar inte när du söker efter utgiftssyften.</span><span class="sxs-lookup"><span data-stu-id="cb73b-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="cb73b-117">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="cb73b-117">Resource Management</span></span>

     - <span data-ttu-id="cb73b-118">Fast: nummer i avstämningen har uppdaterats till att vara högerjusterad.</span><span class="sxs-lookup"><span data-stu-id="cb73b-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="cb73b-119">Fast: namngivna resurser kan inte tilldelas till aktiviteter via fliken **schema**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="cb73b-120">Projektledning</span><span class="sxs-lookup"><span data-stu-id="cb73b-120">Project Management</span></span>

     - <span data-ttu-id="cb73b-121">Fast: Null referensundantag vid tilldelning av teammedlem när **TransactionType** saknas i inställningsinformation för **enhet** och **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="cb73b-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="cb73b-122">Sales</span><span class="sxs-lookup"><span data-stu-id="cb73b-122">Sales</span></span>

     - <span data-ttu-id="cb73b-123">Fast: dubbla transaktionstypposter returnerar ett fel när rollprisposter skapas.</span><span class="sxs-lookup"><span data-stu-id="cb73b-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="cb73b-124">Fast: extra knappar för **ny affärsmöjlighet** , **offert** , **orderrad** och **lägg till produkt** visas i kommandon för affärsmöjligheter, offerter, orderprodukter och de projektbaserade raderna i underrutnätet.</span><span class="sxs-lookup"><span data-stu-id="cb73b-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


