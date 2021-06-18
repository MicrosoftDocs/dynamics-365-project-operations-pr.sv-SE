---
title: Etablera en ny miljö
description: I det här ämnet finns information om hur du etablerar en ny Project Operations-miljö.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995508"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="03c1f-103">Etablera en ny miljö</span><span class="sxs-lookup"><span data-stu-id="03c1f-103">Provision a new environment</span></span>

<span data-ttu-id="03c1f-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="03c1f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="03c1f-105">I det här ämnet finns information om hur du tillhandahåller en ny Dynamics 365 Project Operations-miljö för resurser/icke-lagerbaserade scenarier.</span><span class="sxs-lookup"><span data-stu-id="03c1f-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="03c1f-106">Aktivera automatisk etablering av Project Operations i ett LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="03c1f-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="03c1f-107">Följ stegen nedan om du vill aktivera det automatiska etableringsflödet för Project Operations för ditt LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="03c1f-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="03c1f-108">Gå till [LCS](https://lcs.dynamics.com/v2) och välj ikonen **Hantering av förhandsgranskningsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="03c1f-109">I listan **Förhandsgranskningsfunktion** väljer du **Project Operations-funktion** och sedan **Förhandsgranskningsfunktion aktiverad** för att aktivera Project Operations.</span><span class="sxs-lookup"><span data-stu-id="03c1f-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="03c1f-110">Det här steget utförs endast en gång per LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="03c1f-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="03c1f-111">Etablera en Project Operations-miljö</span><span class="sxs-lookup"><span data-stu-id="03c1f-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="03c1f-112">Öppna en ny Dynamics 365 Finance [demomiljö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandbox-miljö/produktionsmiljö](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) distribution.</span><span class="sxs-lookup"><span data-stu-id="03c1f-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="03c1f-113">Gå igenom guiden **Miljöetablering**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="03c1f-114">Kontrollera att den valda programversionen är 10.0.13 eller senare.</span><span class="sxs-lookup"><span data-stu-id="03c1f-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="03c1f-115">Om du vill etablera Project Operations väljer du, under **Avancerade inställningar**, **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="03c1f-116">Aktivera **Common Data Service-inställningen** genom att välja **Ja** och sedan ange information i de obligatoriska fälten:</span><span class="sxs-lookup"><span data-stu-id="03c1f-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="03c1f-117">Namn</span><span class="sxs-lookup"><span data-stu-id="03c1f-117">Name</span></span>
  - <span data-ttu-id="03c1f-118">Region</span><span class="sxs-lookup"><span data-stu-id="03c1f-118">Region</span></span>
  - <span data-ttu-id="03c1f-119">Språk</span><span class="sxs-lookup"><span data-stu-id="03c1f-119">Language</span></span>
  - <span data-ttu-id="03c1f-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="03c1f-120">Currency</span></span>
 
5. <span data-ttu-id="03c1f-121">I fältet **Common Data Service-mall** väljer du **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="03c1f-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="03c1f-122">Välj miljötypen för din distribution.</span><span class="sxs-lookup"><span data-stu-id="03c1f-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="03c1f-123">Med en prenumerationsbaserad utvärderingsversion kan du distribuera en CDS-miljö i 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="03c1f-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Distributionsinställningar](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="03c1f-125">Välj **Godkänn** för att bekräfta tjänstvillkoren och välj sedan **Klar** för att återgå till distributionsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="03c1f-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Distributionsmedgivande](./media/2DeploymentConsent.png)

7. <span data-ttu-id="03c1f-127">Valfritt – Tillämpa demodata på miljön.</span><span class="sxs-lookup"><span data-stu-id="03c1f-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="03c1f-128">Gå till **Avancerade inställningar** väljer du **Anpassa konfiguration av SQL-databas** och ange **Ange en datauppsättning för programdatabas** som **Demo**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="03c1f-129">Fyll i de återstående obligatoriska fälten i guiden och bekräfta distributionen.</span><span class="sxs-lookup"><span data-stu-id="03c1f-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="03c1f-130">Tiden för etablering av miljön varierar beroende på miljötypen.</span><span class="sxs-lookup"><span data-stu-id="03c1f-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="03c1f-131">Etableringen kan ta upp till sex timmar.</span><span class="sxs-lookup"><span data-stu-id="03c1f-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="03c1f-132">När distributionen har slutförts visas miljön som **Distribuerad**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="03c1f-133">Bekräfta att miljön har distribuerats korrekt genom att välja **Inloggning** och logga in i miljön för att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="03c1f-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ miljöinformation](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="03c1f-135">Tillämpa uppdateringar av Finance-miljön</span><span class="sxs-lookup"><span data-stu-id="03c1f-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="03c1f-136">Project Operations kräver en Finance-miljö med programversion **10.0.13 (10.0.569.20009)** eller senare.</span><span class="sxs-lookup"><span data-stu-id="03c1f-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="03c1f-137">Du kan behöva tillämpa kvalitetsuppdateringar av Finance-miljön för att få den här versionen.</span><span class="sxs-lookup"><span data-stu-id="03c1f-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="03c1f-138">I LCS, på sidan **Miljöinformation**, i avsnittet **Tillgängliga uppdateringar**, väljer du **Visa uppdatering**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visa uppdateringar](./media/5ViewUpdates.png)

2. <span data-ttu-id="03c1f-140">På sidan **Binära uppdateringar** väljer du **Spara paket.**</span><span class="sxs-lookup"><span data-stu-id="03c1f-140">On the **Binary updates** page, select **Save package.**</span></span>

![Spara paket](./media/6SavePackage.png)

3. <span data-ttu-id="03c1f-142">Klicka på **Välj alla** och välj sedan **Spara paket**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-142">Click **Select all** and then select **Save package**.</span></span>

![Granska och spara uppdateringar](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="03c1f-144">Ange ett namn och en beskrivning för paketet och välj sedan **Spara**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="03c1f-145">Beroende på vilken internetanslutning du har kan processen ta lite tid.</span><span class="sxs-lookup"><span data-stu-id="03c1f-145">Depending on the internet connection, this process might take some time.</span></span>

![Ladda upp paket till resursbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="03c1f-147">När paketet har sparats väljer du **Klart** och sparar det här paketet i resursbiblioteket i LCS-projektet.</span><span class="sxs-lookup"><span data-stu-id="03c1f-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="03c1f-148">Det kan ta ~ 15 minuter att spara och verifiera paketet.</span><span class="sxs-lookup"><span data-stu-id="03c1f-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="03c1f-149">Om du vill tillämpa uppdateringen navigerar du till sidan **Miljöinformation** i LCS och väljer **Upprätthåll** > **Tillämpa uppdateringar**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Upprätthåll miljöer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="03c1f-151">Välj det paket du skapade i listan med uppdateringar och välj **Tillämpa**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Tillämpa uppdateringar](./media/10ApplyUpdates.png)

<span data-ttu-id="03c1f-153">Miljöunderhållet tar lite tid.</span><span class="sxs-lookup"><span data-stu-id="03c1f-153">Environment servicing will take some time.</span></span> <span data-ttu-id="03c1f-154">När det är klart kommer miljön att återgå till ett distribuerat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="03c1f-154">After it is complete, the environment will return to a deployed state.</span></span>

![Miljö distribuerad](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="03c1f-156">Upprätta en anslutning med dubbelskrivning</span><span class="sxs-lookup"><span data-stu-id="03c1f-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="03c1f-157">I ditt LCS-projekt går du till sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="03c1f-158">Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="03c1f-159">När länken är klar väljer du **Länk till CDS for Apps** igen.</span><span class="sxs-lookup"><span data-stu-id="03c1f-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="03c1f-160">Du omdirigeras då till dubbelskrivning i Finance.</span><span class="sxs-lookup"><span data-stu-id="03c1f-160">You will be redirected to Dual Write in Finance.</span></span>

![Länk till CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="03c1f-162">Välj **Tillämpa lösning** för att komma åt de entiteter som ska mappas i integrationen.</span><span class="sxs-lookup"><span data-stu-id="03c1f-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Tillämpa lösningar](./media/13ApplySolutions.png)

5. <span data-ttu-id="03c1f-164">Välj båda lösningarna, **Dynamics 365 Finance and Operations-entitetskarta för dubbelskrivning** och **Dynamics 365 Project Operations-entitetskartor för dubbelskrivning** och välj sedan **Verkställ**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekräfta lösningar](./media/14ConfirmSolutions.png)

<span data-ttu-id="03c1f-166">När lösningarna har tillämpats tillämpas entiteterna med dubbelskrivning i miljön.</span><span class="sxs-lookup"><span data-stu-id="03c1f-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Tillämpa lösningar](./media/15ApplyingSolutions.png)

<span data-ttu-id="03c1f-168">När entiteterna har tillämpats visas alla tillgängliga mappningar i miljön.</span><span class="sxs-lookup"><span data-stu-id="03c1f-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Kartor dubbelskrivning](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="03c1f-170">Uppdatera dataentiteterna efter uppdateringen</span><span class="sxs-lookup"><span data-stu-id="03c1f-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="03c1f-171">I Finance går du till arbetsytan **Datahantering**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-171">In Finance, go to the **Data management** workspace.</span></span>

![Datahantering arbetsyta](./media/16DataManagement.png)

2. <span data-ttu-id="03c1f-173">Välj ikonen **Ramverksparametrar**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-173">Select the **Framework parameters** tile.</span></span>

![Ramverksparametrar](./media/17FrameworkParameters.png)

3. <span data-ttu-id="03c1f-175">På sidan **Entitetsinställningar** väljer du **Uppdatera entitetslista**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Uppdatera entitetslista](./media/18RefreshEntityList.png)

<span data-ttu-id="03c1f-177">Uppdateringen ska ta cirka 20 minuter.</span><span class="sxs-lookup"><span data-stu-id="03c1f-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="03c1f-178">Du kommer att få en avisering när den är klar.</span><span class="sxs-lookup"><span data-stu-id="03c1f-178">You will receive an alert when it is complete.</span></span>

![Uppdateringsbekräftelse](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="03c1f-180">Uppdatera säkerhetsinställningarna för Project Operations i Dataverse</span><span class="sxs-lookup"><span data-stu-id="03c1f-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="03c1f-181">Gå till Project Operations i din Dataverse-miljö.</span><span class="sxs-lookup"><span data-stu-id="03c1f-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="03c1f-182">Gå till **Inställningar** > **Säkerhet** > **Säkerhetsroller**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="03c1f-183">På sidan **Säkerhetsroller**, i listan över roller, väljer du **Användare av appar för dubbelriktad skrivning** och välj fliken **Anpassade entiteter**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="03c1f-184">Kontrollera att rollen har behörigheterna **Läs** och **Lägg till i** för:</span><span class="sxs-lookup"><span data-stu-id="03c1f-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="03c1f-185">**Växelkurstyp för valuta**</span><span class="sxs-lookup"><span data-stu-id="03c1f-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="03c1f-186">**Kontolista**</span><span class="sxs-lookup"><span data-stu-id="03c1f-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="03c1f-187">**Kalender för räkenskapsår**</span><span class="sxs-lookup"><span data-stu-id="03c1f-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="03c1f-188">**Transaktionsregister**</span><span class="sxs-lookup"><span data-stu-id="03c1f-188">**Ledger**</span></span>

5. <span data-ttu-id="03c1f-189">När säkerhetsrollen uppdateras går du till **Inställningar** > **Säkerhet** > **Teams** och väljer standardteamet i teamvyn **Lokala företagsägare**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="03c1f-190">Välj **Hantera roller** och kontrollera att säkerhetsbehörigheten **Användare av appar för dubbelriktad skrivning** gäller för det här teamet.</span><span class="sxs-lookup"><span data-stu-id="03c1f-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="03c1f-191">Kör kartor för dubbelskrivning i Project Operations</span><span class="sxs-lookup"><span data-stu-id="03c1f-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="03c1f-192">I ditt LCS-projekt går du till sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="03c1f-193">Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="03c1f-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="03c1f-194">När du har valt länken dirigeras du om till listan över entiteter i mappningarna.</span><span class="sxs-lookup"><span data-stu-id="03c1f-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="03c1f-195">Starta kartorna enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="03c1f-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="03c1f-196">Kontrollera att du följer sekvensen enligt anvisningarna nedan.</span><span class="sxs-lookup"><span data-stu-id="03c1f-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="03c1f-197">**Entitetsmappning**</span><span class="sxs-lookup"><span data-stu-id="03c1f-197">**Entity Map**</span></span> | <span data-ttu-id="03c1f-198">**Uppdatera entitet**</span><span class="sxs-lookup"><span data-stu-id="03c1f-198">**Refresh entity**</span></span> | <span data-ttu-id="03c1f-199">**Initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="03c1f-199">**Initial sync**</span></span> | <span data-ttu-id="03c1f-200">**Huvud för initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="03c1f-200">**Master for initial sync**</span></span> | <span data-ttu-id="03c1f-201">**Kör förutsättningar**</span><span class="sxs-lookup"><span data-stu-id="03c1f-201">**Run prerequisites**</span></span> | <span data-ttu-id="03c1f-202">**Förutsättningar initial synkronisering**</span><span class="sxs-lookup"><span data-stu-id="03c1f-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="03c1f-203">**Projektresursroller för alla företag (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="03c1f-204">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-204">No</span></span> | <span data-ttu-id="03c1f-205">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-205">Yes</span></span> | <span data-ttu-id="03c1f-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="03c1f-206">Common Data Service</span></span> | <span data-ttu-id="03c1f-207">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-207">No</span></span> | <span data-ttu-id="03c1f-208">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-208">N\A</span></span> |
| <span data-ttu-id="03c1f-209">**Juridiska personer (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="03c1f-210">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-210">No</span></span> | <span data-ttu-id="03c1f-211">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-211">Yes</span></span> | <span data-ttu-id="03c1f-212">Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="03c1f-212">Finance and Operations apps</span></span> | <span data-ttu-id="03c1f-213">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-213">No</span></span> | <span data-ttu-id="03c1f-214">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-214">N\A</span></span> |
| <span data-ttu-id="03c1f-215">**Huvudbok (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="03c1f-216">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-216">No</span></span> | <span data-ttu-id="03c1f-217">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-217">Yes</span></span> | <span data-ttu-id="03c1f-218">Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="03c1f-218">Finance and Operations apps</span></span> | <span data-ttu-id="03c1f-219">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-219">Yes</span></span> | <span data-ttu-id="03c1f-220">Ja, Finance and Operations-appar</span><span class="sxs-lookup"><span data-stu-id="03c1f-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="03c1f-221">**Verkliga värden för Project Operations-integrering (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="03c1f-222">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-222">No</span></span> | <span data-ttu-id="03c1f-223">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-223">No</span></span> | <span data-ttu-id="03c1f-224">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-224">N\A</span></span> | <span data-ttu-id="03c1f-225">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-225">Yes</span></span> | <span data-ttu-id="03c1f-226">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-226">No</span></span> |
| <span data-ttu-id="03c1f-227">**Projektkontraktrader (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="03c1f-228">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-228">No</span></span> | <span data-ttu-id="03c1f-229">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-229">No</span></span> | <span data-ttu-id="03c1f-230">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-230">N\A</span></span> | <span data-ttu-id="03c1f-231">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-231">No</span></span> | <span data-ttu-id="03c1f-232">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-232">No</span></span> |
| <span data-ttu-id="03c1f-233">**Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="03c1f-234">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-234">No</span></span> | <span data-ttu-id="03c1f-235">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-235">No</span></span> | <span data-ttu-id="03c1f-236">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-236">N\A</span></span> | <span data-ttu-id="03c1f-237">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-237">No</span></span> | <span data-ttu-id="03c1f-238">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-238">N\A</span></span> |
| <span data-ttu-id="03c1f-239">**Milstolpar för kontraktrad för Project Operations-integration (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="03c1f-240">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-240">No</span></span> | <span data-ttu-id="03c1f-241">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-241">No</span></span> | <span data-ttu-id="03c1f-242">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-242">N\A</span></span> | <span data-ttu-id="03c1f-243">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-243">No</span></span> | <span data-ttu-id="03c1f-244">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-244">N\A</span></span> |
| <span data-ttu-id="03c1f-245">**Entitet för Project Operations-integration för utgiftsuppskattningar (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="03c1f-246">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-246">No</span></span> | <span data-ttu-id="03c1f-247">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-247">No</span></span> | <span data-ttu-id="03c1f-248">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-248">N\A</span></span> | <span data-ttu-id="03c1f-249">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-249">No</span></span> | <span data-ttu-id="03c1f-250">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-250">N\A</span></span> |
| <span data-ttu-id="03c1f-251">**Entitet för export av projektutgiftkategorier i Project Operations-integration (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="03c1f-252">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-252">No</span></span> | <span data-ttu-id="03c1f-253">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-253">No</span></span> | <span data-ttu-id="03c1f-254">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-254">N\A</span></span> | <span data-ttu-id="03c1f-255">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-255">No</span></span> | <span data-ttu-id="03c1f-256">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-256">N\A</span></span> |
| <span data-ttu-id="03c1f-257">**Entitet för export av projektutgifter i Project Operations-integrering (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="03c1f-258">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-258">Yes</span></span> | <span data-ttu-id="03c1f-259">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-259">No</span></span> | <span data-ttu-id="03c1f-260">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-260">N\A</span></span> | <span data-ttu-id="03c1f-261">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-261">No</span></span> | <span data-ttu-id="03c1f-262">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-262">N\A</span></span> |
| <span data-ttu-id="03c1f-263">**Entitet för Project Operations-integration för tidsuppskattningar (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="03c1f-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="03c1f-264">Ja</span><span class="sxs-lookup"><span data-stu-id="03c1f-264">Yes</span></span> | <span data-ttu-id="03c1f-265">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-265">No</span></span> | <span data-ttu-id="03c1f-266">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-266">N\A</span></span> | <span data-ttu-id="03c1f-267">Inga</span><span class="sxs-lookup"><span data-stu-id="03c1f-267">No</span></span> | <span data-ttu-id="03c1f-268">N\A</span><span class="sxs-lookup"><span data-stu-id="03c1f-268">N\A</span></span> |


4. <span data-ttu-id="03c1f-269">Om du vill uppdatera entiteten väljer du kartnamnet och väljer sedan **Uppdatera entiteter**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Uppdatera karta](./media/20RefreshMapping.png)

5. <span data-ttu-id="03c1f-271">Kör kartan efter att uppdateringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="03c1f-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="03c1f-272">Innan du aktiverar nästa karta ska du kontrollera att kartan i tabellen är i tillståndet **Körs**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="03c1f-273">Det kan ta en stund att köra kartor med ett större antal förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="03c1f-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="03c1f-274">Om du vill köra en karta med förutsättningar ska du aktivera **Visa relaterade entitetskartor**.</span><span class="sxs-lookup"><span data-stu-id="03c1f-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="03c1f-275">Om tabellen anger att **Förutsättning initial synkronisering** är **Nej**, verifierar du att flaggan **Initial synkronisering** är **Av** i alla förutsättningskartor innan du kör den.</span><span class="sxs-lookup"><span data-stu-id="03c1f-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kör karta](./media/21RunMap.png)

6. <span data-ttu-id="03c1f-277">Kontrollera att alla projektrelaterade kartor är i körläge.</span><span class="sxs-lookup"><span data-stu-id="03c1f-277">Validate all project related maps are in the running state.</span></span>

![Alla kartor körs](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="03c1f-279">Använda konfigurationsdata i CDS för Project Operations (valfritt)</span><span class="sxs-lookup"><span data-stu-id="03c1f-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="03c1f-280">Om du har använt demonstrationsdata i Finance-miljön läser du [Konfigurera och tillämpa konfigurationsdata i Common Data Service för Project Operations](resource-apply-pro-setup-config-data.md) för att tillämpa demonstrations data på CDS-miljön.</span><span class="sxs-lookup"><span data-stu-id="03c1f-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="03c1f-281">Project Operations-miljön har nu etablerats och konfigurerats.</span><span class="sxs-lookup"><span data-stu-id="03c1f-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]