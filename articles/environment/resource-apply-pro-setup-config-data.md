---
title: Ställ in och använd konfigurationsdata i Common Data Service
description: I det här ämnet finns information om hur du konfigurerar och tillämpar konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401150"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="e6684-103">Ställ in och använd konfigurationsdata i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e6684-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="e6684-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="e6684-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e6684-105">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="e6684-105">Prerequisites</span></span>

<span data-ttu-id="e6684-106">Innan du börjar konfigurera data i Common Data Service (CDS) måste följande krav uppfyllas:</span><span class="sxs-lookup"><span data-stu-id="e6684-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="e6684-107">Konfigurera en CDS-miljö och en Dynamics 365 Finance-miljö för Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e6684-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="e6684-108">Information om juridisk person från Dynamics 365 Finance delas med CDS-miljön.</span><span class="sxs-lookup"><span data-stu-id="e6684-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="e6684-109">Detta innebär att entiteten **företag** i CDS-skivor har följande företagsposter:</span><span class="sxs-lookup"><span data-stu-id="e6684-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="e6684-110">THPM</span><span class="sxs-lookup"><span data-stu-id="e6684-110">THPM</span></span>
  - <span data-ttu-id="e6684-111">USPM</span><span class="sxs-lookup"><span data-stu-id="e6684-111">USPM</span></span>
  - <span data-ttu-id="e6684-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="e6684-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e6684-113">Installationsinställning och konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="e6684-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="e6684-114">Hämta, avblockera och packa upp paketet [Inställnings- och konfigurationsdata](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="e6684-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="e6684-115">Navigera till den uppackade mappen och kör den körbara filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e6684-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e6684-116">På sidan 1 i guiden Common Data Service konfigurationsmigrering (CMT) väljer du **Importera data** och sedan **Fortsätt**.</span><span class="sxs-lookup"><span data-stu-id="e6684-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigrering](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e6684-118">På sidan 2 i guiden CMT väljer du **Microsoft 365** som **Distributionstyp**.</span><span class="sxs-lookup"><span data-stu-id="e6684-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e6684-119">Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.</span><span class="sxs-lookup"><span data-stu-id="e6684-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e6684-120">Välj region för klientorganisationen, ange autentiseringsuppgifter och välj **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="e6684-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e6684-122">På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="e6684-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e6684-123">På sidan 4 väljer du zip-filen *SampleSetupAndConfigData* från den uppackade mappen.</span><span class="sxs-lookup"><span data-stu-id="e6684-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Välj zip-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="e6684-126">När du har markerat zip-filen väljer du **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="e6684-126">After the zip file is selected, select **Import Data**.</span></span>

![Importera data](./media/5ImportData.png)

10. <span data-ttu-id="e6684-128">Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet.</span><span class="sxs-lookup"><span data-stu-id="e6684-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e6684-129">När importen är klar stänger du guiden för CMT.</span><span class="sxs-lookup"><span data-stu-id="e6684-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e6684-130">Kontrollera om organisationen har data i följande 19 entiteter:</span><span class="sxs-lookup"><span data-stu-id="e6684-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="e6684-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="e6684-131">Currency</span></span>
  - <span data-ttu-id="e6684-132">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="e6684-132">Organizational Unit</span></span>
  - <span data-ttu-id="e6684-133">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e6684-133">Contact</span></span>
  - <span data-ttu-id="e6684-134">Momsgrupp</span><span class="sxs-lookup"><span data-stu-id="e6684-134">Tax Group</span></span>
  - <span data-ttu-id="e6684-135">Kundgrupp</span><span class="sxs-lookup"><span data-stu-id="e6684-135">Customer Group</span></span>
  - <span data-ttu-id="e6684-136">Enhet</span><span class="sxs-lookup"><span data-stu-id="e6684-136">Unit</span></span>
  - <span data-ttu-id="e6684-137">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="e6684-137">Unit Group</span></span>
  - <span data-ttu-id="e6684-138">Prislista</span><span class="sxs-lookup"><span data-stu-id="e6684-138">Price List</span></span>
  - <span data-ttu-id="e6684-139">Prislista för projektparameter</span><span class="sxs-lookup"><span data-stu-id="e6684-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="e6684-140">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="e6684-140">Invoice Frequency</span></span>
  - <span data-ttu-id="e6684-141">Bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="e6684-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="e6684-142">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="e6684-142">Transaction Category</span></span>
  - <span data-ttu-id="e6684-143">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="e6684-143">Expense Category</span></span>
  - <span data-ttu-id="e6684-144">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="e6684-144">Role Price</span></span>
  - <span data-ttu-id="e6684-145">Pris för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="e6684-145">Transaction Category Price</span></span>
  - <span data-ttu-id="e6684-146">Egenskap</span><span class="sxs-lookup"><span data-stu-id="e6684-146">Characteristic</span></span>
  - <span data-ttu-id="e6684-147">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="e6684-147">Bookable Resource</span></span>
  - <span data-ttu-id="e6684-148">Association för bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="e6684-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e6684-149">Egenskap för bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="e6684-149">Bookable Resource Characteristic</span></span>

![Slutför import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e6684-151">Uppdatera Project Operations-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e6684-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e6684-152">Navigera till CE-miljön.</span><span class="sxs-lookup"><span data-stu-id="e6684-152">Navigate to the CE environment.</span></span> <span data-ttu-id="e6684-153">Du hittar den genom att öppna [Power Platform-administratörscenter](https://admin.powerplatform.microsoft.com/environments), välja miljön och sedan välja **Öppna miljö**.</span><span class="sxs-lookup"><span data-stu-id="e6684-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Öppna miljön](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e6684-155">Gå till **Projekt** > **Resurser** och välj sedan **Ny** för att skapa en bokningsbar resurs för användaren.</span><span class="sxs-lookup"><span data-stu-id="e6684-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Bokningsbara resurser](./media/8BookableResources.png)

3. <span data-ttu-id="e6684-157">Under fliken **Allmänt** väljer du administratörsanvändare.</span><span class="sxs-lookup"><span data-stu-id="e6684-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e6684-158">Kontrollera att tidszonen överensstämmer med den som du befinner dig i.</span><span class="sxs-lookup"><span data-stu-id="e6684-158">Verify that the time zone matches the one you are in.</span></span> 

![Ny bokningsbar resurs](./media/9NewBookableResource.png)

4. <span data-ttu-id="e6684-160">Under fliken **Schemaläggning**, i fältet **Företag**, väljer du företaget **USPM** och sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="e6684-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Fliken Schemaläggning](./media/10SchedulingTab.png)

5. <span data-ttu-id="e6684-162">Välj fliken **Arbetstider**.</span><span class="sxs-lookup"><span data-stu-id="e6684-162">Select the **Work hours** tab.</span></span>  

![Arbetstider](./media/11WorkHours.png)

6. <span data-ttu-id="e6684-164">Dubbelklicka på ett värde i kalendern och välj **Redigera** > **Alla händelser i serien**.</span><span class="sxs-lookup"><span data-stu-id="e6684-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbetskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="e6684-166">Ändra arbetstider till en åttatimmars arbetsdag, markera helger som lediga dagar och kontrollera att tidszonen överensstämmer med din.</span><span class="sxs-lookup"><span data-stu-id="e6684-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e6684-167">Välj **Spara och stäng**.</span><span class="sxs-lookup"><span data-stu-id="e6684-167">Select **Save and close**.</span></span>

![Uppdatera kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e6684-169">Gå till **Inställningar** > **Kalender-mallar** och välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e6684-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendermallar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e6684-171">Ange ett namn, välj den mallresurs som du har skapat och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="e6684-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Spara kalendermall](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e6684-173">Gå till **Parametrar** och dubbelklicka på posten.</span><span class="sxs-lookup"><span data-stu-id="e6684-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparametrar](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e6684-175">Uppdatera följande fält:</span><span class="sxs-lookup"><span data-stu-id="e6684-175">Update the following fields:</span></span>

 - <span data-ttu-id="e6684-176">**Standardföretag**: USPM</span><span class="sxs-lookup"><span data-stu-id="e6684-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="e6684-177">**Standardorganisationsenhet**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e6684-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e6684-178">**Faktureringsfrekvens**: sjunde och sista dagen</span><span class="sxs-lookup"><span data-stu-id="e6684-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e6684-179">**Arbetstidsmall**: ändra till den mall du skapade.</span><span class="sxs-lookup"><span data-stu-id="e6684-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e6684-180">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="e6684-180">Select **Save**.</span></span> 

![Uppdaterade projektparametrar](./media/17UpdatedProjectParameters.png)
