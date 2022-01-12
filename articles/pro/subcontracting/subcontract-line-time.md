---
title: Underavtalsrader för tid
description: I detta ämne beskrivs hur du registrerar underavtalsrader för tid och registrerar köp av tid från leverantörer.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547266"
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

| **Fält** | **Beskrivning** | **Funktionellt påverkan** |
| --- | --- | --- |
| Namn | Namn på underleverantörsraden för identifiering. | Detta visas som den första kolumnen i alla uppslag baserat på underkonsekvensrader. |
| Beskrivning | En kort beskrivning av tjänster som köps på underavtalsraden. |Nej |
| Linjetyp |   Detta fält har standardvärdet **Kvantitetsbaserad**.| Nej |
| Faktureringsmetod | Detta är en tillvalssats som representerar de två huvudentreprenadmodeller som stöds av Project Operations: **Fast pris** och **Tid och material**. | Baserat på den valda faktureringsmetoden milstolpebaserat fakturaschema görs tillgängligt för underleverantörsrader om faktureringsmetoden Fast pris har valts. |
| Transaktionsklass | Standardvärdet är **Tid**. | Detta indikerar att underleverantörsraden används för att registrera ett köp av underleverantörstid. |
| Roll | Välj rollen för de underleverantörsresurser vars tid köps. | Rollen som utförs av underleverantörerna avgör kostnaden för inköpet. |
| Begärd start | Ange det datum då underleverantörsresurserna krävs för att börja arbeta. | Begärd start används för att välja en projektprislista från de projektprislistor som är kopplade till underleverantörslistan. Kostnaden för rollen på underleverantörsraden kommer från den prislistan. |
| Begärt slut | Ange datumet då underleverantörsresursens tilldelning slutar. | Detta används för att visa varningar när en projektledare förser sig från kapaciteten för resurskraven som inträffar efter detta datum. |
| Beställd kvantitet | Ange antalet timmar för rollen som köps från leverantören. | Detta används för att visa varningar när en projektledare förser sig från kapaciteten för resurskraven som inträffar. |
| Enhetsgrupp | Standardvärdet är **Tidsenhetsgrupp**, som inte kan ändras. | Nej|
| Enhet | Standardvärdet för det här fältet är basenhet för timmar från **Tidsenhetsgrupp**. Du kan ändra detta värde om du vill köpa valfri **Tidsenhetsgrupp**, till exempel dag eller vecka. | Kombinationen av **Roll** och **Enhet** används som standard eller beräknas för enhetspriset för underleverantörsraden. |
| Enhetspris | Standardpriset använder kombinationen av **Roll** och **Enhet** från projektprislistan som gäller för **Begärd start** datum för underleverantörslinjen. | Om det i den aktuella projektprislistan har angetts ett pris i en annan enhet än enheten på underactalsraden använder systemet enhetskonverteringen för att beräkna enhetspriset. |
| Delsumma |    Det här är ett skrivskyddat fält som beräknas som enhetspris för kvantitet X om både kvantitets- och enhetsprisvärden anges. Om antingen kvantitet, enhetspris eller båda är tomma kan du ange ett värde i fältet. | Nej|
| Moms |   Ange momsbeloppet. |Nej |
| Totalbelopp | Totalbelopp för underavtalsraden inklusive moms. Detta fält beräknas som delsumma + moms.|Nej |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]