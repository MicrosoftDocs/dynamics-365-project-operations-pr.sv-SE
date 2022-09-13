---
title: Kopiera projektbaserade kontrakt
description: Den här artikeln innehåller information om hur du kopierar projektkontrakt i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410341"
---
# <a name="copy-project-based-contracts"></a>Kopiera projektbaserade kontrakt

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Du kan enkelt skapa nya projektkontrakt genom att kopiera befintliga kontrakt på ett av två sätt:

- På listsidan **Projektkontrakt** väljer du ett projektkontrakt och sedan **Kopiera**.
- På informationssidan **Projektkontrakt** väljer du **Kopiera**.

I båda fallen visas en dialogruta, där du kan ange parametrarna för det kopierade kontraktet. Dialogrutan innehåller följande fält. Beroende på vilka värden du väljer kan kopieringsprocessen ändras.

| Fält | Description | Inverkan nedströms |
| --- | --- | --- |
| Ämnesnamn | Ange ämnet för målkontraktet. När dialogrutan öppnas ställer systemet in fältet på namnet för källkontraktet, men ordet "kopia" läggs till på slutet. | Det här fältet har ingen inverkan nedströms. |
| Kunder | En referens till kundens företag eller kontopost. När dialogrutan öppnas ställer systemet in detta fält på kontot i källkontraktet. | Det här fältet är den primära kunden i kontraktet. |
| Ägande företag | Det företag som är ansvarigt för leveransen av de projekt som är associerade med detta avtal. När dialogrutan öppnas ställer systemet in detta fält på det företag som äger källkontraktet. | Det ägande företaget är den juridiska entitet som ska genomföra projektet efter att affären har stängts. Det ägande företagets valuta måste stämma överens med den kontrakterande enhetens valuta. |
| Kontrakteringsenhet | Den organisationsenhet som är ansvarig för leveransen av projekten som är associerade med detta avtal. När dialogrutan öppnas ställer systemet in detta fält på den kontrakterande enheten till källkontraktet. | Den avtalande enheten är den avdelning i företaget som ska utföra projekten efter det att affären har stängts. Varje avtalande enhet har en valuta. Valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under projektet. |
| Valuta | Det är valutan som avtalet genomförs i. När dialogrutan öppnas ställer systemet in fältet till valutan som används i källkontraktet. Valutan kan ändras. Om så är fallet är fältet **Kopiera prissättning** alltid inställt på **Nej** eftersom prislistorna i källkontraktet inte längre är relevanta. | Den här valutan används för standardprislistor för att generera ekonomisk uppskattningar i kontraktet och för att fakturera kunden när affären tas hem. |
| Begärt leveransdatum | Leveransdatumet som begärts av kunden. | Detta datum används som slutdatum när faktureringsdatum skapas med utgångspunkt från en viss frekvens. |
| Kopiera prissättning | Ett värde som indikerar om prissättningen i kontraktet ska kopieras från källkontraktet. | Om fältet är inställt på **Ja** kopieras referenserna projektprislista och produktprislista från källkontraktet till målkontraktet. Om det är inställt på **Nej** används standardprislistor utifrån de senaste prislistorna för konto- eller projektparametrarna. |

När du väljer **OK** i dialogrutan skapar systemet en kopia av kontraktet utifrån de parametervärden du anger. Det nya kontraktet öppnas.

Följande information kopieras **inte** från källkontraktet till målkontraktet eftersom den är specifik för varje kontrakt:

- Faktureringsscheman
- Kontrakt och kontraktradkunder
- Projektreferens på projektbaserade kontraktrader
- Information om kundbudget

Kontraktrader för projekt och produkter, uppskattningar av kontraktradsinformation och värden som inte ska överskridas på kontraktnivån kopieras. Inledande standardpriser och kostnadstaxa beror på valet i fältet **Kopiering av prissättning** i dialogrutan **Kopiera parametrar**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
