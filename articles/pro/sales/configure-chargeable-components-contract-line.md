---
title: Konfigurera debiteringsbara komponenter i en projektrelaterad kontraktrad
description: I det här ämnet finns information om hur du lägger till debiterbara komponenter i kontraktrader i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085447"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Konfigurera debiteringsbara komponenter i en projektrelaterad kontraktrad

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En projektrelaterad kontraktrad har *inkluderade* komponenter och *debiterbara* komponenter.

Inkluderade komponenter är komponenter som är föremål för:

  - Faktureringsmetod och kunddelning
  - Undre gränser 
  - Inställningar för faktureringsfrekvenser som definierats på den projektbaserade kontraktraden

En delmängd av de inkluderade komponenterna kan markeras som debiterbar med hjälp av fältet **Faktureringstyp**. Fältet **Faktureringstyp** är en alternativuppsättning som gör det möjligt att använda följande värden i kontraktradens sammanhang:

  - Debiterbart
  - Ej debiterbar

Debiterbara komponenter kan definieras för uppgifter, roller och transaktionskategorier.

Debiterbarhet anges för uppgifter för en projektkontraktrad och gäller alla transaktionsklasser som finns på raden. Om fältet **Inkludera uppgifter** på en kontraktrad är tomt eller har värdet **Hela projektet** är fliken **Debiterbara uppgifter** inte tillgängliga.

Debiteringsbarhet som definieras på roller för en projektkontraktsrad gäller endast för transaktionsklassen **Tid**. Om fältet **Inkludera tid** på en kontraktrad är angiven till **Nej** , är fliken **Debiterbara roller** inte tillgänglig.

Debiteringsbarhet som definieras på transaktionskategorier för en projektkontraktsrad gäller endast för transaktionsklassen **Utgift**. Om fältet **Inkludera utgifter** på en kontraktrad är angiven till **Nej** , är fliken **Debiterbara kategorier** inte tillgänglig.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Uppdatera en projektuppgift som debiterbar eller ej debiterbar

En projektuppgift kan vara debiterbar eller ej debiterbar på en specifik kontraktrad som gör följande inställningar möjliga:

Om en projektbaserad kontraktrad innehåller **Tid** och en viss uppgift associerad **T1** till den som debiterbar. Om det finns en andra kontraktrad som inkluderar **Utgift** kan du associera T1-uppgiften på kontraktraden som icke debiterbar. Resultatet blir att all tid som har registrerats på uppgiften är debiterbar och att alla utgifter är icke debiterbara.

Faktureringstypen för en uppgift kan konfigureras under fliken **Debiterbara uppgifter** på kontraktraden genom att uppdatera fältet **Faktureringstyp** i underrutnätet för uppgifter på kontraktraden. Du kan också uppdatera fältet **Faktureringstyp** i underrutnätet för faktureringsinställningar för ett projekt som visar de kontraktrader som är associerade med en uppgift.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Uppdatera en roll som debiterbar eller ej debiterbar

En roll kan vara debiterbar eller inte debiterbar på en specifik kontraktrad.

En rolls faktureringstyp kan konfigureras under fliken **Debiterbara roller** på en kontraktrad. Det gör du genom att uppdatera fältet **Faktureringstyp** i underrutnätet **Debiterbara roller**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori som debiterbar eller inte debiterbar

En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik kontraktrad.

En transaktions faktureringstyp kan konfigureras under fliken **Debiterbara kategorier** på en projektbaserad kontraktrad. Det gör du genom att uppdatera fältet **Faktureringstyp** i underrutnätet **Debiterbara kategorier**.

### <a name="resolve-chargeability"></a>Åtgärda debiterbarhet

En uppskattning eller ett faktiskt värde som skapats för tid anses endast vara debiterbart om **Tid** finns på kontraktraden och om **Uppgift** och **Roll** har konfigurerats som debiterbara på kontraktraden.

En uppskattning eller ett faktiskt värde som skapats för utgift anses endast vara debiterbart om **Utgift** finns på kontraktraden och om kategorierna **Uppgift** och **Transaktion** har konfigurerats som debiterbara på kontraktraden.


| Inkluderar tid | Inkluderar utgift | Inkluderar uppgifter | Roll           | Kategori       | Aktivitet                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ja           | Ja              | Hela projektet | Debiterbart     | Debiterbart     | Fakturering för faktiskt värde för Tid: **Debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Debiterbart**           |
| Ja           | Ja              | Valda uppgifter | Debiterbart     | Debiterbart     | Fakturering för faktiskt värde för Tid: **Debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Debiterbart**           |
| Ja           | Ja              | Valda uppgifter | Ej debiterbar | Debiterbart     | Fakturering för faktiskt värde för Tid: **Ej debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Debiterbart**       |
| Ja           | Ja              | Valda uppgifter | Debiterbart     | Debiterbart     | Fakturering för faktiskt värde för Tid: **Ej debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Ej debiterbart** |
| Ja           | Ja              | Valda uppgifter | Ej debiterbar | Debiterbart     | Fakturering för faktiskt värde för Tid: **Ej debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Ej debiterbart** |
| Ja           | Ja              | Valda uppgifter | Ej debiterbar | Ej debiterbar | Fakturering för faktiskt värde för Tid: **Ej debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Ej debiterbart** |
| Inga            | Ja              | Hela projektet | Kan inte anges   | Debiterbart     | Fakturering för faktiskt värde för Tid: **Inte tillgängligt**</br>Faktureringstyp för faktiskt värde för Utgift: **Debiterbart**          |
| Inga            | Ja              | Hela projektet | Kan inte anges   | Ej debiterbar | Fakturering för faktiskt värde för Tid: **Inte tillgängligt**</br> Faktureringstyp för faktiskt värde för Utgift: **Ej debiterbart**     |
| Ja           | Inga               | Hela projektet | Debiterbart     | Kan inte anges   | Fakturering för faktiskt värde för Tid: **Debiterbart** </br> Faktureringstyp för faktiskt värde för Utgift: **Inte tillgängligt**        |
| Ja           | Inga               | Hela projektet | Ej debiterbar | Kan inte anges   | Fakturering för faktiskt värde för Tid: **Ej debiterbart** </br>Faktureringstyp för faktiskt värde för Utgift: **Inte tillgängligt**   |
