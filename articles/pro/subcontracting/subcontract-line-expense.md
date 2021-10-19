---
title: Underavtalsrader för utgiftskategorier
description: I detta ämne finns information om hur du registrerar underavtalsrader för utgifter och använder fälten för att registrera tidsinköp från leverantörer.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506121"
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
