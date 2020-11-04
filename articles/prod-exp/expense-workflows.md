---
title: Ställ in arbetsflöden för utgiftshantering
description: Du kan konfigurera en arbetsflödesprocess för att granska och godkänna rese- och utgiftsdokument.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085694"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="84428-103">Ställ in arbetsflöden för utgiftshantering</span><span class="sxs-lookup"><span data-stu-id="84428-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84428-104">Du kan konfigurera en arbetsflödesprocess som används för att granska och godkänna rese- och utgiftsdokument.</span><span class="sxs-lookup"><span data-stu-id="84428-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="84428-105">Dokument för vilka arbetsflöden kan definieras innefattar utgiftsrapporter, reserekvisitioner och förfrågningar om förskott.</span><span class="sxs-lookup"><span data-stu-id="84428-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="84428-106">Ett arbetsflöde representerar en affärsprocess.</span><span class="sxs-lookup"><span data-stu-id="84428-106">A workflow represents a business process.</span></span> <span data-ttu-id="84428-107">Den definierar hur ett dokument flödar i systemet och anger vem som måste utföra en uppgift eller godkänna ett dokument.</span><span class="sxs-lookup"><span data-stu-id="84428-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="84428-108">Det finns flera fördelar med att använda arbetsflödessystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="84428-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="84428-109">**Konsekventa processer** – du kan definiera godkännandeprocessen för specifika dokument, t.ex. inköpsrekvisitioner och utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="84428-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="84428-110">Genom att använda arbetsflödessystemet ser du till att dokumenten bearbetas och godkänns på ett konsekvent och effektivt sätt.</span><span class="sxs-lookup"><span data-stu-id="84428-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="84428-111">Processens synlighet – Du kan spåra status, historik och prestandamått för en specifik arbetsflödesinstans.</span><span class="sxs-lookup"><span data-stu-id="84428-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="84428-112">På det här sättet kan du fastställa om ändringar ska göras i arbetsflödet för att öka effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="84428-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="84428-113">Centraliserad arbetslista – Användare kan visa en centraliserad arbetslista för att visa uppgifter och godkännanden som har tilldelats dem.</span><span class="sxs-lookup"><span data-stu-id="84428-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="84428-114">**Typer av arbetsflöden som du kan skapa**</span><span class="sxs-lookup"><span data-stu-id="84428-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="84428-115">I följande tabell visas de typer av arbetsflöden som du kan skapa i **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="84428-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="84428-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="84428-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="84428-117"><strong>Använd den här typen för att</strong></span><span class="sxs-lookup"><span data-stu-id="84428-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="84428-118"><strong>Utgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="84428-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="84428-119">Skapa godkännande arbetsflöden för utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="84428-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="84428-120"><strong>Automatisk bokföring av utgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="84428-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="84428-121">Skapa arbetsflöden för automatisk bokföring av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="84428-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="84428-122"><strong>Utgiftsradobjekt</strong></span><span class="sxs-lookup"><span data-stu-id="84428-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="84428-123">Skapa godkännande arbetsflöden för radobjekt på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="84428-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="84428-124"><strong>Automatisk bokföring av utgiftsradartiklar</strong></span><span class="sxs-lookup"><span data-stu-id="84428-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="84428-125">Skapa arbetsflöden för automatisk bokföring för radobjekt på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="84428-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="84428-126"><strong>Reserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="84428-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="84428-127">Skapa godkännande arbetsflöden för reserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="84428-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="84428-128"><strong>Begäran om förskott</strong></span><span class="sxs-lookup"><span data-stu-id="84428-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="84428-129">Skapa godkännande arbetsflöden för begäran om förskott.</span><span class="sxs-lookup"><span data-stu-id="84428-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="84428-130"><strong>Momsåtervinning</strong></span><span class="sxs-lookup"><span data-stu-id="84428-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="84428-131">Skapa godkännande arbetsflöden för att momsåtervinning.</span><span class="sxs-lookup"><span data-stu-id="84428-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

