---
title: Skicka en resursbegäran
description: I den här artikeln finns information om hur du skickar en förfrågan för en projektresurs.
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
ms.openlocfilehash: c446dc0f99a5b9c9cdf3698cdf774cfd1e5d4d6a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928868"
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
