---
title: Stäng en offert
description: I det här ämnet finns information om hur du stänger offerter i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993443"
---
# <a name="close-a-quote"></a>Stäng en offert

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En projektoffert kan stängas som Vunnen eller Förlorad. Eftersom funktionerna Aktivera och revidera inte stöds av offerter i Microsoft Dynamics 365 Project Operations, kan du stänga en utkastoffert.

## <a name="close-a-quote-as-won"></a>Stänga en offert som Vunnen

Om du stänger en projektoffert som Vunnen anges statusen för offerten till **Stängd** och statusorsaken till **Vunnen**. Om du stänger offerter blir de skrivskyddade och ett utkast skapas i ett projektkontrakt med all offertinformationen. Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.

Projektkontraktet som skapas från en projektoffert görs också tillgängligt i projektlednings- och redovisningsmodulen i Project Operations. Om ett projektkontrakt inte är mappat till ett projekt på någon av raderna blir det här projektkontraktet tillgängligt som ett inaktivt projektkontrakt och aktiveras så fort ett projekt har mappats till minst en av kontraktraderna.

Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Ekonomiska följder av att stänga en offert som Vunnen

Om det finns verkliga värden för tid som har registrerats i ett projekt men det fortfarande är kopplat till ett utkast till en offert, registreras endast kostnaden för tiden eller kostnaden. När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad. Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktraden. Om de faktiska värdena för kostnad hänvisar till kontaktraden för tid och material, skapar systemet automatiskt motsvarande ofakturerade faktiska värden för försäljning när offerten stängs och projektkontraktet skapas. Om de faktiska värdena för kostnad hänvisar till en kontraktrad för fast pris, slutar programmet att behandla de faktiska värdena för kostnad baserat på reglerna för delad fakturering för projektkontraktets kunder.

Alla ombearbetade verkliga värden finns i modulen Projektledning och redovisning för projektrevisorn att granska, uppdatera och bokföra i huvudboken. 

## <a name="close-a-quote-as-lost"></a>Stänga en offert som Förlorad

Om du stänger en projektoffert som Förlorad anges status till **Stängd** och statusorsak som **Förlorad**. Om du stänger offerten blir den skrivskyddad. Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.

Om projektofferten som stängs som Förlorad har ett projekt som refererar till någon av raderna visas även det projektet som Stängt och eventuella resursbokningar från den dagen framåt annulleras.

> [!NOTE]
> När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]