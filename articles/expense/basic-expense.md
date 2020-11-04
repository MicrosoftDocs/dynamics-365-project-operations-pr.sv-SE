---
title: Post för utgift (enkel)
description: I det här ämnet finns information om hur du arbetar med utgiftsposter i en enkel distribution.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085424"
---
# <a name="expense-entry-lite"></a>Post för utgift (enkel)

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Grundläggande, eller enkel, utgiftshantering är möjligheten att registrera enkla utgifter. Du kan registrera utgifter för ett projekt och sedan kommer projektgodkännaren att granska och godkänna dem.

Mer information om utgiftsfunktioner i Dynamics 365 Project Operations finns i [Utgiftsöversikt](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Registrera en grundläggande utgift

Du kan registrera dina utgifter så att du kan skicka dem till god kännaren.

1. Gå till **Utgifter** och välj **Ny**.
2. Ange önskad utgiftsinformation på sidan **Ny utgift** och välj sedan **Spara**.

## <a name="submit-a-basic-expense"></a>Skicka in en grundläggande utgift

När du har registrerat alla dina utgifter och du är redo att godkänna dem måste du skicka in dem.

1. Gå till **Utgifter** och välj en utgift. Du kan också markera alla utgifter genom att använda kryssrutan längst upp.
2. Välj **Skicka**. Systemet bearbetar de markerade posterna och skapar sedan en förfrågan om utgiftsgodkännande.

## <a name="recall-a-basic-expense"></a>Återkalla en grundläggande utgift

När du skickar en utgift av misstag kan du återkalla den. Den tid som krävs för att återkalla en utgiftspost beror på godkännandestadiet.  Om godkännaren ännu inte har godkänt posten kan återkallelsen ske omedelbart. Om posten redan har godkänts ombeds godkännaren emellertid att godkänna återkallandet och återföra transaktionen.

1. Gå till **Utgifter** och välj sedan den kostnad du vill återkalla i listan över utgifter.
2. Välj **återkalla**. Om utgiftsposten ännu inte har godkänts återkallar systemet den omedelbart. Om utgiftsposten redan har godkänts skapas en förfrågan om återkallande för att meddela godkännaren om att du vill återföra utgiften. Godkännaren bekräftar då att återföringen kan utföras och att posten returneras.

## <a name="delete-a-basic-expense"></a>Ta bort en grundläggande utgift

Utgifter som ännu inte har skickats kan tas bort. Om du vill ta bort en utgift som redan har skickats måste du först återkalla den.

## <a name="see-also"></a>Se även

- [Översikt över godkännanden](../approvals/approvals-overview.md)
