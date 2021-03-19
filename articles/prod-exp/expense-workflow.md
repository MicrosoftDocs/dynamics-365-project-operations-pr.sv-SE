---
title: Arbetsflöde för utgiftshantering
description: I det här ämnet förklaras hur du kan använda arbetsflödessystemet i Microsoft Dynamics 365 Finance för att konfigurera en granskningsprocess för utgiftsrapporter i utgiftshantering.
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
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271690"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="e555c-103">Arbetsflöde för utgiftshantering</span><span class="sxs-lookup"><span data-stu-id="e555c-103">Expense management workflow</span></span>

<span data-ttu-id="e555c-104">Du kan använda arbetsflödessystemet för att konfigurera en granskningsprocess för utgiftsrapporter i utgiftshantering.</span><span class="sxs-lookup"><span data-stu-id="e555c-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="e555c-105">Du kan konfigurera ett arbetsflöde som använder följande kriterier för att avgöra vem som godkänner utgiftsrapporter:</span><span class="sxs-lookup"><span data-stu-id="e555c-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="e555c-106">Hierarkin för medarbetarrapporter och fördefinierade godkännandegränser</span><span class="sxs-lookup"><span data-stu-id="e555c-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="e555c-107">Ett godkännande på flera nivåer som stöder interimistiska godkännare och en slutlig godkännare</span><span class="sxs-lookup"><span data-stu-id="e555c-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="e555c-108">Ekonomiska dimensioner och projektansvar</span><span class="sxs-lookup"><span data-stu-id="e555c-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="e555c-109">Tilldelning till specifika användare eller användargrupper</span><span class="sxs-lookup"><span data-stu-id="e555c-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="e555c-110">Du kan skapa arbetsflödesgodkännanden för utgiftsrapporter, reserekvisitioner, förskott och återbetalning av moms.</span><span class="sxs-lookup"><span data-stu-id="e555c-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="e555c-111">**Exempel**</span><span class="sxs-lookup"><span data-stu-id="e555c-111">**Example**</span></span>

<span data-ttu-id="e555c-112">Följande process är ett exempel på arbetsflödet för utgiftshantering för en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="e555c-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="e555c-113">En medarbetare skapar och sparar en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="e555c-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="e555c-114">Medarbetaren skickar in utgiftsrapporten för godkännande.</span><span class="sxs-lookup"><span data-stu-id="e555c-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="e555c-115">Godkännaren identifieras utifrån de regler som definierades när arbetsflödet konfigurerades.</span><span class="sxs-lookup"><span data-stu-id="e555c-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="e555c-116">Godkännaren får ett meddelande om att en utgiftsrapport är klar för godkännande.</span><span class="sxs-lookup"><span data-stu-id="e555c-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="e555c-117">Godkännaren granskar utgiftsrapporten och kontrollerar att följande villkor uppfylls:</span><span class="sxs-lookup"><span data-stu-id="e555c-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="e555c-118">Utgifterna strider inte mot några utgiftsprinciper.</span><span class="sxs-lookup"><span data-stu-id="e555c-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="e555c-119">Om en utgift bryter mot en princip verifierar godkännaren att utgiftsrapporten innehåller en giltig affärsmotivering.</span><span class="sxs-lookup"><span data-stu-id="e555c-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="e555c-120">Elektroniska kvitton bifogas utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="e555c-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="e555c-121">Godkännaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="e555c-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="e555c-122">Utgiftsrapporten tilldelas koordinatorn för bokföring i leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="e555c-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="e555c-123">Ett av följande steg inträffar, beroende på om automatisk bokföring är konfigurerad:</span><span class="sxs-lookup"><span data-stu-id="e555c-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="e555c-124">Om automatisk bokföring är konfigurerad bearbetas utgiftsrapporten för betalningen och utgiftsrapportens status uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e555c-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="e555c-125">Om automatisk bokföring inte är konfigurerad verifierar koordinatorn för leverantörsreskontra att alla ursprungliga kvitton har skickats in och att kvittona stämmer överens med utgifterna i utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="e555c-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="e555c-126">Alla momskoder som anges i utgiftsrapporten måste också verifieras som riktiga.</span><span class="sxs-lookup"><span data-stu-id="e555c-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="e555c-127">När dessa krav har verifierats bokförs utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="e555c-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="e555c-128">När utgiftsrapporten har bokförts auktoriseras betalningen för utgiftsrapporten och medarbetaren återbetalas.</span><span class="sxs-lookup"><span data-stu-id="e555c-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]