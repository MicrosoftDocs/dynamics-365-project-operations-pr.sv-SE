---
title: Beräkna en projektbaserad kontraktrad
description: I det här ämnet finns information om beräkningar om att arbeta med en projektbaserad kontraktrad.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180484"
---
# <a name="estimate-a-projectbased-contract-line"></a>Beräkna en projektbaserad kontraktrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_ 

I Dynamics 365 Project Operations innehåller en projektrelaterad kontraktradinformation som hjälper till att beräkna kostnaden och potentiella intäkter för det arbete som är ägnat att leverera kontraktraden.

Om du vill beräkna en projektrelaterad kontraktrad går du till fliken **kontraktradsinformation** på den projektbaserade **kontraktraden**.  Det finns två sätt att skapa en uppskattning på en projektbaserad kontraktsrad:

   - Skapa en uppskattning direkt på kontraktraden genom att lägga till kontraktraddetaljer manuellt.
   - Skapa ett projekt och en projektplan och koppla sedan projektet och aktiviteterna till projektets kontraktrad. Detta aktiverar processen genom vilken du kan importera uppskattningen av projektplanen till kontraktraden utifrån komponenterna som ingår i kontraktraden.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Skapa ett uppskattning direkt för en projektbaserad kontraktrad

1. Gå till kontraktraden och välj fliken **kontraktradinformation**. Raderna som du skapar på den här fliken sammanfattas och visas som det **kontrakterade värdet** för den här **kontraktraden**. 
2. I underrutnätet **kontraktradinformation**, välj **+ Ny kontraktraddetalj**. Ett skjutreglage för snabbregistrering öppnas. Följande fält är tillgängliga i formuläret **information om kontraktrad**:

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Beskrivning** | **Snabbregistrering** | En beskrivning av den specifika uppskattningen. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Transaktionsklass** | **Snabbregistrering** | Denna listrutan är en lista över transaktionsklasser som finns på fliken **Allmänt** i den projektbaserade kontraktraden. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Roll** | **Snabbregistrering** | Rollen för personen som utför det här arbetet eller ådrar sig utgiften. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Kategori** | **Snabbregistrering** | Kategorin för arbetet eller kostnaden. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Startdatum** | **Snabbregistrering** | Startdatumet för arbetet. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Slutdatum** | **Snabbregistrering** | Slutdatumet för arbetet. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Resursföretag** | **Snabbregistrering** | Det resursföretag eller den juridiska personen som ådrar sig kostnaden och som tillhandahåller resursen att arbeta med den. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. Fältet används också för att hämta självkostnad. |
| **Resursenhet** | **Snabbregistrering** | Den omlokaliseringsenhet som ådrar sig kostnaden och visar att resursen fungerar. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. Fältet används också för att hämta självkostnad. |
| **Enhetsschema** | **Snabbregistrering** | Enhetsgruppen för arbete eller utgift. Enheter tillhör ett enhetsschema eller en grupp enheter. T.ex. *mil* och *kilometer (km)* är enheter som tillhör en gruppenheter som beskriver avståndet. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Enhet** | **Snabbregistrering** | Enheten för arbete eller utgift. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Antal** | **Snabbregistrering** | Kvantiteten för arbete eller utgift. | Det här fältet används som standard för den relaterade kontraktradinformationen för kostnader som skapas automatiskt. |
| **Enhetspris** | **Snabbregistrering** | Faktureringskursen för den roll som utför arbetet eller försäljningspriset för utgiftskategorin. Det här fältet används för **Tid** utifrån kombinationen av roll och resursenhet på projektprislistan som gäller för startdatumet. För utgifter är fältets standardvärde från prisinställningen för transaktionskategorin i den projekt prislista som gäller startdatum. Om prissättningsmodellen för transaktionskategorin inte är **pris per enhet**, finns det inget standardvärde och fältet lämnas tomt. | Kostnadstaxa för den roll som utför arbetet eller kostnaden per enhet för utgiftskategorin. Det här fältet används som standard för **Tid baserat på rollen** och resursenhetskombinationen på rollprislistan för den kostnadsprislista som bifogas den upphandlande enheten som gäller för startdatumet. För utgifter baseras detta fältets standard på kategoriprisraden i kostnadsprislistan som är bifogad till den upphandlande enheten som träder i kraft för startdatumet. Om prissättningsmodellen för transaktionskategorin inte är pris per enhet, finns det inget standardvärde och fältet lämnas tomt. |
| **Beräknad skatt** | **Snabbregistrering** | Den uppskattade momsen för det här arbetet eller den här kostnaden som indata av användaren. | Den uppskattade momsen för det här arbetet eller den här kostnaden som indata av användaren. |
| **Belopp** | **Snabbregistrering** | Värdet i det här fältet kan läggas till av användaren om fälten **Kvantitet** och **Pris** lämnas tomma. Om **kvantitet** och **pris** är ifyllda är fältet **belopp** skrivskyddat och beräknas som **(kvantitet \* per enhet) och moms**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Uppdatera priser på kontraktradinformation

Om du ändrar priser på den projektprislista som är bifogad till kontraktet eller den upphandlande enhetens kostnadslista, kan du uppdatera priserna på den enskilda kontraktradinformation för att återspegla ändringen. På sidan **Kontrakt**, välj **Omberäkna**. En varning öppnas för att meddela att priserna för alla kontraktrader i det här kontraktet har återställts. Välj **Ja** du vill uppdatera priser för information om kontraktradinformation för både försäljning och kostnad.

## <a name="access-contract-line-details-for-cost"></a>Åtkomst till kontraktradinformation för kostnad

På fliken **kontraktradinformation** markerar du en rad i rutnätet om du vill visa åtgärder i verktygsfältet i underrutnätet. Den första åtgärden i verktygsfältet för under rutnätet är **öppen kostnadsdetalj**. Välj om du vill se den relaterade kostnadsnivån och beloppet för denna detalj i detalj **öppna kostnadsdetalj**. 

> [!NOTE]
> Ändra resursföretag, resursenhet, kvantitet, datum, roll eller kategorivärden på kontraktradinformation för **Kostnad** ändrar också motsvarande värden på kontraktradinformation för **Försäljning**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta på kontraktradinformation för kostnad och försäljning

Kontraktradinformation för **försäljning** anger standardvalutan från den projektprislista som gäller för startdatumet för kontraktradinformationen.

Kontraktradinformation för **Kostnad** anger standardvalutan från prislista av den upphandlande enheten i kontraktet som träder i kraft för startdatumet för kontraktradinformation för **Kostnad**.

Vid beräkningen av lönsamhet konverteras beloppen för kontraktradinformation för **kostnad** och **försäljning** i miljöns basvaluta för att det ska gå att rapportera de totala faktiska och uppskattade marginalerna i kontraktet.

> [!NOTE]
> Fel i valutaavrundning och ändrade marginaler kan uppstå på grund av att valutakurserna inte fungerar på ett effektivt datum. Använd de här beräkningarna i projektkontrakt endast som uppskattningar och inte för verklig lagstadgad eller annan rapportering som kräver högre precision för avrundning och datumeffektivitet för växelkurser.


[!INCLUDE[footer-include](../includes/footer-banner.md)]