---
title: Avbryt tidigare godkända tids- och utgiftsposter
description: I det här ämnet finns information om hur du avbryter en godkänd projekttid och utgiftstransaktion.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf3d146d2b07723b4d2e6e85eafd6f1b23b8b83f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014768"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="7e867-103">Avbryt tidigare godkända tids- eller utgiftsposter</span><span class="sxs-lookup"><span data-stu-id="7e867-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7e867-104">I den senaste versionen av Dynamics 365 Project Service Automation kan godkännare annullera tids- eller utgiftsposter som de tidigare har godkänt.</span><span class="sxs-lookup"><span data-stu-id="7e867-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="7e867-105">Avbryt en tidigare godkänd tids- eller utgiftspost</span><span class="sxs-lookup"><span data-stu-id="7e867-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="7e867-106">Följ stegen nedan om du vill avbryta en tids- eller utgiftstransaktion som du tidigare godkänt.</span><span class="sxs-lookup"><span data-stu-id="7e867-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="7e867-107">Gå till **Projekt** \> **Mitt arbete** \> **Godkännanden**.</span><span class="sxs-lookup"><span data-stu-id="7e867-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="7e867-108">På listsidan **godkännanden** ändrar du vyn till **mina tidigare godkännanden**.</span><span class="sxs-lookup"><span data-stu-id="7e867-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="7e867-109">En lista över de tids- och utgiftstransaktioner som du tidigare godkänt visas.</span><span class="sxs-lookup"><span data-stu-id="7e867-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="7e867-110">Markera en eller flera poster och välj sedan **Avbryt godkännande**.</span><span class="sxs-lookup"><span data-stu-id="7e867-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="7e867-111">Ett varningsmeddelande visas.</span><span class="sxs-lookup"><span data-stu-id="7e867-111">You receive a warning message.</span></span>
4. <span data-ttu-id="7e867-112">Välj **OK** för att avbryta godkännandet.</span><span class="sxs-lookup"><span data-stu-id="7e867-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="7e867-113">Ta reda på hur du avbryter ett godkännande av tids- eller utgiftspost</span><span class="sxs-lookup"><span data-stu-id="7e867-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="7e867-114">När ett godkännande har annullerats finns det både driftseffekter och ekonomiska effekter.</span><span class="sxs-lookup"><span data-stu-id="7e867-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="7e867-115">Driftseffekter</span><span class="sxs-lookup"><span data-stu-id="7e867-115">Operational impact</span></span>

<span data-ttu-id="7e867-116">På driftssidan återställs statusen för posten när ett godkännande avbryts **Utkast** och godkännandet visas inte längre i vyn **Mina senaste godkännanden**.</span><span class="sxs-lookup"><span data-stu-id="7e867-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="7e867-117">I stället visas det annullerade godkännandet i antingen vyn **Tidsposter för godkännande** eller vyn **Utgiftsposter för godkännande** beroende på om det är en tidspost eller en utgiftspost.</span><span class="sxs-lookup"><span data-stu-id="7e867-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="7e867-118">Dessutom ändras statusen för den relaterade tids- eller utgiftsposten till **skickad** så att den relaterade posten överensstämmer med godkännanden som har statusen **utkast**.</span><span class="sxs-lookup"><span data-stu-id="7e867-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="7e867-119">Som godkännare kan du redigera en del av fälten för ett godkännande som har statusen **utkast**.</span><span class="sxs-lookup"><span data-stu-id="7e867-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="7e867-120">Dessa fält inkluderar **faktureringstyp** och **fakturerbara timmar för tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="7e867-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="7e867-121">När du har gjort ändringar kan du godkänna posten igen.</span><span class="sxs-lookup"><span data-stu-id="7e867-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="7e867-122">Alternativt kan du avvisa transaktionen.</span><span class="sxs-lookup"><span data-stu-id="7e867-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="7e867-123">Om du avvisar godkännandet av en tidspost ändras transaktionens status till **returnerad**.</span><span class="sxs-lookup"><span data-stu-id="7e867-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="7e867-124">Om du avvisar godkännandet av en utgiftspost ändras transaktionens status till **Avvisad**.</span><span class="sxs-lookup"><span data-stu-id="7e867-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="7e867-125">Funktionen returnerade och avvisade poster fungerar på samma sätt som en post som har statusen **utkast**.</span><span class="sxs-lookup"><span data-stu-id="7e867-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="7e867-126">En projektgruppmedlem kan antingen göra nödvändiga ändringar i transaktionen och sedan skicka den på nytt för godkännande, eller ta bort posten helt.</span><span class="sxs-lookup"><span data-stu-id="7e867-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="7e867-127">Finansiella effekter</span><span class="sxs-lookup"><span data-stu-id="7e867-127">Financial impact</span></span>

<span data-ttu-id="7e867-128">Ett projekt påverkas också ekonomiskt när ett godkännande annulleras.</span><span class="sxs-lookup"><span data-stu-id="7e867-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="7e867-129">Först uppdateras motsvarande verkliga värden för kostnader och försäljning på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="7e867-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="7e867-130">Justeringsstatus är inställd på **justerad**.</span><span class="sxs-lookup"><span data-stu-id="7e867-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="7e867-131">Faktureringsstatus är inställd på **Avbrutet**.</span><span class="sxs-lookup"><span data-stu-id="7e867-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="7e867-132">Sedan skapas återföringsposter i tabellen faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="7e867-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="7e867-133">Om du vill skapa återföringsposter kopieras systemet över fältvärdena från de ursprungliga värdena.</span><span class="sxs-lookup"><span data-stu-id="7e867-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="7e867-134">De enda värden som inte kopieras över är antalet värden.</span><span class="sxs-lookup"><span data-stu-id="7e867-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="7e867-135">De här värdena återförs i stället.</span><span class="sxs-lookup"><span data-stu-id="7e867-135">These values are reversed instead.</span></span> <span data-ttu-id="7e867-136">Återförda faktiska värden skapas både för **kostnad** och för **fakturerade försäljningsvärden**.</span><span class="sxs-lookup"><span data-stu-id="7e867-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="7e867-137">Fältet **justeringsstatus** på de återförda verkliga värdena ställs till att värdet **inte justerat** och faktureringsstatus är **annullerad**.</span><span class="sxs-lookup"><span data-stu-id="7e867-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="7e867-138">När ändringarna har gjorts bokförs det belopp som har registrerats som förbrukat i projektet och den totala förväntande omsättningen i projektet tar längre tid för de belopp som dessa faktiska värden representerar.</span><span class="sxs-lookup"><span data-stu-id="7e867-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]