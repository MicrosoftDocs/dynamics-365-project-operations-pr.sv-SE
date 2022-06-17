---
title: Konfigurera kostnads- och försäljningstaxa för material
description: Den här artikeln innehåller information om hur du anger kostnader och försäljningstaxor för material som används i projekt.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911802"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Konfigurera kostnads- och försäljningstaxa för material

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan ställa in kostnads- och försäljningspriser för produkter i Dynamics 365 Project Operations. Kostnads- och försäljningspriser för produkter kan endast visas i en valuta, vilket måste vara valutan i prislistehuvudet.

Gör så här om du vill ange kostnads- och försäljningstaxa för produkter: 

1. Gå till **Sales** > **Kunder** > **Prislistor** och välj **Ny** om du vill skapa en ny prislista. 
2. I **Prislisteobjekt** i underrutnätsmenyn, välj **Nytt prislisteobjekt**. 
3. På sidan **Snabbskapa** ange den produkt och enhet som du skapar det nya priset för.

Mer information om hur du definierar priser för katalogobjekt finns i [Definiera produktprissättning med prislistor och prislisteobjekt](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) samt [Decimalprecision i valuta och prissättning](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations stöder inte alla prissättningsmodeller för produkter såsom Dynamics 365 Sales. Den enda prissättningsmetod som stöds för produkter som ska användas i projekt är *Valutabelopp*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
