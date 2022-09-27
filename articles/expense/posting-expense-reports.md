---
title: Bokföra utgiftsrapporter
description: I den här artikeln finns information om hur du publicerar utgiftsrapporter.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524892"
---
# <a name="post-expense-reports"></a>Bokföra utgiftsrapporter

När en utgiftsrapport har godkänts och överförts till den allmänna journalen kan den bokföras. När du bokför en utgiftsrapport identifieras utgifter som är berättigade att få tillbaka moms. Uppgiften att kontrollera och få tillbaka moms tilldelas den medarbetare som ansvarar för att kontrollera utgiftsrapporten.

Om utgifter i en utgiftsrapport debiteras ett företag som inte är samma företag där medarbetar arbetar, måste du kontrollera både företaget som dessa utgifter är skyldiga till och företaget de är skyldiga från. Den anställde som har skickat en utgiftsrapport fungerar till exempel för DAT-företaget men debiterar en utgift i DIR-företaget. I det här fallet är DAT det företag som utgiften är skyldig till och DIR är det företag som utgiften är skyldig från. När du har kontrollerat dessa journalrader kan du bokföra utgiftsraderna i huvudboken.

Om du vill bokföra en utgiftsrapport på sidan **Godkända utgiftsrapporter** väljer du utgiftsrapport och sedan, i åtgärdsfönstret, väljer du **Bokför**.

Du kan också bokföra alla utgiftsrapporter i listan på samma gång. Välj alla utgiftsrapporter och välj sedan **Bokför**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Aktivera möjligheten att efterkostnadsansvar i leverantörsvaluta för funktionen för kontantbetalningsmetod

Funktionen **möjligheten att efterkostnadsansvar i leverantörsvaluta för kontantbetalningsmetod** gör att utgiftsrapporter kan läggas upp i en valuta för leverantörsvalutan för kassametoden.

När du för närvarande skickar in kassakostnader, läggs utgiftsrapporter upp i redovisningsvalutan. På grund av beloppskonvertering mellan transaktionsvalutan, redovisningsvalutan och leverantörsvalutan betalas ett felaktigt belopp till leverantörer om transaktionsdatumet för kostnaden och det faktiska betalningsdatumet har olika växelkurser.

Med den här funktionen ser du till att leverantörssaldot registreras i leverantörsvalutan när utgiftsrapporten publiceras.

1. Gå till **Arbetsytor** \> **Funktionshantering**.
2. I listan sök efter och välj **möjligheten att efterkostnadsansvar i leverantörsvaluta för kontantbetalningsmetod** och sedan **Aktivera nu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
