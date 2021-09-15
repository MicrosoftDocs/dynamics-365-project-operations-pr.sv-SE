---
title: Underavtalsrader för tid
description: I detta ämne beskrivs hur du registrerar underavtalsrader för tid och registrerar köp av tid från leverantörer.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323888"
---
# <a name="subcontract-lines-for-time"></a>Underavtalsrader för tid

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Ett underavtal i Dynamics 365 Project Operations kan ha en underavtalsrad för tid. Underavtalsrader för tid tillåter en projektledare att köpa resurstid för leverantörer för att bemanna projektuppgifter och resurskrav.

Följ dessa steg för att skapa en underavtalsrad för tid i Project Operations.

1. I navigeringsfönstret väljer du **Underavtal** och öppnar ett underavtal.
2. På fliken **Underavtalsrader** väljer du **Ny** för att skapa en ny underavtalsrad.
3. På sidan **Snabbregistrering**, i fältet **Transaktionsklass**, väljer du **Tid**.
4. Ange återstående fältinformation och välj sedan **Spara**.

  Följande tabell innehåller information om fälten på sidorna **Underavtalsrad** och **Snabbregistrering**.

| **Fält** | **Beskrivning** |
| --- | --- |
| Namn | Namn på underavtalsraden. |
| Beskrivning | En kort beskrivning av tjänster som köps på underavtalsraden. | 
| Radtyp | Detta fält är ett standardvärde.  |
| Faktureringsmetod | Välj faktureringsmetod. Utifrån den refererade underavtalsradens faktureringsmetod görs ett milstolpebaserat fakturaschema tillgängligt för faktureringsmetoden med fast pris. |
| Transaktionsklass | Detta fält är ett standardvärde som anger huruvida underavtalsraden används för att registrera ett köp av underleverantörstid. |
| Roll | Rollen för de underavtalsresurser vars tid köps. Den roll som tilldelas underavtalsresurserna avgör kostnaden för köpet. |
| Begärd start | Det datum då när underleverantörers resurser måste börja arbeta. Den begärda starten används för att välja en projektprislista från de projektprislistor som bifogas underavtalet. Kostnaden för rollen på underavtalsraden hämtar sitt standardvärde från den prislistan. |
| Begärt slut | Det datum då tilldelningen av underleverantörers resurser upphör. Detta datum används för att visa varningar när en projektledare använder denna kapacitet för resurskrav som inträffar efter detta datum. |
| Beställd kvantitet | Antalet rolltimmar som köps från leverantören. Detta värde används för att visa varningar när en projektledare överutnyttjar denna kapacitet för resurskrav. |
| Enhetsgrupp | Detta fältvärde återgår till enhetsgruppen Tid och kan inte ändras.  |
| Enhet | Standardvärdet för detta fält är i basenheten "timmar" från enhetsgruppen Tid. Du kan ändra detta värde om du vill köpa valfri enhet i enhetsgruppen Tid, till exempel dag eller vecka. Kombinationen av Roll och Enhet används för att beräkna enhetspriset för underavtalsraden. |
| Enhetspris | Enhetspriset beräknas som standard utifrån kombinationen av Roll och Enhet från projektprislistan som gäller för det begärda startdatumet för underavtalsraden. Om det i den aktuella projektprislistan har angetts ett pris i en annan enhet än enheten på underactalsraden använder systemet enhetskonverteringen för att beräkna enhetspriset. |
| Delsumma | Detta är ett skrivskyddt fält som automatiskt beräknas som **Kvantitet x enhetspris** om värden för såväl kvantitets- som enhetspris anges. Om antingen kvantitet, enhetspris eller båda är tomma kan du ange ett värde i fältet. |
| Moms |  Ange momsbeloppet. |
| Totalbelopp | Totalbelopp för underavtalsraden efter moms ingår. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
