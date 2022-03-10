---
title: Projektbaserade offertrader – Översikt
description: I det här ämnet finns information om hur du använder projektbaserade offertrader för projektarbete.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 2f2d38c7fb3bc3ec26cf64525ef8275adecafd7fc48e97d6daef595d341c045d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001588"
---
# <a name="project-based-quote-lines-overview"></a>Projektbaserade offertrader – Översikt 

_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_

Projektbaserade offertrader har utformats för att hjälpa till att uppskatta projektarbetet för ett åtagande. Strukturen på en projektrelaterad offertrad utökas för projektuppskattningar med följande koncept:

- Faktureringsmetod
- Mappning av projekt och uppgifter
- Inkluderade transaktionsklasser
- Undre gräns
- Debiterbar inställning
- Uppskattning med hjälp av offertradsinformation
- Offertradskunder

Följande tabell innehåller information om fälten under fliken **Allmänt** i den projektbaserade offertraden. Med hjälp av dessa fält kan du konfigurera grunden för en detaljerad uppskattning för projektarbete.

| **Fält** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- |
| Namn | Namnet på offertraden som gör det lättare att identifiera den diskreta komponenten i offerten som beräknas. | Kopieras till projektkontraktraden som skapas från den här offertraden när offerten har vunnits. |
| Faktureringsmetod | I en offert som skapats från en affärsmöjlighet kopieras värdet från motsvarande fält på affärsmöjlighetsraden. Fältet innehåller de två huvudkontraktsmodeller som stöds av Dynamics 365 Project Operations:</br>- Fast pris</br>- Tid och material.| Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Project | Använd det här valfria fältet för att identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet. När ett projekt är mappat till en offertrad bidrar det till att lägga till debiterbara uppgifter och till att i en projektbaserad uppskattning använda offertraden som offertradsinformation. När ett projekt inte är mappat till en projektrelaterad offertrad ska du skapa uppskattningen manuellt genom att skapa varje offertradsinformation. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns.|
| Uppgifter som ingår | Anger om den här offertraden används för alla eller några av projektuppgifterna för det valda projektet. Fältet har följande möjliga värden:</br>- Alla projektuppgifter</br>- Endast valda projektuppgifter</br>Ett tomt värde i det här fältet motsvarar alternativet **Alla projektuppgifter**. | När **Endast markerade projektuppgifter** väljs på projektsidan låter fliken **Faktureringsinställningar för uppgift** dig välja specifika uppgifter för att associera dem till denna offertrad. Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Inkludera tid | Ett värde **Ja**/**Nej** anger om tidstransaktioner eller arbetskostnader för det valda projektet kommer att tas med i beräkningen på offertraden. Ett **Nej**-värde anger att tidstransaktionerna eller arbetskostnaderna inte inkluderas i uppskattningen i offertraden. Ett **Ja**-värde anger att tidstransaktionerna eller arbetskostnaderna inkluderas i uppskattningen i offertraden. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Ta med utgift | Ett värde **Ja**/**Nej** anger om utgiftskostnader för det valda projektet kommer att tas med i beräkningen på offertraden. Ett **Nej**-värde anger att utgiftskostnaderna inte inkluderas i uppskattningen i offertraden. Ett **Ja**-värde anger att utgiftskostnaderna inkluderas i uppskattningen i offertraden. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Ta med material | Ett värde **Ja**/**Nej** anger om materialkostnader för det valda projektet kommer att tas med i beräkningen på offertraden. Ett värde för **Nej** indikerar att materialkostnaderna inte kommer att inkluderas i uppskattningen på denna offertrad. Ett värde för **Ja** indikerar att materialkostnaderna kommer att inkluderas i uppskattningen på denna offertrad. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Inkludera avgift | Ett värde **Ja**/**Nej** anger om utgifter för det valda projektet kommer att tas med i beräkningen på offertraden. Ett **Nej**-värde anger att utgifterna inte inkluderas i uppskattningen i offertraden. Ett **Ja**-värde anger att utgifterna inkluderas i uppskattningen i offertraden. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Offererad belopp | Det här är det belopp som kunden ska beräknas för allt arbete som förutses på den projektbaserade offertraden. I en offert som skapats från en affärsmöjlighet kopieras värdet från fältet **Kundbudget** på affärsmöjlighetsraden. När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån beloppet i offertradsinformationen. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Beräknad skatt | Det här är ett redigerbart fält för användaren att lägga till det uppskattade momsbeloppet på offertraden. När en projektbaserad offertrad innehåller radinformation är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet i offertradsinformationen. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Offererat belopp efter skatt | Fältet är offertradsbeloppet efter skatt och skrivskyddat. Beloppet i det här fältet beräknas som *Offererat belopp + moms*. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Undre gräns | Det här fältet är redigerbart och är endast tillgängligt på projektbaserade offertrader som har faktureringsmetoden **Tid och material**. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |
| Kundbudget | Det här fältet är redigerbart och kopieras från motsvarande fält på affärsmöjlighetsraden om offerten skapades från en affärsmöjlighet. | Värdet kopieras till projektkontraktraden som skapas från offertraden när offerten vanns. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Valideringsregler för fält under fliken Allmänt i projektbaserade offertrader

**Regel 1**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, tas ett projekt med i offertraden.

**Regel 2**: om fältet **Inkluderade uppgifter** är tomt, eller om det är inställt på **Alla projektuppgifter**, kan ett projekt och en viss transaktionsklass endast finnas på en projektbaserad offertrad för en offert.

**Regel 3**: om fältet **Inkluderade uppgifter** är inställt på **Endast valda projektuppgifter**, kan ett projekt och en viss transaktionsklass finnas på flera projektbaserade offertrader för en offert.

**Regel 4**: om en affärsmöjlighet har flera offerter kan det finnas offertrader från olika offerter som alla refererar till samma projekt och inkluderar samma transaktionsklass.

**Regel 5**: om offerterna inte tillhör samma affärsmöjlighet får de inte ha samma projekt- och transaktionsklass.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Affärsmöjlighet</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Offert</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Offertrad</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Inkluderade uppgifter</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Inkludera tid</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Ta med utgift</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Ta med material</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ta med</strong>
                </p>
                <p>
                    <strong>Avgift</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Giltigt/ogiltigt</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Orsak</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Överträdelse av regel 2. Tid, utgifter och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Inga </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Överträdelse av regel 2. Tid, material och avgifter på P1-projekt tas med på båda offertraderna, QL1 och QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Inga </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Tid, material och avgifter på P1-projekt tas med i QL1 <br>
Utgiften på P1-projektet ingår i QL2 <br>
Ingen överlappar vad som ingår på varje offertrad och därför är giltigt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Inga </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Inga </p>
            </td>
            <td width="41" valign="top">
                <p>
Inga </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Överträdelse av regel #2 </p>
                <p>
Q1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1 </p>
                <p>
QL2 omfattar tid, utgifter och avgifter för hela projektet P1 och därmed överlappar vad som ingår i Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tom </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per regel #3, </p>
                <p>
Q1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.
                </p>
                <p>
QL2 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.
                </p>
                <p>
Den enda ytterligare valideringen är runt deluppsättningen av uppgifter på QL1, som skiljer sig från uppgiftsuppsättningen på QL2 för att säkerställa att ingen överlappar. Detta görs av systemet när uppgifter associeras.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Endast valda uppgifter </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alla projektuppgifter eller tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per regel #5, Q1 och Q2 är två offerter på samma möjlighet, så de kan båda uppskatta för samma delar av ett projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alla projektuppgifter eller tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alla projektuppgifter eller tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per regel #4, Q1 och Q2 är två offerter på olika möjligheter, så de kan båda uppskatta för samma delar av samma projekt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alla projektuppgifter eller tomt </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
