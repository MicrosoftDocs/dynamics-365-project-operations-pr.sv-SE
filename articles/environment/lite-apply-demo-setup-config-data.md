---
title: Använda demoinställning och konfigurationsdata
description: I det här ämnet finns information om hur du tillämpar demoinställning konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949097"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="15c21-103">Använd demoinställning och konfigurationsdata för Project Operations lite-distributionen – avtal till proforma-fakturering</span><span class="sxs-lookup"><span data-stu-id="15c21-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="15c21-104">_\*\*Lite-distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="15c21-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="15c21-105">Hämta [Huvuddatapaketet](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="15c21-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="15c21-106">Navigera till mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT* och kör den körbara filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="15c21-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="15c21-107">På sidan 1 i guiden Common Data Service konfigurationsmigrering (CMT) väljer du **Importera data** och sedan **Fortsätt**.</span><span class="sxs-lookup"><span data-stu-id="15c21-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigrering](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="15c21-109">På sidan 2 i guiden CMT väljer du **Office 365** som **Distributionstyp**.</span><span class="sxs-lookup"><span data-stu-id="15c21-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="15c21-110">Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.</span><span class="sxs-lookup"><span data-stu-id="15c21-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="15c21-111">Välj region för klientorganisationen, ange autentiseringsuppgifter och välj sedan **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="15c21-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="15c21-113">På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer sedan **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="15c21-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="15c21-114">På sidan 4 väljer du zip-filen *MasterAndSetupData* från den uppackade mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT*.</span><span class="sxs-lookup"><span data-stu-id="15c21-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="15c21-117">När du har markerat zip-filen väljer du **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="15c21-117">After the zip file is selected, select **Import Data**.</span></span>

![Importera data](./media/5ImportData.png)

10. <span data-ttu-id="15c21-119">Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet.</span><span class="sxs-lookup"><span data-stu-id="15c21-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="15c21-120">När den är klar stänger du guiden för CMT.</span><span class="sxs-lookup"><span data-stu-id="15c21-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="15c21-121">Kontrollera om organisationen har data i följande 20 entiteter:</span><span class="sxs-lookup"><span data-stu-id="15c21-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="15c21-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="15c21-122">Currency</span></span>
- <span data-ttu-id="15c21-123">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="15c21-123">Organizational Unit</span></span>
- <span data-ttu-id="15c21-124">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="15c21-124">Contact</span></span>
- <span data-ttu-id="15c21-125">Momsgrupp</span><span class="sxs-lookup"><span data-stu-id="15c21-125">Tax Group</span></span>
- <span data-ttu-id="15c21-126">Kundgrupp</span><span class="sxs-lookup"><span data-stu-id="15c21-126">Customer Group</span></span>
- <span data-ttu-id="15c21-127">Enhet</span><span class="sxs-lookup"><span data-stu-id="15c21-127">Unit</span></span>
- <span data-ttu-id="15c21-128">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="15c21-128">Unit Group</span></span>
- <span data-ttu-id="15c21-129">Prislista</span><span class="sxs-lookup"><span data-stu-id="15c21-129">Price List</span></span>
- <span data-ttu-id="15c21-130">Prislista för projektparameter</span><span class="sxs-lookup"><span data-stu-id="15c21-130">Project Parameter Price List</span></span>
- <span data-ttu-id="15c21-131">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="15c21-131">Invoice Frequency</span></span>
- <span data-ttu-id="15c21-132">Information om faktureringsfrekvens</span><span class="sxs-lookup"><span data-stu-id="15c21-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="15c21-133">Bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="15c21-133">Bookable Resource Category</span></span>
- <span data-ttu-id="15c21-134">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="15c21-134">Transaction Category</span></span>
- <span data-ttu-id="15c21-135">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="15c21-135">Expense Category</span></span>
- <span data-ttu-id="15c21-136">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="15c21-136">Role Price</span></span>
- <span data-ttu-id="15c21-137">Pris för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="15c21-137">Transaction Category Price</span></span>
- <span data-ttu-id="15c21-138">Egenskap</span><span class="sxs-lookup"><span data-stu-id="15c21-138">Characteristic</span></span>
- <span data-ttu-id="15c21-139">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="15c21-139">Bookable Resource</span></span>
- <span data-ttu-id="15c21-140">Association för bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="15c21-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="15c21-141">Egenskap för bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="15c21-141">Bookable Resource Characteristic</span></span>

![Slutför import](./media/6CompleteImport.png)
