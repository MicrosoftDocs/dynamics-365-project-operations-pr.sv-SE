---
title: Underavtalsrader för utgiftskategorier
description: I den här artikeln finns information om hur du registrerar underleverantörsrader för utgifter och hur du använder fälten för att registrera köp av tid från leverantörer.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261863"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Underavtalsrader för utgiftskategorier

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Ett underavtal i Dynamics 365 Project Operations kan ha en rad för utgiftskategorier. Med underleverantörsrader för utgiftskategorier kan en projektledare köpa kategorier av tjänster eller produkter från leverantörer som de kan debitera för ett projekt.

Följ dessa steg för att skapa en underavtalsrad för utgiftskategorier i Project Operations.

1. I navigeringsfönstret väljer du **Underavtal** och öppnar sedan det underavtal du vill arbeta med.
2. På fliken **Underavtalsrader** väljer du **Ny** för att skapa en ny rad.
3. På sidan **Snabbregistrering**, i fältet **Transaktionsklass**, väljer du **Utgift** och anger eller väljer valfri erforderlig fältinformation.

Följande tabell innehåller information om fälten på detaljsidan **Underavtalsrad** och sidan **Snabbregistrering**.

| **Fält** | **Beskrivning** | **Funktionellt påverkan** |
| --- | --- | --- |
| Namn | Namn på underleverantörsraden för identifiering. | Detta visas som den första kolumnen i alla uppslag baserat på underkonsekvensrader. |
| Beskrivning | En kort beskrivning av de utgiftskategorier som köps på underleverantörsraden. | Nej |
|Linjetyp | Detta fält har standardvärdet **Kvantitetsbaserad**. |Nej |
| Faktureringsmetod | Detta är en tillvalssats som representerar de två huvudentreprenadmodeller som stöds av Project Operations: **Fast pris** och **Tid och material**. | Ett milstolpebaserat fakturaschema görs tillgängligt för underleverantörsrader om faktureringsmetoden Fast pris har valts. |
| Transaktionsklass | Detta fält har standardvärdet **Tid**. Om du vill skapa underavtalsrader för inköp av produkter anger du fältet **Transaktionsklass** som **Utgift**.  | Detta indikerar att underleverantörsraden används för att registrera inköp av en kategoriutgifter som ska användas för projekt. |
| Transaktionskategori | Visar en lista med aktiva transaktionskategorier i systemet. |Nej |
| Begärd start | Ange det datum då kategorierna för inköp måste vara tillgängliga från leverantören. | Begärd start används för att välja en projektprislista från de projektprislistor som är kopplade till underleverantörslistan. Kostnaden för kategorin på underleverantörsraden kommer från den prislistan. |
| Begärt slut | Ange det datum då köpkategorierna inte längre behövs. | Används för att visa varningar när en projektledare associerar denna underleverantör till specifika utgifter för det projekt som krävs efter detta datum. |
| Beställd kvantitet | Kvantitet för den kategori som köps från leverantören. | Detta används för att visa varningar när en projektledare förser med för mycket information från den här kvantiteten.|
| Enhetsgrupp | Standardvärdet baseras på den standardenhetsgrupp som har ställts in för den valda kategorin. |Nej |
| Enhet | Standarden är baserad på standardenheten som är inställd för den valda kategorin.  | Kombinationen av **Kategori** och **Enhet** används som standard eller beräknas för enhetspriset för underleverantörsraden.  |
| Enhetspris | Standardvärdet använder kombinationen av **Kategori** och **Enhet** från de kategoripriser som är relaterade till projektprislistan, som gäller vid den begärda starten av underleverantörsraden. |Nej |
| Delsumma | Det här är ett skrivskyddat fält som beräknas som enhetspris för kvantitet X om både kvantitets- och enhetsprisvärden anges. Om något av eller båda fälten är tomma kan du ange ett värde i det här fältet. |Nej |
| Moms | Ange momsbeloppet. |Nej |
| Totalbelopp | Totalbelopp för underavtalsraden inklusive moms. Detta fält beräknas som delsumma + moms. |Nej |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
