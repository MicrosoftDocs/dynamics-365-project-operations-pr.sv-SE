---
title: Resurser för underavtalsrad
description: Den här artikeln innehåller information om hur du anger dedicerade resurser som tillhandahålls av leverantören för en viss underleverantörsrad för tid.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522395"
---
# <a name="subcontract-line-resources"></a>Resurser för underavtalsrad

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

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
