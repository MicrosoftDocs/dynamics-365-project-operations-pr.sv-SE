---
title: Skapa resurstilldelningar
description: I det här ämnet finns information om hur du skapar generiska och namngivna resurstilldelningar.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 829c1d1de7270e7cafbb98ef80235ae6404f77f7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131770"
---
# <a name="create-resource-assignments"></a>Skapa resurstilldelningar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


En resurstilldelning är den direkta associeringen mellan en medlem i ett projektteam och en lövnodsuppgift. I det här ämnet finns information om de olika sätten för att tilldela resurser.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Skapa en generisk teammedlem genom tilldelning av aktiveter


När du skapar en generisk teammedlem via uppgiftstilldelning skapar du en platshållare eller en generisk resurs. Denna generiska resurs som beskriver egenskaperna för den namngivna resurs du i slutändan vill ska arbeta med uppgifterna. Därefter skapar du ett krav, eller skickar in en begäran med hjälp av kravet, som används för att söka och boka den namngivna resursen.

1. I rutnätet Schema för en uppgift väljer du ikonen du Resurs i cellen **Resurs**.
2. Ange ett namn som utgör resursnamnet för platshållaren. Till exempel Programhanterare.
3. Välj **skapa** och ange rollen för den generiska resursen i fältet **Snabbregistering av projektteammedlem**.
4. Tilldela uppgifter efter behov till denna platshållarresurs genom att välja resursen i uppgiftens **resursväljare**. Resurserna listade under **Teammedlemmar**.
5. När du är klar med att tilldela den generiska resursen väljer du den generiska resursen i fliken **Team** och sedan **Generera krav** för att skapa ett resurskrav för den generiska resursen.
6. Välj **Boka** för den generiska resursen. Du kan sedan använda schemaläggningstavlan för att söka efter och boka en riktig resurs. Du kan också skicka in kravet för expediering genom en resursansvarig.
7. När den generiska resursen har uppfyllts helt och hållet (delvis uppfyllt resurskrav leder inte till resurstilldelning) med en namngiven resurs tas den generiska resursen bort från teamet. Uppgiftstilldelningarna för den generiska resursen tilldelas den namngivna resursen som uppfyller den generiska resursens resurskrav.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tilldela en namngiven resurs från listan över alla bokningsbara resurser

Du kan använda sökrutan i **resursväljaren** för att söka efter alla aktiva bokningsbara resurser och tilldela dem till en lövnodsuppgift. Resurser som är tilldelade detta sätt läggs till i teamet utan att behöva boka. Detta påminner om att lägga till en teammedlem och välja **Ingen** som allokeringsmetod. Resursen visas på flikarna **Team**, **Resurstilldelning** och **Avstämning** som resurser med endast tilldelningar och ett bokningsunderskott. Schemalägg dem om du vill använda deras tillgänglighet.

1. Navigera till cellen **Tilldelad till** från uppgiftsrutnätet, tavlan eller tidslinjen.
2. Börja med att skriva ett namn i sökrutan. Sökresultaten för namnet visas i resursväljaren under **resursväljaren** under **andra resurser**.
3. Välj den resurs du vill tilldela uppgiften eller välj namnet på resursen under **Andra teamresurser**.
