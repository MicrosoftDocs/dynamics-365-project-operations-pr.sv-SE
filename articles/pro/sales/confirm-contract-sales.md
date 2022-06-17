---
title: Bekräfta ett projektkontrakt
description: Den här artikeln innehåller information om hur du bekräftar avtal i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930018"
---
# <a name="confirm-a-project-contract"></a>Bekräfta ett projektkontrakt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

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