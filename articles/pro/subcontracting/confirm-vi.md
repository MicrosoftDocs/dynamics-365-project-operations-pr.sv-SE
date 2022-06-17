---
title: Bekräfta en projektfaktura för leverantör
description: I denna artikel beskrivs hur du bekräftar en projektleverantörsfaktura i Microsoft Dynamics 365 Project Operations och den ekonomiska påverkan av att bekräfta en projektleverantörsfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932456"
---
# <a name="confirm-a-project-vendor-invoice"></a>Bekräfta en projektfaktura för leverantör

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

När du har kontrollerat alla rader på en leverantörsfaktura i Microsoft Dynamics 365 Project Operations kan du bekräfta leverantörsfakturan med hjälp av åtgärden Bekräfta.

När du väljer **Bekräfta** på en leverantörsfaktura sker följande:

1. Leverantörsfakturans tillstånd uppdateras till **Bekräftad**.
2. Den bekräftade leverantörsfakturan och dess relaterade poster blir skrivskyddade och kan inte redigeras eller tas bort.
3. Om några faktiska kostnader refererar till leverantörens fakturarad som en del av matchningsprocessen kommer alla faktiska kostnader som är kopplade till den refererade leverantörens fakturarad att återställas.
4. Nya faktiska kostnader skapas med hjälp av informationen på leverantörens fakturarad.
5. När leverantörsfakturan är bekräftad kan du inte längre skapa korrigeringsjournaler, behandla återkallning av tidsposter eller avbryta godkännande av den ursprungliga tiden, utgiften eller faktiska material som har återförts.

> [!NOTE]
> Om någon rad i en leverantörsfaktura har en annan verifikationsstatus än **Slutförd** kan leverantörsfakturan inte bekräftas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
