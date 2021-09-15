---
title: Detaljerad sidhuvudinformation för underavtal
description: Detta ämne förklarar de funktioner som tillhandahålls i underavtalshuvudet i Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323663"
---
# <a name="header-details-for-subcontracts"></a>Detaljerad sidhuvudinformation för underavtal

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Detta ämne förklarar de funktioner som tillhandahålls i underavtalshuvudet i Dynamics 365 Project Operations.

I takt med att projektledare planerar och genomför projekt kan de anlita underleverantörer och köpa produkter och tjänster från leverantörer. När en projektledare behöver köpa produkter eller tjänster kan han eller hon skapa ett underavtal i Project Operations.

Skapa ett underavtal genom att följa stegen nedan.

1. I navigeringsfönstret väljer du **Underavtal**, innan du på sidan **Underavtal** väljer **Ny**.
2. Ange information som krävs och klicka sedan på **Spara**.

    Följande tabell innehåller information om fälten på sidan Underavtalshuvud.

    | **Fält** | **Beskrivning** |
    | --- | --- | 
    | Namn | Namnet på underavtalet. |
    | Beskrivning | En kort beskrivning av tjänster produkter som köps i underavtalet. |
    | Leverantör | Namnet på det företag som produkterna och tjänsterna köps från. Denna kontopost har relationstypen **Säljare** eller **Leverantör**. |
    | underavtalsdatum | Det datum då underavtalet skapades. |
    | Statusorsak | Status för underavtalet. |
    | Valuta | Den valuta som produkter och tjänster köps i. Värdet i detta fält kommer från som standard från leverantörskontot, men kan ändras. Projektprislistor som används för prissättning av produkter och tjänster i underavtalet ska vara i den här valutan. Prislistor i andra valutor kan inte associeras med underavtalet. Kostnaden för produkter och tjänster somd etta underavtal medför registreras i denna valuta för projektet. |
    | Kontrakteringsenhet | Den avdelning i företaget som ingår ett köpekontrakt eller ett underavtal med leverantören. |
    | Betalningsvillkor | Betalningsvillkoren för leverantörsfakturor som utfärdas för denna underleverantör. Värdet i detta fält kommer från som standard från leverantörskontoposten. |
    | Betalningsadress | Adressen där betalningen på leverantörsfakturor skickas. Värdet i detta fält kommer från som standard från leverantörskontoposten. |
    | Fakturera till namn | Namnet på den person eller avdelning i det leverantörsföretag som ska skicka fakturan. Värdet i det här fältet kommer från leverantörskontoposten och används som namnet på den primära kontakten på leverantörsfakturor som skapas för detta underavtal. |
    | Faktureringsadress | Den adress som används på fakturor från denna leverantör. Värdet i detta fält kommer från som standard från leverantörskontoposten. Denna adress används också som faktureringsadress på leverantörsfakturor som skapas för den här underleverantören. |
    | Delsumma | Om ett underavtal inte har några rader anger du ett värde i det här fältet som anger orderns delsumma före moms. Om underavtalet har rader är det här fältet skrivskyddat. Det belopp som visas är delsummans belopp från alla rader i underavtalet. |
    | Total moms | Om ett underavtal inte har några rader anger du ett värde i det här fältet som anger momsen i detta underavtal. Om underavtalet har rader är det här fältet skrivskyddat. Det belopp som visas är summan av momsbeloppet från alla rader i underavtalet. |
    | Totalbelopp |  Detta beräknade fält visar totalbeloppet för underavtalet efter det att moms har inkluderats.  |
    | Bekräftelsedatum | Det datum då underavtalet bekräftades.  |
    | Begärd av | Standardvärdet för detta fält är namnet på den användare som skapar underavtalet. Detta värde kan ändras av den som skapade underavtalet i syfte att ange den person för vilken han eller hon skapar underavtalet.  |
    | Leverantörens kontoansvariga | Namnet på den primära kontakten för leverantörskontot. Värdet i detta fält kommer från som standard från leverantörskontoposten. Detta fältvärde kan ändras av användaren om denne vill välja en annan kontakt som leverantörskontohanterare för underavtalet. E-postaviseringar och prisförseningar kan konfigureras och skickas av den här kontakten. |


