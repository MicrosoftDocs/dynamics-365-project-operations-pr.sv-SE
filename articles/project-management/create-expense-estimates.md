---
title: Utgiftsberäkningar
description: I det här ämnet finns information om hur du definierar eller uppskattar projektbaserade utgifter.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085462"
---
# <a name="expense-estimates"></a><span data-ttu-id="cc2d9-103">Utgiftsberäkningar</span><span class="sxs-lookup"><span data-stu-id="cc2d9-103">Expense estimates</span></span>
<span data-ttu-id="cc2d9-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="cc2d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc2d9-105">Tillsammans med att definiera resursbaserade uppskattningar kan projektledare med hjälp av Dynamics 365 Project Operations definiera projektbaserade utgifter för varje projekt.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="cc2d9-106">Varje utgiftspost kan kopplas till en specifik projektuppgift eller utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="cc2d9-107">Utgiftskategorier definieras vanligtvis på organisationsnivå.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="cc2d9-108">Prissättning för varje utgiftskategori definieras vanligtvis i följande hierarki:</span><span class="sxs-lookup"><span data-stu-id="cc2d9-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="cc2d9-109">Organisation</span><span class="sxs-lookup"><span data-stu-id="cc2d9-109">Organization</span></span>
- <span data-ttu-id="cc2d9-110">Kund</span><span class="sxs-lookup"><span data-stu-id="cc2d9-110">Customer</span></span>
- <span data-ttu-id="cc2d9-111">Offert/kontrakt</span><span class="sxs-lookup"><span data-stu-id="cc2d9-111">Quote/contract</span></span>

<span data-ttu-id="cc2d9-112">Följ stegen nedan om du vill visa, lägga till eller ta bort en projektutgift.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="cc2d9-113">Gå till **Projekt** och välj det projekt du vill arbeta med.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="cc2d9-114">Välj fliken **Projektuppskattningar** och visa listan med projektutgifter.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="cc2d9-115">Välj **Ny utgift** om du vill lägga till en utgift.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="cc2d9-116">Du kan också välja vilka utgifter som ska tas bort och sedan välja **Ta bort utgift**.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="cc2d9-117">Följande attribut anges för varje utgiftsradartikel:</span><span class="sxs-lookup"><span data-stu-id="cc2d9-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="cc2d9-118">**Kategori** : de vanliga grupperingarna som används för att beskriva alla utgifter som uppstått i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="cc2d9-119">**Startdatum** : det datum då utgiften bedöms bli påförd.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="cc2d9-120">**Antal** : uppskattat antal utgiftsartiklar för en specifik kategori.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="cc2d9-121">**Självkostnad per enhet** : det enhetspris som används för att beräkna kostnaden för utgiften.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="cc2d9-122">**Försäljningspris per enhet** : det enhetspris som används för att beräkna försäljningspriset för utgiften.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

