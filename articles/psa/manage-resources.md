---
title: Hantera resurser
description: I det här ämnet finns information om hur du hanterar resurser.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 37377367751592fc533447748b80b124cb6548ad
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151365"
---
# <a name="manage-resources"></a>Hantera resurser

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation innehåller en instrumentpanel för resurshantering som ger en grafisk översikt över resursbehov och utnyttjande i hela organisationen. Du kan använda diagrammen på den här instrumentpanelen för att visualisera följande information:

- **Resursbehov** – diagrammet **aktiva resursbegäran** innehåller resurser som har skickats in. Resurserna aggregeras antingen efter roll eller projekt.
- **Ej skickad resursbehov**  – diagrammet **Otilldelat resursbehov** visar alla resurskrav som inte har skickats. Den hjälper resursansvariga att visa behov som inte är fast och kan skickas via en resursförfrågan.
- **Fakturerbar tid för den senaste veckan** – diagrammet **användning efter roll** visar procentandelen av organisationens faktiska fakturerbara användning efter roll mot den faktiska fakturerbara användning efter roll.

    > [!NOTE]
    > Om du vill göra diagrammet **Användning efter roll** tillgänglig skapar du ett jobb som kör arbetsflödet UpdateRoleUtilization. Detta återkommande jobb körs var sjunde dag för att beräkna fakturerbart utnyttjande för de föregående sju dagarna. Resultatet aggregeras efter roll.

## <a name="manage-project-team-members"></a>Hantera projektteammedlemmar

Projektledarna kan använda resurshanterarens instrumentpanel för att hantera resurser i projekt. De kan till exempel lägga till en gruppmedlem direkt i ett projekt och boka en grupp medlem för att uppfylla de resurskrav som har samlats upp av en generisk resurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Lägga till en teammedlem direkt i ett projekt

Om du vill lägga till en teammedlem direkt i ett projekt väljer du **Projekt** på sidan **Team** och väljer **Ny**. Dialogrutan **Snabbregistrering: Projektteammedlem**. I den här dialogrutan kan du utföra de här uppgifterna:

- **Boka en namngiven resurs** – i fältet **Bokningsbar resurs** anger du namnet på resursen. Välj sedan rollen, ange period och välj en allokeringsmetod. Den namngivna resursen som du har valt läggs till i projektet med hjälp av den valda allokeringsregeln och resurskalendern.
- **Lägg till en generisk resurs** – Lämna fältet **Bokningsbar resurs** tomt och välj sedan rollen, ange perioden och välj önskad allokeringsmetod. En generisk resurs läggs till i teamet som en platshållare för att hålla efterfrågemönstret som används för att boka namngivna resurser i teamet. Kravet ställs i enlighet med projektkalendern.
- **Lägg till en namngiven resurs i teamet utan förbrukningsresurskapacitet** – Välj en resurs i fältet **bokningsbar resurs**. Välj sedan period och välj **Ingen** som allokeringsmetod. Resursen läggs till i teamet, men resursens kapacitet förbrukas inte via en bokning.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Boka en teammedlem som uppfyller resurskraven för en generisk resurs

I PSA kan du boka en generisk resurs i ett projektteam och du kan ange vilken kapacitet som krävs samt hur kapaciteten ska fördelas. Du kan ange attribut som är associerade med den allmänna resursen i resursbehovet. Dessa attribut innehåller obligatoriska kunskaper, den prioriterade organisationsenheten och önskade resurser.

Följ stegen nedan för att ange vilka kunskaper som krävs på en generisk resurs för en utvecklare.

1. På sidan **projekt** på fliken **team** väljer du **ny** för att boka en generisk resurs.

    ![Allmänna resurser bokade i teamet](media/Resource-Management-image9.png)

2. I vyn **Alla teammedlemmar** i kolumnen **Resurskrav** väljer du länk om du vill lägga till obligatoriska kunskaper för den generiska resursen.

    ![Kravlänk](media/Resource-Management-image10.png)

3. På sidan **Resurskrav** som visas i rutnätet **Färdigheter** välj sedan ellipsen (**...**) och sedan **Lägg till ny kravegenskap** för att lägga till nödvändiga färdigheter för din utvecklare.

    ![Kommandot Lägg till ny kravegenskap](media/Resource-Management-image11.png)

4. I dialogrutan **Snabbregistrering: Kravegenskap** som visas väljer du önskad färdighet i fältet **egenskap**. I fältet **värderingsvärde** väljer du sedan önskad kompetensnivå för den färdigheten. Slutligen, i fältet **Resurskrav** anger du behovet av källresurser från organisationsenheter eller till och med namngivna resurser. När du är klar väljer du **Spara**.

    ![Snabbregistrering: dialogrutan kravegenskap](media/Resource-Management-image12.png)

5. På sidan **Resurskrav**, välj **Boka** för att uppfylla resursbehovet.

    ![Knappen Boka på sidan Resurskrav](media/Resource-Management-image13.png)

    Du kan också markera den allmänna resursen i rutnätet **alla teammedlemmar** och väljer sedan **boka**.

    ![Knappen Boka ovanför rutnätet Alla teammedlemmar](media/Resource-Management-image14.png)

    > [!NOTE]
    > I det här exemplet finns 40 obligatoriska timmar men inga egentliga timmar eftersom allmänna resurser inte har några bokningar. Det finns inte heller några tilldelade timmar eftersom den allmänna resursen lades till direkt i teamet. Du lades inte till med hjälp av tilldelning av uppgifter.

    På sidan **schemaläggningsassistent** kan du filtrera tillgängliga resurser utifrån de krav som anges i resursbehovet. Resurserna sorteras enligt de sorteringsparametrar som anges på schemaläggningstavlan.

    ![Sidan Schemaläggningsassistenten](media/Resource-Management-image15.png)

    Här följer några filter som ofta används:

    - **Egenskaper tillsammans med en värdering** – filtrera efter kunskaper, certifieringar och andra resurser, samt bedömningar av kompetenser.
    - **Roller** – filtrera efter de standardroller som tilldelas bokningsbara resurser.
    - **Organisationsenheter** – filtrera bokningsbara resurser efter de organisationsenheter de är tilldelade till.

6. Om du inte är nöjd med resultatet av den första kravsökningen kan du ändra filtervillkoren. Expandera rutan **filtervy** till vänster och välj sedan **Sök** efter ytterligare resurser.

    ![Fönstret Filtervy](media/Resource-Management-image16.png)

7. Om du vill ändra hur resultatet sorteras väljer du **sortera**.

    ![Kommandot Sortera](media/Resource-Management-image17.png)

8. Välj resurser enligt den begäran som anges på kravet, som anges längst upp på rutnätet. Du kan radera urvalet av celler i rutnätet och låta den öppna resurskapaciteten vara öppen. Det går bara att markera en resurs åt gången som bokad.

9. Välj **boka** om du vill boka den valda resursen och låta schemaläggningstavlan vara öppen så att du kan välja ytterligare resurser. Du kan också välja **Boka och avsluta** om du vill boka den valda resursen och stänga schemaläggningstavlan.

    ![Resurs att boka](media/Resource-Management-image19.png)

    Du får ett meddelande om bokade timmar. Begäranindikatorerna illustrerar hur mycket av bokningskravet som är uppfyllt och hur mycket som återstår. Du kan också se hur mycket av den valda resurskapaciteten som förbrukas. Välj **expandera** om du vill visa mer information om resursbokningar.

9. Gå tillbaka till vyn **Alla teammedlemmar**. Observera att den allmänna resursen i rutnätet har ersatts av den namngivna resursen och 40 timmar har ställts in som bokad för resursen.

    ![Uppdaterat rutnätet för alla teammedlemmar](media/Resource-Management-image20.png)

    > [!NOTE]
    > Inga timmar visas eftersom de har bokats direkt i teamet. De har inte bokats med hjälp av tilldelning av uppgifter.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tilldela allmänna resurser till uppgifter och generera resurskrav

Du kan skapa uppgifter i PSA och sedan tilldela dem allmänna resurser. På det här sättet kan resursbehovet representeras av platshållare samtidigt som du uppskattar ditt schema och finansiell numrering. Du kan sedan generera resurskrav för de allmänna resurserna och uppfylla dem.

1. På sidan **projekt** på fliken **schema** väljer du **lägg till** för att skapa en uppgift.

    ![Ny uppgift skapad](media/Resource-Management-image21.png)

2. I fältet **Resurser**, välj symbolen **Resursväljare**. Resursväljaren visas och visar befintliga teammedlemmar för projektet.

    ![Resursväljare](media/Resource-Management-image22.png)

3. Ange namnet på den nya generiska resursen och välj sedan **skapa**.

    ![Namnet på en ny generisk resurs angavs](media/Resource-Management-image23.png)

4. I dialogrutan **Snabbregistrering: Projektteammedlem** som visas väljer du roll för generisk resurs i fältet **roll**. I fältet **Resursenhet** väljer du organisationsenhet för den generiska resursen. Välj sedan **Spara**.

    ![Snabbregistrering: dialogrutan Projektteammedlem.](media/Resource-Management-image24.png)

    Den generiska teammedlemmen har nu tilldelats till aktiviteten.

    ![Den generiska teammedlemmen har tilldelats till aktiviteten.](media/Resource-Management-image25.png)

    På fliken **team** visas den nya generiska teammedlemmen. Observera att det endast har tilldelats timmar. De här timmarna är summan av alla uppgifter som är tilldelade till den generiska teammedlemmen. Den generiska teammedlemmen har ännu inte krävt några timmar eller ett resurskrav.

    ![Generisk teammedlem på fliken team](media/Resource-Management-image26.png)

5. Du kan nu tilldela den generiska teammedlemmen till andra uppgifter med hjälp av resursväljaren.

    ![Generisk team medlem i resursväljaren](media/Resource-Management-image27.png)

    När du har tilldelat generisk resurs till uppgiften kan du skapa ett resurskrav för den generiska resursen.

5. På fliken **Team**, välj den generiska resursen och välj sedan **generera krav**.

    ![Kommandot Generera krav](media/Resource-Management-image28.png)

    När kravet skapas får den generiska teammedlemmen obligatoriska timmar och en länk för resurskravet.

    ![Länk för resurskrav](media/Resource-Management-image29.png)

    När du har bokat en namngiven resurs tas den allmänna resursen bort från teamet och ersätts av den namngivna resursen.

    ![Den generiska resursen ersätts av den namngivna resursen](media/Resource-Management-image30.png)

    På fliken **Schema** tas den generiska resurstilldelningar och ersätts av den namngivna resursen på fliken schema.

    ![Generiska resurstilldelningar som ersätts av den namngivna resursen på fliken schema.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Det här problemet uppstår endast när en namngiven resurs är helt bokad för generiska resurskrav. När en namngiven resurs delvis ersätter det generiska resurs behovet eller flera namngivna resurser ersätter det allmänna resurs behovet, förblir den allmänna resursen tilldelad aktiviteten.

    I följande bild har en 80-timmars uppgift planerats för en varaktighet på fem dagar (16 timmar per dag över fem dagar) och tilldelats den generiska resurs som kallas **funktionell**.

    ![80-timmars, fem dagars uppgift tilldelad till den funktionella generiska resursen](media/Resource-Management-image32.png)

    När du genererar kravet är det för 80 timmar i fem dagar.

    ![Krav som genereras för 80 timmar i fem dagar](media/Resource-Management-image33.png)

    Eftersom tillgängliga resurser endast arbetar åtta timmar per dag krävs det två resurser för att uppfylla kravet.

    ![Andra resursen](media/Resource-Management-image35.png)

    På fliken **team** kan du nu se att den allmänna resursen inte har några obligatoriska timmar, men att de tilldelade timmarna fortfarande visas tillsammans med de två namngivna resurser som utgör uppfyllandet.

    ![Två namngivna resurser på fliken Team](media/Resource-Management-image36.png)

    På fliken **schema** har den allmänna resursen fortfarande tilldelats uppgiften.

    ![Generiska resurser på fliken Schema](media/Resource-Management-image37.png)

PSA tilldelar inte båda resurserna till uppgiften eftersom det kan ge ett mindre förutsägbart schema. I det här enkla exemplet är det enkelt att fördela timmarna lika mellan två resurser. I mer komplexa scenarier med flera uppgifter och flera resurser måste PSA emellertid göra antagandet om hur den bör allokera de bokningar som tas emot för flera resurser i flera olika uppgifter.

Därför är projektledare är ansvarig för att analysera flera bokningar och tilldela dem efter behov. För att kunna allokera bokningarna tilldelas projektledaren uppgifterna från de allmänna resurserna till de namngivna resurserna och sedan används vyn **avstämning** för att se till att allokeringen fungerar med bokningarna.

### <a name="edit-a-resource-requirement"></a>Redigera ett resurskrav

När ett resurskrav har skapats kan en projektledare eller en resursansvarig behöva redigera informationen för att förfina sökvillkoren när schemaläggningstavlan används. Följ stegen nedan om du vill redigera resurskravet.

1. På sidan **projekt** på fliken **team** väljer du länken till alla krav på en generisk resurs.
2. På sidan **resursbehov** som visas kan du uppdatera flera attribut. Här följer några exempel:

    - Namn
    - Från och med
    - Hittills
    - Varaktighet
    - Resurstyp

På sidan **resurskrav** kan projektledaren eller resursansvarig även ange följande information:

- Kompetens
- Roller
- Resursinställningar
- Prioriterade organisationsenheter

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Uppdatera resursbokningar efter att de har bokats i ett projekt

När du har lagt till en allmän eller namngiven resurs i ett projektteam kan du ändra resursens bokföring.

1. På sidan **Projekt** på fliken **Team** väljer du en teammedlem och sedan **Underhåll bokningar**.

    ![Schemaläggningstavlan öppnas för den valda teammedlemmen](media/Resource-Management-image40.png)

    Schemaläggningstavla visas och visar projektmedlemmens bokningar. Expandera teammedlemmens post om du vill visa vilka tider som har bokats i projektet och andra projekt som konsumerar teammedlemmens kapacitet.

2. Välj och dra bokningen för att utöka eller förkorta den. Dialogrutan **Skapa resursbokning** öppnas där du kan justera bokningen.

    ![Dialogrutan Skapa resursbokning](media/Resource-Management-image41.png)

3. Högerklicka på bokningen. Sedan kan du använda snabbmenyn för att utföra följande åtgärder:

    - Ändra bokningsstatus.
    - Redigera bokningen.
    - Ersätt en resurs i projektteamet.

### <a name="change-the-booking-status"></a>Ändra bokningsstatus

Du kan ändra vilken status som helst för alla standard- eller anpassade bokningar.

![Kommandot Ändra status](media/Resource-Management-image42.png)

Följande statusar ingår i PSA:

- **Annullerad** – den här statusen avbryter en resursbokning och frigör resursens kapacitet.
- **Fast bokning** – den här statusen förbrukar en resurskapacitet. En bokning har vanligtvis denna status när du öppnar **Underhåll bokningar** från rutnätet **Alla teammedlemmar** på sidan **projekt**.
- **Preliminär bokning** – den här statusen lägger till en resurs i ett team, men förbrukar inte resursens kapacitet. Den indikerar att resursen har reserverats för potentiellt arbete men fortfarande har kapacitet för andra jobb. I vyn över övergripande resurstillgänglighet får preliminära bokningar annan status än fasta bokningar.
- **Föreslagen** – denna status representerar resursansvariges eller projektledarens förslag för en resurs. Förslag förbrukar inte resursens kapacitet och resursen läggs inte till i projektteamet. Om du vill göra en fast bokning för resursen i teamet måste projektledaren godkänna förslaget.

### <a name="submit-resource-requests"></a>Skicka resursbegäran

Resursbegäran används för att bära en begäran (resurskrav) som måste uppfyllas av en resursansvarig. För en generisk resurs som redan finns i teamet kan du skicka en resursbegäran direkt. En resursbegäran kan uppfyllas på två sätt:

- Resurshanteraren uppfyller direkt begäran. I det här fallet ersätts den generiska resursen av en fast bokning med en namngiven resurs.
- Resursansvarig föreslår en resurs för projektledaren och projektledaren godkänner eller avvisar den föreslagna resursen.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direkt uppfyllelse av resursbegäran

När ett resurskrav skapas kan en projektledare skicka en resursbegäran för en generisk resurs genom att välja resursen och sedan välja **skicka begäran**.

![Knappen Skicka begäran](media/Resource-Management-image45.png)

Kommentarer om resursen kan ges till den resursansvarige som uppfyller begäran. När begäran har skickats ändras fältet **status** för teammedlemmen till **skickad**.

![Ange valfria kommentarer](media/Resource-Management-image46.png)

När resursansvarig fullföljer begäran ersätts den generiska teammedlemmen av den namngivna resursen i rutnätet **alla teammedlemmar**.

![En generisk teammedlem som ersatts av den namngivna resursen i rutnätet alla teammedlemmar](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Använda ett resursförslag för resursbegäran

I stället för att direkt boka en resurs i en resursbegäran kan en resursansvarig föreslå projektresurs till projektledare. En resursansvarig kan använda det här alternativet om en exakt matchning för kraven inte är tillgänglig. När en resursansvarig föreslår en resurs ser projektledare fältet **status** för den allmänna teammedlemmen ändras till **Måste granskas**.

![Den generiska teammedlemmens status ändras till Måste granskas](media/Resource-Management-image48.png)

Om du vill visa den föreslagna resursen tillsammans med en visualisering av effekten av förslagets bokning, dubbelklickar du på den teammedlem som har statusvärdet **Måste granskas**. Välj sedan fliken **föreslagna resurser**.

![Fliken Föreslagna resurser](media/Resource-Management-image49.png)

Markera **acceptera alla förslag** för att acceptera alla föreslagna resurser eller **avvisa alla förslag** för att avvisa dem. Om du accepterar de föreslagna resurserna är de fast bokade i projektet som teammedlemmar och ersätter generiska resurser.

> [!NOTE]
> Du måste antingen acceptera eller avvisa alla föreslagna resurser. Du kan inte delvis acceptera eller avvisa dem.

### <a name="substitute-a-resource-on-the-project-team"></a>Ersätt en resurs i projektteamet.

Ibland måste en projektledare ersätta en teammedlem i ett projekt.

1. På sidan **Projekt** på fliken **Team** väljer du den resurs som behöver en ersättning och sedan **Underhåll bokningar**.
2. Expandera resursen om du vill visa de projekt som den är tilldelad till.

    ![Resurs utökad för att visa tilldelade projekt](media/Resource-Management-image50.png)

3. Högerklicka på projektet och välj sedan **Ersättningsresurs**.
4. Om du känner till den resurs du vill ersätta den aktuella resursen med markerar du eller skriver namnet och väljer sedan **tilldela igen**.

    ![Ange en ersättningsresurs](media/Resource-Management-image51.png)

    Du kan också söka efter en resurs genom att följa stegen nedan:

    1. Välj **Sök ersättning**.

        ![Söka efter en ersättningsresurs](media/Resource-Management-image52.png)

        Schemaassistenten visar en lista över tillgängliga ersättningar. I schemaläggningsassistenten kan du ytterligare filtrera tillgängliga resurser för att hitta en lämplig ersättare.

        ![Lista över tillgängliga ersättare](media/Resource-Management-image53.png)

    2. För att ersätta resursen, välj resursen och välj **ersättare**.

        ![Vald ersättningsresurs](media/Resource-Management-image54.png)

    Bokningarna och tilldelningarna ersätts med den nya resursen.

    ![Bokningarna och tilldelningarna ersätts med den nya resursen.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Avstämning av bokningar och tilldelningar av teammedlemmar

För teammedlemmar kombineras inte bokningar och tilldelningar är löst kopplade. Med andra ord kan resurser ha tilldelningar, men inga bokningar, eller så kan de inte ha bokningar men inga tilldelningar. Vanligtvis justeras projektbokningar och tilldelningar så att resurserna har rätt kapacitet för att utföra sina aktivitetstilldelningar. Bokningarna kan emellertid vara baserade på tillgänglighet, och tidsinställningar för aktiviteter kan ändras när projektet fortsätter. Därför är den fria kopplingen av bokningar och tilldelningar flexiblare.

PSA har fliken **avstämning** låter projektledarna avstämma teammedlemmarnas bokningar och deras tilldelningar för sina projektteam.

![Fliken Avstämning](media/Resource-Management-image56.png)

Fliken **avstämning** visar bokningar och tilldelningar ned till nivån för enskilda uppgiftstilldelningen för varje teammedlem. Den visar antalet timmar i celler som kan representera tidsperioder från månader ned till dagar.

Fliken visar även en total nettosumma för projektet tillsammans med en total kolumn.

För varje resurs beräknar fliken en skillnad mellan en teammedlems bokningar och sammanslagningen av teammedlemmens aktivitetstilldelningar. Vi rekommenderar att skillnaden är 0 (noll). Det bör alltså inte finnas någon skillnad mellan bokningar och tilldelningar. Skillnader är färgade och tonade för att framhäva två villkor:

- **Underskott för bokning** – Underskott för bokning uppstår om en resurs har fler tilldelningar än bokningar. Eftersom denna kapacitet inte har reserverats kan en projektledare korrigera problemet genom att utöka resursens bokningar så att underskottet täcks.
- **Överflödiga bokningar** – Överflödiga bokningar inträffar när en resurs har bokats i projektet men inte tilldelats aktiviteter. Det här tillståndet kan vara acceptabelt i de fall då resursen togs i projektet före tilldelning av uppgifter. I andra fall är inte resursen planerad att tilldelas till uppgifter. I så fall bör projektledaren överväga att annullera resursbokningarna så att kapaciteten kan användas för ett annat projekt.

I vissa fall kan du se en nettoskillnad i noll för en resurs (t.ex. månadsnivån) när du visar tid på en högre nivå än dag nivå (till exempel månadsnivån). Om du visar tid på veckonivån kan du se att det finns tilldelningar på noll timmar och bokningar på 40 timmar under den första veckan men tilldelningar på 40 timmar och bokningar på noll timmar i den andra veckan i månaden. Generellt synkroniseras bokningarna och tilldelningarna, men de skiljer sig från en vecka till nästa.

När du visar högre tidsnivåer visar har celler i fliken **avstämning** har en indikator som meddelar att det finns olikheter på lägre nivåer. Genom att dubbelklicka i en cell kan du zooma in för att visa skillnaden. Du kan sedan högerklicka för att zooma ut. Genom att välja en resurs och sedan använda kontrollen **nästa skillnad** i verktygsfältet i rutnätet kan du gå vidare till nästa skillnad mellan bokningar och tilldelningar för resursen. Därefter kan du använda kontrollen **föregående skillnad** för att gå tillbaka. Du kan också inaktivera skillnadsindikator och navigeringsbeteende under **inställningar**.

![Skillnadsindikator](media/Resource-Management-image57.png)

I situationer där du har aktivitetstilldelningar för en resurs men inga bokningar, på sidan **Projekt** på fliken **Avstämning**, välj underskott för bokningen och sedan **utöka bokning**. I dialogrutan **utöka bokning** visas och visar den bokning som behövs för att lösa resursens underskott. Den visar även resursens befintliga bokningar för alla projekt eller andra schemalagda entiteter. Om du väljer **OK** för att skapa bokningen för resursen, oavsett resursens tillgänglighet, kan det leda till överbokning.

![Dialogrutan utöka bokning](media/Resource-Management-image58.png)

Projektledaren eller resursansvarig kan sedan använda schemaläggningstavlan för att hantera alla situationer där en resurs har blivit överbokad utanför sin kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]