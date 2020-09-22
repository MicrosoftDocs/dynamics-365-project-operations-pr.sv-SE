---
title: Modeller för färdigheter och kompetens
description: I den här ämne finns information om hur du använder kunskaps- och färdighetsmodeller.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756292"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="f2312-103">Modeller för färdigheter och kompetens</span><span class="sxs-lookup"><span data-stu-id="f2312-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f2312-104">Kompetenser är resursegenskaper som delas mellan Dynamics 365 Project Service Automation och i förekommande fall Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="f2312-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="f2312-105">Om du vill behålla kunskapsdatabasen i Project Service Automation, gå till **resurser** \> **resurskvalifikationer**.</span><span class="sxs-lookup"><span data-stu-id="f2312-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Resursfärdigheter](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f2312-107">Använd kompetensmodeller för att gradera resurser</span><span class="sxs-lookup"><span data-stu-id="f2312-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f2312-108">Kunskaper för resurser klassificeras efter kompetensmodeller.</span><span class="sxs-lookup"><span data-stu-id="f2312-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f2312-109">De enskilda klassificeringarna är en kompetensmodell.</span><span class="sxs-lookup"><span data-stu-id="f2312-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f2312-110">Om du vill skapa en kompetensmodell, gå till **resurser** \> **kompetensmodeller** och välj sedan **ny**.</span><span class="sxs-lookup"><span data-stu-id="f2312-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="f2312-111">I den nya klassificeringsmodellen anger du minsta klassificeringsvärdet, det maximala klassificeringsvärdet och den entitet som värderas.</span><span class="sxs-lookup"><span data-stu-id="f2312-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f2312-112">I rutnätet **klassificeringsvärden** kan du definiera de olika klassificeringsvärdena, från minimum till maximum.</span><span class="sxs-lookup"><span data-stu-id="f2312-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimi- och maximivärden som definierats](media/Resource-Management-image85.png)

<span data-ttu-id="f2312-114">De här klassificeringsvärdena visas på filtren **resurskrav**, **schematavla** och **schemaassistent**.</span><span class="sxs-lookup"><span data-stu-id="f2312-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
