---
title: Underavtalsrader för utgiftskategorier
description: I detta ämne finns information om hur du registrerar underavtalsrader för utgifter och använder fälten för att registrera tidsinköp från leverantörer.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323843"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Underavtalsrader för utgiftskategorier

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Ett underavtal i Dynamics 365 Project Operations kan ha en rad för utgiftskategorier. Med underleverantörsrader för utgiftskategorier kan en projektledare köpa kategorier av tjänster eller produkter från leverantörer som de kan debitera för ett projekt.

Följ dessa steg för att skapa en underavtalsrad för utgiftskategorier i Project Operations.

1. I navigeringsfönstret väljer du **Underavtal** och öppnar sedan det underavtal du vill arbeta med.
2. På fliken **Underavtalsrader** väljer du **Ny** för att skapa en ny rad.
3. På sidan **Snabbregistrering**, i fältet **Transaktionsklass**, väljer du **Utgift** och anger eller väljer valfri erforderlig fältinformation.

Följande tabell innehåller information om fälten på detaljsidan **Underavtalsrad** och sidan **Snabbregistrering**.

| **Fält** |  **Beskrivning** |
| ----------| ---------------- |
| Namn | Namn på underavtalsraden. |
| Beskrivning | En kort beskrivning av de tjänste- eller produktkategorier som köps på underavtalsraden. |
| Radtyp | Detta fält har standardvärdet **Kvantitetsbaserad**.  |
| Faktureringsmetod | Faktureringsmetod för underavtalsraden. Utifrån radens faktureringsmetod är ett milstolpebaserat fakturaschema tillgängligt för faktureringsmetoden med fast pris.  |
| Transaktionsklass | Detta fält har standardvärdet **Tid**. Om du vill skapa underavtalsrader för inköp av produkter anger du fältet **Transaktionsklass** som **Utgift**. Detta fältvärde anger att underavtalsraden används för att registrera ett köp av en produkt- eller tjänstekategorier som ska användas för projekt. |
| Transaktionskategori | Välj transaktionskategorin. |
| Begärd start | Det datum då inköpskategorierna måste vara tillgängliga från leverantören. Den begärda starten används för att välja en projektprislista från de projektprislistor som bifogas underavtalet. Kostnaden för kategorin på underleverantörsraden kommer från den prislistan. |
| Begärt slut | Det datum då inköpskategorierna inte längre behövs. Detta datum avger en varning när en projektledare associerar denna underavtalsrad med specifika utgiftsprognoser för de projekt som är daterade efter detta datum. |
| Beställd kvantitet | Kvantiteten för den kategori som köps från leverantören. Om en projektledare tar ut för mycket av den inköpta kvantiteten visas en varning.  |
| Enhetsgrupp | Detta fältvärde baseras på den standardenhetsgrupp som har ställts in för den valda kategorin. |
| Enhet | Detta fältvärde återfår sitt standardvärde baserat på den standardenhetskonfiguration som har ställts in för den valda kategorin. Kombinationen av kategori och enhet används för att återställa enhetspriset för underavtalsraden till dess standardvärde. |
| Enhetspris | Fältvärdet för enhetspris återgår till standardvärdet genom att använda kombinationen av kategori och enhet från de kategoripriser som relaterar till den projektprislista som gäller för begärd start för underavtalsraden.  |
| Delsumma | Detta skrivskyddade fält beräknas automatiskt som kvantitetens enhetspris om värden för såväl kvantitets- som enhetspris anges. Om någotdera eller båda fält är tomma kan du ange ett värde manuellt i detta fält.  |
| Moms | Ange momsbeloppet.  |
| Totalbelopp | Totalbelopp för underavtalsraden inklusive moms. Detta fält beräknas som delsumma + moms.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
