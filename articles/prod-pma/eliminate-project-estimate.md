---
title: Eliminera en projektuppskattning
description: I det här ämnet finns information om hur du eliminerar en projektuppskattning efter att den har slutförts.
author: Yowelle
ms.date: 05/26/2020
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
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006938"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="98a53-103">Eliminera en projektuppskattning</span><span class="sxs-lookup"><span data-stu-id="98a53-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98a53-104">Projektuppskattningar ger den ekonomiska vyn för arbete som har uppskattats och schemalagts för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="98a53-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="98a53-105">Om du vill arbeta med uppskattningar för ett projekt måste du koppla projektet till ett uppskattningsprojekt.</span><span class="sxs-lookup"><span data-stu-id="98a53-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="98a53-106">Ett uppskattningsprojekt bygger alltid på ett befintligt projekt, men flera projekt kan emellertid referera till ett enda uppskattningsprojekt.</span><span class="sxs-lookup"><span data-stu-id="98a53-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="98a53-107">Det går endast att koppla projekt med fast pris och investering till uppskattningsprojekt och projekten måste tillhöra samma projektgrupp som uppskattningsprojektet.</span><span class="sxs-lookup"><span data-stu-id="98a53-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="98a53-108">Om du vill eliminera ett uppskattningsprojekt måste det vara klart.</span><span class="sxs-lookup"><span data-stu-id="98a53-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="98a53-109">I följande steg förklaras hur du eliminerar en uppskattning.</span><span class="sxs-lookup"><span data-stu-id="98a53-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="98a53-110">Gå till **Projektledning och redovisning** > **Alla projekt** och öppna projektet.</span><span class="sxs-lookup"><span data-stu-id="98a53-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="98a53-111">Under fliken **Hantera** väljer du **Uppskattningar** och på sidan **Uppskatta** väljer du **Eliminera**.</span><span class="sxs-lookup"><span data-stu-id="98a53-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="98a53-112">På sidan **Eliminera uppskattning** under fliken **Allmänt** anger du följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="98a53-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="98a53-113">**Periodkod**: Välj periodkoden för att välja lämpliga uppskattningsprojekt.</span><span class="sxs-lookup"><span data-stu-id="98a53-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="98a53-114">**Uppskattningsdatum**: Välj lämpligt uppskattningsdatum för eliminering.</span><span class="sxs-lookup"><span data-stu-id="98a53-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="98a53-115">**Eliminera med PIA-varningar**: Aktivera det här alternativet om du vill att aviseringar ska visas när en uppskattning som är kopplad till ett pågående arbete (PIA) ska elimineras.</span><span class="sxs-lookup"><span data-stu-id="98a53-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="98a53-116">Om det här alternativet inte är aktiverat kan eliminering inte fortsätta om det finns icke uppskattade transaktioner.</span><span class="sxs-lookup"><span data-stu-id="98a53-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="98a53-117">Det här alternativet är endast tillgängligt när eliminering tillämpas på ett uppskattningsprojekt.</span><span class="sxs-lookup"><span data-stu-id="98a53-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="98a53-118">Det är inte tillgängligt om du använder periodiska bokningar.</span><span class="sxs-lookup"><span data-stu-id="98a53-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="98a53-119">Den här inställningen fungerar med inställningarna under fliken **Uppskattning** på sidan **Projektparametrar** i fältgruppen **Tillåt eliminering när transaktioner som inte uppskattas finns**.</span><span class="sxs-lookup"><span data-stu-id="98a53-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="98a53-120">**Ange att stadiet har slutförts**: Aktivera det här alternativet om du vill att uppskattningsprojektets stadium ska vara anges som **Slutfört** efter att elimineringen har körts.</span><span class="sxs-lookup"><span data-stu-id="98a53-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="98a53-121">**Skriv ut uppskattningslista**: Välj vilken information som ska inkluderas när uppskattningslistan skrivs ut.</span><span class="sxs-lookup"><span data-stu-id="98a53-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="98a53-122">**Visa informationslogg**: Aktivera det här alternativet om du vill visa informationsloggen.</span><span class="sxs-lookup"><span data-stu-id="98a53-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="98a53-123">**Bokföringsdatum**: Välj datumet då uppskattningen bokförs i transaktionsregistret.</span><span class="sxs-lookup"><span data-stu-id="98a53-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="98a53-124">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="98a53-124">Select **OK**.</span></span>
5. <span data-ttu-id="98a53-125">När elimineringsprocessen har slutförts visas det eliminerade uppskattningsprojektet med ett negativt värde.</span><span class="sxs-lookup"><span data-stu-id="98a53-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="98a53-126">Om du inte har för avsikt att eliminera en uppskattning kan du markera den eliminerade uppskattningen och välja **Återför eliminering**.</span><span class="sxs-lookup"><span data-stu-id="98a53-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]