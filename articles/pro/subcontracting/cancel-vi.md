---
title: Annullera en projektleverantörsfaktura
description: I detta ämne beskrivs hur du annullerar en projektleverantörsfaktura i Microsoft Dynamics 365 Project Operations och den ekonomiska påverkan av att annullera en projektleverantörsfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580662"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annullera en projektleverantörsfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

När du har bekräftat en leverantörsfaktura går det inte att redigera eller ta bort den. Om ett fel inträffade i en leverantörsfaktura som bekräftades kan du använda åtgärden Avbryt för att återställa påverkan på leverantörsfakturan och skapa en ny leverantörsfaktura.

När du väljer **Avbryt** på en leverantörsfaktura sker följande:

1. Leverantörsfakturans tillstånd uppdateras till **Annullerad**.
2. Den annullerade leverantörsfakturan och dess relaterade poster blir skrivskyddade och kan inte redigeras eller tas bort.
3. Eventuella faktiska kostnader som skapats baserat på leverantörsfakturarader som en del av bekräftelsen på leverantörsfakturan återförs.
4. Om några faktiska kostnader kopplades till leverantörsfakturaraderna som en del av matchningsprocessen, återfördes dessa av den ursprungliga leverantörens fakturabekräftelse. När leverantörens faktura annulleras skapas de faktiska kostnaderna på nytt. Ursprunget pekar på tids-, utgifts- eller materialanvändningsposter.
5. När leverantörsfakturan annulleras kan du åter skapa korrigeringsjournaler, behandla återkallning av tidsposter samt annullera godkännande av ursprunglig tiden, utgift eller faktiskt material.

> [!NOTE]
> Endast bekräftade leverantörsfakturor kan annulleras. Leverantörsfakturor med annan status kan inte annulleras.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
