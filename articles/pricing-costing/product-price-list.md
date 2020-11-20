---
title: Produktprislistor
description: I det här ämne finns information om prislistorna för katalogpriser som används för projektofferter och kontrakt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 702402854c0787dae0bde854c9c274f5c23c131f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119620"
---
# <a name="product-price-lists"></a>Produktprislistor

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Entiteterna prislistor och prislistepost stöder produktkatalogspris. För det mesta används den här funktionen för katalogbaserade rader i projektofferter och projektkontrakt.

För projektbaserade rader representerar ett kontrakt avtalet efter det har vunnits. Eftersom förhandlingsprocessen vanligtvis föregår vinsten kopieras alltid den prissättning som är kopplad till offerten som den är till en ny prislista och bifogas kontraktet. Den nya prislistan kan inte ändras utanför kontraktets omfattning. Den här begränsningen bidrar till att skydda den prislista som förhandlades efter eventuella prisändringar som inträffar i huvudprislistan.

Produkterna bör konfigureras så att de har standardkostnads- och prislistor i produktkatalogen. Använda listpris, standardkostnad och aktuell kostnad om du vill konfigurera standardkostnad och listpriser. Standardprislista används endast på en offertrad eller i en projektkontraktrad om systemet inte kan hitta en prislisterad för produkten i produktprislistan för offert eller projektkontraktet.

Självkostnaden för produktkatalograder kan ändras mellan offerter. Det här är viktigt eftersom du inte behöver följa upp kostnaderna noggrant, men du kan inte ange driftsvinster för projektåtaganden. Som standard används produktens standardkostnad som självkostnad. Standardsjälvkostnaden kan emellertid uppdateras på offertraden om det finns ett annat självkostnadspris för offerten.

## <a name="price-list-items"></a>Prislisteposter

Du kan lägga till produkter från en produktkatalog i olika prislistor. Prislistrader för produkter refererar alltid till en specifik enhet. Priser för en produkt på prislisteposter kan konfigureras som ett valutabelopp. Du kan även konfigurera den som en funktion i listpris, aktuell kostnad eller standardkostnad.

PSA stöder olika avrundningsalternativ när priser konfigureras som en funktion i listpriset, standardkostnad eller aktuell kostnad. Förutom att använda flera prissättningsmetoder och avrundningsalternativ kan du associera rabattlistor med prislisteposter. 

När du skapar en ny anpassad prislista för en offert genom att **Skapa anpassad prissättning** på sidan **Projektoffert** skapas en kopia av prislistan och fältet **Entitet** i rubriken på den nya prislistan anges till **försäljningsentitet**. Namnet på den nya prislistan läggs till med namnet på offerten och tidstämpeln. Du kan även använda namnet på den nya prislistan och namnet på offerten i anpassade arbetsflöden om du vill utlösa ytterligare granskning och godkännanden för offerter som använder anpassad prissättning.

 
## <a name="default-product-price-list"></a>Standardprislista för en produkt.
Varje kundpost har ett fält för **standardprislista** där du kan ange en prislista som överensstämmer med kundens valuta. Ett standardvärde anges inte automatiskt i det här fältet. När ett anpassat prissättningsavtal med en viss kund finns kan du använda det här fältet för att associera en prislista med den kunden.

Entiteterna affärsmöjlighet, offert och projektkontrakt använder följande ordning för att ange standardprislistor för produkter. Samma order används för prislistor för projekt.

1.  Offert
2.  Affärsmöjlighet
3.  Kund
4.  Globala inställningar 

Som standard listar fältet **produkt** på offertraden alla aktiva produkter i offertens produktprislista. Om en produkt har inaktiverats eller om det är en utkast produkt visas den inte, även om den är i prislistan. 

Produktkatalograder läggs till som fakturarader på den första fakturan som skapas för ett projektkontrakt. På en utkastfaktura kan dessa fakturarader tas bort. I så fall visas raderna på en efterföljande faktura tills de har fakturerats, eller tills fakturan skickas till kunden. Du kan inte fakturera en del av en produktfakturarad. När produktraderna från projektkontraktet faktureras skapas verkliga värden. De faktiska värdena länkas emellertid inte till den relaterade projektentiteten. Produkter som bygger på projektkontraktrader är med andra ord oberoende av projektbaserade användningstider. Materialförbrukningen i projekt spåras inte.
