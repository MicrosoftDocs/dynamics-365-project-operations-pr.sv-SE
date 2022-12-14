---
title: Ställ in valutakonvertering för att beräkna försäljningspriser utifrån kostnadstaxa
description: Den här artikeln innehåller information om hur du konfigurerar valutakonverteringsbeteendet som används i Microsoft Dynamics 365 Project Operations när försäljningstransaktioner skapas från kostnadstransaktioner.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816678"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Ställ in valutakonvertering för att beräkna försäljningspriser utifrån kostnadstaxa

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

I Microsoft Dynamics 365 Project Operations kan försäljningspriser för utgiftskategorier anges som numeriska värden, eller så kan de konfigureras så att de beräknas utifrån de kostnader som uppstått.

När de är konfigurerade att beräknas utifrån den kostnader som uppstått är följande alternativ tillgängliga:

- Vid kostnad
- Markera procentsats över kostnad

I scenarier där utgiftskostnaden uppstår i en valuta som skiljer sig från försäljningsvalutan för projektkontraktet, krävs valutakonvertering för att beräkna försäljningspriset utifrån kostnaden.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Valutakonverteringsbeteende som använder ursprungliga Dataverse växelkurser

Som standard används i Project Operations de växelkurser som är lagrade i tabellen Valuta i Dataverse. Följ stegen nedan om du vill konfigurera Project Operations så att ursprungliga växelkurser används för beräkning av försäljningspriser utifrån kostnad.

1. Gå till **Project Operations \> Inställningar \> Parametrar**.
1. Öppna informationssidan för **Projektparameter**.
1. Ange ett tomt värde i fältet **Valutakonverteringslogik**.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valutakonverteringsbeteende som använder växelkurser från appar för ekonomi och drift

De växelkurser i valutatabellen som är inbyggt i är inte Dataverse datumspecifika. Därför kanske de inte alltid skalas efter de krav du har för beräkning av försäljningspriser utifrån kostnadsnivåer.

Du kan använda växelkurser från ekonomi- och driftmiljön för att beräkna försäljningspriset i försäljningsvalutan utifrån en kostnadstaxa i kostnadsvalutan. Konfigurera valutakonverteringsbeteendet genom att följa stegen nedan.

1. På sidan **Projektparametrar**, lägg till fältet **Valutakonverteringslogik**. Spara och publicera sedan anpassningen.
1. Gå till **Project Operations \> Inställningar \> Parametrar**.
1. Öppna informationssidan för **Projektparameter**. 
1. Ange fältet **Valutakonverteringsbeteende** till **Utökat med reserv till standardvärde**.
1. Ge säkerhetsroll **Användare av appar för dubbelriktad skrivning** **Global läsbehörighet** till följande tabeller:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. I ekonomi- och driftmiljön kör du följande dubbla skrivmappningar med inledande synkronisering:

    - Valutakurstyp (msdyn\_exchangeratetypes)
    - Valutapar för valutakurs (msdyn\_currencyexchangeratepairs)
    - CDS valutakurser (msdyn\_currencyexchangerates)

När ändringarna är slutförda med dubbelskrivning blir växelkurserna från ekonomi- och operationsmiljön tillgängliga i Dataverse. I Project Operations används dessa växelkurser för att konvertera kostnadssatser till kontraktets försäljningsvaluta.

> [!NOTE]
> Valutakonverteringsbeteendet gäller endast beräkning av försäljningspriser från kostnadsnivåer. Den används inte för att beräkna basvalutavärden allmänt. I basvalutavärden används alltid ursprungliga Dataverse växelkurser oavsett om du slutför proceduren eller inte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
