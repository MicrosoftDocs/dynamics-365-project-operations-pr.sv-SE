---
title: Projektkontrakt
description: I det här ämnet finns exempel på de projektkontrakt som du kan skapa för olika typer av projekt och finansieringskällor och hur du kan hantera kontrakt och fakturera projektkunder.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cfc5183ce28574d865389eba72cafd3528741cc
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683514"
---
# <a name="project-contracts"></a>Projektkontrakt

[!include [banner](../includes/banner.md)]

I det här ämnet finns exempel på de projektkontrakt som du kan skapa för olika typer av projekt och finansieringskällor och hur du kan hantera kontrakt och fakturera projektkunder.

Den typ av projekt som du skapar för ett projektkontrakt avgör vilken metod som används för att fakturera projektkunderna. Du kan ändra ett projektkontrakt och ett relaterat projekt, men du kan inte ändra projekttypen. 

Genom att använda ett projektkontrakt kan du fakturera ett eller flera projekt samtidigt. Projektkontraktet ger även garanti för ett konsekvent faktureringsförfarande för varje del projekt i en projektstruktur. 

Alla projekt som ska faktureras måste kopplas till ett projektkontrakt. Inställningarna för ett projektkontrakt gäller för alla projekt och del projekt som är associerade med projektkontraktet. 

Ett projektkontrakt kan ange en eller flera finansieringskällor. Därför kan du dela upp faktureringen mellan flera olika fonder, ange finansieringsgränser så att finansieringskällor inte faktureras mer än ett visst belopp och konfigurera finansieringsregler för debitering av utgifter.

## <a name="funding-for-project-contracts"></a>Finansiering av projektkontrakt
I vissa projektkontrakt anges att flera parter delar ansvaret för att finansiera projektkostnaderna. Här följer några exempel:

-   En stor kund som har en förfrågan om flera divisioner som påverkar projektets finansiering.
-   Företaget delar kostnaderna för ett stort projekt med en extern organisation.
-   Ett vägprojekt finansieras av två kommuner.
-   Ett broprojekt finansieras av ett statligt bidrag och ett privat företag.

I Dynamics 365 Finance kan du dela faktureringen för en enstaka transaktion eller ett helt projekt mellan flera kunder, anslag eller organisationer. 

I projekt som har flera fonder kallas alla parter som bidrar till finansieringen av ett avancerat finansieringsprojekt för finansieringskällor. När en kund, organisation eller ett bidrag har definierats som en finansieringskälla kan den tilldelas en eller flera finansieringsregler. Finansieringsregler innehåller kriterier som avgör hur avgifter fördelas till olika finansieringskällor för ett projekt. 

Eftersom lagerartiklar, t.ex. de som visas på inköpsrekvisitioner och inköpsorder, inte kan delas, kan kostnadsbeloppet inte delas upp mellan flera finansieringskällor vid distributionstillfället. Därför kvarstår värdet för finansieringskällan som 0 (noll) tills lagerproblemet bokförs. När lager utleveransen har bokförts fördelas kostnadsbeloppet enligt konto distributionsreglerna för projektet.

Här följer några steg som du kan vidta för att göra det lättare att dela faktureringen mellan flera finansieringskällor:

-   Ange att alla transaktioner som anges för ett projekt använder samma försäljningsvaluta som projektkontraktet.
-   Ställ in finansieringsgränser så att en finansieringskälla inte faktureras mer än ett visst belopp mot ett projekt.
-   Konfigurera finansieringsregler och finansieringsgränser för varje arbetare, artikel, kategori, kategorigrupp och transaktionstyp (eller för alla transaktionstyper).
-   Välj valfria start- och slutdatum för att definiera den period när varje finansieringsregel är giltig.
-   Ange den procentsats som varje finansieringskälla är ansvarig för.
-   Ange vilken finansieringskälla som ansvarar för avrundningsdifferenser som orsakas av beräkningar av finansieringstilldelningar.
-   Ställ in regler som avgör hur projektkostnader faktureras till externa kunder och debiteras interna organisationer.
-   Registrera transaktioner på ett spärrat finansieringskonto tills ytterligare finansiering kan erhållas, eller tills du bestämmer dig för att bära kostnaderna internt.

För att avgöra vilken momsgrupp som ska kopplas till en transaktion, genomsöks projektet efter en tilldelning av skattegrupp. Om ingen tilldelning av skattegrupp har gjorts på projektnivån genomsöks projektkontraktet.

### <a name="example-multiple-funding-sources-simple"></a>Exempel: flera finansieringskällor (enkel)

Följande tabell innehåller scenarier för hantering av en finansieringsfördelning mellan flera finansieringskällor. De här scenarierna bygger på följande förutsättningar:

-   Prioritetsinställningarna gäller för tilldelning av medel innan andra kriterier för finansieringsregler tillämpas.
-   Inget datumintervall har angetts för att definiera perioden när finansieringsregeln är giltig.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Finansieringskälla</strong></td>
<td><strong>Allokeringsprocent</strong></td>
<td><strong>Allokeringsprioritet</strong></td>
</tr>
<tr class="even">
<td>Du vill fördela kostnaderna till en finansieringskälla tills fonderna är uttömda kan du fördela kostnaderna till en andra finansieringskälla tills medlen är uttömt och slutligen fördela de återstående kostnaderna till en tredje finansieringskälla.</td>
<td><ul>
<li>Finansieringskälla 1</li>
<li>Finansieringskälla 2</li>
<li>Finansieringskälla 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du vill tilldela 75 procent av kostnader till en finansieringskälla och 25 procent till en andra finansieringskälla. När någon av dessa finansieringskällor är uttömda vill du betala de återstående kostnaderna från en tredje finansieringskälla.</td>
<td><ul>
<li>Finansieringskälla 1</li>
<li>Finansieringskälla 2</li>
<li>Finansieringskälla 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Du vill tilldela 75 procent av kostnader till en finansieringskälla och 25 procent till en andra finansieringskälla. När någon av dessa finansieringskällor är uttömda vill du dela upp de återstående kostnaderna mellan en tredje finansieringskälla och en fjärde finansieringskälla.</td>
<td><ul>
<li>Finansieringskälla 1</li>
<li>Finansieringskälla 2</li>
<li>Finansieringskälla 3</li>
<li>Finansieringskälla 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du vill tilldela de första 25 procent av kostnader till en finansieringskälla och resten till en andra finansieringskälla.</td>
<td><ul>
<li>Finansieringskälla 1</li>
<li>Finansieringskälla 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exempel: flera finansieringskällor (komplex)

Du har tre finansieringskällor som du vill använda i följande ordning:

1.  Använd finansieringskälla 2 och finansieringskällan 3 lika tills finansieringskällan 2 är uttömd.
2.  Fortsätt använda finansieringskällan 3 tills den är uttömd.
3.  Använd finansieringskällan 1 efter att finansieringskällan 3 har uttömts.

För att uppnå detta måste du göra följande:

-   Ställ in finansieringsgränser för finansieringskällan 2 och finansieringskällan 3 för respektive belopp.
-   Skapa följande finansieringsregler:
    -   Regel 1 (prioritet 1): allokera 50 procent av transaktionerna till finansieringskällan 2 och 50 procent till finansieringskällan 3.
    -   Regel 2 (prioritet 2): tilldela 100 procent av transaktionerna till finansieringskällan 3.
    -   Regel 3 (prioritet 3): tilldela 100 procent av transaktionerna till finansieringskällan 1.

Installationen fungerar eftersom transaktionerna kontrolleras mot regler och begränsningar för att avgöra om någon av dem gäller för transaktionen. Om inga specifika regler eller begränsningar gäller för transaktionen gäller regeln Alla transaktioner. Regeln Alla transaktioner matchar alla transaktioner. 

Om en regel hittas som matchar en transaktion tillämpas först den procent som har tilldelats i den regeln, men först efter att matchningarna har kontrollerats mot eventuella begränsningar som har ställts in. Om en gräns har uppnåtts och en finansieringskällas medel är uttömda bortses från finansieringsregeln som är associerad med finansieringsgränsen och programmet kontrollerar om nästa regel som gäller. 

I vissa fall kan endast en del av en transaktion fördelas under en regel. Detta kan inträffa om en gräns uppnås när transaktionen har fördelats. I det här fallet fördelas endast ett visst belopp enligt den regeln, till exempel 50 procent för varje finansieringskälla. Detta är fallet i regel 1, som beskrivs ovan i det här avsnittet. Återstoden fördelas enligt nästa regel i sekvensen. 

I följande tabell granskas detta scenario mer detaljerat.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Detaljer</strong></td>
</tr>
<tr class="even">
<td>Finansieringsregler</td>
<td><ul>
<li>Regel 1 (prioritet 1): alla transaktioner. Fördela finansieringskällan 2 med 50 % och finansieringskällan 3 vid 50 %.</li>
<li>Regel 2 (prioritet 2): alla transaktioner. Fördela finansieringskällan 3 med 100 %.</li>
<li>Regel 3 (prioritet 2): alla transaktioner. Fördela finansieringskällan 1 med 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansieringsgränser</td>
<td><ul>
<li>Finansieringskälla 1 gräns = 10 000,00</li>
<li>Finansieringskälla 2 gräns = 500,00</li>
<li>Finansieringskälla 3 gräns = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaktion 1</td>
<td><strong>Transaktionsbelopp:</strong> 100,00<strong>Finansiering:</strong> Transaktionen betalas enligt regel 1 endast på grund av att transaktionen är helt betald efter att regel 1 har tillämpats. Transaktionen finansieras lika mycket mellan finansieringskällan 2 och finansieringskällan 3.
<ul>
<li>Finansieringskälla 2: 50,00</li>
<li>Finansieringskälla 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaktion 2</td>
<td><strong>Transaktionsbelopp:</strong> 5 000,00<strong>Finansiering:</strong> Transaktionen betalas enligt alla tre regler. <strong>Regel 1</strong>
<ul>
<li>Finansieringskälla 2: 450,00</li>
<li>Finansieringskälla 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finansieringskälla 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finansieringskälla 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Totalt antal som fördelas för varje finansieringskälla</td>
<td><ul>
<li>Finansieringskälla 1: 3 850,00</li>
<li>Finansieringskälla 2: 500,00</li>
<li>Finansieringskälla 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Faktureringsregler
När du förhandlar ett projektkontrakt med en kund anger du hur och när du kan fakturera kunden för arbete med ett projekt. När du har ställt in projektkontraktet och projekten kan du ange faktureringsregler för projektet. Faktureringsregler bygger på de projekt villkor som har angetts i projektkontraktet. Vilka faktureringsregler du kan skapa beror på villkoren i projektkontraktet och projekttypen, till exempel tid och material eller fast pris, som du associerar med faktureringsregeln. Du kan skapa mer än en faktureringsregel för ett projektkontrakt. Du kan också tilldela en faktureringsregel till flera projekt som är associerade med samma projektkontrakt och som har liknande faktureringsvillkor. 

Du kan ange följande typer av faktureringsregler:

-   **Leveransenhet** – fakturera en kund när du fyller i en leveransenhet. Du anger leveransenheterna i kontraktet.
-   **Förlopp** – fakturera en kund när du slutför en angiven procentsats av projektet. Du kan ange att en procentandel av arbetet som har slutförts automatiskt ska beräknas med en faktureringsregel, eller så kan du beräkna kundens procentsats manuellt med beloppet.
-   **Milstolpe** – fakturera en kund med hela beloppet för en projekt milstolpe när milstolpen nås.
-   **Avgift** – fakturera en kund för dina tjänster plus en hanteringsavgift som vanligtvis är en procentandel av servicekostnaden.
-   **Tid och material** – fakturera en kund för värdet av tid och material som används i ett projekt.

För alla typer av faktureringsregler kan du ange en kvarhållande procent som dras av från kundfakturor tills ett projekt når ett överenskommet stadium. Procentsats för kvarhållandet anges i projektkontraktet. Beloppet beräknas utifrån och subtraheras det totala värdet på raderna i en kundfaktura. 

För faktureringsregler för **Tid och material** och **Förlopp** kan du tilldela debiterbara kategorier. Debiterbara kategorier visar de transaktioner som ska tas med på kundfakturor. 

När du är klar att fakturera kunden beräknas beloppet för att fakturera för projektet utifrån faktureringsregler och ett projektfakturaförslag skapas. 

I följande avsnitt finns exempel som visar hur du skapar och hanterar faktureringsregler för ett projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exempel: skapa en faktureringsregel som baseras på antalet levererade enheter

Företaget går in i ett avtal för att tillhandahålla totalt fem utbildningar till en kunds anställda med en kostnad på 10 000 per utbildningssession. Kunden faktureras efter varje utbildningssession. 

När du anger faktureringsregler för kontraktet använder du följande värden:

-   Leveransenheten är en utbildningssession.
-   Enhetspriset är 10 000 per utbildningssession.
-   Det totala antalet enheter är fem utbildningssessioner.

När du har slutfört en utbildningssession kan du skapa en faktura för 10 000 för den första enheten som levererades och sedan skicka fakturan till kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exempel: skapa en faktureringsregel som bygger på en angiven procentsats av projektslutförande (manuell beräkning)

Din organisation, ett programvarukonsultföretag, går in i ett avtal med en kund för att utveckla en del av en produkt som kunden utvecklar. Din organisation godkänner att programvarukoden levereras under en period om sex månader. Kunden går med på att betala organisationen totalt 100 000 för arbetet. Du skapar en faktureringsregel för att fakturera kunden utifrån den procentsats av arbete som har slutförts på projektet, enligt vad som anges i kontraktet.

-   Vid slutet av den första månaden uppfyllde du kunden för att fastställa procentandelen av arbetet som slutförts. När du och kunden har granskat projektet bestämmer du att projektet är 15 procent klart.
-   Du skapar en faktura för 15 000 (15 procent av 100 000) och skickar den till kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exempel: skapa en faktureringsregel som bygger på en angiven procentsats av projektslutförande (automatisk beräkning)

Din organisation, ett företag för programutveckling, kan komma att utveckla ett lönebokföringspaket för en kund i 30 000. Kunden samtycker till att betala din organisation baserat på procentandelen av genomfört arbete. Du uppskattar att projektkostnaderna är 20 000. I projektkontraktet anges de arbetskategorier som du använder i faktureringsprocessen. Du ställer in faktureringsregler som automatiskt beräknar fakturabeloppen för den procentandel av arbetet som slutförts för varje kategori. Du lägger upp en budget för varje kategori:

-   **Utveckling** – kostnad på 15 000 och intäkt på 20 000
-   **Installation** – kostnad på 5 000 och intäkt på 10 000

När du skapar en kundfaktura för första gången beräknas fakturabeloppet automatiskt utifrån följande information:

-   Efter en månad skickar arbetaren i projektet en tidrapport för projektet. Kostnaden för arbetarens timmar är 5 000 för utveckling och 1 000 för installation. Utvecklingsarbetet är 33 procent färdigt (5 000 faktiska kostnader/15 000 budgeterad kostnad) och installationen är 20 procent färdig (1 000 faktisk kostnad/5 000 budgetkostnad).
-   Fakturabeloppet på 8 667 beräknas automatiskt (33 procent av 20 000 + 20 procent av 10 000).
-   Du skapar en faktura för 8 667 och skickar den till kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exempel: skapa en faktureringsregel som baseras på avtalade milstolpar

Din organisation, ett konsultföretag inom företagsledning, åtar sig att genomföra marknads undersökningar för en konsumentprodukt som kunden planerar att sälja. Kunden accepterar att använda dina tjänster under en period på tre månader, med början i mars och går med på att betala din organisation 50 000. Det finns tre milstolpar i projektet:

-   Milstolpe 1: samla in konsumentdata – 31 mars
-   Milstolpe 2: analysera konsumentdata – 30 april
-   Milstolpe 3: presentera ett förslag till produktlivsduglighet – 31 maj

Kunden går med på att betala din organisation 10 000 för den första milstolpen, 20 000 för den andra milstolpen och 20 000 för den tredje milstolpen. 

När du skapar projektkontraktet godkänner du att fakturera kunden utifrån den milstolpe som har slutförts. Inställningarna av faktureringsregler består av följande steg:

-   Definiera projektets milstolpar.
-   Definiera beloppet för att fakturera kunden när varje milstolpe är slutförd.

När den första milstolpen är avslutad den 31 mars markerar du den som slutförd och skapar sedan en faktura för 10 000 och skickar den till kunden. Du kan inte skapa en faktura för en milstolpe förrän du har markerat milstolpen som slutförd.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exempel: skapa en faktureringsregel som bygger på tjänster plus en hanteringsavgift

Din organisation, ett konsultföretag inom företagsledning, åtar sig att genomföra marknadsundersökningar för att utvärdera livskraften hos en produkt som kunden, ett detaljhandelsbolag, utvecklar. Villkoren i avtalet anger att du ska tillhandahålla tjänster för de tre viktigaste ledningskonsulterna, som kommer att utföra forskningen på tid och material. Kunden går med på att betala 100 per timme och en hanteringsavgift på 10 procent för de konsulttider som debiteras för projektet. 

När du skapar projektkontraktet skapar du en faktureringsregel som lägger till en hanteringsavgift på 10 procent för de konsulttimmar som debiteras projektet. 

När du skapar en faktura för kunden faktureras kunden en hanteringsavgift på 10 procent plus kostnaden för konsulttimmarna. Om de tre konsulterna arbetade med 200 timmar totalt i projektet skapas en faktura på 22 000 på grundval av följande beräkning:

-   200 timmar för 100 per timme = 20 000
-   10 procents hanteringsavgift = 2 000
-   Totalt fakturabelopp = 22 000

Om avgifter är momspliktiga till en kund och du väljer en momsgrupp i projektkontraktet, registreras momsgruppen automatiskt i faktureringsregeln för avgifter.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exempel: skapa en faktureringsregel för värdet av tid och material

Din organisation, ett programvarukonsultföretag, godkänner att de tillhandahåller fem tekniska konsulter för att arbeta med ett programutvecklingsprojekt för en kund under de kommande sex månaderna. Kunden accepterar att betala 150 för varje konsulttimme plus kostnaden för kontorsmateriel. Din organisation skickar en faktura till kunden i slutet av varje månad. 

När du skapar projektkontraktet godkänner du att fakturera kunden varje månad för tid och material i projektet. Du skapar en faktureringsregel som innehåller följande information:

-   Kontraktperioden är sex månader.
-   Konsultens tid beräknas till 150 per timme.
-   Kontorsmateriel faktureras till kostnaden och den totala kostnaden för projektet får inte överstiga 10 000.
-   Du skapar en kundfaktura i slutet av varje kalendermånad under projektet.

Under den första månaden registreras sammanlagt 800 timmar av konsulterna i projektet. Kostnaden för kontorsmateriel som debiteras för projektet är 2 000. I slutet av månaden skapar du därför en faktura på 122 000 som beräknas som 800 timmar vid 150 per timme, plus 2 000 för kontorsmateriel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]