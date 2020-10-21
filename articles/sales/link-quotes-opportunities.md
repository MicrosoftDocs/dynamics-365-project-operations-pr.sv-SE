---
title: Skapa projektofferter från affärsmöjligheter
description: I det här ämnet finns information om hur man skapar en projektoffert från en affärsmöjlighet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898554"
---
# <a name="create-project-quotes-from-opportunities"></a>Skapa projektofferter från affärsmöjligheter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan skapa offerter utifrån projektmöjligheter på följande sätt:

- Från fliken **Offerter** på sidan **Projektmöjlighet**
- Från affärsmöjlighetens försäljningsflöde
- Genom att uppdatera affärsmöjlighetsreferensen på en befintlig offert

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Från fliken Offerter på sidan Projektmöjlighet

Följ stegen nedan om du vill skapa en projektoffert från en affärsmöjlighet.

1. Öppna sidan **Projektmöjlighet** och välj fliken **Offerter**. 
2. I underrutnätet **Offerter** väljer du **+** för att skapa en ny projektoffert baserad på affärsmöjligheten. Alla affärsmöjlighetsrader och relaterade projektprislistor kopieras till den nya offerten från affärsmöjligheten.

## <a name="from-the-opportunity-sales-process-flow"></a>Från affärsmöjlighetens försäljningsflöde

Följ stegen nedan om du vill skapa en offert från affärsmöjlighetens försäljningsflöde.

1. Öppna affärsmöjligheten i försäljningsflödet för affärsmöjligheten.
2. Välj steget **Kvalificera**. 
3. Välj **Nästa** och välj sedan **+ Skapa** för att skapa en ny offert. Merparten av informationen under fliken **Sammanfattning** för den här nya offerten visas som standard från affärsmöjligheten. 
4. Ange eventuell information som saknas eller uppdatera standardvärden efter behov på fliken **Sammanfattning**.
5. Välj **Spara**. Den nya offerten skapas och associeras med affärsmöjligheten. Du kan nu visa offertinformationen under fliken **Offerter** på sidan **Affärsmöjlighet**. 

   Försäljningsprocessen för affärsmöjligheten flyttas till nästa stadium **Föreslå**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Genom att uppdatera affärsmöjlighetsreferensen på en befintlig offert

En befintlig offert kan länkas till en affärsmöjlighet. Följ stegen nedan om du vill uppdatera affärsmöjlighetsinformationen för en befintlig offert.

1. Öppna sidan **Offert** och välj fliken **Sammanfattning**.
2. I fälet **Affärsmöjlighet** väjer du den affärsmöjlighet som du vill koppla till offerten. Du kan se offerten i rutnätet **Offerter** i affärsmöjligheten. 
3. Med hjälp affärsmöjlighetens försäljningsprocess kan affärsmöjligheten flyttas till nästa stadium, **Föreslå**. 

   När du flyttar en affärsmöjlighet till detta stadium kan du välja den här offerten från en lista med offerter som är associerade med den här affärsmöjligheten. Om du väljer den här offerten betyder det att du går vidare med den.

   Alla andra offerter som är associerade med affärsmöjligheten är fortfarande tillgängliga och aktiva tills en av dem har vunnits. Du kan flytta tillbaka försäljningsprocessen till föregående stadium **Kvalificera** och välja en annan offert att gå vidare med.
