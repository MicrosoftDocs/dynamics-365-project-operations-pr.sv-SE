---
title: Underavtalsrader för produkter
description: I denna artikel beskrivs hur du registrerar underleverantörsrader för produkter och använder de olika fälten för att registrera produktinköp från leverantörer.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff9636f86102fa671a443d7646614070b3e2ee79
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934388"
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

| Fält | Beskrivning | Funktionellt påverkan|
| ----- | ----------- | ----------- |
| Namn | Namn på underleverantörsraden för identifiering. |Detta visas som den första kolumnen i alla uppslag baserat på underkonsekvensrader.
| Beskrivning | En kort beskrivning av produkter som beställs på underavtalsraden. | Nej |
| Linjetyp | Detta fält har standardvärdet **Kvantitetsbaserad**. |Nej |
| Faktureringsmetod | Detta är en tillvalssats som representerar de två huvudentreprenadmodeller som stöds av Project Operations: **Fast pris** och **Tid och material**. | Baserat på den valda faktureringsmetoden milstolpebaserat fakturaschema görs tillgängligt för underleverantörsrader om faktureringsmetoden Fast pris har valts. |
| Transaktionsklass |Detta fält har standardvärdet **Tid**. Om du vill skapa underavtalsrader för inköp av produkter anger du fältet **Transaktionsklass** som **Material**.  | Detta indikerar att underleverantörsraden används för att registrera inköp av produkter som ska användas i projekt. |
| Välj produkt | Välj om produkten som köps bibehållss i produktkatalogen eller om den är en oregistrerad produkt. |Nej |
| Produkt | Välj en aktiv produkt från katalogen. Detta fält är endast tillgängligt när **Välj produkt** har angetts som **Befintlig**. |Kombinationen av **Produkt** och **Enhet** används som standard eller beräknas för enhetspriset för underleverantörsraden.
| Produkt ej i register | Ange namnet på den oregistrerade produkten. Detta fält är endast tillgängligt när **Välj produkt** har angetts som **Oregistrerad**.  |Inköpspriset fylls inte i automatiskt för inskrivningsprodukter.|
| Begärt leveransdatum | Ange det leveransdatum som krävs för produkterna.| Detta datum används också för att välja en projektprislista bland de projektprislistor som bifogas underavtalet. Kostnaden för produkten på underavtalsraden hämtar sitt standardvärde från den prislistan. |
| Kontrakterat leveransdatum | Ange det datum då produkterna har avtalats om att levereras.  |Nej|
| Beställd kvantitet | Ange kvantiteten för den produkt som köps från leverantören.| Detta används för att visa varningar när en projektledare förser med för mycket information från den här kvantiteten.|
| Enhetsgrupp | Detta värde återfår sitt standardvärde endast för katalogprodukter. |När både **Produkt** och **Begärt leveransdatum** har valts väljer systemet tillämpbar prislista baserat på leveransdatum. De relaterade prislisteposterna genomsöks efter den matchande produkten. Värdena för enhet och enhetsgrupp återgår till sina standardvärden i samband med installationen av posten för prislistepost. |
| Enhet | Det här värdet är standardvärdet för enheten som angetts för posten för prislisteobjekt. Du kan ändra detta till en annan enhet vid behov.| Kombinationen av produkt och enhet används för att återställa enhetspriset för underavtalsraden för befintliga katalogprodukter. |
| Enhetspris | Enhetspriset återgår till standardvärdet genom att använda kombinationen av produkt och enhet från de prislisteposter som gäller för det begärda leveransdatumet för underavtalsraden.  |Nej |
| Delsumma | Detta skrivskyddade fält beräknas som Kvantitet x enhetspris om båda fälten har angetts. Om antingen fältet **Kvantitet** eller fältet **Enhetspris** - eller båda - är tomma, kan du ange ett värde manuellt.  |Nej |
| Moms | Ange värdet för momsbelopp. |Nej |
| Totalbelopp | Detta beräknade fält visar totalbeloppet för underavtalsraden efter det att moms har inkluderats. Värdet i detta fält beräknas som delsumma + moms. |Nej |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
