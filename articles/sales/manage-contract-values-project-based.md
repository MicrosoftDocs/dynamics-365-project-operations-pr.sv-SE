---
title: Arbeta med projektbaserade kontraktrader
description: I det här ämnet finns information om projektbaserade kontraktrader.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990068"
---
# <a name="work-with-projectbased-contract-lines"></a>Arbeta med projektbaserade kontraktrader

Projektbaserade kontraktrader i Dynamics 365 Project Operations är utformade för att rymma uppskattningar och faktureringsavtal för specifika komponenter i projektarbetet med ett åtagande. Strukturen på en projektbaserad kontraktrad utökas för projektuppskattningar och faktureringsscenarier med följande koncept:

- Faktureringsmetod
- Mappning av projekt och uppgifter
- Inkluderade transaktionsklasser
- Undre gräns
- Debiterbar inställning
- Uppskattningar med hjälp av kontraktradsdetaljer
- Kontraktradens kund

Följande fält finns på fliken **Allmänt** i projektbaserade kontraktrader. Med hjälp av dessa fält kan du ställa in grunden för en detaljerad grundläggande uppskattning och faktureringsordning för projektbaserat arbete.

| Fält | Beskrivning | Inverkan nedströms |
| --- | --- | --- |
| **Namn** | Namnet på den kontraktrad som identifierar den diskreta komponenten för det kontrakt som uppskattas. För ett projektkontrakt som har skapats utifrån en offert kopieras värdet från ett motsvarande värde på den projektbaserade offertraden. | Fältvärdet kopieras till projektfakturaraden som skapas från den här kontraktraden när fakturan skapas. |
| **Faktureringsmetod** | I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden. Det här är ett alternativuppsättning som representerar de två huvudsakliga upphandlingsmodellerna som stöds av Project Operations:</br>- **Fast pris**</br>- **Tid och material** | Den faktiska transaktionen bearbetas i enlighet med faktureringsmetoden för den refererade kontraktraden. Om den kontraktrad som har refererats av det faktiska värdet har en metod och en metod för materialfakturering skapas en kostnad och en faktisk fakturerad försäljningspost. Om kontraktraden som refereras av det faktiska värdet har en faktureringsmetod med fast pris skapas endast en verklig kostnad. |
| **Project** | Använd det här fältet om du vill identifiera det projekt som ska användas för att leverera arbetet i det här åtagandet. | Värdet i det här fältet används tillsammans med fälten **inkluderade uppgifter** och **inkluderade transaktionsklasser** för att lösa kontraktradreferensen på en post för en faktisk post eller en post för beräkningsrader. |
| **Inkludera tid** | En flagga anger om tidstransaktioner eller arbetskostnader för det valda projektet ingår på den här kontraktraden. Ett **Nej**-värde anger att tidstransaktionerna och arbetskraftskostnaderna inte ska tas med på den här kontraktraden. Ett **Ja**-värde anger att de ska vara. | Fältvärdet används tillsammans med projekt för att lösa en kontraktradsreferens på en faktisk post eller en post för beräkningsrad. |
| **Ta med utgift** | En flagga anger om utgiftskostnader för det valda projektet kommer att ingå i den här kontraktraden. Ett **Nej**-värde anger att utgiftskostnaden inte ska tas med på den här kontraktraden. Ett **Ja**-värde anger att det ska vara. | Fältvärdet används tillsammans med projekt för att lösa en kontraktradsreferens på en faktisk post eller en post för beräkningsrad. |
| **Inkludera avgift** | En flagga anger om avgifter för det valda projektet kommer att ingå i den här kontraktraden. Ett **Nej**-värde anger att avgifter inte ska tas med på den här kontraktraden. Ett **Ja**-värde anger att de ska vara. | Fältvärdet används tillsammans med projekt för att lösa en kontraktradsreferens på en faktisk post eller en post för beräkningsrad. |
| **Avtalat belopp** | På en kontraktrad med fast pris är det överenskommet värde som ska faktureras kunden för alla arbetskomponenter som är associerade med den här kontraktraden. På en kontraktrad för tid och material är detta belopp ett beräknat värde av det som ska faktureras kunden för alla arbetskomponenter som är associerade till den här kontraktraden. I ett projektkontrakt som har skapats utifrån en offert kopieras värdet från motsvarande fält på offertraden. När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån beloppet på kontraktraddetaljer. | När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra beloppen i radinformationen. På en kontraktrad med fast pris används det här värdet för att generera beloppet före skatt på periodiska faktureringsmilstolpar. |
| **Beräknad skatt** | Användaren kan redigera fältet och ange det uppskattade momsbeloppet på kontraktraden. När en projektbaserad kontraktrad innehåller raddetaljer är det här fältet låst för redigering och sammanfattas utifrån momsbeloppet på kontraktraddetaljer. | När kontraktraden innehåller raddetaljer kan det här värdet ändras genom att ändra momsbeloppen i radinformationen. På en kontraktrad med fast pris används det här värdet för att generera skatt på periodiska faktureringsmilstolpar. |
| **Kontrakterat belopp efter skatt** | Beloppet på kontraktraden efter skatt. Fältet är skrivskyddat och beräknas som **kontrakterat belopp + moms**. | På en kontraktrad med fast pris används det här värdet för att generera periodiska faktureringsmilstolpar. |
| **Undre gräns** | Användaren kan redigera det här fältet och det är endast tillgängligt på projektbaserade kontraktrader som har en metod för fakturering av tid och material. | Användaren kan redigera det här fältet. När en tid eller kostnad faktiskt refererar till den här kontraktraden för tid och material, utvärderas det faktiska beloppet mot gränsen för undre gräns för den här kontraktraden efter redovisning för redan förbrukade och bekräftade belopp. |
| **Kundbudget** | Det här fältet kan redigeras och kopieras från motsvarande fält på offertraden om kontraktet skapades från en offert. | Det här fältet används endast för information och har inte någon efterföljande betydelse. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Valideringsregel för alternativen på fliken Allmänt i projektbaserade kontraktrader

Regel: ett projekt och en viss transaktionsklass kan endast tas med på en projektbaserade kontraktrad i ett kontrakt.

| Kontrakt | Kontraktrad | Project | Inkludera tid | Ta med utgift | Inkludera avgift | Giltigt/ogiltigt | Anledning                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ogiltigt       | Bryter mot regeln. Tid, utgifter och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.                                                                                       |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ogiltigt       | Bryter mot regeln. Tid, utgifter och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.                                                                                       |
| C1       | CL1           | P1      | Ja          | Inga              | Ja         | Ogiltigt       | Bryter mot regeln. Tid och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.                                                                                                   |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ogiltigt       | Bryter mot regeln. Tid och avgifter i projekt P1 tas med på både kontraktrader, CL1 och CL2.                                                                                                   |
| C1       | CL1           | P1      | Ja          | Inga              | Ja         | Giltig           | Tid och avgifter för projekt P1 ingår på CL1. Utgiften på P1-projektet ingår i CL2. </br>   Det finns ingen överlappning i vad som ska tas med på varje kontraktrad och är därför giltigt.  |
| C1       | CL2           | P1      | Inga           | Ja             | Inga          | Giltig           | Tid och avgifter för projekt P1 ingår på CL1. Utgiften på P1-projektet ingår i CL2. </br>   Det finns ingen överlappning i vad som ska tas med på varje kontraktrad och är därför giltigt.  |
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ogiltigt       | Bryter mot regeln. Tid, utgifter och avgifter i projekt P1 tas med på raderna på de två kontrakten.                                                                                               |
| CL2      | CL2           | P1      | Ja          | Ja             | Ja         | Ogiltigt       | Bryter mot regeln. Tid, utgifter och avgifter i projekt P1 tas med på raderna på de två kontrakten.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]