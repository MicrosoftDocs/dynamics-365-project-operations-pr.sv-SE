---
title: Konfigurera ett kvarhållarschema
description: I det här ämnet finns information om hur du skapar ett kvarhållarschema i Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1c48f04aa47d50c9f3ab46031ef0d6cd68619d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574774"
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