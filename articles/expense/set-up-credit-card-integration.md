---
title: Konfigurera kreditkortsintegration
description: Den ämne förklarar hur du arbetar med utgiftsrelaterade kreditkortstransaktioner.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001852"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="50fba-103">Konfigurera kreditkortsintegration</span><span class="sxs-lookup"><span data-stu-id="50fba-103">Set up credit card integration</span></span>

<span data-ttu-id="50fba-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="50fba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50fba-105">Utgift som är relaterade kreditkortstransaktioner kan ställas in så att de importeras automatiskt i ett återkommande schema.</span><span class="sxs-lookup"><span data-stu-id="50fba-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="50fba-106">Transaktionerna kan också importeras manuellt när de krävs.</span><span class="sxs-lookup"><span data-stu-id="50fba-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="50fba-107">Kreditkortstransaktionerna importeras via dataentiteten för kreditkortstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="50fba-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="50fba-108">Importera kreditkortstransaktioner</span><span class="sxs-lookup"><span data-stu-id="50fba-108">Import credit card transactions</span></span>

<span data-ttu-id="50fba-109">Importera kreditkortstransaktioner genom att följa stegen nedan:</span><span class="sxs-lookup"><span data-stu-id="50fba-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="50fba-110">På sidan **Kreditkortstransaktioner** väljer du **importera transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="50fba-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="50fba-111">Om du öppnar datahantering för första gången måste du uppdatera listan med dataentiteter i systemet innan du kan fortsätta.</span><span class="sxs-lookup"><span data-stu-id="50fba-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="50fba-112">I fältet **Namn** ange en unik beskrivning för importjobbet.</span><span class="sxs-lookup"><span data-stu-id="50fba-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="50fba-113">I fältet **Källdataformat** väljer du formatet för den fil som innehåller de kreditkortstransaktioner som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="50fba-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="50fba-114">Välj **överför** välj sedan den fil du vill importera.</span><span class="sxs-lookup"><span data-stu-id="50fba-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="50fba-115">När filen har överförts kontrollerar du mappningen av kreditkortstransaktionsfilen och kolumnerna i dataentiteten för kreditkortstransaktioner genom att välja länken **Visa karta** på panelen.</span><span class="sxs-lookup"><span data-stu-id="50fba-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="50fba-116">Om det uppstår mappningsfel eller om du måste ändra mappningen gör du mappningsändringarna antingen från fliken **Mappningsvisualisering** eller **Mappningsinformation**.</span><span class="sxs-lookup"><span data-stu-id="50fba-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="50fba-117">Om du vill automatisera kreditkortstransaktionerna väljer du **Skapa återkommande datajobb**.</span><span class="sxs-lookup"><span data-stu-id="50fba-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="50fba-118">Du kan ange en återkommande tid som anger hur ofta kreditkortstransaktioner ska importeras.</span><span class="sxs-lookup"><span data-stu-id="50fba-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="50fba-119">När du är klar väljer du **OK**.</span><span class="sxs-lookup"><span data-stu-id="50fba-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="50fba-120">Välj importera om du vill importera den valda filen nu **Import**.</span><span class="sxs-lookup"><span data-stu-id="50fba-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="50fba-121">Om det uppstår fel under importen kan du visa körningsloggen eller testdata och se vilka fel du måste åtgärda för att importen ska lyckas.</span><span class="sxs-lookup"><span data-stu-id="50fba-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="50fba-122">Om du måste importera fler än ett filformat måste du skapa separata importjobb för varje formattyp.</span><span class="sxs-lookup"><span data-stu-id="50fba-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="50fba-123">Tilldela om kreditkortstransaktionerna för avslutade medarbetare</span><span class="sxs-lookup"><span data-stu-id="50fba-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="50fba-124">När en anställds post har avslutats inaktiveras den anställdes konto Active Directory Domain Services (AD DS) är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="50fba-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="50fba-125">Det kan dock finnas aktiva kreditkortstransaktioner som fortfarande måste vara utgifter och ersättas.</span><span class="sxs-lookup"><span data-stu-id="50fba-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="50fba-126">På sidan **Kreditkortstransaktioner** kan du tilldela om den anställde för alla kreditkortstransaktioner där den associerade medarbetaren har avslutats.</span><span class="sxs-lookup"><span data-stu-id="50fba-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="50fba-127">Välj en eller flera kreditkortstransaktioner och välj sedan **tilldela om transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="50fba-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="50fba-128">Du kan sedan välja en annan medarbetare att tilldela kreditkortstransaktionerna till.</span><span class="sxs-lookup"><span data-stu-id="50fba-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="50fba-129">När kreditkortstransaktionerna har omtilldelats kan de väljas för en utgiftsrapport och betalas i den normala processen för återbetalning av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="50fba-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="50fba-130">Ta bort kreditkortstransaktioner</span><span class="sxs-lookup"><span data-stu-id="50fba-130">Delete credit card transactions</span></span> 

<span data-ttu-id="50fba-131">Ibland, efter att kreditkortstransaktioner har importerats, kan vissa transaktioner behöva raderas.</span><span class="sxs-lookup"><span data-stu-id="50fba-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="50fba-132">Det kan beror på att transaktionerna är dubbletter eller på att data kanske inte är korrekta.</span><span class="sxs-lookup"><span data-stu-id="50fba-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="50fba-133">Administratörer kan använda funktionen **"Ta bort kreditkortstransaktioner"** för att välja och ta bort kreditkortstransaktioner som **inte är bifogad** till en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="50fba-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="50fba-134">Gå till **Periodiska uppgifter** > **Ta bort kreditkortstransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="50fba-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="50fba-135">Välj **Filter** och tillhandahåll information om vilka poster som ska ingå.</span><span class="sxs-lookup"><span data-stu-id="50fba-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="50fba-136">Välj **OK** för att ta bort posterna.</span><span class="sxs-lookup"><span data-stu-id="50fba-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
