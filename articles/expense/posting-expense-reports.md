---
title: Bokföra utgiftsrapporter
description: I det här ämnet beskrivs hur du bokför utgiftsrapporter.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907430"
---
# <a name="post-expense-reports"></a>Bokföra utgiftsrapporter

När en utgiftsrapport har godkänts och överförts till den allmänna journalen kan den bokföras. När du bokför en utgiftsrapport identifieras utgifter som är berättigade att få tillbaka moms. Uppgiften att kontrollera och få tillbaka moms tilldelas den medarbetare som ansvarar för att kontrollera utgiftsrapporten.

Om utgifter i en utgiftsrapport debiteras ett företag som inte är samma företag där medarbetar arbetar, måste du kontrollera både företaget som dessa utgifter är skyldiga till och företaget de är skyldiga från. Den anställde som har skickat en utgiftsrapport fungerar till exempel för DAT-företaget men debiterar en utgift i DIR-företaget. I det här fallet är DAT det företag som utgiften är skyldig till och DIR är det företag som utgiften är skyldig från. När du har kontrollerat dessa journalrader kan du bokföra utgiftsraderna i huvudboken.

Om du vill bokföra en utgiftsrapport på sidan **Godkända utgiftsrapporter** väljer du utgiftsrapport och sedan, i åtgärdsfönstret, väljer du **Bokför**.

Du kan också bokföra alla utgiftsrapporter i listan på samma gång. Välj alla utgiftsrapporter och välj sedan **Bokför**.
