---
title: Konfigurera en tidsplan för arvoden – Lite
description: I det här ämnet finns information om hur du skapar ett kvarhållarschema i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181294"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Konfigurera en tidsplan för arvoden – Lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Kvarhållarscheman ställs in på sidan **projektkontrakt** i Dynamics 365 Project Operations.

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
