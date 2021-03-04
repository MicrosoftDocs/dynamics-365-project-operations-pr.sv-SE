---
title: Felsöka arbete i uppgiftsrutnätet
description: Detta ämne ger felsökningsinformation som behövs när du arbetar i uppgiftsrutnätet.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031559"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="8d61a-103">Felsöka arbete i uppgiftsrutnätet</span><span class="sxs-lookup"><span data-stu-id="8d61a-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="8d61a-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="8d61a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d61a-105">Detta ämne beskriver hur du åtgärdar problem som kan uppstå när du arbetar med kostnadshantering.</span><span class="sxs-lookup"><span data-stu-id="8d61a-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="8d61a-106">Aktivera cookies</span><span class="sxs-lookup"><span data-stu-id="8d61a-106">Enable cookies</span></span>

<span data-ttu-id="8d61a-107">För Project Operations krävs att tredjeparts-cookies aktiveras för att den uppdelade arbetsstrukturen ska kunna återges.</span><span class="sxs-lookup"><span data-stu-id="8d61a-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="8d61a-108">När cookies från tredje part inte är aktiverade visas en tom sida i stället för uppgifter när du väljer fliken **Uppgifter** på sidan **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tom flik när cookies från tredje part inte är aktiverade](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="8d61a-110">Lösning</span><span class="sxs-lookup"><span data-stu-id="8d61a-110">Workaround</span></span>
<span data-ttu-id="8d61a-111">För Microsoft Edge eller Google Chrome-webbläsare beskriver följande förfaranden hur du uppdaterar dina webbläsarinställningar i syfte att aktivera cookies från tredje part.</span><span class="sxs-lookup"><span data-stu-id="8d61a-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="8d61a-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8d61a-112">Microsoft Edge</span></span>

1. <span data-ttu-id="8d61a-113">Öppna din Edge-webbläsare.</span><span class="sxs-lookup"><span data-stu-id="8d61a-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="8d61a-114">I det övre högra hörnet väljer du **ellipsen** (...) och sedan **Inställningar**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="8d61a-115">Under **Cookies och webbplatsbehörigheter** väljer du **Cookies och webbplatsdata**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="8d61a-116">Inaktivera **Blockera cookies från tredje part**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="8d61a-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="8d61a-117">Google Chrome</span></span>

1. <span data-ttu-id="8d61a-118">Öppna Chrome-webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="8d61a-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="8d61a-119">Välj de tre vertikala punkterna i det övre högra hörnet och välj sedan **Inställningar**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="8d61a-120">Under **Sekretess och säkerhet** väljer du **Cookies och annan webbplatsdata**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="8d61a-121">Välj **Tillåt alla cookies**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d61a-122">Om du blockerar cookies från tredje part blockeras alla cookies och webbplatsdata från andra webbplatser, även om webbplatsen är tillåten i undantagslistan.</span><span class="sxs-lookup"><span data-stu-id="8d61a-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="8d61a-123">PEX-slutpunkt</span><span class="sxs-lookup"><span data-stu-id="8d61a-123">PEX Endpoint</span></span>

<span data-ttu-id="8d61a-124">För Project Operations krävs att en projektparameter refererar till PEX-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="8d61a-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="8d61a-125">Denna slutpunkt krävs för att kommunicera med den tjänst som används för att återge den uppdelade arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="8d61a-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="8d61a-126">Om parametern inte är aktiverad visas felmeddelandet "Projektparametern är inte giltig".</span><span class="sxs-lookup"><span data-stu-id="8d61a-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="8d61a-127">Lösning</span><span class="sxs-lookup"><span data-stu-id="8d61a-127">Workaround</span></span>
 ![Fältet för PEX-slutpunkt i projektparametern](media/projectparameter.png)

1. <span data-ttu-id="8d61a-129">Lägg till fältet **PEX-slutpunkt** på sidan **Projektparametrar**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="8d61a-130">Uppdatera fältet med följande värde: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="8d61a-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="8d61a-131">Ta bort fältet från sidan **Projektparametrar**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="8d61a-132">Privilegier för projekt för webben</span><span class="sxs-lookup"><span data-stu-id="8d61a-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="8d61a-133">Project Operations förlitar sig på en extern schemaläggningstjänst.</span><span class="sxs-lookup"><span data-stu-id="8d61a-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="8d61a-134">Tjänsten kräver att en användare har flera roller tilldelade för att att läsa och skriva till entiteter relaterade till den uppdelade arbetsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="8d61a-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="8d61a-135">Dessa entiteter omfattar projektuppgifter, resurstilldelningar och aktivitetsberoenden.</span><span class="sxs-lookup"><span data-stu-id="8d61a-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="8d61a-136">Om en användare inte kan rendera den uppdelade arbetsstrukturen när han eller hon går till fliken **Uppgifter** beror detta förmodligen på att Project Operations inte har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="8d61a-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="8d61a-137">En användare kan få antingen ett säkerhetsrollsfel eller ett fel relaterat till nekad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="8d61a-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="8d61a-138">Lösning</span><span class="sxs-lookup"><span data-stu-id="8d61a-138">Workaround</span></span>

1. <span data-ttu-id="8d61a-139">Gå till **Inställning > Säkerhet > Användare > Programanvändare**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Programläsare](media/applicationuser.jpg)
   
2. <span data-ttu-id="8d61a-141">Dubbelklicka på programanvändarposten för att bekräfta följande:</span><span class="sxs-lookup"><span data-stu-id="8d61a-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="8d61a-142">Användaren har åtkomst till projektet.</span><span class="sxs-lookup"><span data-stu-id="8d61a-142">The user has access to the project.</span></span> <span data-ttu-id="8d61a-143">Verifieringen sker oftast genom att användaren innehar säkerhetsrollen **Projektansvarig**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="8d61a-144">Microsoft Project-programmets användare finns och är korrekt konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="8d61a-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="8d61a-145">Om denna användare inte finns kan du skapa en ny användarpost.</span><span class="sxs-lookup"><span data-stu-id="8d61a-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="8d61a-146">Välj **Ny användare**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-146">Select **New Users**.</span></span> <span data-ttu-id="8d61a-147">Ändra postformuläret till **Programanvändare** och lägg sedan till **Program-ID**.</span><span class="sxs-lookup"><span data-stu-id="8d61a-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Information om programanvändare](media/applicationuserdetails.jpg)

4. <span data-ttu-id="8d61a-149">Kontrollera att användaren har tilldelats rätt licens och att tjänsten är aktiverad i serviceplaninformationen för licensen.</span><span class="sxs-lookup"><span data-stu-id="8d61a-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="8d61a-150">Kontrollera att användaren kan öppna project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8d61a-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="8d61a-151">Kontrollera genom projektparametrarna att systemet pekar på rätt projektslutpunkt.</span><span class="sxs-lookup"><span data-stu-id="8d61a-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="8d61a-152">Kontrollera att projektprogrammets användare har skapats.</span><span class="sxs-lookup"><span data-stu-id="8d61a-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="8d61a-153">Tillämpa följande säkerhetsroller på användaren:</span><span class="sxs-lookup"><span data-stu-id="8d61a-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="8d61a-154">Användare av Dataverse</span><span class="sxs-lookup"><span data-stu-id="8d61a-154">Dataverse User</span></span>
  - <span data-ttu-id="8d61a-155">Project Operations-systemet</span><span class="sxs-lookup"><span data-stu-id="8d61a-155">Project Operations System</span></span>
  - <span data-ttu-id="8d61a-156">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="8d61a-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="8d61a-157">Fel vid uppdatering av uppdelad arbetsstruktur</span><span class="sxs-lookup"><span data-stu-id="8d61a-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="8d61a-158">När en eller flera uppdateringar görs i den uppdelade arbetsstrukturen misslyckas ändringarna och sparas inte.</span><span class="sxs-lookup"><span data-stu-id="8d61a-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="8d61a-159">Ett fel uppstår i schemarutnätet och meddelandet "Det gick inte att spara den senaste ändringen du har gjort" visas.</span><span class="sxs-lookup"><span data-stu-id="8d61a-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="8d61a-160">Lösning</span><span class="sxs-lookup"><span data-stu-id="8d61a-160">Workaround</span></span>

1. <span data-ttu-id="8d61a-161">Kontrollera att användaren har tilldelats rätt licens och att tjänsten är aktiverad i serviceplaninformationen för licensen.</span><span class="sxs-lookup"><span data-stu-id="8d61a-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="8d61a-162">Kontrollera att användaren kan öppna project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8d61a-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="8d61a-163">Kontrollera att systemet pekar på rätt projektslutpunkt.</span><span class="sxs-lookup"><span data-stu-id="8d61a-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="8d61a-164">Kontrollera att projektprogrammets användare har skapats.</span><span class="sxs-lookup"><span data-stu-id="8d61a-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="8d61a-165">Tillämpa följande säkerhetsroller på användaren:</span><span class="sxs-lookup"><span data-stu-id="8d61a-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="8d61a-166">Dataverse-användare eller basanvändare</span><span class="sxs-lookup"><span data-stu-id="8d61a-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="8d61a-167">Project Operations-systemet</span><span class="sxs-lookup"><span data-stu-id="8d61a-167">Project Operations System</span></span>
  - <span data-ttu-id="8d61a-168">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="8d61a-168">Project System</span></span>
  - <span data-ttu-id="8d61a-169">Dubbelskrivningssystem för Project Operations (denna roll krävs om du distribuerar det resurs-/icke-lagerbaserade scenariot för Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="8d61a-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
