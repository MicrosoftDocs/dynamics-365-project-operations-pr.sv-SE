---
title: Skicka en resursbegäran
description: Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961752"
---
# <a name="submit-a-resource-request"></a>Skicka en resursbegäran

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.

1. I Dynamics 365 Project Operations, på sidan **Projekt**, väljer du fliken **Team** för att visa en lista över bokningsbara resurser. 
2. Välj den generiska resurs som har ett resurskrav i listan och klicka på **Skicka förfrågan**.

Status för begäran för den allmänna teammedlemmen ändras till **skickad**.

När förfrågan har uppfyllts ersätts den generiska resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs. om resursansvarig föreslår en namngiven resurs kvarstår annars den generiska resursen i teamet och status för förfrågan ändras till **Måste granskas**.
