---
title: Utgiftsspecificering
description: I den här artikeln beskrivs hur du specificerar utgifter med den nya arbetsytan för utgifter.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920956"
---
# <a name="expense-itemization"></a>Utgiftsspecificering

[!include [banner](../includes/banner.md)]

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Organisationer kräver ofta att anställda ger en detaljerad uppdelning av de utgifter som uppstått under resan. Ett hotell kan till exempel innehålla flera specificerade rader med rumspris, moms, parkering och andra diverse utgifter som uppstår varje dag under hela tiden. Eller utgifter för måltider kan krävs att du ger en mer detaljerad uppdelning för frukost, lunch eller middag. Oavsett organisationens behov kan varje utgiftskategori konfigureras så att den återspeglar de underkategorier eller radobjekt som utgör en utgift. Även om det alltid har funnits stöd för specificering i **Utgiftshantering**, möjliggör den nya arbetsytan för **utgifter** effektivare specificering när funktionen **Möjlighet att specificera återkommande utgifter snabbt** är aktiverad.  

## <a name="enable-quick-itemization"></a>Aktivera snabbspecificering 

Du kan använda funktionen **Möjlighet att specificera återkommande utgifter snabbt** för att specificera återkommande utgifter snabbt, samtidigt som du inte behöver ange dagliga utgifter varje gång för hela vistelsen. Aktivera snabbspecificering genom att följa stegen nedan.

1. Gå till arbetsytan **Funktionshantering** och i listan över funktioner lokaliserar du och väljer **Nya utgiftsrapporter**. 
2. Välj **Aktivera nu**. 
3. I funktionslistan lokaliserar och väljer du **Möjlighet att specificera återkommande utgifter snabbt**.
4. Välj **Aktivera nu**. 

## <a name="itemization-grid"></a>Rutnät för specificering 

Om en utgiftskategori har underkategorier eller olika komponenter som utgör utgiften kan den specificeras. Om du vill specificera en utgift väljer du utgiftsraden i utgiftsrapporten och i fönstret **Utgiftsdetaljer** väljer du **Åtgärder** > **Specificera**. Skjutreglaget **Specificering** visar ett rutnät av fält. Följande tabell innehåller ett exempel på varje fält i rutnätet och hur fältet renderas i utgiftsrapporten. 

|     Fält          |     Description                                                                                  |     Exempel              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Underkategori    |     Listan över underkategorier som konfigurerats under utgiftskategoritypen **Hotell**.             |     Dagspris för rum      |
|     Startdatum     |     Det datum då utgiftsartikeln först uppstod.                                           |     09/13/2021           |
|     Dagspris     |     Det belopp som uppstått för utgiftsartikeln.                                                    |     200                  |
|     Kvantitet       |     Antalet gånger debiteringen upprepas under en kontinuerlig period.                       |     3                    |

![Specificera utgift.](media/Itemization%20screen%201.png)

När du sparar en specificering visas en individuell, specificerad rad för kvantiteten som anges i rutnätet för specificering. Varje rad startar på det datum som anges i rutnätet.

![Specificerad rapport.](media/Itemization%20screen%202.png)

