---
title: Inaktivera prislistor
description: Här ämne hur du inaktiverar eller tar bort oanvända eller gamla prislistor.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001358"
---
# <a name="deactivate-price-lists"></a>Inaktivera prislistor 

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du måste slutföra två steg om du vill ta bort Dynamics 365 Project Operations gamla eller oanvända prislistor. 

1. Ta bort eller radera prislistan från specifika sidor.
2. Inaktivera eller ta bort prislistan från aktiva prislistor på sidan **Prislistor**.

>[!IMPORTANT]
> Du måste slutföra båda stegen för att helt ta bort en prislista. Det räcker inte att utföra steg 2, som är att direkt ta bort eller inaktivera prislistan från vyn Aktiva prislistor. Du måste också ta bort prislistans association från alla platser som anges i steg 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Ta bort prislistan från specifika sidor
1. Om du vill ta bort en prislista från Project Operations går du till följande sidor:  

      - Sidan **Projektparameter** > fliken **Prislistor**
      - Sidan **Organisationsenhet** > rutnätet **Prislistor**
      - Sidan **Konto** > rutnätet **Projektprislistor**
      - Sidan **Projektofferter** > rutnätet **Projektprislistor**: Detta gäller för alla aktiva projektofferter.
      - Sidan **Projektkontrakt** > rutnätet **Projektprislistor**: Detta gäller för alla aktiva projektkontrakt.

 2. För varje sida måste du markera den prislista du vill ta bort och sedan välja **Ta bort**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Ta bort eller inaktivera prislistan från sidan Prislistor
 
1. Om du vill ta bort en prislista från de aktiva prislistorna går du **Försäljning** > **Kunder** > **Prislistor**. 
2. Välj den prislista som du vill ta bort och tryck sedan på **Ta bort**. Om prislistan refereras till befintliga transaktioner går det inte att ta bort den. Om det händer kan du inaktivera prislistan så att den inte visas i några vyer. 
3. Om du vill inaktivera prislistan markerar du prislistan igen och väljer sedan **Inaktivera**.   
