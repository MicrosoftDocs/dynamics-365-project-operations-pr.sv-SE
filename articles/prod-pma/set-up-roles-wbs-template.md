---
title: Konfigurera roller i mallar för uppdelad arbetsstruktur
description: I det här ämnet finns information om hur du konfigurerar rollinformation i mallar för uppdelad arbetsstruktur.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
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
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a8363c1f94a974881df984869ee56bfc198ac5c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288671"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Konfigurera roller i mallar för uppdelad arbetsstruktur

[!include [banner](../includes/banner.md)]

Projektledarna kan skapa en mall för uppdelad arbetsstruktur (WBS) som de kan använda när de skapar WBS för nya projekt. Projektledarna kan lägga till roller när de skapar en mall. Följ stegen nedan om du vill tilldela en roll till en WBS-mall.

1. Välj **Projektledning och redovisning** > **Konfiguration** > **Projekt** > **Mallar för uppdelad arbetsstruktur**.
2. Välj **Detaljer** för en markerad WBS-mall.
3. Välj en uppgift i listan och i fältet **Roll** välj en roll för att tilldela uppgiften.

## <a name="work-with-a-wbs"></a>Arbeta med WBS

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
2. Välj **Plan** > **Aktiviteter** > **Uppdelad arbetsstruktur**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]