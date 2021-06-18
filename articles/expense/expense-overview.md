---
title: Översikt över utgifter
description: I det här ämnet finns information om funktionen Utgift i Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2a26b321e15080cc6a4a6a3ed410be175e790a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995418"
---
# <a name="expense-home-page"></a><span data-ttu-id="58061-103">Startsida för utgifter</span><span class="sxs-lookup"><span data-stu-id="58061-103">Expense home page</span></span>

<span data-ttu-id="58061-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="58061-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="58061-105">Dynamics 365 Project Operations stöder möjligheten att bearbeta utgifter.</span><span class="sxs-lookup"><span data-stu-id="58061-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="58061-106">Utgiftsbehandling sker med eller utan projekt med hjälp av ett anpassningsbart arbetsflöde med principer, transaktionskategorier och godkännanden.</span><span class="sxs-lookup"><span data-stu-id="58061-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="58061-107">I Project Operations finns två distributionsmodeller som har stöd för utgift:</span><span class="sxs-lookup"><span data-stu-id="58061-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="58061-108">**Fullständig**: Fullständig distribution finns tillgänglig för **Project Operations för resursbaserade/icke-lagerbaserade scenarier** eller **Project Operations för produktionsorderbaserade scenarier**.</span><span class="sxs-lookup"><span data-stu-id="58061-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="58061-109">**Grundläggande**: grundläggande distribution är tillgänglig för **Project Operations för resursbaserade/icke lagerbaserade scenarier** och **Enkel distribution – avtal till proforma-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="58061-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="58061-110">Fullständig</span><span class="sxs-lookup"><span data-stu-id="58061-110">Full</span></span> 
<span data-ttu-id="58061-111">Fullständig utläggsdistribution ger en fullständig policyefterlevnad och omfattar möjligheten att skapa policyer, till exempel:</span><span class="sxs-lookup"><span data-stu-id="58061-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="58061-112">Gränser för utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="58061-112">Expense category limits</span></span>
  - <span data-ttu-id="58061-113">Resor</span><span class="sxs-lookup"><span data-stu-id="58061-113">Travel</span></span>
  - <span data-ttu-id="58061-114">Per dag</span><span class="sxs-lookup"><span data-stu-id="58061-114">Per diem</span></span>
  - <span data-ttu-id="58061-115">Import av kreditkort</span><span class="sxs-lookup"><span data-stu-id="58061-115">Credit card imports</span></span>
  - <span data-ttu-id="58061-116">Optisk teckenigenkänning på kvitto</span><span class="sxs-lookup"><span data-stu-id="58061-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="58061-117">Grundläggande</span><span class="sxs-lookup"><span data-stu-id="58061-117">Basic</span></span> 
<span data-ttu-id="58061-118">Scenariot med grundläggande utgiftsdistribution kan du endast registrera grundläggande utgifter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="58061-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="58061-119">Mer information finns i [Utgiftspost (enkel)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="58061-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="58061-120">Fastställa din utgiftsdistribution</span><span class="sxs-lookup"><span data-stu-id="58061-120">Determine your Expense deployment</span></span>
<span data-ttu-id="58061-121">Kontrollera om du kör distributionen Grundläggande utgiftshantering genom att kontrollera att webbadressen slutar på **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="58061-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]