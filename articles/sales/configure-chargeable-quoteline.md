---
title: Konfigurera debiterbara komponenter på en projektbaserad offertrad
description: Detta ämne innehåller information om inkluderade, debiterbara och icke-debiterbara komponenter på projektbaserade offertrader.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9febf305e3cd29bab42cd6c83a941f7b494fa56
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013598"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurera debiterbara komponenter på en projektbaserad offertrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En projektbaserad offertrad kan ha inkluderade komponenter och debiterbara komponenter.

Inkluderade komponenter omfattas av faktureringsmetod, kunddelningar, gränser som inte får överskridas samt inställningar för fakturafrekvens som definierats på den projektbaserade offertraden.
En delmängd av inkluderade komponenter kan markeras som debiterbar med hjälp av **Faktureringstyp**. Du kan välja ett av följande alternativ i fältet **Faktureringstyp** i kontexten för en offertrad:

   - Debiterbart
   - Ej debiterbar

Debiterbara komponenter kan definieras för roller och transaktionskategorier.

Debiteringsbarhet som definieras i roller för en projektoffertrad gäller bara för transaktionsklassen **Tid**. Om en projektoffertrad har **Inkludera tid** = **Nej** är fliken **Debitera roller** inte tillgänglig.

Debiteringsbarhet som definieras i transaktionskategorier för en projektoffertrad gäller bara för transaktionsklassen **Utgift**. Om en projektoffertrad har **Inkludera utgifter** = **Nej** är fliken **Debitera kategorier** inte tillgänglig.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Uppdatera en roll så att den är debiterbar eller ej debiterbar
En roll kan vara debiterbar eller icke-debiterbar på en projektbaserad offertrad. Faktureringstypen för en roll kan konfigureras på fliken **Debiterbara roller** för en projektbaserad offertrad. Det gör du genom att uppdatera fältet **Faktureringstyp** i underrutnätet **Debiterbara roller**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar
En transaktionskategori kan vara debiterbar eller icke-debiterbar på en projektbaserad offertrad. Faktureringstypen för en transaktion kan konfigureras på fliken **Debiterbara kategorier** för en projektbaserad offertrad. Det gör du genom att uppdatera fältet **faktureringstyp** i under rutnätet **debiterbara kategorier**. 

## <a name="resolve-chargeability"></a>Åtgärda debiteringsbarhet

En uppskattning eller ett faktiskt värde som skapas för tid kommer endast att anses debiterbar om tiden inkluderas på offertraden och om rollen är konfigurerad som debiteringsbar.
En uppskattning eller ett faktiskt värde som skapas för en utgift kommer endast att anses debiterbar om utgiften inkluderas på offertraden och om transaktionskategorin är konfigurerad som debiteringsbar på offertraden. I följande tabell visas hur debiteringsbarheten återställs till standardvärdet för respektive faktiska värde. Standardvärdena baseras på de inkluderade komponenterna och den faktureringstyp som ställs in på offertraden.

| Inkluderar tid | Inkluderar utgift | Roll | Kategori | Uppgift |
| --- | --- | --- | --- | --- |
| Ja | Ja | Debiterbart | Debiterbart | Fakturering för faktiskt värde för Tid: Debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Ej debiterbar | Debiterbart | Fakturering för faktiskt värde för Tid: Ej debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Ej debiterbar | Ej debiterbar | Fakturering för faktiskt värde för Tid: Ej debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Inga | Ja | Kan inte anges | Debiterbart | Fakturering för faktiskt värde för Tid: Inte tillgängligt </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Inga | Ja | Kan inte anges | Ej debiterbar | Fakturering för faktiskt värde för Tid: Inte tillgängligt </br>Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Ja | Inga | Debiterbart | Kan inte anges | Fakturering för faktiskt värde för Tid: Debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Inte tillgängligt |
| Ja | Inga | Ej debiterbar | Kan inte anges | Fakturering för faktiskt värde för Tid: Ej debiterbart </br> Faktureringstyp för faktiskt värde för Utgift: Inte tillgängligt |


[!INCLUDE[footer-include](../includes/footer-banner.md)]