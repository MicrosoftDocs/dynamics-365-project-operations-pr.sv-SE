---
title: Konfigurera ett kvarhållarschema
description: Den här artikeln innehåller information om hur du upprättar kvarhållarschema i Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 077961d2f649754149315438252970609c246555
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927764"
---
# <a name="set-up-a-retainer-schedule"></a>Konfigurera ett kvarhållarschema

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Kvarhållarscheman konfigureras på sidan **Projektkontrakt** i Dynamics 365 Project Operations.

1. På sidan **Projektkontrakt** på fliken **Förskott och kvarhållare**, välj **Ställ in kvarhållarschema**.
2. På dialogsidan som öppnas visas fälten som visas i följande tabell. I tabellen kan du få en uppfattning om hur de angivna värdena påverkar eller påverkar det kvarhållarschema som kommer att skapas.

| Fält | Beskrivning | Inverkan nedströms |
| --- | --- | --- |
| Projektkontraktskund | Kunden på kontraktet som faktureras för denna kvarhållare eller förskott. | Om du har flera kunder i kontraktet och kontrakt och om du behöver fakturera var och dem för en viss kvarhållande eller förskott skapar du manuellt en faktura för varje kund. |
| Start för kvarhållarschema | Ange startdatum för kvarhållarschema. | Datumet får inte vara det datum då den första kvarstår eller förskott skapas. Datumet då den första beställdes eller förskott skapas påverkas även av fakturafrekvensen. |
| Slut för kvarhållarschema | Ange slutdatum för kvarhållarschema. | Datumet får inte vara det datum då den sista kvarstår eller förskott skapas. Datumet då den sista beställdes eller förskott skapas påverkas även av fakturafrekvensen. |
| Antal kvarhållare att skapa | När du anger antalet kvarhållare som ska skapas använder systemet startdatum och frekvens för att skapa numret i det här fältet. | När fältet uppdateras manuellt ignoreras värdet i fältet **Slut för kvarhållarschema** och i stället skapas det specifika antalet kvarhållna eller förskott. |
| Fakturafrekvens | Hur ofta programmet ska skapa balanserade och förskott. | Värdet påverkar direkt antalet kvarhållare och förskott samt de datum som skapats. |
| Totalbelopp | Total beloppet är det belopp som är uppdelat i den individuella beställnings- eller förskottsbetalningen som ska skapas. | Det här fältet har ingen inverkan nedströms. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]