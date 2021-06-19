---
title: Konfigurera Project Service Automation
description: Steg för att konfigurera Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002873"
---
# <a name="configure-project-service"></a><span data-ttu-id="0cef3-103">Konfigurera Project Service</span><span class="sxs-lookup"><span data-stu-id="0cef3-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0cef3-104">Innan du kan använda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-automatiseringsfunktionerna i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] för att hantera dina konton, projekt och resurser, så måste du slutföra några konfigurationssteg i syfte att säkerställa att [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-lösningen matchar din organisations behov.</span><span class="sxs-lookup"><span data-stu-id="0cef3-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="0cef3-105">Stegen är följande:</span><span class="sxs-lookup"><span data-stu-id="0cef3-105">These steps include:</span></span>  
  
-   <span data-ttu-id="0cef3-106">[Ange tidsenheter](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="0cef3-107">Konfigurera tidsenheterna i produktkatalogen som ska använda som bas för tidsplanering och fakturering av dina projekt.</span><span class="sxs-lookup"><span data-stu-id="0cef3-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="0cef3-108">[Ställa in valutor och växelkurser](../psa/set-up-currencies-exchange-rates.md)</span><span class="sxs-lookup"><span data-stu-id="0cef3-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="0cef3-109">Ställ in valutorna som ska användas för dina projekt.</span><span class="sxs-lookup"><span data-stu-id="0cef3-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="0cef3-110">[Skapa organisationsenheter](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="0cef3-111">Ställ in de grupper som företaget använder för att dela upp sin verksamhet, efter geografi, affärsfunktioner eller andra logiska indelningar.</span><span class="sxs-lookup"><span data-stu-id="0cef3-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="0cef3-112">[Ange faktureringsfrekvenser](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="0cef3-113">Ställ in de tidsperioder som du vill använda för fakturering av dina kunder.</span><span class="sxs-lookup"><span data-stu-id="0cef3-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="0cef3-114">[Konfigurera transaktionskategorier](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="0cef3-115">Ställ in transaktionskategorier som dina konsulter kan debitera sina fakturerbara och ej fakturerbara utgifter till.</span><span class="sxs-lookup"><span data-stu-id="0cef3-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="0cef3-116">[Konfigurera utgiftskategorier](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="0cef3-117">Ställ in de kategorier som dina konsulter kan debitera sina fakturerbara och ej fakturerbara utgifter till.</span><span class="sxs-lookup"><span data-stu-id="0cef3-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="0cef3-118">[Skapa produktkatalogobjekt](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="0cef3-119">Lägg till produkter som du säljer, till exempel programvarulicenser, i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="0cef3-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="0cef3-120">[Skapa en prislista](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="0cef3-121">Konfigurera olika prislistor, beroende på hur mycket du vill debitera dina kunder för varje roll som projektet kräver.</span><span class="sxs-lookup"><span data-stu-id="0cef3-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="0cef3-122">[Konfigurera resurser](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="0cef3-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="0cef3-123">Lägg till de färdigheter, kompetenser, resursroller och annan resursinformation som du behöver för dina projekt.</span><span class="sxs-lookup"><span data-stu-id="0cef3-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0cef3-124">Se även</span><span class="sxs-lookup"><span data-stu-id="0cef3-124">See Also</span></span>  
 <span data-ttu-id="0cef3-125">[Översikt över Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="0cef3-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="0cef3-126">[Konfigurera Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="0cef3-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="0cef3-127">[Guide för kontohanteraren](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0cef3-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="0cef3-128">[Guiden för projektledare](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0cef3-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="0cef3-129">[Guide för resurshanteraren](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="0cef3-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="0cef3-130">Guide för tid, utgifter och samarbete</span><span class="sxs-lookup"><span data-stu-id="0cef3-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]