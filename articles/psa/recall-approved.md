---
title: Återkalla godkända tids- eller utgiftsposter
description: I det här ämnet finns information om hur du återkallar en tidigare godkänd tids- eller utgiftstransaktion.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147877"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="6004b-103">Återkalla godkända tids- eller utgiftsposter</span><span class="sxs-lookup"><span data-stu-id="6004b-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6004b-104">En projektteammedlem eller en annan person som skickar en tids- eller utgiftspost kan återkalla den tids- eller utgiftsposten efter att den har godkänts.</span><span class="sxs-lookup"><span data-stu-id="6004b-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="6004b-105">Processen för att återkalla en godkänd tids- eller utgiftspost består av två steg:</span><span class="sxs-lookup"><span data-stu-id="6004b-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="6004b-106">En avsändare begär återkallande.</span><span class="sxs-lookup"><span data-stu-id="6004b-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="6004b-107">En godkännare godkänner återkallningen.</span><span class="sxs-lookup"><span data-stu-id="6004b-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="6004b-108">Begär en återkallelse</span><span class="sxs-lookup"><span data-stu-id="6004b-108">Request a recall</span></span>

<span data-ttu-id="6004b-109">Följ stegen nedan om du vill begära en återkallelse för en godkänd tids- eller utgiftstransaktion.</span><span class="sxs-lookup"><span data-stu-id="6004b-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="6004b-110">För tidsposter går du till **projekt** \> **mitt arbete** \> **tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="6004b-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="6004b-111">–eller–</span><span class="sxs-lookup"><span data-stu-id="6004b-111">–or–</span></span>

    <span data-ttu-id="6004b-112">För utgiftsposter går du till **projekt** \> **mitt arbete** \> **utgifter**.</span><span class="sxs-lookup"><span data-stu-id="6004b-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="6004b-113">För tidsposter, välj alla tidposter för en specifik kombination av ett projekt och en uppgift.</span><span class="sxs-lookup"><span data-stu-id="6004b-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="6004b-114">I rutnätet kan du också välja enskilda celler för tid på ett visst datum för ett visst projekt.</span><span class="sxs-lookup"><span data-stu-id="6004b-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="6004b-115">–eller–</span><span class="sxs-lookup"><span data-stu-id="6004b-115">–or–</span></span>

    <span data-ttu-id="6004b-116">För utgiftsposter markerar du raden för den utgiftspost du vill återkalla.</span><span class="sxs-lookup"><span data-stu-id="6004b-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="6004b-117">Välj **återkalla**.</span><span class="sxs-lookup"><span data-stu-id="6004b-117">Select **Recall**.</span></span> <span data-ttu-id="6004b-118">En dialogruta för bekräftelse visas.</span><span class="sxs-lookup"><span data-stu-id="6004b-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="6004b-119">Om de valda tids- och utgiftsposterna redan har godkänts uppmanas du att ange ett skäl till att återkalla det.</span><span class="sxs-lookup"><span data-stu-id="6004b-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="6004b-120">Ange ett skäl till återkallningen och klicka sedan på **OK** för att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6004b-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="6004b-121">Systemet skickar personen som godkände posterna en förfrågan om att godkänna återkallandet.</span><span class="sxs-lookup"><span data-stu-id="6004b-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="6004b-122">Även om godkända tids- och utgiftsposter kan återkallas, om en godkänd tid eller utgift redan har fakturerats till kunden, kan en återkallningsbegäran inte skapas.</span><span class="sxs-lookup"><span data-stu-id="6004b-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="6004b-123">En användare som försöker skapa en återkallningsbegäran får ett meddelande om att tiden eller kostnaden inte kan återkallas eftersom den redan har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="6004b-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="6004b-124">Godkänna eller avvisa en återkallningsbegäran</span><span class="sxs-lookup"><span data-stu-id="6004b-124">Approve or reject a recall request</span></span>

<span data-ttu-id="6004b-125">Följ stegen nedan om du vill godkänna eller avvisa en återkallningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="6004b-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="6004b-126">Gå till **Projekt** \> **Mitt arbete** \> **Godkännanden**.</span><span class="sxs-lookup"><span data-stu-id="6004b-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="6004b-127">På listsidan **godkännanden** ändrar du vyn till **återkallningsbegäran för godkännande**.</span><span class="sxs-lookup"><span data-stu-id="6004b-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="6004b-128">En lista med skickade återkallningsbegäran visas.</span><span class="sxs-lookup"><span data-stu-id="6004b-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="6004b-129">Markera en eller flera poster och välj sedan antingen **Godkänn** eller **Avvisa**.</span><span class="sxs-lookup"><span data-stu-id="6004b-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="6004b-130">Om du valde **Godkänn** visas ett varningsmeddelande som förklarar hur godkännandet har påverkats.</span><span class="sxs-lookup"><span data-stu-id="6004b-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="6004b-131">Bekräfta åtgärden genom att välja **OK**.</span><span class="sxs-lookup"><span data-stu-id="6004b-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="6004b-132">Återkallningsbegäran är godkänd.</span><span class="sxs-lookup"><span data-stu-id="6004b-132">The recall request is approved.</span></span>

    <span data-ttu-id="6004b-133">–eller–</span><span class="sxs-lookup"><span data-stu-id="6004b-133">–or–</span></span>

    <span data-ttu-id="6004b-134">Om du valde **avvisa** kommer återkallningsbegäran att avvisas.</span><span class="sxs-lookup"><span data-stu-id="6004b-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="6004b-135">När ett återkallande begärs, när ett återkallande godkänns kontrollerar systemet om det finns någon faktureringsaktivitet för tids- eller utgiftsposterna.</span><span class="sxs-lookup"><span data-stu-id="6004b-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="6004b-136">Om en post redan har fakturerats eller om den är på en utkastfaktura får godkännaren ett fel meddelande om att tiden eller kostnaden inte kan godkännas för återkallande eftersom den redan har fakturerats.</span><span class="sxs-lookup"><span data-stu-id="6004b-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="6004b-137">Hur en återkallningsbegäran påverkas</span><span class="sxs-lookup"><span data-stu-id="6004b-137">Impact of a recall request</span></span>

<span data-ttu-id="6004b-138">När ett godkännande återkallas finns det både driftseffekter och ekonomiska effekter.</span><span class="sxs-lookup"><span data-stu-id="6004b-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="6004b-139">Driftseffekter</span><span class="sxs-lookup"><span data-stu-id="6004b-139">Operational impact</span></span>

<span data-ttu-id="6004b-140">Om en återkallningsbegäran har godkänts markeras godkännandeposten som **avvisad**.</span><span class="sxs-lookup"><span data-stu-id="6004b-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="6004b-141">Status för transaktionen ändras till antingen **returnerad** eller **avvisad** beroende på om det är en tids- eller utgiftspost.</span><span class="sxs-lookup"><span data-stu-id="6004b-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="6004b-142">Projektteammedlemmen kan visa poster, redigera och skicka om poster eller endast ta bort poster.</span><span class="sxs-lookup"><span data-stu-id="6004b-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="6004b-143">Om en återkallningsbegäran förblir **godkänd** och posten inte kan redigeras av projektteammedlemmen eller godkännaren för projektet.</span><span class="sxs-lookup"><span data-stu-id="6004b-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="6004b-144">Finansiella effekter</span><span class="sxs-lookup"><span data-stu-id="6004b-144">Financial impact</span></span>

<span data-ttu-id="6004b-145">Om en återkallningsbegäran godkänns kommer motsvarande verkliga värden för kostnader och försäljning på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="6004b-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="6004b-146">Fältet **Justeringsstatus** uppdateras till **Justerad**.</span><span class="sxs-lookup"><span data-stu-id="6004b-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="6004b-147">Fältet **Faktureringsstatus** uppdateras till **Annullerad**.</span><span class="sxs-lookup"><span data-stu-id="6004b-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="6004b-148">Sedan skapas återföringsposter i tabellen faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="6004b-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="6004b-149">Om du vill skapa återföringsposter kopieras systemet över fältvärdena från de ursprungliga värdena.</span><span class="sxs-lookup"><span data-stu-id="6004b-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="6004b-150">De enda värden som inte kopieras över är antalet värden.</span><span class="sxs-lookup"><span data-stu-id="6004b-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="6004b-151">De här värdena återförs i stället.</span><span class="sxs-lookup"><span data-stu-id="6004b-151">These values are reversed instead.</span></span> <span data-ttu-id="6004b-152">Återförda faktiska värden skapas både för **kostnad** och för **fakturerade försäljningsvärden**.</span><span class="sxs-lookup"><span data-stu-id="6004b-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="6004b-153">Fältet **justeringsstatus** på de återförda verkliga värdena ställs till att värdet **inte justerat** och fält **faktureringsstatus** är **annullerad**.</span><span class="sxs-lookup"><span data-stu-id="6004b-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="6004b-154">På grund av dessa ändringar tar de registrerade utgifterna och den totala förväntande omsättningen kommer inte längre att räknas för de belopp som dessa faktiska värden representerar.</span><span class="sxs-lookup"><span data-stu-id="6004b-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="6004b-155">Om en återkallningsbegäran avslås påverkas inte projektets ekonomiska påverkan.</span><span class="sxs-lookup"><span data-stu-id="6004b-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="6004b-156">Ändringar i tidsposter</span><span class="sxs-lookup"><span data-stu-id="6004b-156">Changes to time entry records</span></span>

<span data-ttu-id="6004b-157">Följande illustration visar de ändringar som inträffar för godkända tidsposter när de återkallas.</span><span class="sxs-lookup"><span data-stu-id="6004b-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Tidpostens tillståndsövergångar](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="6004b-159">Ändringar i utgiftsposter</span><span class="sxs-lookup"><span data-stu-id="6004b-159">Changes to expense entry records</span></span>

<span data-ttu-id="6004b-160">Följande illustration visar de ändringar som inträffar för godkända utgiftsposter när de återkallas.</span><span class="sxs-lookup"><span data-stu-id="6004b-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Utgiftspostens tillståndsövergångar](media/ExpenseEntryStateTransitions.png)
