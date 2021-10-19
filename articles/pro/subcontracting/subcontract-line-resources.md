---
title: Resurser för underavtalsrad
description: I detta ämne beskrivs hur du anger dedikerade resurser som tillhandahålls av leverantören för en viss underleverantörsrad för tid.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558479"
---
# <a name="subcontract-line-resources"></a>Resurser för underavtalsrad

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I Dynamics 365 Project Operations kan en leverantör ange resurser som ska användas för att tillhandahålla den resurskapacitet som köps på underleverantörsraden för tid.

## <a name="create-subcontract-line-resources"></a>Skapa resurser för underavtalrad

Skapa resurser för underavtal genom att följa stegen nedan.

1. I navigeringsfönstret väljer du **Underavtal** och öppnar sedan det underavtal du vill arbeta med.
2. Öppna underavtalsraden för den tid som du vill ange leverantörsresurser för.
3. På fliken **Resurser för underavtalsrad** väljer du **+ Ny resurs för underavtalsrad** i underrutnätet.
4. Ange den information som krävs på sidan **Ny underleverantörsresurs för rad** och välj sedan **Spara och stäng**.

I följande tabell förklaras fälten på resursen för underavtalsrad.

| Fält | Beskrivning | Funktionellt påverkan |
| ----- | ----------- | ----------------- |
| Bokningsbar resurs | Välj en bokningsbar resurs av typen **Kontraktanställd** som du vill använda som resurs på underavtalsraden.| Lämna det här fältet tomt om du inte har skapat en bokningsbar resurs för kontraktarbetaren. När du sparar posten skapas en bokningsbar resurs.  |
| Kontaktperson | Du kan skapa en underleverantörsresurs från en befintlig kontakt. Använd uppslagsvyn om du vill visa listan över aktiva kontakter i systemet. Välj en kontakt för leverantören av detta underavtal. Om den valda kontakten inte är en giltig kontakt för leverantören i underleverantören sparas inte resursposten för underkontaktraden.| Om det inte finns någon bokningsbar resurs för den valda kontakten skapar systemet en bokningsbar resurs för den valda kontakten innan resursen för underavtalsraden skapas. |
| Användare | Du kan skapa en resurs för underleverantörsrad genom att välja en aktiv användare. Använd uppslagsvyn om du vill visa listan över aktiva användare i systemet.| Om det inte finns någon bokningsbar resurs för den valda användaren skapar systemet en bokningsbar resurs för den valda användaren innan resursen för underavtalsraden skapas. |
| Startdatum | Det datum då underavtalsmedarbetarens tilldelning startar.| Om denna resurs bokas för en period som infaller före detta datumintervall visas en varning. |
| Slutdatum | Det datum då underavtalsmedarbetarens tilldelning avslutas.| Om denna resurs bokas för en period som infaller efter detta datumintervall visas en varning. |
| Insats | Totalt antal insatstimmar som den kontrakterade arbetaren ska lägga ned på den här underleverantörsraden.| Om resursen bokas utöver den insats som tilldelas för den här resursen, visas en varning. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
