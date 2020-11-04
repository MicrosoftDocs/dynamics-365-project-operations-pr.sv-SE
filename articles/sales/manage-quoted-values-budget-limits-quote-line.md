---
title: Projektbaserade offertrader
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085407"
---
# <a name="project-based-quote-lines"></a>Projektbaserade offertrader

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande. Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:

- Faktureringsmetod
- Projektmappning
- Inkluderade transaktionsklasser
- Undre gräns
- Debiterbar inställning
- Uppskattning med hjälp av offertradsinformation
- Offertradskunder

Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden. Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.

| **Fält** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
| --- | --- | --- |
| Namn | Namnet på en offertrad som kan hjälpa dig att identifiera den diskreta komponenten i offerten som uppskattas. | Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Faktureringsmetod | I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden. Det här fältet innehåller de två huvudmodellerna för kontrakt som stöds av Dynamics 365 Project Operations:</br>- Fast pris</br>- Tid och material.| Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Project | Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet. När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation. När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Inkludera tid | En **Ja**/**Nej** -flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden. Ett **Nej** -värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden. Ett **Ja** -värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Ta med utgift | En **Ja**/**Nej** -flagga anger om utgiftskostnader för det valda projektet ska tas med i uppskattningen på den här offertraden. Ett **Nej** -värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden. Ett **Ja** -värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Inkludera avgift | En **Ja**/**Nej** -flagga anger om avgifter för det valda projektet ska tas med i uppskattningen på den här offertraden. Ett **Nej** -värde anger att avgifterna inte inkluderas i uppskattningen i offertraden. Ett **Ja** -värde anger att avgifterna inkluderas i uppskattningen i offertraden. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Offererad belopp | Det här är det belopp som är offererat till kunden för allt arbete som baseras på den projektbaserade offertraden. I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden. När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Beräknad skatt | Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden. När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Offererat belopp efter skatt | Fältet är offertradsbeloppet efter skatt och skrivskyddat. Beloppet i det här fältet beräknas som *Offererat belopp + moms*. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Undre gräns | Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Kundbudget | Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet. | Detta fältvärde kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader

**Regel 1** : en viss transaktionsklass i det valda projektet kan bara tas med på en projektbaserad offertrad av en offert.

**Regel 2** : om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.

**Regel 3** : om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Affärsmöjlighet</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Offert</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Offertrad</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inkludera tid</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Ta med utgift</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inkludera</strong>
                </p>
                <p>
                    <strong>avgift</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Giltigt/ogiltigt</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Orsak</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Överträdelse av regel 1. Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Inga </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Överträdelse av regel 1. Tid och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Inga </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Tid och avgifter för P1-projekt ingår i QL1.
Utgiften på P1-projektet ingår i QL2.
Det finns ingen överlappning i vad som ska tas med på varje offertrad så att den är giltig.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Inga </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Inga </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Överträdelse av regel 1 ovan </p>
                <p>
I Q1 ingår tid, utgifter och avgifter för hela projektet P1.
                </p>
                <p>
QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och överlappar med vad som ingår i Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Baserat på regel 2 är Q1 och Q2 två offerter av samma affärsmöjlighet, så de båda kan uppskatta samma komponenter i ett projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 på Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Baserat på regel 3 är Q1 och Q2 två offerter av olika affärsmöjligheter, så de kan inte uppskatta samma komponenter i samma projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
                <p>
Ogiltigt </p>
            </td>
        </tr>
    </tbody>
</table>

