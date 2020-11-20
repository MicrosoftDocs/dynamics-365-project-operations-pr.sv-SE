---
title: Modeller för färdigheter och kompetens
description: I den här ämne finns information om hur du använder kunskaps- och färdighetsmodeller.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124210"
---
# <a name="skills-and-proficiency-models"></a>Modeller för färdigheter och kompetens

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kompetenser är resursegenskaper som delas mellan Dynamics 365 Project Service Automation och i förekommande fall Dynamics 365 Field Service. 

Om du vill behålla kunskapsdatabasen i Project Service Automation, gå till **resurser** \> **resurskvalifikationer**. 

> ![Resursfärdigheter](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Använd kompetensmodeller för att gradera resurser

Kunskaper för resurser klassificeras efter kompetensmodeller. De enskilda klassificeringarna är en kompetensmodell. 

1. Om du vill skapa en kompetensmodell, gå till **resurser** \> **kompetensmodeller** och välj sedan **ny**.
2. I den nya klassificeringsmodellen anger du minsta klassificeringsvärdet, det maximala klassificeringsvärdet och den entitet som värderas.
3. I underrutnätet **klassificeringsvärden** kan du definiera de olika klassificeringsvärdena, från minimum till maximum.

> ![Minimi- och maximivärden som definierats](media/Resource-Management-image85.png)

De här klassificeringsvärdena visas på filtren **resurskrav**, **schematavla** och **schemaassistent**.
