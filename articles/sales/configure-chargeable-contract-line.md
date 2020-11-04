---
title: Konfigurera debiterbara komponenter i en projektbaserad kontraktrad
description: I det här ämnet finns information om inkluderade, debiterbara och icke debiterbara komponenter på kontraktrader.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085477"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurera debiterbara komponenter i en projektbaserad kontraktrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En projektrelaterad kontraktrad har konceptet av inkluderade, debiterbara och icke debiterbara komponenter.

Inkluderade komponenter omfattas av faktureringsmetoden, kundens delningar, gränser som inte för överskridas och inställningarna för faktureringsfrekvenser som definierats på den projektbaserade kontraktraden.

En delmängd av de inkluderade komponenterna kan markeras som debiterbar genom att uppdatera fältet **Faktureringstyp**.

Debiterbara komponenter kan definieras för roller och transaktionskategorier.

För en projektkontraktsrad gäller endast den debiterbarhet som angetts för en roll för transaktionsklassen **Tid**. Om **Inkludera tid** är inställt på **Nej** på en projektkontraktrad, är fliken **Debiterbara roller** inte tillgänglig.

Debiteringsbarhet som definieras på transaktionskategorier för en projektkontraktsrad gäller endast för transaktionsklassen **Utgift**. Om **Inkludera utgifter** är inställt på **Nej** på en projektkontraktrad, är fliken **Debiterbara kategorier** inte tillgänglig.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Uppdatera en roll så att den är debiterbar eller ej debiterbar

En roll kan vara debiterbar eller inte debiterbar på en specifik projektbaserad kontraktrad.

Under fliken **Debiterbara roller** på en projektbaserad kontraktrad, i underrutnätet **Debiterbara kategorier** , i fältet **Faktureringstyp** , uppdaterar du faktureringstypen för en roll.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar

En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik projektbaserad kontraktrad.

Under fliken **Debiterbara kategorier** på en projektbaserad kontraktrad, i underrutnätet **Debiterbara kategorier** , i fältet **Faktureringstyp** , uppdaterar du faktureringstypen för en transaktion.

### <a name="resolve-chargeability"></a>Åtgärda debiterbarhet

En uppskattning eller ett faktiskt värde som skapats för tid anses endast vara debiterbart om Tid finns på kontraktraden och om rollen har konfigurerats som debiterbar på kontraktraden.

En uppskattning eller ett faktiskt värde som skapats för utgift anses endast vara debiterbart om Utgift finns på kontraktraden och om transaktionskategorin har konfigurerats som debiterbar på kontraktraden.

| Inkluderar tid | Inkluderar utgift | Roll | Kategori | Aktivitet |
| --- | --- | --- | --- | --- |
| Ja | Ja | Debiterbart | Debiterbart | Fakturering för faktiskt värde för Tid: Debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Ej debiterbar | Debiterbart | Fakturering för faktiskt värde för Tid: Ej debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Ej debiterbar | Ej debiterbar | Fakturering för faktiskt värde för Tid: Ej debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Inga | Ja | Kan inte anges | Debiterbart | Fakturering för faktiskt värde för Tid: Inte tillgängligt </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Inga | Ja | Kan inte anges | Ej debiterbar | Fakturering för faktiskt värde för Tid: Inte tillgängligt </br>Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Ja | Inga | Debiterbart | Kan inte anges | Fakturering för faktiskt värde för Tid: Debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Inte tillgängligt |
| Ja | Inga | Ej debiterbar | Kan inte anges | Fakturering för faktiskt värde för Tid: Ej debiterbart </br> Faktureringstyp för faktiskt värde för Utgift: Inte tillgängligt |
