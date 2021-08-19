---
title: Beräkna en projektkontraktrad
description: Detta ämne ger information om hur en projektkontraktrad ser ut.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ae2d96170348a00b58f1571b6c9b31af894c281bdfdfcb00f4e348b2705186c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986918"
---
# <a name="estimate-a-project-contract-line"></a>Beräkna en projektkontraktrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_ 

I Dynamics 365 Project Operations innehåller en projektrelaterad kontraktradinformation som hjälper till att beräkna kostnaden och potentiella intäkter för det arbete som är ägnat att leverera kontraktraden.

Om du vill beräkna en projektrelaterad kontraktrad går du till fliken **kontraktradsinformation** på den projektbaserade **kontraktraden**.  Det finns två sätt att skapa en uppskattning på en projektbaserad kontraktsrad:

   - Skapa en uppskattning direkt på kontraktraden genom att lägga till kontraktraddetaljer manuellt.
   - Skapa ett projekt och en projektplan och koppla sedan projektet och aktiviteterna till projektets kontraktrad. Detta aktiverar processen genom vilken du kan importera uppskattningen av projektplanen till kontraktraden utifrån komponenterna som ingår i kontraktraden.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Skapa beräkningar direkt från ett projekt på en kontraktrad

För att skapa beräkningar direkt från ett projekt på en kontraktrad, följ dessa steg:

1. Gå till kontraktraden och välj fliken **kontraktradinformation**. Raderna som du skapar på den här fliken sammanfattas och visas som det **kontrakterade värdet** för den här **kontraktraden**. 
2. I underrutnätet **kontraktradinformation**, välj **Ny kontraktraddetalj**. Ett skjutreglage för snabbregistrering öppnas. Följande fält är tillgängliga på sidan **Information om kontraktrad**.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Beskrivning** | **Snabbregistrering** | En beskrivning av den specifika uppskattningen. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Transaktionsklass** | **Snabbregistrering** | Den här listan med transaktionsklasser finns på fliken **Allmänt** projektbaserade kontraktraden. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Välj produkt** | **Snabbregistrering** | Tillämpas när transaktionsklassen är **Material**. Du kan välja att ange att beräkningsraden är för en **Befintlig** (katalog) produkt eller en **Ej registrerad** produkt. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Produkt** | **Snabbregistrering** | ID för produkten från produktkatalogen. Det här fältet är endast aktiverat när du väljer **Befintlig produkt** i fältet **Välj produkt**. ID används för att hämta försäljningspriset från projektprislistan i kontraktet. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Oregistrerad produkt** | **Snabbregistrering** | Ett textfält som ska ange produktnamnet. Det här fältet är endast aktiverat när du väljer **Oregistrerad** i fältet **Välj produkt**.| Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Roll** | **Snabbregistrering** | Rollen för personen som utför det här arbetet eller ådrar sig utgiften. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt.|
| **Kategori** | **Snabbregistrering** | Kategorin för arbetet eller kostnaden. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt.|
| **Startdatum** | **Snabbregistrering** | Startdatumet för arbetet. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Slutdatum** | **Snabbregistrering** | Slutdatumet för arbetet. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Resursföretag** | **Snabbregistrering** | Det företag eller juridisk enhet som tar på sig kostnaden och som tillhandahåller resursen för att arbeta med den. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt och används i hämtning av självkostnad. |
| **Resursenhet** | **Snabbregistrering** | Den enhet som tar på sig kostnaden och som tillhandahåller resursen för att arbeta med den. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt och används i hämtning av självkostnad. |
| **Enhetsschema** | **Snabbregistrering** | Enhetsgruppen för arbetet, produkten eller utgifter. Enheter tillhör ett enhetsschema eller en grupp enheter. T.ex. *mil* och *kilometer (km)* är enheter som tillhör en gruppenheter som beskriver avståndet. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Enhet** | **Snabbregistrering** | Arbetsenhet, produkten eller utgifter. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Antal** | **Snabbregistrering** | Mängd arbete, produkten eller utgifter. | Det här värdet är som standard den relaterade kontraktsdetaljen för kostnad som skapas automatiskt. |
| **Enhetspris** | **Snabbregistrering** | Faktureringskursen för den roll som utför arbetet, enhetspriset för produkten eller försäljningspriset för produkten eller utgiftskategorin. Standard för **Tid** baserat på kombinationen av värden för prissättningsdimension på rollprisraden i projektprislistan som gäller för startdatumet. För **utgifter** är standardvärdet för det här fältet från priskonfigurationen för transaktionskategorin i projektprislistan som är effektiv för startdatum. Om prissättningsmodellen för transaktionskategorin inte är **pris per enhet**, finns det inget standardvärde och fältet lämnas tomt. För produkter baseras fältets standard på raden **Prislisteobjekt** i projektprislistan som gäller för startdatumet.| Kostnadstaxan för den roll som utför arbetet, eller kostnaden per enhet i kostnadskategorin eller enhetskostnaden för produkten. Standard för **Tid** baserat på kombinationen av värden för prissättningsdimension på prislista för självkostnad som bifogas den upphandlande enheten som gäller för startdatumet. För **utgifter** är standardvärdet för det här fältet baseras på kategoriprisraden i den kostnadsprislista som är bifogad till den upphandlande enheten som träder i kraft för startdatumet. Om prissättningsmodellen för transaktionskategorin inte är pris per enhet, finns det inget standardvärde och fältet lämnas tomt. För produkter baseras fältets standard på raden **Prislisteobjekt** i kostnadsprislistan som är bifogad den upphandlande enheten som träder i kraft för startdatumet.|
| **Beräknad skatt** | **Snabbregistrering** | Den uppskattade momsen för det här arbetet eller den här kostnaden som indata av användaren. | &nbsp; |
| **Belopp** | **Snabbregistrering** | Värdet i det här fältet kan läggas till om fälten **Kvantitet** och **Pris** lämnas tomma. Om **Kvantitet** och **Pris** fylls i är fältet **Belopp** skrivskyddat och beräknas som **(Kvantitet \* Enhetspris) + Moms**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Uppdatera priser på kontraktradinformation

Om du ändrar priser på den projektprislista som är bifogad till kontraktet eller den upphandlande enhetens kostnadslista, kan du uppdatera priserna på den enskilda kontraktradinformation för att återspegla ändringen. På sidan **Kontrakt**, välj **Omberäkna**. En varning visas om att priserna för alla kontraktrader i det här kontraktet återställs. Välj **Ja** du vill uppdatera priser för information om kontraktradinformation för både försäljning och kostnad.

## <a name="access-contract-line-details-for-cost"></a>Åtkomst till kontraktradinformation för kostnad

På fliken **kontraktradinformation** markerar du en rad i rutnätet om du vill visa åtgärder i verktygsfältet i underrutnätet. Den första åtgärden i verktygsfältet för under rutnätet är **öppen kostnadsdetalj**. Välj om du vill se den relaterade kostnadsnivån och beloppet för denna detalj i detalj **öppna kostnadsdetalj**. 

> [!NOTE]
> Ändra resursföretag, resursenhet, kvantitet, datum, roll eller kategorivärden på kontraktradinformation för **Kostnad** ändrar också motsvarande värden på kontraktradinformation för **Försäljning**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta på kontraktradinformation för kostnad och försäljning

Kontraktradinformation för **försäljning** anger standardvalutan från den projektprislista som gäller för startdatumet för kontraktradinformationen.

Kontraktradinformation för **Kostnad** anger standardvalutan från prislista av den upphandlande enheten i kontraktet som träder i kraft för startdatumet för kontraktradinformation för **Kostnad**.

Vid beräkningen av lönsamhet konverteras beloppen för kontraktradinformation för **kostnad** och **försäljning** i miljöns basvaluta för att det ska gå att rapportera de totala faktiska och uppskattade marginalerna i kontraktet.

> [!NOTE]
> Fel i valutaavrundning och ändrade marginaler kan uppstå på grund av att valutakurserna inte fungerar på ett effektivt datum. Använd endast dessa beräkningar i projektkontrakt eftersom de inte är för faktiska lagstadgade eller andra rapporter som kräver högre precision för avrundning och medvetenheten om datumrelativitet för växelkurser.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
