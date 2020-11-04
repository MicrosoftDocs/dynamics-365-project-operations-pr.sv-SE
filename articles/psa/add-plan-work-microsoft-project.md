---
title: Använd tillägget Project Service för att planera ditt arbete i Microsoft Project | Microsoft-dokument
description: I den här ämnet finns information om hur du lägger till, konfigurerar och använder Microsoft Project-tillägget för Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085670"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="b9eb0-103">Använd Project Service Automation-tillägget för att planera ditt arbete i Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="b9eb0-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="b9eb0-104">gör det enklare för dig att göra din projektplanering inklusive uppskattningar.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="b9eb0-105">Du kan definiera arbetet så att utgifter, arbete och försäljningsvärde är tydliga när det slutliga förslaget skickas in.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="b9eb0-106">Nu kan du installera [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] och göra planeringen i den välkända miljön i Microsoft Project [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="b9eb0-107">Använd de stabila funktionerna för planering och hantering av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och uppdatera projektplanen i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="b9eb0-108">För att använda SharePoint-dokumenthanteringsfunktionen i dina [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer för [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt kommer din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratör att aktivera dokumenthantering.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="b9eb0-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] är endast kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="b9eb0-110">Ladda ned och installera tillägg</span><span class="sxs-lookup"><span data-stu-id="b9eb0-110">Download and install the add-in</span></span>  
 <span data-ttu-id="b9eb0-111">Ha din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-inloggningsinformation tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="b9eb0-112">Du behöver denna information för att ansluta från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="b9eb0-113">Från hämtningscenter kan du hämta tillägget för den version av Project Service som stöds antingen [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="b9eb0-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="b9eb0-114">Klicka på hämtningslänken.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-114">Click the download link.</span></span>  

3.  <span data-ttu-id="b9eb0-115">När hämtningen är klar klickar du på **Ja** för att installera tillägget.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="b9eb0-116">Konfigurera tillägget</span><span class="sxs-lookup"><span data-stu-id="b9eb0-116">Configure the add-in</span></span>  

1. <span data-ttu-id="b9eb0-117">Öppna [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och klicka på fliken **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="b9eb0-118">Klicka på **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="b9eb0-119">Ange din inloggningsinformation och klicka sedan på **logga in**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="b9eb0-120">Nu kan du börja använda tillägget.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="b9eb0-121">Läsa från en mall</span><span class="sxs-lookup"><span data-stu-id="b9eb0-121">Read from a template</span></span>  
 <span data-ttu-id="b9eb0-122">Läsa från en mall som du skapat i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] och kopierat till [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] för att starta din projektplanering.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b9eb0-123">[Skapa en projektmall (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="b9eb0-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="b9eb0-124">Från fliken **Project Service** klickar du på **Läs** > **Project Service Automation-projektmall**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="b9eb0-125">Välj en projektmall i listan och klicka sedan på **öppna**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="b9eb0-126">Som standard ställs aktiviteter som kopieras från mallen till projekt in som manuellt schemalagda.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="b9eb0-127">Tilldela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller till projektresurser</span><span class="sxs-lookup"><span data-stu-id="b9eb0-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="b9eb0-128">Öppna ett projekt och klicka på menyfliksområdet **Aktivitet**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="b9eb0-129">Klicka på **Gantt-schemat** -menyn och välj sedan **Resurslista**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="b9eb0-130">Klicka på Resurslista i listrutan **Resursroller för Project Service** och välj en roll för Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="b9eb0-131">Bemanna dina projektet med resurser</span><span class="sxs-lookup"><span data-stu-id="b9eb0-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="b9eb0-132">Från fliken Project Service väljer du en rad och klickar på **Hitta resurser**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="b9eb0-133">På skärmen **Boka resurs** väljer du den resurs som du vill använda för projektet.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="b9eb0-134">Klicka på **Boka** och sedan på **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="b9eb0-135">Publicera dina projekt</span><span class="sxs-lookup"><span data-stu-id="b9eb0-135">Publish your project</span></span>  
<span data-ttu-id="b9eb0-136">När din projektplanering är klar är nästa steg är att importera och publicera projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="b9eb0-137">Projektet kommer att importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="b9eb0-138">Prissättning och teamgenerationsprocess tillämpas.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="b9eb0-139">Öppna projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] för att se att teamet, projektuppskattningar och uppdelad arbetsstruktur har genererats.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="b9eb0-140">I följande tabell visas var du hittar resultatet:</span><span class="sxs-lookup"><span data-stu-id="b9eb0-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="b9eb0-141">**Redigera diagram**</span><span class="sxs-lookup"><span data-stu-id="b9eb0-141">**Gantt Chart**</span></span>   | <span data-ttu-id="b9eb0-142">Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **uppdelad arbetsstruktur**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="b9eb0-143">**Resursark**</span><span class="sxs-lookup"><span data-stu-id="b9eb0-143">**Resource Sheet**</span></span> |   <span data-ttu-id="b9eb0-144">Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektteammedlemmar**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="b9eb0-145">**Använd användning**</span><span class="sxs-lookup"><span data-stu-id="b9eb0-145">**Use Usage**</span></span>    |    <span data-ttu-id="b9eb0-146">Importerar till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektberäkningar**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="b9eb0-147">**Importera och publicera projektet**</span><span class="sxs-lookup"><span data-stu-id="b9eb0-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="b9eb0-148">Från fliken **Project Service** klickar du på **Publicera** > **Nytt Project Service Automation-projekt**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="b9eb0-149">På dialogrutan **publicera ett nytt projekt i Project Service** anger du **projektnamnet** och väljer **kund**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="b9eb0-150">Du kan också kontrollera **länka projektplanen i Project Service Automation** till länka planen Projektfil till Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="b9eb0-151">Klicka på **Publicera**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-151">Click **Publish**.</span></span>  

   <span data-ttu-id="b9eb0-152">Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] till skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="b9eb0-153">Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="b9eb0-154">Redigera ett projekt som har importerats</span><span class="sxs-lookup"><span data-stu-id="b9eb0-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="b9eb0-155">Om du vill göra ändringar i en projektplan som importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] har du två alternativ:</span><span class="sxs-lookup"><span data-stu-id="b9eb0-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="b9eb0-156">Öppna huvudfilen och redigera den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="b9eb0-157">Ta bort länken från huvudfilen och redigera direkt i Project Service.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="b9eb0-158">Som standard är ett projekt som har överförts från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och kan endast redigeras i Project.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="b9eb0-159">Redigera filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], filens länk har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="b9eb0-160">Redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="b9eb0-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="b9eb0-161">I huvudmenyn klickar du på **Project Service** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="b9eb0-162">I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="b9eb0-163">Klicka på **öppen i MS Project** från menyfliken.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="b9eb0-164">Detta kommer att öppna den länkade huvudfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="b9eb0-165">Ta bort en fil och redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="b9eb0-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="b9eb0-166">I huvudmenyn klickar du på **Project Service** > **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="b9eb0-167">I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="b9eb0-168">Klicka på **Ta bort länk från MS Project** från menyfliken.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="b9eb0-169">Skicka en projektfil till SharePoint eller Office-grupper</span><span class="sxs-lookup"><span data-stu-id="b9eb0-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="b9eb0-170">Du kan överföra din projektfil till SharePoint och hitta den under den associerade dokument för ditt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="b9eb0-171">Din administratör måste konfigurera dokumenthantering för SharePoint och aktivera den för projektentiteten.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="b9eb0-172">Du kan också överföra projektfilen till [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] om du har Office-grupper inställda.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="b9eb0-173">Ladda upp en fil för SharePoint</span><span class="sxs-lookup"><span data-stu-id="b9eb0-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="b9eb0-174">I huvudmenyn klickar du på **Project Service** > **Överför**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="b9eb0-175">Välj **Till projektdokument i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="b9eb0-176">I dialogrutan **Aktivera öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** väljer du **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="b9eb0-177">När du klickar på **Ja** kommer du att kunna klicka på knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** -knappen i Project Service Automation och starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="b9eb0-178">När du klickar på **Nej** kommer länken för knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="b9eb0-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="b9eb0-180">Överför en fil för Office Group</span><span class="sxs-lookup"><span data-stu-id="b9eb0-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="b9eb0-181">I huvudmenyn klickar du på **Project Service** > **Överför**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="b9eb0-182">Välj **Till projektdokument i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="b9eb0-183">I dialogrutan **Aktivera öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** väljer du **Ja** eller **Nej**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="b9eb0-184">När du klickar på **Ja** kommer du att kunna klicka på knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** -knappen i Project Service Automation och starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="b9eb0-185">När du klickar på **Nej** kommer länken för knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="b9eb0-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="b9eb0-187">Publicera dina projekt som en mall</span><span class="sxs-lookup"><span data-stu-id="b9eb0-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="b9eb0-188">Du kan spara projektet och återanvända det genom att spara det som en projektmall i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="b9eb0-189">Projektmallar är återanvändbara projektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b9eb0-190">[Skapa en projektmall (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="b9eb0-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="b9eb0-191">Från fliken **Project Service** klickar du på **Publicera** > **Ny Project Service Automation-mall**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="b9eb0-192">På dialogrutan **publicera ett nytt projekt i Project Service-mall** anger du **Namn på projektmall**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="b9eb0-193">Du kan också kontrollera **länka projektplanen i Project Service Automation** till länka Projektfil till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="b9eb0-194">Klicka på **Publicera**.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-194">Click **Publish**.</span></span>  

<span data-ttu-id="b9eb0-195">Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-mallen till skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="b9eb0-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="b9eb0-196">Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b9eb0-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="b9eb0-197">Se även</span><span class="sxs-lookup"><span data-stu-id="b9eb0-197">See Also</span></span>  
 [<span data-ttu-id="b9eb0-198">Guiden för projektledare</span><span class="sxs-lookup"><span data-stu-id="b9eb0-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
