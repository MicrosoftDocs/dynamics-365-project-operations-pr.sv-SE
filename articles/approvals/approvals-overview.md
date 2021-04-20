---
title: Översikt över godkännanden
description: I det här ämne finns information om hur du arbetar med godkännanden i Project Operations.
author: stsporen
manager: Annbe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b2da22e10cf6c40a2c84bcd32437b2830f830d07
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852521"
---
# <a name="approvals-overview"></a><span data-ttu-id="a9dd3-103">Översikt över godkännanden</span><span class="sxs-lookup"><span data-stu-id="a9dd3-103">Approvals overview</span></span>

<span data-ttu-id="a9dd3-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="a9dd3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a9dd3-105">Skicka in tid, utgifter och materialanvändning passerar ett godkännandearbetsflöde.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="a9dd3-106">När posterna har godkänts registreras transaktioner i schemat med verkliga värden och tid.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="a9dd3-107">Arbetsflöde för godkännande</span><span class="sxs-lookup"><span data-stu-id="a9dd3-107">Approvals workflow</span></span>
<span data-ttu-id="a9dd3-108">När du skapar och skickar en tids-, kostnad- eller materialanvändningspost skapas en godkännandepost.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="a9dd3-109">Projektgodkännaren eller chefen granskar och godkänner posten.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="a9dd3-110">Om posten är relaterad till ett projekt skapas de faktiska värdet när den godkänns.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="a9dd3-111">Det gör att kostnaden och faktureringen kan spåras.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="a9dd3-112">Godkänna en post</span><span class="sxs-lookup"><span data-stu-id="a9dd3-112">Approve an entry</span></span>
<span data-ttu-id="a9dd3-113">På sidan **Godkännanden** kan du växla mellan olika vyer så att du kan visa de olika typerna av godkännanden.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="a9dd3-114">Gå till sidan **Godkännanden** och välj **Utgifter**, **Tid**, **Materialanvändning** eller **Återkallade**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="a9dd3-115">Granska varje godkännande och markera de du vill godkänna.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="a9dd3-116">Välj **Godkänn** om du vill godkänna de markerade posterna.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="a9dd3-117">Systemet bearbetar posterna och skapar faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="a9dd3-118">Avvisa en post</span><span class="sxs-lookup"><span data-stu-id="a9dd3-118">Reject an entry</span></span>
<span data-ttu-id="a9dd3-119">Som projektgodkännare kan du behöva skicka tillbaka en post till en användare för korrigering.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="a9dd3-120">Gå till sidan **Godkännanden** och välj den post som ska avvisas.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="a9dd3-121">Välj **Avvisa**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-121">Select **Reject**.</span></span>
3. <span data-ttu-id="a9dd3-122">Valfritt, lägg till en kommentar i dialogrutan **Kommentarer till avvisning** för att informera användaren om varför posten avvisas.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="a9dd3-123">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-123">Select **OK**.</span></span> <span data-ttu-id="a9dd3-124">Posten skickas tillbaka till användaren.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="a9dd3-125">Avbryt godkännandet</span><span class="sxs-lookup"><span data-stu-id="a9dd3-125">Cancel approval</span></span>
<span data-ttu-id="a9dd3-126">I vissa fall kan du behöva avbryta en post som godkänts tidigare.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="a9dd3-127">Om du avbryter en tidigare godkänd post får det ekonomiska effekter.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="a9dd3-128">Återkalla godkännandebegäran</span><span class="sxs-lookup"><span data-stu-id="a9dd3-128">Approving recall requests</span></span>
<span data-ttu-id="a9dd3-129">I vissa fall kan en konsult behöva godkänna en post som godkänts tidigare.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="a9dd3-130">Om du avbryter en tidigare godkänd post får det ekonomiska effekter.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="a9dd3-131">Projekt godkännaren krävs för att godkänna affären för att återställa transaktionen i Faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="a9dd3-132">Specificera projektgodkännare</span><span class="sxs-lookup"><span data-stu-id="a9dd3-132">Specify Project approvers</span></span>
<span data-ttu-id="a9dd3-133">Varje projekt har ett antal projektteammedlemmar.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-133">Each project has a number of project team members.</span></span> <span data-ttu-id="a9dd3-134">Du kan ange vilka teammedlemmar som också är projektgodkännare.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="a9dd3-135">Gå till sidan **Projekt** och öppna projektet från listan.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="a9dd3-136">Under fliken **Team** väljer du den teammedlem som ska vara projektgodkännare och trycker sedan på **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="a9dd3-137">Sätt fältet **Projektgodkännare** på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="a9dd3-138">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-138">Select **Save**.</span></span>
5. <span data-ttu-id="a9dd3-139">Upprepa steg 2–4 om du vill lägga till ytterligare projektgodkännare.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="a9dd3-140">Konfigurera användarens chef</span><span class="sxs-lookup"><span data-stu-id="a9dd3-140">Configure the user's manager</span></span>

1. <span data-ttu-id="a9dd3-141">Gå till **Inställningar** > **Säkerhet** > **Användare**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="a9dd3-142">Välj den användare som du vill tilldela en chef och välj sedan chef från listan i området **organisationsinformation**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="a9dd3-143">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
