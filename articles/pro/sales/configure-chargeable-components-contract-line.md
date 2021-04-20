---
title: Konfigurera debiteringsbara komponenter på en projektbaserad kontraktrad
description: I det här ämnet finns information om hur du lägger till debiterbara komponenter i kontraktrader i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858495"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurera debiteringsbara komponenter på en projektbaserad kontraktrad

_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_

En projektrelaterad kontraktrad har *inkluderade* komponenter och *debiterbara* komponenter.

Inkluderade komponenter är komponenter som är föremål för:

  - Faktureringsmetod och kunddelning
  - Undre gränser 
  - Inställningar för faktureringsfrekvenser som definierats på den projektbaserade kontraktraden

En delmängd av de inkluderade komponenterna kan markeras som debiterbar med hjälp av fältet **Faktureringstyp**. Fältet **Faktureringstyp** är en alternativuppsättning som gör det möjligt att använda följande värden i kontraktradens sammanhang:

  - Debiterbart
  - Ej debiterbar

Debiterbara komponenter kan definieras för uppgifter, roller och transaktionskategorier.

Debiteringsbarhet anges för uppgifter för en projektkontraktrad och gäller alla transaktionsklasser som finns på raden. Om fältet **Inkludera uppgifter** på en kontraktrad är tomt eller har värdet **Hela projektet** är fliken **Debiterbara uppgifter** inte tillgänglig.

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

En beräkning eller faktisk beräkning för tiden kommer endast att anses vara debiterbar om:

   - **Tid** finns med på kontraktraden.
   - **Roll** konfigureras som debiterbar på kontraktraden.
   - **Uppgifter som ingår** anges till **Markerade uppgifter** på kontraktraden.
 
 Om de här tre sakerna stämmer konfigureras uppgiften som debiterbar. 

En beräkning eller faktisk beräkning för utgift kommer endast att anses vara debiterbar om:

   - **Utgift** finns med på kontraktraden
   - **Transaktionskategori** konfigureras som debiterbar på kontraktraden
   - **Uppgifter som ingår** anges till **Markerad uppgift** på kontraktraden
  
 Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar. 

En beräkning eller faktisk beräkning för material kommer endast att anses vara debiterbar om:

   - **Material** finns med på kontraktraden
   - **Uppgifter som ingår** anges till **Markerade uppgifter** på kontraktraden

Om de här två sakerna stämmer konfigureras **uppgiften** som debiterbar. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inkluderar tid</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inkluderar utgift</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Ta med material</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Uppgifter som ingår</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Roll</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategori</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Uppgift</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Påverkan av debiterbarhet</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="70" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för Tid: <strong>Debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde för Utgift: <strong>Debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt material: <strong>Debiterbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="70" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för Tid: <strong>Debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde för Utgift: <strong>Debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt material: <strong>Debiterbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde för Utgift: Debiterbart </p>
                <p>
Faktureringstyp för faktiskt material: Debiterbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="70" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av material: <strong>Ej debiterbart</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt material: Debiterbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inga</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Debiterbart</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde för Utgift: Debiterbart </p>
                <p>
Faktureringstyp för faktiskt material: Debiterbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inga</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Inte tillgängligt</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt material: Debiterbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inga</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för Tid: Debiterbart </p>
                <p>
Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </p>
                <p>
Faktureringstyp för faktiskt material: Debiterbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inga</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde för utgift:<strong> Inte tillgängligt</strong>
                </p>
                <p>
Faktureringstyp för faktiskt material: Debiterbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inga</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="70" valign="top">
                <p>
Debiterbart </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för Tid: Debiterbart </p>
                <p>
Faktureringstyp för faktiskt värde för Utgift: Debiterbart </p>
                <p>
Faktureringstyp för faktiskt värde för material:<strong> Inte tillgängligt</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inga</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Hela projektet </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Ej debiterbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kan inte anges </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för tid: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde av utgift: <strong>Ej debiterbart</strong>
                </p>
                <p>
Faktureringstyp för faktiskt värde för material: <strong>Inte tillgängligt</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
