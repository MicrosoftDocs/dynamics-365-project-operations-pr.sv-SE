---
title: Projektbaserade fakturor för korrigering
description: Den här artikeln innehåller information om hur du skapar och bekräftar korrigerande projektbaserade fakturor i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931122"
---
# <a name="corrective-project-based-invoices"></a>Projektbaserade fakturor för korrigering

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

En bekräftad projektfaktura kan korrigeras för att bearbeta förändringar eller krediter som har förhandlats med kunden och projektledaren.

Om du vill göra ändringar i en bekräftad faktura öppnar du den bekräftade fakturan och väljer **Korrigera den här fakturan**. 

> [!NOTE]
> Detta val är inte tillgängligt om inte en projektfaktura bekräftas eller om den projektbaserade fakturan har förskott eller arvode eller avstämningar av förskott eller arvode.

Ett nytt utkast till faktura skapas från den bekräftade fakturan. All fakturaradsinformation från den tidigare bekräftade fakturan kopieras till det nya utkastet. Nedan följer några av de viktigaste begreppen som du bör förstå om radinformation på den nya korrigerade fakturan:

- Alla kvantiteter uppdateras till noll. Dynamics 365 Project Operations förutsätter att alla fakturerade objekt krediteras helt. Om det behövs kan du manuellt uppdatera dessa kvantiteter för att återspegla den kvantitet som faktureras och inte den kvantitet som krediteras. Beroende på vilken kvantitet du anger beräknar programmet det krediterade antalet. Det här beloppet återspeglas i de faktiska värdena som skapas när den korrigerade fakturan bekräftas. Om du gör ändringar i momsbeloppet måste du ange rätt momsbelopp och inte det momsbelopp som ska krediteras.
- Ändringar av milstolpar bearbetas alltid som fulla krediter.


> [!IMPORTANT]
> För fakturaradsinformation som är korrigeringar för andra redan fakturerade debiteringar har fältet **Korrigering** angett till **Ja**. För fakturor som har korrigerat fakturaradinformation har fältet **Har korrigeringar** angett till **Ja**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Fakta som skapas när en korrigerande faktura bekräftas

I följande tabell visas de faktiska värden som skapas när en korrigeringsfaktura bekräftas.

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
Fakturera hela krediten för en tidigare fakturerad materialtransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturerad försäljning för kvantitet och belopp på det ursprungliga fakturadetalj för material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ofakturerad faktisk försäljning för kvantitet och belopp på det ursprungliga fakturadetalj för material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturera delkrediten för en materialtransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En fakturerad försäljning för kvantitet och fakturerat belopp på det ursprungliga fakturadetalj för material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny faktisk ofakturerad försäljning som är debiterbar för kvantitet och belopp på den redigerade fakturaradsdetaljen, en siffra som motsvarar den faktiska faktureringen.
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
Fakturastatus för milstolpen uppdateras från det att <b>Bokförd kundfaktura</b> till <b>Klar att fakturera</b>.
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
Det här scenariot stöds inte.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
