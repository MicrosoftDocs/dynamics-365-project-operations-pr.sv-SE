---
title: Importera beräkningar för ett projekt till en projektoffertrad
description: Det här ämnet ger information om hur du importerar produkter från ett projekt till en projektoffertrad.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae491495575ce2a5e4aaf0d8f22a14ea4b5e72de
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010223"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Importera beräkningar för ett projekt till en projektoffertrad

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


Om ett projekt skapas under stadiet före försäljning kan du välja att importera den ekonomiska uppskattningen från projektet till den projektbaserade offertraden.

1. Kontrollera att den projektbaserade offertraden har projektinformationen i fältet **Projekt**.
2. Under fliken **Offertradsinformaiton** väljer du **Importera från Projektuppskattning**.
3. Välj ett av följande sammanfattningsalternativ i dialogrutan som öppnas:

  - **Transaktionsklass**
  - **Kategori**
  - **Roll** 
  - **Projektuppgift**

Utifrån ditt val kopieras uppskattningen från projektet för alla transaktionsklasser som ingår i offertraden. Om du vill kontrollera vilka transaktionsklasser som är inkluderade väljer du fliken **Allmänt** på den projektbaserade offertraden och kontrollerar värdena för **Inkludera tid**, **Inkludera utgifter** och **Inkludera avgifter**.

När du importerar uppskattningar kommer systemet att använda prissättningen utifrån de projektprislistor som är kopplade till offerten och den faktureringstyp som angetts på den projektbaserade offertraden. Om en roll eller kategori konfigureras på den projektbaserade offertraden som icke debiterbar, sätts den importerade uppskattningsraden som icke debiterbar och kommer inte att motsvara offertvärdet på offertraden.

När en offertrad har radinformation sammanfattas fälten **Offertvärde** och **Uppskattad moms** på offertraden och kan inte redigeras.

När flera sammanfattningsalternativ har valts försöker systemet att sammanfatta med alla valda alternativ. Resultatet är att utdata från importerade offertrader blir fler än om du bara valde ett sammanfattningsalternativ.

Om projektet till exempel har följande uppskattningsrader för utgifter.

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| Uppgift B | Hotell | 10/1/2020 | 4 | 200 | 800 |
| Uppgift C | Hotell | 11/1/2020 | 2 | 200 | 400 |

När användaren väljer att sammanfatta efter transaktionsklass kommer följande information att importeras.

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

När användaren väljer att sammanfatta efter transaktionsklass och kategori kommer följande information att importeras.

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| | Hotell | 10/1/2020 | 6 | 200 | 1200 |

När användaren väljer att sammanfatta efter transaktionsklass, kategori och lövnodsuppgift kommer följande information att importeras. Observera att resultatet är samma som det som fanns i projektet.

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| Uppgift B | Hotell | 10/1/2020 | 4 | 200 | 800 |
| Uppgift C | Hotell | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
