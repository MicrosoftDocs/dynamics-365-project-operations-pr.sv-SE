---
title: Kopiera projektkontrakt - lite
description: Den här artikeln innehåller information om att kopiera projektkontrakt i Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a1846af677f7cea3ec22fdba4408f2bbd7db8a3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932640"
---
# <a name="copy-project-contracts---lite"></a>Kopiera projektkontrakt - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Du kan enkelt skapa nya projektkontrakt genom att skapa kopior av befintliga kontrakt på ett av två sätt: 

  - På listsidan **Projektkontrakt**, välj ett projektkontrakt och välj sedan **Kopiera**.
  - På informationssidan **Projektkontrakt** väljer du **Kopiera**.

En dialogsida öppnas där du kan välja parametrarna för det kopierade kontraktet. Följande fält finns i dialogrutan. Beroende på vilka värden du väljer i dialogrutan kan kopieringsprocessen ändras.

| **Fält** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- |
| Område | Ange ämnet för målkontraktet. När dialogrutan öppnas ställer systemet in fältet på namnet för källkontraktet med tillägget **-kopia**. | Det här fältet har ingen inverkan nedströms. |
| Kund | Referens till kundens företag eller kontopost. När dialogen öppnas ställer systemet in detta fält på kontot i källkontraktet. | Det här fältet är den primära kunden i kontraktet. |
| Kontrakteringsenhet | Den organisationsenhet som är ansvarig för leveransen av projekten som är associerade med detta avtal. När dialogrutan öppnas ställs den in för kontrakteringsenheten i källkontraktet. | Den avtalande enheten är den avdelning i företaget som ska utföra projekten efter det att affären har stängts. Varje avtalande enhet har en valuta. Valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under projektet. |
| Valuta | Det är valutan som avtalet genomförs i. När dialogrutan öppnas ställer systemet in fältet till valutan som används i källkontraktet. Valutan kan ändras. Om så är fallet är fältet **Kopiera prissättning** alltid inställt på **Nej** eftersom prislistorna i källkontraktet inte längre är relevanta. | Valutan används för att standardisera prislistor för att skapa ekonomisk uppskattningar i kontraktet och för att fakturera kunden när affären tas hem. |
| Begärt leveransdatum | Leveransdatumet som begärts av kunden. | Detta datum används som slutdatum när faktureringsdatum skapas med utgångspunkt från en viss frekvens. |
| Kopiera prissättning | Anger om prissättningen i kontraktet ska kopieras från källkontraktet. | Om fältet är inställt på **Ja** kopieras referenserna projektprislista och produktprislista från källkontraktet till målkontraktet. Om **Nej** har valts återställs prislistor utifrån de senaste prislistorna för konto- eller projektparametrarna. |

När du väljer **OK** i dialogrutan skapas en kopia av kontraktet utifrån de parametrar som valts. Det nya kontraktet öppnas.

Följande information kopieras inte från **Källkontrakt** till **Målkontrakt**:

  - Faktureringsscheman
  - Kontrakt och kontraktradkunder
  - Projektreferens på projektbaserade kontraktrader
  - Information om kundbudget

Eftersom informationen är specifik för varje kontrakt kopieras inte dessa fält och poster. Kontraktrader för projekt och produkter, uppskattningar av kontraktradsinformation och värden som inte ska överskridas på kontraktnivån kopieras. Pris- och kostnadstaxa varierar beroende på valet i fältet **Kopiering av prissättning** i dialogrutan **Kopiera parametrar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]