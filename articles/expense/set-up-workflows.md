---
title: Ställ in arbetsflöden för utgiftshantering
description: Du kan konfigurera en arbetsflödesprocess som används för att granska och godkänna rese- och utgiftsdokument.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276055"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="de13a-103">Ställ in arbetsflöden för utgiftshantering</span><span class="sxs-lookup"><span data-stu-id="de13a-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="de13a-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="de13a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de13a-105">Du kan konfigurera en arbetsflödesprocess för att granska och godkänna rese- och utgiftsdokument.</span><span class="sxs-lookup"><span data-stu-id="de13a-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="de13a-106">Du kan definiera arbetsflöden för utgiftsrapporter, reserekvisitioner och begäran om förskott.</span><span class="sxs-lookup"><span data-stu-id="de13a-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="de13a-107">Ett arbetsflöde representerar en affärsprocess och definierar hur ett dokument flödar i systemet.</span><span class="sxs-lookup"><span data-stu-id="de13a-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="de13a-108">I arbetsflödet anges också vem som måste slutföra en uppgift eller godkänna ett dokument.</span><span class="sxs-lookup"><span data-stu-id="de13a-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="de13a-109">Det finns flera fördelar med att använda arbetsflödessystemet i organisationen:</span><span class="sxs-lookup"><span data-stu-id="de13a-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="de13a-110">**Konsekventa processer**: du kan definiera godkännande processen för specifika dokument, t.ex. inköpsrekvisitioner och utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="de13a-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="de13a-111">Genom att använda arbetsflödessystemet ser du till att dokumenten bearbetas och godkänns på ett konsekvent och effektivt sätt.</span><span class="sxs-lookup"><span data-stu-id="de13a-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="de13a-112">**Processens synlighet**: du kan spåra status, historik och prestandamått för en specifik arbetsflödesinstans.</span><span class="sxs-lookup"><span data-stu-id="de13a-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="de13a-113">På det här sättet kan du fastställa om ändringar ska göras i arbetsflödet för att öka effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="de13a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="de13a-114">**Centraliserad arbetslista**: användare kan visa en centraliserad arbetslista för att visa uppgifter och godkännanden som har tilldelats dem.</span><span class="sxs-lookup"><span data-stu-id="de13a-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="de13a-115">Arbetsflödestyper</span><span class="sxs-lookup"><span data-stu-id="de13a-115">Workflow types</span></span>

<span data-ttu-id="de13a-116">I följande tabell visas de typer av arbetsflöden som du kan skapa i **utgiftshantering**.</span><span class="sxs-lookup"><span data-stu-id="de13a-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="de13a-117"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="de13a-118"><strong>Använd den här typen för att</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="de13a-119"><strong>Utgiftsrapport för automatiskt godkännande</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="de13a-120">Skapa godkännande arbetsflöden för utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="de13a-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="de13a-121"><strong>Automatisk bokföring av utgiftsrapporter</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="de13a-122">Skapa arbetsflöden för automatisk bokföring av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="de13a-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="de13a-123"><strong>Utgiftsradobjekt</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="de13a-124">Skapa godkännande arbetsflöden för radobjekt på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="de13a-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="de13a-125"><strong>Automatisk bokföring av utgiftsradartiklar</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="de13a-126">Skapa arbetsflöden för automatisk bokföring för radobjekt på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="de13a-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="de13a-127"><strong>Reserekvisition</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="de13a-128">Skapa godkännande arbetsflöden för reserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="de13a-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="de13a-129"><strong>Begäran om förskott</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="de13a-130">Skapa godkännande arbetsflöden för begäran om förskott.</span><span class="sxs-lookup"><span data-stu-id="de13a-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="de13a-131"><strong>Momsåtervinning</strong></span><span class="sxs-lookup"><span data-stu-id="de13a-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="de13a-132">Skapa godkännande arbetsflöden för att momsåtervinning.</span><span class="sxs-lookup"><span data-stu-id="de13a-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]