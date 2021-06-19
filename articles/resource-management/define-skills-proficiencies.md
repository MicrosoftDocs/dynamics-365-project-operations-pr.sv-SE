---
title: Definiera kunskaper och färdigheter
description: I det här ämnet finns information om hur du konfigurerar kompetensmodeller för att gradera resurser.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015353"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="324dc-103">Definiera kunskaper och färdigheter</span><span class="sxs-lookup"><span data-stu-id="324dc-103">Define skills and proficiencies</span></span>

<span data-ttu-id="324dc-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="324dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="324dc-105">Kompetenser är resursegenskaper som delas mellan Dynamics 365 Project Operations och i förekommande fall Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="324dc-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="324dc-106">Om du vill behålla kunskapsdatabasen i Project Operations, gå till **resurser** \> **resurskvalifikationer**.</span><span class="sxs-lookup"><span data-stu-id="324dc-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="324dc-107">Använd kompetensmodeller för att gradera resurser</span><span class="sxs-lookup"><span data-stu-id="324dc-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="324dc-108">Kunskaper för resurser klassificeras efter kompetensmodeller.</span><span class="sxs-lookup"><span data-stu-id="324dc-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="324dc-109">De enskilda klassificeringarna är en kompetensmodell.</span><span class="sxs-lookup"><span data-stu-id="324dc-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="324dc-110">Om du vill skapa en kompetensmodell, gå till **resurser** \> **kompetensmodeller** och välj sedan **ny**.</span><span class="sxs-lookup"><span data-stu-id="324dc-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="324dc-111">I den nya klassificeringsmodellen anger du minsta klassificeringsvärdet, det maximala klassificeringsvärdet och den entitet som värderas.</span><span class="sxs-lookup"><span data-stu-id="324dc-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="324dc-112">I underrutnätet **klassificeringsvärden** kan du definiera de olika klassificeringsvärdena, från minimum till maximum.</span><span class="sxs-lookup"><span data-stu-id="324dc-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="324dc-113">De här klassificeringsvärdena visas på filtren **resurskrav**, **schematavla** och **schemaassistent**.</span><span class="sxs-lookup"><span data-stu-id="324dc-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]