---
title: Annullera en projektleverantörsfaktura
description: I den här artikeln beskrivs hur du annullerar en projektleverantörsfaktura i Microsoft Dynamics 365 Project Operations och den ekonomiska påverkan av att annullera en projektleverantörsfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261113"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annullera en projektleverantörsfaktura

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
