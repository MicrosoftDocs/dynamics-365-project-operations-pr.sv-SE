---
title: Kopiera projektbaserade offerter
description: I det här ämnet finns information om hur du kopierar projektbaserade offerter i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 247f9d33bc2e7b0bcbeae8114bb436ed237efce660d0840e58d536d2a290639e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992183"
---
# <a name="copy-project-based-quotes"></a>Kopiera projektbaserade offerter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan enkelt skapa en ny projektoffert genom att kopiera en befintlig. 

- Om du vill kopiera en projektoffert går du till listan **Projektofferter** eller sidan **Projektoffert**, väljer den projektoffert du vill kopiera och väljer sedan **Kopiera**.

Då öppnas en dialogsida där du kan ange parametrarna för kopian. Följande tabell visar de fält som ingår i dialogsidan. Beroende på vilka värden du väljer kan kopieringsprocessen ändras.

| **Fält** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- |
| Område | Ange relevant ämne, eller namn, för målofferten. När dialogrutan öppnas anges den i systemet som ämnet för källofferten med tillägget **-kopia**. | |
| Potentiell kund | Referens till kundens företag eller kontopost. När dialogen öppnas ställs den in för kontot i källofferten. | Det här fältet är den primära kunden i offerten. |
| Kontrakteringsenhet | Den organisationsenhet som är ansvarig för leveransen av projekten som är associerade med detta avtal.
När dialogen öppnas ställs den in för den avtalande enheten i källofferten. | Den avtalande enheten är den avdelning i företaget som ska utföra projekten efter det att affären har stängts. Varje avtalande enhet har en valuta. Valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under projektets genomförande. |
| Valuta | Det är valutan som avtalet genomförs i. När dialogen öppnas ställs den in för valutan i källofferten. Detta kan ändras och om det ändras ställs fältet **Kopiera prissättning** alltid in på **Nej**. Detta beror på att prislistorna för källofferten inte längre är relevanta. | Valutan används för att standardisera en prislista för att skapa en ekonomisk uppskattning av offerten och slutligen för att fakturera kunden när affären tas hem. |
| Begärt leveransdatum | Det här är det leveransdatum som kunden har begärt. | Detta används som slutdatum när faktureringsdatum skapas med utgångspunkt från en viss frekvens. |
| Kopiera prissättning | Värdet Ja/Nej anger om prissättningen i offerten ska kopieras från källofferten. | Om **Ja** har valts kopieras referenserna projektprislista och produktprislista från källofferten till målofferten. Om **Nej** har valts återställs prislistor utifrån de senaste prislistorna som konfigurerades för konto- eller projektparametrarna. |

När du väljer **OK** i dialogrutan skapas en kopia av projektofferten utifrån de parametrar som valts i dialogen. Den nya projektofferten öppnas. 

> [!NOTE]
> Följande information kopieras inte från käll- till målofferten:
>
> - Faktureringsscheman
> - Offert- och offertradskunder
> - Projektreferens för projektbaserade offertrader – kundens budgetinformation
>
>Eftersom informationen är mycket specifik för varje offert kopieras inte dessa fält och poster. Offertrader för projekt och produkter, uppskattningar av offertradsinformation och värden som inte ska överskridas på offertnivån kopieras. Pris- och kostnadstaxa varierar beroende på vilket alternativ för **kopiering av prissättning** som väljs i dialogrutan **Kopiera parametrar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]