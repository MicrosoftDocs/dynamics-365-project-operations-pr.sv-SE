---
title: Konfigurera projektkategorier
description: I det här ämnet finns information om inställningar för projektkategorier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287530"
---
# <a name="configure-project-categories"></a><span data-ttu-id="1a9aa-103">Konfigurera projektkategorier</span><span class="sxs-lookup"><span data-stu-id="1a9aa-103">Configure project categories</span></span>

<span data-ttu-id="1a9aa-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="1a9aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a9aa-105">Med Project Operations får du robusta funktioner för att kategorisera intäkter och utgifter i projekt.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="1a9aa-106">Med kategorier kan du rapportera och analysera projekttransaktioner samt driva bokföring till huvudboken.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="1a9aa-107">I följande diagram illustreras korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="1a9aa-108">Transaktionskategorier är den grundläggande grupperingen för projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="1a9aa-109">Inom gruppen finns det en uppsättning delade kategorier som kan delas mellan program och moduler.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="1a9aa-110">Projektkategorierna är de mest detaljerade kategorierna för att få ännu mer specifika steg.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="1a9aa-111">Projektkategorier är specifika för juridisk person, modul och program.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="1a9aa-113">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="1a9aa-113">Transaction categories</span></span>

<span data-ttu-id="1a9aa-114">Transaktionskategorier representerar den grundläggande grupperingen av projekttransaktioner och är inte företags- eller transaktionsspecifika.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="1a9aa-115">Contoso Robotics använder t.ex. transaktionskategorierna Design, Resor, Installation och Tjänst för att gruppera projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="1a9aa-116">Transaktionskategorier definieras i modulen Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="1a9aa-117">Gå till **Inställningar** \> **Transaktionskategorier** för att öppna formuläret.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="1a9aa-118">Skapa en ny transaktionskategori genom att välja **Ny** eller genom att välja **Importera från Excel**.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="1a9aa-119">Delade kategorier</span><span class="sxs-lookup"><span data-stu-id="1a9aa-119">Shared categories</span></span>

<span data-ttu-id="1a9aa-120">Dynamics 365 använder konceptet Delade kategorier för att kategorisera utgifter i olika program, till exempel Dynamics 365 Finance, Dynamics 365 Supply Chain och Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="1a9aa-121">För varje transaktionskategori som skapas, skapar Project Operations fyra relaterade delade kategorier automatiskt: Timmar, Utgift, Avgifter och Artikel.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="1a9aa-122">Du kan granska och justera de delade kategorierna genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Delade kategorier**.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="1a9aa-123">Produktkategorier</span><span class="sxs-lookup"><span data-stu-id="1a9aa-123">Project categories</span></span>

<span data-ttu-id="1a9aa-124">Projektkategorierna representerar den mest detaljerade nivån av kategorikonfiguration och måste konfigureras separat och för varje företag av en projektrevisor.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="1a9aa-125">Gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Projektkategorier**.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="1a9aa-126">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-126">Select **New**.</span></span>
3. <span data-ttu-id="1a9aa-127">Välj **Kategori-ID** för den delade kategori du skapade i föregående avsnitt.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="1a9aa-128">Med Project Operations kan du endast använda de delade kategorierna som är associerade med transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="1a9aa-129">Välj en kategorigrupp.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="1a9aa-130">Kategorigrupper</span><span class="sxs-lookup"><span data-stu-id="1a9aa-130">Category groups</span></span>

<span data-ttu-id="1a9aa-131">Kategorigrupper används för att dela egenskaper, främst bokföringsprofiler, mellan relaterade projektkategorier.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="1a9aa-132">Det måste finnas minst en kategorigrupp för varje transaktionstyp och varje projektkategori tilldelas en grupp.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="1a9aa-133">Bokföringsspecifikationen i Project Operations definieras av reglerna för projektkostnads- och intäktsprofiler, projektkategorierna och kategorigrupperna.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="1a9aa-134">Du kan ställa in kategorigrupper genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Kategorigrupper**.</span><span class="sxs-lookup"><span data-stu-id="1a9aa-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]