---
title: Definiera projektkalendrar
description: I det här ämnet finns information om hur du använder en projektkalender för att följa upp projektschemat.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085714"
---
# <a name="define-project-calendars"></a>Definiera projektkalendrar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

För att skapa ett projektschema skapar du en projektkalendermall som definierar antalet arbetstimmar per dag och alla öppettider för företaget. Om du vill skapa en projektkalendermall associerar du en arbetsmall med fältet **kalendermallen** för projektet. Skapa en arbetsmall genom att följa stegen nedan.

1. I vänster navigeringsfönster, välj **Resurser**. 
2. På listsidan **Resurser** , öppna en användarpost och välj sedan **Visa arbetstimmar**.

  > [!NOTE]
  > Kontrollera att popup-fönster tillåts på webbsidan. På så sätt kan du se resursens arbetstider.
  
3. På sidan **månatlig visning** , klicka på **konfigurera**. En lista med tre alternativ visas: 

  - Nytt veckoschema
  - Arbetsschema för en dag
  - Ledig tid

4. Välj **Nytt veckoschema** och ange alternativen för det här resursschemat. Du kan ange ett återkommande veckoschema, dagliga timparametrar, företagets öppettider och mycket annat.
5. Ange datumintervall, välj **Spara** och klicka på **Stäng**. 
6. Gå tillbaka till listsidan **Resurser** och välj den resurs som du anger arbetstider för. 
7. Välj **Ange kalender som** för att ställa in arbetsmallen. 
8. I dialogrutan **Arbetsmall** anger du ett namn på arbetsmallen och klickar på **Använd**. 

Du kan nu associera arbetsmallen med en projektkalendermall.
