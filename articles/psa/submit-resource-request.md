---
title: Skicka en resursbegäran
description: I den här ämnet finns information om hur du skickar en förfrågan för en projektresurs.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013193"
---
# <a name="submitting-a-resource-request"></a>Skicka en resursbegäran

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.

1. I Project Service Automation (PSA), på sidan **Projekt**, klicka på fliken **Team** för att visa en lista över bokningsbara resurser. 
2. Markera den allmänna resurs som har ett resurskrav i listan och klicka på **skicka förfrågan**.

![Skicka en resursbegäran](media/RM-how-to-18.png)

Status för begäran för den allmänna teammedlemmen ändras till **skickad**.

När förfrågan har uppfyllts av resursansvarig ersätts den allmänna resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs. Annars kvarstår den allmänna resursen på teamet och status för förfrågan ändras till **måste granskas** om resursansvarig har föreslagit en namngiven resurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]