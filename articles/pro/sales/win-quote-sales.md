---
title: Stänga en offert - lite
description: I det här ämnet finns information om hur du stänger en offert i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764886"
---
# <a name="close-a-quote---lite"></a>Stänga en offert - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En projektoffert kan stängas som Vunnen eller Förlorad. Ett offertutkast kan komma att stängas eftersom aktiverings- och ändringsåtgärder för offerter inte stöds i Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Stänga en offert som Vunnen

När du stänger en projektoffert som "Vunnen" får den statusen "Stängd" och statusorsaken "Vunnen". Om du stänger offerten blir projektofferten skrivskyddad och ett utkast skapas i ett projektkontrakt som innehåller offertinformationen. Eftersom en stängd offert inte kan öppnas på nytt kommer en bekräftelsedialog att bekräfta dina ändringar.

Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Ekonomiska följder av att stänga en offert som Vunnen

Om några faktiska värden för tid i ett projekt fortfarande är kopplade till ett offertutkast, registreras endast kostnaden för tid eller utgifter. När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad. Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktraden. Om kostnadens faktiska värden refererar till en tids- och materialkontraktrad, skapas motsvarande icke-fakturerade försäljningsfakturerade faktiska värden när offerten stängs och projektkontraktet skapas. Om de faktiska kostnaderna refererar till en kontraktrad med fast pris, kommer programmet att sluta bearbeta om de faktiska kostnader som bygger på delningsfaktureringsregler för projektkontraktskunderna.

## <a name="closing-a-quote-as-lost"></a>Stänga en offert som förlorad:

När du stänger en projektoffert som "Förlorad" får den statusen "Stängd" och statusorsaken "Förlorad". Om du stänger offerten blir projektofferten skrivskyddad. Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.

Om projektofferten som har stängts som Förlorad refererar till ett projekt på någon av raderna markeras det också som Stängt. Eventuella resursbokningar från den dagen framåt annulleras.

> [!NOTE]
> När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]