---
title: Konfigurera projektkategorier
description: I det här ämnet finns information om inställningar för projektkategorier.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995193"
---
# <a name="configure-project-categories"></a><span data-ttu-id="5a4ca-103">Konfigurera projektkategorier</span><span class="sxs-lookup"><span data-stu-id="5a4ca-103">Configure project categories</span></span>

<span data-ttu-id="5a4ca-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="5a4ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5a4ca-105">Med Project Operations får du robusta funktioner för att kategorisera intäkter och utgifter i projekt.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="5a4ca-106">Med kategorier kan du rapportera och analysera projekttransaktioner samt driva bokföring till huvudboken.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="5a4ca-107">I följande diagram illustreras korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="5a4ca-108">Transaktionskategorier är den grundläggande grupperingen för projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="5a4ca-109">Inom gruppen finns det en uppsättning delade kategorier som kan delas mellan program och moduler.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="5a4ca-110">Projektkategorierna är de mest detaljerade kategorierna för att få ännu mer specifika steg.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="5a4ca-111">Projektkategorier är specifika för juridisk person, modul och program.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="5a4ca-113">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="5a4ca-113">Transaction categories</span></span>

<span data-ttu-id="5a4ca-114">Transaktionskategorier representerar den grundläggande grupperingen av projekttransaktioner och är inte företags- eller transaktionsspecifika.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="5a4ca-115">Till exempel använder Contoso Robotics kategorierna Design, Resor, Installation och Service för att gruppera projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="5a4ca-116">Transaktionskategorier definieras i modulen Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="5a4ca-117">Gå till **Inställningar** \> **Transaktionskategorier** för att öppna formuläret.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="5a4ca-118">Skapa en ny transaktionskategori genom att välja **Ny** eller genom att välja **Importera från Excel**.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="5a4ca-119">Delade kategorier</span><span class="sxs-lookup"><span data-stu-id="5a4ca-119">Shared categories</span></span>

<span data-ttu-id="5a4ca-120">Dynamics 365 använder konceptet Delade kategorier för att kategorisera utgifter i olika program, till exempel Dynamics 365 Finance, Dynamics 365 Supply Chain och Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="5a4ca-121">För varje transaktionskategori som skapas, skapar Project Operations fyra relaterade delade kategorier automatiskt: Timmar, Utgift, Avgifter och Artikel.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="5a4ca-122">Du kan granska och justera de delade kategorierna genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Delade kategorier**.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="5a4ca-123">Produktkategorier</span><span class="sxs-lookup"><span data-stu-id="5a4ca-123">Project categories</span></span>

<span data-ttu-id="5a4ca-124">Projektkategorierna representerar den mest detaljerade nivån av kategorikonfiguration och måste konfigureras separat och för varje företag av en projektrevisor.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="5a4ca-125">Gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Projektkategorier**.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="5a4ca-126">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-126">Select **New**.</span></span>
3. <span data-ttu-id="5a4ca-127">Välj **Kategori-ID** för den delade kategori du skapade i föregående avsnitt.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="5a4ca-128">Med Project Operations kan du endast använda de delade kategorierna som är associerade med transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="5a4ca-129">Välj en kategorigrupp.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="5a4ca-130">Kategorigrupper</span><span class="sxs-lookup"><span data-stu-id="5a4ca-130">Category groups</span></span>

<span data-ttu-id="5a4ca-131">Kategorigrupper används för att dela egenskaper, främst bokföringsprofiler, mellan relaterade projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="5a4ca-132">Det måste finnas minst en kategorigrupp för varje transaktionstyp och varje projektkategori tilldelas en grupp.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="5a4ca-133">Bokföringsspecifikationen i Project Operations definieras av reglerna för projektkostnads- och intäktsprofiler, projektkategorierna och kategorigrupperna.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="5a4ca-134">Du kan ställa in kategorigrupper genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Kategorigrupper**.</span><span class="sxs-lookup"><span data-stu-id="5a4ca-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]