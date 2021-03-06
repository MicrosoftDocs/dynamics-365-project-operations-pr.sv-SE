---
title: Stäng offerter
description: I det här ämnet finns information om hur du stänger en offert i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896213"
---
# <a name="close-quotes"></a>Stäng offerter 

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

En projektoffert kan stängas som Vunnen eller Förlorad. Åtgärderna för att aktivera och omarbeta offerter stöds inte i Microsoft Dynamics 365 Project Operations, så ett utkast till en offert kan stängas.

## <a name="close-a-quote-as-won"></a>Stänga en offert som Vunnen

Om du stänger en projektoffert som vunnen stängs offerten med status satt till Stängd och statusorsaken inställd på Vunnen. Om du stänger offerten blir projektofferten skrivskyddad och ett utkast skapas i ett projektkontrakt som innehåller offertinformationen. Eftersom det inte går att öppna en stängd offert igen visas en bekräftelsedialogruta innan ändringarna görs eftersom en stängd offert inte kan öppnas på nytt och ändringarna inte kan ångras.

Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Ekonomiska följder av att stänga en offert som Vunnen

Om det finns verkliga värden för tid som har registrerats i ett projekt men det fortfarande är kopplat till ett utkast till en offert, registreras endast kostnaden för tiden eller kostnaden. När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad. Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktsraden. Om de faktiska värdena för kostnad hänvisar till kontaktraden för tid och material, skapar systemet automatiskt motsvarande ofakturerade faktiska värden för försäljning när offerten stängs och projektkontraktet skapas. Om de faktiska värdena för kostnad hänvisar till en kontraktrad för fast pris, slutar programmet att behandla de faktiska värdena för kostnad baserat på reglerna för delad fakturering för projektkontraktets kunder.

## <a name="closing-a-quote-as-lost"></a>Stänga en offert som förlorad:

Om du stänger en projektoffert som Förlorad anges status till Stängd för statusorsak som Förlorad. Om du stänger offerten blir projektofferten skrivskyddad. Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.

Om projektofferten som stängs som Förlorad har ett projekt som refererar till någon av raderna visas även det projektet som Stängt och eventuella resursbokningar från den dagen framåt annulleras.

> [!NOTE]
> När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.
