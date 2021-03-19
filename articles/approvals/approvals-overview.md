---
title: Översikt över godkännanden
description: I det här ämne finns information om hur du arbetar med godkännanden i Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a7573b95998387453b72dbcb73c3de977ed7d913
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290381"
---
# <a name="approvals-overview"></a><span data-ttu-id="595a1-103">Översikt över godkännanden</span><span class="sxs-lookup"><span data-stu-id="595a1-103">Approvals overview</span></span>

<span data-ttu-id="595a1-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="595a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="595a1-105">Tids-och utgiftsöverföringar rör sig genom ett arbetsflöde för godkännande.</span><span class="sxs-lookup"><span data-stu-id="595a1-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="595a1-106">När posterna har godkänts registreras transaktioner i schemat med verkliga värden och tid.</span><span class="sxs-lookup"><span data-stu-id="595a1-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="595a1-107">Arbetsflöde för godkännande</span><span class="sxs-lookup"><span data-stu-id="595a1-107">Approvals workflow</span></span>
<span data-ttu-id="595a1-108">När du skapar och skickar en tid- eller utgiftspost skapas en godkännandepost.</span><span class="sxs-lookup"><span data-stu-id="595a1-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="595a1-109">Projektgodkännaren eller din chef granskar och godkänner posten.</span><span class="sxs-lookup"><span data-stu-id="595a1-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="595a1-110">Om posten är kopplad till ett projekt, skapas de faktiska värdena när den har godkänts.</span><span class="sxs-lookup"><span data-stu-id="595a1-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="595a1-111">Det gör att kostnaden och faktureringen kan spåras.</span><span class="sxs-lookup"><span data-stu-id="595a1-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="595a1-112">Godkänna en post</span><span class="sxs-lookup"><span data-stu-id="595a1-112">Approve an entry</span></span>
<span data-ttu-id="595a1-113">Med formuläret **Godkännanden** kan du växla mellan olika vyer så att du kan visa olika typer av godkännanden.</span><span class="sxs-lookup"><span data-stu-id="595a1-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="595a1-114">Gå till formuläret **Godkännanden** och välj **Utgifter**, **Tid** eller **Återkallanden**.</span><span class="sxs-lookup"><span data-stu-id="595a1-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="595a1-115">Granska varje godkännande och markera de du vill godkänna.</span><span class="sxs-lookup"><span data-stu-id="595a1-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="595a1-116">Välj **Godkänn** om du vill godkänna de markerade posterna.</span><span class="sxs-lookup"><span data-stu-id="595a1-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="595a1-117">Posterna kommer att bearbetas och verkliga värden och bokningar skapas.</span><span class="sxs-lookup"><span data-stu-id="595a1-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="595a1-118">Avvisa en post</span><span class="sxs-lookup"><span data-stu-id="595a1-118">Reject an entry</span></span>
<span data-ttu-id="595a1-119">Som projektgodkännare kan du behöva skicka tillbaka en post till en användare för korrigering.</span><span class="sxs-lookup"><span data-stu-id="595a1-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="595a1-120">Gå till formuläret **Godkännanden** och markera den post du vill avvisa.</span><span class="sxs-lookup"><span data-stu-id="595a1-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="595a1-121">Välj **Avvisa**.</span><span class="sxs-lookup"><span data-stu-id="595a1-121">Select **Reject**.</span></span>
3. <span data-ttu-id="595a1-122">Valfri – Lägg till en kommentar i dialogrutan **Avvisade kommentarer** om du vill meddela användaren varför posten har avvisats.</span><span class="sxs-lookup"><span data-stu-id="595a1-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="595a1-123">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="595a1-123">Select **OK**.</span></span> <span data-ttu-id="595a1-124">Posten skickas tillbaka till användaren.</span><span class="sxs-lookup"><span data-stu-id="595a1-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="595a1-125">Återkalla poster</span><span class="sxs-lookup"><span data-stu-id="595a1-125">Recall entries</span></span>
<span data-ttu-id="595a1-126">Du kan behöva återkalla en post som du har skickat.</span><span class="sxs-lookup"><span data-stu-id="595a1-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="595a1-127">Om posten inte har godkänts returneras den omedelbart.</span><span class="sxs-lookup"><span data-stu-id="595a1-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="595a1-128">En godkänd post kan emellertid ha en väsentlig inverkan.</span><span class="sxs-lookup"><span data-stu-id="595a1-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="595a1-129">Projektgodkännaren måste godkänna återkallningen för att kunna återföra transaktionen i faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="595a1-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="595a1-130">Specificera projektgodkännare</span><span class="sxs-lookup"><span data-stu-id="595a1-130">Specify Project approvers</span></span>
<span data-ttu-id="595a1-131">Varje projekt har ett antal projektteammedlemmar.</span><span class="sxs-lookup"><span data-stu-id="595a1-131">Each project has a number of project team members.</span></span> <span data-ttu-id="595a1-132">Du kan ange vilka teammedlemmar som också är projektgodkännare.</span><span class="sxs-lookup"><span data-stu-id="595a1-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="595a1-133">Gå till formuläret **Projekt** och öppna projektet från listan.</span><span class="sxs-lookup"><span data-stu-id="595a1-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="595a1-134">Under fliken **Team** väljer du den teammedlem som ska vara projektgodkännare och trycker sedan på **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="595a1-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="595a1-135">Sätt fältet **Projektgodkännare** på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="595a1-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="595a1-136">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="595a1-136">Select **Save**.</span></span>
5. <span data-ttu-id="595a1-137">Upprepa steg 2–4 om du vill lägga till ytterligare projektgodkännare.</span><span class="sxs-lookup"><span data-stu-id="595a1-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="595a1-138">Konfigurera användarens chef</span><span class="sxs-lookup"><span data-stu-id="595a1-138">Configure the user's manager</span></span>

1. <span data-ttu-id="595a1-139">Gå till **Inställningar** > **Säkerhet** > **Användare**.</span><span class="sxs-lookup"><span data-stu-id="595a1-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="595a1-140">Välj den användare som du vill tilldela en chef och välj sedan chef från listan i området **organisationsinformation**.</span><span class="sxs-lookup"><span data-stu-id="595a1-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="595a1-141">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="595a1-141">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]