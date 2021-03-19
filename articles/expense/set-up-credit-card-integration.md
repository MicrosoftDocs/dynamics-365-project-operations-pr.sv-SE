---
title: Konfigurera kreditkortsintegration
description: I det här ämnet beskrivs hur du importerar och underhåller utgifter för kreditkortstransaktioner.
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
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276190"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="9e29b-103">Konfigurera kreditkortsintegration</span><span class="sxs-lookup"><span data-stu-id="9e29b-103">Set up credit card integration</span></span>

<span data-ttu-id="9e29b-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="9e29b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e29b-105">Utgift som är relaterade kreditkortstransaktioner kan ställas in så att de importeras automatiskt i ett återkommande schema.</span><span class="sxs-lookup"><span data-stu-id="9e29b-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="9e29b-106">Transaktionerna kan också importeras manuellt när de krävs.</span><span class="sxs-lookup"><span data-stu-id="9e29b-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="9e29b-107">Kreditkortstransaktionerna importeras via dataentiteten för kreditkortstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="9e29b-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="9e29b-108">Importera kreditkortstransaktioner</span><span class="sxs-lookup"><span data-stu-id="9e29b-108">Import credit card transactions</span></span>

1. <span data-ttu-id="9e29b-109">På sidan **Kreditkortstransaktioner** väljer du **importera transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="9e29b-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="9e29b-110">Om du öppnar datahantering för första gången måste du uppdatera listan med dataentiteter i systemet innan du kan fortsätta.</span><span class="sxs-lookup"><span data-stu-id="9e29b-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="9e29b-111">I fältet **Namn** ange en unik beskrivning av import jobbet.</span><span class="sxs-lookup"><span data-stu-id="9e29b-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="9e29b-112">I fältet **Källdataformat** väljer du formatet för den fil som innehåller de kreditkortstransaktioner som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="9e29b-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="9e29b-113">Välj **överför** välj sedan den fil du vill importera.</span><span class="sxs-lookup"><span data-stu-id="9e29b-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="9e29b-114">När filen har överförts kontrollerar du mappningen av kreditkortstransaktionsfilen och kolumnerna i dataentiteten för kreditkortstransaktioner genom att välja länken **Visa karta** på panelen.</span><span class="sxs-lookup"><span data-stu-id="9e29b-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="9e29b-115">Om det uppstår mappningsfel eller om du måste ändra mappningen gör du mappningsändringarna antingen från fliken **Mappningsvisualisering** eller **Mappningsinformation**.</span><span class="sxs-lookup"><span data-stu-id="9e29b-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="9e29b-116">Om du vill automatisera kreditkortstransaktionerna väljer du **Skapa återkommande datajobb**.</span><span class="sxs-lookup"><span data-stu-id="9e29b-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="9e29b-117">Du kan ange en återkommande tid som anger hur ofta kreditkortstransaktioner ska importeras.</span><span class="sxs-lookup"><span data-stu-id="9e29b-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="9e29b-118">När du är klar väljer du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e29b-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="9e29b-119">Välj importera om du vill importera den valda filen nu **Import**.</span><span class="sxs-lookup"><span data-stu-id="9e29b-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="9e29b-120">Om det uppstår fel under importen kan du visa körningsloggen eller mellanlagringsmappen för att se de fel du måste åtgärda för att kunna garantera en lyckad import.</span><span class="sxs-lookup"><span data-stu-id="9e29b-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="9e29b-121">Om du måste importera fler än ett fil format måste du skapa separata importjobb för varje formattyp.</span><span class="sxs-lookup"><span data-stu-id="9e29b-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="9e29b-122">Tilldela om kreditkortstransaktionerna för avslutade medarbetare</span><span class="sxs-lookup"><span data-stu-id="9e29b-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="9e29b-123">När en anställds post har avslutats inaktiveras den anställdes konto Active Directory Domain Services (AD DS) är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="9e29b-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="9e29b-124">Det kan dock finnas aktiva kreditkortstransaktioner som fortfarande måste vara utgifter och ersättas.</span><span class="sxs-lookup"><span data-stu-id="9e29b-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="9e29b-125">På sidan **Kreditkortstransaktioner** kan du omtilldela medarbetaren för en kreditkortstransaktion där den associerade medarbetaren har avslutas.</span><span class="sxs-lookup"><span data-stu-id="9e29b-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="9e29b-126">Välj en eller flera kreditkortstransaktioner och välj sedan **tilldela om transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="9e29b-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="9e29b-127">Du kan sedan välja en annan medarbetare att tilldela kreditkortstransaktionerna till.</span><span class="sxs-lookup"><span data-stu-id="9e29b-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="9e29b-128">När kreditkortstransaktionerna har omtilldelats kan de väljas för en utgiftsrapport och betalas i den normala processen för återbetalning av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="9e29b-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]