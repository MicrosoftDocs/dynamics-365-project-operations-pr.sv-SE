---
title: Distribuera appen Project Operations Dataverse manuellt med stöd för dubbelriktad skrivning
description: I ämne beskrivs hur du manuellt distribuerar appen Project Operations Dataverse så att den har stöd för dubbelriktad skrivning.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274030"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="6bae5-103">Distribuera appen Project Operations Dataverse manuellt med stöd för dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="6bae5-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="6bae5-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="6bae5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6bae5-105">I ämne beskrivs hur du manuellt distribuerar appen Microsoft Dynamics 365 Project Operations i Microsoft Dataverse så att den har stöd för dubbelriktad skrivning.</span><span class="sxs-lookup"><span data-stu-id="6bae5-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="6bae5-106">Project Operations identifierar miljöns konfiguration och lägger till ytterligare stöd för dubbelriktad skrivning om kraven uppfylls.</span><span class="sxs-lookup"><span data-stu-id="6bae5-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="6bae5-107">Under distributionen via Microsoft Dynamics Lifecycle Services (LCS), om du har följt instruktionerna i det här ämnet kan du hoppa över distributionen av Microsoft Power Platform-integrering (kallades tidigare Common Data Service-miljö).</span><span class="sxs-lookup"><span data-stu-id="6bae5-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="6bae5-108">Processen av att distribuera Project Operations i Dataverse så att den stöder dubbelriktad skrivning har fyra huvudsteg:</span><span class="sxs-lookup"><span data-stu-id="6bae5-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="6bae5-109">[Skapa en ny miljö i Dataverse som ger stöd för dubbelriktad skrivning](#create).</span><span class="sxs-lookup"><span data-stu-id="6bae5-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="6bae5-110">[Lägg till krav för dubbelriktad skrivning i miljön](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="6bae5-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="6bae5-111">[Lägg till Project Operations Dataverse-app](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="6bae5-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="6bae5-112">[Länka dina miljöer](#link).</span><span class="sxs-lookup"><span data-stu-id="6bae5-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="6bae5-113">Skapa en ny miljö i Dataverse som ger stöd för dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="6bae5-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="6bae5-114">Du måste logga in som en administratör.</span><span class="sxs-lookup"><span data-stu-id="6bae5-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="6bae5-115">Öppna [Power Platform administrationscenter](https://admin.powerplatform.com) och logga in som en administratör.</span><span class="sxs-lookup"><span data-stu-id="6bae5-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="6bae5-116">Skapa en ny miljö och namnge den.</span><span class="sxs-lookup"><span data-stu-id="6bae5-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="6bae5-117">Välj miljötypen.</span><span class="sxs-lookup"><span data-stu-id="6bae5-117">Select the environment type.</span></span> <span data-ttu-id="6bae5-118">Välj om du har registrerat dig för erbjudande om utvärderingsversion **utvärderingsversion (prenumerationsbaserad)**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="6bae5-119">Bekräfta distributionsområdet.</span><span class="sxs-lookup"><span data-stu-id="6bae5-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="6bae5-120">Aktivera alternativet **Skapa en databas för miljön**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="6bae5-121">Bekräfta språket och kontrollera sedan att valutan matchar valutan för Finance and Operations-apparna.</span><span class="sxs-lookup"><span data-stu-id="6bae5-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="6bae5-122">Aktivera alternativet **Dynamics 365-appar** och bekräfta att fältet **Automatiskt distribuera dessa appar** har angetts till **Inget**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="6bae5-123">Lägg till en säkerhetsgrupp om en säkerhetsgrupp krävs.</span><span class="sxs-lookup"><span data-stu-id="6bae5-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="6bae5-124">Välj **Spara** för att skapa miljön.</span><span class="sxs-lookup"><span data-stu-id="6bae5-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="6bae5-125">Vänta tills distributionen har slutförts och miljön har nått tillståndet **Klar**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="6bae5-126">Lägg till krav för dubbelriktad skrivning i miljön.</span><span class="sxs-lookup"><span data-stu-id="6bae5-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="6bae5-127">Stöd för dubbelriktad skrivning omfattar ytterligare fält som läggs till i nyckelentiteter, till exempel entiteten **Företag**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="6bae5-128">Om du lägger till stöd för dubbelriktad skrivning i en befintlig miljö kan du behöva uppdatera informationen för att aktivera supporten.</span><span class="sxs-lookup"><span data-stu-id="6bae5-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="6bae5-129">Information om hur du startar data finns i [Bootstrap företagsdata](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="6bae5-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="6bae5-130">Mer information om dubbelriktad skrivning finns i [Systemkrav för dubbelriktad skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="6bae5-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="6bae5-131">Slutför proceduren om du vill lägga till krav med dubbelriktad skrivningar i miljön.</span><span class="sxs-lookup"><span data-stu-id="6bae5-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="6bae5-132">Öppna den miljö du just skapat och gå sedan till **Resurs** \> **Dynamics 365-appar**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="6bae5-133">Välj **lösning för dubbelriktad skrivning** i applistan och installera den.</span><span class="sxs-lookup"><span data-stu-id="6bae5-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="6bae5-134">Vänta tills installationen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="6bae5-134">Wait until the installation is completed.</span></span> <span data-ttu-id="6bae5-135">Välj sedan **Orkestreringslösning för dubbelriktad skrivning** i applistan och installera den.</span><span class="sxs-lookup"><span data-stu-id="6bae5-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="6bae5-136">Lägg till Project Operations Dataverse-app</span><span class="sxs-lookup"><span data-stu-id="6bae5-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="6bae5-137">Du kan endast utföra den här proceduren om du har slutfört de föregående procedurerna innan du installerade Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6bae5-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="6bae5-138">Under installationen analyseras miljökonfigurationen och stöd för dubbelriktning skrivning läggs till om det behövs.</span><span class="sxs-lookup"><span data-stu-id="6bae5-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="6bae5-139">Öppna den miljö du just skapat och gå sedan till **Resurs** \> **Dynamics 365-appar**.</span><span class="sxs-lookup"><span data-stu-id="6bae5-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="6bae5-140">Välj **Microsoft Dynamics 365 Project Operations** i applistan och installera det.</span><span class="sxs-lookup"><span data-stu-id="6bae5-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="6bae5-141">Länka dina miljöer.</span><span class="sxs-lookup"><span data-stu-id="6bae5-141">Link your environments</span></span>

<span data-ttu-id="6bae5-142">När Dataverse-miljön har distribuerats kan du konfigurera länken i dina Finance and Operations-appar.</span><span class="sxs-lookup"><span data-stu-id="6bae5-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="6bae5-143">Följ anvisningarna i [Använd guiden för dubbelriktade skrivningar för att länka dina miljöer](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="6bae5-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
