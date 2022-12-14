---
title: Stäng projektofferter
description: Den här artikeln innehåller information om att stänga en offert i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826198"
---
# <a name="close-project-quotes"></a>Stäng projektofferter

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En projektoffert kan stängas som Vunnen eller Förlorad. Ett offertutkast kan komma att stängas eftersom aktiverings- och ändringsåtgärder för offerter inte stöds i Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Stänga en offert som Vunnen

När du stänger en projektoffert som "Vunnen" får den statusen "Stängd" och statusorsaken "Vunnen". Om du stänger offerten blir projektofferten skrivskyddad och ett utkast skapas i ett projektkontrakt som innehåller offertinformationen. Eftersom en stängd offert inte kan öppnas på nytt kommer en bekräftelsedialog att bekräfta dina ändringar.

Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Ekonomiska följder av att stänga en offert som Vunnen

Om några faktiska värden för tid i ett projekt fortfarande är kopplade till ett offertutkast, registreras endast kostnaden för tid eller utgifter. När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad. Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktraden. Om kostnadens faktiska värden refererar till en tids- och materialkontraktrad, skapas motsvarande icke-fakturerade försäljningsfakturerade faktiska värden när offerten stängs och projektkontraktet skapas. Om de faktiska kostnaderna refererar till en kontraktrad med fast pris, kommer programmet att sluta bearbeta om de faktiska kostnader som bygger på delningsfaktureringsregler för projektkontraktskunderna.

## <a name="closing-a-quote-as-lost"></a>Stänga en offert som förlorad

När du stänger en projektoffert som "Förlorad" får den statusen "Stängd" och statusorsaken "Förlorad". Om du stänger offerten blir projektofferten skrivskyddad. Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.

Om projektofferten som har stängts som Förlorad refererar till ett projekt på någon av raderna markeras det också som Stängt. Eventuella resursbokningar från den dagen framåt annulleras.

> [!NOTE]
> När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
