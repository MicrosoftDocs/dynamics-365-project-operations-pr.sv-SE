---
title: Bekräfta en projektfaktura för leverantör
description: I denna artikel beskrivs hur du bekräftar en projektleverantörsfaktura i Microsoft Dynamics 365 Project Operations och den ekonomiska påverkan av att bekräfta en projektleverantörsfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261535"
---
# <a name="confirm-a-project-vendor-invoice"></a>Bekräfta en projektfaktura för leverantör

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
