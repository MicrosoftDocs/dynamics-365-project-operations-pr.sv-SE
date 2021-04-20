---
title: Konfigurera de debiterbara komponenterna på en offertrad
description: I det här ämnet finns information om hur du konfigurerar debiterbara och icke debiterbara komponenter på en projektbaserad offertrad.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858315"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurera debiterbara komponenter på en offertrad 

_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_

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

En projektuppgift kan vara debiterbar eller ej debiterbar i kontexten för en specifik projektbaserad offertrad, vilket gör följande konfiguration möjlig.

Om en projektbaserad offertrad innehåller **Tid** och uppgiften **T1** associeras uppgiften till offertraden som debiterbar. Om det finns en andra offertrad som inkluderar **Utgifter** kan du associera uppgiften **T1** på offertraden som icke debiterbar. Resultatet blir att all tid som registreras på uppgiften är debiterbar och att alla utgifter som registreras på uppgiften är icke debiterbara.

Faktureringstypen för en uppgift kan konfigureras på **Debiterbara uppgifter** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **offertradens uppgifter**. Alternativt kan du uppdatera faktureringstypen för en projektuppgift i **faktureringstyp** fält på undernätet för uppgiftsfakturering för ett projekt som visar offertraderna som är associerade med en uppgift.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Uppdatera en roll så att den är debiterbar eller ej debiterbar

En roll kan vara debiterbar eller inte debiterbar i kontexten för en specifik projektbaserad offertrad.

Faktureringstypen för roller uppgift kan konfigureras på **Debiterbara roller** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** i underrutnätet **Debiterbara roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Uppdatera en transaktionskategori så att den är debiterbar eller inte debiterbar

En transaktionskategori kan vara debiterbar eller inte debiterbar på en specifik offertrad.

En transaktion faktureringstyp kan konfigureras på **Debiterbara kategorier** på en projektbaserad offertrad genom uppdatering fält **Faktureringstyp** på underrutnätet **Debiterbara kategorier**.

### <a name="resolve-chargeability"></a>Åtgärda debiteringsbarhet
En beräkning eller faktisk beräkning för tid kommer endast att anses vara debiterbar om:

   - **Tid** finns med på offertraden.
   - **Roll** konfigureras som debiterbar på offertraden.
   - **Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden. 

Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar. 

En beräkning eller faktisk beräkning för utgift kommer endast att anses vara debiterbar om: 

   - **Utgift** finns med på offertraden.
   - **Transaktionskategori** konfigureras som debiterbar på offertraden.
   - **Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.

Om de här tre sakerna stämmer konfigureras **uppgiften** som debiterbar. 

En beräkning eller faktisk beräkning för material kommer endast att anses vara debiterbar om:

   - **Material** finns med på offertraden.
   - **Uppgifter som ingår** anges till **Markerade uppgifter** på offertraden.

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
Fakturering för faktiskt värde för Tid: Debiterbart </p>
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
Debiterbart </p>
            </td>
            <td width="350" valign="top">
                <p>
Fakturering för faktiskt värde för Tid: Debiterbart </p>
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
