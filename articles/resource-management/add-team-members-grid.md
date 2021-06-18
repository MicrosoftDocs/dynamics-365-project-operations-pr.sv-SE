---
title: Lägga till teammedlemmar från rutnätet med teammedlemmar
description: I det här ämnet finns information om hur du hanterar resurser i form av teammedlemmar.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 95f9e1d836e49672cfb51ace59aa77ea9da65b35
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998883"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Lägga till teammedlemmar från rutnätet med teammedlemmar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations innehåller en instrumentpanel för resurshantering som ger en grafisk översikt över resursbehov och utnyttjande i hela organisationen. Du kan använda diagrammen på den här instrumentpanelen för att visualisera följande information:

- **Resursbehov**: diagrammet **Aktiv resursbegäran** innehåller resurser som har skickats in. Resurserna aggregeras antingen efter roll eller projekt.
- **Ej skickat resursbehov**: diagrammet **Otilldelat resursbehov** visar alla resurskrav som inte har skickats. Detta diagram hjälper resursansvariga att visa behov som inte är fast och kan skickas via en resursförfrågan.
- **Fakturerbar användning för den senaste veckan**: diagrammet **Användning efter roll** visar procentandelen av organisationens faktiska fakturerbara användning efter roll mot målet för fakturerbar användning efter roll.

    > [!NOTE]
    > Om du vill göra diagrammet **Användning efter roll** tillgänglig skapar du ett jobb som kör arbetsflödet **UpdateRoleUtilization**. Detta återkommande jobb körs var sjunde dag för att beräkna fakturerbart utnyttjande för de föregående sju dagarna. Resultatet aggregeras efter roll.

## <a name="manage-project-team-members"></a>Hantera projektteammedlemmar

Projektledarna kan använda instrumentpanelen för resursansvariga för att hantera resurser i projekt. De kan till exempel lägga till en gruppmedlem direkt i ett projekt och boka en grupp medlem för att uppfylla de resurskrav som har samlats upp av en generisk resurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Lägga till en teammedlem direkt i ett projekt

Om du vill lägga till en teammedlem direkt i ett projekt går du till formuläret **Projekt** under fliken **Team** och väljer **Ny**. Dialogrutan **Snabbregistrering: Projektteammedlem**. I den här dialogrutan kan du utföra de här uppgifterna:

- **Boka en namngiven resurs**: i fältet **Bokningsbar resurs** anger du namnet på resursen. Välj sedan rollen, ange period och välj en allokeringsmetod. Den namngivna resursen som du har valt läggs till i projektet med hjälp av den valda allokeringsregeln och resurskalendern.
- **Lägg till en generisk resurs**: Lämna fältet **Bokningsbar resurs** tomt och välj sedan rollen, ange perioden och välj önskad allokeringsmetod. En allmän resurs läggs till i teamet som platshållare. Platshållaren innehåller det efterfrågansmönster som används för att boka namngivna resurser i teamet. Kravet ställs i enlighet med projektkalendern.
- **Lägg till en namngiven resurs i teamet utan förbrukningsresurskapacitet**: Välj en resurs i fältet **Bokningsbar resurs**. Välj period och välj sedan **Ingen** som allokeringsmetod. Resursen läggs till i teamet, men resursens kapacitet förbrukas inte via en bokning.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Boka en teammedlem som uppfyller resurskraven för en generisk resurs

I Project Operations kan du boka en allmän resurs i ett projektteam. Du kan även ange rollen, vilken kapacitet som krävs och hur denna kapacitet fördelas. Du kan ange attribut som är associerade med den allmänna resursen för resursbehovet. Dessa attribut innehåller obligatoriska kunskaper, den prioriterade organisationsenheten och önskade resurser.

Slutför stegen nedan för att ange vilka kunskaper som krävs på en generisk resurs för en utvecklare.

1. På formuläret **Projekt** under fliken **Team** väljer du **Ny** för att boka en generisk resurs.
2. I vyn **Alla teammedlemmar** i kolumnen **Resurskrav** väljer du länk om du vill lägga till obligatoriska kunskaper för den generiska resursen.
3. På formuläret **Resurskrav** som visas i rutnätet **Färdigheter** välj sedan ellipsen (**...**) och sedan **Lägg till ny kravegenskap** för att lägga till nödvändiga färdigheter för din utvecklare.
4. I dialogrutan **Snabbregistrering: Kravegenskap** som visas väljer du önskad färdighet i fältet **Egenskap**.
5. I fältet **Värderingsvärde** väljer du sedan önskad kompetensnivå för den färdigheten. 
6. I fältet **Resurskrav** anger du behovet av källresurser från organisationsenheter eller till och med namngivna resurser. När du är klar väljer du **Spara**.
7. På formuläret **Resurskrav**, välj **Boka** för att uppfylla resursbehovet. Du kan också markera den allmänna resursen i rutnätet **alla teammedlemmar** och väljer sedan **boka**.

    > [!NOTE]
    > I det här exemplet finns 40 obligatoriska timmar men inga egentliga timmar eftersom allmänna resurser inte har några bokningar. Det finns inte heller några tilldelade timmar eftersom den allmänna resursen lades till direkt i teamet i stället för att läggas till genom uppgiftstilldelning.

    På formuläret **Schemaläggningsassistent** kan du filtrera tillgängliga resurser utifrån de krav som anges i resursbehovet. Resurserna sorteras enligt de sorteringsparametrar som anges på schemaläggningstavlan.

   Här följer några av de vanligaste filtren:

    - **Egenskaper tillsammans med en värdering**: filtrera efter kunskaper, certifieringar och andra resurser, samt bedömningar av kompetenser.
    - **Roller**: filtrera efter de standardroller som tilldelas bokningsbara resurser.
    - **Organisationsenheter**: filtrera bokningsbara resurser efter de organisationsenheter de är tilldelade till.

8. Om du inte är nöjd med resultatet av den första kravsökningen kan du ändra filtervillkoren. Expandera rutan **filtervy** till vänster och välj sedan **Sök** efter ytterligare resurser. Om du vill ändra hur resultatet sorteras väljer du **sortera**.
9. Välj resurser enligt den begäran som anges på kravet, som anges längst upp på rutnätet. Du kan radera urvalet av celler i rutnätet och låta den öppna resurskapaciteten vara öppen. Det går bara att markera en resurs åt gången som bokad.
10. Välj **boka** om du vill boka den valda resursen och låta schemaläggningstavlan vara öppen så att du kan välja ytterligare resurser. Du kan också välja **Boka och avsluta** om du vill boka den valda resursen och stänga schemaläggningstavlan.
11. Gå tillbaka till vyn **Alla teammedlemmar**. Observera att den allmänna resursen i rutnätet har ersatts av den namngivna resursen och 40 timmar har ställts in som bokad för resursen.

    > [!NOTE]
    > Inga timmar visas eftersom de har bokats direkt i teamet. De har inte bokats med hjälp av tilldelning av uppgifter.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tilldela allmänna resurser till uppgifter och generera resurskrav

Du kan skapa uppgifter i Project Operations och sedan tilldela dem allmänna resurser. Resursbehovet kan då representeras av platshållare samtidigt som du uppskattar ditt schema och finansiell numrering. Du kan sedan generera resurskrav för de allmänna resurserna och uppfylla dem.

1. På formuläret **Projekt** under fliken **Schema** väljer du **Lägg till** för att skapa en uppgift.
2. I fältet **Resurser**, välj symbolen **Resursväljare**. Resursväljaren visas och visar befintliga teammedlemmar för projektet.
3. Ange namnet på den nya generiska resursen och välj sedan **skapa**.
4. I dialogrutan **Snabbregistrering: Projektteammedlem** som visas väljer du roll för generisk resurs i fältet **roll**. 
5. I fältet **Resursenhet** väljer du organisationsenhet för den generiska resursen. Välj sedan **Spara**. Den generiska teammedlemmen har nu tilldelats till aktiviteten.

   På fliken **team** visas den nya generiska teammedlemmen. Observera att det endast har tilldelats timmar. De här timmarna är summan av alla uppgifter som är tilldelade till den generiska teammedlemmen. Den generiska teammedlemmen har inte krävt några timmar eller ett resurskrav.

6. Du kan nu tilldela den generiska teammedlemmen till andra uppgifter med hjälp av resursväljaren.

   När du har tilldelat generisk resurs till uppgiften kan du skapa ett resurskrav för den generiska resursen.

7. På fliken **Team**, välj den generiska resursen och välj sedan **generera krav**. När kravet skapas får den generiska teammedlemmen obligatoriska timmar och en länk för resurskravet.

  När du har bokat en namngiven resurs tas den allmänna resursen bort från teamet och ersätts av den namngivna resursen. På fliken **Schema** tas den generiska resurstilldelningar och ersätts av den namngivna resursen på fliken schema.

  > [!NOTE]
  > Det här problemet uppstår endast när en namngiven resurs är helt bokad för generiska resurskrav. När en namngiven resurs delvis ersätter det generiska resurs behovet eller flera namngivna resurser ersätter det allmänna resurs behovet, förblir den allmänna resursen tilldelad aktiviteten.

Project Operations tilldelar inte båda resurserna till uppgiften eftersom det kan ge ett mindre förutsägbart schema. I det här enkla exemplet är det enkelt att fördela timmarna lika mellan två resurser. I mer komplexa scenarier med flera uppgifter och flera resurser måste PSA emellertid göra antagandet om hur den bör allokera de bokningar som tas emot för flera resurser i flera olika uppgifter.

Därför är projektledaren ansvarig för att analysera flera bokningar och tilldela dem efter behov. För att kunna allokera bokningarna tilldelas projektledaren uppgifterna från de allmänna resurserna till de namngivna resurserna och sedan används vyn **Avstämning** för att se till att allokeringen fungerar med bokningarna.

### <a name="edit-a-resource-requirement"></a>Redigera ett resurskrav

När ett resurskrav har skapats kan en projektledare eller en resursansvarig behöva redigera informationen för att förfina sökvillkoren när schemaläggningstavlan används. Följ stegen nedan om du vill redigera resurskravet.

1. På formuläret **Projekt** under fliken **Team** väljer du länken till alla krav på en generisk resurs.
2. I formuläret **Resurskrav** som visas anger du nödvändig information

   I formuläret **Resurskrav** kan projektledare eller resursansvariga även definiera färdigheter, roller, resurspreferenser samt önskad organisationsenhet.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Uppdatera resursbokningar efter att de har bokats i ett projekt

När du har lagt till en allmän eller namngiven resurs i ett projektteam kan du ändra resursens bokföring.

1. På formuläret **Projekt** under fliken **Team** väljer du en teammedlem och sedan **Underhåll bokningar**.
 
   Schemaläggningstavla visas och visar projektmedlemmens bokningar. Expandera teammedlemmens post om du vill visa vilka tider som har bokats i projektet och andra projekt som konsumerar teammedlemmens kapacitet.

2. Välj och dra bokningen för att utöka eller förkorta den. Dialogrutan **Skapa resursbokning** öppnas där du kan justera bokningen.
3. Högerklicka på bokningen. Sedan kan du använda snabbmenyn för att utföra följande åtgärder:

    - Ändra bokningsstatus
    - Redigera bokningen
    - Ersätt en resurs i projektteamet.

### <a name="change-the-booking-status"></a>Ändra bokningsstatus

Du kan ändra vilken status som helst för alla standard- eller anpassade bokningar.

Följande statusar ingår i Project Operations:

- **Annullerad**: avbryter en resursbokning och frigör resursens kapacitet.
- **Fasta bokningar**: förbrukar en resurs kapacitet. En bokning har vanligtvis denna status när du öppnar **Underhåll bokningar** från rutnätet **Alla teammedlemmar** på formuläret **Projekt**.
- **Preliminär bokning**: lägger till en resurs i ett team, men förbrukar inte resursens kapacitet. Den här statusen indikerar att resursen har reserverats för potentiellt arbete men fortfarande har kapacitet för andra jobb. I vyn över övergripande resurstillgänglighet får preliminära bokningar annan status än fasta bokningar.
- **Föreslagen**: representerar resursansvariges eller projektledarens förslag för en resurs. Förslag förbrukar inte resursens kapacitet och resursen läggs inte till i projektteamet. Om du vill göra en fast bokning för resursen i teamet måste projektledaren godkänna förslaget.

### <a name="submit-resource-requests"></a>Skicka resursbegäranden

Resursbegäran används för att bära en begäran eller ett resurskrav som måste uppfyllas av en resursansvarig. För en generisk resurs som redan finns i teamet kan du skicka en resursbegäran direkt. En resursbegäran kan uppfyllas på två sätt:

- Den resursansvarige uppfyller direkt begäran. I det här fallet ersätts den generiska resursen av en fast bokning med en namngiven resurs.
- Resursansvarig föreslår en resurs för projektledaren och projektledaren godkänner eller avvisar den föreslagna resursen.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direkt uppfyllelse av resursbegäran

När ett resurskrav skapas kan en projektledare skicka en resursbegäran för en generisk resurs genom att välja resursen och sedan välja **Skicka begäran**. Kommentarer om resursen kan ges till den resursansvarige som uppfyller begäran. När begäran har skickats ändras fältet **status** för teammedlemmen till **skickad**. När resursansvarig fullföljer begäran ersätts den generiska teammedlemmen av den namngivna resursen i rutnätet **Alla teammedlemmar**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Använda ett resursförslag för resursbegäran

I stället för att direkt boka en resurs i en resursbegäran kan en resursansvarig föreslå resurs till projektledare. En resursansvarig kan använda det här alternativet om en exakt matchning för kraven inte är tillgänglig. När en resursansvarig föreslår en resurs ser projektledare fältet **Status** för den allmänna teammedlemmen ändras till **Måste granskas**.

Du kan visa den föreslagna resursen tillsammans med en visualisering av förslagets bokning. 

1. Dubbelklicka på teammedlemmen som har statusen **Måste granskas**. 
2. Välj fliken **Föreslagna resurser**.
3. Markera **acceptera alla förslag** för att acceptera alla föreslagna resurser eller **avvisa alla förslag** för att avvisa dem. Om du accepterar de föreslagna resurserna är de fast bokade i projektet som teammedlemmar och ersätter generiska resurser.

> [!NOTE]
> Du måste antingen acceptera eller avvisa alla föreslagna resurser. Du kan inte delvis acceptera eller avvisa dem.

### <a name="substitute-a-resource-on-the-project-team"></a>Ersätt en resurs i projektteamet.

Ibland måste en projektledare ersätta en teammedlem i ett projekt.

1. På formuläret **Projekt** under fliken **Team** väljer du den resurs som behöver en ersättning och sedan **Underhåll bokningar**.
2. Expandera resursen om du vill visa de projekt som den är tilldelad till.
3. Högerklicka på projektet och välj sedan **Ersättningsresurs**.
4. Om du känner till den resurs du vill ersätta den aktuella resursen med markerar du eller skriver namnet och väljer sedan **Tilldela igen**.

Eller. om du behöver söka efter en resurs utför du följande steg.

1. Välj **Sök ersättning**.

   Schemaassistenten visar en lista över tillgängliga ersättningar. I schemaläggningsassistenten kan du ytterligare filtrera tillgängliga resurser för att hitta en lämplig ersättare.

2. För att ersätta resursen, välj resursen och välj **ersättare**.   

   Bokningarna och tilldelningarna ersätts med den nya resursen.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Avstämning av bokningar och tilldelningar av teammedlemmar

För teammedlemmar kombineras inte bokningar och tilldelningar är löst kopplade. Med andra ord kan resurser ha tilldelningar, men inga bokningar, eller så kan de inte ha bokningar men inga tilldelningar. Vanligtvis justeras projektbokningar och tilldelningar så att resurserna har rätt kapacitet för att utföra sina aktivitetstilldelningar. Bokningarna kan emellertid vara baserade på tillgänglighet, och tidsinställningar för aktiviteter kan ändras när projektet fortsätter. Därför är den fria kopplingen av bokningar och tilldelningar flexiblare.

Project Operations har fliken **Avstämning** där projektledarna kan avstämma teammedlemmarnas bokningar och deras tilldelningar för sina projektteam.

Fliken **avstämning** visar bokningar och tilldelningar ned till nivån för enskilda uppgiftstilldelningen för varje teammedlem. Den visar antalet timmar i celler som kan representera tidsperioder från månader ned till dagar.

Fliken visar även en total nettosumma för projektet tillsammans med en total kolumn.

För varje resurs beräknar fliken en skillnad mellan en teammedlems bokningar och sammanslagningen av teammedlemmens aktivitetstilldelningar. Vi rekommenderar att skillnaden är 0 (noll). Det bör alltså inte finnas någon skillnad mellan bokningar och tilldelningar. Skillnader är färgade och tonade för att framhäva två villkor:

- **Underskott för bokning**: uppstår om en resurs har fler tilldelningar än bokningar. Eftersom denna kapacitet inte har reserverats kan en projektledare korrigera problemet genom att utöka resursens bokningar så att underskottet täcks.
- **Överflödiga bokningar**: inträffar när en resurs har bokats i projektet men inte tilldelats aktiviteter. Det här tillståndet kan vara acceptabelt i de fall då resursen togs i projektet före tilldelning av uppgifter. I andra fall är inte resursen planerad att tilldelas till uppgifter. I så fall bör projektledaren överväga att annullera resursbokningarna så att kapaciteten kan användas för ett annat projekt.

I vissa fall kan du se en nettoskillnad på noll för en resurs när du visar tid på en högre nivå än dagnivå, t.ex. månadsnivå. Med andra ord, bokningar = tilldelningar. Om du visar tid på veckonivån kan du se att det finns tilldelningar på noll timmar och bokningar på 40 timmar under den första veckan men tilldelningar på 40 timmar och bokningar på noll timmar i den andra veckan i månaden. Generellt synkroniseras bokningarna och tilldelningarna, men de skiljer sig från en vecka till nästa.

När du visar högre tidsnivåer visar har celler i fliken **avstämning** har en indikator som meddelar att det finns olikheter på lägre nivåer. Dubbelklicka i en cell för att zooma in för att visa skillnaden. Du kan sedan högerklicka för att zooma ut. Genom att välja en resurs och sedan välja **Nästa skillnad** i verktygsfältet i rutnätet för att gå vidare till nästa skillnad mellan bokningar och tilldelningar för resursen. Välj **Föregående skillnad** om du vill gå tillbaka. Du kan också inaktivera skillnadsindikator och navigeringsbeteende under **inställningar**.

I situationer där du har uppgiftstilldelningar för en resurs men inga bokningar, på formuläret **Projekt** under fliken **Avstämning**, välj underskott för bokningen och sedan **Utöka bokning**. I dialogrutan **utöka bokning** visas och visar den bokning som behövs för att lösa resursens underskott. Dialogrutan visar även resursens befintliga bokningar för alla projekt eller andra schemalagda entiteter. Om du väljer **OK** för att skapa bokningen för resursen, oavsett resursens tillgänglighet, kan det leda till överbokning.

Projektledaren eller resursansvarig kan sedan använda schemaläggningstavlan för att hantera alla situationer där en resurs har blivit överbokad utanför sin kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]