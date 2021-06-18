---
title: Ställ in och använd konfigurationsdata i Common Data Service
description: I det här ämnet finns information om hur du konfigurerar och tillämpar konfigurationsdata i Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001313"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="8ad42-103">Ställ in och använd konfigurationsdata i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8ad42-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="8ad42-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="8ad42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="8ad42-105">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="8ad42-105">Prerequisites</span></span>

<span data-ttu-id="8ad42-106">Innan du börjar konfigurera data i Common Data Service (CDS) måste följande krav uppfyllas:</span><span class="sxs-lookup"><span data-stu-id="8ad42-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="8ad42-107">Konfigurera en CDS-miljö och en Dynamics 365 Finance-miljö för Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8ad42-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="8ad42-108">Information om juridisk person från Dynamics 365 Finance delas med CDS-miljön.</span><span class="sxs-lookup"><span data-stu-id="8ad42-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="8ad42-109">Detta innebär att entiteten **företag** i CDS-skivor har följande företagsposter:</span><span class="sxs-lookup"><span data-stu-id="8ad42-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="8ad42-110">THPM</span><span class="sxs-lookup"><span data-stu-id="8ad42-110">THPM</span></span>
  - <span data-ttu-id="8ad42-111">USPM</span><span class="sxs-lookup"><span data-stu-id="8ad42-111">USPM</span></span>
  - <span data-ttu-id="8ad42-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="8ad42-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="8ad42-113">Installationsinställning och konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="8ad42-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="8ad42-114">Hämta, avblockera och packa upp paketet [Inställnings- och konfigurationsdata](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="8ad42-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="8ad42-115">Navigera till den uppackade mappen och kör den körbara filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="8ad42-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="8ad42-116">På sidan 1 i guiden Common Data Service Configuration Migration (CMT) väljer du **Importera data** och sedan **Fortsätt**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Configuration Migration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="8ad42-118">På sidan 2 i guiden CMT väljer du **Microsoft 365** som **Distributionstyp**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="8ad42-119">Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="8ad42-120">Välj region för klientorganisationen, ange autentiseringsuppgifter och välj **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="8ad42-122">På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer **Logga in**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="8ad42-123">På sidan 4 väljer du zip-filen *SampleSetupAndConfigData* från den uppackade mappen.</span><span class="sxs-lookup"><span data-stu-id="8ad42-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Välj zip-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="8ad42-126">När du har markerat zip-filen väljer du **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-126">After the zip file is selected, select **Import Data**.</span></span>

![Importera data](./media/5ImportData.png)

10. <span data-ttu-id="8ad42-128">Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet.</span><span class="sxs-lookup"><span data-stu-id="8ad42-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="8ad42-129">När importen är klar stänger du guiden för CMT.</span><span class="sxs-lookup"><span data-stu-id="8ad42-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="8ad42-130">Kontrollera om organisationen har data i följande 26 entiteter:</span><span class="sxs-lookup"><span data-stu-id="8ad42-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="8ad42-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="8ad42-131">Currency</span></span>
  - <span data-ttu-id="8ad42-132">Kontolista</span><span class="sxs-lookup"><span data-stu-id="8ad42-132">Chart of Accounts</span></span>
  - <span data-ttu-id="8ad42-133">Kalender för räkenskapsår</span><span class="sxs-lookup"><span data-stu-id="8ad42-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="8ad42-134">Typer av valutakurser</span><span class="sxs-lookup"><span data-stu-id="8ad42-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="8ad42-135">Betalningsdag</span><span class="sxs-lookup"><span data-stu-id="8ad42-135">Payment Day</span></span>
  - <span data-ttu-id="8ad42-136">Betalningsschema</span><span class="sxs-lookup"><span data-stu-id="8ad42-136">Payment Schedule</span></span>
  - <span data-ttu-id="8ad42-137">Betalningsvillkor</span><span class="sxs-lookup"><span data-stu-id="8ad42-137">Payment Term</span></span>
  - <span data-ttu-id="8ad42-138">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="8ad42-138">Organizational Unit</span></span>
  - <span data-ttu-id="8ad42-139">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="8ad42-139">Contact</span></span>
  - <span data-ttu-id="8ad42-140">Momsgrupp</span><span class="sxs-lookup"><span data-stu-id="8ad42-140">Tax Group</span></span>
  - <span data-ttu-id="8ad42-141">Kundgrupp</span><span class="sxs-lookup"><span data-stu-id="8ad42-141">Customer Group</span></span>
  - <span data-ttu-id="8ad42-142">Leverantörsgrupp</span><span class="sxs-lookup"><span data-stu-id="8ad42-142">Vendor Group</span></span>
  - <span data-ttu-id="8ad42-143">Enhet</span><span class="sxs-lookup"><span data-stu-id="8ad42-143">Unit</span></span>
  - <span data-ttu-id="8ad42-144">Enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="8ad42-144">Unit Group</span></span>
  - <span data-ttu-id="8ad42-145">Prislista</span><span class="sxs-lookup"><span data-stu-id="8ad42-145">Price List</span></span>
  - <span data-ttu-id="8ad42-146">Prislista för projektparameter</span><span class="sxs-lookup"><span data-stu-id="8ad42-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="8ad42-147">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="8ad42-147">Invoice Frequency</span></span>
  - <span data-ttu-id="8ad42-148">Bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="8ad42-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="8ad42-149">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="8ad42-149">Transaction Category</span></span>
  - <span data-ttu-id="8ad42-150">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="8ad42-150">Expense Category</span></span>
  - <span data-ttu-id="8ad42-151">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="8ad42-151">Role Price</span></span>
  - <span data-ttu-id="8ad42-152">Pris för transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="8ad42-152">Transaction Category Price</span></span>
  - <span data-ttu-id="8ad42-153">Egenskap</span><span class="sxs-lookup"><span data-stu-id="8ad42-153">Characteristic</span></span>
  - <span data-ttu-id="8ad42-154">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="8ad42-154">Bookable Resource</span></span>
  - <span data-ttu-id="8ad42-155">Association för bokningsbar resurskategori</span><span class="sxs-lookup"><span data-stu-id="8ad42-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="8ad42-156">Egenskap för bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="8ad42-156">Bookable Resource Characteristic</span></span>

![Slutför import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="8ad42-158">Uppdatera Project Operations-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="8ad42-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="8ad42-159">Navigera till CE-miljön.</span><span class="sxs-lookup"><span data-stu-id="8ad42-159">Navigate to the CE environment.</span></span> <span data-ttu-id="8ad42-160">Du hittar den genom att öppna [Power Platform-administratörscenter](https://admin.powerplatform.microsoft.com/environments), välja miljön och sedan välja **Öppna miljö**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Öppna miljön](./media/7OpenEnvironment.png)

2. <span data-ttu-id="8ad42-162">Gå till **Projekt** > **Resurser** och välj sedan **Ny** för att skapa en bokningsbar resurs för användaren.</span><span class="sxs-lookup"><span data-stu-id="8ad42-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Bokningsbara resurser](./media/8BookableResources.png)

3. <span data-ttu-id="8ad42-164">Under fliken **Allmänt** väljer du administratörsanvändare.</span><span class="sxs-lookup"><span data-stu-id="8ad42-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="8ad42-165">Kontrollera att tidszonen överensstämmer med den som du befinner dig i.</span><span class="sxs-lookup"><span data-stu-id="8ad42-165">Verify that the time zone matches the one you are in.</span></span> 

![Ny bokningsbar resurs](./media/9NewBookableResource.png)

4. <span data-ttu-id="8ad42-167">Under fliken **Schemaläggning**, i fältet **Företag**, väljer du företaget **USPM** och sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Fliken Schemaläggning](./media/10SchedulingTab.png)

5. <span data-ttu-id="8ad42-169">Välj fliken **Arbetstider**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-169">Select the **Work hours** tab.</span></span>  

![Arbetstider](./media/11WorkHours.png)

6. <span data-ttu-id="8ad42-171">Dubbelklicka på ett värde i kalendern och välj **Redigera** > **Alla händelser i serien**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbetskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="8ad42-173">Ändra arbetstider till en åttatimmars arbetsdag, markera helger som lediga dagar och kontrollera att tidszonen överensstämmer med din.</span><span class="sxs-lookup"><span data-stu-id="8ad42-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="8ad42-174">Välj **Spara och stäng**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-174">Select **Save and close**.</span></span>

![Uppdatera kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="8ad42-176">Gå till **Inställningar** > **Kalender-mallar** och välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendermallar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="8ad42-178">Ange ett namn, välj den mallresurs som du har skapat och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Spara kalendermall](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="8ad42-180">Gå till **Parametrar** och dubbelklicka på posten.</span><span class="sxs-lookup"><span data-stu-id="8ad42-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparametrar](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="8ad42-182">Uppdatera följande fält:</span><span class="sxs-lookup"><span data-stu-id="8ad42-182">Update the following fields:</span></span>

 - <span data-ttu-id="8ad42-183">**Standardföretag**: USPM</span><span class="sxs-lookup"><span data-stu-id="8ad42-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="8ad42-184">**Standardorganisationsenhet**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="8ad42-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="8ad42-185">**Faktureringsfrekvens**: sjunde och sista dagen</span><span class="sxs-lookup"><span data-stu-id="8ad42-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="8ad42-186">**Arbetstidsmall**: ändra till den mall du skapade.</span><span class="sxs-lookup"><span data-stu-id="8ad42-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="8ad42-187">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="8ad42-187">Select **Save**.</span></span> 

![Uppdaterade projektparametrar](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
