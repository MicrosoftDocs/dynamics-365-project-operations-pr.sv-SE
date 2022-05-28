---
title: Importera en beräkning till en projektbaserad kontraktrad - lite
description: I det här ämnet finns information om hur du importerar ekonomiska uppskattningar från ett projekt till en kontraktrad.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 52abaa785b50b914e7813aaf4660504ee99129d6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582088"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importera en beräkning till en projektbaserad kontraktrad - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I Dynamics 365 Project Operations kan du importera beräkningar från ett projekt till en projektbaserad kontraktrad.

1. Kontrollera att fältet **Projekt** på den projektbaserade kontraktraden är ifyllt.
2. Under fliken **Kontraktradsinformation** i underrutnätet väljer du **Importera från projektuppskattning**. En dialogruta med sammanfattningsalternativ öppnas. De tillgängliga alternativen för sammanfattning är **Transaktionsklass**, **Kategori**, **Roll** och **Projektuppgift**.
3. Utifrån valet för sammanfattning kopieras uppskattningen från projektet för alla transaktionsklasser och uppgifter som ingår i kontraktraden. Om du vill kontrollera vilka transaktionsklasser som är inkluderade går du till fliken **Allmänt** på den projektbaserade kontraktraden och kontrollerar värdena i fälten **Inkludera tid**, **Inkludera utgifter** och **Inkludera avgifter**. 
4. Om du vill se vilka uppgifter som ingår väljer du fliken **Debiterbara uppgifter** på kontraktraden. Baserat på associerade uppgifter där fältet **Inkluderade transaktionsklasser** har angetts till **Ja**, importeras alla uppskattningar för de kombinationerna av uppgifter och transaktionsklasser till kontraktraden.

När du importerar uppskattningar kommer systemet att använda prissättningen utifrån de projektprislistor som är kopplade till kontraktet och den faktureringstyp som angetts på kontraktraden. Om en uppgift, roll eller kategori konfigureras på kontraktraden som icke debiterbar, sätts den importerade uppskattningsraden som icke debiterbar och kommer inte att motsvara kontraktvärdet på kontraktraden.

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
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

När användaren väljer att sammanfatta efter **Transaktionsklass** och **Kategori** kommer följande information att importeras:

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotell | 10/1/2020 | 6 | 200 | 1200 |

När användaren väljer att sammanfatta efter **Transaktionsklass**, **Kategori** och **Lövnodsuppgift** kommer följande att importeras. Observera att resultatet är samma som det som fanns i projektet:

| Aktivitet | Kategori | Datum | Antal | Enhetspris | Belopp |
| --- | --- | --- | --- | --- | --- |
| Uppgift A | Flyg | 10/1/2020 | 4 | 400 | 1600 |
| Uppgift B | Hotell | 10/1/2020 | 4 | 200 | 800 |
| Uppgift C | Hotell | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]