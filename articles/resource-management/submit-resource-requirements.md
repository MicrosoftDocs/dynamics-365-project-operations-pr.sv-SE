---
title: Skicka en resursbegäran
description: Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128845"
---
# <a name="submit-a-resource-request"></a>Skicka en resursbegäran

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.

1. I Dynamics 365 Project Operations, på sidan **Projekt**, väljer du fliken **Team** för att visa en lista över bokningsbara resurser. 
2. Välj den generiska resurs som har ett resurskrav i listan och klicka på **Skicka förfrågan**.

Status för begäran för den allmänna teammedlemmen ändras till **skickad**.

När förfrågan har uppfyllts ersätts den generiska resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs. om resursansvarig föreslår en namngiven resurs kvarstår annars den generiska resursen i teamet och status för förfrågan ändras till **Måste granskas**.
