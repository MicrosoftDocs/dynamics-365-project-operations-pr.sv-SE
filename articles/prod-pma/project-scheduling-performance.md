---
title: Resultat av projektresursschemaläggning
description: I det här ämnet finns information om hur du kan förbättra prestanda för resursschemaläggning för ett stort antal projekt.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010043"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="2c0e0-103">Resultat av projektresursschemaläggning</span><span class="sxs-lookup"><span data-stu-id="2c0e0-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="2c0e0-104">Prestandaproblem som hänger samman med resursschemaläggning kan inträffa när antalet projekt når tusentals.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="2c0e0-105">För att förbättra resursschemaläggningens prestanda finns en funktion som gör att användare kan öppna formulär för resurstillgänglighet snabbare.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="2c0e0-106">Detta tar bort synkroniseringsprocessen för sammanslagning av resurskapacitet och använder tabellen **ResProjectResource** för att påskynda resursuppslaget.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="2c0e0-107">Observera att tabellen **ResRollup** inte längre används.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c0e0-108">Om det finns ett beroende antingen på den pågående synkroniseringen för sammanslagning av resurskapacitet eller i tabellen **ResProjectResource** ska du inte använda den här funktionen.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2c0e0-109">Aktivera förbättrad prestanda hos resursschemaläggning</span><span class="sxs-lookup"><span data-stu-id="2c0e0-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="2c0e0-110">Följ stegen nedan om du vill aktivera prestandaförbättringar för resursschemaläggning.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="2c0e0-111">Gå till **Funktionshantering** > **Alla** och i listan med funktioner letar du upp **Aktivera förbättrad prestanda hos schemaläggning av projektresurser**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2c0e0-112">Välj **Aktivera nu**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="2c0e0-113">Om du inte hittar funktionen i listan kan du välja **Sök efter uppdateringar** för att uppdatera listan.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="2c0e0-114">Uppdatera webbläsaren och gå sedan till **Projekthantering och redovisning** > **Periodiskt** > **Projektresurser** > **Synkronisera resurskalenderns kapacitet för alla företag**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="2c0e0-115">Ställ in **Ta bort befintliga kapacitetsposter** på **Ja** om du vill ta bort tidigare data.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2c0e0-116">Om du vill generera stegvisa data anger du det till **Nej**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="2c0e0-117">I fältet **Periodkod** väljer du den period då data ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2c0e0-118">Om du väljer en periodkod behöver du inte ange start- och slutdatum.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="2c0e0-119">Om du lämnar fältet **Periodkod** tomt ska du välja specifika start- och slutdatum för att generera data.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="2c0e0-120">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2c0e0-121">Detta innebär att allmänna data distribueras till tabellen **ResCalendarCapacity** i alla företag i din miljö, så att batch-jobbet endast behöver köras i en juridisk person.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2c0e0-122">Data i det här batch-jobbet behövs för att beräkna resurskapacitet via den associerade kalendern.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="2c0e0-123">Gå till **Projektledning och redovisning** > **Periodiskt** > **Projektresurser** > **Fylla i projektresurser över alla företag** och välj sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="2c0e0-124">Detta är datauppgraderingsskriptet för allmänna data i tabellerna **ResProjectResource**, **ResCalendarDateTimeRange** och **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="2c0e0-125">Värden för fältet **PSAPRojSchedRole.RootActivity** uppdateras också.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="2c0e0-126">Om det inte körs får du en varning när du försöker köra resursplaneringsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2c0e0-127">Inaktivera förbättrad prestanda hos resursschemaläggning</span><span class="sxs-lookup"><span data-stu-id="2c0e0-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="2c0e0-128">Gå till **Funktionshantering** > **Alla** och sök efter **Aktivera förbättrad prestanda hos schemaläggning av projektresurser**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2c0e0-129">Markera funktionen och välj sedan knappen **Inaktivera**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="2c0e0-130">Uppdatera webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-130">Refresh your browser.</span></span>
4. <span data-ttu-id="2c0e0-131">Gå till **Projektledning och redovisning** > **Periodiskt** > **Kapacitetssynkronisering** > **Synkronisera sammanslagning av resurskapacitet**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="2c0e0-132">På sidan **Synkronisering av sammanslagning av kapacitet** ställer du in **Ta bort befintliga kapacitetsposter** på **Ja** för att ta bort tidigare data.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2c0e0-133">Om du vill generera stegvisa data anger du det till **Nej**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="2c0e0-134">I fältet **Periodkod** väljer du den period då data ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2c0e0-135">Om du väljer en periodkod behöver du inte ange start- och slutdatum.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="2c0e0-136">Om du lämnar fältet **Periodkod** tomt ska du välja specifika start- och slutdatum för att generera data.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="2c0e0-137">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="2c0e0-138">Detta innebär att allmänna data distribueras till tabellen **ResRollup** i alla företag i din miljö, så att batch-jobbet endast behöver köras i en juridisk person.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2c0e0-139">Det här batch-jobbet krävs för alla vyer i **Resurstillgänglighet**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="2c0e0-140">Om det här batch-jobbet inte körs kommer **ResRollup**-data att skapas i farten, vilket kan ta tid.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]