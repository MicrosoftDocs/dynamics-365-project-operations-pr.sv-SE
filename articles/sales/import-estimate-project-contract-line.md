---
title: Importera en uppskattning till en projektbaserad kontraktrad
description: I det här ämnet finns information om hur du importerar uppskattningar från ett projekt till en kontraktrad.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f8d9637e4a8bd09664c43ccc2b02514dc825997e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010268"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importera en uppskattning till en projektbaserad kontraktrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I Dynamics 365 Project Operations kan du importera beräkningar från ett projekt till en projektbaserad kontraktrad.

1. Kontrollera att fältet **Projekt** på den projektbaserade kontraktraden är ifyllt.
2. Under fliken **Kontraktradsinformation** i underrutnätet väljer du **Importera från projektuppskattning**. En dialogruta med sammanfattningsalternativ öppnas. De tillgängliga alternativen för sammanfattning är **Transaktionsklass**, **Kategori**, **Roll** och **Projektuppgift**. Utifrån valen för sammanfattning val kopieras uppskattningen från projektet för alla transaktionsklasser som ingår i kontraktraden. 
3. Om du vill kontrollera vilka transaktionsklasser som är inkluderade går du till fliken **Allmänt** på kontraktraden och kontrollerar värdena i fälten **Inkludera tid**, **Inkludera utgifter** och **Inkludera avgifter**.

När du importerar uppskattningar kommer programmet att använda prissättningen utifrån de projektprislistor som är kopplade till kontraktet och den faktureringstyp som angetts på kontraktraden. Om en roll eller kategori konfigureras på kontraktraden som icke debiterbar, sätts den importerade uppskattningsraden för rollen eller kategorin som icke debiterbar och kommer inte att motsvara kontraktvärdet på kontraktraden.

När en kontraktrad har radinformation sammanfattas fälten **Kontraktvärde** och **Uppskattad moms** på kontraktraden och kan inte redigeras.

När flera sammanfattningsalternativ har valts försöker systemet att sammanfatta med alla valda alternativ. Resultatet av sammanfattningen resulterar i fler importerade kontraktrader än om du endast väljer ett sammanfattningsalternativ.

Om projektet till exempel har följande uppskattningsrader för utgifter:

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| Uppgift B | Hotell | 10/1/2020 | 4 | 200 | 800 |
| Uppgift C | Hotell | 11/1/2020 | 2 | 200 | 400 |

När användaren väljer att sammanfatta efter **Transaktionsklass** kommer följande information att importeras:

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

När användaren väljer att sammanfatta efter **Transaktionsklass** och **Kategori** kommer följande information att importeras:

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotell | 10/1/2020 | 6 | 200 | 1200 |

När användaren väljer att sammanfatta efter **Transaktionsklass**, **Kategori** och **Lövnodsuppgift** kommer följande att importeras. Observera att resultatet är samma som det som fanns i projektet:

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| Uppgift B | Hotell | 10/1/2020 | 4 | 200 | 800 |
| Uppgift C | Hotell | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]