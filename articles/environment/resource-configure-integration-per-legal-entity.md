---
title: Konfigurera Project Operations-integrering efter juridisk person
description: I det här ämnet finns information om hur du konfigurerar integrering efter juridisk person i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277000"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="ce91f-103">Konfigurera Project Operations-integrering efter juridisk person</span><span class="sxs-lookup"><span data-stu-id="ce91f-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="ce91f-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="ce91f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ce91f-105">Det ämne genom stegen som krävs för att konfigurera Dynamics 365 Project Operations per juridisk entitet.</span><span class="sxs-lookup"><span data-stu-id="ce91f-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="ce91f-106">Aktivera funktionsnycklar i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ce91f-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="ce91f-107">Följ stegen nedan om du vill aktivera de funktioner som krävs.</span><span class="sxs-lookup"><span data-stu-id="ce91f-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="ce91f-108">I Dynamics 365 Finance går du till arbetsytan **Funktionshantering**.</span><span class="sxs-lookup"><span data-stu-id="ce91f-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="ce91f-109">I **Funktionslista** letar du upp och aktiverar följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="ce91f-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="ce91f-110">**Aktivera flera kontraktrader för ett projekt**</span><span class="sxs-lookup"><span data-stu-id="ce91f-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="ce91f-111">**Aktivera Project Operations på Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="ce91f-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="ce91f-112">Om du inte ser **Funktionsnycklar** kontrollerar du att din version av Finance uppfyller minimikraven (programversion 10.0.13 med alla kvalitetsuppdateringar eller senare).</span><span class="sxs-lookup"><span data-stu-id="ce91f-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="ce91f-113">Välj **Sök efter uppdateringar** för att uppdatera funktionslistan.</span><span class="sxs-lookup"><span data-stu-id="ce91f-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="ce91f-114">Definiera ett scenario för distribution av Project Operations för en juridisk person</span><span class="sxs-lookup"><span data-stu-id="ce91f-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="ce91f-115">Du kan aktivera Project Operations på Dynamics 365 Customer Engagement på en nivå för juridisk person.</span><span class="sxs-lookup"><span data-stu-id="ce91f-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="ce91f-116">Du kan ha en juridisk person med Project Operations i Dynamics 365 Customer Engagement för resursbaserade/icke lagerbaserade scenarier.</span><span class="sxs-lookup"><span data-stu-id="ce91f-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="ce91f-117">I samma miljö kan du ha en annan juridisk person med Project Operations för lagerbaserade/produktionsorderbaserade scenarier.</span><span class="sxs-lookup"><span data-stu-id="ce91f-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="ce91f-118">I Dynamics 365 Finance går du till **Projektledning och redovisning** > **Konfiguration** > **Global projektledning och redovisningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="ce91f-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="ce91f-119">I listan över tillgängliga juridiska personer väljer du entiteter där flera kontraktrader och Project Operations i Dynamics 365 Customer Engagement-funktioner aktiveras.</span><span class="sxs-lookup"><span data-stu-id="ce91f-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="ce91f-120">Lämna juridiska personer som ska använda Project Operations för lagerbaserade/produktionsorderbaserade scenarier omarkerade.</span><span class="sxs-lookup"><span data-stu-id="ce91f-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="ce91f-121">En juridisk person kan endast väljas om den inte har några befintliga projekt.</span><span class="sxs-lookup"><span data-stu-id="ce91f-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="ce91f-122">Konfigurera parametrar för projektledning och redovisning</span><span class="sxs-lookup"><span data-stu-id="ce91f-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="ce91f-123">Varje juridisk person som använder Project Operations i Dynamics 365 Customer Engagement behöver en uppsättning standardparametrar.</span><span class="sxs-lookup"><span data-stu-id="ce91f-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="ce91f-124">Dessa parametrar konfigureras under fliken **Project Operations** på sidan **Projektledning och redovisningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="ce91f-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="ce91f-125">Parametrarna är:</span><span class="sxs-lookup"><span data-stu-id="ce91f-125">The parameters are:</span></span>

  - <span data-ttu-id="ce91f-126">**Standard för faktureringstyp**: Project Operations använder en fast uppsättning standardfaktureringstyper som måste mappas till egenskaper i Finance.</span><span class="sxs-lookup"><span data-stu-id="ce91f-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="ce91f-127">Skapa en post för varje faktureringstyp: **Inte angiven**, **Debiterbar**, **Inte debiterbar**, **Kostnadsfri** och **Ej tillgänglig**.</span><span class="sxs-lookup"><span data-stu-id="ce91f-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="ce91f-128">**Standardprojektkategori**: Välj de projektkategorier som ska användas som standard för varje transaktionstyp.</span><span class="sxs-lookup"><span data-stu-id="ce91f-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="ce91f-129">De här standardvärdena används i **Project Operations integreringsjournal** och i uppskattningar där ingen transaktionskategori har angetts för projektets faktiska värden.</span><span class="sxs-lookup"><span data-stu-id="ce91f-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="ce91f-130">**Prognoser**: Välj vilken prognosmodell som ska användas för uppskattning av tid och utgifter.</span><span class="sxs-lookup"><span data-stu-id="ce91f-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]