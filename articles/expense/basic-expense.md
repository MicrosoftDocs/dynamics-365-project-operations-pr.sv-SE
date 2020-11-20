---
title: Post för utgift (enkel)
description: I det här ämnet finns information om hur du arbetar med utgiftsposter i en enkel distribution.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121105"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="6bfb7-103">Post för utgift (enkel)</span><span class="sxs-lookup"><span data-stu-id="6bfb7-103">Expense entry (lite)</span></span>

<span data-ttu-id="6bfb7-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="6bfb7-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6bfb7-105">Grundläggande, eller enkel, utgiftshantering är möjligheten att registrera enkla utgifter.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="6bfb7-106">Du kan registrera utgifter för ett projekt och sedan kommer projektgodkännaren att granska och godkänna dem.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="6bfb7-107">Mer information om utgiftsfunktioner i Dynamics 365 Project Operations finns i [Utgiftsöversikt](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6bfb7-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="6bfb7-108">Registrera en grundläggande utgift</span><span class="sxs-lookup"><span data-stu-id="6bfb7-108">Capture a basic expense</span></span>

<span data-ttu-id="6bfb7-109">Du kan registrera dina utgifter så att du kan skicka dem till god kännaren.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="6bfb7-110">Gå till **Utgifter** och välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="6bfb7-111">Ange önskad utgiftsinformation på sidan **Ny utgift** och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="6bfb7-112">Skicka in en grundläggande utgift</span><span class="sxs-lookup"><span data-stu-id="6bfb7-112">Submit a basic expense</span></span>

<span data-ttu-id="6bfb7-113">När du har registrerat alla dina utgifter och du är redo att godkänna dem måste du skicka in dem.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="6bfb7-114">Gå till **Utgifter** och välj en utgift.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="6bfb7-115">Du kan också markera alla utgifter genom att använda kryssrutan längst upp.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="6bfb7-116">Välj **Skicka**.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-116">Select **Submit**.</span></span> <span data-ttu-id="6bfb7-117">Systemet bearbetar de markerade posterna och skapar sedan en förfrågan om utgiftsgodkännande.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="6bfb7-118">Återkalla en grundläggande utgift</span><span class="sxs-lookup"><span data-stu-id="6bfb7-118">Recall a basic expense</span></span>

<span data-ttu-id="6bfb7-119">När du skickar en utgift av misstag kan du återkalla den.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="6bfb7-120">Den tid som krävs för att återkalla en utgiftspost beror på godkännandestadiet.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="6bfb7-121">Om godkännaren ännu inte har godkänt posten kan återkallelsen ske omedelbart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="6bfb7-122">Om posten redan har godkänts ombeds godkännaren emellertid att godkänna återkallandet och återföra transaktionen.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="6bfb7-123">Gå till **Utgifter** och välj sedan den kostnad du vill återkalla i listan över utgifter.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="6bfb7-124">Välj **återkalla**.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-124">Select **Recall**.</span></span> <span data-ttu-id="6bfb7-125">Om utgiftsposten ännu inte har godkänts återkallar systemet den omedelbart.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="6bfb7-126">Om utgiftsposten redan har godkänts skapas en förfrågan om återkallande för att meddela godkännaren om att du vill återföra utgiften.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="6bfb7-127">Godkännaren bekräftar då att återföringen kan utföras och att posten returneras.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="6bfb7-128">Ta bort en grundläggande utgift</span><span class="sxs-lookup"><span data-stu-id="6bfb7-128">Delete a basic expense</span></span>

<span data-ttu-id="6bfb7-129">Utgifter som ännu inte har skickats kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="6bfb7-130">Om du vill ta bort en utgift som redan har skickats måste du först återkalla den.</span><span class="sxs-lookup"><span data-stu-id="6bfb7-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="6bfb7-131">Se även</span><span class="sxs-lookup"><span data-stu-id="6bfb7-131">See also</span></span>

- [<span data-ttu-id="6bfb7-132">Översikt över godkännanden</span><span class="sxs-lookup"><span data-stu-id="6bfb7-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
