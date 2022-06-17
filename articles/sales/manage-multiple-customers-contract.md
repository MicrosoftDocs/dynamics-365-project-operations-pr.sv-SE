---
title: Hantera flera kunder i projektkontrakt
description: Den här artikeln ger information om hur du hanterar flera kunder på ett projektkontrakt.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928362"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Hantera flera kunder i projektkontrakt

Den här artikeln ger information om hur du hanterar flera kunder på ett projektkontrakt. Du kan använda ett projektkontrakt när ett avtal för flera kunder behövs för finansiering av en affär. På sidan **Projektkontrakt** innehåller fliken **Sammanfattning** information om den primära kunden för en affär. Andra kunder som deltar i affären kan läggas till på fliken **Kunder**.

Alla kontraktskunder på fliken **Kunder** i projektkontraktet blir som standard kontraktskunder på nya, projektbaserade kontraktrader som skapats för projektkontraktet. Alla befintliga, projektbaserade kontraktrader ärver inte nya kontraktskundposter som skapas vid ett senare tillfälle.

Du kan lägga till, uppdatera samt ta bort kontrakt och kontraktradskunder när som helst innan kontraktet vunnits. En kund på projektkontraktet måste ställas in som en kund i det ägande företaget eller juridisk person på sidan **Kunder**. Juridiska personer ställs in i modulen **Projektledning och redovisning** i Dynamics 365 Project Operations och finns att tillgå som företag i modulerna **Projektförsäljning** och **Leverans** i Project Operations.

## <a name="primary-customers"></a>Primära kunder

Den potentiella kunden som listas på fliken **Sammanfattning** i projektkontraktet är kontraktets primära kund. Du kan inte uppdatera den primära kunden från listan över kontraktskunder. Om du försöker ta bort den primära kunden från en kundlista i kontraktet visas ett felmeddelande som anger att det inte går att ta bort en primär kundpost i ett kontrakt. Ändra istället kunden i fältet **Potentiell kund** på fliken **Sammanfattning** i projektkontraktet. När du uppdaterar detta fält läggs den nyvalda kunden till som en ny kontraktkund, med flaggan **Primär** inställd på **Ja**. Den tidigare primära kunden är fortfarande en kund på kontraktet men är inte längre den primära kunden.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Skapa, uppdatera eller ta bort en kontrakt kundpost

Du kan skapa, uppdatera eller radera en kontraktskund från fliken **Kontraktskund** på sidan **Kontrakt**. Följande fält inkluderas i kundkontraktsposten för ett projektkontrakt.

| **Fält** | **Plats** | **Beskrivning** | 
| --- | --- | --- | 
| Konto | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Lista alla aktiva konton. Det här fältet låses efter att posten skapas. Om du vill uppdatera posten måste du ta bort den och sedan skapa den på nytt. Om du har registrerat verkliga värden, eller om kontraktets kundpost är en primär kund, kan du inte ta bort posten. När en kontraktad skapas kopieras kontraktkund som kontraktradskunder. |
| Delningsprocent för fakturering | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Motsvarar procentandelen av varje icke-fakturerad försäljningstransaktion som tilldelats den här kontraktkunden. När nya projektkontraktrader skapas kopieras uppdelningsprocenten för fakturering till nya kontraktrader som skapats, samt till projektkontraktradskunder. |
| Namn på kontakten som ska faktureras | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Detta textfält ska användas för att identifiera fakturans kontaktperson för kunden. Standardvärdet kommer från den relaterade kontoposten. Kontaktnamnet kopieras till fältet **Fakturera till kontraktnamn** på den faktura som genereras för kunden. |
| Fakturera till namn | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Använd detta fält för att identifiera fakturans kontaktperson för kunden. Standardvärdet kommer från den relaterade kontoposten. Namnet kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden. |
| Betalningsvillkor | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Standardvärdet kommer från den relaterade kontoposten. Villkoren kopieras till fältet **Fakturera till kontraktnamn** på den faktura som genereras för kunden. |
| Ägande företag | Redigerbart rutnät i fliken **Projektkontraktskunder** samt på huvud- och snabbregistreringssidorna för en projektkontraktskund. | Den juridiska person där kunden ställs in i modulen **Projekthantering och redovisning**. Fältet är skrivskyddat och inställt på det företag som äger projektkontraktet.</br>Listan över kunder som ska läggas till i fältet **Konto** är redan filtrerad mot listan från det ägande företaget i modulen **Projektledning och redovisning** i Project Operations. Det ägande företaget är lika med den juridiska personen i modulen **Projektledning och redovisning** i Project Operations. Alla kostnader och intäkter från det här projektet redovisas i det ägande företagets huvudbok. |
| Är Avrundning | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Anger om kunden är en standardavrundande kund för affären. Det kan bara finnas en avrundning av kunden i ett projektkontrakt. När kostnad och icke-fakturerad försäljnings delas i kvantitet och leder till en avrundningsskillnad, används den differensen på den faktiska som har mappats till kunden. |
| Undre gräns | Redigerbart rutnät i fliken **Kontraktskunder** samt på huvud- och snabbregistreringssidorna för en kontraktskund. | Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för åtagandet. Den gräns som upprättas på kontraktskundnivå och som inte får överskridas kommer att utvärderas baserat på icke-fakturerade, faktiska försäljningsvärden som refererar till kontraktkunden. |

## <a name="edit-billing-split-percentages"></a>Redigera delningsprocent för fakturering

Du kan redigera faktureringsdelningsprocenten i rutnätet. När den totala faktureringsdelningsprocenten inte uppgår till 100 procent genereras ett felmeddelande. När du har redigerat faktureringsdelningsprocenten uppdaterar du sidan **Projektkontrakt** för att avlägsna felet.

Du kan också välja **Fördela jämnt** i underrutnätet för projektkontraktskunder. Faktureringsdelningar allokeras till samtliga kunder i projektkontraktet. Om det finns någon avrundningsfaktor kommer denna att läggas till i den avrundade kunden. En av kontraktskunderna har alltid flaggan **Avrundning** inställd på **Ja**. Den kunden är avrundningskunden. Vanligtvis är avrundningskunden också den primära kunden i kontraktet, men detta krävs inte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]