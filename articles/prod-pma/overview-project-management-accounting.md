---
title: Översikt över projektledning och redovisning
description: Funktionerna för projektledning och redovisning kan användas i flera branscher för att tillhandahålla tjänster, producera produkter och få resultat.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 634e35f7bd399d3d97659b4bd6f2f3a6dbd5839f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085683"
---
# <a name="project-management-and-accounting-overview"></a>Översikt över projektledning och redovisning

[!include [banner](../includes/banner.md)]

Funktionerna för projektledning och redovisning kan användas i flera branscher för att tillhandahålla tjänster, producera produkter och få resultat.  

Ett projekt är en grupp med aktiviteter som har utformats för att tillhandahålla en tjänst, producera en produkt eller uppnå ett resultat. Projekt förbrukar resurser och genererar ekonomiska resultat i form av intäkter eller tillgångar.

## <a name="projects-across-industries"></a>Projekt mellan branscher
Du kan använda funktionerna för projektledning och redovisning i flera branscher, som du ser på följande bild.

[![Projekt mellan branscher](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

I ett callcenter kan en biljett användas för att beskriva den uppsättning åtgärder som krävs för att lösa ett samtal. Konsultbolag, t.ex. företagslednings- eller tekniska konsultorganisationer eller reklambyråer, avser deras verksamhet som projekt. I marknadsföring representerar en kampanj en uppsättning arbete som måste levereras. I projektbaserade tillverkningstyper relaterar en produktionsorder det arbete som måste utföras för att producera vissa färdiga varor. Vilket namn som används för dem omfattar projekten resurser, scheman och kostnader och projektlednings- och redovisningsfunktionerna kan hjälpa dig att planera, utföra och analysera de här projekten.

## <a name="project-phases"></a>Projektfaser
Även om följande processflöde riktar sig mot externa projekt, eller projekt som har slutförts för en eller flera kunder, gäller funktionerna även för interna, kostnads projekt. 

![Tre etapper av ett projekt](./media/3-stages-of-a-project.png) 

Som framgår av illustrationen ovan kan projektledning och redovisning delas upp i tre faser:

1.  Initiera
2.  Kör
3.  Analysera

## <a name="initiate-the-project"></a>Initiera projektet
Under projektets initiering sker flera viktiga processer. Du kan använda en projektoffert för att kommunicera det uppskattade arbetet, kostnaderna och materialet för kunden. Du kan registrera faktureringsvillkor, begränsningar och avtal i ett projektkontrakt. Du kan använda en struktur för att planera och beräkna arbetet. Du kan ställa in prognoser och budgetar för att guida projektkörningen. I följande illustration visas projektstrukturen.[![projektstruktur](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Skicka projektofferter

I den inledande försäljningsfasen av ett projekt låter ett projektoffert dig ge en kund ett icke-bindande erbjudande. En offert kan innehålla element som artiklar och tjänster som offereras, grundläggande kontaktinformation, särskilda handelsavtal och rabatter samt möjliga skatter och tilläggsavgifter.

Du kan även utfärda en garanti för en projekt offert transaktion mellan organisationen och kunden. När projektofferten har skapats kan du skapa en begäran om garantibrev för kunden och skicka in den till banken. När banken har godkänt förfrågan skickas garanti brevet till kunden. 

Mer information finns i [Projektofferter](project-quotations.md).

### <a name="create-project-contracts"></a>Skapa ett projektkontrakt

När du anger ett kontrakt med en kund eller annan finansieringskälla för att slutföra ett projekt måste du först skapa ett projektkontrakt. När du sedan skapar projektet måste du tilldela det motsvarande kontrakt. Den typ av projekt som du skapar för ett projektkontrakt avgör vilken metod som används för att fakturera projektkunderna. Du kan ändra ett projektkontrakt och ett relaterat projekt, men du kan inte ändra projekttypen. Mer information om projekttyper finns i avsnittet "skapa projekt".

Mer information om projektkontrakt finns i [projektkontrakt](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Skapa uppdelad arbetsstruktur

Graden av detaljer i en WBS beror på vilken exakthet som krävs i uppskattningarna och vilken uppföljningsnivå som krävs för dessa uppskattningar. Projekt som har mycket låg tolerans för förseningar i schemat eller kostnaden kräver vanligen en mer detaljerad WBS och du måste också ha en noggrann uppföljning av arbetsförloppet och WBS. 

Mer information finns i [Översikt över uppdelad arbetsstruktur](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Skapa projektprognoser och budgetar

Du kan använda prognoser om organisationen har ett operationellt perspektiv och fokuserar på intäkter och kostnader som härleds från vissa transaktioner. Men om din organisation fokuserar mer på ekonomiska belopp kan du använda budgetering. Varje metod har sina fördelar. Mer information finns i [projektprognoser och budgetar](project-forecasts-budgets.md).

### <a name="create-projects"></a>Skapa projekt

Du kan skapa sex typer av projekt i Finance. Varje projekttyp ställs in på ett annat sätt för kostnader och intäktsredovisning. Projekttypen som du väljer beror på syftet med projektet. I följande tabell beskrivs hur de olika projekttyperna används ofta.
                                                                                                            
<table>
  <tr>
    <td>Projekttyp</th>
    <td>Beskrivning</th>
  </tr>
  <tr>
    <td>Tid och material</td>
    <td>I tids- och materialprojekt faktureras kunden för alla kostnader som uppstår i ett projekt. Kostnaderna omfattar kostnader för timmar, utgifter, artiklar och avgifter.</td>
  </tr>
  <tr>
    <td>Fast pris</td>
    <td>I fastprisprojekt består fakturor av à conto-transaktioner. Ett fastprisprojekt faktureras enligt en faktureringsplan som baseras på ett projektkontrakt. Intäkter för ett fastprisprojekt kan beräknas och bokföras i hela projektet med metoden slutförd procent. Intäkterna kan också beräknas och bokföras när projektet har slutförts med metoden slutfört kontrakt. Företag kan ofta dra nytta av värdet av produkter i arbete (PIA) för att beräkna hur mycket ett projekt eller en grupp av projekt är färdigställt.</td>
  </tr>
  <tr>
    <td>Investering</td>
    <td>Investeringsprojekt är projekt som inte producerar omedelbara intäkter. De används vanligtvis för långfristiga interna projekt där kostnaderna måste kapitaliseras. Endast kostnader för artiklar, timmar och utgifter kan registreras för ett investeringsprojekt. Kostnader i ett investeringsprojekt spåras och styrs med hjälp av funktionen för uppskattning. Investeringsprojekt kan ställas in med en valfri maximal kapitalisering. I takt med att ett projekt fortlöper registrerar du kostnaderna i PIA-konton där kostnaderna innehas tills projektet har slutförts. När projektet har eliminerats överför du PIA-värdet till en anläggningstillgång, ett redovisningskonto eller ett nytt projekt. <br></br> <strong>OBS!</strong> Transaktioner för investeringsprojekt visas inte på sidan <strong>Bokför kostnader<strong>, <strong>Periodisera intäkter</strong> eller <strong>Skapa fakturaförslag</strong>.</td>
  </tr>
  <tr>
    <td>Kostnadsprojekt</td>
    <td>Precis som investeringsprojekt används kostnadsprojekt vanligtvis för att spåra interna projekt och det är bara timmar, utgifter och artiklar som kan registreras. Kostnadsprojekt är emellertid vanligtvis kortare än investeringsprojekt. Till skillnad från investeringsprojekt kan kostnadsprojekt också inte kapitaliseras mot balansräkningskonto. Deras projekttransaktioner bokförs endast på vinst- och förlust konton. <br></br> <strong>OBS!</strong> Transaktioner för kostnadsprojekt visas inte på sidan <strong>Bokför kostnader</strong>, <strong>Periodisera intäkter</strong> eller <strong>Skapa fakturaförslag</strong>. Eftersom kostnadsprojekt vanligtvis används för att spåra interna projekt behöver de inte vanligtvis vara associerade med ett kundkonto. Om installationen kräver att artikel behoven skapas för inköps order måste du emellertid associera kostnadsprojektet med en kund. Den här kopplingen krävs eftersom artikel behoven hanteras som försäljningsorderrader och systemet kräver att en kund ska anges. Den här inställningen medför emellertid inte att artikel behov skapas automatiskt från en inköpsorder. För kostnadsprojekt ignoreras inställningen <strong>skapa artikelkrav</strong>. Om du behöver ett artikelkravs i ett kostnadsprojekt kan du skapa det manuellt, förutsatt att kunden är associerad med projektet.</td>
  </tr>
  <tr>
    <td>Intern</td>
    <td>Interna projekt används för att spåra kostnader i ett projekt som är internt i organisationen. Interna projekt kan tillhandahålla ett planeringsverktyg för att hantera resursförbrukning. <br></br><strong>OBS!<strong> Transaktioner på interna projekt återspeglas inte i sidan <strong>Periodiserad intäkt</strong> eller <strong>Skapa fakturaförslag</strong>.</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>Tidsprojekt används för att spåra tid som associeras med icke debiterbara och icke produktiva aktiviteter, till exempel ett projekt för att spåra sjuktid för arbetare. Transaktioner i tidsprojekt bokförs inte i redovisningen. De ingår i stället i rapporterna om användning av arbetare. Endast timtransaktioner kan registreras i tidsprojekt. Du kan använda en timjournal eller en tidrapport för att registrera dessa timmar för projektet. När timmarna har registrerats visas de som projekttransaktioner men har inte motsvarande verifikationstransaktioner. <br></br><strong>OBS!</strong> Transaktioner för tidprojekt visas inte på sidan <strong>Bokför kostnader</strong>, <strong>Periodisera intäkter</strong> eller <strong>Skapa fakturaförslag</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Tilldela arbetare, kategorier och resurser

Du kan schemalägga arbetsresurser utifrån antingen krav och schema för ett projekt, eller på arbetarnas kompetens och tillgänglighet. Med funktionerna för schemaläggning av resurser kan du driftsätta organisationens arbetare på ett effektivt och effektivt sätt. Du kan snabbt hitta de mest kvalificerade arbetarna som är tillgängliga för att arbeta med projektet. Du kan också enkelt se hur dessa arbetare kan användas mer effektivt under projektets gång. 

Här följer några exempel på hur du kan använda funktionen för schemaläggning av resurser:

-   Använd information om arbetares attribut, till exempel utbildning, färdigheter, certifiering och projekterfarenhet, för att matcha arbetaren med projektets krav.
-   Använd information om en arbetares kalender och tillgänglighet så att de överensstämmer med arbetsschemats projektkalender.
-   Granska varje arbetares kapacitet och kontrollera hur kapaciteten som används. Om en arbetare exempelvis används kan arbetaren tilldelas ett projekt som passar hans eller hennes tillgänglighet och attribut.
-   Granska en arbetares tillgänglighet för att se till att det inte finns några kalenderkonflikter med arbetarens tilldelningar.
-   Granska informationen om användning av arbetare i antingen en sammanfattningsvy (t.ex. efter avdelning eller efter arbetare) eller en detaljerad vy (t.ex. av arbetare på en avdelning eller per veckas information för varje arbetare).
-   Ändra resurstilldelningar för olika tidsenheter, till exempel dag, vecka eller månad, om du vill optimera arbetarnas användning.

## <a name="execute-the-project"></a>Kör projektet
När projekt körs registrerar gruppmedlemmar eller chefer arbete och de utgifter som uppstår, med hjälp av tidrapporter, utgiftsrapporter och andra affärsdokument. Projektledarna har verktyg som du kan använda för att övervaka förbrukningen av budgeterade belopp för projektet. Projektledarna kan också beställa, plocka eller anskaffa material för projekt med hjälp av inköpsorder och andra affärsdokument. Fakturor är förberedda och godkända så att kunder kan faktureras för pågående arbete. Slutligen identifieras intäkter under den här processen för att påverka organisationens ekonomi.

### <a name="manage-work-breakdown-structures"></a>Hantera uppdelad arbetsstruktur

En WBS är en beskrivning av det arbete som ska utföras för ett projekt. En WBS är en hierarki med uppgifter. Den representerar inte bara arbetet för varje uppgift utan även aktivitetens storlek, kostnad och varaktighet. 

Mer information finns i [Översikt över uppdelad arbetsstruktur](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Hantera projektprognoser och budgetar

Det finns två sätt att hantera och kontrollera dina projekt: projektprognoser och projektbudgetar. Du kan använda prognoser om organisationen har ett operationellt perspektiv och fokuserar på intäkter och kostnader som härleds från vissa transaktioner. Men om din organisation fokuserar mer på ekonomiska belopp kan du använda budgetering.

Mer information finns i [projektprognoser och budgetar](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Skapa produktionsorder

En projektrelaterad produktionsorder kan länkas till en försäljningsorder eller ett artikelkrav antingen med metoden slutförd eller för förbrukad artikel. Om produktionsordern skapas manuellt finns det även en länk mellan produktionsordern och försäljningsordern eller artikel behovet (ingen länk till order). Men om produktionsordern skapas automatiskt för att uppfylla en försäljningsorder eller ett artikelkrav finns det en länk mellan produktionsordern och försäljningsordern eller artikelkravet (länk till order). 

Använd en av följande metoder utifrån kombinationer av dessa faktorer:

- **Slutförd artikel/länka till order** – länka projektet till en försäljningsorder eller ett artikelkrav. När du använder den här metoden bokförs faktiska projektkostnader när försäljningsordern är fakturerad eller när följesedeln uppdateras för artikelkravet. Kostnaden bokförs som en färdig artikel.
- **Slutförd artikel/ingen länk till order** – de faktiska kostnaderna kan inte bokföras förrän produktionscykeln för en artikel har statusen **avslutad**. Kostnaden för den färdiga artikeln bokförs som en enskild transaktion.
- **Förbrukad artikel/länka till order** – länka projektet till ett artikelkrav. Med den här metoden kan du visa faktiska projektkostnader när produktionen har statusen **startad** eller rapporterad som avslutad. Kostnaderna bokförs som flera projektartikel transaktioner för råmaterial och timmar som förbrukas för produktion. När följesedeln uppdateras för artikelkrav bokförs inga projektkostnader. Du kan även ange vilken nivå i strukturen (BOM) som projekten i produktionen ska spåras med.
- *<strong><em>Förbrukad artikel/ingen länka till order</em></strong>* – länka projektet till ett artikelkrav. Med den här metoden kan du visa faktiska projektkostnader när produktionen har statusen <strong>startad</strong> eller rapporterad som avslutad. Kostnaderna bokförs som flera projektartikel transaktioner för råmaterial och timmar som förbrukas för produktion. Du kan även ange nivån i strukturhierarkin som projekten i produktionen ska spåras med.

### <a name="procure-products-and-services"></a>Anskaffa produkter och tjänster

Inköp och försäljning av artiklar är vanliga aktiviteter i många projekt som fokuseras på företag.

#### <a name="purchase-orders-for-projects"></a>Inköpsorder för ett projekt

Syftet med inköpsordern avgör när inköpsordern konsumeras och därför när artiklar debiteras för ett projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metod</th>
<th>Syfte</th>
<th>Förbrukning av artiklar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skapa en ny inköpsorder direkt.</td>
<td>Köp artiklar från en extern leverantör för förbrukning i ett projekt. Du kan skapa inköpsorder på följande sätt:
<ul>
<li>Från själva projektet. I det här fallet är projektet redan definierat för inköpsordern.</li>
<li>Genom att navigera till projektets inköpsorder. Du måste välja både leverantören och projektet för att skapa inköpsordern.</li>
</ul></td>
<td>Artiklar förbrukas när leverantörsfakturan uppdateras.</td>
</tr>
<tr class="even">
<td>Skapa en inköpsorder från en försäljningsorder.</td>
<td>Köpa artiklar när du skapar en försäljningsorder från ett projekt.</td>
<td>Artiklar förbrukas när försäljningsordern faktureras kunden.</td>
</tr>
<tr class="odd">
<td>Skapa en inköpsorder från ett artikelkrav.</td>
<td>Köp artiklar när du skapar ett artikelkrav från ett projekt.</td>
<td>Artiklar förbrukas när följesedeln för artikelkrav uppdateras.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Försäljningsorder för projekt

I projektledning och redovisning kan du registrera förbrukningen av artiklar på flera sätt. Du kan sälja artiklar eller köpa artiklar från ett projekt, eller reservera artiklar för ett projekt. 

Du kan beställa artiklar från företagets lager för förbrukning i ett projekt. Alternativt kan du köpa artiklar från en extern leverantör. Artiklar kan förbrukas i alla typer av projekt utom tidsprojekt. 

Hur du beställer artiklar beror på varifrån du beställer dem:

-   Om du vill beställa artiklar från företagets lager måste du ange ordern som ett artikelkrav. Om du använder sidan **artikelkrav** kan du ange behovet så att du får artiklarna som delleveranser.Därför kan du skjuta upp förbrukningen av ett antal artiklar tills artiklarna är obligatoriska.
-   Om du vill beställa artiklar från en extern leverantör måste du skapa ordern som en inköpsorder på sidan **inköpsorder**.

> [!NOTE] 
> Följesedeln för en projektrelaterad försäljningsorder kan inte annulleras om artiklarna redan har markerats för paketering. 

I följande tabell visas metoderna för att beställa artiklar och beskriver hur artiklarna förbrukas.

| Metod            | Syfte                                                                                                                                                        | Förbrukning av artikeltransaktioner                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Försäljningsorder       | Ange en transaktion direkt på ett tids- och materialprojekt.                                                                                                   | Artikeltransaktioner förbrukas när kundfakturan bokförs.                                                                               |
| Lagerjournal | Snabbt registrera och underhålla artikelposter. Om du till exempel vill ange ett artikelkrav utifrån en utskriven lista kan lagerjournalen användas. | Artikeltransaktioner förbrukas när journalen bokförs.                                                                                        |
| Artikelkrav  | Ange artiklar som inte ska förbrukas direkt. Med den här metoden kan du spåra antalet artiklar som har konsumerats i en post för ett artikelkrav.    | Artikeltransaktioner förbrukas när följesedeln uppdateras. Det innebär att artikelkravet skapas när följesedeln bokförs. |
| Inköpsorder   | Ange transaktioner på en av tre platser, beroende på vilken inköpsmetod du har.                                                                              | Artikeltransaktioner förbrukas när följesedeln uppdateras eller när kunden eller leverantören faktureras.                                      |

### <a name="process-project-invoices"></a>Bearbeta projektfakturor

Projekttypen bestämmer vilken faktureringsmetod som ska användas. Endast de två externa projekt typerna (tid och material och fast pris) kan faktureras. Tids- och materialprojekt och fastprisprojekt är alltid kopplade till ett projektkontrakt. 

Innan du skapar en kundfaktura för ett projekt kan du skapa en preliminär faktura eller ett fakturaförslag. I ett fakturaförslag kan du välja projekttransaktioner som ska tas med i en projektfaktura. Du kan sedan granska fakturadetaljerna innan du bokför projektfakturan och skicka den till kunden eller andra finansieringskällor. 


Mer information om hur du bearbetar projektfakturor finns i [Fakturering av projekt](https://docs.microsoft.com/dynamics365/finance/accounts-payable/project-invoicing).


### <a name="calculate-the-cost-to-complete-a-project"></a>Beräkna kostnaden för att slutföra ett projekt

När du skapar en uppskattning kan du välja vilken metod som ska användas för att beräkna kostnaden för att slutföra projektet. Du väljer en metod i fältet **Metoden kostnad för att slutföra** på sidan **Skapa uppskattning**. Den metod du väljer används separat för varje kostnadsrad i kostnadsberäkningen. När en rad har statusen **skapad** kan du ändra metoden som tillämpas på den på sidan **kostnadsuppskattning**. 

I följande tabell beskrivs metoderna för att beräkna kostnaden för att slutföra ett projekt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metod</th>
<th>Beskrivning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Total kostnad – faktisk</td>
<td>Du måste ange beräknade kostnader manuellt. När kolumnen <strong>Total kostnad</strong> eller <strong>Total kvantitet</strong> på sidan <strong>Kostnadsuppskattning</strong> har slutförts subtraheras de faktiska kostnaderna från de summor som anges av användaren. Resultatet är kostnaden för att slutföra projektet. Vanligtvis spåras inte förloppet för kostnaderna, t.ex. antalet hotellvistelser och måltider som registreras i varje period. I stället. Spårningen grundar sig vanligtvis på en jämförelse mellan det totala antalet timmar som uppskattas. Den här metoden kräver ingen prognosmodell och den totala kostnaden eller det totala antalet kan ändras manuellt. När ett värde anges i kolumnen <strong>Total kostnad</strong> eller <strong>Total kvantitet</strong> jämför Finance detta värde med de faktiska transaktioner som bokförs i perioden och sedan minskas värdet i kolumnen <strong>Kvantitet att slutföra</strong> eller <strong>Kostnad att slutföra</strong>.</td>
</tr>
<tr class="even">
<td>Total budget – faktisk</td>
<td>Faktiska kostnader jämförs med den prognosmodell som du väljer för att fastställa kostnaden. I den här metoden används en total budgetmodell som omfattar prognostiserade transaktioner. Om du vill få en mer korrekt vy av projektet kan du justera budgetmodellen när projektet pågår. Om du måste justera prognosen följer du nedanstående allmänna process:
<ol>
<li>Kopiera prognostransaktioner till en annan prognosmodell.</li>
<li>Jämför prognostransaktioner med faktiska transaktioner.</li>
<li>Upprätthålla, minska eller öka uppskattningarna för nästa period.</li>
</ol>
Finance minskar inte automatiskt de prognostiserade uppskattningarna. Därför är det en bra idé att skapa en original prognosmodell för fastprisprojekt och skapa en original plan för jämförelse när projektet har slutförts. 
<br></br> <strong>Obs!</strong> Om du väljer den här metoden ska du använda minst två prognosmodeller. En modell ska innehålla originalprognosen. För den andra modellen ska du kopiera prognostransaktioner från en annan modell. Den här metoden gäller endast för fastpris- och investeringsprojekt.</td>
</tr>
<tr class="odd">
<td>Resterande budget</td>
<td>I den här metoden används en resterande budgetmodell för att beräkna kostnaden för att slutföra projektet. När du använder den här metoden läggs de faktiska kostnaderna och prognosbeloppen i den resterande budgetmodellen samman. Resultatet blir en total kostnad. Innan du använder den här metoden måste en resterande budgetmodell konfigureras för att dra av transaktioner utifrån faktiska transaktioner som registreras i systemet. På sidan <strong>Prognosmodeller</strong> kontrollerar du att fälten är markerade i gruppen <strong>Automatisk prognosreducering</strong>. Vanligtvis kopieras en resterande budget från en ursprunglig budget. När transaktioner registreras minskar transaktionerna i den resterande budgeten. Om du bestämmer dig för att den resterande budgeten måste justeras debiterar du prognostransaktionerna till den återstående budgeten. <br></br> <strong>Obs!</strong> Den här metoden kan endast användas om en prognosmodell är kopplad till uppskattningen.</td>
</tr>
<tr class="even">
<td>Som föregående uppskattning</td>
<td>Samma uppskattningsmetod som användes i föregående period tillämpas. Den här metoden kräver en prognosmodell om den föregående perioden kräver en prognosmodell.</td>
</tr>
<tr class="odd">
<td>Ange att kostnaden ska slutföras till noll</td>
<td>Vanligtvis används den här metoden innan uppskattningsprojektet tas bort. Den här metoden överensstämmer med de totala uppskattningarna med de faktiska transaktionerna som har bokförts och rensar kolumnen <strong>Kostnad för att slutföra</strong>. Den resulterande slutförandeprocenten är alltid 100 procent. Fältet <strong>Prognos</strong> är inte markerat för varje kostnadsrad som du skapar och den totala uppskattningen kopieras från den föregående kostnadsberäkningen. Den faktiska förbrukningen för uppskattningsperioden dras från kostnaden för att slutföra projektet. Den här metoden kräver ingen prognosmodell.</td>
</tr>
<tr class="even">
<td>Från kostnadsmall</td>
<td>Kostnaden för slutförandemetoden som har angetts i kostnadsmallen som är associerad med det valda uppskattningsprojektet används.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analysera projektet
På den mest grundläggande nivån används ett projekt för att gruppera transaktioner som registrerar kostnader och sedan bokföra kostnaderna i redovisningen. 

Vanligtvis är dessa transaktioner resultatet av affärsdokument, t.ex. tidrapporter, utgiftsrapporter, leverantörsfakturor eller lagertransaktioner. Livscykeln för ett projekt börjar vanligen med uppskattningar, prognoser och budgetar som hjälper till att planera och förutse projektets arbete och ekonomiska påverkan. När du analyserar ett projekt kan du utvärdera inte bara de transaktioner som inträffade under projektet, utan också riktigheten av dina uppskattningar och prognoser, utnyttjandegraderna för medlemmar i projektgruppen och projektets totala framgång.

### <a name="analyze-cash-flow"></a>Analysera kassaflöde

Använd kassaflödesövervakning för att granska både prognostiserade kassaflöden och faktiska kassaflöden för ett projekt. Du kan granska kassaflöden medan ett projekt pågår eller också kan du visa kassaflödena för ett avslutat projekt. 

Genom att övervaka kassaflödena kan du utvärdera ett enskilt projekt, använda rapporterna för att visa flera projekt och överföra projekt kassaflöden till kassaflödesprognoserna i redovisningen.

#### <a name="cash-inflow-forecasting"></a>Kassainflödesprognoser

Beroende på vilken inställning du har kan du prognostisera kassainflödet för ett valt projekt. Om projektdatumet är 5 mars 2012 och du fakturerar den 31 mars 2012, kan du prognostisera förfallodatum och förväntat betalningsdatum för försäljning.

-   **Projektdatum:** 5 mars 2012.
-   **Fakturadatum:** 31 mars 2012. Datumet bestäms utifrån fakturafrekvensen. I det här exemplet anger du fakturafrekvensen till den aktuella månaden. Därför faktureras alla transaktioner som är bokförda i mars månad den sista dagen i månaden.
-   **Förfallodatum:** 14 April 2012. Datumet bestäms utifrån de betalningsvillkor som har ställts in för projektet. I det här exemplet valde du betalningsvillkoren 14 dagar. Därför läggs 14 dagar till i fakturadatumet till förfallodatumet 14 april 2012.
-   **Förväntat betalningsdatum:** 27 April 2012. Det här datumet beräknas genom att addera antalet dagar i fältet **Allmänna buffertdagar** på sidan **Projektlednings- och redovisningsparametrar** till antal dagar i fältet **Individuella buffertdagar** på sidan **Projektkontrakt** och sedan lägga till summan till antalet dagar i fältet **Förfallodatum**. I det här exemplet angav du **3** i fältet **Allmänna buffertdagar** och **10** i fältet **Individuella buffertdagar**. Därför läggs 13 dagar till i förfallodatumet för att komma till förväntat betalningsdatum för försäljning den 27 april 2012.

De allmänna buffertdagarna kan antingen ersätta de enskilda buffertdagarna eller läggas till i de enskilda buffertdagarna:

-   Om du vill använda de allmänna buffertdagarna som ersättning för de enskilda buffertdagarna anger du det genomsnittliga antalet dagar mellan förfallodatum och faktiskt betalningsdatum för kunder.
-   Om du vill lägga till de allmänna buffertdagarna i de enskilda buffertdagarna anger du i fältet **Allmänna buffertdagar** din uppskattning för antalet dagar mellan dagen då kunden skickar betalningen och dagen då din organisation tar emot betalningen.

Ställ in enskilda buffertdagar i projektets kontrakt. Dagarna beräknas utifrån både förfallodatum för försäljningsfakturan och organisationens erfarenhet av en kunds betalningsmönster.

#### <a name="actual-cash-inflow"></a>Faktiskt kassainflöde

Faktiskt kassainflöde påminner om prognoser, men du kan börja med att göra beräkningar från det första fakturadatumet. Här följer ett exempel:

-   **Fakturadatum:** 2 mars 2012.
-   **Förfallodatum:** 16 mars 2012. Betalningsvillkoren har värdet 14 dagar.
-   **Förväntat betalningsdatum:** 29 mars 2012. Beräkningen består av tre allmänna buffertdagar och 10 individuella buffertdagar.

#### <a name="cost-forecasting"></a>Kostnadsprognos

Baserat på de dagar som har definierats kan kostnadsbetalningsdatumet skilja sig från projektdatumet. I det här fallet beräknas kostnaden för betalningsdatumet genom att antalet dagar från projektdatumet läggs till efter antalet dagar i betalningsvillkoren. 

Projektdatumet för transaktionen är till exempel 5 mars 2012 och följande betalningsvillkor har ställts in:

-   **Timmar:** aktuell månad ( **M** )
-   **Utgifter:** 14 dagar ( **D14** )
-   **Artiklar:** 30 dagar ( **D30** )

Baserat på dessa inställningar är betalningsdatumet för kostnaden för varje transaktionstyp:

-   **Timmar:** 31 mars 2012, som är den sista dagen i den valda månaden.
-   **Utgifter:** 19 mars 2012, som är 14 dagar efter transaktionsdatum.
-   **Artiklar:** 4 april 2012, som är 30 dagar efter transaktionsdatum.

> [!NOTE] 
> Förfallodatumet för inköpsordern är baserat på leverantörstransaktionen när projektinköpsordern skapas. Förfallodatumet avgörs inte av några standardinställningar. 

Kostnadsbetalningsdatumet beräknas inte på de aktuella buffertdagarna. När ett projekt har slutförts bokförs både kostnaden och försäljningen på resultatkontona när all kostnadsberäkning och fakturering är slutförd. 

När alla försäljnings- och leverantörsfakturor har slutförts kan du visa relationen mellan fälten på sidan **Kassaflöde** och fält på sidan **Projektutdrag**.

:::row:::
    :::column:::
        #### <a name="cash-flow-page"></a>Sidan kassaflöde
        - Kassainflöden 
        - Kassautflöden
        - Nettokassaflöden
    :::column-end:::
    :::column:::
        #### <a name="project-statements-page"></a>Sidan projektutdrag
        - Intäkt
        - Total kostnad
        - Bruttomarginal
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Granska kostnader

Du kan övervaka kostnaderna som organisationen ådrar sig under ett projekt på sidan **kostnadskontroll**. Genom att jämföra de ursprungliga budgeterade kostnaderna för projektet med de aktuella faktiska kostnaderna och utfästa kostnaderna kan du avgöra om projektet ska spåras, överskrida budget eller under budget. 

> [!NOTE] 
> När du använder sidan **kostnadskontroll** för att visa den aktuella statusen för projektkostnader använder du prognosmodellerna som valdes för ursprunglig och resterande budget. Om du väljer andra prognosmodeller när du beräknar kostnader blir det beräknade resultatet inte korrekt.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Visa de resterande budgeterade beloppen

Om **Resterande budget** väljs som kostnadskontrollmetod på sidan **Projektlednings- och redovisningsparametrar** beräknar sidan **Kostnadskontroll** kostnader som inte har bokförts som faktiska eller markerade som åtaganden. Särskilt beloppen på fliken **Allmänt** i den nedre fönstret **Kostnadskontroll** beräknas på följande sätt:

-   **Faktisk kostnad** – Det total belopp som har lagts ned på projektet för den valda kostnadsraden. Det faktiska kostnadsbeloppet beräknas på sidan med **redovisningsuppdateringar**.
-   **Bekräftade kostnader** – det extra belopp som den juridiska personen har åtagit sig att betala. De specifika utfästa kostnadsbeloppen beräknas på sidan **Utfästa kostnader**.
-   **Resterande budget** – beloppet för det ursprungliga budgeterade beloppet som fortfarande är tillgängligt för den valda kostnadsraden. Det resterande budgetbeloppet beräknas på **förhandsgranskningssidan för redovisning**.
-   **Totalkostnad** – summan av den faktiska kostnaden, utfästa kostnader och resterande budgetbelopp.

På sidan **Kostnadskontroll** på fliken **Avvikelse** kan du visa en jämförelse av den totala förväntade kostnaden med den ursprungliga budgeten. I jämförelsen visas eventuella skillnader mellan beloppen. Därför kan du se var informationen inte matchar. Avvikelsebeloppen beräknas på följande sätt:

-   **Ursprunglig budget** – det belopp som ursprungligen budgeterades för den valda kostnadsraden. Det ursprungliga budgetbeloppet beräknas på **förhandsgranskningssidan för redovisning**.
-   **Totalkostnad** – summan av den faktiska kostnaden, utfästa kostnader och resterande budget som rapporteras på fliken **Allmänt**.
-   **Avvikelse** – skillnaden mellan den totala kostnaden och den ursprungliga budgeten.
-   **Varians utifrån kvantitet** – den totala skillnaden mellan den ursprungliga prognosen och den totala prognosen. Denna skillnad kan uttryckas matematiskt som (total prognoskvantitet) × (ursprungligt genomsnittspris – totalt genomsnittspris). Den här beräkningen gäller endast för projekttimmar.
-   **Varians utifrån pris** – den totala skillnaden mellan den ursprungliga prognosen och den totala prognosen. Denna skillnad kan uttryckas matematiskt som (total prognospris) × (ursprunglig prognoskvantitet – totalt genomsnittspris). Den här beräkningen gäller endast för projekttimmar.

#### <a name="viewing-the-total-budgeted-amounts"></a>Visa de totala budgeterade beloppen

Om **Total budget** väljs som kostnads kontrollmetod på sidan **Projektledning och redovisningsparametrar** , sidan **Kostnadskontroll** beräknar de faktiska kostnaderna och de totala kostnaderna för projektet för att hjälpa dig att upptäcka någon skillnad mellan de två. Särskilt på sidan **Kostnadskontroll** beräknas beloppen i kolumnerna i den nedre rutan på fliken **Allmänt** på följande sätt:

-   **Total budgeterad kostnad** – det totala budgeterade beloppet för den valda kostnadsraden.
-   **Faktisk kostnad** – Det totala kostnaden för projektet hittills för de valda kostnadsraderna.
-   **Bekräftade kostnader** – Det total belopp som har bekräftats för den valda kostnadsraden.
-   **Varians** – skillnaden mellan summan av de faktiska och bekräftade kostnader och den totala kostnaden. Avvikelsen anger om ytterligare kostnader måste anges för totala budgeten.

På sidan **Kostnadskontroll** på fliken **Avvikelse** kan du visa skillnaden mellan den totala budgeten och den ursprungliga budgeten genom att se till att följande fält är:

-   **Ursprunglig budget** – det belopp som ursprungligen budgeterades för kostnadsraden. Det ursprungliga budget beräknas på **förhandsgranskningssidan för redovisning**.
-   **Total budgeterad kostnad** – den totala kostnad som ursprungligen budgeterades för kostnadsraden. Den totala budgeterade kostnaden beräknas på **förhandsgranskningssidan för redovisning**.
-   **Avvikelse** – avvikelsen för kostnadsraden. Det här beloppet beräknas genom att den totala kostnaden subtraheras från den ursprungliga budgeten.
-   **Varians utifrån kvantitet** – den totala skillnaden mellan den ursprungliga budgeten och den totala budgeten. Detta belopp beräknas genom att subtrahera de totala budgettimmarna från de ursprungliga budgettimmarna och sedan multiplicera differensen med den ursprungliga budgeterade självkostnaden. Denna skillnad kan uttryckas matematiskt som (ursprungligt budgeterat kostnadspris) × (ursprungliga budgettimmar – totala budgettimmar). Den här beräkningen gäller endast för projekttimmar.
-   **Varians baserat på pris** – Detta belopp beräknas genom att subtrahera de totala budgettimmarna från de ursprungliga budgettimmarna och sedan multiplicera differensen med det totala antalet förbrukade timmar. Denna skillnad kan uttryckas matematiskt som (totala förbrukade timmar) × (ursprungliga budgettimmar – totala budgettimmar). Den här beräkningen gäller endast för projekttimmar.

### <a name="analyze-utilization"></a>Analysera utnyttjande

Utnyttjandegraden är den procentandel av tiden som en arbetare utför fakturerbar tid eller produktivt arbete under en specifik arbetsperiod. Fakturerbara timmar är arbetarens timmar som kan debiteras en specifik kund. 

En arbetares utnyttjandegrad beräknas genom att antalet fakturerbara timmar divideras med antalet arbetstimmar under en angiven period. Om en arbetare till exempel har 30 fakturerbara timmar under en period och antalet arbetstimmar i samma period är 40, blir arbetarens utnyttjandegrad 75 procent. 

När du beräknar utnyttjandegrad för en arbetare kan du beräkna antingen fakturerbart pris eller effektivitetsgrad:

-   **Andel fakturerbar tid** – skillnaden mellan fakturerbara och icke fakturerbara timmar eller normtimmar.
-   **Effektivitetsgrad** – skillnaden mellan produktiva timmar och icke produktiva timmar eller normtimmar. Produktiva timmar är de timmar som arbetaren tillbringar med att bidra till ett visst projekt. Produktiva timmar faktureras vanligtvis till kunder utom när det gäller interna projekt. Icke-produktiva timmar faktureras aldrig till en kund.

Du beräknar användnings tarifferna på sidan **Timutnyttjande**. Beräkningarna bygger på standardinställningar. De här inställningarna anger också hur timmar beräknas genom att fördela **utnyttjande** eller **börda** för varje projekttyp. Detta gäller beräkningar av andel fakturerbar tid och beräkningar av effektivitetsgraden.

-   **Utnyttjande** – timmar som rapporteras för den valda projekttypen beaktas alltid för fakturerbarheten eller effektivitetsutnyttjande.
-   **Börda** – timmar som rapporteras för den valda projekttypen beaktas alltid för icke fakturerbarheten eller icke effektivitetsutnyttjande.
-   **Enligt radegenskap** – radegenskaperna för en viss timtransaktion avgör om timmarna ska beaktas för fakturerbar tid eller för effektivitetsutnyttjande.
-   **Ej inkluderad** – timmar är inte en faktor i beräkningen av fakturerbarheten eller effektivitetsutnyttjande.

På sidan **Timutnyttjande** kan du förutom den totala utnyttjandegraden i procent för en arbetare eller ett projekt visa det antal timmar som använts för att beräkna utnyttjandegraden för följande typer av timmar:

-   **Ej inkluderade timmar** – de här timmarna ingår inte i timutnyttjande.
-   **Inkluderade timmar** – dessa timmar beräknas genom att du lägger till nyttjande tider och ej fakturerbara timmar. Dessa timmar ingår i utnyttjandegraden.
-   **Ej fakturerbara timmar** – om du beräknar en andel fakturerbar tid är de här timmarna samma timmar som inte debiterbara timmar. Om du beräknar en effektivitetsgrad är timmarna samma timmar som icke-produktiva timmar.
-   **Nyttjande timmar** – om du beräknar en andel fakturerbar tid är de här timmarna samma timmar som debiterbara timmar. Om du beräknar en effektivitetsgrad är timmarna samma timmar som produktiva timmar.

När du beräknar utnyttjandegrad för en arbetare kan du använda normal timmar eller inkluderade timmar. Om du använder inkluderade timmar måste du se till att arbetare registrerar hela sin arbetstid för tidrapportsperioder, eftersom beräkningen uttrycks i procent av timmar som anges. När du beräknar timutnyttjande för ett projekt, projektkontrakt, kundpost eller kategori måste du använda inkluderade timmar för beräkningen.

### <a name="review-project-statements"></a>Granska projektutdrag

Du kan skapa ett projektutdrag för att visa en snabb bild av förloppet av ett projekt. När du kör ett projektutdrag kan du ange kriterier som används för att beräkna kontoutdraget genom att göra val på fliken **Allmänt** på sidan **Projektutdrag**. Du kan välja att ta med eller utelämna följande information:

-   Projekttyper
-   Transaktionstyper
-   Projektdatum/redovisningsdatum
-   Data

När utdraget har beräknats kan du visa följande information på de olika flikarna på sidan **Projektutdrag** :

-   **Allmänt** – allmän information om projektets grundläggande struktur för vinst och förlust.
-   **Vinst och förlust** – information om upplupna intäkter.
-   **PIA** – information om saldon för PIA-konton.
-   **Förbrukning** – information om timmar, artiklar, utgifter och lönetransaktioner.
-   **Faktura** – information om fakturor och à conto-fakturering.
-   **Timtariff** – Timtariffer för timmar som har bokförts på intäkts- och kostnadskonton.


[!INCLUDE[footer-include](../includes/footer-banner.md)]