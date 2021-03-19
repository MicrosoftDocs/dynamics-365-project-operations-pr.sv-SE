---
title: Konfigurera debiterbara komponenter på en offertrad- lite
description: I det här ämnet finns information om hur du konfigurerar debiterbara och icke debiterbara komponenter på en projektbaserad offertrad.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273895"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Konfigurera debiterbara komponenter på en offertrad- lite

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

Faktureringstypen för en uppgift kan konfigureras på **Debiterbara uppgifter** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **offertradens uppgifter**. Alternativt kan du uppdatera faktureringstypen för en projektuppgift i **faktureringstyp** fält på undernätet för uppgiftsfakturering för ett projekt som visar offertraderna som är associerade med en uppgift.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Uppdatera en roll så att den är debiterbar eller ej debiterbar

En roll kan vara debiterbar eller inte debiterbar i kontexten för en specifik projektbaserad offertrad.

Faktureringstypen för roller uppgift kan konfigureras på **Debiterbara roller** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **Debiterbara roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar

En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik offertrad.

En transaktion faktureringstyp kan konfigureras på **Debiterbara kategorier** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** på underrutnätet **Debiterbara kategorier**.

### <a name="resolve-chargeability"></a>Åtgärda debiteringsbarhet
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]