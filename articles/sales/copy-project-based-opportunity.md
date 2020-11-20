---
title: Kopiera projektbaserade affärsmöjligheter
description: I det här ämnet finns information om hur du kopierar projektbaserade affärsmöjligheter i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085479"
---
# <a name="copy-project-based-opportunities"></a>Kopiera projektbaserade affärsmöjligheter

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


Det går enkelt att kopiera projektmöjligheter för att skapa nya projektmöjligheter. 

1. Gå till sidan **Projektmöjligheter** och välj en affärsmöjlighet i listan. Du kan också öppna en informationssida för en specifik affärsmöjlighet. 
2. Från någon av sidorna väljer du **Kopiera**. En dialogruta öppnas som innehåller följande fältinformation. Beroende på vilka värden du väljer i dialogrutan kan kopieringsprocessen ändras.

    | **Fält** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
    | --- | --- | --- |
    | Område | Ange relevant ämne för målmöjligheten. När dialogrutan öppnas anges den i systemet som ämnet för källmöjligheten med tillägget **-kopia**. | Det här fältet har ingen inverkan nedströms. |
    | Konto | Referens till kundens företag eller kontopost. När dialogen öppnas ställs den in för kontot i källmöjligheten. | Det här fältet är den primära kunden i affärsmöjligheten. |
    | Kontrakteringsenhet | Den organisationsenhet som är ansvarig för leveransen av projekten som är associerade med detta avtal. När dialogen öppnas ställs den in för kontrakteringsenheten i källmöjligheten. | Kontrakteringsenheten är den avdelning i företaget som utför projekten efter det att affären har stängts. Varje avtalande enhet har en valuta och valutan används för att rapportera uppskattade och faktiska kostnader som uppstår under projektet. |
    | Valuta | Det är valutan som avtalet genomförs i. När dialogrutan öppnas ställs den in på den valuta som används i källmöjligheten. | Valutan används för att standardisera en prislista och bygga ekonomiska uppskattningar för offerten. Slutligen används valutan för att fakturera kunden när affären vinns. |
    | Kopiera prissättning | Ett ja/nej-värde som anger om prissättningen i affärsmöjligheten ska kopieras från källmöjligheten. | Om **Ja** har valts kopieras prislistor från käll- till målmöjligheten. Om **Nej** har valts återställs prislistor utifrån de senaste prislistorna som konfigurerades. |

3. Välj **OK**. Systemet skapar en kopia av projektmöjligheten utifrån valda parametrar och den nya projektmöjligheten öppnas.