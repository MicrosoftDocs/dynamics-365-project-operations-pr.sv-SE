---
title: Etablera en ny miljö
description: I det här ämnet finns information om hur du etablerar en ny Project Operations-miljö.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950556"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="de8fe-103">Etablera en ny miljö</span><span class="sxs-lookup"><span data-stu-id="de8fe-103">Provision a new environment</span></span>

<span data-ttu-id="de8fe-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="de8fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="de8fe-105">I det här ämnet finns information om hur du tillhandahåller en ny Dynamics 365 Project Operations-miljö för resurser/icke-lagerbaserade scenarier.</span><span class="sxs-lookup"><span data-stu-id="de8fe-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="de8fe-106">Aktivera automatisk etablering av Project Operations i ett LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="de8fe-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="de8fe-107">Följ stegen nedan om du vill aktivera det automatiska etableringsflödet för Project Operations för ditt LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="de8fe-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="de8fe-108">Gå till [LCS](https://lcs.dynamics.com/v2) och välj ikonen **Hantering av förhandsgranskningsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="de8fe-109">I listan **Förhandsgranskningsfunktion** väljer du **Project Operations-funktion** och sedan **Förhandsgranskningsfunktion aktiverad** för att aktivera Project Operations.</span><span class="sxs-lookup"><span data-stu-id="de8fe-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="de8fe-110">Det här steget utförs endast en gång per LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="de8fe-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="de8fe-111">Etablera en Project Operations-miljö</span><span class="sxs-lookup"><span data-stu-id="de8fe-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="de8fe-112">Öppna en ny Dynamics 365 Finance [demomiljö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandbox-miljö/produktionsmiljö](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) distribution.</span><span class="sxs-lookup"><span data-stu-id="de8fe-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="de8fe-113">Gå igenom guiden **Miljöetablering**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="de8fe-114">Kontrollera att den valda programversionen är 10.0.13 eller senare.</span><span class="sxs-lookup"><span data-stu-id="de8fe-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="de8fe-115">Om du vill etablera Project Operations väljer du, under **Avancerade inställningar**, **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="de8fe-116">Aktivera **Common Data Service-inställningen** genom att välja **Ja** och sedan ange information i de obligatoriska fälten:</span><span class="sxs-lookup"><span data-stu-id="de8fe-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="de8fe-117">Namn</span><span class="sxs-lookup"><span data-stu-id="de8fe-117">Name</span></span>
  - <span data-ttu-id="de8fe-118">Region</span><span class="sxs-lookup"><span data-stu-id="de8fe-118">Region</span></span>
  - <span data-ttu-id="de8fe-119">Språk</span><span class="sxs-lookup"><span data-stu-id="de8fe-119">Language</span></span>
  - <span data-ttu-id="de8fe-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="de8fe-120">Currency</span></span>
 
5. <span data-ttu-id="de8fe-121">I fältet **Common Data Service-mall** väljer du **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="de8fe-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="de8fe-122">Välj miljötypen för din distribution.</span><span class="sxs-lookup"><span data-stu-id="de8fe-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="de8fe-123">Med en prenumerationsbaserad utvärderingsversion kan du distribuera en CDS-miljö i 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="de8fe-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Distributionsinställningar](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="de8fe-125">Välj **Godkänn** för att bekräfta tjänstvillkoren och välj sedan **Klar** för att återgå till distributionsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="de8fe-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Distributionsmedgivande](./media/2DeploymentConsent.png)

7. <span data-ttu-id="de8fe-127">Valfritt – Tillämpa demodata på miljön.</span><span class="sxs-lookup"><span data-stu-id="de8fe-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="de8fe-128">Gå till **Avancerade inställningar** väljer du **Anpassa konfiguration av SQL-databas** och ange **Ange en datauppsättning för programdatabas** som **Demo**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="de8fe-129">Fyll i de återstående obligatoriska fälten i guiden och bekräfta distributionen.</span><span class="sxs-lookup"><span data-stu-id="de8fe-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="de8fe-130">Tiden för etablering av miljön varierar beroende på miljötypen.</span><span class="sxs-lookup"><span data-stu-id="de8fe-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="de8fe-131">Etableringen kan ta upp till sex timmar.</span><span class="sxs-lookup"><span data-stu-id="de8fe-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="de8fe-132">När distributionen har slutförts visas miljön som **Distribuerad**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="de8fe-133">Bekräfta att miljön har distribuerats korrekt genom att välja **Inloggning** och logga in i miljön för att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="de8fe-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ miljöinformation](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="de8fe-135">Tillämpa uppdateringar av Finance-miljön</span><span class="sxs-lookup"><span data-stu-id="de8fe-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="de8fe-136">Project Operations kräver en Finance-miljö med programversion **10.0.13 (10.0.569.20009)** eller senare.</span><span class="sxs-lookup"><span data-stu-id="de8fe-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="de8fe-137">Du kan behöva tillämpa kvalitetsuppdateringar av Finance-miljön för att få den här versionen.</span><span class="sxs-lookup"><span data-stu-id="de8fe-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="de8fe-138">I LCS, på sidan **Miljöinformation**, i avsnittet **Tillgängliga uppdateringar**, väljer du **Visa uppdatering**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visa uppdateringar](./media/5ViewUpdates.png)

2. <span data-ttu-id="de8fe-140">På sidan **Binära uppdateringar** väljer du **Spara paket.**</span><span class="sxs-lookup"><span data-stu-id="de8fe-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spara paket](./media/6SavePackage.png)

3. <span data-ttu-id="de8fe-142">Klicka på **Välj alla** och välj sedan **Spara paket**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-142">Click **Select all** and then select **Save package**.</span></span>

![Granska och spara uppdateringar](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="de8fe-144">Ange ett namn och en beskrivning för paketet och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="de8fe-145">Beroende på vilken internetanslutning du har kan processen ta lite tid.</span><span class="sxs-lookup"><span data-stu-id="de8fe-145">Depending on the internet connection, this process might take some time.</span></span>

![Ladda upp paket till resursbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="de8fe-147">När paketet har sparats väljer du **Klart** och sparar det här paketet i resursbiblioteket i LCS-projektet.</span><span class="sxs-lookup"><span data-stu-id="de8fe-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="de8fe-148">Det kan ta ~ 15 minuter att spara och verifiera paketet.</span><span class="sxs-lookup"><span data-stu-id="de8fe-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="de8fe-149">Om du vill tillämpa uppdateringen navigerar du till sidan **Miljöinformation** i LCS och väljer **Upprätthåll** > **Tillämpa uppdateringar**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Upprätthåll miljöer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="de8fe-151">Välj det paket du skapade i listan med uppdateringar och välj **Tillämpa**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Tillämpa uppdateringar](./media/10ApplyUpdates.png)

<span data-ttu-id="de8fe-153">Miljöunderhållet tar lite tid.</span><span class="sxs-lookup"><span data-stu-id="de8fe-153">Environment servicing will take some time.</span></span> <span data-ttu-id="de8fe-154">När det är klart kommer miljön att återgå till ett distribuerat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="de8fe-154">After it is complete, the environment will return to a deployed state.</span></span>

![Miljö distribuerad](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="de8fe-156">Upprätta en anslutning med dubbelskrivning</span><span class="sxs-lookup"><span data-stu-id="de8fe-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="de8fe-157">I ditt LCS-projekt går du till sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="de8fe-158">Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="de8fe-159">När länken är klar väljer du **Länk till CDS for Apps** igen.</span><span class="sxs-lookup"><span data-stu-id="de8fe-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="de8fe-160">Du omdirigeras då till dubbelskrivning i Finance.</span><span class="sxs-lookup"><span data-stu-id="de8fe-160">You will be redirected to Dual Write in Finance.</span></span>

![Länk till CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="de8fe-162">Välj **Tillämpa lösning** för att komma åt de entiteter som ska mappas i integrationen.</span><span class="sxs-lookup"><span data-stu-id="de8fe-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Tillämpa lösningar](./media/13ApplySolutions.png)

5. <span data-ttu-id="de8fe-164">Välj båda lösningarna, **Dynamics 365 Finance and Operations-entitetskarta för dubbelskrivning** och **Dynamics 365 Project Operations-entitetskartor för dubbelskrivning** och välj sedan **Verkställ**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekräfta lösningar](./media/14ConfirmSolutions.png)

<span data-ttu-id="de8fe-166">När lösningarna har tillämpats tillämpas entiteterna med dubbelskrivning i miljön.</span><span class="sxs-lookup"><span data-stu-id="de8fe-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Tillämpa lösningar](./media/15ApplyingSolutions.png)

<span data-ttu-id="de8fe-168">När entiteterna har tillämpats visas alla tillgängliga mappningar i miljön.</span><span class="sxs-lookup"><span data-stu-id="de8fe-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kartor dubbelskrivning](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="de8fe-170">Uppdatera dataentiteterna efter uppdateringen</span><span class="sxs-lookup"><span data-stu-id="de8fe-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="de8fe-171">I Finance går du till arbetsytan **Datahantering**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-171">In Finance, go to the **Data management** workspace.</span></span>

![Datahantering arbetsyta](./media/16DataManagement.png)

2. <span data-ttu-id="de8fe-173">Välj ikonen **Ramverksparametrar**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-173">Select the **Framework parameters** tile.</span></span>

![Ramverksparametrar](./media/17FrameworkParameters.png)

3. <span data-ttu-id="de8fe-175">På sidan **Entitetsinställningar** väljer du **Uppdatera entitetslista**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Uppdatera entitetslista](./media/18RefreshEntityList.png)

<span data-ttu-id="de8fe-177">Uppdateringen ska ta cirka 20 minuter.</span><span class="sxs-lookup"><span data-stu-id="de8fe-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="de8fe-178">Du kommer att få en avisering när den är klar.</span><span class="sxs-lookup"><span data-stu-id="de8fe-178">You will receive an alert when it is complete.</span></span>

![Uppdateringsbekräftelse](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="de8fe-180">Uppdatera säkerhetsinställningarna för Project Operations i Dataverse</span><span class="sxs-lookup"><span data-stu-id="de8fe-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="de8fe-181">Gå till Project Operations i din Dataverse-miljö.</span><span class="sxs-lookup"><span data-stu-id="de8fe-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="de8fe-182">Gå till **Inställningar** > **Säkerhet** > **Säkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="de8fe-183">På sidan **Säkerhetsroller**, i listan över roller, väljer du **Användare av appar för dubbelriktad skrivning** och välj fliken **Anpassade entiteter**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="de8fe-184">Kontrollera att rollen har behörigheterna **Läs** och **Lägg till i** för:</span><span class="sxs-lookup"><span data-stu-id="de8fe-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="de8fe-185">**Växelkurstyp för valuta**</span><span class="sxs-lookup"><span data-stu-id="de8fe-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="de8fe-186">**Kontolista**</span><span class="sxs-lookup"><span data-stu-id="de8fe-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="de8fe-187">**Kalender för räkenskapsår**</span><span class="sxs-lookup"><span data-stu-id="de8fe-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="de8fe-188">**Transaktionsregister**</span><span class="sxs-lookup"><span data-stu-id="de8fe-188">**Ledger**</span></span>

5. <span data-ttu-id="de8fe-189">När säkerhetsrollen uppdateras går du till **Inställningar** > **Säkerhet** > **Teams** och väljer standardteamet i teamvyn **Lokala företagsägare**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="de8fe-190">Välj **Hantera roller** och kontrollera att säkerhetsbehörigheten **Användare av appar för dubbelriktad skrivning** gäller för det här teamet.</span><span class="sxs-lookup"><span data-stu-id="de8fe-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="de8fe-191">Kör kartor för dubbelskrivning i Project Operations</span><span class="sxs-lookup"><span data-stu-id="de8fe-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="de8fe-192">I ditt LCS-projekt går du till sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="de8fe-193">Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="de8fe-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="de8fe-194">När du har valt länken dirigeras du om till listan över entiteter i mappningarna.</span><span class="sxs-lookup"><span data-stu-id="de8fe-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="de8fe-195">Starta kartorna enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="de8fe-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="de8fe-196">Kontrollera att du följer sekvensen enligt anvisningarna nedan.</span><span class="sxs-lookup"><span data-stu-id="de8fe-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="de8fe-197">**Entitetsmappning**</span><span class="sxs-lookup"><span data-stu-id="de8fe-197">**Entity Map**</span></span> | <span data-ttu-id="de8fe-198">**Uppdatera entitet**</span><span class="sxs-lookup"><span data-stu-id="de8fe-198">**Refresh entity**</span></span> | <span data-ttu-id="de8fe-199">**Initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="de8fe-199">**Initial sync**</span></span> | <span data-ttu-id="de8fe-200">**Huvud för initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="de8fe-200">**Master for initial sync**</span></span> | <span data-ttu-id="de8fe-201">**Kör förutsättningar**</span><span class="sxs-lookup"><span data-stu-id="de8fe-201">**Run prerequisites**</span></span> | <span data-ttu-id="de8fe-202">**Förutsättningar initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="de8fe-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="de8fe-203">**Projektresursroller för alla företag (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="de8fe-204">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-204">No</span></span> | <span data-ttu-id="de8fe-205">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-205">Yes</span></span> | <span data-ttu-id="de8fe-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="de8fe-206">Common Data Service</span></span> | <span data-ttu-id="de8fe-207">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-207">No</span></span> | <span data-ttu-id="de8fe-208">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-208">N\A</span></span> |
| <span data-ttu-id="de8fe-209">**Juridiska personer (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="de8fe-210">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-210">No</span></span> | <span data-ttu-id="de8fe-211">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-211">Yes</span></span> | <span data-ttu-id="de8fe-212">Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="de8fe-212">Finance and Operations apps</span></span> | <span data-ttu-id="de8fe-213">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-213">No</span></span> | <span data-ttu-id="de8fe-214">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-214">N\A</span></span> |
| <span data-ttu-id="de8fe-215">**Huvudbok (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="de8fe-216">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-216">No</span></span> | <span data-ttu-id="de8fe-217">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-217">Yes</span></span> | <span data-ttu-id="de8fe-218">Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="de8fe-218">Finance and Operations apps</span></span> | <span data-ttu-id="de8fe-219">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-219">Yes</span></span> | <span data-ttu-id="de8fe-220">Ja, Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="de8fe-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="de8fe-221">**Verkliga värden för Project Operations-integrering (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="de8fe-222">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-222">No</span></span> | <span data-ttu-id="de8fe-223">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-223">No</span></span> | <span data-ttu-id="de8fe-224">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-224">N\A</span></span> | <span data-ttu-id="de8fe-225">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-225">Yes</span></span> | <span data-ttu-id="de8fe-226">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-226">No</span></span> |
| <span data-ttu-id="de8fe-227">**Projektkontraktrader (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="de8fe-228">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-228">No</span></span> | <span data-ttu-id="de8fe-229">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-229">No</span></span> | <span data-ttu-id="de8fe-230">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-230">N\A</span></span> | <span data-ttu-id="de8fe-231">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-231">No</span></span> | <span data-ttu-id="de8fe-232">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-232">No</span></span> |
| <span data-ttu-id="de8fe-233">**Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="de8fe-234">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-234">No</span></span> | <span data-ttu-id="de8fe-235">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-235">No</span></span> | <span data-ttu-id="de8fe-236">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-236">N\A</span></span> | <span data-ttu-id="de8fe-237">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-237">No</span></span> | <span data-ttu-id="de8fe-238">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-238">N\A</span></span> |
| <span data-ttu-id="de8fe-239">**Milstolpar för kontraktrad för Project Operations-integration (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="de8fe-240">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-240">No</span></span> | <span data-ttu-id="de8fe-241">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-241">No</span></span> | <span data-ttu-id="de8fe-242">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-242">N\A</span></span> | <span data-ttu-id="de8fe-243">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-243">No</span></span> | <span data-ttu-id="de8fe-244">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-244">N\A</span></span> |
| <span data-ttu-id="de8fe-245">**Entitet för Project Operations-integration för utgiftsuppskattningar (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="de8fe-246">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-246">No</span></span> | <span data-ttu-id="de8fe-247">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-247">No</span></span> | <span data-ttu-id="de8fe-248">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-248">N\A</span></span> | <span data-ttu-id="de8fe-249">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-249">No</span></span> | <span data-ttu-id="de8fe-250">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-250">N\A</span></span> |
| <span data-ttu-id="de8fe-251">**Entitet för export av projektutgiftkategorier i Project Operations-integration (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="de8fe-252">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-252">No</span></span> | <span data-ttu-id="de8fe-253">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-253">No</span></span> | <span data-ttu-id="de8fe-254">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-254">N\A</span></span> | <span data-ttu-id="de8fe-255">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-255">No</span></span> | <span data-ttu-id="de8fe-256">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-256">N\A</span></span> |
| <span data-ttu-id="de8fe-257">**Entitet för export av projektutgifter i Project Operations-integrering (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="de8fe-258">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-258">Yes</span></span> | <span data-ttu-id="de8fe-259">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-259">No</span></span> | <span data-ttu-id="de8fe-260">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-260">N\A</span></span> | <span data-ttu-id="de8fe-261">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-261">No</span></span> | <span data-ttu-id="de8fe-262">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-262">N\A</span></span> |
| <span data-ttu-id="de8fe-263">**Entitet för Project Operations-integration för tidsuppskattningar (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="de8fe-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="de8fe-264">Ja</span><span class="sxs-lookup"><span data-stu-id="de8fe-264">Yes</span></span> | <span data-ttu-id="de8fe-265">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-265">No</span></span> | <span data-ttu-id="de8fe-266">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-266">N\A</span></span> | <span data-ttu-id="de8fe-267">Inga</span><span class="sxs-lookup"><span data-stu-id="de8fe-267">No</span></span> | <span data-ttu-id="de8fe-268">N\A</span><span class="sxs-lookup"><span data-stu-id="de8fe-268">N\A</span></span> |


4. <span data-ttu-id="de8fe-269">Om du vill uppdatera entiteten väljer du kartnamnet och väljer sedan **Uppdatera entiteter**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Uppdatera karta](./media/20RefreshMapping.png)

5. <span data-ttu-id="de8fe-271">Kör kartan efter att uppdateringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="de8fe-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="de8fe-272">Innan du aktiverar nästa karta ska du kontrollera att kartan i tabellen är i tillståndet **Körs**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="de8fe-273">Det kan ta en stund att köra kartor med ett större antal förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="de8fe-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="de8fe-274">Om du vill köra en karta med förutsättningar ska du aktivera **Visa relaterade entitetskartor**.</span><span class="sxs-lookup"><span data-stu-id="de8fe-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="de8fe-275">Om tabellen anger att **Förutsättning initial synkronisering** är **Nej**, verifierar du att flaggan **Initial synkronisering** är **Av** i alla förutsättningskartor innan du kör den.</span><span class="sxs-lookup"><span data-stu-id="de8fe-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kör karta](./media/21RunMap.png)

6. <span data-ttu-id="de8fe-277">Kontrollera att alla projektrelaterade kartor är i körläge.</span><span class="sxs-lookup"><span data-stu-id="de8fe-277">Validate all project related maps are in the running state.</span></span>

![Alla kartor körs](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="de8fe-279">Använda konfigurationsdata i CDS för Project Operations (valfritt)</span><span class="sxs-lookup"><span data-stu-id="de8fe-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="de8fe-280">Om du har använt demonstrationsdata i Finance-miljön läser du [Konfigurera och tillämpa konfigurationsdata i Common Data Service för Project Operations](resource-apply-pro-setup-config-data.md) för att tillämpa demonstrations data på CDS-miljön.</span><span class="sxs-lookup"><span data-stu-id="de8fe-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="de8fe-281">Project Operations-miljön har nu etablerats och konfigurerats.</span><span class="sxs-lookup"><span data-stu-id="de8fe-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]