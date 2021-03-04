---
title: Använda demoinställning och konfigurationsdata – Lite
description: I det här ämnet finns information om hur du tillämpar demoinställning konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089141"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f4f34-103">Använda demoinställning och konfigurationsdata Project Operations - Lite</span><span class="sxs-lookup"><span data-stu-id="f4f34-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f4f34-104">_\*\*Lite-distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="f4f34-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f4f34-105">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="f4f34-105">Prerequisites</span></span>

<span data-ttu-id="f4f34-106">Innan du påbörjar konfigurationen måste du ha installerat en Common Data Service (CDS)-miljö för Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f4f34-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f4f34-107">Anvisningar</span><span class="sxs-lookup"><span data-stu-id="f4f34-107">Instructions</span></span>

1. <span data-ttu-id="f4f34-108">Hämta [Huvuddatapaketet](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="f4f34-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="f4f34-109">Navigera till mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT* och kör den körbara filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f4f34-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f4f34-110">På sidan 1 i guiden Common Data Service Configuration Migration (CMT) väljer du **Importera data** och sedan **Fortsätt**.</span><span class="sxs-lookup"><span data-stu-id="f4f34-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Configuration Migration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f4f34-112">På sidan 2 i guiden CMT väljer du **Microsoft 365** som **Distributionstyp**.</span><span class="sxs-lookup"><span data-stu-id="f4f34-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f4f34-113">Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.</span><span class="sxs-lookup"><span data-stu-id="f4f34-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f4f34-114">Välj region för klientorganisationen, ange autentiseringsuppgifter och välj sedan **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="f4f34-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f4f34-116">På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer sedan **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="f4f34-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f4f34-117">På sidan 4 väljer du zip-filen *MasterAndSetupData* från den uppackade mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT*.</span><span class="sxs-lookup"><span data-stu-id="f4f34-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![ZIP-fil](./media/3ZipFile.png)

   ![Välj en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="f4f34-120">När du har markerat zip-filen väljer du **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="f4f34-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importera data](./media/5ImportData.png)

10. <span data-ttu-id="f4f34-122">Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet.</span><span class="sxs-lookup"><span data-stu-id="f4f34-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f4f34-123">När den är klar stänger du guiden för CMT.</span><span class="sxs-lookup"><span data-stu-id="f4f34-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f4f34-124">Kontrollera om organisationen har data i följande 20 entiteter:</span><span class="sxs-lookup"><span data-stu-id="f4f34-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="f4f34-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4f34-125">Currency</span></span>
    -   <span data-ttu-id="f4f34-126">Konto</span><span class="sxs-lookup"><span data-stu-id="f4f34-126">Account</span></span>
    -   <span data-ttu-id="f4f34-127">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="f4f34-127">Organizational Unit</span></span>
    -   <span data-ttu-id="f4f34-128">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="f4f34-128">Contact</span></span>
    -   <span data-ttu-id="f4f34-129">Enhet</span><span class="sxs-lookup"><span data-stu-id="f4f34-129">Unit</span></span>
    -   <span data-ttu-id="f4f34-130">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="f4f34-130">Unit Group</span></span>
    -   <span data-ttu-id="f4f34-131">Prislista</span><span class="sxs-lookup"><span data-stu-id="f4f34-131">Price List</span></span>
    -   <span data-ttu-id="f4f34-132">Prislista för projektparameter</span><span class="sxs-lookup"><span data-stu-id="f4f34-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="f4f34-133">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="f4f34-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="f4f34-134">Bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="f4f34-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="f4f34-135">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="f4f34-135">Transaction Category</span></span>
    -   <span data-ttu-id="f4f34-136">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="f4f34-136">Expense Category</span></span>
    -   <span data-ttu-id="f4f34-137">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="f4f34-137">Role Price</span></span>
    -   <span data-ttu-id="f4f34-138">Pris för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="f4f34-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="f4f34-139">Egenskap</span><span class="sxs-lookup"><span data-stu-id="f4f34-139">Characteristic</span></span>
    -   <span data-ttu-id="f4f34-140">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="f4f34-140">Bookable Resource</span></span>
    -   <span data-ttu-id="f4f34-141">Association för bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="f4f34-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="f4f34-142">Egenskap för bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="f4f34-142">Bookable Resource Characteristic</span></span>

    ![Slutför import](./media/6CompleteImport.png)
