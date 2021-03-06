---
title: Hantera flera kunder på projektbaserade offertrader
description: I det här ämnet beskrivs hur du hanterar flera kunder på projektbaserade offertrader.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6a509fcf8d1fa11b4ce1ba1493d9c3cc64b4f22f
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965904"
---
# <a name="managing-multiple-customers-on-project-based-quote-lines"></a>Hantera flera kunder på projektbaserade offertrader

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Projektbaserade offertrader har stöd för scenarier där varje offertrad har en lista över kunder som betalar för den. Den här listan över kunder på den projektbaserade offertraden kan vara samma som kundlistan i offerten. Du kan också ändra listan med kunder så att den blir annorlunda. När en projektoffert har vunnits kopieras kundlistan på den projektbaserade offertraden till motsvarande projektbaserade kontraktrad för att skapa projektkontraktet. Kunder i den projektbaserade offerten kopieras till projektkontraktet.

När du fakturerar projektkontraktet prioriteras kundlistan för den projektbaserade kontraktraden över projektkontraktets lista. Kundlistan i projektkontraktet används endast för standardvärden för nya projektkontraktrader.

Alla offertkunder under fliken **kunder** i projektofferten anges som offertradskunder på alla nya projektbaserade offertrader som skapas för projektofferten. Eventuella befintliga projektbaserade offertrader ärver inte nya offertkundposter som skapats efter dem.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Skapa, uppdatera eller ta bort en kundpost i en offertrad

Du kan skapa, uppdatera eller ta bort en offertradskund under fliken **Offertradskunder** på sidan **Projektbaserad offertrad**. När du lägger till en ny kund på den projektbaserade offertraden läggs kunden också till i den övergripande offerten som en offertkund, med en standardprocent för delning av fakturering i den övergripande offerten på 0 %. Procentsatsen för delning av faktureringen i den övergripande offerten kopieras till nya offertrader och till projektkontraktet. När du fakturerar från kontraktet används emellertid procentsatsen för faktureringsdelningen på offertradsnivån, inte procentsatsen för faktureringsdelningen på den övergripande kontraktnivån. 

I följande tabell visas fälten på kundposten för offertraden i en projektrelaterad offertrad.

| Fält | Plats | Beskrivning och vägledning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Konto** | Ett redigerbart rutnät under fliken **Offertradskunder**, huvudformuläret och formulären för snabbskapande för en offertradskund. | Lista alla aktiva konton. Det här fältet låses efter att posten skapas. Om du behöver uppdatera fältet tar du bort och återskapar posten. Om du har registrerat verkliga värden kan du inte ta bort posten. | När du plockar ett konto från huvudkontolistan med konton som ska läggas till läggs även offertradskunder till som en offertkund när du sparar den. När en offert har vunnits kopieras offertradskunder till projektets kontraktradkunder. |
| **Delningsprocent för fakturering** | Ett redigerbart rutnät under fliken **Offertradskunder**, huvudformuläret och formulären för snabbskapande för en offertradskund. | Motsvarar procentandelen av varje fakturerad försäljningstransaktion som kommer att tillskrivas kunden i den här offertraden. | Kopierad till projektets kontraktradkunder. |
| **Undre gräns** | Ett redigerbart rutnät under fliken **Offertradskunder**, huvudformuläret och formulären för snabbskapande för en offertradskund. | Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för den här offertraden. | Kopieras till projektets kontraktsradkunder när en offert har vunnits. |
| **Avrundas** | Ett redigerbart rutnät under fliken **Offertradskunder**, huvudformuläret och formulären för snabbskapande för en offertradskund. | Anger om kunden är en kund med standardavrundning för denna projektbaserade offertrad. | Kopieras till projektets kontraktkunder när en offert har vunnits. |

## <a name="edit-billing-split-percentages"></a>Redigera delningsprocent för fakturering

Du kan redigera delningsprocentför fakturering på raden. När delningsprocenten för fakturering inte är 100 % uppstår ett fel. När du har redigerat delningsprocenten för fakturering uppdaterar du offertradssidan för att ta bort felet.

Använd åtgärden jämn distribution på offertradskunders underrutnät för att fördela faktureringsdelningar till alla offertradskunder. Om det finns en avrundningsfaktor kommer den att läggas till i den avrundande kunden. En av offertradskundernas märks alltid som den avrundande kunden, vilket innebär att avrundningsflaggan har värdet **Ja** i posten för offertradskunden. 
