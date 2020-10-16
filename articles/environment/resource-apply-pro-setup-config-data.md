---
title: Konfigurera och använda konfigurationsdata i Common Data Service för Project Operations
description: I det här ämnet finns information om hur du konfigurerar och tillämpar konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949100"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="bd3ba-103">Konfigurera och använda konfigurationsdata i Common Data Service för Project Operations</span><span class="sxs-lookup"><span data-stu-id="bd3ba-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="bd3ba-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="bd3ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="bd3ba-105">Installationsinställning och konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="bd3ba-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="bd3ba-106">Hämta, avblockera och packa upp paketet [Inställnings- och konfigurationsdata](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="bd3ba-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="bd3ba-107">Navigera till den uppackade mappen och kör den körbara filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="bd3ba-108">På sidan 1 i guiden Common Data Service konfigurationsmigrering (CMT) väljer du **Importera data** och sedan **Fortsätt**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigrering](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="bd3ba-110">På sidan 2 i guiden CMT väljer du **Office 365** som **Distributionstyp**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="bd3ba-111">Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="bd3ba-112">Välj region för klientorganisationen, ange autentiseringsuppgifter och välj **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="bd3ba-114">På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="bd3ba-115">På sidan 4 väljer du zip-filen *SampleSetupAndConfigData* från den uppackade mappen.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Välj zip-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="bd3ba-118">När du har markerat zip-filen väljer du **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-118">After the zip file is selected, select **Import Data**.</span></span>

![Importera data](./media/5ImportData.png)

10. <span data-ttu-id="bd3ba-120">Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="bd3ba-121">När importen är klar stänger du guiden för CMT.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="bd3ba-122">Kontrollera om organisationen har data i följande 19 entiteter:</span><span class="sxs-lookup"><span data-stu-id="bd3ba-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="bd3ba-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="bd3ba-123">Currency</span></span>
  - <span data-ttu-id="bd3ba-124">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="bd3ba-124">Organizational Unit</span></span>
  - <span data-ttu-id="bd3ba-125">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="bd3ba-125">Contact</span></span>
  - <span data-ttu-id="bd3ba-126">Momsgrupp</span><span class="sxs-lookup"><span data-stu-id="bd3ba-126">Tax Group</span></span>
  - <span data-ttu-id="bd3ba-127">Kundgrupp</span><span class="sxs-lookup"><span data-stu-id="bd3ba-127">Customer Group</span></span>
  - <span data-ttu-id="bd3ba-128">Enhet</span><span class="sxs-lookup"><span data-stu-id="bd3ba-128">Unit</span></span>
  - <span data-ttu-id="bd3ba-129">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="bd3ba-129">Unit Group</span></span>
  - <span data-ttu-id="bd3ba-130">Prislista</span><span class="sxs-lookup"><span data-stu-id="bd3ba-130">Price List</span></span>
  - <span data-ttu-id="bd3ba-131">Prislista för projektparameter</span><span class="sxs-lookup"><span data-stu-id="bd3ba-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="bd3ba-132">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="bd3ba-132">Invoice Frequency</span></span>
  - <span data-ttu-id="bd3ba-133">Bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="bd3ba-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="bd3ba-134">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="bd3ba-134">Transaction Category</span></span>
  - <span data-ttu-id="bd3ba-135">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="bd3ba-135">Expense Category</span></span>
  - <span data-ttu-id="bd3ba-136">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="bd3ba-136">Role Price</span></span>
  - <span data-ttu-id="bd3ba-137">Pris för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="bd3ba-137">Transaction Category Price</span></span>
  - <span data-ttu-id="bd3ba-138">Egenskap</span><span class="sxs-lookup"><span data-stu-id="bd3ba-138">Characteristic</span></span>
  - <span data-ttu-id="bd3ba-139">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="bd3ba-139">Bookable Resource</span></span>
  - <span data-ttu-id="bd3ba-140">Association för bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="bd3ba-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="bd3ba-141">Egenskap för bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="bd3ba-141">Bookable Resource Characteristic</span></span>

![Slutför import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="bd3ba-143">Uppdatera Project Operations-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="bd3ba-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="bd3ba-144">Navigera till CE-miljön.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-144">Navigate to the CE environment.</span></span> <span data-ttu-id="bd3ba-145">Du hittar den genom att öppna [Power Platform-administratörscenter](https://admin.powerplatform.microsoft.com/environments), välja miljön och sedan välja **Öppna miljö**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Öppna miljön](./media/7OpenEnvironment.png)

2. <span data-ttu-id="bd3ba-147">Gå till **Projekt** > **Resurser** och välj sedan **Ny** för att skapa en bokningsbar resurs för användaren.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Bokningsbara resurser](./media/8BookableResources.png)

3. <span data-ttu-id="bd3ba-149">Under fliken **Allmänt** väljer du administratörsanvändare.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="bd3ba-150">Kontrollera att tidszonen överensstämmer med den som du befinner dig i.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-150">Verify that the time zone matches the one you are in.</span></span> 

![Ny bokningsbar resurs](./media/9NewBookableResource.png)

4. <span data-ttu-id="bd3ba-152">Under fliken **Schemaläggning**, i fältet **Företag**, väljer du företaget **USPM** och sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Fliken Schemaläggning](./media/10SchedulingTab.png)

5. <span data-ttu-id="bd3ba-154">Välj fliken **Arbetstider**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-154">Select the **Work hours** tab.</span></span>  

![Arbetstider](./media/11WorkHours.png)

6. <span data-ttu-id="bd3ba-156">Dubbelklicka på ett värde i kalendern och välj **Redigera** > **Alla händelser i serien**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbetskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="bd3ba-158">Ändra arbetstider till en åttatimmars arbetsdag, markera helger som lediga dagar och kontrollera att tidszonen överensstämmer med din.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="bd3ba-159">Välj **Spara och stäng**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-159">Select **Save and close**.</span></span>

![Uppdatera kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="bd3ba-161">Gå till **Inställningar** > **Kalender-mallar** och välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendermallar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="bd3ba-163">Ange ett namn, välj den mallresurs som du har skapat och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Spara kalendermall](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="bd3ba-165">Gå till **Parametrar** och dubbelklicka på posten.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparametrar](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="bd3ba-167">Uppdatera följande fält:</span><span class="sxs-lookup"><span data-stu-id="bd3ba-167">Update the following fields:</span></span>

 - <span data-ttu-id="bd3ba-168">**Standardföretag**: USPM</span><span class="sxs-lookup"><span data-stu-id="bd3ba-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="bd3ba-169">**Standardorganisationsenhet**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="bd3ba-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="bd3ba-170">**Faktureringsfrekvens**: sjunde och sista dagen</span><span class="sxs-lookup"><span data-stu-id="bd3ba-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="bd3ba-171">**Arbetstidsmall**: ändra till den mall du skapade.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="bd3ba-172">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="bd3ba-172">Select **Save**.</span></span> 

![Uppdaterade projektparametrar](./media/17UpdatedProjectParameters.png)
