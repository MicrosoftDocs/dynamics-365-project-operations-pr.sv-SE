---
title: Underavtalsrader för produkter
description: I detta ämne finns information om hur du registrerar underavtalsrader för produkter och använder de olika fälten för att registrera produktinköp från leverantörer.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323708"
---
# <a name="subcontract-lines-for-products"></a>Underavtalsrader för produkter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En underleverantör i Dynamics 365 Project Operations kan ha en underavtalsrad för produkter. Raderna gör att en projektledare kan köpa produkter från leverantörer som de sedan kan använda för projektuppgifter.

Skapa en underavtalsrad för produkter i Project Operations genom att följa stegen nedan.

1. På navigeringssidan väljer du **Underavtal** och öppnar sedan det underavtal du vill arbeta med. 
2. På fliken **Underavtalsrader** väljer du **+ Ny** för att skapa en ny underavtalsrad.
3. På sidan **Snabbregistrering**, i fältet **Transaktionsklass**, väljer du **Material** och anger eller väljer erforderlig fältinformation. 
4. Välj **Spara**.

Följande tabell innehåller information om fälten på sidorna för **Detaljinformation för underavtalsrader** och **Snabbregistrering** eftersom dessa är relevanta för inköp av produkter.

| Fält | Beskrivning |
| ----- | ----------- |
| Namn | Namn på underavtalsraden. |
| Beskrivning | En kort beskrivning av produkter som beställs på underavtalsraden. |
| Radtyp | Detta fältvärde har standardvärdet **Kvantitetsbaserad**. |
| Faktureringsmetod |  Faktureringsmetod för underavtalsraden. För faktureringsmetoder med fast pris finns ett milstolpebaserat fakturaschema. |
| Transaktionsklass | Detta fältvärde har standardvärdet **Tid**. Om du vill skapa underavtalsrader för inköp av produkter gå du till fältet **Transaktionsklass** och väljer **Material**. Detta val anger att underavtalsraden används för att registrera ett köp av produkter som ska användas i projekt. |
| Välj produkt | Välj om produkten som köps bibehållss i produktkatalogen eller om den är en oregistrerad produkt. |
| Produkt | Välj en aktiv produkt från katalogen. Detta fält är endast tillgängligt när **Välj produkt** har angetts som **Befintlig**. |
| Produkt ej i register | Ange namnet på den oregistrerade produkten. Detta fält är endast tillgängligt när **Välj produkt** har angetts som **Oregistrerad**.  |
| Begärt leveransdatum | Välj erforderligt leveransdatum för produkterna. Detta datum används också för att välja en projektprislista bland de projektprislistor som bifogas underavtalet. Kostnaden för produkten på underavtalsraden hämtar sitt standardvärde från den prislistan. |
| Kontrakterat leveransdatum | Välj det datum då produkterna ska levereras enligt avtal.  |
| Beställd kvantitet | Ange kvantiteten för den produkt som köps från leverantören. Om en projektledare tar ut för mycket av denna kvantitet visas en varning. |
| Enhetsgrupp | Detta värde återfår sitt standardvärde endast för katalogprodukter. När både **Produkt** och **Begärt leveransdatum** har valts väljer systemet tillämpbar prislista baserat på leveransdatum. De relaterade prislisteposterna genomsöks efter den matchande produkten. Värdena för enhet och enhetsgrupp återgår till sina standardvärden i samband med installationen av posten för prislistepost. |
| Enhet | Detta värde återgår till enhetskonfigurationen för posten för prislisteobjekt. Du kan ändra detta till en annan enhet vid behov. Kombinationen av produkt och enhet används för att återställa enhetspriset för underavtalsraden för befintliga katalogprodukter. |
| Enhetspris | Enhetspriset återgår till standardvärdet genom att använda kombinationen av produkt och enhet från de prislisteposter som gäller för det begärda leveransdatumet för underavtalsraden.  |
| Delsumma | Detta skrivskyddade fält beräknas som Kvantitet x enhetspris om båda fälten har angetts. Om antingen fältet **Kvantitet** eller fältet **Enhetspris** - eller båda - är tomma, kan du ange ett värde manuellt.  |
| Moms | Ange värdet för momsbelopp. |
| Totalbelopp | Detta beräknade fält visar totalbeloppet för underavtalsraden efter det att moms har inkluderats. Värdet i detta fält beräknas som delsumma + moms. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
