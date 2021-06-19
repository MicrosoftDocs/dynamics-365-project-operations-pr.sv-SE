---
title: Modeller för färdigheter och kompetens
description: I den här ämne finns information om hur du använder kunskaps- och färdighetsmodeller.
author: ruhercul
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008693"
---
# <a name="skills-and-proficiency-models"></a>Modeller för färdigheter och kompetens

[!include [banner](../includes/psa-now-project-operations.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]