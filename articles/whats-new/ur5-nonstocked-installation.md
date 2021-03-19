---
title: Uppdatera Project Operations i din Finance-miljö
description: I detta ämne finns information om hur du uppdaterar Project Operations i din Dynamics 365 Finance-miljö.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5292001"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="dc404-103">Uppdatera Project Operations i din Finance-miljö</span><span class="sxs-lookup"><span data-stu-id="dc404-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="dc404-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="dc404-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="dc404-105">I detta ämne finns information om hur du uppdaterar Dynamics 365 Project Operations i din Dynamics 365 Finance-miljö.</span><span class="sxs-lookup"><span data-stu-id="dc404-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="dc404-106">Det krävs tre procedurer för att uppdatera Project Operations till Uppdatering 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="dc404-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="dc404-107">Importera paketet till förhandsgranskningsprojektet</span><span class="sxs-lookup"><span data-stu-id="dc404-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="dc404-108">Applicera uppdateringen</span><span class="sxs-lookup"><span data-stu-id="dc404-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="dc404-109">Uppdatera din Dataverse-miljö</span><span class="sxs-lookup"><span data-stu-id="dc404-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="dc404-110">Importera paketet till ditt LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="dc404-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="dc404-111">Logga in på [Lifecycle Services (LCS)](https://lcs.dynamics.com/) som projektägare eller miljöansvarig.</span><span class="sxs-lookup"><span data-stu-id="dc404-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="dc404-112">Välj ditt LCS-projekt i listan över projekt.</span><span class="sxs-lookup"><span data-stu-id="dc404-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="dc404-113">På sidan **Projekt**, i gruppen **Miljöer**, öppnar du den miljö som du vill uppdatera.</span><span class="sxs-lookup"><span data-stu-id="dc404-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="dc404-114">Kontrollera att miljön körs.</span><span class="sxs-lookup"><span data-stu-id="dc404-114">Verify that the environment is running.</span></span> <span data-ttu-id="dc404-115">Starta miljön om den inte redan körs.</span><span class="sxs-lookup"><span data-stu-id="dc404-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="dc404-116">I avsnittet **Ny version**, under **Tillgängliga uppdateringar**, väljer du **Visa uppdatering** för 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="dc404-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Visa uppdateringsknappen](media/view-update.png)

6. <span data-ttu-id="dc404-118">På sidan **Binära uppdateringar** väljer du **Spara paket**.</span><span class="sxs-lookup"><span data-stu-id="dc404-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="dc404-119">På sidan **Granska och spara uppdateringar** väljer du **Spara paket**.</span><span class="sxs-lookup"><span data-stu-id="dc404-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="dc404-120">I fönstret **Spara paket i tillgångsbibliotek** som visas anger du paketets namn och väljer sedan **Spara paket**.</span><span class="sxs-lookup"><span data-stu-id="dc404-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="dc404-121">När LCS har slutat spara paketet aktiveras knappen **Klar**.</span><span class="sxs-lookup"><span data-stu-id="dc404-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="dc404-122">Välj **Utfört**.</span><span class="sxs-lookup"><span data-stu-id="dc404-122">Select **Done**.</span></span> <span data-ttu-id="dc404-123">LCS verifierar paketet.</span><span class="sxs-lookup"><span data-stu-id="dc404-123">LCS will verify the package.</span></span> <span data-ttu-id="dc404-124">Verifieringen kan ta allt mellan några minuter och upp till en timme.</span><span class="sxs-lookup"><span data-stu-id="dc404-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="dc404-125">Verkställ paketuppdateringen</span><span class="sxs-lookup"><span data-stu-id="dc404-125">Apply the package update</span></span>

1. <span data-ttu-id="dc404-126">På sidan **Miljöinformation** i LCs väljer du **Underhåll** > **Verkställ uppdateringar**.</span><span class="sxs-lookup"><span data-stu-id="dc404-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="dc404-127">Välj det paket du sparade tidigare i listan och välj Sedan **Verkställ**.</span><span class="sxs-lookup"><span data-stu-id="dc404-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="dc404-128">Markera **Ja** om du vill bekräfta att du vill distribuera paketet.</span><span class="sxs-lookup"><span data-stu-id="dc404-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Dialogrutan Bekräfta paketdistribution](media/confirm-package-deployment.png)

4. <span data-ttu-id="dc404-130">Markera **Ja** om du vill bekräfta att du vill uppdatera programmet.</span><span class="sxs-lookup"><span data-stu-id="dc404-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Dialogrutan Bekräfta programuppdatering](media/confirm-application-update.png)

<span data-ttu-id="dc404-132">Distributionen och programuppdateringen startar.</span><span class="sxs-lookup"><span data-stu-id="dc404-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="dc404-133">På sidan **Miljöinformation** uppdateras miljöstatusen till **Underhåll** i det övre högra hörnet.</span><span class="sxs-lookup"><span data-stu-id="dc404-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="dc404-134">Uppdateringen kommer att slutföras på cirka två timmar.</span><span class="sxs-lookup"><span data-stu-id="dc404-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="dc404-135">Programmets versionsinformation uppdateras till **Microsoft Dynamics 365 for Finance and Operations 10.0.15** och miljöstatusen uppdateras till **Distribuerad**.</span><span class="sxs-lookup"><span data-stu-id="dc404-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="dc404-136">Uppdatera din Dataverse-miljö</span><span class="sxs-lookup"><span data-stu-id="dc404-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="dc404-137">Logga in på [Power Platform administratörscenter](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="dc404-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="dc404-138">Leta upp och öppna den miljö du använde för att installera Project Operations i listan.</span><span class="sxs-lookup"><span data-stu-id="dc404-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="dc404-139">På sidan **Miljöer** väljer du **Resurs** > **Dynamics 365-appar**.</span><span class="sxs-lookup"><span data-stu-id="dc404-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="dc404-140">Leta upp **Microsoft Dynamics 365 Project Operations** i listan. I kolumnen **Status** väljer du **Uppdatering finns**.</span><span class="sxs-lookup"><span data-stu-id="dc404-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="dc404-141">Markera kryssrutan **Jag godkänner användarvillkoren** och välj sedan **Uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="dc404-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="dc404-142">Den senaste versionen av lösningen installeras.</span><span class="sxs-lookup"><span data-stu-id="dc404-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="dc404-143">När installationen är färdig har du version 4.5.0.134 installerad.</span><span class="sxs-lookup"><span data-stu-id="dc404-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="dc404-144">Konfigurera nya funktioner</span><span class="sxs-lookup"><span data-stu-id="dc404-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="dc404-145">Aktivera mappning för dubbelskrivning</span><span class="sxs-lookup"><span data-stu-id="dc404-145">Enable dual-write mapping</span></span>

<span data-ttu-id="dc404-146">När du har slutfört uppdateringen för Finance- och Dataverse-miljöer kan du aktivera de nödvändiga mappningarna för dubbelskrivning.</span><span class="sxs-lookup"><span data-stu-id="dc404-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="dc404-147">Slutför följande procedurer för att aktivera mappningar för dubbelskrivning:</span><span class="sxs-lookup"><span data-stu-id="dc404-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="dc404-148">Uppdatera säkerhetsinställningar i Customer Engagement-miljön</span><span class="sxs-lookup"><span data-stu-id="dc404-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="dc404-149">Uppdatera dataentiteter</span><span class="sxs-lookup"><span data-stu-id="dc404-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="dc404-150">Uppdatera och kör mappningarna för dubbel skrivning</span><span class="sxs-lookup"><span data-stu-id="dc404-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="dc404-151">Uppdatera säkerhetsinställningar i Dataverse-miljön</span><span class="sxs-lookup"><span data-stu-id="dc404-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="dc404-152">Följande uppdateringar av säkerhetsprivilegier för entiteter krävs som en del av uppdateringen till UR5.</span><span class="sxs-lookup"><span data-stu-id="dc404-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="dc404-153">I din Dataverse-miljö går du till **Inställningar**. I gruppen **System** väljer du **Säkerhet**.</span><span class="sxs-lookup"><span data-stu-id="dc404-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Inställningar för Dataverse-miljö](media/Picture21.png)

2. <span data-ttu-id="dc404-155">Välj **säkerhetsroller**</span><span class="sxs-lookup"><span data-stu-id="dc404-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="dc404-156">I listan över roller väljer du **Användare av appar för dubbelriktad skrivning** och sedan fliken **Anpassade entiteter**.</span><span class="sxs-lookup"><span data-stu-id="dc404-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="dc404-157">Kontrollera att rollen har behörigheterna **Läs** och **Lägg till i** för:</span><span class="sxs-lookup"><span data-stu-id="dc404-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="dc404-158">**Växelkurstyp för valuta**</span><span class="sxs-lookup"><span data-stu-id="dc404-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="dc404-159">**Kontolista**</span><span class="sxs-lookup"><span data-stu-id="dc404-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="dc404-160">**Kalender för räkenskapsår**</span><span class="sxs-lookup"><span data-stu-id="dc404-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="dc404-161">**Transaktionsregister**</span><span class="sxs-lookup"><span data-stu-id="dc404-161">**Ledger**</span></span>

5. <span data-ttu-id="dc404-162">När säkerhetsrollen uppdateras går du till **Inställningar** > **Säkerhet** > **Teams**.</span><span class="sxs-lookup"><span data-stu-id="dc404-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="dc404-163">Kontrollera att rollen **Användare av appar för dubbelriktad skrivning** har tillämpats på teamet.</span><span class="sxs-lookup"><span data-stu-id="dc404-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="dc404-164">Uppdatera dataentiteter från uppdateringen</span><span class="sxs-lookup"><span data-stu-id="dc404-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="dc404-165">Öppna arbetsytan **Datahantering** i Finance-miljön, och öppna sedan sidan **Ramverksparametrar**.</span><span class="sxs-lookup"><span data-stu-id="dc404-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="dc404-166">I fliken **Entitetsinställningar** väljer du **Uppdatera entitetslista**.</span><span class="sxs-lookup"><span data-stu-id="dc404-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="dc404-167">Bekräfta entitetsuppdateringen genom att välja **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="dc404-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="dc404-168">Processen tar cirka 20 minuter att genomföra.</span><span class="sxs-lookup"><span data-stu-id="dc404-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="dc404-169">Du meddelas när uppdateringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="dc404-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="dc404-170">Uppdatera mappningar för dubbelskrivning</span><span class="sxs-lookup"><span data-stu-id="dc404-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="dc404-171">I arbetsytan **Datahantering** väljer du **Dubbel skrivning**.</span><span class="sxs-lookup"><span data-stu-id="dc404-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="dc404-172">Välj **Tillämpa lösningar**, markera båda lösningarna i listan och välj Sedan **Bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="dc404-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="dc404-173">På sidan **Dubbelskrivning** markerar du följande tabellmappningar och väljer sedan **Stoppa**.</span><span class="sxs-lookup"><span data-stu-id="dc404-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="dc404-174">**Faktiska värden för Project Operations-integrering (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="dc404-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="dc404-175">**Utgiftskategorier för integreringsprojekt för Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="dc404-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="dc404-176">**Exportentitet för faktiska projektutgifter för Project Operations-integrering (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="dc404-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="dc404-177">På sidan **Tabellmappningsversion** tillämpar du en ny version av mappningen på respektive av de tre entiteterna.</span><span class="sxs-lookup"><span data-stu-id="dc404-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="dc404-178">På sidan **Dubbelriktad skrivning** väljer du Kör för att starta om mappningarna.</span><span class="sxs-lookup"><span data-stu-id="dc404-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="dc404-179">I mappningslistan väljer du mappningen **Huvudbok (msdyn_ledgers)** med alla obligatoriska delar och väljer sedan kryssrutan **Initial synkc**.</span><span class="sxs-lookup"><span data-stu-id="dc404-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="dc404-180">I fältet **Master för initial synk** väljer du **Finance and Operations-appar** och sedan **Kör**.</span><span class="sxs-lookup"><span data-stu-id="dc404-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synkronisering av huvudboksmappning](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]