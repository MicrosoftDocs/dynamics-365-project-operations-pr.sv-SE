---
title: Resurshantering för projekt
description: I det här ämnet finns information om resurshantering för projekt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756152"
---
# <a name="project-resourcing"></a>Resurshantering för projekt

[!include [banner](../includes/banner.md)]

I det här ämnet finns information om resurshantering för projekt.

En utmaning för projektledarna och resurshanterare under projektplaneringsfasen är resursallokering, där de måste bestämma och reservera rätt resurs för att arbeta med ett projekt. I Dynamics 365 Finance kan du med hjälp av omdirigeringsfunktioner för projekt definiera roller som behandlas som tillfälliga resurser och som kan reserveras för ett specifikt åtagande eller en del av ett ärende. Med den här typen av resurshantering kan projektledarna och resursansvariga utföra följande uppgifter:

- Definiera en roll som har den kompetens som krävs, så att det är lätt att matcha resurser.
- Använd roller för att definiera ett engagemangsschema som bygger på reserverade resurser.
- Uppskatta kostnader och fastställa en ursprunglig budget utifrån tilldelade roller och resurser för ett projekt.
- Använd roller för att uppskatta antalet resursreservationer som krävs för varje ärende.
- Uppskatta antalet resurser som krävs under hela livscykeln för ett projekt.
- Skapa ett utkast till en uppdelad arbetsstruktur med hjälp av de första resurstilldelningarna.

[![Projektets livscykel](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

När projektplaneringen fortsätter kan planerade resurser ersättas med personalresurser. Projektledaren kan också gå tillbaka och uppdatera resurshanteringsreservationerna under alla projektstadier.

## <a name="set-up-project-resources"></a>Konfigurera projektresurser
Du måste ange en kalender och associera den med en medarbetare eller arbetare. Kalendern används för att schemalägga projektet och arbetstiden för de resurser som reserveras för projektet. Under kalenderinstallationen kan projektledarna göra resursutjämning som en del av resursoptimeringen. Begränsningar kan anges för resurser utifrån kalenderschemat. Du kan skapa en kalender på sidan **kalendrar**.

När du konfigurerar en arbetare som en projektresurs kan du välja bland arbetare som arbetar i det företag som du konfigurerar resurser för. Alternativt kan du välja arbetare från andra företag i organisationen. Dessa arbetare kallas för koncerninterna resurser.

I följande procedurer förklaras hur du konfigurerar en arbetare som en projektresurs i företaget och hur du skapar en koncernintern projektresurs.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurera en arbetare som en projektresurs

1. På sidan **arbetare** i listan **arbetare** väljer du den arbetare som du vill lägga till som en projektresurs i listan arbetare och öppnar sedan arbetarens post.
2. I åtgärdsfönstret, välj **Projekt** &gt; **Inställning** &gt; **Projektinställningar**.
3. Välj en kalender och stäng sidan.

Du kan även ange standardprojekt för en resurs som en typ av förtilldelning. Förtilldelningar kan användas när resurs chefen eller projektledaren vet vilka projektresursen kommer att arbeta i förväg. Förtilldelningar kan också baseras på en förfrågan från en projekt sponsor eller kund. Om du vill förtilldela ett projekt fördelat på sidan **Tilldela projekt** på fliken **Projekt** i listan **Återstående projekt** välj lämpligt projekt.

### <a name="set-up-an-intercompany-resource"></a>Konfigurera en koncernintern resurs

När du konfigurerar en arbetare som en koncernintern resurs måste du fylla i inställningarna både i långivande bolaget och låntagande bolaget.

**I långivande bolaget**

1. I Finance kontrollera att långivande bolaget är valt och slutför proceduren i det föregående avsnittet "Konfigurera en arbetare som projektresurs".
2. På sidan **Koncernintern redovisning** klicka på **Ny**.
3. I fältet **juridisk person-ID**välj långivande bolag. Fyll i de återstående fälten efter behov och välj sedan **Spara**.
4. På sidan **Överföringspris** klicka på **Ny**.
5. I fältet **låntagande juridisk person** välj rätt bolag.
6. Om du vill låna ut till det låntagande bolaget endast till den resurs du skapade i början av det här avsnittet markerar du i fältet **resurs** namnet på den resurs som du har skapat. För att göra alla resurser i det långivande bolaget tillgängligt för det låntagande bolaget, lämna fältet **Resurs** tom.
7. På sidan **Projektledning och redovisningsparametrar** på fliken **Koncerninternt** ange alternativet **Aktivera koncernintern resursschemaläggning och tidrapport** till **Ja**.

**I låntagande bolaget**

- På sidan **Resurslista** i sökfiltret ange namnet på den resurs som du skapade för det långivande bolaget för att verifiera att namnet ingår i resurslistan för det långivande bolaget.

## <a name="manage-resource-competencies"></a>Hantera resurskompetens
Resurskompetens är en viktig del av resurshanteringen. Kompetenser kan användas som en grundnivå för att fastställa resurser som har rätt balans mellan färdigheter, utbildning, certifiering och projekterfarenhet. Du bör ange den här informationen för varje resurs och uppdatera den med jämna mellanrum. På det här sättet kan du maximera funktioner när specifika resurskompetenser matchas vid projekttilldelning.

[![Exempel på kunskaper, certifieringar, utbildning och projekterfarenheter](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

I följande procedurer förklaras hur du konfigurerar en del av kompetenserna för en resurs.

Om du vill ange kompetenser för en arbetare kan du antingen använda listsidan **Arbetare** i personal eller listsidan **Resurser** i projekthantering och redovisning. För följande procedurer används listsidan **Arbetare** i personal.

### <a name="set-up-competencies-certificates"></a>Konfigurera kompetenser: certifikat

1. På listsidan **arbetare** markerar du den rad där arbetaren ska lägga till intygsinformation för.
2. I åtgärdsfönstret på fliken **Arbetare** i gruppen **Kompetenser** välj **Certifikat**.
3. Välj **Ny** och sedan i fältet **Certifikattyp** väljer du **PMP**.
4. I fältet **Startdatum** välj **10/1/2015** och välj **Spara**.

### <a name="set-up-competencies-skills"></a>Konfigurera kompetenser: färdigheter

1. Listsida **Arbetare**, se till att den arbetare som du använde i föregående procedur fortfarande är vald. I åtgärdsfönstret på fliken **Arbetare** i gruppen **Kompetenser** välj **Färdigheter**.
2. Välj **Nytt**.
3. I fältet **Färdighet** välj **Projekthantering**.
4. I fältet **Nivå** välj **5 Expert**.
5. I fältet **Nivådatum** välj **1-/14/2014**.
6. I fältet **År av erfarenhet** ange **10**.
7. Klicka på **Spara** och stäng sedan sidan.

## <a name="create-a-new-project"></a>Skapa ett nytt projekt
1. På sidan **Projekthantering** välj **Ny projekt** och ange följande värden:

    - **Projekttyp:** tid och material
    - **Projektnamn:** XYZ uppgraderingsfas 2
    - **Projektgrupp:** TM\_WIP
    - **Projektkontrakt-ID:** 00000002

2. Välj **Skapa projekt**.

### <a name="assign-a-resource-to-a-project"></a>Tilldela en resurs en projekt

1. På sidan **arbetare** i listan **arbetare** välj posten för den arbetare som du tidigare har ställt in kompetenser för och öppna arbetarposten.
2. I åtgärdsfönstret på fliken **Projekt** i gruppen **Inställning** välj **Tilldela projekt**.
3. På sidan **Tilldelning av resursvalideringsprojekt** på fliken **Projekt** i fältet **Lägg till projektet i utvalda projekt** i projektet **XYZ uppgradering fas 2**.
4. I fönstret **Återstående projekt**, välj ett projekt och välj sedan pilknappen för att lägga till det i rutan **Valda projekt**.

Du kan även tilldela kategorier för en resurs som du behöver. Kategoritypen är antingen **kostnad** eller **intäkt**. Kategoritypen bestäms av din organisation. Om du inte har tilldelats några kategorier för en resurs slår Finance upp kategorin som standard för timkostnader för kostnader och intäkter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Ange egenskaper för projektresurser och roller

En projektledare kan använda projektets källfunktioner för att skapa de roller som krävs för projektet. Roller kan användas om bekräftade resurser fortfarande är okända när resurser reserveras. Roller kan tillfälligt reserveras som planerade resurser så att du kan fortsätta med projektplaneringsfaserna.

[![Exempel på en roll](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso anställdes för att slutföra ett tids- och materialprojekt som har en godkänd projektstadgar. Juniorprojektledaren håller fortfarande på att slutföra projektets omfattning. Resurshanteraren identifierar just nu specifika resurser som ska reserveras för att fungera i det nya projektet. På grund av projektets kritiska karaktär begärde projektsponsor chefsprojektledare som en av rollerna. Resurshanteraren måste skaffa den nya resursen och definiera rollen i systemet om oerfarna projektledare kräver resursinformationen under projektplanering.

I följande steg visas hur resurshanteraren kan konfigurera rollen som ansvarig för projektchefen och associera resursegenskaper med den. Senare kan rollen användas för att söka efter tillgängliga resurser som matchar de begärda resurskompetenserna.

1. På sidan **Konfigurera roller** välj **Ny** och ange följande värden:

    - **Roll-ID:** chefsprojektledare
    - **Beskrivning:** chefsprojektledare

2. Välj **Skapa**.
3. Välj rollen **Chefsprojektledare** och välj sedan **Konfigurera egenskaper**.
4. I fältet **Egenskapstyp** välj **Färdighet**.
5. I fältet **Tillgängliga egenskaper** anger du den färdighet du vill söka efter.
6. I fältet **Egenskapstyp** välj **Certifikat**.
7. I fältet **Tillgängliga egenskaper** anger du den certifikattyp du vill söka efter.

### <a name="assign-a-project-resource-to-a-project"></a>Tilldela en projektresurs en projekt

1. På sidan **Alla projekt** välj **XYZ uppgradera fas 2** projekt.
2. På sidan **Projektgrupp och schemaläggning** välj **Lägg till**.
3. I fält **Roll** välj **Teammedlem**.
4. Välj **Boka från kalendern**.
5. På sidan **Resurstillgänglighet** väljer du **Vyinställningar**.
6. På sida **Justera vyinställningarna** ange följande värden:

    - **Format för datumintervall:** dag
    - **Visa tillgänglighetsbeskrivningar:** Ja
    - **Visa resterande kapacitet:** Ja

7. Välj en resurs i listan över resurser.
8. Välj **Fast bokning** och **Full kapacitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Tilldela en resurs till en standardroll

Om du vill att projekt eller resurshanterare ska kunna öka detaljnivån ytterligare information om vilka resurser som kan reserveras för ett projekt. Du kan associera en standardroll med en befintlig resurs eller en nyligen hämtad resurs. När till exempel Daniel har anställts har han erfarenheten och färdigheterna för rollen affärsanalytiker. Resurshanteraren har tilldelat rollen som Daniels standardroll. Därför lade resurshanteraren Daniel till i en pool av affärsanalytiker som är tillgängliga för att arbeta med projekt.

Vid resursreservationen kan projektledarna filtrera de rollresurser som är tillgängliga för arbete i projekt. De kan använda den här informationen som ett kriterium när de utför beslutsanalys med flera villkor när resurser är uppfyllda. De kan också lägga till andra resursegenskaper i filtret och söka efter resurser med specifika kunskaper, utbildning och erfarenheter för ett visst projekt.

**Scenario:** ett godkänt projekt har startats och rollen som chefsprojektledare reserverades som en planerad resurs under projektplaneringsfasen. Resurshanteraren har nu skaffat en resurs för att kunna utföra rollen som chefsprojektledare.

1. På sidan **Resurslista** välj **Daniel Goldschmidt**.
2. På sidan **Resursroll** välj **Ny** och ange följande värden:

    - **Giltig från:** Ange aktuellt datum.
    - **Förfallodatum:** ange **aldrig**.
    - **Roll:** Ange **chefsprojektledare**.

3. Klicka på **Spara** och stäng sedan sidan.
4. På fliken **kompetenser** lägger du till kompetensen **ProjectMgmt** och **PMP**-intyg.

## <a name="set-up-role-based-pricing"></a>Konfigurera rollbaserad prissättning
Alla kostnads-, försäljnings- och överföringspriser kan ställas in för roller.

1. På sidan **Försäljningspris (timma)** välj **Ny** och ange ett giltigt datum.
2. I kolumnen **Roll** välj en roll.
3. I kolumnen **Prissättning** ange ett pris för den valda resursrollen i kolumnen prissättning.

## <a name="form-a-project-team"></a>Forma ett projektteam
För att du ska kunna använda rollerna som har ställts in tidigare i ett projekt måste en projektledare associera rollerna med projektet. Flera roller kan tilldelas för ett projekt. För att undvika förvirring märks rollerna automatiskt under reservation. Om projektledaren t.ex. kräver tre programmerare är det tre programmerare som har **programmerare 1**, **programmerare 2** och **programmerare 3** när deras etiketter genereras automatiskt. Om rollegenskaperna tidigare har angetts för rollen används de som ett filter vid sökning efter en resurs. Ytterligare kännetecken kan läggas till som krävs för att sökningen ska kunna förfinas ytterligare.

Vyinställningar kan också anpassas så att du får en bättre bild av resurstillgängligheten. Det finns alternativ för att visa tim-, dygns-, vecko-, månads-, kvartals- och årstillgänglighet. Det finns även ett alternativ för att visa tillgänglig och återstående kapacitet för resurser. Det här alternativet är användbart vid tidshantering när du uppskattar tillgänglig tid för aktiviteter eller resurstillgänglighet.

Projektledaren kan välja en roll på sidan och om det finns en tillgänglig resurs som passar för kravet väljer du om du vill reservera en resurs som ska fylla rollen. Observera att resurserna inte behöver reserveras vid den här tidpunkten i planeringsfasen. När du skapar en struktur kan du ersätta roller med personalresurser för projektet. Om roller ersätts med personalresurser i WBS uppdateras projektets teamlista och schemaläggning automatiskt i resursinställningarna.

[![Projektteamlistor som innehåller både roller och faktiska resurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektledaren har olika alternativ för att boka en resurs för ett projekt, till exempel **återstående kapacitet**, **full kapacitet**, **kapacitetsprocent** och **ange timmar**. De här bokningsalternativen kan när som helst annulleras om resurstilldelningar ändras. Två typer av bokningar stöds:

- **Fast bokning** – resursreservationen har godkänts och bekräftats för att arbeta med åtagandet för den angivna varaktigheten.
- **Mjuk bokning** – resursreservationerna har godkänts och preliminärt angetts till att arbeta med åtagandet för den angivna varaktigheten.

Följande procedur förklarar hur du skapar ett projektteam.

### <a name="create-a-project-team"></a>Skapa ett projektteam

1. På listsidan **Alla projekt** välj ett projekt och välj sedan **Redigera**.
2. På fliken **Projektteam och schemaläggning** i fältet **Schemalägg slutdatum** ange startdatum för schemaläggning plus en månad. Om exempelvis schemats startdatum är 24 juni 2017 (24/06/2017) anger du **24/07/2017**.
3. Markera **Lägg till**.
4. I fältet **Lägg till roller i projekt** i fältet **Roll** väljer du **chefsprojektledare**.
5. Välj **nödvändig kompetens**.
6. På sidan **Välj egenskaper** är de egenskaper som du tidigare angett för rollen chefsprojektledare markerad som standard. Välj **OK**.
7. På sidan **Lägg till roller i projekt** i fältet **Antal resurser** ange **1**.
8. I fältet **resurs** visas alla resurser som har nödvändig kompetens i sökningen. Välj **Daniel Goldschmidt** och välj sedan **Skapa**.
9. På sidan **Projekt** välj **Lägg till**.
10. I fältet **Lägg till roller i projekt** i fältet **Roll** väljer du **teammedlem**. Ange **5** i fältet **Antal resurser**.
11. Välj **Skapa**.
12. På sidan **projekt** väljer du **uppfylla resurser**.

## <a name="resource-capacity-synchronization"></a>Synkronisering av resurskapacitet
Med hjälp av processerna för synkronisering av resurser kan du garantera att informationen för kalendern och baskalendern rinner ned i projektresursens schemaläggning. Om kalendern ändras gör processerna de nödvändiga uppdateringarna till schemaläggning av projektresurser. Processerna bidrar också till att förbättra prestanda eftersom kalenderns resursinformation synkroniseras i förväg. Uppdateringarna av resursplaneringsinformationen kan därför snabbare uppdateras. Vi rekommenderar att du schemalägger processerna som en batch i stället för en i taget. I annat fall kommer någon att glömma bort de ingående datumen när informationen senast synkroniserades. Om ingående datum inte används kan luckor uppstå vid synkronisering av datum.

![Synkronisering av kalender](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synkronisering av resurskapacitets sammanslagningar

Synkroniseringsprocessen synkroniserar all information i resurskalendern. Den här informationen inkluderar baskalenderinformation om eventuella ändringar i tabellen resurskalenderkapacitet för projektet. Om nya resurser läggs till i projektet hjälper synkroniseringen till att säkerställa att den uppdaterade kalenderinformationen är tillgänglig. Du kan utföra synkroniseringen när som helst.

Vi rekommenderar att du använder en batch. Alternativen är tillgängliga under synkroniseringen av kapacitetsreservationer.

1. Välj **Projektledning och redovisning** &gt; **Periodisk** &gt; **Synkronisering av kapacitet** &gt; **Synkronisering av resurskapacitets sammanslagningar**.
2. Ange alternativen visas i följande tabell.

    | Alternativ      | Beskrivning |
    |-------------|-------------|
    | Periodkod | Alternativt kan du välja en intervallkod för räkenskapsåret för att ange start- och slutdatum för synkroniseringsprocessen för resurskapacitets sammanslagningar. |
    | Startdatum  | Ange startdatum för synkroniseringsprocessen för resurskapacitets sammanslagning. |
    | Slutdatum    | Ange slutdatum för synkroniseringsprocessen för resurskapacitets sammanslagning. |

[![Synkroniseringsprocess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Ange roller i WBS-mallar
Projektledarna kan skapa en WBS-mall som de kan använda när de skapar en WBS för nya projekt. Projektledarna kan lägga till roller när de skapar en mall. Följ stegen nedan om du vill tilldela en roll till en WBS-mall.

1. Välj **Projektledning och redovisning** &gt; **Inställningar** &gt; **Projekt** &gt; **Mallar för uppdelad arbetsstruktur**.
2. Välj **Detaljer** för en markerad WBS-mall.
3. Välj en uppgift i listan och i fältet **Roll** välj en roll för att tilldela uppgiften.

### <a name="work-with-a-wbs"></a>Arbeta med WBS

Du kan skapa en helt ny WBS eller också kan du kopiera en WBS från en befintlig WBS-mall. En projektledare kan enkelt hantera resurserna genom att tilldela roller till nya uppgifter på WBS. Roller kan ersättas antingen efter att en resurs har anskaffats eller efter att en bekräftad resurs fungerar för uppgiften. Den här flexibiliteten gör att projektledarna kan utföra följande uppgifter:

- Identifiera antalet resurser som krävs för WBS-arbetspaket.
- Beräkna projektkostnader.
- Bestäm en preliminär budget.
- Beräkna varaktighet för aktiviteten utifrån roller och resurser.
- Utveckla några projekthanteringsplaner utifrån den tillgängliga projektinformationen.

Ytterligare alternativ har lagts till i strukturen för att bättre använda funktionen för resurshantering.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternativ</th>
<th>Beskrivning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resurstilldelningar</td>
<td>Visa de tilldelade resurserna, datumen, antalet timmar och bokningstypen för uppgifter i WBS.</td>
</tr>
<tr class="even">
<td>Autogenerera team</td>
<td>Lägga till planerade resurser automatiskt med hjälp av roller som är associerade med en uppgift. Finance föreslår automatiskt planerade resurser med hjälp av beslutsanalys med flera villkor som bygger på roller. När du har angett att rollerna och arbetsinsatsen (timmar) har ställts in för uppgifterna i WBS och efter att strukturen har släppts väljer du <strong>Skapa team automatiskt</strong>. Det obligatoriska antalet planerade resurser läggs till i WBS och fliken <strong>Projekt och teamschemaläggning</strong>.</td>
</tr>
<tr class="odd">
<td>Resurs (listruta)</td>
<td>På sidan <strong>starta resurstilldelning</strong> kan du välja resurser till en fast pärm eller en mjuk pärm, utifrån den angivna varaktigheten. Du kan ändra visningsinställningarna om du vill visa och ange varaktigheten för resursaktiviteterna. Du kan välja och tilldela resurser på arbetspaketnivån med hjälp av följande alternativ:
<ul>
<li><strong>Acceptera</strong> – Bekräfta ändringar av resursen som är tilldelad en aktivitet.</li>
<li><strong>Avbryt</strong> – Avbryt ändringar av resursen som är tilldelad en aktivitet.</li>
<li><strong>Tilldela automatiskt</strong> – en tillgänglig personalresurs som har en matchande roll väljs automatiskt och tilldelas den valda uppgiften.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På sidan **Alla projekt** välj **XYZ uppgradera fas 2** projekt.
2. Välj **plan** &gt; **aktiviteter** &gt; **uppdelad arbetsstruktur**.
3. Välj **ny** om du vill lägga till följande nivå ett-aktiviteter i WBS:

    - Initiera
    - Planering
    - Körs
    - Övervakning och kontroll
    - Stäng

4. Ange datum och tid (timmar) enligt illustrationen nedan.

    [![Ange datum och ansträngning](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Välj aktivitetsrad **initiering** och sedan i fältet **roll** välj **chefsprojektledare**.
6. Välj **Publicera**.
7. På samma rad i fältet **Resurs** välj **Daniel Goldschmidt** och välj sedan **Acceptera**.
8. Markera uppgiftsraden **Planera** och i fältet **Roll** väljer du **Affärsanalytiker**.
9. Välj **Publicera** och välj sedan **Skapa team automatiskt**.
10. I meddelandefältet som visas väljer du **Ja**.
11. Fältet **Resurs** kontrollera att värdet är **Affärsanalytiker 1**.
12. För resursen **Affärsanalytiker 1** öppna uppslaget och välj **Starta resurstilldelningar**. Välj sedan en arbetare för uppgiften.
13. Markera **Mjukt tilldela** &gt; **Full kapacitet**.

    > [!NOTE] 
    > Du får ingen varning om att den angivna resursen nu är 2 eftersom antalet resurser fortfarande är 1.

14. På sidan **Uppdelad arbetsstruktur** validerar du resurstilldelningen i WBS och väljer sedan **Spara**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resursuppfyllelse för planerade resurser
En projektledare kan planera nödvändiga resursroller för ett projekt. Resurshanteraren visar de här planerade resurserna som förfrågningar på sidan **Resursuppfyllelse** och kan tilldela verkliga resurser.

1. På sidan **Alla projekt** välj **XYZ uppgradera fas 2** projekt.
2. Välj **Projekt** och välj sedan **Redigera**.
3. På sidan **Projektgrupp och schemaläggning** välj **Lägg till**.
4. I dialogrutan **Lägg till roller** välj rollen **Programvaruutvecklare**.
5. Klicka på **Skapa** och stäng sedan projektsidan.
6. På sidan **Resursuppfyllelse** väljer du **Programvaruutvecklare 1** för projektet **XYZ uppgradering projektfas 2**.
7. Välj en arbetare och sedan **Tilldela**.
8. Kontrollera att raden för **programvaruutvecklare 1** har tagits bort för projektet **XYZ uppgradering projektfas 2**.
9. På fliken **Projektteam och schemaläggning** för projekt **XYZ uppgradera fas 2**, kontrollera att arbetaren som du valde i föregående steg har lagts till som **Programvaruutvecklare**.

## <a name="requests-for-project-resources"></a>Begäran för projektresurser
Med funktionerna för schemaläggning av projektresurser kan du bara distribuera personalresurser för åtaganden eller projekt. Aktivera den här funktionen genom att utföra följande uppgifter eller kontrollera att de har slutförts:

- Ställ in nummerserier.
- Ställ in arbetsflöden för projekthantering och redovisning.
- Aktivera arbetsflöden för resursförfrågan.

När föregående aktiviteter har slutförts kan du utföra följande uppgifter som du behöver:

- Skapa en resursförfrågan från en bemannad resurs med mjuka bokningar.
- Övervaka resursförfrågningar.
- Uppfyll resursförfrågningar.
- Begära en personalresurs från en WBS.
- Boka resurser i ett projekt utan att behöva begära en personalresurs.

## <a name="monitor-project-teams"></a>Övervaka projektteam
1. På sidan **All projekt** välj länken **projekt-ID** för projekt **XYZ uppgradering fas 2**.
2. Snabbflik **Projektgrupp och schemaläggning**, verifiera att de projektresurser som anges är korrekta.
