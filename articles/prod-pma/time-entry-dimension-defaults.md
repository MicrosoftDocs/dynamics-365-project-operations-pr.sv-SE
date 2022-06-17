---
title: Återställa ekonomiska mått för projekttidsposter
description: I den här artikeln finns information om hur återställning av ekonomiska mått tillämpas på tidsposter.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916586"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Återställa ekonomiska mått för projekttidsposter

[!include [banner](../includes/banner.md)]

När du använder ekonomiska mått för projekttidsposter ska du tänka på att standardvärdet bedöms i följande ordning:

1. Resurs
2. Project
3. Finansieringskälla

Om exempelvis standardmåttet anges för en resurs tillämpas standardvärdet före det standardvärde som anges för projektet. Om standardmåttet på samma sätt anges för ett projekt tillämpas standardvärdet före det standardvärde som anges för finansieringskällan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
