---
title: Etablera en ny miljö
description: I det här ämnet finns information om hur du etablerar en ny Project Operations-miljö.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643014"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="6d44a-103">Etablera en ny miljö</span><span class="sxs-lookup"><span data-stu-id="6d44a-103">Provision a new environment</span></span>

<span data-ttu-id="6d44a-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="6d44a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6d44a-105">I det här ämnet finns information om hur du tillhandahåller en ny Dynamics 365 Project Operations-miljö för resurser/icke-lagerbaserade scenarier.</span><span class="sxs-lookup"><span data-stu-id="6d44a-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="6d44a-106">Aktivera automatisk etablering av Project Operations i ett LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="6d44a-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="6d44a-107">Följ stegen nedan om du vill aktivera det automatiska etableringsflödet för Project Operations för ditt LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="6d44a-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="6d44a-108">Gå till [LCS](https://lcs.dynamics.com/v2) och välj ikonen **Hantering av förhandsgranskningsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="6d44a-109">I listan **Förhandsgranskningsfunktion** väljer du **Project Operations-funktion** och sedan **Förhandsgranskningsfunktion aktiverad** för att aktivera Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6d44a-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="6d44a-110">Det här steget utförs endast en gång per LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="6d44a-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="6d44a-111">Etablera en Project Operations-miljö</span><span class="sxs-lookup"><span data-stu-id="6d44a-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="6d44a-112">Öppna en ny Dynamics 365 Finance [demomiljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandbox-miljö/produktionsmiljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) distribution.</span><span class="sxs-lookup"><span data-stu-id="6d44a-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="6d44a-113">Gå igenom guiden **Miljöetablering**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="6d44a-114">Kontrollera att den valda programversionen är 10.0.13 eller senare.</span><span class="sxs-lookup"><span data-stu-id="6d44a-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="6d44a-115">Om du vill etablera Project Operations väljer du, under **Avancerade inställningar**, **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="6d44a-116">Aktivera **Common Data Service-inställningen** genom att välja **Ja** och sedan ange information i de obligatoriska fälten:</span><span class="sxs-lookup"><span data-stu-id="6d44a-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="6d44a-117">Namn</span><span class="sxs-lookup"><span data-stu-id="6d44a-117">Name</span></span>
  - <span data-ttu-id="6d44a-118">Region</span><span class="sxs-lookup"><span data-stu-id="6d44a-118">Region</span></span>
  - <span data-ttu-id="6d44a-119">Språk</span><span class="sxs-lookup"><span data-stu-id="6d44a-119">Language</span></span>
  - <span data-ttu-id="6d44a-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="6d44a-120">Currency</span></span>
 
5. <span data-ttu-id="6d44a-121">I fältet **Common Data Service-mall** väljer du **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="6d44a-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="6d44a-122">Välj miljötypen för din distribution.</span><span class="sxs-lookup"><span data-stu-id="6d44a-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="6d44a-123">Med en prenumerationsbaserad utvärderingsversion kan du distribuera en CDS-miljö i 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="6d44a-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Distributionsinställningar](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="6d44a-125">Välj **Godkänn** för att bekräfta tjänstvillkoren och välj sedan **Klar** för att återgå till distributionsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="6d44a-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Distributionsmedgivande](./media/2DeploymentConsent.png)

7. <span data-ttu-id="6d44a-127">Fyll i de återstående obligatoriska fälten i guiden och bekräfta distributionen.</span><span class="sxs-lookup"><span data-stu-id="6d44a-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="6d44a-128">Hur lång tid det tar att etablera miljön varierar beroende på miljötypen.</span><span class="sxs-lookup"><span data-stu-id="6d44a-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="6d44a-129">Etableringen kan ta upp till sex timmar.</span><span class="sxs-lookup"><span data-stu-id="6d44a-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="6d44a-130">När distributionen har slutförts visas miljön som **Distribuerad**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="6d44a-131">Du bekräftar att miljön har distribuerats genom att välja **Logga in** och sedan logga in på miljön.</span><span class="sxs-lookup"><span data-stu-id="6d44a-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ miljöinformation](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="6d44a-133">Tillämpa Project Operations Finance-demodata (valfritt steg)</span><span class="sxs-lookup"><span data-stu-id="6d44a-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="6d44a-134">Tillämpa Project Operations Finance-demodata till 10.0.13-tjänstutgåvan av molnbaserad miljö enligt beskrivningen i [den här artikeln](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="6d44a-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="6d44a-135">Tillämpa uppdateringar av Finance-miljön</span><span class="sxs-lookup"><span data-stu-id="6d44a-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="6d44a-136">Project Operations kräver en Finance-miljö med programversion **10.0.13 (10.0.569.20009)** eller senare.</span><span class="sxs-lookup"><span data-stu-id="6d44a-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="6d44a-137">Du kan behöva tillämpa kvalitetsuppdateringar av Finance-miljön för att få den här versionen.</span><span class="sxs-lookup"><span data-stu-id="6d44a-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="6d44a-138">I LCS, på sidan **Miljöinformation**, i avsnittet **Tillgängliga uppdateringar**, väljer du **Visa uppdatering**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visa uppdateringar](./media/5ViewUpdates.png)

2. <span data-ttu-id="6d44a-140">På sidan **Binära uppdateringar** väljer du **Spara paket.**</span><span class="sxs-lookup"><span data-stu-id="6d44a-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spara paket](./media/6SavePackage.png)

3. <span data-ttu-id="6d44a-142">Klicka på **Välj alla** och välj sedan **Spara paket**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-142">Click **Select all** and then select **Save package**.</span></span>

![Granska och spara uppdateringar](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="6d44a-144">Ange ett namn och en beskrivning för paketet och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="6d44a-145">Beroende på vilken internetanslutning du har kan processen ta lite tid.</span><span class="sxs-lookup"><span data-stu-id="6d44a-145">Depending on the internet connection, this process might take some time.</span></span>

![Ladda upp paket till resursbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="6d44a-147">När paketet har sparats väljer du **Klart** och sparar det här paketet i resursbiblioteket i LCS-projektet.</span><span class="sxs-lookup"><span data-stu-id="6d44a-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="6d44a-148">Det kan ta ~ 15 minuter att spara och verifiera paketet.</span><span class="sxs-lookup"><span data-stu-id="6d44a-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="6d44a-149">Om du vill tillämpa uppdateringen navigerar du till sidan **Miljöinformation** i LCS och väljer **Upprätthåll** > **Tillämpa uppdateringar**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Upprätthåll miljöer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="6d44a-151">Välj det paket du skapade i listan med uppdateringar och välj **Tillämpa**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Tillämpa uppdateringar](./media/10ApplyUpdates.png)

<span data-ttu-id="6d44a-153">Miljöunderhållet tar lite tid.</span><span class="sxs-lookup"><span data-stu-id="6d44a-153">Environment servicing will take some time.</span></span> <span data-ttu-id="6d44a-154">När det är klart kommer miljön att återgå till ett distribuerat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="6d44a-154">After it is complete, the environment will return to a deployed state.</span></span>

![Miljö distribuerad](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="6d44a-156">Upprätta en anslutning med dubbelskrivning</span><span class="sxs-lookup"><span data-stu-id="6d44a-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="6d44a-157">I ditt LCS-projekt går du till sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="6d44a-158">Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="6d44a-159">När länken är klar väljer du **Länk till CDS for Apps** igen.</span><span class="sxs-lookup"><span data-stu-id="6d44a-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="6d44a-160">Du omdirigeras då till dubbelskrivning i Finance.</span><span class="sxs-lookup"><span data-stu-id="6d44a-160">You will be redirected to Dual Write in Finance.</span></span>

![Länk till CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="6d44a-162">Välj **Tillämpa lösning** för att komma åt de entiteter som ska mappas i integrationen.</span><span class="sxs-lookup"><span data-stu-id="6d44a-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Tillämpa lösningar](./media/13ApplySolutions.png)

5. <span data-ttu-id="6d44a-164">Välj båda lösningarna, **Dynamics 365 Finance and Operations-entitetskarta för dubbelskrivning** och **Dynamics 365 Project Operations-entitetskartor för dubbelskrivning** och välj sedan **Verkställ**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekräfta lösningar](./media/14ConfirmSolutions.png)

<span data-ttu-id="6d44a-166">När lösningarna har tillämpats tillämpas entiteterna med dubbelskrivning i miljön.</span><span class="sxs-lookup"><span data-stu-id="6d44a-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Tillämpa lösningar](./media/15ApplyingSolutions.png)

<span data-ttu-id="6d44a-168">När entiteterna har tillämpats visas alla tillgängliga mappningar i miljön.</span><span class="sxs-lookup"><span data-stu-id="6d44a-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kartor dubbelskrivning](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="6d44a-170">Uppdatera dataentiteterna efter uppdateringen</span><span class="sxs-lookup"><span data-stu-id="6d44a-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="6d44a-171">I Finance går du till arbetsytan **Datahantering**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-171">In Finance, go to the **Data management** workspace.</span></span>

![Datahantering arbetsyta](./media/16DataManagement.png)

2. <span data-ttu-id="6d44a-173">Välj ikonen **Ramverksparametrar**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-173">Select the **Framework parameters** tile.</span></span>

![Ramverksparametrar](./media/17FrameworkParameters.png)

3. <span data-ttu-id="6d44a-175">På sidan **Entitetsinställningar** väljer du **Uppdatera entitetslista**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Uppdatera entitetslista](./media/18RefreshEntityList.png)

<span data-ttu-id="6d44a-177">Uppdateringen ska ta cirka 20 minuter.</span><span class="sxs-lookup"><span data-stu-id="6d44a-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="6d44a-178">Du kommer att få en avisering när den är klar.</span><span class="sxs-lookup"><span data-stu-id="6d44a-178">You will receive an alert when it is complete.</span></span>

![Uppdateringsbekräftelse](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="6d44a-180">Kör kartor för dubbelskrivning i Project Operations</span><span class="sxs-lookup"><span data-stu-id="6d44a-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="6d44a-181">I ditt LCS-projekt går du till sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="6d44a-182">Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="6d44a-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="6d44a-183">När du har valt länken dirigeras du om till listan över entiteter i mappningarna.</span><span class="sxs-lookup"><span data-stu-id="6d44a-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="6d44a-184">Starta kartorna enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="6d44a-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="6d44a-185">Kontrollera att du följer sekvensen enligt anvisningarna nedan.</span><span class="sxs-lookup"><span data-stu-id="6d44a-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="6d44a-186">**Entitetsmappning**</span><span class="sxs-lookup"><span data-stu-id="6d44a-186">**Entity Map**</span></span> | <span data-ttu-id="6d44a-187">**Uppdatera entitet**</span><span class="sxs-lookup"><span data-stu-id="6d44a-187">**Refresh entity**</span></span> | <span data-ttu-id="6d44a-188">**Initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="6d44a-188">**Initial sync**</span></span> | <span data-ttu-id="6d44a-189">**Huvud för initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="6d44a-189">**Master for initial sync**</span></span> | <span data-ttu-id="6d44a-190">**Kör förutsättningar**</span><span class="sxs-lookup"><span data-stu-id="6d44a-190">**Run prerequisites**</span></span> | <span data-ttu-id="6d44a-191">**Förutsättningar initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="6d44a-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="6d44a-192">**Projektresursroller för alla företag (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="6d44a-193">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-193">No</span></span> | <span data-ttu-id="6d44a-194">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-194">Yes</span></span> | <span data-ttu-id="6d44a-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6d44a-195">Common Data Service</span></span> | <span data-ttu-id="6d44a-196">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-196">No</span></span> | <span data-ttu-id="6d44a-197">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-197">N\A</span></span> |
| <span data-ttu-id="6d44a-198">**Juridiska personer (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="6d44a-199">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-199">No</span></span> | <span data-ttu-id="6d44a-200">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-200">Yes</span></span> | <span data-ttu-id="6d44a-201">Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="6d44a-201">Finance and Operations apps</span></span> | <span data-ttu-id="6d44a-202">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-202">No</span></span> | <span data-ttu-id="6d44a-203">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-203">N\A</span></span> |
| <span data-ttu-id="6d44a-204">**Huvudbok (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="6d44a-205">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-205">No</span></span> | <span data-ttu-id="6d44a-206">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-206">Yes</span></span> | <span data-ttu-id="6d44a-207">Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="6d44a-207">Finance and Operations apps</span></span> | <span data-ttu-id="6d44a-208">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-208">Yes</span></span> | <span data-ttu-id="6d44a-209">Ja, Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="6d44a-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="6d44a-210">**Verkliga värden för Project Operations-integrering (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="6d44a-211">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-211">No</span></span> | <span data-ttu-id="6d44a-212">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-212">No</span></span> | <span data-ttu-id="6d44a-213">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-213">N\A</span></span> | <span data-ttu-id="6d44a-214">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-214">Yes</span></span> | <span data-ttu-id="6d44a-215">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-215">No</span></span> |
| <span data-ttu-id="6d44a-216">**Projektkontraktrader (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="6d44a-217">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-217">No</span></span> | <span data-ttu-id="6d44a-218">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-218">No</span></span> | <span data-ttu-id="6d44a-219">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-219">N\A</span></span> | <span data-ttu-id="6d44a-220">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-220">No</span></span> | <span data-ttu-id="6d44a-221">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-221">No</span></span> |
| <span data-ttu-id="6d44a-222">**Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="6d44a-223">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-223">No</span></span> | <span data-ttu-id="6d44a-224">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-224">No</span></span> | <span data-ttu-id="6d44a-225">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-225">N\A</span></span> | <span data-ttu-id="6d44a-226">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-226">No</span></span> | <span data-ttu-id="6d44a-227">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-227">N\A</span></span> |
| <span data-ttu-id="6d44a-228">**Milstolpar för kontraktrad för Project Operations-integration (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="6d44a-229">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-229">No</span></span> | <span data-ttu-id="6d44a-230">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-230">No</span></span> | <span data-ttu-id="6d44a-231">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-231">N\A</span></span> | <span data-ttu-id="6d44a-232">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-232">No</span></span> | <span data-ttu-id="6d44a-233">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-233">N\A</span></span> |
| <span data-ttu-id="6d44a-234">**Entitet för Project Operations-integration för utgiftsuppskattningar (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="6d44a-235">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-235">No</span></span> | <span data-ttu-id="6d44a-236">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-236">No</span></span> | <span data-ttu-id="6d44a-237">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-237">N\A</span></span> | <span data-ttu-id="6d44a-238">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-238">No</span></span> | <span data-ttu-id="6d44a-239">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-239">N\A</span></span> |
| <span data-ttu-id="6d44a-240">**Entitet för export av projektutgiftkategorier i Project Operations-integration (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="6d44a-241">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-241">No</span></span> | <span data-ttu-id="6d44a-242">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-242">No</span></span> | <span data-ttu-id="6d44a-243">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-243">N\A</span></span> | <span data-ttu-id="6d44a-244">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-244">No</span></span> | <span data-ttu-id="6d44a-245">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-245">N\A</span></span> |
| <span data-ttu-id="6d44a-246">**Entitet för export av projektutgifter i Project Operations-integration (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="6d44a-247">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-247">Yes</span></span> | <span data-ttu-id="6d44a-248">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-248">No</span></span> | <span data-ttu-id="6d44a-249">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-249">N\A</span></span> | <span data-ttu-id="6d44a-250">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-250">No</span></span> | <span data-ttu-id="6d44a-251">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-251">N\A</span></span> |
| <span data-ttu-id="6d44a-252">**Entitet för Project Operations-integration för tidsuppskattningar (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="6d44a-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="6d44a-253">Ja</span><span class="sxs-lookup"><span data-stu-id="6d44a-253">Yes</span></span> | <span data-ttu-id="6d44a-254">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-254">No</span></span> | <span data-ttu-id="6d44a-255">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-255">N\A</span></span> | <span data-ttu-id="6d44a-256">Inga</span><span class="sxs-lookup"><span data-stu-id="6d44a-256">No</span></span> | <span data-ttu-id="6d44a-257">N\A</span><span class="sxs-lookup"><span data-stu-id="6d44a-257">N\A</span></span> |


4. <span data-ttu-id="6d44a-258">Om du vill uppdatera entiteten väljer du kartnamnet och väljer sedan **Uppdatera entiteter**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Uppdatera karta](./media/20RefreshMapping.png)

5. <span data-ttu-id="6d44a-260">Kör kartan efter att uppdateringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="6d44a-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="6d44a-261">Innan du aktiverar nästa karta ska du kontrollera att kartan i tabellen är i tillståndet **Körs**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="6d44a-262">Det kan ta en stund att köra kartor med ett större antal förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="6d44a-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="6d44a-263">Om du vill köra en karta med förutsättningar ska du aktivera **Visa relaterade entitetskartor**.</span><span class="sxs-lookup"><span data-stu-id="6d44a-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="6d44a-264">Om tabellen anger att **Förutsättning initial synkronisering** är **Nej**, verifierar du att flaggan **Initial synkronisering** är **Av** i alla förutsättningskartor innan du kör den.</span><span class="sxs-lookup"><span data-stu-id="6d44a-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kör karta](./media/21RunMap.png)

6. <span data-ttu-id="6d44a-266">Kontrollera att alla projektrelaterade kartor är i körläge.</span><span class="sxs-lookup"><span data-stu-id="6d44a-266">Validate all project related maps are in the running state.</span></span>

![Alla kartor körs](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="6d44a-268">Använda konfigurationsdata i CDS för Project Operations (valfritt)</span><span class="sxs-lookup"><span data-stu-id="6d44a-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="6d44a-269">Om du har använt demonstrationsdata i Finance-miljön läser du [Konfigurera och tillämpa konfigurationsdata i Common Data Service för Project Operations](resource-apply-pro-setup-config-data.md) för att tillämpa demonstrations data på CDS-miljön.</span><span class="sxs-lookup"><span data-stu-id="6d44a-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="6d44a-270">Project Operations-miljön har nu etablerats och konfigurerats.</span><span class="sxs-lookup"><span data-stu-id="6d44a-270">Your Project Operations environment is now provisioned and configured.</span></span> 
