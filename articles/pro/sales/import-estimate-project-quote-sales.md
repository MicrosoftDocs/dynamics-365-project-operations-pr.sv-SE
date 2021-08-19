---
title: Importera beräkningar för ett projekt till en projektbaserad offertrad - lite
description: I det här ämnet finns information om hur du importerar uppskattningar från ett projekt till en offertrad.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5ac7827f3499aafb63f6bc0b8580ca52e883f272464532bd353170a12b3ae55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986153"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importera beräkningar för ett projekt till en projektbaserad offertrad 

_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_

Om ett projekt skapas under stadiet före försäljning kan du välja att importera den ekonomiska uppskattningen från projektet till den projektbaserade offertraden.

1. Kontrollera att den projektbaserade offertraden har projektinformationen i fältet **Projekt**.
2. Under fliken **Offertradsinformaiton** väljer du **Importera från Projektuppskattning**.
3. Välj ett av följande sammanfattningsalternativ i dialogrutan som öppnas.

  - **Transaktionsklass**
  - **Kategori**
  - **Roll** 
  - **Projektuppgift**

Utifrån ditt val kopieras uppskattningen från projektet för alla transaktionsklasser som ingår i offertraden. Välj den för att kontrollera vilka transaktionsklasser som ingår i fliken **Allmänt** på den projektbaserade offertraden och kontrollera värdena för **Inkludera tid**, **Inkludera utgifter**, **Inkludera material** och **Inkludera avgifter**.  Om du vill kontrollera vilka uppgifter som ingår väljer du fliken **Debiterbara uppgifter** på offertraden.

Beroende på associerade uppgifter och inkluderade transaktionsklasser importeras uppskattningar för kombinationerna av uppgifter och transaktionsklasser till offertraden.

När du importerar uppskattningar kommer systemet att använda prissättningen utifrån de projektprislistor som är kopplade till offerten och den faktureringstyp som angetts på den projektbaserade offertraden. Om en uppgift, roll eller kategori konfigureras på den projektbaserade offertraden som icke debiterbar, sätts den importerade uppskattningsraden som icke debiterbar och kommer inte att motsvara offertvärdet på offertraden.

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
|||10/1/2020 | 3.34 | 840 | 2800 |

När användaren väljer att sammanfatta efter transaktionsklass och kategori kommer följande information att importeras.

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| | Hotell | 10/1/2020 | 6 | 200 | 1200 |

När användaren väljer att sammanfatta efter Transaktionsklass, Kategori och Lövnodsuppgift kommer följande information att importeras. Observera att resultatet är samma som det som fanns i projektet.

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| Uppgift B | Hotell | 10/1/2020 | 4 | 200 | 800 |
| Uppgift C | Hotell | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
