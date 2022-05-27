---
title: Hur tilldelar jag en bokningsbar resurs till en uppgift i webbappen
description: En översikt över olika sätt att tilldela bokningsbara resurser.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 0aaf7f69fa8ae081a74fbc4f18014686f625661c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578868"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Hur tilldelar jag en bokningsbar resurs till en aktivitet i webbappen (programmet Project Service v2.x)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Det finns två sätt att tilldela en resurs till en aktivitet i Project Service. Du kan schemalägga en resurs som en teammedlem och sedan tilldela den till en aktivitet. Du kan också skapa en allmän teammedlem genom tilldelning av roller för uppgifter, skapa ett team och sedan uppfylla underlagskraven med en namngiven resurs.

Observera att om du vill tilldela en aktivitet en bokningsbar resurs så måste den bokningsbara teammedlemmen ha tillräckligt med tillgängliga bokningar. Bokningsstatusen måste vara av bekräftelsetypen Fast bokning och med statusen Bekräftad. Om det inte finns tillräckligt med bokningar för resursen kommer Project Service att ta bort tilldelningen och visa följande felmeddelande:

*Det gick inte att tilldela en resurs till aktiviteten - Följande resurs(er) har inte tillräckligt antal timmar bokade för projektet*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Boka en resurs som en teammedlem och tilldela sedan resursen till en aktivitet

Med den här metoden kan du lägga till en resurs i projektteamet och sedan tilldela uppgifter till resursen i projektschemat. Så här gör du detta:
1.  Lägg till en ny teammedlem genom att välja **Nytt** i rutnätet för teammedlem.
2.  Markera namnet på den bokningsbara resursen och ange en roll i fönstret Snabbregistrering av teammedlem.
3.  Välj **Från**- och **Till**-datum.

    > [!div class="mx-imgBorder"] 
    > ![Skärmbild av lägga till teammedlem.](media/FAQ-Resources-to-Tasks2-1.png "Skärmbild av lägga till teammedlem")
 
4.  Välj en av följande tilldelningsmetoder för bokning av resursen:
    - **Full kapacitet** bokar resursens fulla kapacitet för angivna från- och till-datum.
    - **Procentandelskapacitet** bokar resursen under en viss procentandel av resursens kapacitet för angivna från- och till-datum.
    - **Efter timmar - fördela jämnt** bokar resursen under ett angivet antal timmar och fördelar tiden jämnt per dag under angivna från- och till-datum.
    - **Efter timmar - Tidigareläggning** bokar resursen under ett angivet antal timmar och tidigarelägger timmarna per dag under angivna från- och till-datum.

    Välj inte **Ingen** eftersom detta lägger till resursen i teamet men inte skapar några bokningar som tar upp resursens kapacitet.
5.  Välj **Spara**.

    Observera att tiderna för bokningen måste täcka insatstimmar och tidsintervall för de uppgifter som du tilldelar resursen till. Om så inte är fallet kan du inte tilldela resursen till aktiviteten.

6.  Klicka på listrutan för resurscellen i uppgiftens uppdelade arbetsstruktur (WBS). Därefter: 

    1. Markera **Lägg till**.
    2. Välj listrutan under **Resurser** och välj den teammedlem som du just skapade.
    3. Välj **OK**. Teammedlemmen har nu tilldelats till aktiviteten.

    > [!div class="mx-imgBorder"] 
    > ![Skärmbild av lägga till resurser med WBS.](media/FAQ-Resources-to-Tasks2-2.png "Skärmbild av lägga till resurser med WBS")
 
I rutnätet för teammedlem visas summan av resursens tilldelade timmar under Tilldelade timmar. Denna är mindre än eller lika med bokat antal timmar för resursen. 

> [!div class="mx-imgBorder"] 
> ![Skärmbild av tilldelade timmar för en resurs.](media/FAQ-Resources-to-Tasks2-3.png "Skärmbild av tilldelade timmar för en resurs")
 
Om den aktivitet som du försöker tilldela till resursen startas efter resursbokningarnas slutdatum kommer resursen inte att visas i listrutan.

Observera att du kan tilldela en resurs till fler timmar än deras bokade timmar om resursen har viss återstående, icke-tilldelad kapacitet. I det fallet kopplas resursen endast delvis till deras bokningar. Du kan se dessa återstående, icke-tilldelade uppgiftstimmar genom att lägga till kolumnen Obemannade timmar i den uppdelade arbetsstrukturen.

Om resurser har tilldelats till deras bokade timmar (deras bokade timmar är lika med deras tilldelade timmar) visas följande felmeddelande när du försöker tilldela dem ytterligare uppgifter:

*Det gick inte att tilldela en resurs till aktiviteten - Följande resurs(er) har inte tillräckligt antal timmar bokade för projektet.*

Dessutom läggs den teammedlem som utgör förvald projektledare till i teamet utan bokningar när du skapar projektet, och kan heller inte tilldelas till en aktivitet. De visas inte i resurslistrutan för aktiviteter.

Om du vill tilldela den här resursen måste du ta bort dem från teamet och sedan lägga till dem igen med en tilldelningsmetod som inte är "Ingen". Orsaken till att de läggs till i teamet när projektet skapas är så att ett projekt har minst en projektgodkännare som standard.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Skapa en allmän teammedlem genom tilldelning av roller för uppgifter

Denna metod garanterar att resurser har tillräckligt med bokningar för aktiviteter. Först måste du skapa en platshållare eller generisk resurs som beskriver egenskaperna för den namngivna resurs du i slutändan vill ska arbeta med uppgifterna genom att skapa ett team efter tilldelning av roller till uppgifter. Så här gör du detta:

1. Välj en uppgift i den uppdelade arbetsstrukturen.
2. Välj ikonen för listruta för **Tilldelad roll** i resurscellen.
3. Välj listrutan **Roll** och markera rollen för den generiska resursen.
4. Välj **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Skärmbild av använda WBS för att lägga till resurser.](media/FAQ-Resources-to-Tasks2-4.png "Skärmbild av använda WBS för att lägga till resurser")
 
När du är klar med att tilldela roller för aktiviteterna i WBS markerar du **Skapa projektteam**. Project Service skapar det lägsta antalet generiske teammedlemmar utifrån rollerna, söker organisationsenheter och organiserar projektkalendern genom att samla in aktivitetens tilldelningar.

> [!div class="mx-imgBorder"] 
> ![Skärmbild på hur du skapar ett projektteam.](media/FAQ-Resources-to-Tasks2-5.png "Skärmbild på hur du skapar ett projektteam")
 
I rutnätet Teammedlem ser du resurser av typen Allmän resurs, med namn på roll och befattning. Om två resurser behövs för att en roll ska kunna slutföra arbetet skapar funktionen Skapa team två teammedlemmar och avgränsar dessa med hjälp av befattningens namn.

> [!div class="mx-imgBorder"] 
> ![Skärmbild av att lägga till två allmänna resurser.](media/FAQ-Resources-to-Tasks2-6.png "Skärmbild av att lägga till två allmänna resurser")
 
Du kan öppna kravet på underliggande resurs för allmän teammedlem genom att välja länken under Resurskrav.

> [!div class="mx-imgBorder"] 
> ![Skärmbild av öppna krav för underliggande resurs.](media/FAQ-Resources-to-Tasks2-7.png "Skärmbild av öppna krav för underliggande resurs")

Välj **Boka** för den generiska resursen. Du kan sedan använda schemaläggningstavlan för att söka efter och boka en riktig resurs. Du kan också skicka in kravet för expediering av resursansvarig genom att välja **Skicka begäran**.

Om den generiska resursen har kompletterats med en namngiven resurs tas den generiska resursen bort från teamet, och aktivitetstilldelningarna för den generiska resursen tilldelas den namngivna resurs som uppfyllt den generiska resursens resurskrav.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
