---
title: Konfigurera debiteringsbara komponenter på en projektbaserad kontraktrad - lite
description: I det här ämnet finns information om hur du lägger till debiterbara komponenter i kontraktrader i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513901"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurera debiteringsbara komponenter på en projektbaserad kontraktrad - lite

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

Debiteringsbarhet anges för uppgifter för en projektkontraktrad och gäller alla transaktionsklasser som finns på raden. Om fältet **Inkludera uppgifter** på en kontraktrad är tomt eller har värdet ***Hela projektet*** är fliken **Debiterbara uppgifter** inte tillgänglig.

Debiteringsbarhet som definieras på roller för en projektkontraktsrad gäller endast för transaktionsklassen **Tid**. Om fältet **Inkludera tid** på en kontraktrad är angiven till **Nej**, är fliken **Debiterbara roller** inte tillgänglig.

Debiteringsbarhet som definieras på transaktionskategorier för en projektkontraktsrad gäller endast för transaktionsklassen **Utgift**. Om fältet **Inkludera utgifter** på en kontraktrad är angiven till **Nej**, är fliken **Debiterbara kategorier** inte tillgänglig.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Uppdatera en projektuppgift som debiterbar eller ej debiterbar

En projektuppgift kan vara debiterbar eller ej debiterbar på en specifik kontraktrad som gör följande inställningar möjliga:

Om en projektbaserad kontraktrad innehåller **Tid** och en viss uppgift associerad **T1** till den som debiterbar. Om det finns en andra kontraktrad som inkluderar **Utgift** kan du associera T1-uppgiften på kontraktraden som icke debiterbar. Resultatet blir att all tid som har registrerats på uppgiften är debiterbar och att alla utgifter är icke debiterbara.

Faktureringstypen för en uppgift kan konfigureras på **Debiterbara uppgifter** på kontraktraden genom att uppdatera fält **Faktureringstyp** i underrutnätet uppgifter i kontraktsraden. Du kan också uppdatera fältet **faktureringstyp** i underrutnätet i inställningarna för uppgiftsfakturering i ett projekt som visar de kontraktrader som är associerade med en uppgift.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Uppdatera en roll som debiterbar eller ej debiterbar

En roll kan vara debiterbar eller inte debiterbar på en specifik kontraktrad.

En rolls faktureringstyp kan konfigureras under fliken **Debiterbara roller** på en kontraktrad. Det gör du genom att uppdatera fältet **faktureringstyp** i under rutnätet **debiterbara roller**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori som debiterbar eller inte debiterbar

En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik kontraktrad.

En transaktions faktureringstyp kan konfigureras under fliken **Debiterbara kategorier** på en projektbaserad kontraktrad. Det gör du genom att uppdatera fältet **faktureringstyp** i under rutnätet **debiterbara kategorier**.

### <a name="resolve-chargeability"></a>Åtgärda debiteringsbarhet

En uppskattning eller ett faktiskt värde som skapats för tid anses endast vara debiterbart om **Tid** finns på kontraktraden och om **Uppgift** och **Roll** har konfigurerats som debiterbara på kontraktraden.

En uppskattning eller ett faktiskt värde som skapats för utgift anses endast vara debiterbart om **Utgift** finns på kontraktraden och om kategorierna **Uppgift** och **Transaktion** har konfigurerats som debiterbara på kontraktraden.


| Inkluderar tid | Inkluderar utgift | Inkluderar uppgifter | Roll           | Kategori       | Uppgift                                                                                                      |
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]