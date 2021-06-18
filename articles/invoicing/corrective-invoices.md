---
title: Skapa projektbaserade fakturor för korrigering
description: Detta ämne ger information om korrigeringsfakturor i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001656"
---
# <a name="create-corrective-project-based-invoices"></a>Skapa projektbaserade fakturor för korrigering 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En bekräftad projektfaktura kan korrigeras för att bearbeta förändringar eller krediter som har förhandlats med kunden och projektledaren.

Om du vill göra ändringar i en bekräftad faktura öppnar du den bekräftade fakturan och väljer **Korrigera den här fakturan**. 

> [!NOTE]
> Det här alternativet är endast tillgängligt om projektfakturan är bekräftad.

Ett nytt utkast till faktura skapas från den bekräftade fakturan. All fakturaradsinformation från den tidigare bekräftade fakturan kopieras till det nya utkastet. Nedan följer några viktiga punkter som hjälper dig att förstå mer om radinformationen för den nya korrigerade fakturan:

- Alla kvantiteter uppdateras till noll. Detta förutsätter att alla fakturerade objekt krediteras helt. Om det behövs kan du manuellt uppdatera dessa kvantiteter för att återspegla den kvantitet som faktureras och inte den kvantitet som krediteras. Beroende på vilken kvantitet du anger beräknar programmet det krediterade antalet. Det här beloppet återspeglas i de faktiska värdena som skapas när den korrigerade fakturan bekräftas. Om du gör ändringar i momsbeloppet måste du ange rätt momsbelopp och inte det momsbelopp som ska krediteras.
- Ändringar av milstolpar bearbetas alltid som fulla krediter.
- Behållare eller förskott kan korrigeras om kunden fakturerades för ett felaktigt belopp.
- Det går att korrigera avstämningar av behållare och förskott om ett felaktigt belopp användes för att stämma av mot avgifterna på en tidigare bekräftad faktura.

> [!IMPORTANT]
> Fakturaradsinformation som är korrigeringar för andra redan fakturerade debiteringar har fältet **Korrigering** angett till **Ja**. Fakturor med korrigerad fakturaradsinformation har ett fält med namnet **Har korrigeringar** som också har värdet **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiska värden som skapas vid bekräftelse av en korrigeringsfaktura

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
Stöds inte </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
