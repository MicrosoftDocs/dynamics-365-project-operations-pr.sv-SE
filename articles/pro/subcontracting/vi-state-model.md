---
title: Tillståndsövergångar i en leverantörsfaktura
description: Denna artikel förklarar tillståndsövergångarna på en leverantörsfaktura i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934342"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Tillståndsövergångar i en leverantörsfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Denna artikel förklarar tillståndsövergångarna på en leverantörsfaktura i Microsoft Dynamics 365 Project Operations. Följande tillstånd används: **Utkast**, **Granskas**, **Bekräftad**, **Pausad** samt **Annullerad**.

Illustrationen som följer visar dessa statusövergångar.

![Övergångsmodell för underleverantörstillstånd.](../media/VI_State_Model.jpg)

I följande tabell förklaras vad respektive tillstånd representerar i livscykeln för en leverantörsfaktura i Project Operations.

| State | Description | Tillåtna övergångar |
| --- | --- | --- |
| Utkast | Den här statusen är det ursprungliga tillståndet för en leverantörsfaktura. Raderna och prissättningen kan komma att ändras. En leverantörsfaktura med detta tillstånd kan redigeras och raderas. | Pågår |
| Granskning pågår | Detta tillstånd representerar behandlingsstatusen för en leverantörsfaktura. Minst en leverantörsfakturarad har verifieringsstatusen **Pågår**. | Bekräftad, Väntande |
| Bekräftat | Den här statusen representerar tillståndet för en leverantörsfaktura där programmet har skapat faktiska kostnader för respektive leverantörsfakturarad. Eventuella länkade faktiska kostnader som matchats med leverantörsfakturaraderna har återförts och ersatts med de faktiska kostnaderna från dessa leverantörsfakturarader. Det går inte att redigera eller radera en leverantörsfaktura med detta tillstånd. Med knappen **Avbryt** kan du annullera en bekräftad leverantörsfaktura. Åtgärden Avbryt upphäver effekten av åtgärden Bekräfta. | Avbruten |
| Väntande | <p>Den här statusen representerar ett steg i en leverantörsfaktura där leverantörsfakturan inte kan flyttas på grund av ett problem med fakturan eller leverantörens status. En leverantörsfaktura med detta tillstånd kan inte bekräftas, annulleras, redigeras eller tas bort.</p><p>Du kan använda åtgärden Öppna igen om du vill flytta leverantörsfakturan till tillståndet **Utkast** eller **Granskas**. Om minst en rad på leverantörsfakturan har verifieringsstatusen **Pågående** eller **Slutförd** öppnas leverantörsfakturan på nytt i tillståndet **Granskas**. Om alla rader i leverantörsfakturan har verifieringsstatusen **Ej startad** öppnas leverantörsfakturan på nytt med tillståndet **Utkast**.</p> | Utkast, Granskas |
| Avbruten | Detta tillstånd representerar tillståndet för en underleverantör där faktisk leverans av material och/eller arbete av underleverantörer inte längre krävs. En underleverantör i det här tillståndet kan inte användas för att beräkna och bemanna projektkrav för resurser och material, och kan heller inte hänvisas till tids-, utgifts- och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
