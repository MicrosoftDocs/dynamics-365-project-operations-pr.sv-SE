---
title: Använd tillägget Project Service för att planera ditt arbete i Microsoft Project | Microsoft-dokument
description: I den här ämnet finns information om hur du lägger till, konfigurerar och använder Microsoft Project-tillägget för Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756179"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="7e087-103">Använd Project Service Automation-tillägget för att planera ditt arbete i Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="7e087-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="7e087-104">gör det enklare för dig att göra din projektplanering inklusive uppskattningar.</span><span class="sxs-lookup"><span data-stu-id="7e087-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="7e087-105">Du kan definiera arbetet så att utgifter, arbete och försäljningsvärde är tydliga när det slutliga förslaget skickas in.</span><span class="sxs-lookup"><span data-stu-id="7e087-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="7e087-106">Nu kan du installera [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] och göra planeringen i den välkända miljön i Microsoft Project [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="7e087-107">Använd de stabila funktionerna för planering och hantering av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och uppdatera projektplanen i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7e087-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="7e087-108">För att använda SharePoint-dokumenthanteringsfunktionen i dina [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer för [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt kommer din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratör att aktivera dokumenthantering.</span><span class="sxs-lookup"><span data-stu-id="7e087-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7e087-109">[Aktivera SharePoint dokumenthantering för specifika entiteter](../admin/enable-sharepoint-document-management-specific-entities.md)</span><span class="sxs-lookup"><span data-stu-id="7e087-109">[Enable SharePoint document management for specific entities](../admin/enable-sharepoint-document-management-specific-entities.md)</span></span>  
> - <span data-ttu-id="7e087-110">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] är endast kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="7e087-110">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="7e087-111">Ladda ned och installera tillägg</span><span class="sxs-lookup"><span data-stu-id="7e087-111">Download and install the add-in</span></span>  
 <span data-ttu-id="7e087-112">Ha din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-inloggningsinformation tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="7e087-112">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="7e087-113">Du behöver denna information för att ansluta från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-113">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="7e087-114">Från hämtningscenter kan du hämta tillägget för den version av Project Service som stöds antingen [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="7e087-114">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="7e087-115">Klicka på hämtningslänken.</span><span class="sxs-lookup"><span data-stu-id="7e087-115">Click the download link.</span></span>  

3.  <span data-ttu-id="7e087-116">När hämtningen är klar klickar du på **Ja** för att installera tillägget.</span><span class="sxs-lookup"><span data-stu-id="7e087-116">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="7e087-117">Konfigurera tillägget</span><span class="sxs-lookup"><span data-stu-id="7e087-117">Configure the add-in</span></span>  

1. <span data-ttu-id="7e087-118">Öppna [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och klicka på fliken **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="7e087-118">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="7e087-119">Klicka på **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="7e087-119">Click **Connect**.</span></span>  

3. <span data-ttu-id="7e087-120">Ange din inloggningsinformation och klicka sedan på **logga in**.</span><span class="sxs-lookup"><span data-stu-id="7e087-120">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="7e087-121">Nu kan du börja använda tillägget.</span><span class="sxs-lookup"><span data-stu-id="7e087-121">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="7e087-122">Läsa från en mall</span><span class="sxs-lookup"><span data-stu-id="7e087-122">Read from a template</span></span>  
 <span data-ttu-id="7e087-123">Läsa från en mall som du skapat i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] och kopierat till [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] för att starta din projektplanering.</span><span class="sxs-lookup"><span data-stu-id="7e087-123">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7e087-124">[Skapa en projektmall (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="7e087-124">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1.  <span data-ttu-id="7e087-125">Från fliken **Project Service** klickar du på **Läs** > **Project Service Automation-projektmall**.</span><span class="sxs-lookup"><span data-stu-id="7e087-125">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="7e087-126">Välj en projektmall i listan och klicka sedan på **öppna**.</span><span class="sxs-lookup"><span data-stu-id="7e087-126">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="7e087-127">Som standard ställs aktiviteter som kopieras från mallen till projekt in som manuellt schemalagda.</span><span class="sxs-lookup"><span data-stu-id="7e087-127">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="7e087-128">Tilldela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller till projektresurser</span><span class="sxs-lookup"><span data-stu-id="7e087-128">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="7e087-129">Öppna ett projekt och klicka på menyfliksområdet **Aktivitet**.</span><span class="sxs-lookup"><span data-stu-id="7e087-129">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="7e087-130">Klicka på **Gantt-schemat** -menyn och välj sedan **Resurslista**.</span><span class="sxs-lookup"><span data-stu-id="7e087-130">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="7e087-131">Klicka på Resurslista i listrutan **Resursroller för Project Service** och välj en roll för Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7e087-131">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="7e087-132">Bemanna dina projektet med resurser</span><span class="sxs-lookup"><span data-stu-id="7e087-132">Staff your project with resources</span></span>  

1.  <span data-ttu-id="7e087-133">Från fliken Project Service väljer du en rad och klickar på **Hitta resurser**.</span><span class="sxs-lookup"><span data-stu-id="7e087-133">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="7e087-134">På skärmen **Boka resurs** väljer du den resurs som du vill använda för projektet.</span><span class="sxs-lookup"><span data-stu-id="7e087-134">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="7e087-135">Klicka på **Boka** och sedan på **OK**.</span><span class="sxs-lookup"><span data-stu-id="7e087-135">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="7e087-136">Publicera dina projekt</span><span class="sxs-lookup"><span data-stu-id="7e087-136">Publish your project</span></span>  
<span data-ttu-id="7e087-137">När din projektplanering är klar är nästa steg är att importera och publicera projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-137">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="7e087-138">Projektet kommer att importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-138">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="7e087-139">Prissättning och teamgenerationsprocess tillämpas.</span><span class="sxs-lookup"><span data-stu-id="7e087-139">The pricing and team generation process are applied.</span></span> <span data-ttu-id="7e087-140">Öppna projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] för att se att teamet, projektuppskattningar och uppdelad arbetsstruktur har genererats.</span><span class="sxs-lookup"><span data-stu-id="7e087-140">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="7e087-141">I följande tabell visas var du hittar resultatet:</span><span class="sxs-lookup"><span data-stu-id="7e087-141">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="7e087-142">**Redigera diagram**</span><span class="sxs-lookup"><span data-stu-id="7e087-142">**Gantt Chart**</span></span>   | <span data-ttu-id="7e087-143">Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **uppdelad arbetsstruktur**.</span><span class="sxs-lookup"><span data-stu-id="7e087-143">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="7e087-144">**Resursark**</span><span class="sxs-lookup"><span data-stu-id="7e087-144">**Resource Sheet**</span></span> |   <span data-ttu-id="7e087-145">Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektteammedlemmar**.</span><span class="sxs-lookup"><span data-stu-id="7e087-145">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="7e087-146">**Använd användning**</span><span class="sxs-lookup"><span data-stu-id="7e087-146">**Use Usage**</span></span>    |    <span data-ttu-id="7e087-147">Importerar till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektberäkningar**.</span><span class="sxs-lookup"><span data-stu-id="7e087-147">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="7e087-148">**Importera och publicera projektet**</span><span class="sxs-lookup"><span data-stu-id="7e087-148">**To import and publish your project**</span></span>  
1. <span data-ttu-id="7e087-149">Från fliken **Project Service** klickar du på **Publicera** > **Nytt Project Service Automation-projekt**.</span><span class="sxs-lookup"><span data-stu-id="7e087-149">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="7e087-150">På dialogrutan **publicera ett nytt projekt i Project Service** anger du **projektnamnet** och väljer **kund**.</span><span class="sxs-lookup"><span data-stu-id="7e087-150">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="7e087-151">Du kan också kontrollera **länka projektplanen i Project Service Automation** till länka planen Projektfil till Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7e087-151">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="7e087-152">Klicka på **Publicera**.</span><span class="sxs-lookup"><span data-stu-id="7e087-152">Click **Publish**.</span></span>  

   <span data-ttu-id="7e087-153">Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] till skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="7e087-153">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="7e087-154">Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-154">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="7e087-155">Redigera ett projekt som har importerats</span><span class="sxs-lookup"><span data-stu-id="7e087-155">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="7e087-156">Om du vill göra ändringar i en projektplan som importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] har du två alternativ:</span><span class="sxs-lookup"><span data-stu-id="7e087-156">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="7e087-157">Öppna huvudfilen och redigera den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-157">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="7e087-158">Ta bort länken från huvudfilen och redigera direkt i Project Service.</span><span class="sxs-lookup"><span data-stu-id="7e087-158">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="7e087-159">Som standard är ett projekt som har överförts från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och kan endast redigeras i Project.</span><span class="sxs-lookup"><span data-stu-id="7e087-159">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="7e087-160">Redigera filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], filens länk har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7e087-160">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="7e087-161">Redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="7e087-161">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="7e087-162">I huvudmenyn klickar du på **Project Service** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="7e087-162">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="7e087-163">I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-163">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="7e087-164">Klicka på **öppen i MS Project** från menyfliken.</span><span class="sxs-lookup"><span data-stu-id="7e087-164">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="7e087-165">Detta kommer att öppna den länkade huvudfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-165">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="7e087-166">Ta bort en fil och redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="7e087-166">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="7e087-167">I huvudmenyn klickar du på **Project Service** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="7e087-167">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="7e087-168">I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-168">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="7e087-169">Klicka på **Ta bort länk från MS Project** från menyfliken.</span><span class="sxs-lookup"><span data-stu-id="7e087-169">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="7e087-170">Skicka en projektfil till SharePoint eller Office-grupper</span><span class="sxs-lookup"><span data-stu-id="7e087-170">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="7e087-171">Du kan överföra din projektfil till SharePoint och hitta den under den associerade dokument för ditt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e087-171">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="7e087-172">Din administratör måste konfigurera dokumenthantering för SharePoint och aktivera den för projektentiteten.</span><span class="sxs-lookup"><span data-stu-id="7e087-172">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7e087-173">[Ställ in SharePoint-integrering](../admin/set-up-sharepoint-integration.md)</span><span class="sxs-lookup"><span data-stu-id="7e087-173">[Set up SharePoint integration](../admin/set-up-sharepoint-integration.md)</span></span>  

 <span data-ttu-id="7e087-174">Du kan också överföra projektfilen till [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] om du har Office-grupper inställda.</span><span class="sxs-lookup"><span data-stu-id="7e087-174">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7e087-175">[Samarbeta med dina kolleger med hjälp av Office 365-grupper](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span><span class="sxs-lookup"><span data-stu-id="7e087-175">[Collaborate with your colleagues using Office 365 Groups](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span></span>  

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="7e087-176">Ladda upp en fil för SharePoint</span><span class="sxs-lookup"><span data-stu-id="7e087-176">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="7e087-177">I huvudmenyn klickar du på **Project Service** > **Överför**.</span><span class="sxs-lookup"><span data-stu-id="7e087-177">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="7e087-178">Välj **Till projektdokument i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="7e087-178">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="7e087-179">I dialogrutan **Aktivera öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** väljer du **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="7e087-179">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="7e087-180">När du klickar på **Ja** kommer du att kunna klicka på knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-knappen i Project Service Automation och starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="7e087-180">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="7e087-181">När du klickar på **Nej** kommer länken för knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="7e087-181">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="7e087-182">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e087-182">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="7e087-183">Överför en fil för Office Group</span><span class="sxs-lookup"><span data-stu-id="7e087-183">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="7e087-184">I huvudmenyn klickar du på **Project Service** > **Överför**.</span><span class="sxs-lookup"><span data-stu-id="7e087-184">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="7e087-185">Välj **Till projektdokument i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="7e087-185">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="7e087-186">I dialogrutan **Aktivera öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** väljer du **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="7e087-186">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="7e087-187">När du klickar på **Ja** kommer du att kunna klicka på knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-knappen i Project Service Automation och starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="7e087-187">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="7e087-188">När du klickar på **Nej** kommer länken för knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="7e087-188">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="7e087-189">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="7e087-189">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="7e087-190">Publicera dina projekt som en mall</span><span class="sxs-lookup"><span data-stu-id="7e087-190">Publish  your project as a template</span></span>  
 <span data-ttu-id="7e087-191">Du kan spara projektet och återanvända det genom att spara det som en projektmall i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-191">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="7e087-192">Projektmallar är återanvändbara projektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-192">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="7e087-193">[Skapa en projektmall (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="7e087-193">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1. <span data-ttu-id="7e087-194">Från fliken **Project Service** klickar du på **Publicera** > **Ny Project Service Automation-mall**.</span><span class="sxs-lookup"><span data-stu-id="7e087-194">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="7e087-195">På dialogrutan **publicera ett nytt projekt i Project Service-mall** anger du **Namn på projektmall**.</span><span class="sxs-lookup"><span data-stu-id="7e087-195">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="7e087-196">Du kan också kontrollera **länka projektplanen i Project Service Automation** till länka Projektfil till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-196">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="7e087-197">Klicka på **Publicera**.</span><span class="sxs-lookup"><span data-stu-id="7e087-197">Click **Publish**.</span></span>  

<span data-ttu-id="7e087-198">Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-mallen till skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="7e087-198">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="7e087-199">Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="7e087-199">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="7e087-200">Se även</span><span class="sxs-lookup"><span data-stu-id="7e087-200">See Also</span></span>  
 [<span data-ttu-id="7e087-201">Guiden för projektledare</span><span class="sxs-lookup"><span data-stu-id="7e087-201">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
