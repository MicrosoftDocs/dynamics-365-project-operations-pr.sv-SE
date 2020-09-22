---
title: Nyheter i Project Service Automation uppdatering version 13, v3
description: I den här ämnet finns information om nyheter i Project Service Automation uppdatering version 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756215"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="ae4d2-103">Project Service Automation V3, uppdatering version 13</span><span class="sxs-lookup"><span data-stu-id="ae4d2-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="ae4d2-104">Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="ae4d2-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ae4d2-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ae4d2-107">Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="ae4d2-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ae4d2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ae4d2-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 13.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="ae4d2-110">Den här versionen har versionsnumret för V3.10.3.18 och är tillgängligt enligt följande schema:</span><span class="sxs-lookup"><span data-stu-id="ae4d2-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="ae4d2-111">**Allmän tillgänglighet (självuppdatering):** 2019 november</span><span class="sxs-lookup"><span data-stu-id="ae4d2-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="ae4d2-112">**Automatisk uppdatering:** December 2019</span><span class="sxs-lookup"><span data-stu-id="ae4d2-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="ae4d2-113">Uppdatering version 13</span><span class="sxs-lookup"><span data-stu-id="ae4d2-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="ae4d2-114">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="ae4d2-114">Bug fixes</span></span>

- <span data-ttu-id="ae4d2-115">Tid och utgift</span><span class="sxs-lookup"><span data-stu-id="ae4d2-115">Time and Expense</span></span>

     - <span data-ttu-id="ae4d2-116">Fast: Sökfunktionen på sidan **utgiftsgodkännande** fungerar inte när du söker efter utgiftssyften.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="ae4d2-117">Resurshantering</span><span class="sxs-lookup"><span data-stu-id="ae4d2-117">Resource Management</span></span>

     - <span data-ttu-id="ae4d2-118">Fast: nummer i avstämningen har uppdaterats till att vara högerjusterad.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="ae4d2-119">Fast: namngivna resurser kan inte tilldelas till aktiviteter via fliken **schema**.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="ae4d2-120">Projektledning</span><span class="sxs-lookup"><span data-stu-id="ae4d2-120">Project Management</span></span>

     - <span data-ttu-id="ae4d2-121">Fast: Null referensundantag vid tilldelning av teammedlem när **TransactionType** saknas i inställningsinformation för **enhet** och **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="ae4d2-122">Sales</span><span class="sxs-lookup"><span data-stu-id="ae4d2-122">Sales</span></span>

     - <span data-ttu-id="ae4d2-123">Fast: dubbla transaktionstypposter returnerar ett fel när rollprisposter skapas.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="ae4d2-124">Fast: extra knappar för **ny affärsmöjlighet**, **offert**, **orderrad** och **lägg till produkt** visas i kommandon för affärsmöjligheter, offerter, orderprodukter och de projektbaserade raderna i underrutnätet.</span><span class="sxs-lookup"><span data-stu-id="ae4d2-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


