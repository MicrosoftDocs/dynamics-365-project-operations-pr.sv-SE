---
title: Bekräfta en proforma-faktura
description: I det här ämnet finns information om hur du bekräftar proforma-fakturor i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085448"
---
# <a name="confirming-a-proforma-invoice"></a>Bekräfta en proforma-faktura

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


När en proforma-faktura har bekräftats uppdateras statusen på projektfakturan till **Bekräftad**. När en faktura har bekräftats blir den skrivskyddad. I framtiden går det bara att korrigera en faktura om korrigering eller kreditering har inletts av kunden, eller om fakturan har markerats som betald.

I följande tabell visas de faktiska värden som har skapats av systemet. Dessa faktiska värden skapas när vissa operationer utförs i utkastet av projektfakturan innan den bekräftas.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Faktiska värden skapas vid bekräftelse</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturera ett förskott eller ett arvode </p>
            </td>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning av typen <strong>Arvode</strong> skapas för beloppet på förskottet eller arvodet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett icke fakturerat faktiskt värde för försäljning av ett negativt belopp av arvodet eller förskottet som ska användas för avstämning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
När du har stämt av ett arvode eller ett förskott på en faktura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning. Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning för beloppet på den här fakturan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
När du har delvis stämt av ett arvode eller ett förskott på en faktura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning. Det här beloppet är positivt eftersom det är avsett att ta bort det negativ som skapades när arvodet eller förskottet fakturerades.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning för beloppet på den här fakturan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett negativt icke fakturerat faktiskt värde för försäljning av det kvarstående beloppet av arvodet eller förskottet som ska användas för avstämning på framtida fakturor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en tidtransaktion utan några ändringar i utkastfakturan.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av en tidstransaktion som redigerades för att minska antalet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för de återstående timmarna och det återstående beloppet efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en tidstransaktion som redigerades för att öka antalet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en ofakturerad försäljning som gäller timmar och belopp på det ursprungliga tidsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en utgiftstransaktion utan några ändringar i utkastfakturan.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av en utgiftstransaktion som redigerades för att minska antalet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som inte är debiterbart för återstående kvantitet och belopp efter att de korrigerade siffrorna har dragits av på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en utgiftstransaktion som redigerades för att öka antalet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återföring av en ofakturerad försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för återstående kvantitet och belopp på den redigerade fakturaraden, en återföring av det ofakturerade faktiska värdet för försäljning och ett motsvarande fakturerat faktiskt värde för försäljning. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av en avgift.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en ofakturerad försäljning som gäller avgiftbeloppet på den ursprungliga journalraden.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga journalraden för avgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturera en milstolpe.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning för milstolpens belopp på den ursprungliga milstolpen på projektkontraktraden.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturera en produktbaserad kontraktrad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ett fakturerat faktiskt värde för försäljning för produktraden med kvantitet och belopp som kommer från den produktbaserade kontraktraden.
                </p>
            </td>
        </tr>
    </tbody>
</table>
