---
title: Skicka en resursbegäran
description: I den här ämnet finns information om hur du skickar en förfrågan för en projektresurs.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149745"
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