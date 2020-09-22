---
title: Konfigurera Project Service Automation
description: Steg för att konfigurera Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756199"
---
# <a name="configure-project-service"></a><span data-ttu-id="72e56-103">Konfigurera Project Service</span><span class="sxs-lookup"><span data-stu-id="72e56-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="72e56-104">Innan du kan använda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-automatiseringsfunktionerna i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] för att hantera dina konton, projekt och resurser, så måste du slutföra några konfigurationssteg i syfte att säkerställa att [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-lösningen matchar din organisations behov.</span><span class="sxs-lookup"><span data-stu-id="72e56-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="72e56-105">Stegen är följande:</span><span class="sxs-lookup"><span data-stu-id="72e56-105">These steps include:</span></span>  
  
-   <span data-ttu-id="72e56-106">[Ange tidsenheter](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="72e56-107">Konfigurera tidsenheterna i produktkatalogen som ska använda som bas för tidsplanering och fakturering av dina projekt.</span><span class="sxs-lookup"><span data-stu-id="72e56-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="72e56-108">[Ställa in valutor och växelkurser](../project-service/set-up-currencies-exchange-rates.md)</span><span class="sxs-lookup"><span data-stu-id="72e56-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="72e56-109">Ställ in valutorna som ska användas för dina projekt.</span><span class="sxs-lookup"><span data-stu-id="72e56-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="72e56-110">[Skapa organisationsenheter](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="72e56-111">Ställ in de grupper som företaget använder för att dela upp sin verksamhet, efter geografi, affärsfunktioner eller andra logiska indelningar.</span><span class="sxs-lookup"><span data-stu-id="72e56-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="72e56-112">[Ange faktureringsfrekvenser](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="72e56-113">Ställ in de tidsperioder som du vill använda för fakturering av dina kunder.</span><span class="sxs-lookup"><span data-stu-id="72e56-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="72e56-114">[Konfigurera transaktionskategorier](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="72e56-115">Ställ in transaktionskategorier som dina konsulter kan debitera sina fakturerbara och ej fakturerbara utgifter till.</span><span class="sxs-lookup"><span data-stu-id="72e56-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="72e56-116">[Konfigurera utgiftskategorier](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="72e56-117">Ställ in de kategorier som dina konsulter kan debitera sina fakturerbara och ej fakturerbara utgifter till.</span><span class="sxs-lookup"><span data-stu-id="72e56-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="72e56-118">[Skapa produktkatalogobjekt](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="72e56-119">Lägg till produkter som du säljer, till exempel programvarulicenser, i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="72e56-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="72e56-120">[Skapa en prislista](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="72e56-121">Konfigurera olika prislistor, beroende på hur mycket du vill debitera dina kunder för varje roll som projektet kräver.</span><span class="sxs-lookup"><span data-stu-id="72e56-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="72e56-122">[Konfigurera resurser](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="72e56-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="72e56-123">Lägg till de färdigheter, kompetenser, resursroller och annan resursinformation som du behöver för dina projekt.</span><span class="sxs-lookup"><span data-stu-id="72e56-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="72e56-124">Se även</span><span class="sxs-lookup"><span data-stu-id="72e56-124">See Also</span></span>  
 <span data-ttu-id="72e56-125">[Översikt över Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="72e56-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="72e56-126">[Konfigurera Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="72e56-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="72e56-127">[Guide för kontohanteraren](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="72e56-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="72e56-128">[Guiden för projektledare](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="72e56-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="72e56-129">[Guide för resurshanteraren](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="72e56-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="72e56-130">Guide för tid, utgifter och samarbete</span><span class="sxs-lookup"><span data-stu-id="72e56-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
