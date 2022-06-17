---
title: Hantera flera kunder på projektbaserade kontraktrader - lite
description: Den här artikeln innehåller information om att hantera flera kunder på projektbaserade kontraktsrader.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922152"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Hantera flera kunder på projektbaserade kontraktrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Projektbaserade kontraktrader kan innehålla en lista med kunder som är ansvarig för betalning. Den här listan med kunder på den projektbaserade kontraktraden kan vara samma som listan med kunder i kontraktet, men det är inte obligatoriskt. När en projektoffert visas och ett projektkontrakt skapas, kopieras kundlistan på offertraden till motsvarande kontraktrad. Kunderna i offerten kopieras till kontraktet.

När projektkontraktet faktureras prioriteras kundlistan i projektbaserade kontrakt med prioritet över kundlistan i kontraktet. Kundlistan i projektkontraktet används endast som standard för nya kontraktrader.

Alla kontraktkunder på fliken **Kunder** av projektkontraktets standard som kontraktskunder på nya kontraktsrader som skapats för projektkontraktet. Alla befintliga kontraktrader kommer inte att ärva de nya kontraktkundposterna som skapats efter dem.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Skapa, uppdatera eller ta bort en kontraktrad kundpost

Du kan skapa, uppdatera eller ta bort en kontraktradkund på fliken Kontraktradens kund och sidan Projektbaserade kontraktrader. När en ny kund läggs till på den projektbaserade kontraktraden läggs de också till i det allmänna kontraktet som en kontraktkund med en standard delningsprocent på noll procent. Delningsprocenten för faktureringen i hela kontraktet kopieras till nya kontraktrader och projektkontraktet. När du fakturerar ett kontrakt är det emellertid faktureringsdelningsprocenten på den kontraktradnivå som används och inte för faktureringsdelningsprocenten procenten på den övergripande kontraktnivån.

Nedan visas fälten på kundposten för **kontrakt** raden för en projektbaserad kontraktrad som du bör tänka på när du arbetar med den:

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Konto** | Redigerbart rutnät på fliken **kontraktradkunder** och på **huvud**- och **snabbregistrering** sformulär för en kontraktradskund. | Alla aktiva konton. Det här fältet låses efter att posten skapas. Om du vill uppdatera fältet tar du bort posten och skapar en ny post. Om du har registrerat verkliga värden kan du inte ta bort posten. Men du kan ange en faktureringsdelningsprocenten som noll för det kontot. När posten har markerats som noll påverkas alla framtida och faktiska intäkter som hänförs till den här kunden. | När du plockar ett konto från huvudkontolistan för att lägga till och spara dem läggs kontraktradkunden också till som en kontraktkund. Kontraktradkunder används när fakturor skapas. |
| **Delningsprocent för fakturering** | Redigerbart rutnät på fliken **kontraktradkunder** och på **huvud**- och **snabbregistrering** sformulär för en kontraktradskund. | Detta fält motsvarar procentandelen av varje fakturerad försäljningstransaktion som tilldelats den här kontraktradkunden. | Kontraktradkunder och faktureringsdelningsprocent används när faktiska värden skapas efter godkännande och när fakturan har genererats. |
| **Undre gräns** | Redigerbart rutnät på fliken **kontraktradkunder** och på **huvud**- och **snabbregistrering** sformulär för en kontraktradskund. | Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för kontaktraden. | Undre gränsen för kontraktradkunden används när faktiska värden skapas och fakturorna skapas. |
| **Är Avrundning** | Redigerbart rutnät på fliken **kontraktkunder** och på **huvud**- och **snabbregistrerings** formulär för en kontraktradskund. | I det här fältet anges om kunden är en standardavrundning för kunden för den projektbaserade kontraktraden. | När du genererar ett faktiskt värde enligt faktureringsdelningsprocenten kan det finnas vissa avrundningsdifferenser. Den här kunden avräknar avrundningsdifferenserna i det här fallet. |

## <a name="edit-billing-split-percentages"></a>Redigera delningsprocent för fakturering

Faktureringsdelningsprocenten kan redigeras i rutnätet. När faktureringsdelningsprocenten inte är total till 100 procent får du ett felmeddelande. När du har redigerat faktureringsdelningsprocenten uppdaterar du sidan så att felmeddelandet stängs.

Du kan också välja **Fördela jämnt** i underrutnätet för kontraktsradkunden. Den här åtgärden tilldelar jämn faktureringsdelning till alla kontraktradkunder. Om det finns en avrundningsfaktor kommer den att läggas till i den avrundade kunden. En kontraktradkund märks alltid som den **avrundande** kunden med **avrundning** inställd på **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]