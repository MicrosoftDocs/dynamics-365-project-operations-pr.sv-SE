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
ms.reviewer: johnmichalak
ms.openlocfilehash: d22f52771f55a551416d1ba2f7105d59d7b912f0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577488"
---
# <a name="submitting-a-resource-request"></a>Skicka en resursbegäran

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.

1. I Project Service Automation (PSA), på sidan **Projekt**, klicka på fliken **Team** för att visa en lista över bokningsbara resurser. 
2. Markera den allmänna resurs som har ett resurskrav i listan och klicka på **skicka förfrågan**.

![Skicka en resursbegäran.](media/RM-how-to-18.png)

Status för begäran för den allmänna teammedlemmen ändras till **skickad**.

När förfrågan har uppfyllts av resursansvarig ersätts den allmänna resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs. Annars kvarstår den allmänna resursen på teamet och status för förfrågan ändras till **måste granskas** om resursansvarig har föreslagit en namngiven resurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
