---
title: Korrigerade fakturor - lite
description: I det här ämnet finns information om korrigerade fakturor i Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274255"
---
# <a name="corrected-invoices---lite"></a>Korrigerade fakturor - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En bekräftad projektfaktura kan korrigeras för att bearbeta förändringar eller krediter som har förhandlats med kunden och projektledaren.

Om du vill göra ändringar i en bekräftad faktura öppnar du den bekräftade fakturan och väljer **Korrigera den här fakturan**. 

> [!NOTE]
> Det här alternativet är endast tillgängligt om projektfakturan är bekräftad.

Ett nytt utkast till faktura skapas från den bekräftade fakturan. All fakturaradsinformation från den tidigare bekräftade fakturan kopieras till det nya utkastet. Nedan följer några av de viktigaste begreppen som du bör förstå om radinformation på den nya korrigerade fakturan:

- Alla kvantiteter uppdateras till noll. Programmet antar att alla fakturerade artiklar är helt krediterade. Om det behövs kan du manuellt uppdatera dessa kvantiteter för att återspegla den kvantitet som faktureras och inte den kvantitet som krediteras. Beroende på vilken kvantitet du anger beräknar programmet det krediterade antalet. Det här beloppet återspeglas i de faktiska värdena som skapas när den korrigerade fakturan bekräftas. Om du gör ändringar i momsbeloppet måste du ange rätt momsbelopp och inte det momsbelopp som ska krediteras.
- Tidigare bekräftade produktbaserade kontraktrader kopieras inte över. Bearbetning av korrigeringar på en produktbaserad projektfaktura stöds inte.
- Ändringar av milstolpar bearbetas alltid som fulla krediter.
- Behållare eller förskott kan korrigeras om kunden fakturerades för ett felaktigt belopp.
- Det går att korrigera avstämningar av behållare och förskott om ett felaktigt belopp användes för att stämma av mot avgifterna på en tidigare bekräftad faktura.

> [!IMPORTANT]
> Fakturaradsinformation som är korrigeringar av andra redan fakturerade avgifter har fältet **Korrigering** värdet **Ja**. Fakturor med korrigerad fakturaradsinformation har ett fält med namnet **Har korrigeringar** som också har värdet **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiska värden som skapas vid bekräftelse av en korrigeringsfaktura:

Nedan visas de faktiska värden som skapas av programmet vid bekräftelse av korrigeringen utifrån de åtgärder som utförs på utkastet till den korrigerade fakturan innan bekräftelse.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Bekräfta korrigeringen av ett fakturerat förskott eller en behållare.<strong></strong>
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
Ett fakturerat faktiskt värde för försäljning skapas för beloppet på arvodet eller förskottet för att återföra den ursprungliga fakturerade försäljningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt fakturerat faktiskt värde för försäljning skapas för det korrigerade beloppet på behållaren eller den förskottsbaserade korrigerade fakturaraden.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett icke fakturerat faktiskt värde för försäljning av ett negativt belopp av arvodet eller den förskottsbaserade fakturaraden, som ska användas för avstämning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
En bekräftelse av korrigeringen av ett tidigare avstämt arvode eller förskott.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturerad återförd försäljning av arvodet eller förskottet som skapades för avstämning. Det här beloppet är positivt och är avsett att ta bort det negativ som skapades när den tidigare avstämningen gjordes.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Återföring av ett fakturerat faktiskt värde för försäljning för beloppet på föregående faktura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt fakturerat faktiskt värde för försäljning för det korrigerade kvarhållarbeloppet som tillämpas på den korrigerade fakturan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett icke fakturerat faktiskt värde för försäljning med ett negativt belopp från den överblivna arvodet eller förskottet, som ska användas för avstämning på senare fakturor.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av hela krediten för en tidigare fakturerad tidstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt fakturerat faktiskt värde för försäljning som gäller timmar och belopp på den ursprungliga fakturaradsinformationen för tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av delkrediten för en tidstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller timmar och belopp som fakturerats på den ursprungliga fakturaradsinformationen för tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för timmar och belopp på den redigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående timmar och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av hela krediten för en tidigare fakturerad utgiftstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för utgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering av delkrediten för en tidigare fakturerad utgiftstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för en utgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ej fakturerat faktiskt värde för försäljning som debiteras för återstående kvantitet och belopp efter avdrag för de korrigerade siffrorna i fakturaradsinformationen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av hela krediten för en tidigare fakturerad avgiftstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som gäller kvantitet och belopp på den ursprungliga fakturaradsinformationen för avgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering av delkrediten för en tidigare fakturerad avgiftstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller kvantitet och belopp som fakturerats på den ursprungliga fakturaradsinformationen för avgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ett nytt ofakturerat faktiskt värde för försäljning som är debiterbart för kvantitet och belopp på den redigerade korrigerade fakturaraden, en återföring av detta och ett motsvarande fakturerat faktiskt värde för försäljning.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering av hela krediten för en tidigare fakturerad milstolpe.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Återförande av en fakturerad försäljning som gäller belopp på den ursprungliga fakturaradsinformationen för milstolpen.
                </p>
                <p>
Milstolpens faktura- eller faktureringsstatus på projektkontraktsraden uppdateras till **Redo att fakturera**.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering av delkrediten för en tidigare fakturerad milstolpe.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stöds inte </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Kredit och korrigeringar av en tidigare fakturerad produktbaserad kontraktrad.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stöds inte </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]