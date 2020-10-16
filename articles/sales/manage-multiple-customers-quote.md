---
title: Hantera flera kunder i projektofferter
description: I det här ämnet finns information om hur du arbetar med offerter som omfattar flera kunder som ska finansiera projektet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908654"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Hantera flera kunder i projektofferter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektofferter har stöd för scenariot där ett förslag omfattar flera kunder som ska finansiera affären. Under fliken **Sammanfattning** i offerten finns fältet **Potentiell kund**, som identifierar affärens primära kund. Andra kunder för affären kan konfigureras under fliken **Kunder** i projektofferten.

Alla offertkunder under fliken **Kunder** i projektofferten anges som offertradskunder på alla **nya** projektbaserade offertrader som skapas för offerten. Eventuella befintliga projektbaserade offertrader ärver inte nya offertkundposter som skapats efter dem.

Du kan när som helst lägga till, uppdatera eller ta bort offertkunder och offertradskunder innan offerten har vunnits. En giltig kund i offerten måste vara inställd som en kund i det ägande företaget eller den juridiska entiteten på sidan **Kunder**. Juridiska entiteter konfigureras i modulen **Projektledning och redovisning** i Dynamics 365 Project Operations och görs tillgängliga som företag i modulen **Projektförsäljning och leverans** i Project Operations.

## <a name="concept-of-a-primary-customer"></a>Koncept för en primär kund

Kunden som visas under fliken **Sammanfattning** i projektofferten som den potentiella kunden är den primära kunden i offerten. Om du försöker ta bort den primära kunden från listan över kunder i offerten visas ett felmeddelande om att det inte går att ta bort en post för en primär kund i en offert.

Den primära kunden får inte uppdateras från kundlistan i offerten. Du kan emellertid påverka den primära kunden genom att ändra den potentiella kunden under fliken **Sammanfattning** i offerten. När fältet uppdateras i **Offertsammanfattning** läggs den nya potentiella kunden till som en ny offertkund med flaggan **Primär**. Den gamla potentiella kunden är fortfarande en kund i offerten.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Skapa, uppdatera eller ta bort en kundpost i en offert

Du kan skapa, uppdatera eller ta bort en offertkund från fliken **Offertkunder** på sidan **Offert**. Fälten som visas i följande tabell är på offertkundposten i en projektoffert.

| **Fält** | **Plats** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Konto | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Lista alla aktiva konton. Det här fältet låses efter att posten skapas. Om du vill uppdatera tar du bort posten och skapar den på nytt. Om du har registrerat verkliga värden, eller om offertkundposten är en primär kund, får du ta bort posten. | Offertkunder kopieras som offertradskunder när en offertrad skapas. Offertkunder kopieras också till projektkontraktkunder när en offert har vunnits. |
| Delningsprocent för fakturering | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Motsvarar procentandelen av varje fakturerad försäljningstransaktion som kommer att tillskrivas denna offertkund. | Kopierat till nya offertrader som skapats och till kunder av projektkontraktet. |
| Namn på kontakten som ska faktureras | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Det här är ett textfält som ska användas för att identifiera kundens kontaktperson för fakturering. Dessa hämtas från den relaterade kontoposten | Kopieras till kunder av projektkontraktet när en offert har vunnits och till fältet Namn på kontakten som ska faktureras på fakturan som genereras för kunden. |
| Fakturera till namn | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Det här textfältet ska användas för att identifiera kundens kontaktperson för fakturering. | Kopieras till kunder av projektkontraktet när en offert har vunnits och till fältet **Namn på kontakten som ska faktureras** på fakturan som genereras för kunden. |
| Betalningsvillkor | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Det här är en alternativuppsättning med värden som hämtas från den relaterade kontoposten. | Kopieras till kunder av projektkontraktet när en offert har vunnits och till fältet **Namn på kontakten som ska faktureras** på fakturan som genereras för kunden. |
| Är Avrundning | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Anger om kunden är en avrundningskund för den här affären. | Kopieras till projektets kontraktkunder när en offert har vunnits. |
| Ägande företag | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Den juridiska person som den här kunden har konfigurerats med i modulen **Projekthantering och redovisning**. Fältet är skrivskyddat och är inställt på det ägande företaget i själva offerten. Listan över kunder som ska läggas till i fältet **Konto** är redan filtrerad mot listan från det ägande företaget i modulen **Projektledning och redovisning** i Project Operations. | Det ägande företaget är lika med begreppet juridisk person i modulen **Projektlednings och redovisning** i Project Operations. Alla kostnader och intäkter som härrör från detta projekt redovisas i det ägande företagets huvudbok. |
| Undre gräns | Redigerbart rutnät under fliken **Offertkunder** och formulären **Huvudsakligt** och **Snabbskapa** för en offertkund. | Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för det här åtagandet. | Kopieras till projektets kontraktkunder när en offert har vunnits. |

## <a name="editing-billing-split-percentages"></a>Redigera delningsprocent för fakturering

Du kan redigera procentandelarna för faktureringsdelning med hjälp av redigeringsfunktionen i rutnätet. När delningsprocenten för fakturering inte är 100 % uppstår ett fel. När du har uppdaterat delningsprocenten för fakturering uppdaterar du sidan för att ta bort felet.

Du kan också prova att välja **Jämnt fördelat** på offertkundens underrutnät. Med den här åtgärden tilldelas faktureringsdelningar till alla offertkunder. Om det finns en avrundningsfaktor kommer den att läggas till i den avrundande kunden. En av offertkunderna är alltid märkt som den avrundande kunden. detta innebär att offertkundposten har flaggan **Avrundning** inställd på **Ja**. Det är vanligtvis den primära kunden i offerten, men det kan ändras.