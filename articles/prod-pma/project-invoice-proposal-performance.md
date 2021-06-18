---
title: Prestanda för projektfakturaförslag
description: Detta ämne ger information om prestandaförbättringar av projektfakturaförslag.
author: Yowelle
ms.date: 04/20/2021
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999513"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="a4f8e-103">Prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="a4f8e-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4f8e-104">När du skapar ett nytt fakturaförslag kan du stöta på prestandaproblem när antalet projekt och delprojekt ökar.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="a4f8e-105">För att förbättra prestanda är en funktion tillgänglig som minskar den tid som krävs för att skapa ett nytt fakturaförslag för bokförda projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="a4f8e-106">Aktivera förbättring av prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="a4f8e-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="a4f8e-107">Så här aktiverar du funktionen för förbättring av prestanda för projektfakturaförslag:</span><span class="sxs-lookup"><span data-stu-id="a4f8e-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="a4f8e-108">Gå till **Funktionshantering** > **Alla**.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="a4f8e-109">Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="a4f8e-110">Välj **Aktivera nu**.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="a4f8e-111">Uppdatera webbläsaren och skapa sedan ett nytt fakturaförslag.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="a4f8e-112">Inaktivera förbättring av prestanda för projektfakturaförslag</span><span class="sxs-lookup"><span data-stu-id="a4f8e-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="a4f8e-113">Slutför följande steg för att stänga av prestandaförbättringen av projektfakturaförslaget.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="a4f8e-114">Gå till **Funktionshantering** > **Alla**.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="a4f8e-115">Leta reda på i listan över funktioner **Förbättring av prestanda för projektfakturaförslag**.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="a4f8e-116">Välj **Inaktivera**.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="a4f8e-117">Uppdatera webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="a4f8e-118">Prestanda för fakturaförslag kan inte tillämpas när faktureringsregler är aktiverade eller batchprocesser körs.</span><span class="sxs-lookup"><span data-stu-id="a4f8e-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
