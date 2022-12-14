---
title: Skapa resurstilldelningar
description: Den här artikeln innehåller information om hur du skapar generiska och namngivna resurstilldelningar.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812016"
---
# <a name="create-resource-assignments"></a>Skapa resurstilldelningar

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


En resurstilldelning är den direkta associeringen mellan en medlem i ett projektteam och en lövnodsuppgift. Den här artikeln innehåller information om de olika sätten att tilldela resurser.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Skapa en generisk teammedlem genom tilldelning av aktiveter


När du skapar en generisk teammedlem via uppgiftstilldelning skapar du en platshållare eller en generisk resurs. Denna generiska resurs som beskriver egenskaperna för den namngivna resurs du i slutändan vill ska arbeta med uppgifterna. Därefter skapar du ett krav, eller skickar in en begäran med hjälp av kravet, som används för att söka och boka den namngivna resursen.

1. I rutnätet Schema för en uppgift väljer du ikonen du Resurs i cellen **Resurs**.
2. Ange ett namn som utgör resursnamnet för platshållaren. Till exempel Programhanterare.
3. Välj **skapa** och ange rollen för den generiska resursen i fältet **Snabbregistering av projektteammedlem**.
4. Tilldela uppgifter efter behov till denna platshållarresurs genom att välja resursen i uppgiftens **resursväljare**. Resurserna listade under **Teammedlemmar**.
5. När du är klar med att tilldela den generiska resursen väljer du den generiska resursen i fliken **Team** och sedan **Generera krav** för att skapa ett resurskrav för den generiska resursen.
6. Välj **Boka** för den generiska resursen. Du kan sedan använda schemaläggningstavlan för att söka efter och boka en riktig resurs. Du kan också skicka in kravet för expediering genom en resursansvarig.
7. När den generiska resursen är helt uppfylld med en namngiven resurs tas den generiska resursen bort från teamet. (Uppfyllelse av partiellt resurskrav kommer inte att resultera i en resurstilldelning.) Uppgiftstilldelningarna för den generiska resursen tilldelas den namngivna resursen som uppfyllde den generiska resursens resurskrav.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tilldela en namngiven resurs från listan över alla bokningsbara resurser

Du kan använda sökrutan i **resursväljaren** för att söka efter alla aktiva bokningsbara resurser och tilldela dem till en lövnodsuppgift. Resurser som är tilldelade detta sätt läggs till i teamet utan att behöva boka. Detta påminner om att lägga till en teammedlem och välja **Ingen** som allokeringsmetod. Resursen visas på flikarna **Team**, **Resurstilldelning** och **Avstämning** som resurser med endast tilldelningar och ett bokningsunderskott. Schemalägg dem om du vill använda deras tillgänglighet.

1. Navigera till cellen **Tilldelad till** från uppgiftsrutnätet, tavlan eller tidslinjen.
2. Börja med att skriva ett namn i sökrutan. Sökresultaten för namnet visas i resursväljaren under **resursväljaren** under **andra resurser**.
3. Välj den resurs du vill tilldela uppgiften eller välj namnet på resursen under **Andra teamresurser**.

## <a name="editing-resource-assignment-contours"></a>Redigera resurstilldelningsprofiler

När resurser tilldelas en uppgift i schemat fördelas resursernas insats linjärt till varje resurs, baserat på resursens arbetstid och projektets schemaläge. En projektledare kan använda resurstilldelningsrutnätet för att förfina arbetet för varje resurs som har tilldelats en eller flera uppgifter på olika tidsskalan. Med hjälp av den här funktionen kan projektansvariga skapa bättre kostnader och intäkter, vilket beror på de resurstilldelningar som skapas när en resurs tilldelas en uppgift. Dessutom kan projektansvariga lättare återspegla den resurskrav som krävs för att skapa en resurs för att skapa en resurs.

### <a name="navigation"></a>Navigering

För att komma åt konturredigeringsrutnätet väljer projektledaren först fliken **Uppgifter** på projektets huvudsida och väljer sedan fliken **Tilldelningar**.

![Fliken Tilldelningar på fliken Uppgifter på projektets huvudsida.](media/AssignmentGrid.png)

Rutnätet stöder två metoder för att gruppera: **gruppera efter resurs** och **gruppera efter uppgift**. Till skillnad från i rutnätsvyn är kolumner inte konfigurerbara. De enda synliga kolumnerna är **Tilldelad till**, **Uppgiftsnamn**, **Tilldelningsstart**, **Tilldelningsslut** och **Tilldelningsinsats**.

När rutnätet först renderas startar det vid första tilldelningen. Om schemat inte innehåller några försökstilldelningar blir rutnätet tomt och inget renderas.

![Tomt tilldelningsrutnät.](media/emptyassignmentgrid.png)

Om du vill visa information om resurstilldelningar och olika tidsskalor finns det skrivskyddade resurstilldelningsrutnätet och resursallokeringsrutnätet tillgängliga.

### <a name="resource-calendars"></a>Resurskalendrar

Möjligheten att redigera en dag styrs av resursens arbetsdagar, vilket återspeglas i kalendern. Om en cell är inaktiverad för en viss resurs har resursen inte arbetsdagar under den perioden.

Resursens varaktighet kan sträcka sig utanför den tilldelade uppgiftens aktuella start- och slutdatum. Om en resurs uppdateras så att den inträffar efter det senaste slutdatumet för en uppgift eller det första startdatumet för en uppgift, ändras uppgiftens slutdatum eller startdatum efter behov. Om en resurs uppdateras tidigare än startdatum för en uppgift som har kopplats till ett fel, kan uppdateringen dock inte genomföras eftersom tilldelningen utlöser uppgiftens start innan åtgärdens funktion har slutförts och funktionen stöds för närvarande inte.

### <a name="co-authoring"></a>Medförfattare

Ändringar i resurstilldelningsrutnätet återspeglas automatiskt i alla associerade vyer, inklusive diagram-, tidslinje-, styrelse- och rutnätsvyer. Om flera användare granskar projektet samtidigt kommer alla ändringar som en användare gör att reflekteras i rutnätet. Omvänt visas alla ändringar som görs i resurstilldelningsrutnätet för alla andra användare som visar projektet i samma session.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
