---
title: Bekräfta en proforma projektbaserad faktura
description: Den här artikeln innehåller information om bekräfta proforma-projektbaserad faktura.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a4ad243e8959af61993e2ff6ce89209be378f7df
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929466"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Bekräfta en proforma projektbaserad faktura

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

När en proforma-faktura har bekräftats uppdateras statusen på projektfakturan till **Bekräftad**. När en faktura har bekräftats blir den skrivskyddad. Framöver kan fakturan endast korrigeras om det finns några korrigeringar eller krediter som initierats av kunden.

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
En ofakturerad försäljning med ett negativt belopp för den försäljare eller det förskott som ska användas för avstämning.
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
Ny icke fakturerad försäljning som är icke debiterbar för återstående timmar och belopp efter att ha dras av de korrigerade siffrorna i detalj på den redigerade fakturaraden, en jämförelse av den faktiska försäljningen och motsvarande faktiska fakturering.
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
Ett fakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på det ursprungliga utgiftsgodkännandet.
                </p>
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
Fakturera en materialtransaktion utan att redigera utkastfakturan.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ofakturerad försäljning för kvantitet och belopp på det ursprungliga godkännandet av materialanvändningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En fakturerad faktisk försäljning för kvantitet och belopp på det ursprungliga godkännandet av materialanvändningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturera en materialtransaktion som redigerats för att minska kvantiteten.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ofakturerad försäljning för kvantitet och belopp på det ursprungliga godkännandet av tidsanvändningen.
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
Fakturera en materialtransaktion som redigerats för att öka kvantiteten.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En ofakturerad försäljning för kvantitet och belopp på det ursprungliga godkännandet av materialanvändningen.
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
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
