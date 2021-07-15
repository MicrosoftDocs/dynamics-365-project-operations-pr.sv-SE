---
title: Prestanda för projektfakturaförslag
description: Detta ämne ger information om prestandaförbättringar av projektfakturaförslag.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269812"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="1a6ad-103">Prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="1a6ad-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a6ad-104">När du skapar ett nytt fakturaförslag kan du stöta på prestandaproblem när antalet projekt och delprojekt ökar.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="1a6ad-105">För att förbättra prestanda är en funktion tillgänglig som minskar den tid som krävs för att skapa ett nytt fakturaförslag för bokförda projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="1a6ad-106">Aktivera förbättring av prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="1a6ad-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="1a6ad-107">Så här aktiverar du funktionen för förbättring av prestanda för projektfakturaförslag:</span><span class="sxs-lookup"><span data-stu-id="1a6ad-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="1a6ad-108">Gå till **Funktionshantering** > **Alla**.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="1a6ad-109">Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="1a6ad-110">Välj **Aktivera nu**.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="1a6ad-111">Uppdatera webbläsaren och skapa sedan ett nytt fakturaförslag.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="1a6ad-112">Inaktivera förbättring av prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="1a6ad-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="1a6ad-113">Slutför följande steg för att stänga av prestandaförbättringen av projektfakturaförslaget.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="1a6ad-114">Gå till **Funktionshantering** > **Alla**.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="1a6ad-115">Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="1a6ad-116">Välj **Inaktivera**.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="1a6ad-117">Uppdatera webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="1a6ad-118">Fakturaförslagsresultat kan inte tillämpas när faktureringsregler har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="1a6ad-119">Under batchprocessen för att skapa fakturaförslag delar antalet underaktiviteter uppgifterna till ett högsta antal baserat på antalet kontrakt med fakturabara transaktioner, oavsett vad du har angett.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="1a6ad-120">Om du till exempel anger **3** för antalet underaktiviteter för att skapa fakturaförslag i batch och det bara finns två kontrakt med faktureringsbara transaktioner skapas endast två underaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="1a6ad-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
