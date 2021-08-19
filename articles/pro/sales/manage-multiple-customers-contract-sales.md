---
title: Hantera flera kunder i projektkontrakt - lite
description: I det här ämnet finns information om hur du hanterar flera kunder i projektkontrakt.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b7010ef75cd71ecdf832abb889db4703baa18fce0adadf3893621c42002fcab9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001768"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Hantera flera kunder i projektkontrakt - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Projektkontrakt i Dynamics 365 Project Operations har stöd för scenariot där ett avtal om flera kunder ingår i ett avtal. På fliken **Sammanfattning** på sidan **Projektkontrakt** inkluderar fältet **Kund**. I det här fältet identifieras den primära kunden för affären. Andra kunder för affären kan ställas in på fliken **kunder** på sidan **projektkontrakt**.

Alla kontraktkunder som är förtecknade i projekkontrakt som standard som kontraktsrad kunder på alla nya projektbaserade kontraktrader som skapas för projektkontraktet. Befintliga projektbaserade kontraktrader ärver inte nya kontraktkunder som nya poster.

Produktbaserade kontraktrader kopplas automatiskt till den primära kunden.

Kontraktskunder och kontraktradkunder kan läggas till, uppdateras eller tas bort när som helst innan kontraktet vanns.

## <a name="primary-customer"></a>Primär kund

Kunden som listas på fliken **Sammanfattning** i projektavtalet eftersom den potentiella kunden är den primära kunden för kontraktet. När du försöker ta bort den primära kunden från kundlistan i kontraktet visas ett felmeddelande om att det inte går att ta bort en primär kundpost i ett kontrakt.

Den primära kunden kan inte uppdateras från listan kontraktkunder. Ändra i stället den potentiella kunden på fliken **Sammanfattning** i kontraktet. När det här fältet uppdateras på sidan **kontraktsammanfattning** läggs den till som en ny kontraktkund med den **primära** flagguppsättningen. Den föregående primära kunden blir fortfarande kund i kontraktet.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Skapa, uppdatera eller ta bort en kontrakt kundpost

En kontraktkund kan skapas, uppdateras eller tas bort från fliken **kunder** på sidan **projektkontrakt**. Fälten i följande tabell visas i kontraktkundposten för ett projektkontrakt och du bör tänka på när du arbetar med kontraktet.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Konto** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund. | Lista alla aktiva konton. Det här fältet låses efter att posten skapas. Om du vill uppdatera kontot tar du bort posten och skapar den på nytt. Om du har registrerat verkliga värden, eller om kontraktets kundpost är en primär kund, kan du inte ta bort posten. | Kontraktskunder kopieras över som kontraktradkunder när en kontraktrad skapas. |
| **Delningsprocent för fakturering** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund. | Motsvarar procentandelen av varje fakturerad försäljningstransaktion som tilldelats den här kontraktkunden. | Kopieras till nya kontraktrader och till projektets kontraktsradkunder på nya projekt kontraktrader. |
| **Namn på kontakten som ska faktureras** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund. | Det här textfältet ska användas för att identifiera kundens kontaktperson för fakturering. Det här fältet används som standard från den relaterade kontoposten. | Kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden. |
| **Fakturera till namn** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund | Det här textfältet ska användas för att identifiera kundens kontaktperson för fakturering. Det här fältet används som standard från den relaterade kontoposten. | Kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden. |
| **Betalningsvillkor** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund. | Standardvärdet från den relaterade kontoposten. | Kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden. |
| **Är Avrundning** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund. | Anger om kunden är en avrundningskund för den här affären. Det kan bara finnas en avrundning av kunden i ett projektkontrakt. | När kostnads- och ofakturerade försäljningsdelningar i kvantitet leder till en avrundningsskillnad används den differensen på den faktiska som har mappats till kunden. |
| **Undre gräns** | Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund | Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för det här åtagandet. | Gränsen **Undre gräns** upprättas på kontraktsnivå kommer att utvärderas den **Faktiska värden för ofakturerad försäljning** som refererar till den här kontraktkunden. |

## <a name="edit-billing-split-percentages"></a>Redigera delningsprocent för fakturering

Du kan redigera delningsprocent satser med hjälp av redigeringsfunktionen i rutnätet. När faktureringsdelningsprocenten inte är total till 100 procent får du ett felmeddelande. När du har redigerat faktureringsdelningsprocenten uppdaterar du sidan så att felmeddelandet stängs.

Du kan också välja **jämnt fördelat** i underrutnätet **kontraktkund** för att fördela faktureringsdelning jämnt för alla kontraktskunder. Om det finns en avrundningsfaktor kommer den att läggas till i den avrundade kunden. En av kontraktskunderna är alltid märkt som **avrundning**, vilket innebär att kontraktets kundpost har avrundningsflaggan satt till **Ja**. Detta är vanligtvis den primära kunden för kontraktet, men det kan också ändras.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]