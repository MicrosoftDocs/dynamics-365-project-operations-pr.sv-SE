---
title: Konfigurera utgiftskategorier
description: I det här ämnet finns information om hur du konfigurerar utgiftskategorier och delade kategorier för utgiftsrapporter.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896708"
---
# <a name="set-up-expense-categories"></a>Konfigurera utgiftskategorier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

När medarbetarna skapar utgiftsrapporter måste varje utgiftspost vara associerad med en utgiftskategori. Utgiftskategorier härleds från delade kategorier som kan delas av alla juridiska entiteter i organisationen. Beroende på hur organisationen har definierats kan de här utgiftskategorierna även delas i andra områden. Baserat på definitionen av din organisation och vägledning från implementeringsteamet måste du avgöra om kategorierna som används i utgiftshantering endast ska användas i utgifts hantering eller delas i andra områden.

> [!NOTE]
> Dessa kategorier kan delas mellan projekthantering och redovisnings- och utgiftshantering, eller mellan projekthantering och redovisning och produktion. De kan emellertid inte delas mellan utgiftshantering och produktion.

Innan du kan börja konfigurationsprocessen måste följande beslut göras för varje utgiftskategori:

- Vilken är utgiftskategorin? Exempel är kategorier för flygningar, hotell och sträcka.
- Kan utgiftskategorin också användas i projekthantering och redovisning? Om den kan det måste du också fatta följande beslut:

    - Vilka kostnadskonton ska användas för följande utgifter?

        - Kostnad
        - Löneallokering
        - PIA-kostnadsvärde
        - Kostnadsartikel
        - PIA-kostnad värdeartikel
        - Upplupen förlust
        - PIA, upplupen förlust

    - Vilka intäktskonton ska användas för följande intäktskällor?

        - Fakturerad intäkt
        - Upplupna intäkter – försäljningsvärde
        - Pia – försäljningsvärde
        - Upplupna intäkter – produktion
        - PIA – Produktion
        - Upplupna intäkter – vinst
        - PIA – vinst
        - Upplupna intäkter – prenumeration
        - PIA-prenumeration

- Vilken är utgiftstypen?
- Vilken är standardbetalningsmetoden för utgiftskategorin?
- Måste utgifter i utgiftskategorin specificeras?
- Vilken är det huvudsakliga standardkontot utgiftskategorin?
- Vad är standardmomsgruppen för utgiftskategorin?
- Är fler betalningsmetoder tillåtna i utgiftskategorin? Vilka är dessa i så fall?
- Finns det några underkategorier i den här utgiftskategorin? Om det finns underkategorier måste du också fatta följande beslut:

    - Har någon av underkategorierna exkluderats från momsåterbetalning?
    - Vad är momsgruppen för underkategorierna?
