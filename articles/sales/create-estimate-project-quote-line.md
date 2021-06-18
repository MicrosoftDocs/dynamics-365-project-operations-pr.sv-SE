---
title: Beräkna en projektoffertrad
description: Det här ämnet ger information om hur man skapar en uppskattning på en projektoffertrad.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: adb5a7f113b15abd2fe7364fa9b592d2c02db389
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000728"
---
# <a name="estimate-a-project-quote-line"></a>Beräkna en projektoffertrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En projektbaserad offertrad innehåller information som hjälper dig att beräkna kostnaden och potentiella intäkter för det arbete som är ägnat på att leverera offertraden.

För att uppskatta en projektbaserad offertrad, välj fliken på offertraden **Information om offertrad**. Det finns två sätt att skapa en uppskattning på en projektbaserad offertrad:

   - Skapa uppskattningen manuellt direkt på offertraden med hjälp av offertradsinformationen. 
   - Skapa ett projekt och en projektplan och koppla sedan projektet och uppgifterna till offertraden. Processen för att importera uppskattningarna i projektplanen till offertraden utifrån den information du har angett kommer att aktiveras.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Skapa uppskattningar direkt på en projektbaserad offertrad

För att skapa beräkningar direkt från en projektbaserad offertrad, följ dessa steg:

1. Om du vill skapa en uppskattning på en projektrelaterad offertrad väljer du fliken **Offertradsinformation**. Radartikeln som du skapar på den här fliken sammanfattar det offererade värdet för den här offertraden. 
2. Om du vill skapa en offertradsinformation markerar du **Ny offertradinformation** i under **rutnätet med information om offertrader**. Ett skjutreglage för snabbskapande öppnas. Följande fält på sidan **Offertrad**.

| **Fält** | **Plats** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Beskrivning | Snabbregistrering | En beskrivning av den specifika uppskattningen. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Transaktionsklass | Snabbregistrering | I den här listrutan visas de transaktionsklasser som finns under fliken **Allmänt** i den projektbaserade offertraden.  | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Välj produkt | Snabbregistrering | Tillämpas när transaktionsklassen är **Material**. Du kan välja att ange att beräkningsraden är för en **Befintlig** (katalog) produkt eller en **Ej registrerad** produkt. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Produkt | Snabbregistrering | ID för produkten från produktkatalogen. Det här fältet är endast aktiverat när du väljer **Befintlig** i fältet **Välj produkt**. ID används för att hämta försäljningspriset från projektprislistan i offerten. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Oregistrerad produkt | Snabbregistrering | En textruta som oregistrerad ska ange produktnamnet. Det här fältet är endast aktiverat när du väljer **Oregistrerad** i fältet **Välj produkt**.| Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Roll | Snabbregistrering | Rollen som den person som ska utföra arbetet eller ådrar sig denna kostnad. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Kategori | Snabbregistrering | Kategorin för arbetet eller kostnaden. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Startdatum | Snabbregistrering | Startdatumet för arbetet. | Det här fältet är som standard den offertraddetaljen för kostnad som skapas automatiskt. |
| Slutdatum | Snabbregistrering | Slutdatumet för arbetet. | Det här fältet är som standard den offertraddetaljen för kostnad som skapas automatiskt. |
| Resursföretag | Snabbregistrering | Det företag eller juridisk enhet som tar på sig kostnaden och som tillhandahåller resursen för att arbeta med den. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt och används i hämtning av självkostnad. |
| Resursenhet | Snabbregistrering | Den enhet som tar på sig kostnaden och som tillhandahåller resursen för att arbeta med den. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt och används i hämtning av självkostnad. |
| Enhetsschema | Snabbregistrering | Enhetsgruppen för arbetet, produkten eller utgifter. Enheter tillhör ett enhetsschema eller en grupp enheter. T.ex. mil och kilometer är enheter som tillhör en gruppenheter som beskriver avståndet. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Enhet | Snabbregistrering | Arbetsenhet, produkten eller utgifter. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Antal | Snabbregistrering | Mängd arbete, produkten eller utgifter. | Det här värdet är som standard den relaterade offertraddetaljen för kostnad som skapas automatiskt. |
| Enhetspris | Snabbregistrering |Faktureringskursen för den roll som utför arbetet, enhetspriset för produkten eller försäljningspriset för produkten eller utgiftskategorin. Standard för **Tid** baserat på kombinationen av värden för prissättningsdimension på rollprisraden i projektprislistan som gäller för startdatumet. För **utgifter** är standardvärdet från prisinställningen för transaktionskategorin i den projekt prislista som gäller startdatum. Om prissättningsmodellen för transaktionskategorin inte är pris per enhet, finns det inget standardvärde och fältet lämnas tomt. För produkter baseras fältets standard på raden **Prislisteobjekt** i projektprislistan som gäller för startdatumet.| Kostnadstaxan för den roll som utför arbetet, eller kostnaden per enhet i kostnadskategorin eller enhetskostnaden för produkten. Standard för **Tid** baserat på kombinationen av värden för prissättningsdimension på prislista för självkostnad som bifogas den upphandlande enheten som gäller för startdatumet. För utgifter är standardvärdet baseras på kategoriprisraden i den kostnadsprislista som är bifogad till den upphandlande enheten som träder i kraft för startdatumet. Om prismodellen för transaktionskategorin inte är pris per enhet finns det ingen standardmodell och fältet lämnas tomt. För produkter baseras fältets standard på raden **Prislisteobjekt** i kostnadsprislistan som är bifogad den upphandlande enheten som träder i kraft för startdatumet.|
| Beräknad skatt | Snabbregistrering | Du kan ange den uppskattade momsen manuellt för det här arbetet eller den här utgiften. | Det här fältet har ingen inverkan nedströms. |
| Belopp | Snabbregistrering | Du kan ange information manuellt i det här fältet om fälten **Antal** och **Pris** lämnas tomma. Om de här fälten inte är tomma blir fältet skrivskyddat och beräknas som (Antal \* Styckpris) + moms. | Det här fältet har ingen inverkan nedströms. |

## <a name="update-prices-on-quote-line-details"></a>Uppdatera priser i offertradsinformation

Om du har ändrat priser i den projektprislista som är bifogad till offerten, eller i en prislista för självkostnad för den avtalande enheten, kan du välja **Omberäkna** på sidan **Offert** för att uppdatera priserna i den enskilda offertradsinformationen så att den avspeglar ändringen. När du väljer **Omberäkna** visas en varning om att priserna på offertradsinformationen för alla offertrader i offerten kommer att återställas. Välj **Ja** om du vill uppdatera priserna i offertradsinformationen för både försäljning och kostnad.

## <a name="access-quote-line-details-for-cost"></a>Visa offertradsinformation för kostnad

Kom åt offertradsinformation för kostnad genom att följa stegen nedan.

1. På fliken **Information om offertrad**, välj en rad i rutnätet för att möjliggöra åtgärder i underrutnätets verktygsfält. 
2. Välj **Öppna kostnadsinformation** om du vill se den relaterade kostnadstaxan och beloppet för den här offertraden.

> [!NOTE]
> Om du ändrar resursenhet, antal, datum, roll eller kategori i offertradsinformationen för kostnad, ändras motsvarande värden i offertradsinformationen för försäljning.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta i offertradsinformation för kostnad och försäljning

Valuta i offertradsdetaljen för försäljningsstandarder från projektprislistan som är effektiv för offertradsdetaljens startdatum.

Valutan på offertraddetaljen för kostnadsinställningar från prislistan för den upphandlande enheten för offerten som träder i kraft för startdatumet för offertraddetaljen för kostnad.

> [!NOTE]
> Vid beräkningen av lönsamhet konverteras beloppet i offertradsinformationen för kostnad och försäljning till miljöns basvaluta för att rapportera den uppskattade övergripande marginalen för offerten. Fel i valutaavrundning och ändrade marginaler kan uppstå på grund av att valutakurserna inte fungerar på ett effektivt datum. Använd endast dessa beräkningar i projektofferter eftersom de inte är för faktiska lagstadgade eller andra rapporter som kräver högre precision för avrundning och medvetenheten om datumrelativitet för växelkurser.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
