---
title: Inställningar för projektkontrakt
description: I det här ämnet finns information om de fält som påverkar kontraktrader och information om kontraktet som summeras mot alla radposterna.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c11d6e76b551e0d2cde8ff514d1a0ddd989d07b9
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088130"
---
# <a name="project-contract-settings"></a>Inställningar för projektkontrakt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I det här ämne finns information om fält som gäller hela projektkontraktet, inklusive inställningar som påverkar alla kontraktrader. Information om kontraktet som sammanfattas över alla radartiklar köra nyckelvärden i projektkontraktet ingår också.

I följande tabell visas fälten i ett projektkontrakt som är unika för Dynamics 365 Project Operations eller som har viktiga ändringar i beteendet från försäljningsorder i Dynamics 365 Sales.

| Fält | Plats | Relevans, syfte och vägledning | Inverkan nedströms |
| --- | --- | --- | --- |
| Type | Fliken **Sammanfattning** (dold) | Det här är en alternativuppsättning med följande alternativ:</br>- **Arbetsbaserad** (endast tillgängligt när Project Operations är installerat)</br>- **Artikelbaserad** (endast tillgänglig när Project Operations och Sales är installerat)</br>- **Serviceunderhåll-baserad** (tillgängligt när Dynamics 365 Field Service är installerat) | I Project Operations är värdet i det här fältet som standard **arbetsbaserat** och klassificerar kontraktet som ett projektbaserat kontrakt. Ett kontrakt ska vara projektbaserat för att alla projektspecifika tillägg och funktioner ska kunna aktiveras. |
| Ägande företag | Fliken **Sammanfattning** | Den juridiska person som ska redovisa de kostnader och intäkter som påförs från de projekt som är associerade med projektkontraktet. När ett kontrakt skapas från en offert kopieras fältet från motsvarande fält på offertposten. | Det ägande företaget är lika med begreppet juridisk person i modulen **Projektledning och redovisning** i Project Operations. Alla kostnader och intäkter som härrör från detta projekt redovisas i det ägande företagets huvudbok. |
| Kund | Fliken **Sammanfattning** | En referens till kundens företag eller kontopost. När ett kontrakt skapas från en offert kopieras fältet från motsvarande fält på offertposten. | Valutan i projektkontraktet används som standard utifrån kundens valuta. Valutan kan ändras innan kontraktet sparas. |
| Kontohanteraren | Fliken **Sammanfattning** | Namnet på kontoansvarig för denna affär. När ett kontrakt skapas från en offert kopieras fältet från motsvarande fält på offertposten. | Kontoansvarig är ansvarig för att hantera relationen med kunden genom att fullborda arbetet på projektet. På grundval av den bokningsbara resursposten som är kopplad till kontoansvarig hämtas den kontrakterande enheten från projektkontraktet. |
| Kontrakteringsenhet | Fliken **Sammanfattning** | Den organisationsenhet som är ansvarig för leveransen av projekten som är associerade med detta kontrakt. När ett kontrakt skapas från en offert kopieras fältet från motsvarande fält på offertposten. | Kontrakteringsenheten är den avdelning i företaget som utför projekten. Varje avtalande enhet har en valuta och valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under projektet. |
| Produktprislista | Fliken **Sammanfattning** | Den här prislistan används som standard för priserna på de produktbaserade kontraktraderna. I listan med listrutealternativ för det här fältet visas en lista med prislistor där prislistans valuta stämmer överens med valutan i kontraktet. När ett kontrakt skapas från en offert kopieras fältet från motsvarande fält på offertposten. I projektkontraktet hämtas detta fält som standard från kontoposten men kan ändras. | Det finns ingen relevans nedströms för det här fältet. |
| Valuta | Fliken **Sammanfattning** | Valutan som används för att rapportera värdet av detta avtal och valutan som kunden ska faktureras i. När ett kontrakt skapas från en offert kopieras fältet från motsvarande fält på offertposten. I projektkontraktet hämtas detta fält som standard från kontoposten men kan ändras. | När ett kontrakt har sparats går det inte längre att redigera det här fältet. Detta fält används för att standardisera produkt- och projektprislistorna i kontraktet. Valutan i kontraktet används för att matcha valutan i prislistan. |
| Undre gräns | Fliken **Sammanfattning** | Detta fält anger det förhandlade taket på det slutgiltiga värde som kunden har accepterat för denna affär. | Taket utvärderas under utförande och är tillämplig för alla radartiklar och projekt som är kopplade till denna affär. |
| Begärt leveransdatum | Fliken **Sammanfattning** | När ett kontrakt skapas från en projektoffert kopieras fältet från motsvarande fält på projektofferten. | Detta datum används som slutdatum för generering av fakturascheman. |

Följande nyckelvärden är tillgängliga under fliken **Kontraktprestanda** i ett projektkontrakt.

| Fält | Plats | Relevans, syfte och vägledning |
| --- | --- | --- |
| Kontraktsvärde | Övergripande kontrakt | Det totala värdet för projektkontraktet. |
| Fakturerat belopp | Övergripande kontrakt | Summan av beloppen på alla fakturor för det här kontraktet. |
| Upparbetade kostnader | Övergripande kontrakt | Summan av alla verkliga kostnadsvärden som har loggats för alla projekt som är mappade till kontraktet. |
| Bruttomarginal | Övergripande kontrakt | Fakturerat belopp – kostnad hittills/fakturerat belopp |
| Förväntad marginal | Övergripande kontrakt | (Kontraktvärde – uppskattade kostnader)/kontraktvärde Uppskattade kostnader = summan av alla beräknade kostnader i alla projekt som är mappade till kontraktet.|
| Kontraktsvärde | Projektbaserade rader | Värdet för kontraktraden. |
| Fakturerat belopp | Projektbaserade rader | För kontraktrad med fast pris: Summan av beloppen i alla fakturerade faktiska värden för försäljningsmilstolpe mot den här kontraktraden på olika fakturor som skapats för det här kontraktet. För kontraktrad för tid och material: Summan av beloppen i alla debiterbara faktiska värden för försäljning mot den här kontraktraden på olika fakturor som skapats för det här kontraktet. |
| Upparbetade kostnader | Projektbaserade rader | Summan av alla faktiska kostnadsvärden som har loggats för alla projekt som är mappade till kontraktraden. |
| Bruttomarginal | Projektbaserade rader | (Fakturerat belopp – kostnad hittills)/fakturerat belopp |
| Förväntad marginal | Projektbaserade rader | (Kontraktradsbelopp i basvaluta – uppskattade kostnader för kontraktraden i basvalutan)/kontraktradsbeloppet i basvalutan |
| Upparbetade kostnader | Detaljerad information om en projektbaserad rad | Tid: Summan av beloppet för faktiska tidskostnader som loggats för den här rollen i projektet som är mappat till den här kontraktraden. Utgifter: Summan av beloppet för alla faktiska utgiftskostnader som loggats för den här kategorin i projektet som är mappat till den här kontraktraden. |
| Loggad kvantitet | Detaljerad information om en projektbaserad rad | Tid: Hela tiden för den faktiska tidskostnaden för en roll i projektet som är mappat till den här kontraktraden. Utgifter: Alla kvantiteter för den här utgiftskategorin i faktiska utgiftskostnader för det projekt som är mappat till den här kontraktraden. |
| Fakturerat belopp | Detaljerad information om en projektbaserad rad | För en kontraktrad med fast pris lämnas det här fältet tomt på detaljnivån och visas endast på kontraktradsnivån. För en kontraktrad för tid och material slutförs beräkningar på detaljnivån. I detaljerna visas summan av beloppet på alla de fakturerade intäktsraderna för den här kontraktraden som kan debiteras. |
| Fakturerad kvantitet | Detaljerad information om en projektbaserad rad | För en kontraktrad med fast pris lämnas det här fältet tomt på detaljnivån och visas endast på kontraktradsnivån. För en kontraktrad för tid och material slutförs beräkningar på detaljnivån för tid och utgifter. Tid: Summan av timmarna på alla de fakturerade intäktsraderna för den här rollen mot kontraktraden som kan debiteras. Utgifter: Alla kvantiteter för den här utgiftskategorin i faktiska utgiftskostnader för det projekt som är mappat till den här kontraktraden. |
| Kontraktsvärde | Produktbaserade rader | Värdet på kontraktraden för den här produktbaserade kontraktraden. |
| Fakturerat belopp | Produktbaserade rader | Summan av beloppen på alla fakturarader mot den här produktbaserade kontraktraden på olika fakturor som skapas för det här kontraktet. |
| Upparbetade kostnader | Produktbaserade rader | Summan av alla faktiska kostnadsvärden som har loggats för den produktbaserade kontraktraden. |
| Bruttomarginal | Projektbaserade rader | Fakturerat belopp – kostnad hittills/fakturerat belopp |
| Förväntad marginal | Produktbaserade rader | (Kontraktradsvärde – uppskattade kostnader för kontraktraden)/kontraktradsvärde |