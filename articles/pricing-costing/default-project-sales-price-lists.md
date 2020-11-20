---
title: Standardprislistor
description: I det här ämnet finns information om standardprislistor och prislistor för självkostnad i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085419"
---
# <a name="default-price-lists"></a>Standardprislistor

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

## <a name="sales-price-lists"></a>Försäljningsprislistor

Alla projektofferter och projektkontrakt i Dynamics 365 projekt Operations innehåller en standardprislista för försäljning. 

### <a name="price-list-default-on-project-quotes"></a>Standardprislista för projektofferter
Systemet slutför följande process för att avgöra vilken prislista som ska vara standard för en projektoffert:

1. Systemet söker efter prislistorna som är kopplade till kontots projektprislistor. 
2. Om det finns projektprislistor som är kopplade till kontoposten kontrollerar systemet de försäljningsprislistor som är kopplade till de projektparametrar som överensstämmer med projektoffertens valuta.
3. Därefter kontrollerar systemet giltighetsdatum för de prislistor som överensstämmer med datumintervallet för projektofferten. Mer bestämt det datum då offerten skapades.
4. Om det finns flera prislistor som är giltiga för projektoffertens datum används alla prislistor i enlighet med projektofferten.
5. Om det inte finns några prislistor som gäller datumen för projektofferten finns ingen standardprislista för projekt i projektofferten. Ett varningsmeddelande kommer att visas i projektofferten. Meddelandet anger att faktiska värden och uppskattningar i projektet inte kommer att prissättas eftersom det inte finns några projektprislistor bifogade.

### <a name="price-list-default-on-project-contracts"></a>Standardprislista för projektkontrakt 
Systemet slutför följande process för att avgöra vilken prislista som ska vara standard för ett projektkontrakt:

1. Om kontraktet skapas från en offert kopieras projektprislistorna i offerten separat och kopplas till projektkontraktet.
2. Om kontraktet skapas från grunden söker systemet igenom de prislistor som är kopplade till kontots projektprislistor. Om det inte finns projektprislistor som är kopplade till kontoposten kontrollerar systemet de försäljningsprislistor som är kopplade till de projektparametrar som överensstämmer med projektkontraktets valuta.
4. Därefter kontrollerar systemet giltighetsdatum för de prislistor som överensstämmer med datumintervallet för projektkontraktet. Mer bestämt det datum då kontraktet skapades.
5. Om det finns flera prislistor som är giltiga för kontraktets datum används alla prislistor i enlighet med kontraktet.
6. Om det inte finns några prislistor som gäller datumet för kontraktet används ingen projektprislista i enlighet med kontraktet. Ett varningsmeddelande kommer att visas i projektkontraktet. Meddelandet anger att faktiska värden och uppskattningar i projektet inte kommer att prissättas eftersom det inte finns några projektprislistor bifogade.

## <a name="cost-price-lists"></a>Prislistor för självkostnad

Prislistor för självkostnad hämtas inte från någon entitet i Project Operations. Det görs alltid en bestämning av vilken kostnadsprislista som ska användas för projektkostnader. Systemet slutför följande process för att avgöra vilken prislista som ska användas för projektkostnader:

1. Systemet söker först efter de prislistor som är kopplade till projektets kontrakterande organisationsenhet.
2. Systemet kontrollerar sedan giltighetsdatumet för prislistor som överensstämmer med datumet på raden för inkommande uppskattning eller faktiskt värde. I den här situationen refererar *uppskattningsraden* till alla tre sammanhang av uppskattning i Project Operations:

    - Projektuppskattningsrad
    - Information om offertrad
    - Kontraktradsinformation
  
3. Om det finns flera prislistor som är giltiga för datumet på den inkommande uppskattningen eller det faktiska värdet, väljs den prislista som skapades senast.
4. Om det inte finns projektprislistor som är kopplade till projektets kontrakterande organisationsenhet kontrollerar systemet de prislistor för självkostnad som är kopplade till de projektparametrar som överensstämmer med projektets valuta.
5. Därefter kontrollerar systemet giltighetsdatumet för prislistor som överensstämmer med datumet på raden för inkommande uppskattning eller faktiskt värde. 
6. Om det finns flera prislistor som är giltiga för datumet på den inkommande uppskattningen eller det faktiska värdet, väljs den prislista som skapades senast.
7. Om inga prislistor för självkostnad är kopplade till de projektparametrar som överensstämmer med valutan och giltighetsdatumet är standardvärdet för kostnadstaxan noll (0) på raden för inkommande uppskattning eller faktiskt värde.