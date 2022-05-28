---
title: Återställa ekonomiska mått för projekttidsposter
description: I det här ämnet finns information om hur återställning av ekonomiska mått tillämpas på tidsposter.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597958"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Återställa ekonomiska mått för projekttidsposter

[!include [banner](../includes/banner.md)]

När du använder ekonomiska mått för projekttidsposter ska du tänka på att standardvärdet bedöms i följande ordning:

1. Resurs
2. Project
3. Finansieringskälla

Om exempelvis standardmåttet anges för en resurs tillämpas standardvärdet före det standardvärde som anges för projektet. Om standardmåttet på samma sätt anges för ett projekt tillämpas standardvärdet före det standardvärde som anges för finansieringskällan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
