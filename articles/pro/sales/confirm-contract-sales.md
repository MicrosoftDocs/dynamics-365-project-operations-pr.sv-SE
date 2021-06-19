---
title: Bekräfta ett projektkontrakt
description: I det här ämnet finns information om hur du bekräftar ett kontrakt i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003698"
---
# <a name="confirm-a-project-contract"></a>Bekräfta ett projektkontrakt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Ett projektkontrakt i Dynamics 365 Project Operations kan vara aktivt på grund av **Bekräftad** eller stängs med orsaken **Förlorad**. När du bekräftar ett projektkontrakt uppdateras statusen från **Utkast** till **Aktiv** och statusorsaken är **Bekräftat**. Ett aktivt eller stängt kontrakt kan inte redigeras eller öppnas på nytt. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Ekonomiska följder av att bekräfta ett projektkontrakt

När ett projektkontrakt bekräftas omberäknar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och skapa nya faktiska värden för kostnad. De nya faktiska värdena för kostnad behandlas sedan baserat på den faktureringsmetod som är kopplad till projektkontraktsraden. Om det faktiska värdet för kostnad refererar till en kontraktrad för tid och material återskapas automatiskt motsvarande ofakturerade faktiska värden för försäljning. Om det faktiska värdet för kostnad refererar till en kontraktrad för fast pris avbryter programmet ombearbetningen av de faktiska värdena för kostnad.

Gränser som inte får överskridas, konfiguration av debiterbarhet och prissättning och kostnader för de faktiska värdena utvärderas och uppdateras sedan som en del av bekräftelseprocessen.

## <a name="close-a-project-contract-as-lost"></a>Stänga ett projektkontrakt som förlorat

När du stänger ett projektkontrakt som förlorat uppdateras kontraktets status till **Stängt** och statusorsaken är **Förlorat**. Projektkontraktet blir skrivskyddat. En bekräftelsedialog visas innan ändringarna är slutförda eftersom du inte kan öppna ett stängt projektkontrakt igen.

Om projektkontraktet som stängs som förlorat refererar ett projekt på dess rader markeras det projektet som stängt. Eventuella resursbokningar från den dagen framåt annulleras. Eventuella ofakturerade faktiska värden för försäljning i projektkontraktet som inte redan finns på en faktura återförs.

> [!NOTE]
> I Dynamics 365 Project Operations om du stänger ett projektkontrakt som förlorat påverkar inte detta status för den associerade affärsmöjligheten. Affärsmöjligheten förblir öppen och måste stängas manuellt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]