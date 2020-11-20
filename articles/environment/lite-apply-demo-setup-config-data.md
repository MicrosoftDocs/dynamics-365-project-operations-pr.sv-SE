---
title: Använda demoinställning och konfigurationsdata – Lite
description: I det här ämnet finns information om hur du tillämpar demoinställning konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401285"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f5e17-103">Använda demoinställning och konfigurationsdata Project Operations - Lite</span><span class="sxs-lookup"><span data-stu-id="f5e17-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f5e17-104">_\*\*Lite-distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="f5e17-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f5e17-105">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="f5e17-105">Prerequisites</span></span>

<span data-ttu-id="f5e17-106">Innan du påbörjar konfigurationen måste du ha installerat en Common Data Service (CDS)-miljö för Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f5e17-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f5e17-107">Anvisningar</span><span class="sxs-lookup"><span data-stu-id="f5e17-107">Instructions</span></span>

1. <span data-ttu-id="f5e17-108">Hämta [Huvuddatapaketet](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="f5e17-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="f5e17-109">Navigera till mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT* och kör den körbara filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f5e17-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f5e17-110">På sidan 1 i guiden Common Data Service konfigurationsmigrering (CMT) väljer du **Importera data** och sedan **Fortsätt**.</span><span class="sxs-lookup"><span data-stu-id="f5e17-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigrering](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f5e17-112">På sidan 2 i guiden CMT väljer du **Microsoft 365** som **Distributionstyp**.</span><span class="sxs-lookup"><span data-stu-id="f5e17-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f5e17-113">Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.</span><span class="sxs-lookup"><span data-stu-id="f5e17-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f5e17-114">Välj region för klientorganisationen, ange autentiseringsuppgifter och välj sedan **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="f5e17-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f5e17-116">På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer sedan **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="f5e17-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f5e17-117">På sidan 4 väljer du zip-filen *MasterAndSetupData* från den uppackade mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT*.</span><span class="sxs-lookup"><span data-stu-id="f5e17-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="f5e17-120">När du har markerat zip-filen väljer du **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="f5e17-120">After the zip file is selected, select **Import Data**.</span></span>

![Importera data](./media/5ImportData.png)

10. <span data-ttu-id="f5e17-122">Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet.</span><span class="sxs-lookup"><span data-stu-id="f5e17-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f5e17-123">När den är klar stänger du guiden för CMT.</span><span class="sxs-lookup"><span data-stu-id="f5e17-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f5e17-124">Kontrollera om organisationen har data i följande 20 entiteter:</span><span class="sxs-lookup"><span data-stu-id="f5e17-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="f5e17-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="f5e17-125">Currency</span></span>
-   <span data-ttu-id="f5e17-126">Konto</span><span class="sxs-lookup"><span data-stu-id="f5e17-126">Account</span></span>
-   <span data-ttu-id="f5e17-127">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="f5e17-127">Organizational Unit</span></span>
-   <span data-ttu-id="f5e17-128">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f5e17-128">Contact</span></span>
-   <span data-ttu-id="f5e17-129">Momsgrupp</span><span class="sxs-lookup"><span data-stu-id="f5e17-129">Tax Group</span></span>
-   <span data-ttu-id="f5e17-130">Kundgrupp</span><span class="sxs-lookup"><span data-stu-id="f5e17-130">Customer Group</span></span>
-   <span data-ttu-id="f5e17-131">Enhet</span><span class="sxs-lookup"><span data-stu-id="f5e17-131">Unit</span></span>
-   <span data-ttu-id="f5e17-132">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="f5e17-132">Unit Group</span></span>
-   <span data-ttu-id="f5e17-133">Prislista</span><span class="sxs-lookup"><span data-stu-id="f5e17-133">Price List</span></span>
-   <span data-ttu-id="f5e17-134">Prislista för projektparameter</span><span class="sxs-lookup"><span data-stu-id="f5e17-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="f5e17-135">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="f5e17-135">Invoice Frequency</span></span>
-   <span data-ttu-id="f5e17-136">Bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="f5e17-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="f5e17-137">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="f5e17-137">Transaction Category</span></span>
-   <span data-ttu-id="f5e17-138">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="f5e17-138">Expense Category</span></span>
-   <span data-ttu-id="f5e17-139">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="f5e17-139">Role Price</span></span>
-   <span data-ttu-id="f5e17-140">Pris för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="f5e17-140">Transaction Category Price</span></span>
-   <span data-ttu-id="f5e17-141">Egenskap</span><span class="sxs-lookup"><span data-stu-id="f5e17-141">Characteristic</span></span>
-   <span data-ttu-id="f5e17-142">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="f5e17-142">Bookable Resource</span></span>
-   <span data-ttu-id="f5e17-143">Association för bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="f5e17-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="f5e17-144">Egenskap för bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="f5e17-144">Bookable Resource Characteristic</span></span>

![Slutför import](./media/6CompleteImport.png)
