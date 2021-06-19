---
title: Projektbaserade kontraktrader – Översikt
description: I det här ämnet finns information om att arbeta med projektbaserade kontraktrader.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003158"
---
# <a name="project-based-contract-lines-overview"></a>Projektbaserade kontraktrader – Översikt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektbaserade kontraktrader i Dynamics 365 Project Operations är utformade för att rymma uppskattningar och faktureringsavtal för specifika komponenter i projektarbetet med ett åtagande. Strukturen på en projektbaserad kontraktrad utökas för projektuppskattningar och faktureringsscenarier med följande koncept:

- Faktureringsmetod
- Mappning av projekt och uppgifter
- Inkluderade transaktionsklasser
- Undre gräns
- Debiterbar inställning
- Uppskattningar med hjälp av kontraktradsdetaljer
- Kontraktradens kund

Följande tabell innehåller fälten på fliken **Allmänt** i projektbaserade kontraktrader som hjälper dig att ställa in grunden för en detaljerad uppskattning och faktureringsordning för projektbaserade arbeten.

| Fält | Beskrivning | Inverkan nedströms |
| --- | --- | --- |
| **Namn** | Namn på kontraktraden. Detta identifierar den diskreta komponenten för det kontrakt som uppskattas. För ett projektkontrakt som har skapats utifrån en offert kopieras värdet från ett motsvarande värde på den projektbaserade offertraden. | Namnet kopieras till projektfakturaraden som skapas från den här kontraktraden när fakturan skapas. |
| **Faktureringsmetod** | I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden. Det här är ett alternativuppsättning som representerar de två huvudsakliga upphandlingsmodellerna som stöds av Project Operations:</br>- **Fast pris**</br>- **Tid och material** | Den faktiska transaktionen bearbetas i enlighet med faktureringsmetoden för den refererade kontraktraden. Om den kontraktrad som har refererats av det faktiska värdet har en metod och en metod för materialfakturering skapas en kostnad och en faktisk fakturerad försäljningspost. Om kontraktraden som refereras av det faktiska värdet har en faktureringsmetod med fast pris skapas endast en verklig kostnad. |
| **Project** | Använd det här fältet om du vill identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet. | Detta värde kommer att användas tillsammans med **Uppgifter som ingår** och **Inkluderade transaktionsklasser** för att lösa kontraktsreferensen på en faktisk eller uppskattad radpost. |
| **Uppgifter som ingår** | Anger om den här kontraktraden omfattar alla projektuppgifter för det valda projektet eller endast en del av uppgifterna. Detta är en alternativuppsättning som har följande möjliga värden:</br>- **Alla projektuppgifter**</br>- **Endast valda projektuppgifter**. Ett tomt värde i det här fältet är lika med att markera **alla projektuppgifter**. | Om **endast valda uppgifter** är markerade kan du välja specifika uppgifter och associera dem till den här kontraktraden på fliken **Faktureringsinställningar för uppgift** på sidan **projekt**. Detta värde används tillsammans med **projekt** och **inkluderade transaktionsklasser** för att lösa kontraktradreferensen på en post för en faktisk post eller en post för beräkningsrader. |
| **Inkludera tid** | Ett värde **Ja**/**Nej** anger om tidstransaktioner eller arbetskostnader för det valda projektet kommer att tas med på denna kontraktrad. Ett **Nej**-värde anger att tidstransaktionerna och arbetskraftskostnaderna inte ska tas med på den här kontraktraden. Ett **Ja**-värde anger att de ska vara. | Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost. |
| **Ta med utgift** | Ett värde **Ja**/**Nej** anger om utgiftskostnader för det valda projektet kommer att tas med på denna kontraktrad. Ett **Nej**-värde anger att utgiftskostnaden inte ska tas med på den här kontraktraden. Ett **Ja**-värde anger att det ska vara. | Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost. |
| **Ta med material** | Ett värde **Ja**/**Nej** anger om materialkostnader för det valda projektet kommer att tas med på denna kontraktrad. Ett värde för **Nej** indikerar att materialkostnaderna inte kommer att inkluderas i på kontraktraden. Ett **Ja**-värde anger att det ska vara. | Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost. |
| **Inkludera avgift** | Ett värde **Ja**/**Nej** anger om avgifter för det valda projektet kommer att tas med på denna kontraktrad. Ett **Nej**-värde anger att avgifter inte ska tas med på den här kontraktraden. Ett **Ja**-värde anger att de ska vara. | Det här värdet används tillsammans med projektet för att matcha referensen till kontraktraden på en faktisk post eller en beräkningsradspost. |
| **Avtalat belopp** | På en kontraktrad med fast pris är detta belopp det överenskommet värde som ska faktureras kunden för alla arbetskomponenter som är associerade till den här kontraktraden. På en kontraktrad för tid och material är detta belopp ett beräknat värde av det som ska faktureras kunden för alla arbetskomponenter som är associerade till den här kontraktraden. I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden. När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån beloppet på kontraktraddetaljer. | När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra beloppen i radinformationen. På en kontraktrad med fast pris används det här värdet för att generera beloppet före skatt på periodiska faktureringsmilstolpar. |
| **Beräknad skatt** | Användaren kan redigera fältet och ange det uppskattade momsbeloppet på kontraktraden. När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet på kontraktraddetaljer. | När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra momsbeloppen i radinformationen. På en kontraktrad med fast pris används det här värdet för att generera skatt på periodiska faktureringsmilstolpar. |
| **Kontrakterat belopp efter skatt** | Beloppet på kontraktraden efter skatt. Fältet är skrivskyddat och beräknas som **kontrakterat belopp + moms**. | På en kontraktrad med fast pris används det här värdet för att generera periodiska faktureringsmilstolpar. |
| **Undre gräns** | Användaren kan redigera det här fältet och det är endast tillgängligt på projektbaserade kontraktrader som har en metod för fakturering av tid och material. | Användaren kan redigera det här fältet. När ett faktiskt värde för tid och material refererar den här kontraktraden för tid och material, utvärderas det faktiska beloppet mot gränsen för undre gräns för den här kontraktraden. Utvärderingen slutförs efter att redan förbrukade och bekräftade belopp redovisas. |
| **Kundbudget** | Det här fältet kan redigeras och kopieras från motsvarande fält på offertraden om kontraktet skapades från en offert. | Det här fältet används endast för information och har inte någon efterföljande betydelse. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Valideringsregler för alternativen på fliken Allmänt i projektbaserade kontraktrader

Regel 1: Om **inkluderade uppgifter** är tomt eller har värdet **alla projekt aktiviteter**, tas alla projekt aktiviteter med på kontraktraden.

Regel 2: När fältet **inkluderade uppgifter** är tomt eller uttryckligen anges som **alla projekt aktiviteter**, kan ett projekt och en viss transaktionsklass endast tas med på en projektbaserad kontraktrad för ett kontrakt.

Regel 3: När fältet **inkluderade uppgifter** anges till **Endast valda projektuppgifter** kan ett projekt och en viss transaktionsklass inkluderas på flera projektbaserade kontraktsrader i ett kontrakt.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Kontrakt</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Kontraktrad</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Inkluderade uppgifter</strong>
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
                    <strong>Ta med material</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Ta med</strong>
                </p>
                <p>
                    <strong>Avgift</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Giltigt/ogiltigt</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Orsak</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Överträdelse av regel 2. Tid, utgifter, material och avgifter på P1-projekt tas med på båda kontraktraderna, CL1 och CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Överträdelse av regel 2. Tid, material och avgifter på P1-projekt tas med på båda kontraktraderna, CL1 och CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Tid, material och avgifter på P1-projekt tas med i CL1.
                </p>
                <ul>
                    <li>
Utgiften på P1-projektet ingår i CL2.
                    </li>
                </ul>
                <p>
Ingen överlappar vad som ingår på varje kontraktrad och därför är giltigt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Inga </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Endast valda uppgifter </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ogiltigt </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Överträdelse av regel #2 </p>
                <p>
C1 inkluderar tid, material, utgifter och avgifter för en delmängd av uppgifter i projekt P1.
                </p>
                <p>
CL2 omfattar tid, material, utgifter och avgifter för hela projektet P1 och därmed överlappar vad som ingår i C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tom </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Endast valda uppgifter </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Giltig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Per regel #3 </p>
                <p>
C1 inkluderar tid, utgifter, material och avgifter för en delmängd av uppgifter i projekt P1.
                </p>
                <p>
CL2 inkluderar tid, utgifter, material och avgifter för en delmängd av uppgifter i projekt P1.
                </p>
                <p>
Den enda ytterligare valideringen är runt deluppsättningen av uppgifter på CL1, som skiljer sig från uppgiftsuppsättningen på CL2 för att säkerställa att ingen överlappar. Detta görs av systemet när uppgifter associeras.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Endast valda uppgifter </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
