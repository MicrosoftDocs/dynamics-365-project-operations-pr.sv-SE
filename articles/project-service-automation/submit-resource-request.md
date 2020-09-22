---
title: Skicka en resursbegäran
description: I den här ämnet finns information om hur du skickar en förfrågan för en projektresurs.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756261"
---
# <a name="submit-a-resource-request"></a>Skicka en resursbegäran

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.

1. I Project Service Automation (PSA), på sidan **Projekt**, klicka på fliken **Team** för att visa en lista över bokningsbara resurser. 
2. Markera den allmänna resurs som har ett resurskrav i listan och klicka på **skicka förfrågan**.

![Skicka en resursbegäran](media/RM-how-to-18.png)

Status för begäran för den allmänna teammedlemmen ändras till **skickad**.

När förfrågan har uppfyllts av resursansvarig ersätts den allmänna resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs. Annars kvarstår den allmänna resursen på teamet och status för förfrågan ändras till **måste granskas** om resursansvarig har föreslagit en namngiven resurs.
