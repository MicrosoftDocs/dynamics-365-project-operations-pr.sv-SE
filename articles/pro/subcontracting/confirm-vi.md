---
title: Bekräfta en projektfaktura för leverantör
description: I detta ämne beskrivs hur du bekräftar en projektleverantörsfaktura i Microsoft Dynamics 365 Project Operations och den ekonomiska påverkan av att bekräfta en projektleverantörsfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595750"
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
