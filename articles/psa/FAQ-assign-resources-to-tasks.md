---
title: Tilldela en resurs till en uppgift
description: I det här ämnet finns information om hur du tilldelar resurser till uppgifter.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b7aef799ec4b90d602a6f3641cbac06264664f00
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125155"
---
# <a name="assign-a-resource-to-a-task"></a>Tilldela en resurs till en uppgift

Det finns tre sätt att tilldela en resurs till en aktivitet i Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Boka en resurs som en teammedlem och tilldela sedan resursen till en aktivitet

Du kan lägga till en resurs i projektteamet och sedan tilldela resursen till uppgifter i projektschemat.

1. På fliken **teammedlem** lägger du till en ny teammedlem genom att välja **Nytt**. 

2. Då öppnas panelen för **snabbregistrering av teammedlem** där du kan markera bokningsbar resurs och ange en roll. 

    Välj en av följande tilldelningsmetoder för bokning av resursen:

    - **Full kapacitet** bokar resursens fulla kapacitet för angivna från- och till-datum.
    - **Procentandelskapacitet** bokar resursen under en viss procentandel av resursens kapacitet för angivna från- och till-datum.
    - **Efter timmar - fördela jämnt** bokar resursen under ett angivet antal timmar och fördelar dessa jämnt per dag under angivna från- och till-datum.
    - **Efter timmar - Tidigareläggning** bokar resursen under ett angivet antal timmar och tidigarelägger timmarna per dag under angivna från- och till-datum.
    - **Ingen** lägger till resursen i teamet men skapar inga bokningar som tar upp kapacitet.

3. På rutnätet **Schemalägg** välj ikonen **Resurs** i resurscellen och under **teammedlem** markerar du den teammedlem du precis har lagt till. 

> [!NOTE]
> På flikarna **Teammedlem** och **Avstämning** visar resursen bokade timmar och tilldelade timmar. Timmarna bör vara desamma men behöver inte vara det, detta eftersom bokningar och tilldelningar inte är nära sammankopplade. Fliken **Avstämning** ger dig information om huruvida de varierar, till exempel när du tilldelar en resurs fler timmar än du har bokat. Om det behövs kan du korrigera denna information för att vidta korrigeringsåtgärder, antingen genom att utöka resursens bokningar eller ändra tilldelningen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Skapa en generisk teammedlem genom tilldelning av aktiveter

När du skapar en generisk teammedlem genom uppgiftstilldelning måste du skapa en platshållare eller generisk resurs som beskriver egenskaperna för den namngivna resurs du i slutändan vill ska arbeta med uppgifterna. Därefter skapar du ett krav (eller skickar in en begäran med hjälp av kravet) som används för att söka och boka den namngivna resursen.

1. I rutnätet **Schema** för en uppgift markerar du **Resurs** i resurscellen.

2. Ange ett namn som utgör resursnamnet för platshållaren. Till exempel Programhanterare.

3. Välj **skapa** och ange rollen för den generiska resursen i fältet **Snabbregistering av projektteammedlem**.

4. Du kan fortsätta att tilldela aktiviteter till denna platshållarresurs genom att välja resursen i aktivitetens **resursväljare**. De är listade under **Teammedlemmar**.

5. När du är klar med att tilldela den generiska resursen markerar du den generiska resursen i **Team** och sedan **Generera krav** för att skapa ett resurskrav för den generiska resursen.

6. Välj **Boka** för den generiska resursen. Du kan sedan använda schemaläggningstavlan för att hitta och boka en verklig resurs. Du kan också skicka in kravet för expediering genom en resursansvarig.

7. Om den generiska resursen har kompletterats med en namngiven resurs tas den generiska resursen bort från teamet, och aktivitetstilldelningarna för den generiska resursen tilldelas den namngivna resurs som uppfyllt den generiska resursens resurskrav.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tilldela en namngiven resurs från listan över alla bokningsbara resurser

Du kan använda sökrutan i **resursväljaren** för att söka efter alla bokningsbara resurser och tilldela dem till en aktivitet.

Resurser som är tilldelade detta sätt läggs till i teamet utan att behöva boka. Detta påminner om att lägga till en teammedlem och välja ingen som allokeringsmetod. Resursen visas på flikarna **Team** och **Avstämning** som resurser med endast tilldelningar och ett bokningsunderskott. Schemalägg dem om du vill använda deras tillgänglighet.

1. I rutnätet **Schema** för en uppgift markerar du **Resurs** i resurscellen.

2. Börja skriva ett namn. Sökresultaten för namnet visas i resursväljaren under **resursväljaren** under **andra resurser**.

3. Välj resursen som du vill tilldela uppgiften.

