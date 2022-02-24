---
title: Post för utgift (enkel)
description: I det här ämnet finns information om hur du arbetar med utgiftsposter i en enkel distribution.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590968"
---
# <a name="expense-entry-lite"></a>Post för utgift (enkel)

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Grundläggande, eller enkel, utgiftshantering är möjligheten att registrera enkla utgifter. Du kan registrera utgifter för ett projekt och sedan kommer projektgodkännaren att granska och godkänna dem.

Mer information om utgiftsfunktioner i finns i Dynamics 365 Project Operations, se [Utgiftsöversikt](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Registrera en grundläggande utgift

Du kan registrera dina utgifter så att du kan skicka dem till god kännaren.

1. Gå till **Utgifter** och välj **Ny**.
2. Ange önskad utgiftsinformation på sidan **Ny utgift** och välj sedan **Spara**.

## <a name="submit-a-basic-expense"></a>Skicka in en grundläggande utgift

När du har registrerat alla dina utgifter och du är redo att godkänna dem måste du skicka in dem.

1. Gå till **Utgifter** och välj en utgift. Du kan också markera alla utgifter genom att använda kryssrutan längst upp.
2. Välj **Skicka**. Systemet bearbetar de markerade posterna och skapar sedan en förfrågan om utgiftsgodkännande.

## <a name="add-an-attachment"></a>Lägg till en bifogad fil

Du kan komma att behöva förse godkännaren med ytterligare dokumentation om din utgift. Du kan bifoga ett kvitto i tidslinjen för utgiftsposten. Välj **Redigera** i avsnittet **Tidslinje**, och välj sedan ikonen för gem för att bifoga ditt kvitto.

## <a name="recall-a-basic-expense"></a>Återkalla en grundläggande utgift

När du skickar en utgift av misstag kan du återkalla den. Den tid som krävs för att återkalla en utgiftspost beror på godkännandestadiet.  Om godkännaren ännu inte har godkänt posten kan återkallelsen ske omedelbart. Om posten redan har godkänts ombeds godkännaren emellertid att godkänna återkallandet och återställa transaktionen.

1. Gå till **Utgifter** och välj sedan den kostnad du vill återkalla i listan över utgifter.
2. Välj **återkalla**. Om utgiftsposten ännu inte har godkänts återkallar systemet den omedelbart. Om utgiftsposten redan har godkänts skapas en förfrågan om återkallande för att meddela godkännaren om att du vill återställa utgiften. Godkännaren bekräftar då att återställandet kan utföras och att posten returneras.

## <a name="delete-a-basic-expense"></a>Ta bort en grundläggande utgift

Utgifter som ännu inte har skickats kan tas bort. Om du vill ta bort en utgift som redan har skickats måste du först återkalla den.

## <a name="see-also"></a>Se även

- [Översikt över godkännanden](../approvals/approvals-overview.md)
