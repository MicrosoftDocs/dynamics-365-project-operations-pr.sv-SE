---
title: Aktivera och revidera en projektoffert
description: Den här artikeln innehåller information om hur du aktiverar och reviderar offerter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410348"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktivera och revidera en projektoffert

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med hjälp av aktiverings- och revisionsfunktioner kan du hålla reda på versionshantering för projektbaserade offerter under faser av uppskattning och förhandling. När ett utkast till en offert aktiveras skrivskyddas det.

Med aktiverings- och revisionsfunktionerna kan du utföra följande åtgärder:

- Offerter kan endast vinnas eller förloras efter aktiveringen.
- Revidera en offert om du vill ändra den befintliga offerten eller skapa en ny version.

> [!NOTE]
> När funktionen för aktivering och revidering av offerter har aktiverats kan den inte inaktiveras.

Aktivera möjligheten att aktivera och revidera projektbaserade offerter genom att följa stegen nedan.

1. Gå till **Inställningar** \> **Parametrar**.
1. Öppna posten **Parametrar**.
1. I åtgärdsfönstret går du till fliken **Funktionskontroll** och väljer **Aktivera aktivering och revidering av offerter**.
1. Klicka på **OK** i bekräftelsedialogrutan.
1. Uppdatera webbläsaren efter en stund. Aktiverings- och revisionsfunktioner bör nu vara tillgängliga. Du vet att funktionerna har aktiverats om knappen **Aktivera aktivering och revidering av offerter** inte längre syns i åtgärdsfönstret.

## <a name="activating-a-quote"></a>Aktivera en offert

När funktionen för aktivering och revidering av offerter har aktiverats är knapparna **Stäng offert som vunnen** och **Stäng offert som förlorad** i åtgärdsfönstret inte tillgängliga för utkast av projektofferter. De är endast tillgängliga när en offert har aktiverats.

Aktivering är stadiet i offertprocessen när du vill förhindra fler ändringar i offerten. I det här stadiet skickas offerten för intern granskning eller till kunden.

Knapparna **Stäng offert som vunnen** och **Stäng offert som förlorad** i åtgärdsfönstret är tillgängliga för aktiverade offerter. Beroende på resultatet av den interna granskningen eller kundgranskningen kan du använda någon av dessa knappar för att stänga en aktiverad offert. Du kan göra förhandlingarna och ändringar på aktiverade offerter genom att välja **Revidera offert**.

## <a name="revising-a-quote"></a>Revidera en offert

Om du måste göra ändringar av en aktiverad offert väljer du **Revidera offert**. Offerten stängs och orsakskoden **reviderad** används. En ny offert skapas med samma ID och ett stegvist revisionsnummer. All information från den ursprungliga offerten kopieras till den nya offerten. Den nya offerten har utkaststatus och kan redigeras efter behov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
