---
title: Nyheter eller ändringar i Project Service Automation version 3
description: I den här artikeln finns information om vad som är nytt och ändrat i Project Service Automation version 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d076e270f426131119eab097e7f359c228edb51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926614"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Nyheter eller ändringar i Project Service Automation version 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



I den här artikeln finns information om ändringar av användargränssnittet, funktioner och terminologi i Project Service Automation mellan version 2 eller version 1 och 3.

## <a name="project-scheduling"></a>Projektscheman
Projektschemat som kallades den uppdelade arbetsstrukturen (WBS) i tidigare versioner har bytt namn till schema och tillgås genom att klicka på fliken **schema**. 

![Projektschema.](media/psa-schedule-01.png)

Nu har schemat en ny yta för interaktioner som både är moderna och tillgängliga. Den underliggande schemaläggningsmotorn för Project Service Automation har inte ändrats. Med kontrollknapparna i verktygsfältet på schemats rutnät kan du interagera med schemat som liknar den tidigare versionen av Project Service Automation. Ytterligare ändringar i schemat är:

- **Gantt-schema** Gantt-diagrammet är inte längre tillgängligt. En ny Gannt-visualisering kommer att returneras vid en senare uppdatering.
- **Kolumnrubriker** – du kan dölja kolumnrubrikerna i rutnätet genom att klicka på indikatorn bredvid kolumnrubriken. 
- **Kolumner** – du kan visa dolda kolumner genom att klicka på **Lägg till kolumn**. 
- **Transaktionskategori** - En sökning av **transaktionskategori** har lagts till i schemarutnätet och visas som standard. 
 
## <a name="project-templates"></a>Projektmallar
Följande ändringar har gjorts i projektmallfunktioner.

### <a name="create-a-project-template"></a>Skapa projektmall 
Du kan skapa en projektmall i version 3, liknande den tidigare versionen av Project Service Automation. Mallen kan endast innehålla ett schema och schemat kan innehålla tilldelningar, men de är inte obligatoriska. Om schemat har tilldelningar kan de bara vara för generiska resurser. Du kan generera resurskrav för generiska resurser, men de kan inte bokas med verkliga resurser i mallen. Du kan inte boka en verklig resurs till ett team i en mall. 

### <a name="create-a-template-from-an-existing-template"></a>Skapa en mall utifrån en befintlig mall
När du skapar en ny projektmall från en befintlig mall i Project Service Automation version 3 händer följande: 

- Källprojektets schema kopieras till mallen. 
- Generiska resurser kopieras till teamet och eventuella allmänna resurstilldelningar kopieras över. Krav för generiska resurser kopieras inte över. 

### <a name="create-a-template-from-an-existing-project"></a>Skapa en mall utifrån ett befintligt projekt
När du skapar en ny projektmall från ett befintligt projekt händer följande: 

- Källprojektets schema kopieras till mallen. 
- Generiska resurser kopieras till teamet och eventuella generiska resurstilldelningar bevaras. Krav för generiska resurser kopieras inte över.    
- Namngivna resurser, både tilldelade och otilldelade, tas bort från teamet och ersätts med generiska resurser.
- Om det finns någon, tas kundinformationen bort. 
- Om det finns några referenser till offerter och kontrakt tas de bort. 

### <a name="create-a-project-from-a-template"></a>Skapa ett projekt från en mall
I Project Service Automation version 3 när du skapar en ny projektmall från en befintlig mall händer följande:

- Schemat, teamet och tilldelningarna kopieras till det nya projektet.   
- Startdatum är antingen kopieringsdatum eller datum som användaren valde.   
- För alla generiska gruppmedlemmar med resurskraven i mallen kopieras eller genereras inte kraven automatiskt. Du måste skapa dem. 

## <a name="copy-a-project"></a>Kopiera ett projekt
I Project Service Automation version 3 när du kopierar ett projekt händer följande: 

- Det uppskattade startdatumet kopieras men kan ändras.  
- Projektschemat och uppgifter kopieras. 
- Generiska resurser och deras tilldelningar kopieras. Resurskrav för generiska resurser kopieras inte. Du måste skapa dem igen. 
- Verkliga resurser och deras tilldelningar kopieras inte. De ersätts i stället av generiska resurser. 
- Faktiska värden kopieras inte till det nya projektet. 

## <a name="move-a-scheduled-project"></a>Flytta ett schemalagt projekt
När du flyttar schemat för ett befintligt projekt händer följande: 

- Uppgiftsdatum flyttas automatiskt till motsvarande rörelseperiod. 
- Tilldelade generiska resurser förblir tilldelade.   
- Om de genereras innan projektet flyttas måste kraven för den generiska resursen vara desamma och inte automatiskt återskapas. Du måste generera dem på nytt för att de nya tilldelningarna ska kunna visas på samma vis som uppgiftsrörelsen. 
- Tilldelningar i verkliga resurser ändras så att de överensstämmer med uppgiftens datumrörelse. Bokningar på verkliga resurser ändras inte. Du måste ändra bokningarna med hjälp av vyn avstämning. 
- Gruppresurser med bokningar men inga tilldelningar ändras. 
- Faktiska värden flyttas inte 

## <a name="estimates"></a>Beräkningar
Beräkningar har delats upp i två flikar **Resurstilldelning** och **Beräkningar**. Fliken **resurstilldelning** innehåller en insatsberäkning och visar resurstilldelningarna för uppgifterna i en tidsfasad vy. Du kan redigera beräkningarna utifrån vad schemaläggningsmotorn har skapat.

![Fliken Resurstilldelningar visar insatsberäkningar och resurstilldelningar för uppgifter.](media/resource-assignments-tab-02.png)

På fliken **Beräkningar** visas kostnads- och försäljningsbeloppen för resurstilldelningar. Beloppen är skrivskyddade. Kostnads- och försäljningsprissättning styrs nu från tilldelningar av gruppmedlemmar i schemat. Det innebär att om du har en uppgift utan tilldelning visas uppgiften under den icke tilldelade bucket. Detta innebär också att utan **roll**, som är en standarddimension för prissättning, visas ingen uppskattad kostnad eller försäljning om du har en kund eller ett kontrakt/offert som är associerad med projektet. 

![Fliken Beräkningar visar kostnads- och försäljningsbelopp.](media/estimates-tab-03.png)
  
Kategorin stöds även för uppgifter i schemaläggningsvyn. Gruppering efter kategori i tidsfasvyn av beräkningar ger en bättre upplevelse, särskilt när du också har beräkningar av utgifter i projektet. Utgiftsberäkningar anges med hjälp av ett rutnät på en separat flik. 

Utgiftsberäkningar kan anges i rutnätet på fliken **Utgiftsberäkningar**. 

![Fliken Utgiftsberäkningar visar rutnät för utgiftsberäkningar.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Resurshantering
I Project Service Automation version 3 med det nya enhetliga gränssnittet för klient och förändringar i relationen mellan bokningar och tilldelningar, bemanna ett projekt med generiska eller verkliga resurser, har ändrats dramatiskt från version 2 och version 1. Begreppen för bokningsbara resurser, både **verkliga** och **generiska**, förblir emellertid samma, och även gruppmedlemmar, krav, tilldelningar och bokningar.   

![Använda resursväljare.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Tilldela en verklig bokningsbar resurs 
I Project Service Automation version 3 är boknings- och uppgiftstilldelningar inte lika sammanlänkade som i tidigare versioner av Project Service Automation. Du kan använda grupprutnätet för att boka **verklig** gruppmedlem på samma sätt som på marknaden.

Med resursväljaren i schemat kan du välja vilken gruppmedlem som skapats i teamvyn och sedan tilldela dem till uppgifter. Du kan fortsätta att tilldela dem uppgifter, även efter sina bokningar. Använd fliken **avstämning** om du vill stämma av gruppmedlemmar som har olika skillnader i bokningar och tilldelningar.

Resursväljaren kommer att visa gruppmedlemmarna för projektet. Du kan även använda resursväljaren om du vill söka efter och visa andra bokningsbara resurser som inte ingår i projektteamet. Du kan tilldela dem till en uppgift och de blir en del av projektteamet. Du måste boka dem med hjälp av fliken **schemaläggningstavla** eller **avstämning**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Tilldela en generisk bokningsbar resurs till en uppgift och ett projektteam och sedan uppfylla en verklig resurs via schemaläggningstavlan 
I Project Service Automation version 3 används inte funktionen generera team för allmänna resurser. I stället kan du skapa och direkt tilldela en generisk resurs från schemat genom att skriva namnet på den generiska resursen i resurscellen i schemat. Du kan också välja resursikonen i cellen och sedan med resursväljaren ange namnet på den generiska resurs som du vill skapa. Då öppnas en snabbregistreringspanel där du kan ange roll och organisationsenhet för den generiska resursgruppmedlemmen. När du har skapat resursen tilldelas den uppgiften och du kan fortsätta att tilldela den generiska resursen till andra uppgifter i schemat.    
 
När du har tilldelat resursen alla relevanta uppgifter kan du skapa ett resurskrav och sedan utföra den genom att direkt boka med **schemaläggningstavlan** eller genom att skicka en resursbegäran. Du kan också lägga till generiska resurser direkt i rutnätet för gruppmedlemmen. 

Generiska resurser läggs till i projektteamet utan resurskrav och med start- och slutdatum för projektet tills resurskravet skapas. Om du vill skapa ett krav markerar du resursen och klickar på **Skapa**. Kravlänken visas nu och de begärda timmarna fylls i med de tilldelade timmarna. Du kan klicka på länken för att öppna och uppdatera kravet.
  
När bokningen är slutförd och helt uppfylld av en namngiven resurs ersätts den generiska resursen med den namngivna resursen och tilldelningen av schemat uppdateras med den namngivna resursen. 

Föreslagna resurser för krav lagras nu på en flik i stället för i ett separat avsnitt.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Flera namngivna resurser uppfyller en generisk resurs
När ett krav uppfylls med flera resurser blir den generiska resursen kvar på teamet och tilldelas uppgiften. De namngivna gruppmedlemmar som är bokade är inte tilldelade som en del av befattningen. Projektledaren kan tilldela arbetet enligt de verkliga resursernas behov.  Vyn **avstämning** ger en sammanfattning av bokningarna över flera resurser till flera uppdragstilldelningar. Detta görs inte automatiskt eftersom du i något scenario är mer komplicerat än när du har ett paket med uppgifter som utgör behovet, hur projektledaren vill tilldela, måste antas av systemet. Eftersom systemet inte kan tolka vad som är troligt är det att antagandena är annorlunda än avsett och att ett felaktigt eller oförutsägbart resultat inträffar. Det förutsägbara resultatet är att den allmänna resursen fortfarande är tilldelad tills projektledaren har tilldelat resurser med hjälp av läget **avstämning**.

### <a name="reconciliation"></a>Avstämning
Fliken **Avstämning** visar bokningarna och alla tilldelningar för varje projektmedlem i gruppen. Vyn visar timmar i celler som kan representera tidpunkter från månader till dagar. Den här vyn tillåter projektledarna att avstämma gruppmedlemmarnas bokningar och deras tilldelningar för sina projektteam. Detta är praktiskt eftersom bokningar och uppgiftstilldelningar inte är tätt sammansatta, vilket gör det lättare att planera ett projekt. 

![Fliken Avstämning visar bokningarna och tilldelningar för varje projektgruppmedlem.](media/resource-reconciliation-tab-06.png)

För varje resurs får vyn en skillnad mellan gruppmedlemmens bokningar och en sammanslagning av deras uppgiftstilldelningar och följande två skillnader som kan uppstå med bokningar och tilldelningar i ett projekt: 

- **Underskott för bokning** – Underskott för bokning uppstår om en resurs har fler tilldelningar än bokningar. Eftersom denna kapacitet inte har reserverats kan en projektledare korrigera detta genom att utöka resursens bokningar så att underskottet täcks. 
- **Överflödiga bokningar** – Överflödiga bokningar inträffar när en resurs har bokats i projektet men inte tilldelats uppgifter.  Detta kan vara en acceptabel förekomst om till exempel resursen har bokats före en uppgiftstilldelning. I andra fall kan det emellertid hända att resursen inte är planerad att tilldelas och PM bör annullera resursbokningarna så att kapaciteten kan användas för ett annat projekt. 

När du har uppgiftstilldelningar för en resurs utan bokningar (underskott för bokning) kan du välja samlad underskott för bokning och sedan välja **utöka bokning**. Härifrån kan du visa den bokning som behövs för att lösa resursens underskott och deras tillgänglighet. 
 
## <a name="time-and-expense"></a>Tid och utgift
Det här avsnittet innehåller information om förändringar av tid, utgifter och godkännande i version 3 Project Service Automation. Som en del av Dynamics 365 Project Service Automation-lösningen har funktionen **tidspost** uppdaterats för att använda ramverk för enhetligt gränssnitt. Detta ger leverans av konsistent, enhetligt användargränssnitt som följer responsiv design för optimal visning på alla skärmstorlekar och enheter. 

### <a name="landing-page"></a>Landningssida
Den icke-utökningsbara anpassade tidspostupplevelsen är inaktuell i version 3. I stället finns nu en utökningsbar och tillgänglig inbyggd rutnätsupplevelse. Du kan komma åt tidspostens funktion med hjälp av webbplatsöversikten till vänster. Med den här ändringen kan du inte längre ange tid för en vecka i taget. I stället måste du skapa en tidspost för varje dag i rutnätet. När några tidsposter har skapats kan användarna masskapa tidsposter med funktionen **kopiering** vilket förklaras senare i denna artikel. 

![Landningssida för tidspost.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Skapa nya tidsposter 
Klicka på **Nytt** i menyfliksområdet om du vill öppna en sida för att snabbregistrera tidspost där du anger varaktighet i minuter, timmar eller dagar. Det gör du genom att endast börja skriva in h, m eller d tillsammans med kvantiteten.  

![Snabbregistrering för tidspost.](media/quick-create-time-entry-08.png)

Uppslagsfält säkerhetskopieras med systemvyer. När du t.ex. anger projektinformation anges fältet **projektuppgifter** som standard till vyn **Mina öppna projektuppgifter**. Om du vill skapa tidsposter för uppgifter som inte är tilldelade till användaren klickar du på **ändra vy** i uppslaget och markerar **Alla aktiva projektuppgifter**. När tidsposten har skapats och visas i rutnätet kan du redigera alla radvärden direkt i rutnätet.  

### <a name="bulk-createcopy"></a>Masskapa/kopiera 
När du har skapat några tidsposter kan du använda kopieringsfunktionen för att masskapa ytterligare tidsposter. Klicka på **Kopiera** så att dialogrutan **Kopiera** öppnas. I **Från period: startdatum** anger du i vilket datumintervall som tidsperioder måste kopieras från. I **Till period: startdatum** anger du det datum då tidsposter ska skapas. Klicka på **kopiera** för att kopiera tidsposterna till motsvarande dag i veckan angivet i **Till-period**. Till exempel kommer måndagens tidspost från förra veckan att kopieras till måndag för den vecka som anges under **Till-period**. 

![Kopiera många tidsposter samtidigt.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importera data 
Tilldelningar och Exchange följer samma användargränssnittsmönster, vilket gör att användaren kan ange ett datumintervall från vilket bokningar behöver importeras. Du måste sedan uttryckligen välja de bokningar som ska kopieras till tidsposter **utkast**. I version 3 kan du inte längre se mönstret för **föreslagna** tidsposter i rutnätet och kalendern.  

### <a name="change-in-calendar-control"></a>Ändra i kalenderkontroll
I version 3 har vi flyttat från den anpassade kalenderkontrollen och använder UC-kalendern för att visa tidsposter för veckan. Med den här kalendern kan du visa dag, vecka och månad. 

> [!NOTE]
> En begränsning i kalendern är att den här kontrollen inte stöder åtgärder för enskilda kalenderobjekt. Du kan till exempel inte markera ett eller flera kalenderobjekt och skicka eller ta bort dessa objekt. Om du klickar på ett kalenderobjekt öppnas sidan **Entitet för tidspost** för ytterligare åtgärder. 

### <a name="extensibility"></a>Utökningsbarhet
**Samla in data på anpassade fält endast i tid- och utgiftsentiteter** - tidspost använder ett redigerbart rutnät, ett skrivskyddat rutnät och kalenderkontroller från plattformen. Alla de här kontrollerna är inbyggda och stöder därför anpassningar. I Project Service Automation version 3 kan du lägga till fler anpassade fält, skapa uppslagsfält och säkerhetskopiera dem med anpassade vyer. Du kan även ange anpassad affärslogik utifrån valda värden i anpassade fält.  

**Samla in data på anpassade fält i tid- och utgiftspost och sprida dem via entiteter som stöder inlämnings- och godkännandeflöden** – den vanligaste bearbetningen av tidsposterna visas i följande diagram.

![Bearbetning av flöde för tidspost.](media/process-time-entries-10.png)

Om affärskrav föreskriver att tids- och utgiftsentiteter måste hämta anpassade prissättningsdimensioner och sprida värden som anges med en tid och en postresurs i den anpassade dimensionen för prissättning via alla entiteter i föregående bild, se [Konfigurera anpassade fält som prissättningsdimensioner](set-up-pricing-dimensions.md)

Om du vill stödja affärskrav där tids- och utgiftsentiteter måste hämta anpassade icke-prissättningsdimensioner och sprida värdena, kan du använda inställningarna för prissättningsdimensioner och uttrycka de anpassade dimensionerna som prissättningsdimensioner utan kostnad eller faktureringskostnader. Ett annat scenario är att lägga till ett anpassat fält i varje entitet med samma fältnamn för alla entiteter. Anpassade plugin-program kan skapas för att relatera poster i entiteter som deltar i överförings-/godkännandeflödet med hjälp av entiteterna transaktionsursprung och transaktionsanslutning.  

### <a name="delegate-time-and-expense-entry"></a>Delegera tids- och utgiftspost
Common Data Service-plattformen stöder inte en användare som personifierar en annan, vilket innebär att det inte finns något stöd för delegerade tids- och utgiftsposter i version 3 av Project Service Automation. Partner och kunder har emellertid en lösning för att aktivera stöd för medhjälpande med delegerade tidspostupplevelser i version 3. Detta är endast en lösning och är inte en komplett lösning, så det är viktigt att du förstår begränsningarna och bara använder den här metoden om begränsningarna är acceptabla. 

> [!IMPORTANT]
> Den här informationen bör endast betraktas som förslag till vägledning för anpassad implementering av en partner/kund. Produktteamet kommer inte att erbjuda formellt stöd för den här funktionen via någon av våra supportkanaler.

### <a name="customization-details"></a>Anpassningsinformation 
Med anpassning kan du lägga till **Bokningsbar resurs** för att skapa och redigera upplevelser, vilket gör att en användare kan agera som ombud genom att ändra fältet **Bokningsbar resurs** till en annan användare som tids- och utgiftsposterna behöver för att registreras. Följande steg omfattar delegering av tidsposter. Samma information gäller delegering av utgiftsposter. 
 
1.  Kontrollera att den delegerade användaren har global säkerhetsåtkomst för projekt och projektuppgifter. 
1.  Eftersom **Bokningsbar resurs**, som är ett fält i entiteten **Tidspost** inte visas på sidan **snabbregistrering** måste du lägga till det.

    -eller-

    Skapa en anpassad vy som inkluderar kolumnen **Bokningsbar resurs** om du endast vill visa tidsposter som har skapats för resursen. Publicera anpassningarna för appmoduldesignern för att den här vyn ska visas under **visningsväljare** på sidan **tidsposter**. Det finns två plugin-program som hanterar inställning av ansvarig för tidsposter som inte är projektrelaterade:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Skapa ett nytt plugin-program för att skriva över fältet **ansvarig** till den användare som är tilldelad i fältet **Bokningsbar resurs**. Använd samma **Körningsstadium** som out-of-band (OOB) plugin-program (före verifiering) och använd en **körning av order** som är högre än OOB-plugin-program (större än 1). Detta innebär att det anpassade plugin-programmet körs efter OOB-plugin-programmen.  
 
### <a name="end-user-experience"></a>Slutanvändarerfarenhet
1.  När du skapar en tidspost på sidan snabbregistrering anger du informationen om projektet och projektuppgiften och väljer sedan användaren i fältet **Bokningsbar resurs** som tidsposterna ska registreras för. 
2.  Som standard används den inloggade användaren i det här fältet, men när användaren åsidosätter det här fältet skapas en tidspost för den valda **Bokningsbara resursen**.
3.  När du skickar tidsposterna som du har skapat för de här posterna placeras posterna i kö för godkännare i projektet som förväntat. 
4.  När du återkallar tidsposterna som skapats för den andra användaren returneras tidsposterna till status **utkast** med fältet **Bokningsbar resurs** till den andra användaren. 
5.  Om du vill kan du växla till den anpassade vyn för att filtrera tidsposter som har skapats för den andra användaren. 
 
### <a name="limitations"></a>Begränsningar
Funktionerna **Kopiera** och **Importera** fungerar endast i samband med den inloggade användaren. Det innebär att det inte är möjligt att kopiera eller importera tidsposter som skapas för den användare som är inloggad som bokningsbar resurs.

Tidsposter som inte finns i ett projekt skickas för godkännande till chefen för bokningsbar resurs endast om steg 4 i avsnittet **anpassningsinformationen** ovan är slutförd. Annars kommer tidsposter som inte är projektrelaterade att skickas till den inloggade användarens chef på ett felaktigt sätt. 

### <a name="other-changes"></a>Andra förändringar 
Funktionen **bokningar och uppgifter** har tagits bort. 

## <a name="multidimensional-pricing"></a>Flerdimensionell prissättning
Om du vill maximera flexibiliteten och uppfylla olika affärskrav stöder version 3 av Project Service Automation diskret tillämpning av uppsättningar för prissättningsdimension till kostnader och faktureringskostnader. Dimensionsvärden kan anges som standard och sedan spridas över kostnads- och prissättningsprocessen från resursprofilering till tidspost till projektets verkliga värden. Kundspecifik konfiguration och ändring eller tillägg använder standardinfrastruktur för anpassningsbarheten.

Project Service Automation levererar en standarduppsättning med prissättningsdimensioner och roller och resursenheter och gör det möjligt att ställa in priser och kostnader för varje kombination av roll och organisationsenhet.

För kunder av Project Service Automation som vill fortsätta att använda de här fälten som prissättningsdimensioner i version 3 kommer det inte att finnas någon ändringsbara förändring. Du kan fortsätta att använda Project Service Automation som vanligt. Om du däremot behöver ett pris eller en kostnad för dina resurser med hjälp av andra ytterligare attribut kan du version 3 för att lägga till anpassade prissättningsdimensioner för Project Service Automation. Utvidgningen av anpassade prissättningsdimensioner är en komplicerad konfigurationsupplevelse. 

## <a name="quotes-and-contracts"></a>Offerter och kontrakt
I version 3 av Project Service Automation har olika aspekter av installation och hantering av offerter och kontrakt ändrats. I följande avsnitt finns mer detaljerad information.

### <a name="set-up-chargeability-options"></a>Skapa debiterbara alternativ
I version 1 och 2 gjordes en debiterbar konfiguration för roller och kategorier för specifika offerter och kontrakt med hjälp vyn **debiteringsbarhet** för debitering som fanns i den övre navigeringen på en offertrad eller en kontraktrad. Du kunde även ange priser för de här rollerna och utgiftskategorierna.

Från och med version 3 görs en inställning av debiteringsalternativ per roll- och utgiftskategori på offert- eller kontraktradnivån. Prissättningsinställningar är separat från debiterbar konfiguration. Du kan söka efter **debiterbara roller** och **debiterbara kategorier**  som flikar på sidorna **offertrad** och  **kontraktrad** utan att behöva använda toppnavigering.

![Debiterbara roller.](media/chargeable-12.png)
 
Inställningarna för de debiterbara rollerna och de debiterbara kategorierna utnyttjar även den medföljande redigerbara rutnätkontrollen. För varje roll och kategori är de alternativ som stöds för faktureringstyp under faserna Offert och Avtalande oförändrade från tidigare versioner som **debiterbara** och **icke-debiterbara**. **Kostnadsfritt** är inte en typ som stöds under faserna Offert eller Avtalande. **Kostnadsfritt** stöds endast under godkännande av tid eller utgift.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Skapa och redigera anpassad prissättning för en Project Service Automation-offert och projektkontrakt
I version 1 och 2 används anpassat prissättningslista för specifika offerter och kontrakt med hjälp av **redigera priser** i vyn **debiterbar**. Vyn **debiterbar** finns i den övre navigeringen på en offertrad eller på en kontraktrad. Du kunde även ange priser för de debiterbara alternativen för roller och utgiftskategorierna.

Från och med version 3 kan du skapa och använda en anpassad projektprislista på en Project Service Automation-offert och Project Service Automation-projektkontrakt har delats upp från den debiterbara installationen. Project Service Automation offert och Project Service Automation projektkontrakt kontrakt har en ny flik med namnet **Prislistor för projekt**. På den här fliken visas en associerad vy över alla prislistor för projekt som är kopplade till Project Service Automation-offerten eller projektkontraktet. Om du vill skapa en anpassad prislista från en befintlig prislista som redan associerats med projektofferten eller kontraktet klickar du **Skapa anpassad prissättning**. Då skapas en kopia av alla associerade prislistor och bifogar dem i offerten eller kontraktet. Nu kan du öppna prislistan och redigera roll- eller utgiftskategoripris så att dessa prissättningsändringar endast gäller för den här offerten eller kontraktet. 
  
Följande bild är innan anpassade prislistor har skapats.

![Före anpassade prislistor.](media/before-custom-price-lists-13.png)

Följande bild är efter anpassade prislistor har skapats.

![Efter anpassade prislistor.](media/after-custom-price-lists-14.png)

> [!NOTE]
> En kort fördröjning kan inträffa när du klickar på **Skapa anpassad prissättning** till när den anpassade prislistan skapas. Vi rekommenderar att du uppdaterar rutnätet i stället för att klicka flera gånger. En anpassad prislista skapas om namnet på den associerade prislistan har offertnamnet eller projektkontraktsnamnet bifogat det.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
