---
title: Resurser för underavtalsrad
description: I detta ämne beskrivs hur du anger dedikerade resurser som tillhandahålls av leverantören för en viss underleverantörsrad för tid.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323393"
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
4. På sidan **Ny milstolpe för underavtalsrad** anger du erforderlig information och väljer sedan **Spara och stäng**.

I följande tabell förklaras fälten på resursen för underavtalsrad.

| Fält |  Beskrivning |
| ----- | ------------ |
| Bokningsbar resurs | Välj en bokningsbar resurs av typen "Kontraktanställd" som du vill använda som resurs på underavtalsraden. Lämna det här fältet tomt om du inte har skapat någon bokningsbar resurs för den kontraktanställde ännu. När du sparar posten skapas en bokningsbar resurs.  |
| Kontaktperson | Om fältet **Bokningsbar resurs** är tomt kan du skapa en underavtalsresurs från en befintlig kontakt. Använd uppslagsvyn om du vill visa listan över aktiva kontakter i systemet. Välj en kontakt för leverantören av detta underavtal. Den kontaktperson du väljer verifieras när du sparar posten. Om den valda kontakten inte är en giltig kontakt sparas inte posten. Om det inte finns någon bokningsbar resurs för den valda kontakten skapar systemet en bokningsbar resurs för den valda kontakten innan resursen för underavtalsraden skapas. |
| Användare | Om fältet **Bokningsbar resurs** är tomt kan du skapa en underavtalsresurs genom att välja en aktiv användare. Använd uppslagsvyn om du vill visa listan över aktiva användare i systemet. Om det inte finns någon bokningsbar resurs för den valda användaren skapar systemet en bokningsbar resurs för den valda användaren innan resursen för underavtalsraden skapas. |
| Startdatum | Det datum då underavtalsmedarbetarens tilldelning startar. Om denna resurs bokas för en period som infaller före detta datumintervall visas en varning. |
| Slutdatum | Det datum då underavtalsmedarbetarens tilldelning avslutas. Om denna resurs bokas för en period som infaller efter detta datumintervall visas en varning. |
| Insats | Totalt antal insatstimmar som underavtalsmedarbetaren ska lägga ned på denna underavtalsrad. Om denna resurs bokas utöver den insats som tilldelats för denna resurs, visas en varning. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
