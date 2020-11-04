---
title: Konfigurera de debiterbara komponenterna på en offertrad
description: I det här ämnet finns information om hur du konfigurerar debiterbara och icke debiterbara komponenter på en projektbaserad offertrad.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085661"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurera de debiterbara komponenterna på en offertrad

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En projektrelaterad offertrad har konceptet av *inkluderade* komponenter och *debiterbara* komponenter.

Inkluderade komponenter är föremål för följande:

  - Faktureringsmetod och kunddelning
  - Undre gränser 
  - Inställningar för faktureringsfrekvenser som definierats på den projektbaserade offertraden

En delmängd av de inkluderade komponenterna kan markeras som debiterbar med hjälp av fältet **Faktureringstyp**. Fältet **Faktureringstyp** är en alternativuppsättning som gör det möjligt att använda följande värden i offertradens sammanhang:

  - Debiterbart
  - Ej debiterbar

Debiterbara komponenter kan definieras för uppgifter, roller och transaktionskategorier.

Debiterbarhet anges för uppgifter för en offertrad och gäller alla transaktionsklasser som finns på raden. Om fältet **Inkludera uppgifter** är inställt på **Hela projektet** eller är tomt, är fliken **Debiterbara uppgifter** inte tillgänglig.

Debiterbarhet definieras på roller för en offertrad och gäller endast för transaktionsklassen **Tid**. Om fältet **Inkludera tid** är inställt på **Nej** på en projektoffertsrad, är fliken **Debiterbara roller** inte tillgänglig.

Debiterbarhet definieras på transaktionskategorier för en offertrad och gäller endast för transaktionsklassen **Utgift**. Om fältet **Inkludera utgifter** är inställt på **Nej** på en projektoffertsrad, är fliken **Debiterbara kategorier** inte tillgänglig.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Uppdatera en projektuppgift så att den är debiterbar eller ej debiterbar

En projektuppgift kan vara debiterbar eller ej debiterbar i kontexten för en specifik projektbaserad offertrad, vilket gör följande konfiguration möjlig:

Om en projektbaserad offertrad innehåller **Tid** och uppgiften **T1** associeras uppgiften till offertraden som debiterbar. Om det finns en andra offertrad som inkluderar **Utgifter** kan du associera uppgiften **T1** på offertraden som icke debiterbar. Resultatet blir att all tid som registreras på uppgiften är debiterbar och att alla utgifter som registreras på uppgiften är icke debiterbara.

Faktureringstypen för en uppgift kan konfigureras under fliken **Debiterbara uppgifter** på en projektbaserad offertrad genom att uppdatera fältet **Faktureringstyp** i underrutnätet **Offertradsuppgifter**. Du kan också uppdatera faktureringstypen för en projektuppgift i fältet **Faktureringstyp** i underrutnätet för faktureringsinställningar för en uppgift som visar de offertrader som är associerade med en uppgift.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Uppdatera en roll så att den är debiterbar eller ej debiterbar

En roll kan vara debiterbar eller inte debiterbar i kontexten för en specifik projektbaserad offertrad.

Faktureringstypen för en roll kan konfigureras under fliken **Debiterbara roller** på en offertrad genom att uppdatera fältet **Faktureringstyp** i underrutnätet **Debiterbara roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar

En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik offertrad.

Faktureringstypen för en transaktion kan konfigureras under fliken **Debiterbara kategorier** på en offertrad genom att uppdatera fältet **Faktureringstyp** i underrutnätet **Debiterbara kategorier**.

### <a name="resolve-chargeability"></a>Åtgärda debiterbarhet
En uppskattning eller ett faktiskt värde som skapats för tid anses endast vara debiterbart om **Tid** finns på offertraden och om **Uppgift** och **Roll** har konfigurerats som debiterbara på offertraden.

En uppskattning eller ett faktiskt värde som skapats för utgift anses endast vara debiterbart om **Utgift** finns på offertraden och om **Uppgift** och **Transaktionskategori** har konfigurerats som debiterbara på offertraden.

| Inkluderar tid | Inkluderar utgift | Uppgifter som ingår | Roll | Kategori | Aktivitet | Fakturering |
| --- | --- | --- | --- | --- | --- | --- |
| Ja | Ja | Hela projektet | Debiterbart | Debiterbart | Kan inte anges | Fakturering för faktiskt värde för Tid: Debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Endast valda uppgifter | Debiterbart | Debiterbart | Debiterbart | Fakturering för faktiskt värde för Tid: Debiterbart</br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Endast valda uppgifter | Ej debiterbar | Debiterbart | Debiterbart | Fakturering för faktiskt värde för Tid: Ej debiterbart</br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Ja | Ja | Endast valda uppgifter | Debiterbart | Debiterbart | Ej debiterbar | Fakturering för faktiskt värde för Tid: Ej debiterbart</br> Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Ja | Ja | Endast valda uppgifter | Ej debiterbar | Debiterbart | Ej debiterbar | Fakturering för faktiskt värde för Tid: Ej debiterbart</br> Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Ja | Ja | Endast valda uppgifter | Ej debiterbar | Ej debiterbar | Debiterbart | Fakturering för faktiskt värde för Tid: Ej debiterbart</br> Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Inga | Ja | Hela projektet | Kan inte anges | Debiterbart | Kan inte anges | Fakturering för faktiskt värde för Tid: Inte tillgängligt </br>Faktureringstyp för faktiskt värde för Utgift: Debiterbart |
| Inga | Ja | Hela projektet | Kan inte anges | Ej debiterbar | Kan inte anges | Fakturering för faktiskt värde för Tid: Inte tillgängligt </br>Faktureringstyp för faktiskt värde för Utgift: Ej debiterbart |
| Ja | Inga | Hela projektet | Debiterbart | Kan inte anges | Kan inte anges | Fakturering för faktiskt värde för Tid: Debiterbart</br>Faktureringstyp för faktiskt värde för Utgift: Inte tillgängligt |
| Ja | Inga | Hela projektet | Ej debiterbar | Kan inte anges | Kan inte anges | Fakturering för faktiskt värde för Tid: Ej debiterbart </br>Faktureringstyp för faktiskt värde för Utgift: Inte tillgängligt |
