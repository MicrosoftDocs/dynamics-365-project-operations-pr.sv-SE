---
title: Bokför en utgiftsrapport
description: I det här ämnet förklaras hur du bokför en utgiftsrapport i redovisningen.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085686"
---
# <a name="post-an-expense-report"></a>Bokför en utgiftsrapport

[!include [banner](../includes/banner.md)]

När en utgiftsrapport har godkänts och överförts till den allmänna journalen kan den bokföras i redovisningen. När du bokför en utgiftsrapport identifieras utgifter som är berättigade att få tillbaka moms. Uppgiften att kontrollera och få tillbaka moms tilldelas den medarbetare som ansvarar för att kontrollera utgiftsrapporten.

Om utgifter i en utgiftsrapport debiteras ett företag som inte är samma företag där medarbetaren arbetar, måste du kontrollera företaget som dessa utgifter är skyldiga till och företaget som utgifterna är skyldiga från. Den anställde som har skickat en utgiftsrapport fungerar till exempel för DAT-företaget men debiterar en utgift i DIR-företaget. I det här fallet är DAT det företag som utgiften är skyldig till och DIR är det företag som utgiften är skyldig från. När du har kontrollerat dessa journalrader kan du bokföra utgiftsraderna i huvudboken.

Om du vill bokföra en utgiftsrapport på sidan **Godkända utgiftsrapporter** väljer du utgiftsrapport och sedan, i åtgärdsfönstret, väljer du **Bokför**.

Du kan också bokföra alla utgiftsrapporter i listan på samma gång. Välj alla utgiftsrapporter och välj sedan **Bokför**.
