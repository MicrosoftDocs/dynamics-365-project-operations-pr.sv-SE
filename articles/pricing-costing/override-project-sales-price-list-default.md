---
title: Åsidosätt projektförsäljningsprislistor
description: I det här ämnet finns information om hur du skapar anpassade försäljningsprislistor.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275560"
---
# <a name="override-project-sales-price-lists"></a>Åsidosätt projektförsäljningsprislistor

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

## <a name="customer-specific-project-price-lists"></a>Kundspecifika projektprislistor

Kundspecifika prisavtal kan anges som projektprislistor för en kontopost i Dynamics 365 Project Operations.

Om du vill skapa en kundspecifik projektprislista i området **försäljning** navigerar du till kontoposten.

1. Öppna listsidan **Konton**.
2. Leta upp och dubbelklicka på en kundpost om du vill öppna informationssidan **konto**.
3. I fliken **Projektprislistor** väljer du **+ Ny projektprislista**.
4. På sidan **Ny projektprislista** väljer du en prislista i listrutan. Endast prislistor som har kontexten inställd på **försäljning** och vars valuta överensstämmer med kontovalutan.
5. Namnge associationen och välj **Spara**. En kundspecifik projektprislista skapas. Den här prislistan används som standard för projektkostnader i projektofferter eller kontrakt som skapats för den här kunden när offertens eller projektkontraktets slutdatum faller inom giltighetsdatum för prislistan.

## <a name="custom-pricing-on-project-quotes"></a>Anpassad prissättning på projektofferter

På projektofferter kan du ange att projektprissättningen ska börja med en standard prislista som hämtas som standard från kunden eller från projektets parametrar.

När du behöver anpassa prissättningen av projekt som hör ihop med en viss offert kan du Visa den från den associerade entiteten projektprislistor.

Följ stegen nedan om du vill skapa ett specifikt offererat projektpris.

1. Öppna projektoffert, välj fliken **Projektprislistor**.
2. I underrutnätet väljer du **Skapa anpassad prissättning**.

Alla projektprislistor som är bifogade till offerten kopieras till nya prislistor. Namnen på de nya prislistorna återspeglar namnet på offerten med en datum- och tidsstämpling för när prislistorna skapades.

Du kan använda var och en av dessa prislistor och göra uppdateringar av arbete (rollpris) och kostnader för utgift (kategoripris). Dessa priser gäller endast för detta projektoffert.

## <a name="price-lists-on-a-project-contract"></a>Prislistor för projektkontrakt

I ett projektkontrakt är projektpriset alltid standard som en anpassad prislista med namnet på kontraktet och datum-tidsstämpeln som läggs till i namnet. Detta gäller oavsett om kontraktet skapades när offerten vanns eller om kontraktet skapades från grunden. Om det behövs kan du ta bort kopplingen till den anpassade prislistan och associera en standardprislista till projektkontraktet i stället.

När du associerar en standardprislista med projektprislistorna för en offert eller ett kontrakt påverkas alla eventuella ändringar av priserna i prislistan för alla offerter och kontrakt som använder prislistan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]