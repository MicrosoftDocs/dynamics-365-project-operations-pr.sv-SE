---
title: Prestanda för projektfakturaförslag
description: Detta ämne ger information om prestandaförbättringar av projektfakturaförslag.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920324"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="4fa6b-103">Prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="4fa6b-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa6b-104">När du skapar ett nytt fakturaförslag kan du stöta på prestandaproblem när antalet projekt och delprojekt ökar.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="4fa6b-105">För att förbättra prestanda är en funktion tillgänglig som minskar den tid som krävs för att skapa ett nytt fakturaförslag för bokförda projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4fa6b-106">Aktivera förbättring av prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="4fa6b-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4fa6b-107">Så här aktiverar du funktionen för förbättring av prestanda för projektfakturaförslag:</span><span class="sxs-lookup"><span data-stu-id="4fa6b-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="4fa6b-108">Gå till **Funktionshantering** > **Alla**.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4fa6b-109">Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4fa6b-110">Välj **Aktivera nu**.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="4fa6b-111">Uppdatera webbläsaren och skapa sedan ett nytt fakturaförslag.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4fa6b-112">Inaktivera förbättring av prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="4fa6b-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4fa6b-113">Slutför följande steg för att stänga av prestandaförbättringen av projektfakturaförslaget.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="4fa6b-114">Gå till **Funktionshantering** > **Alla**.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4fa6b-115">Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4fa6b-116">Välj **Inaktivera**.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="4fa6b-117">Uppdatera webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4fa6b-118">Prestanda för fakturaförslag kan inte tillämpas när faktureringsregler är aktiverade eller batchprocesser körs.</span><span class="sxs-lookup"><span data-stu-id="4fa6b-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
