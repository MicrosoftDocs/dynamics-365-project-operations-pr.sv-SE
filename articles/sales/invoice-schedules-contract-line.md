---
title: Skapa ett faktureringsschema för en projektbaserad kontraktrad
description: I det här ämnet finns information om hur du skapar faktureringsscheman och milstolpar på kontraktrader.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 51a34e5a62fdadf7a6601f0a635efd484238f3565abcac8a1f7de3d49cebf23e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999698"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Skapa ett faktureringsschema för en projektbaserad kontraktrad 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Du kan skapa ett faktureringsschema för en projektbaserad kontraktrad. Fakturering tillåts endast efter att kontraktet har vunnits och du skapar ett projektkontrakt. Med ett faktureringsschema kan du skapa utkast till fakturor för en projektbaserad kontraktrad automatiskt. Om du däremot endast skapar fakturor manuellt kan du hoppa över att skapa faktureringsscheman på kontraktrader.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Skapa ett faktureringsschema för tid och material för en kontraktrad

När en projektbaserad kontraktrad har faktureringsmetoden Tid och material kan du generera ett datumbaserat faktureringsschema. Följ stegen nedan om du vill generera ett datumbaserat faktureringsschema automatiskt.

1. Gå till **Inställningar** > **Faktureringsfrekvenser** och konfigurera en faktureringsfrekvens.
2. Gå till projektkontraktsposten och till fliken **Sammanfattning**, där du väljer ett datum i fältet **Begärt leveransdatum**.
3. Öppna kontraktraden **Tid och material** som du skapar ett datumbaserat faktureringsschema för. 
4. Under fliken **Faktureringsschema** väljer du faktureringsstartdatum och faktureringsfrekvens.
5. I underrutnätet väljer du **Generera faktureringsschema**. Faktureringsschemat genereras med fälten **Fakturans kördatum**, **Transaktionens sista datum** och **Körstatus** på följande sätt:

    - **Fakturans kördatum**: Detta datum dikteras utifrån faktureringsfrekvensen.
    - **Transaktionens sista datum**: Dagen före fakturans kördatum.
    - **Körstatus**: Automatiskt inställd på **Ej körd**. När jobbet för automatiskt skapande av faktura körs för ett visst fakturadatum uppdateras detta fält till **Körning klar** eller **Körning misslyckades**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Skapa ett faktureringsschema för fast pris för en kontraktrad

När kontraktraden har faktureringsmetoden Fast kan du skapa ett milstolpebaserat faktureringsschema. 

> [!NOTE]
> Det går inte att skapa milstolpar på en kontraktrad om det inte finns något projekt mappat till kontraktraden.

Utför följande steg för att generera ett milstolpebaserat faktureringsschema för en fast uppsättning milstolpar som är jämnt fördelade över kalenderperioden.

1. Gå till **Inställningar** > **Faktureringsfrekvenser** och konfigurera en faktureringsfrekvens.
2. Gå till projektkontraktsposten och till fliken **Sammanfattning**, där du väljer ett datum i fältet **Begärt leveransdatum**.
3. Öppna kontrakttraden **Fast pris** som du skapar ett milstolpeschema för. Under fliken **Faktureringsmilstolpar** väljer du faktureringsstartdatum och faktureringsfrekvens. 
4. I underrutnätet väljer du **Generera periodiska milstolpar**. Faktureringsschemat skapas med fälten **Milstolpenamn**, **Milstolpedatum** och **Milstolpebelopp** enligt följande:

    - **Milstolpens namn**: Detta namn bestäms av fakturafrekvensen.
    - **Milstolpedatum**: Detta datum dikteras utifrån faktureringsfrekvensen.
    - **Milstolpebelopp**: Detta belopp beräknas genom att dela kontraktbeloppet på kontraktraden med antalet milstolpar som styrs av frekvensen, faktureringsstarten och önskade leveransdatum.

    Om kontraktraden har ett värde i fältet **Uppskattat momsbelopp** fördelas även detta fält jämnt till varje milstolpe när periodiska milstolpar genereras.

Faktureringsmilstolpar ska vara lika med det kontrakterade värdet på kontraktraden. Om de inte gör det visas ett felmeddelande på sidan **Kontraktrad**. Du kan åtgärda felet genom att kontrollera att faktureringsmilstolparna summerar det kontrakterade värdet på raden genom att skapa, redigera eller ta bort milstolpar. När ändringarna har gjorts uppdaterar du sidan för att ta bort felet.

### <a name="manually-create-milestones"></a>Skapa milstolpar manuellt

Du kan generera milstolpar med fast pris manuellt när de inte delas periodiskt. Följ stegen nedan om du vill skapa en milstolpe manuellt.

1. Öppna kontraktraden för fast pris som du skapar en milstolpe för och gå till fliken **Faktureringsschema**, där du i underrutnätet väljer **+ Skapa ny milstolpe för kontraktrad**. 
2. På sidan **Skapa milstolpe** anger du den nödvändiga informationen baserat på följande tabell.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| Milstolpens namn | Snabbregistrering | Textfält för milstolpens namn. | Detta förs över till milstolpen i projektets kontraktrad och till fakturan. |
| Projektuppgift | Snabbregistrering | Om milstolpen är knuten till en projektuppgift använder du den här referensen för att lägga till anpassad logik och ange milstolpens status utifrån uppgiftens status. | Programmet har inte någon inverkan nedströms för den här referensen till en uppgift. |
| Milstolpens datum | Snabbregistrering | Ange det datum då processen för automatiskt skapande av faktura ska söka efter statusen för den här milstolpen för att överväga fakturering. | Detta förs över till milstolpen i projektets kontraktrad och till fakturan. |
| Fakturastatus | Snabbregistrering | När en milstolpe skapas är statusen alltid inställd på **Inte klar för fakturering** eller **Ej påbörjad**. | Detta förs över till milstolpen i projektets kontraktrad och till fakturan. |
| Radbelopp | Snabbregistrering | Beloppet eller värdet för den milstolpe som ska faktureras kunden. | Detta förs över till milstolpen i projektets kontraktrad och till fakturan. |
| Moms | Snabbregistrering | Momsbeloppet som används på milstolpen. | Detta förs över till milstolpen i projektets kontraktrad och till fakturan. |

3. Välj **Spara och stäng**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]