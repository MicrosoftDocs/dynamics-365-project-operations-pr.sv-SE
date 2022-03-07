---
title: Offerter och offertrader
description: I det här ämnet finns information om offerter och offertrader.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 509bc089e69ec234ddfdecb789c2e446286da82b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129475"
---
# <a name="quotes-and-quote-lines"></a>Offerter och offertrader

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation finns två typer av offerter: projektofferter och försäljningsofferter. De två typerna skiljer sig på följande sätt:

- I en försäljningsoffert finns det bara ett rutnät för radartiklar. I en projektoffert finns det två rutnät för radobjekt: en för projektrader och en för produktrader.
- En försäljningsoffert stöder aktivering och revidering. En projektoffert stöder inte dessa processer.
- Du kan koppla flera order till en försäljningsoffert. Du kan bara bifoga ett projektkontrakt till en projektoffert.
- Du kan vinna en försäljningsoffert och behålla den relaterade affärsmöjligheten öppen. När en projektoffert har vunnits stängs den relaterade affärsmöjligheten.
- En försäljningsoffert innehåller inte några fält och begrepp som ingår i en projektoffert har fält. Fälten inkluderar **Kontrakteringsenhet**, **Kontoansvarig** och **Faktureringsadress, kontaktperson**.  
- Försäljningsofferter och projektofferter identifieras även av ett alternativbaserat fält med namnet **typ**. För en försäljningsoffert har det här fältet värdet **artikelbaserat**. För projektofferter används värdet **arbetsbaserad**.

Det här ämnet fokuserar på detaljerna i projektofferter.

En projektoffert i PSA kan ha flera radobjekt eller offertrader. En projektoffert har faktiskt två rutnät för radobjekt. Ett rutnät är för projektbaserade rader som möjliggör detaljerad uppskattningar. Det andra rutnätet är för produktbaserade rader som använder ett enkelt enhetspris och en mängd baserad metod.

- **Projektbaserade** – beloppet (offererat värde) bestäms när du har beräknat hur mycket arbete som krävs. Du kan beräkna arbetet på en hög nivå, eller så kan du uppskatta det direkt som raddetaljer under varje offertrad. Slutligen kan du beräkna arbete baserat på basuppskattningar med hjälp av ett projekt och en projektplan. Projektbaserade offertrader finns endast i projektbaserade offerter som skapas med hjälp av Project Service Automation. Den här typen av offertrad är en anpassad form av de inskrivna offertrader som är tillgängliga i Microsoft Dynamics 365 Sales.
- **Produktbaserad** – beloppet (offererat värde) bestäms utifrån antalet enheter som säljs och produktens enhetsförsäljningspris. Produkten på en produktbaserad rad kan komma från en produktkatalog i Sales, eller så kan den vara en produkt som du definierar. Den här typen av offertrad är också tillgänglig på projektbaserade offerter som skapas med hjälp av PSA.

Beloppet i en offert är total summan mellan de produktbaserade raderna och de projektbaserade raderna.

> [!NOTE]
> Offerter och offertrader krävs inte i PSA. Du kan starta projektprocessen med ett projektkontrakt (sålt projekt). Det krävs emellertid alltid en affärsmöjlighet, oavsett om du startar med en offert eller ett projektkontrakt.

## <a name="project-based-quote-lines"></a>Projektbaserade offertrader

En projektbaserad offertrad i PSA har följande faktureringsmetoder:

- Tid och material
- Fast pris

### <a name="time-and-material"></a>Tid och material

Faktureringsmetoden för tid och material bygger på förbrukning. När du väljer den här faktureringsmetoden faktureras kunden allteftersom projektet ådrar sig kostnader. Fakturor skapas på en datumbaserad periodisk frekvens. Under försäljningsprocessen ger det offererade värdet för en tids- och materialkomponent endast en uppskattning av den slutliga kostnaden till kunden. Säljaren förbinder sig inte att slutföra projektet till exakt det angivna värdet. Tids- och materialkomponenter ökar kundens risker. Kunderna kanske vill förhandla om ytterligare klausuler som inte får överskridas för att minska riskerna. PSA stöder inte inställning av klausuler som inte får överskridas.

### <a name="fixed-price"></a>Fast pris

I faktureringsmetoden fast pris åtar en leverantör sig att leverera projektet till en fast kostnad för kunden. Kunden faktureras det offererade värdet för offertraden med fast pris oavsett vilka kostnader leverantören ådrar sig för att leverera offertraden. Värdet på offertraden med fast pris faktureras på något av följande sätt: 

- Som ett klumpsumma i början eller slutet av projektet eller när en projekt mil stolpe har nåtts. 
- Vid en datumbaserad frekvens av lika stora avbetalningar av det fasta värdet på offertraden. De här avbetalningarna kallas för periodiska milstolpar.
- Vid avbetalningar som har ett monetärt värde som justeras mot förloppet eller vissa milstolpar som uppnås i projektet. I det här fallet kan värdet för varje avbetalningsvärde skilja sig från varandra, men alla måste läggas till i fast värdet på offertraden.

PSA stöder alla tre typerna av fakturascheman för offertrader med fast pris.

## <a name="transaction-classification"></a>Transaktionsklassificering

Professionella tjänsteorganisationer brukar citera och fakturera sina kunder genom klassificering av kostnader. I PSA representeras kostnaderna av följande transaktionsklassificeringar:

- **Tid** – denna klassificering visar kostnaden för arbete eller personalens tid i ett projekt.
- **Utgift**: – denna klassificering representerar alla andra typer av utgifter i ett projekt. Eftersom utgifter kan klassificeras brett skapar de flesta organisationer underkategorier, t.ex. resa, hyrbil, hotell och kontorsmateriel.
- **Avgift** – denna klassificering representerar diverse omkostnader, sanktioner och andra artiklar som debiteras kunden. 
- **Moms** – den här klassificeringen visar momsbelopp som användare lägger till medan de registrerar utgifter.
- **Materialtransaktion** – den här klassificeringen visar faktiska värden från produktraderna på en bekräftad projektfaktura.
- **Milstolpe** – denna klassificering används av faktureringslogiken för fast pris i PSA.

En eller flera av dessa transaktionsklassificeringar kan associeras med varje offertrad. När en offert har vunnits överförs mappningen mellan transaktionsklassificering och offertrad till kontraktraden.
 
> ![Skärmbild av mappning av transaktionstyper till offert och kontraktrader](media/basic-guide-5.png)
  
En offert kan till exempel innehålla följande två offertrader: 
- Konsultarbete som använder en metod för tids- och materialfakturering där klassificeringar av tid och avgifter gäller. Till exempel är alla tids- och avgiftstransaktioner för exempelprojekten **Dynamics AX Implementering** fakturerade till kunden utifrån den tid och de material som används. 
- Relaterade resekostnader som använder en fast pris faktureringsmetod. Exempelvis faktureras alla resekostnader för exempelprojektet **Dynamics AX Implementering** som ett fast monetärt värde.

> [!NOTE]
> Kombinationen av projekt och transaktionsklassificeringar för **tid**, **utgifter** och **avgifter** som är associerad med en offertrad eller kontraktrad måste vara unika. Om samma kombination av projekt och transaktionsklass är associerad med fler än en kontraktrad eller offertrad fungerar inte PSA korrekt.

## <a name="billing-types"></a>Faktureringstyper

Fältet **faktureringstyp** definierar begreppet debiterbart i PSA. Det är ett alternativuppsättning som har följande möjliga värden:

- **Debiterbar** – kostnaden som periodiseras av denna roll/kategori är en direkt kostnad som driver projektkörning och kunden betalar för det här arbetet. Betalningen kan administreras som en avtalad tid och material eller med fast pris. Den anställde som tillbringar denna tid får emellertid motsvarande kredit för hans eller hennes fakturerbara utnyttjande.
- **Icke-debiterbar** – kostnaden som periodiseras av denna roll/kategori beaktas som en direkt kostnad som driver projektkörning även om kunden inte erkänner detta och kommer inte att betala för det här arbetet. Den medarbetare som tillbringar denna tid krediteras inte med fakturerbart utnyttjande för den.
- **Kostnadsfritt** – kostnaden som periodiseras av denna roll/kategori är en direkt kostnad som driver projektkörning och kunden erkänner detta. Den medarbetare som tillbringar denna tid krediteras med fakturerbart utnyttjande för den. Kostnaden debiteras emellertid inte kunden.
- **Inte tillgängligt** – de kostnader som uppstår för interna projekt som inte kräver någon intäktsspårning spåras med hjälp av det här alternativet.

## <a name="invoice-schedule"></a>Fakturaschema

Ett fakturaschema är en serie datum som visas när ett projekt faktureras. Du kan välja att skapa ett fakturaschema på en offertrad i PSA. Varje offertrad kan ha ett eget fakturaschema. Om du vill skapa ett fakturaschema måste du ange följande attributvärden:

- Startdatum för fakturering 
- Ett leveransdatum som representerar slutdatum för faktureringen i projektet
- En faktureringsfrekvens

För PSA används dessa tre attributvärden för att generera en preliminär uppsättning datum för att skapa fakturering.

## <a name="invoice-frequency"></a>Faktureringsfrekvens

Fakturafrekvens är en entitet som lagrar attributvärden som hjälper till att uttrycka hur ofta fakturan skapas. Följande attribut uttrycker eller definierar entiteten för fakturafrekvens:

- **Period** - perioder för varje månad, varannan vecka och varje vecka stöds. 
- **Körs per period** - för perioderna varje vecka och varannan vecka, kan du endast definiera en körning per period. För månadsperioder kan du definiera mellan en och fyra sekvenser per period. 
- **Dagar av körning** – de dagar då faktureringen ska köras. Du kan konfigurera detta attribut på två olika sätt:
  - **Vardagar** – du kan till exempel ange att faktureringen ska köras varje måndag eller vartannat måndag. Kunder som måste konfigurera fakturering för att köras på en arbetsdag kan föredra den här typen av konfiguration. 
  - **Kalenderdagar** – du kan till exempel ange att faktureringen ska köras den sjunde och tjugonde dagen i varje månad. Vissa organisationer kanske föredrar den här typen av konfiguration eftersom den hjälper till att säkerställa att faktureringen körs enligt ett fast schema varje månad.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fakturaschema för en offertrad med fast pris

För en offertrad med fast pris kan du använda rutnätet **fakturaschema** för att skapa faktureringsmilstolpar som motsvarar värdet på offertraden.

- Om du vill skapa faktureringsmilstolpar som är jämnt fördelade väljer du en fakturafrekvens, anger startdatum för fakturering på offertraden och väljer **begärt slutdatum** för offerten i avsnittet **Sammanfattning** i offerthuvudet. Välj sedan **skapa periodiska milstolpar** för att skapa lika stora milstolpar som bygger på vald fakturafrekvens. 
- Om du vill skapa en klumpsumma för faktureringsmilstolpe skapar du en milstolpe och anger sedan värdet för offertraden som milstolpebelopp.
- Om du vill skapa faktureringsmilstolpar som bygger på specifika uppgifter i projektplanen skapar du en milstolpe och mappar den till projektets schemaelement i användargränssnittet för faktureringsmilstolpe.
