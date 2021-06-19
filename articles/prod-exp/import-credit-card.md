---
title: Importera och underhåll kreditkortstransaktioner
description: I det här ämnet beskrivs hur du importerar och underhåller utgifter för kreditkortstransaktioner. Dessa transaktioner kan ställas in så att de importeras automatiskt till ett återkommande schema, eller så kan de importeras manuellt efter behov.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005183"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="4e017-104">Importera och underhåll kreditkortstransaktioner</span><span class="sxs-lookup"><span data-stu-id="4e017-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="4e017-105">Utgift som är relaterade kreditkortstransaktioner kan ställas in så att de importeras automatiskt i ett återkommande schema.</span><span class="sxs-lookup"><span data-stu-id="4e017-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="4e017-106">Transaktionerna kan också importeras manuellt när de krävs.</span><span class="sxs-lookup"><span data-stu-id="4e017-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="4e017-107">Kreditkortstransaktionerna importeras via dataentiteten för kreditkortstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="4e017-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="4e017-108">Mer information om dataentiteter finns i [Dataentiteter](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="4e017-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="4e017-109">Importera kreditkortstransaktioner</span><span class="sxs-lookup"><span data-stu-id="4e017-109">Import credit card transactions</span></span>

1. <span data-ttu-id="4e017-110">På sidan **Kreditkortstransaktioner** väljer du **importera transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="4e017-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="4e017-111">Om du öppnar datahantering för första gången måste du uppdatera listan med dataentiteter i systemet innan du kan fortsätta.</span><span class="sxs-lookup"><span data-stu-id="4e017-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="4e017-112">I fältet **Namn** ange en unik beskrivning av import jobbet.</span><span class="sxs-lookup"><span data-stu-id="4e017-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="4e017-113">I fältet **Källdataformat** väljer du formatet för den fil som innehåller de kreditkortstransaktioner som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="4e017-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="4e017-114">Välj **överför** välj sedan den fil du vill importera.</span><span class="sxs-lookup"><span data-stu-id="4e017-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="4e017-115">När filen har överförts kontrollerar du mappningen av kreditkortstransaktionsfilen och kolumnerna i dataentiteten för kreditkortstransaktioner genom att välja länken **Visa karta** på panelen.</span><span class="sxs-lookup"><span data-stu-id="4e017-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="4e017-116">Om det uppstår mappningsfel eller om du måste ändra mappningen gör du mappningsändringarna antingen från fliken **Mappningsvisualisering** eller **Mappningsinformation**.</span><span class="sxs-lookup"><span data-stu-id="4e017-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="4e017-117">Om du vill automatisera kreditkortstransaktionerna väljer du **Skapa återkommande datajobb**.</span><span class="sxs-lookup"><span data-stu-id="4e017-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="4e017-118">Du kan ange en återkommande tid som anger hur ofta kreditkortstransaktioner ska importeras.</span><span class="sxs-lookup"><span data-stu-id="4e017-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="4e017-119">När du är klar väljer du **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e017-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="4e017-120">Välj importera om du vill importera den valda filen nu **Import**.</span><span class="sxs-lookup"><span data-stu-id="4e017-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="4e017-121">Om det uppstår fel under importen kan du visa körningsloggen eller mellanlagringsmappen för att se de fel du måste åtgärda för att kunna garantera en lyckad import.</span><span class="sxs-lookup"><span data-stu-id="4e017-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="4e017-122">Om du måste importera fler än ett fil format måste du skapa separata importjobb för varje formattyp.</span><span class="sxs-lookup"><span data-stu-id="4e017-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="4e017-123">Tilldela om kreditkortstransaktionerna för avslutade medarbetare</span><span class="sxs-lookup"><span data-stu-id="4e017-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="4e017-124">När en anställds post har avslutats inaktiveras den anställdes konto Active Directory Domain Services (AD DS) är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="4e017-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="4e017-125">Det kan dock finnas aktiva kreditkortstransaktioner som fortfarande måste vara utgifter och ersättas.</span><span class="sxs-lookup"><span data-stu-id="4e017-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="4e017-126">På sidan **Kreditkortstransaktioner** kan du omtilldela medarbetaren för en kreditkortstransaktion där den associerade medarbetaren har avslutas.</span><span class="sxs-lookup"><span data-stu-id="4e017-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="4e017-127">Välj en eller flera kreditkortstransaktioner och välj sedan **tilldela om transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="4e017-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="4e017-128">Du kan sedan välja en annan medarbetare att tilldela kreditkortstransaktionerna till.</span><span class="sxs-lookup"><span data-stu-id="4e017-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="4e017-129">När kreditkortstransaktionerna har omtilldelats kan de väljas för en utgiftsrapport och betalas i den normala processen för återbetalning av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="4e017-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]