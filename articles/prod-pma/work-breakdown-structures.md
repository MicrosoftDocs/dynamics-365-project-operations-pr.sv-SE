---
title: Översikt över uppdelad arbetsstruktur
description: En uppdelad arbetsstruktur (WBS) är en beskrivning av det arbete som ska utföras för ett projekt. Det är en hierarki av uppgifter som representerar projekt teamets förståelse för arbetsuppgifterna samt storlek, kostnad och varaktighet för varje komponent eller uppgift.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0cfcc27c69695fc6fe897e798b2831528833e6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085515"
---
# <a name="work-breakdown-structures-overview"></a>Översikt över uppdelad arbetsstruktur

[!include [banner](../includes/banner.md)]

En uppdelad arbetsstruktur (WBS) är en beskrivning av det arbete som ska utföras för ett projekt. Det är en hierarki av uppgifter som representerar projekt teamets förståelse för arbetsuppgifterna samt storlek, kostnad och varaktighet för varje komponent eller uppgift. En WBS kan ha tre huvudsakliga syften:

-   Beskriva uppdelning eller sammansättning av arbetet i uppgifter.
-   Planera projektarbetet.
-   Uppskatta kostnaden för varje uppgift.

Graden av detaljer i en WBS beror på vilken exakthet som krävs i uppskattningarna och vilken uppföljningsnivå som krävs för dessa uppskattningar. Projekt som har mycket låg tolerans för förseningar i schemat eller kostnaden kräver vanligen en mer detaljerad WBS och du måste också ha en noggrann uppföljning av arbetsförloppet och WBS. Den här typen av projekt är vanligt inom bygg- och teknikindustrin. 

Projekt i branscher som media och reklam, program vara och IT-infrastruktur brukar vara en av de olika typerna, och produktiviteten är relativ i förhållande till erfarenheten och kompetensen hos den person som utför uppgiften. Därför använder de här branscherna en WBS för att få en tillnärmning av projektets storlek och inte för att följa upp projektets status utförligt. 

Att bygga en WBS är en intensiv process som vanligtvis utförs under en längre tid och som kräver samarbete och information från många olika personer. I den här ämne beskrivs hur du kan använda WBS-förbättringar för att uppfylla dina krav på uppskattningar och spårning.

## <a name="prerequisites-for-creating-a-wbs"></a>Förhandskrav för att skapa en WBS
Om du vill skapa en WBS måste du kunna skapa ett arbetsschema och uppskatta kostnaden för arbetet.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Förutsättningar för att skapa ett arbetsschema

Om du vill använda hela schemaläggningsfunktionerna i strukturfunktionerna utför du följande inställningar:

1.  Skapa en standardkalender och en projektkalender:
    1.  Klicka på **Projektledning och redovisning** &gt; **Inställningar** &gt; **Projektledning och redovisningsparametrar** &gt; **Schemaläggning**. I fältet **standardkalender för arbete** anger du en standardkalender. Det här blir standardarbetskalendern för alla nya projekt som skapas.
    2.  Du kan ändra standardkalendern för ett visst projekt. Klicka på projektets informationssida och snabbfliken **Projektgrupp och schemaläggning** uppdatera fältet **Schemalägga en kalender** genom att välja en annan kalender.

2.  Ange standardarbetsdagar och arbetstid. Kalendern som du anger som arbetskalender för projektet kommer att användas i WBS för att fastställa följande information:

-   Arbetsdagar och semestrar
-   Antalet arbetstimmar på en dag

Om du vill ange arbetsdagar och arbetstider för en kalender eller skapa en ny kalender klickar du på **organisationsadministration** &gt; **vanliga** &gt; **kalendrar**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Förutsättningar för att beräkna kostnaden för arbetet

Om du vill använda alla funktioner för uppskattning av WBS i strukturlistan bör du ange kostnaderna och försäljningspriset för arbetare, kategorier av arbete, utgifter och avgifter samt artiklar.

-   Om du vill ange kostnads- och försäljningspris för kategorierna arbete, kostnader och avgifter klickar du på **Projektledning och redovisning** &gt; **Inställningar** &gt; **Priser**.
-   Om du vill ange kostnads- och försäljningspris för artiklar använder du sidan **handelsavtal** för varje objekt på listsidan **för frisläppta produkter** i produktinformationshantering.

## <a name="creating-a-wbs"></a>Skapa en WBS
När du skapar en WBS ingår tre aktiviteter:

1.  **Arbetsuppdelning** – skapa en uppdelning av arbete till hanterbara segment och uppgifter.
2.  **Arbetsschema** – uppskatta den tid som krävs för att slutföra en uppgift, ange aktivitetsberoenden och ange start- och slutdatum för aktiviteterna.
3.  **Kostnadsuppskattning** – uppskatta kostnaderna för varje aktivitet.

I följande avsnitt beskrivs hur du kan använda WBS-funktionerna för de olika aktiviteterna.

### <a name="work-decomposition"></a>Arbetsuppdelning

Att skapa en uppdelning eller en delaktivitet är vanligtvis det första steget när du skapar en struktur. WBS-funktionerna i fungerar enligt följande grundläggande konstruktioner för arbete eller nedbrytning. 

**Projektets rotaktivitet** projektets rotaktivitet utgörs av sammanfattningsaktiviteten på den högsta nivån för ett projekt. Alla andra projektuppgifter som skapas under den. Namnet på rotuppgiften anges alltid till projektnamnet. Insats, datum och varaktighet för rotnoden sammanfattar värdena för uppgifterna under rotuppgiften. Du kan inte ändra rotnodens egenskaper eller ta bort den.

**Sammanfattning eller behållaraktiviteter** En sammanfattande uppgift är en uppgift som har underuppgifter eller ingående uppgifter under sig. En sammanfattningsuppgift har inte någon egen arbetsinsats eller utgift. Arbetsinsatsen och kostnaden för en sammanfattningsaktivitet är i stället summan av arbetsinsatsen och kostnaden för dess ingående aktiviteter. Det tidigaste startdatumet för de ingående uppgifterna används som startdatum för den sammanfattande uppgiften, och det senaste slutdatumet för de ingående uppgifterna används som slutdatum. Du kan ändra namnet på en sammanfattningsuppgift men du kan inte ändra egenskaper för schemaläggning för arbete, datum och varaktighet. Om du tar bort en sammanfattningsuppgift tas även alla dess ingående uppgifter bort. 

**Lövnodsuppgifter** en lövnodsuppgift representerar det mest detaljerade arbetspaketet i projektet. Lövnodsuppgift uppskattad insats, ett planerat antal resurser, planerade start- och slutdatum och en tid. 

Du kan utföra följande hierarkinivåer om du vill skapa en arbetshierarki eller en dispositionsåtgärd för ett projekt. 

**Ny uppgift** en ny uppgift som du skapar läggs automatiskt till under rotnoden och ett WBS-nummer tilldelas automatiskt uppgiften. WBS-numret visar uppgiftens nivå i hierarkin. För uppgifter på den första nivån under projektets rotaktivitet används ett numreringsschema på 1, 2, 3 och så vidare. För uppgifter under den första nivån används ett numreringsschema på 1.1, 1.2, 1.3 och så vidare. För varje nivå som läggs till under en tidigare nivå läggs en ny prickad serie med nummer till. 

För närvarande går det inte att anpassa WBS-numren. 

**Dra in uppgift** När du drar in en uppgift blir den underordnad den uppgift som föregår den. WBS-numret för den nya underordnade uppgiften räknas om automatiskt baserat på WBS-numret för den nya föräldern. Den överordnade uppgiften är nu en sammanfattning eller en behållaruppgift och kan därför bli en sammanslagning av uppgifter för komponenterna. 

> [!NOTE] 
> När du drar in aktiviteter under en aktivitet som var en lövnod före indraget, kan den nyligen skapade sammanfattningsuppgiften förlora sina egna datum, arbete och antal resurser. Nu används en sammanfattning av värdena för de nya uppgifterna. 

**Dra ut uppgift** När du drar ut en uppgift är den inte längre en del av den överordnade aktiviteten. WBS-nummer beräknas automatiskt om för att återspegla uppgiftens nya nivå i hierarkin. Arbetsinsatsen, kostnaden och datumen för uppgiftens föregående överordnade uppgiften för att exkludera den uppgiften. 

**Flytta upp och flytta ned** när du klickar på **Flytta upp** och **Flytta ned** kan du ändra aktivitetens placering inom dess överordnade hierarki. Uppgiftens position påverkar inte uppgiftens arbete, kostnad, datum eller varaktighet. Men WBS-numret beräknas automatiskt om för att återspegla uppgiftens nya position.

### <a name="schedule-estimation"></a>Schemalägg uppskattning

Schemalägga uppskattning är vanligtvis det andra steget när du skapar en WBS. Du bör genomföra en uppskattning av schema när du har skapat uppgifterna. Sidan **Uppdelad arbetsstruktur** i Finance har två avdelningar. Den övre rutan är avsedd att användas för att tidsplanera en uppskattning och i den nedre rutan finns fliken **Uppskattade kostnader och intäkter** som du kan använda för kostnadsuppskattning. 
**Beroenden mellan uppgifter** i en WBS kan du skapa en föregående relation mellan uppgifter. När du tilldelar föregående uppgifter till en uppgift kan den uppgiften starta först när alla föregående uppgifter har slutförts. Det planerade startdatumet för aktiviteten anges automatiskt till det senaste datumet för alla föregående aktiviteter. 

**Schemaläggning av uppgift** följande faktorer styr schemaläggningen av lövnodsuppgifter:

-   Föregångare
-   Insats
-   Antal resurser
-   Start- och slutdatum

Startdatumet för en lövnodsuppgift som saknar föregångare anges automatiskt till projektets planeringsstartdatum. En lövnodsuppgifts tid beräknas alltid som antalet arbetsdagar mellan dess start- och slutdatum. 

*<strong><em>Schemaläggningsregler</em></strong>* När automatisk schemaläggningshjälp är aktiverad gäller följande regler för schemaläggning av uppgifter för lövnodsuppgifter:

-   Start- och slutdatumen för en uppgift måste alltid vara arbetsdagar enligt projektets schemaläggningskalender.
-   Startdatum för en uppgift med föregångare anges automatiskt till det senaste slutdatumet för föregående uppgifter.
-   Arbetsinsatsen för en uppgift beräknas automatiskt enligt följande:

Antal personer × Varaktighet × Antal timmar under en vanlig arbetsdag i projektkalendern. 

I vissa fall kanske du vill avvika från dessa regler. Du kan inaktivera automatisk schemaläggning om du vill förhindra att Finance automatiskt ställer in eller korrigerar egenskaper för lövnodsuppgifter. När du anger information för en uppgift som orsakar en överträdelse av eventuella schemaläggningsregler visas en ikon för schemaläggningsfel för uppgiften. Om du inte vill att schemaläggningsfelen ska visas klickar du på **Schemaläggningsfel** för att inaktivera funktionen. 

> [!NOTE] 
> Värdena för en sammanfattnings- eller behållaruppgift fortsätter att beräknas som summan av värdena för komponentens uppgifter, oavsett om funktionen för automatisk schemaläggnings hjälp är aktiverad eller inaktiverad. 

**Åtgärda schemaläggningsfel** När funktionen för automatisk schemaläggnings hjälp är aktiverad uppstår inga schemaläggningsfel. Men om du stänger av automatisk schemaläggningshjälp och sedan slår på den senare kan ikoner för schemaläggningsfel visas i WBS. 

**Åtgärda schemaläggningsfel efter uppgift** När du dubbelklickar på ikonen för schemaläggningsfel för en viss uppgift visar en dialogruta alla schemaläggningsfel för den uppgiften. Du kan bestämma vilka schemaläggningsfel som ska åtgärdas för uppgiften. 

**Korrigera alla schemaläggningsfel** om du vill att Finance ska åtgärda alla schemaläggningsfel i WBS klickar du på **korrigera alla schemaläggningsavvikelser** i åtgärdsfönstret. 

> [!NOTE] 
> Den här funktionen kan orsaka stora ändringar av WBS. Felen korrigeras i följande ordning:

1.  Den uppskattade insatsen för alla aktiviteter ändras så att den motsvarar den kapacitet som har definierats i projektkalendern.
2.  Startdatum för varje uppgift ändras så att aktiviteten startar när alla föregående aktiviteter har slutförts.
3.  Startdatum för varje uppgift ändras för att ta bort luckor i startdatumen för föregående aktiviteter.

### <a name="cost-estimation"></a>Kostnadsberäkning

Som tidigare nämnts i det här dokumentet anger du kostnads beräkningen för varje lövnodsuppgift med hjälp av fliken **Uppskattade kostnader och intäkter** i det nedre fönstret på sidan för **uppdelad arbetsstruktur**. 

> [!NOTE] 
> Du kan inte ändra kostnadsberäkningen för en sammanfattning eller behållaruppgift. Kostnadsberäkningen för en sammanfattningsaktivitet är lika med summan av kostnadsberäkningen för dess lövnodsuppgift. Den uppskattade totala kostnaden för varje aktivitet beräknas som summan av de beräknade kostnadsbeloppen för följande transaktionstyper:

-   Arbete
-   Artikel eller material
-   Utgifter

En transaktionstyp **avgift** används för att uppskatta avgiftsbelagda intäkter. Den här transaktionstypen har ingen kostnadskomponent och beaktas därför inte när kostnaderna beräknas. 

En transaktionstyp **à conto** används för att registrera det kontrakterade försäljningsvärdet i en projekttyp med fast värde. Den här transaktionstypen beaktas inte heller när kostnader beräknas. 

När du uppskattar kostnader för arbete, material och utgifter för varje uppgift måste du tilldela en projektkategori till den beräknade kostnaden. 

**Uppskatta arbetskostnader** För varje lövnodsuppgift tilldelar du en arbetsinsats i timmar och en standardkategori. När du anger ett schema för en uppgift läggs därför automatiskt en uppskattning av arbetskostnaden för aktiviteten till i standardkategorin för arbete. Kostnadsberäkningen visas på fliken **uppskattade kostnader och intäkter** i rutnätet **raddetaljer** för aktiviteten. Om du behöver göra fler beräkningar av arbetskostnaden kan du lägga till dem på fliken. Om du ökar eller minskar antalet timmar i uppskattningen av arbetskostnaderna beräknas schemat för aktiviteten om automatiskt. 

**Uppskattning av kostnader och materialkostnader** låter fliken **Uppskattade kostnader och intäkter** dig uppskatta kostnader och materialkostnader för uppgiften om du önskar uppskattningar. 

Kostnaden och försäljningspriset för varje uppskattningsrad för arbete eller kostnad baseras på inställningarna som har definierats för varje kategori i pristabellerna för **projektledning och redovisning** &gt; **konfiguration** &gt; **Prissättning**. För artiklar läggs kostnad och försäljningspris till som standard från artikel- eller handelsavtalen på listsidan **Frisläppta produkter** i produktinformationshantering.

## <a name="tracking-progress-on-the-wbs"></a>Spåra status i WBS
Vissa branscher följer upp förloppet för ett projekt mot en WBS på en mycket detaljerad nivå, medan andra spårar statusen på en högre nivå i WBS. I det här avsnittet beskrivs hur du kan använda WBS-spårning för projektkrav. 

Finance har tre vyer för projektets WBS: planeringsvy, arbetsuppföljningsvy och kostnadsspårningsvy.

### <a name="planning-view"></a>Planeringsvy

Planeringsvyn visar den planerade beräkningen eller originalberäkningen för schema- och kostnadsinformationen. Även om det inte finns några funktioner för att spåra versionen och baslinjen för en projekt WBS är värdena i vyn avsedda att motsvara baslinjeversionen. Avsnitten Schemaläggning och Kostnadsberäkning i detta ämne beskriver den här vyn och hur den används för att skapa en WBS.

### <a name="effort-tracking-view"></a>Insatsspårningsvy

Vyn Insatsspårning visar spårning av framsteg för uppgifter i WBS. Den jämför ackumulerade faktiska insatstimmar för en aktivitet för den planerade arbetsinsatsen. Följande formler tillhandahåller värdena i vyn uppföljning:

-   Förloppsprocent = faktiska insatsen till dagens datum ÷ planerad insats för uppgiften
-   Återstående insats (kallas även Uppskattning för att slutföra \[ETC\]) = planerad insats – faktiska insatsen till dagens datum
-   Uppskattning för att slutföra (EAC) = planerad insats + den faktiska insatsen hittills
-   Planerad insatsavvikelse = planerat arbete – EAC

I vyn uppföljning av arbetsinsats visas en projektion av insatsavvikelsen för uppgiften, baserat på om EAC är mer eller mindre än planerad insats:

-   Om EAC är större än den planerade ansträngningen projiceras aktiviteten för att ta längre tid än vad som ursprungligen planerades och ligger efter i planeringen.
-   Om EAC är mindre än den planerade ansträngningen projiceras aktiviteten för att ta mindre tid än vad som ursprungligen planerades och ligger före i planeringen.

**Projektledarens återprojektering av insatsen** ibland måste projektledaren eller en annan person som följer upp förloppet för ett projekt revidera de ursprungliga uppskattningarna för en aktivitet. Uppgiften kan av olika orsaker gå snabbare eller långsammare än vad som ursprungligen förväntats. Omfattningen har exempelvis minskat, eller så har arbetare mindre erfarenhet än vad som ursprungligen planerades. Prognoser är en projektledares uppfattning om uppskattningar baserat på den aktuella statusen för ett projekt. I allmänhet bör du inte ändra baslinjenumren, eftersom en projektbaslinje representerar ett väl publicerat dokument för projektets schema och kostnadsberäkning som alla intressenter i projektet har gått med på. 

Det finns två sätt som en projektledare kan använda för att ändra insatsen för uppgifter:

-   Ändra den återstående insatsen som automatiskt uppdateras för att uppdatera den faktiska arbetsinsatsen för uppgiften.
-   Ändra den förloppsprocent som automatiskt uppdateras för att uppdatera det faktiska förloppet för uppgiften.

Båda av dessa är en omberäkning av aktivitetens ETC, EAc och förloppsprocent och den planerade insatsavvikelsen för en aktivitet. Procenten för EAC, ETC och förloppsprocent för sammanfattningsaktiviteterna beräknas även om och deras beräknade insatsavvikelse uppdateras. 

**Ändrad insats för sammanfattningsuppgifter** Du kan ändra ansträngningen för sammanfattnings- eller behållaruppgifter. Oavsett om du ändrar dessa värden med återstående ansträngning eller förloppsprocent på sammanfattningsuppgifterna sker beräkningarna automatiskt i följande ordning:

1.  Procentförloppet för EAC, ETC och aktiviteten beräknas.
2.  Nya EAC fördelas till de underordnade uppgifterna i samma proportion som original EAC-beloppet.
3.  Nya EAC för varje lövnodsuppgift beräknas.
4.  Procentsatsen för återstående insats och förloppet beräknas om för alla berörda underordnade uppgifter, baserat på det nya EAC-värdet. Uppgiftens insatsavvikelse beräknas också om.
5.  EAC för sammanfattningsaktiviteterna räknas även om från lövnod.

Klicka på **utöka till nivå** i Insatsspårningsvy om du vill ange på vilken nivå WBS ska spåras och behållas. WBS utökas automatiskt till den nivån i Insatsspårningsvy när du öppnar den.

### <a name="cost-tracking-view"></a>Vyn Kostnadsspårning

Kostnadsspårningsvyn visar en spårning av kostnadsförbrukning för en uppgift. I den här vyn jämförs den faktiska kostnaden som har använts för aktiviteten hittills i förhållande till den planerade kostnaden för aktiviteten. Följande formler tillhandahåller värdena i vyn Kostnadsspårning:

-   Procent av förbrukad kostnad = faktisk kostnad hittills ÷ planerad kostnad för uppgiften
-   Kostnad för att slutföra (CTC) = planerad kostnad – den faktiska kostnaden hittills
-   Uppskattning för att slutföra (EAC) = CTC + den faktiska kostnaden hittills
-   Planerad kostnadsavvikelse = planerad kostnad – EAC

I vyn Kostnadsspårning av arbetsinsats visas en projektion av kostnadsavvikelsen för uppgiften, baserat på om EAC är mer eller mindre än planerad kostnad:

-   Om EAC är större än den planerade kostnaden projiceras aktiviteten för att använda mer pengar än vad som ursprungligen planerades och ligger över budget.
-   Om EAC är mindre än den planerade kostnaden projiceras aktiviteten för att använda mindre pengar än vad som ursprungligen planerades och ligger under budget.

**Projektledarens återprojektering av kostnaderna** Projektledare måste använda CTC för att ändra den ursprungliga kostnadsuppskattningen för en aktivitet. Projektledaren kan ändra CTC-värdet till kostnaden som krävs för att slutföra uppgiften. Om du ändrar CTC-värdet beräknas aktivitetens CTC, EAC och procent andel av kostnaden och projektkostnaden för den projicerade kostnadsavvikelsen för en aktivitet. EAC, ETC och procent av förbrukad kostnad på sammanfattningsaktiviteterna beräknas även om och deras beräknade kostnadsavvikelse uppdateras. 

> [!NOTE] 
> När du reviderar arbetet för en WBS-uppgift i Insatsspårningsvy beräknas aktivitetens CTC, EAC, procent av förbrukad kostnad och planerad kostnadsavvikelse i vyn kostnads spårning. Kostnadsrevisioner påverkar emellertid inte värdena i insatsspårningsvyn eftersom kostnaden efter transaktionstyp (arbete, material eller kostnad) eller projektkategori inte ändras. 

**Projektionsrevision för kostnader för sammanfattningsuppgifter** du kan revidera kostnaderna för sammanfattningsuppgifter och beräkningarna görs automatiskt i följande ordning:

1.  EAC, CTC och procentandel av förbrukad kostnad för aktiviteten beräknas om.
2.  Nya EAC fördelas till de underordnade uppgifterna i samma proportion som original EAC var på aktiviteten.
3.  Den nya EAC för varje uppgift beräknas.
4.  CTS och procentandel av förbrukad kostnad beräknas om för de underordnade uppgifterna som påverkas, utifrån värdet EAC. Uppgiftens kostnadsavvikelse beräknas också om.
5.  EAC för alla sammanfattningsuppgifter beräknas på ny grundval av den här förändringen.

Klicka på **utöka till nivå** i kostnadsspårningsvy om du vill ange på vilken nivå WBS ska spåras och behållas. WBS utökas till den nivån i kostnadsspårningsvy när du öppnar den.

### <a name="earned-value-management"></a>Hantering av upparbetat värde

Du kan använda metoden för upparbetat värde (EVM) om du vill spåra förloppet för ett projekt. Du kan visa värden för upparbetat värde i projektchefens rollcenter. Diagramkomponenten för upparbetat värde visar tidsfaserade värden för planerat värde och verklig kostnad. Upparbetat värde per aktuellt datum visas som en punkt. Tidsfasad data för upparbetat värde är inte tillgängliga för närvarande. 

Tidsfasen i diagrammet för upparbetat värde visas efter vecka eller månad. I det här avsnittet beskrivs tre pelare för EVM: planerat värde, upparbetat värde och faktisk kostnad. 

**Planerat värde** EVM teori anger att den planerade värde observationsrutan representerar den kvot som projektets team har planerat att få värdet i projektet. 

Finance använder 0:100 och en regel för att rita planerat värde. Med den här regeln bokförs värdet för uppgiften till aktiviteten för dess slutdatum. Inget värde bokförs förrän uppgiften är 100 procent slutförd. 

I projektledning och redovisning anger du slutdatumet för lövnoder och den planerade kostnaden för den. När diagrammet med planerat värde visas efter vecka, sammanfattas det planerade värdet per vecka för alla noder för lövnoder under projektets varaktighet. 

**Upparbetat värde** EVM teori anger att den upparbetat värde observationsrutan representerar den kvot som projektets team faktiskt upparbetat värde i projektet. 

Finance använder 0:100 och en regel för att rita dess upparbetade värde. Med den här regeln bokförs värdet för uppgiften till aktiviteten för dess slutdatum. Inget värde bokförs förrän uppgiften är 100 procent slutförd. 

När upparbetat värde beräknas tas procentsatsen för varje uppgift med i förloppet. Enligt 0:100-regeln beaktas endast uppgifter som är slutförda under en given period för beräkningen av upparbetat värde i slutet av den perioden. Det upparbetade värdet i projektet beräknas för alla uppgifter som har slutförts när grafen skapas. 

> [!NOTE] 
> För närvarande finns det inga datastrukturer för WBS-spårning för att lagra historiska procentsatser för varje aktivitet. Därför kan upparbetat värde endast rapporteras i den tid då kuben bearbetas. Bearbeta kuben regelbundet för att uppdatera data för upparbetat värde som visas i rollcentret. 

**Verklig kostnad** EVM teori anger att den faktiska kostnadens ritning representerar den takt som pengar spenderas åt projektet. 

Transaktioner som bokförs till ett projekt används för att rita upp den faktiska kostnadsraden. Kostnaderna sammanfattas efter datum. Dessa data används sedan för att rita upp de faktiska kostnaderna per vecka eller månad i diagrammet över upparbetat värde.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Använda koncepten för planerat värde, upparbetat värde och verklig kostnad

**Schemaavvikelse** under planering skapar du en prognos för arbete på en tidslinje. Planerat värde är alltså den hastighet som projektplanerare ska vara slutförda i projektet. När ett projekt pågår, arbetet är klart och projektet får värdet. Genom att jämföra planerat värde med upparbetat värde kan du se hur arbetet i ett projekt fortlöper. Resultatet av jämförelsen kallas för schemaavvikelse. 

Om det planerade värdet för en period överstiger det upparbetade värdet är det arbete som har utförts i ett projekt mindre än vad som planerades. Projektet ligger därför bakom schemat. Eftersom planerat värde och upparbetat värde uttrycks i monetära termer får tids fördröjningen också ett monetärt värde. 

Om det planerade värdet för en period är mindre det upparbetade värdet är det arbete som har utförts i ett projekt mer än vad som planerades. Projektet ligger därför framför schemat. Ledtiden får också ett monetärt värde.

**Kostnadsavvikelse** eftersom det upparbetade värdet använder självkostnaden som multiplikator, upparbetat värde anger kostnaden för det arbete som utförs i ett projekt. I takt med att projektet fortlöper innehåller transaktionsloggen en post över de belopp som faktiskt ägnas åt projektet. Genom att jämföra upparbetat värde med verklig kostnad kan du visa det belopp som har spenderats jämfört med värdet som intjänas. Resultatet av jämförelsen kallas för kostnadsavvikelse. 

Om den faktiska kostnaden som ägnas åt en period är högre än det upparbetade värdet, användes mer pengar än det intjänade. Projektet är därför över budget. 

Om den faktiska kostnaden som ägnas åt en period är mindre än det upparbetade värdet, intjänades mer pengar än vad som spenderats. Projektet är därför under budget.

## <a name="wbs-templates"></a>WBS-mallar
Du kan använda funktionerna för WBS-mallar för att skapa standardmallar för projekt. Om de projekt som företaget erbjuder omfattar en massa upprepningsbar åtgärd bör du överväga att skapa en WBS-mall. 

Du kan skapa en WBS-mall utifrån WBS i ett befintligt projekt så att kunskaps- och affärspraxis som du har samlat in under planeringen av projektet kan återanvändas i liknande projekt i framtiden. Ibland kanske du vill spara hela WBS som en mall. Därför kan du även skapa mallar från delar av WBS för ett projekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Spara WBS för ett projekt som en mall

När du har skapat en mall kan du importera den till ett nytt projekts WBS under rotnoden, eller under en aktivitet i projektets WBS.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importera en WBS-mall till ett projekts WBS

När du importerar uppgifter ordnas uppgifterna i mallen utifrån startdatum för den uppgift som de importeras under. Under importen används föregående relationer av aktiviteterna i mallen för att beräkna startdatum för de importerade aktiviteterna. Målprojektets standard arbetskalender används för att beräkna slutdatumen för de importerade aktiviteterna, så att arbetsdagar och standard arbetstimmar som har definierats i det aktuella projektets arbetskalender bevaras. 

Kostnadsbelopp och försäljningspriser på uppskattningsraderna används för att garantera att priser som är specifika för projektet eller projektkontraktet har giltiga datum.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Skillnader mellan ett projekts WBS och en WBS-mall

-   Uppgifterna i WBS-mallar har inte start- och slutdatum.

Arbetsdagar och ledig tid är inte inställda för WBS-mallar.

-   WBS-mallar använder alltid schemaläggningskalendern som är inställd som standardkalender för alla projekt.

Standardkalendern för schemaläggning används endast för att ta reda på timmar under en standardarbetsdag.

-   Föregående relationer kopieras inte till en WBS-mall.

Eftersom WBS-mallar inte har datum krävs inte startdatumlogiken som baseras på en föregångares slutdatum.

-   En uppskattningsrad för arbetskostnader skapas automatiskt när en uppgift skapas i en WBS-mall. Försäljningspriset och kostnadsbeloppet kopieras från den valda arbetaren.

Utgift och artikelkostnader kan skapas manuellt, precis som de kan i ett projekts WBS.

-   Schemaläggningsfel visas när det finns avvikelser från följande formel:

Insats = antal resurser × varaktighet × antalet timmar i en standard arbetsdag 

Du kan korrigera alla schemaläggningsfel samtidigt genom att klicka på **åtgärda alla schemaläggningsfel**. 

Du kan även åtgärda eventuella schemaläggningsfel individuellt genom att klicka på varningsikonen för varje uppgift.



