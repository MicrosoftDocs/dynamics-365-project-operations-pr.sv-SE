---
title: Hur anpassar jag affärsprocessflödet för projektstadier?
description: En översikt om hur jag anpassar affärsprocessflödet för projektstadier.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085726"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="138b4-103">Hur anpassar jag affärsprocessflödet för projektstadier?</span><span class="sxs-lookup"><span data-stu-id="138b4-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="138b4-104">Det finns en känd begränsning i tidigare versioner av Project Service-programmet, nämligen att namnen på stadier i affärsprocessflödet för projektstadier måste matcha förväntade engelska namn exakt ( **Quote** , **Plan** , **Close** ).</span><span class="sxs-lookup"><span data-stu-id="138b4-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names ( **Quote** , **Plan** , **Close** ).</span></span> <span data-ttu-id="138b4-105">I annat fall fungerar affärslogiken, som är beroende av de engelska stadiernas namn, inte som förväntat.</span><span class="sxs-lookup"><span data-stu-id="138b4-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="138b4-106">Därför visas inga välbekanta åtgärder som till exempel **Växla process** eller **Redigera process** som finns i projektformuläret, och du uppmuntras inte till att anpassa affärsprocessflödet.</span><span class="sxs-lookup"><span data-stu-id="138b4-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="138b4-107">Den här begränsningen har åtgärdats i version 2.4.5.48 eller senare.</span><span class="sxs-lookup"><span data-stu-id="138b4-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="138b4-108">Denna artikel innehåller rekommenderade lösningar om du vill anpassa det förvalda affärsprocessflödet för tidigare versioner.</span><span class="sxs-lookup"><span data-stu-id="138b4-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="138b4-109">Affärslogik kräver en exakt matchning med engelska stadienamn</span><span class="sxs-lookup"><span data-stu-id="138b4-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="138b4-110">Affärsprocessflödet för projektstadier innehåller affärslogik som ligger till grund för följande problem i programmet:</span><span class="sxs-lookup"><span data-stu-id="138b4-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="138b4-111">När projektet är kopplat till en offert anger koden affärsprocessflödet som stadiet **Quote** (offert).</span><span class="sxs-lookup"><span data-stu-id="138b4-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="138b4-112">När projektet är kopplat till ett kontrakt anger koden affärsprocessflödet till stadiet **Plan**.</span><span class="sxs-lookup"><span data-stu-id="138b4-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="138b4-113">När affärsprocessflödet nått stadiet **Close** (stäng) kommer projektposten att inaktiveras.</span><span class="sxs-lookup"><span data-stu-id="138b4-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="138b4-114">När projektet inaktiveras skrivskyddas projektformulär och uppdelad arbetsstruktur (WBS), namngivna resursbokningar frisläpps och alla kopplade prislistor inaktiveras.</span><span class="sxs-lookup"><span data-stu-id="138b4-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="138b4-115">Denna affärslogik vilar på de engelska namnen på projektstadierna.</span><span class="sxs-lookup"><span data-stu-id="138b4-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="138b4-116">Detta beroende av de engelska stadienamnen är huvudorsaken till varför anpassning av projektstadiernas affärsprocessflöde inte uppmuntras, samt även varför du inte ser de vanliga åtgärderna för affärsprocessflöde som till exempel **Växla process** eller **Redigera process** i projektentiteten.</span><span class="sxs-lookup"><span data-stu-id="138b4-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="138b4-117">Vad händer om stadienamnen inte överensstämmer med de engelska namnen?</span><span class="sxs-lookup"><span data-stu-id="138b4-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="138b4-118">I Project Service-programversion 1.x på plattformen 8.2 gäller följande: När stadienamnen i affärsprocessflödet inte matchar de engelska stadienamnen exakt, kommer den affärslogik som anger rätt stadium för offerter eller kontrakt, eller som stänger projektet, att hoppas över.</span><span class="sxs-lookup"><span data-stu-id="138b4-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="138b4-119">Inga felmeddelanden visas.</span><span class="sxs-lookup"><span data-stu-id="138b4-119">No error messages are displayed.</span></span> <span data-ttu-id="138b4-120">Därför verkar det som att du kan anpassa affärsprocessflödet för projektstadier.</span><span class="sxs-lookup"><span data-stu-id="138b4-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="138b4-121">Inga automatiska processer för offerter, kontrakt och projektstängning kommer emellertid att fungera.</span><span class="sxs-lookup"><span data-stu-id="138b4-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="138b4-122">I appen Project Service, version 2.4.4.30 eller tidigare på plattform 9.0 genomfördes en omfattande strukturell förändring i affärsprocessflödet som krävde en omskrivning av affärslogiken för affärsprocessflöde.</span><span class="sxs-lookup"><span data-stu-id="138b4-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="138b4-123">Som ett resultat av detta får du ett felmeddelande om namnen i processtadiet inte matchar de förväntade engelska namnen.</span><span class="sxs-lookup"><span data-stu-id="138b4-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="138b4-124">Om du vill anpassa affärsprocessflödet för projektstadier för projektentiteten kan du därför endast lägga till helt nya stadier i det förvalda affärsprocessflödet för projektentiteten, medan stadierna **Quote** , **Plan** och **Close** förblir som de är.</span><span class="sxs-lookup"><span data-stu-id="138b4-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote** , **Plan** , and **Close** stages as-is.</span></span> <span data-ttu-id="138b4-125">Denna begränsning säkerställer att du inte får några felmeddelanden från den affärslogik som förväntar sig engelska stadienamn i affärsprocessflödet.</span><span class="sxs-lookup"><span data-stu-id="138b4-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="138b4-126">I en version 2.4.5.48 eller senare har den affärslogik som beskrivs i den här artikeln tagits bort från det förvalda affärsprocessflödet för projektentiteten.</span><span class="sxs-lookup"><span data-stu-id="138b4-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="138b4-127">Om du uppgraderar till den versionen eller senare kan du anpassa eller ersätta det förvalda affärsprocessflödet med ett eget.</span><span class="sxs-lookup"><span data-stu-id="138b4-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="138b4-128">Lösningar för tidigare versioner</span><span class="sxs-lookup"><span data-stu-id="138b4-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="138b4-129">Om uppgradering inte utgör ett alternativ kan du anpassa affärsprocessflödet för projektstadier för projektentiteten på ett av följande två sätt:</span><span class="sxs-lookup"><span data-stu-id="138b4-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="138b4-130">Lägg till fler stadier i standardkonfigurationen samtidigt som du behåller de engelska stadienamnen **Quote** , **Plan** och **Close**.</span><span class="sxs-lookup"><span data-stu-id="138b4-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote** , **Plan** , and **Close**.</span></span>


![Skärmbild på hur du lägger till stadier i standardkonfiguration](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="138b4-132">Skapa ett eget affärsprocessflöde och gör det till primärt affärsprocessflöde för projektentiteten projekt, vilket gör att du kan få alla stadienamn du vill.</span><span class="sxs-lookup"><span data-stu-id="138b4-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="138b4-133">Om du emellertid vill använda samma standardprojektstadier ( **Quote** , **Plan** och **Close** ) måste du göra vissa anpassningar som baseras på dina anpassade stadienamn.</span><span class="sxs-lookup"><span data-stu-id="138b4-133">However, if you want to use the same standard project stages **Quote** , **Plan** , and **Close** , you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="138b4-134">Den mer komplexa logiken finns i nedstängningen av projektet, något som du fortfarande kan utlösa genom att helt enkelt inaktivera projektposten.</span><span class="sxs-lookup"><span data-stu-id="138b4-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF-anpassning](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="138b4-136">Ytterligare överväganden programmet Project Service i version 2.4.4.30 eller tidigare på plattformen 9.0</span><span class="sxs-lookup"><span data-stu-id="138b4-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="138b4-137">I Project Service 2.4.4.30 eller tidigare på plattformen 9.0 kommer fältet **Stadienamn** på den projektentitet som används i listan **Projekt efter fas** samt projektlistvyer inte att uppdateras med ett anpassat affärsprocessflöde, detta eftersom det är kopplat till det förvalda affärsprocessflödet för projektstadier.</span><span class="sxs-lookup"><span data-stu-id="138b4-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="138b4-138">Du kan åtgärda detta problem genom att vidta följande steg:</span><span class="sxs-lookup"><span data-stu-id="138b4-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="138b4-139">Lägg till ett anpassat fält för att registrera det aktuella stadiet för affärsprocessflöde som uppdateras när användaren fortsätter genom det anpassade affärsprocessflödet.</span><span class="sxs-lookup"><span data-stu-id="138b4-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="138b4-140">Ändra diagrammet **Projekt efter stadium** om du vill arbeta med ditt anpassade fält i stället för standardkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="138b4-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="138b4-141">Steg för att skapa ditt eget affärsprocessflöde för projektentiteten</span><span class="sxs-lookup"><span data-stu-id="138b4-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="138b4-142">För att skapa ditt eget affärsprocessflöde för projektentiteten, gör följande:</span><span class="sxs-lookup"><span data-stu-id="138b4-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="138b4-143">Gå till **Inställningar** > **Processcenter**.</span><span class="sxs-lookup"><span data-stu-id="138b4-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="138b4-144">Kopiera inte affärsprocessflödet för projektstadier eftersom affärslogiken för Project Service då kopieras.</span><span class="sxs-lookup"><span data-stu-id="138b4-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Skapa process](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="138b4-146">Använd processdesignern för att skapa de stadienamn du vill.</span><span class="sxs-lookup"><span data-stu-id="138b4-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="138b4-147">Om du vill ha samma funktioner som standardstadierna för **Quote** , **Plan** och **Stäng** måste du skapa detta utifrån stadienamnen på dina anpassade affärsprocessflöden.</span><span class="sxs-lookup"><span data-stu-id="138b4-147">If you want the same functionality as the default stages for **Quote** , **Plan** , and **Close** , you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Skärmbild av den processdesigner som används för att anpassa BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="138b4-149">I processdesignern klickar du på **Processflöde för order** att göra det anpassade affärsprocessflödet till primärt affärsprocessflöde för projektentiteten genom att flytta den ovanför affärsprocessflödet för projektstadier och överst i listan.</span><span class="sxs-lookup"><span data-stu-id="138b4-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="138b4-150">Skärmbild på orderprocessflöde</span><span class="sxs-lookup"><span data-stu-id="138b4-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="138b4-151">Följande åtgärder gäller programmet Project Service version 2.4.4.30 eller tidigare på 9.0-plattformen</span><span class="sxs-lookup"><span data-stu-id="138b4-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="138b4-152">Lägg till ett nytt anpassat fält till projektentiteten för att registrera anpassade stadier i ditt anpassade affärsprocessflöde.</span><span class="sxs-lookup"><span data-stu-id="138b4-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="138b4-153">Du måste lägga till affärslogik (insticksprogram eller arbetsflöden) om du vill uppdatera fältet när stadiet i det anpassade affärsprocessflödet uppdateras.</span><span class="sxs-lookup"><span data-stu-id="138b4-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Skärmbild på anpassning av entitet för projekt](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="138b4-155">Ändra diagrammet **Projekt efter stadium** om du vill använda ditt nya anpassade fält för stadier.</span><span class="sxs-lookup"><span data-stu-id="138b4-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Skärmbild på användning av diagrammet Projekt efter stadium](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="138b4-157">Ändra alla vyer för projektentiteten för att ta med dina nya anpassade fält för stadier.</span><span class="sxs-lookup"><span data-stu-id="138b4-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Skärmbild på ändring av vyer i entiteten för projekt](media/FAQ-Customize-BPF-8-720.png)

