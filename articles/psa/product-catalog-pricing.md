---
title: Prissättning för produktkatalog
description: I det här ämnet finns information om hur produktkatalogspris fungerar i Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e6d9266cfee996b68608c99f77d1b0c053985b3d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085571"
---
# <a name="product-catalog-pricing"></a>Prissättning för produktkatalog 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Entiteterna prislistor och prislistepost stöder produktkatalogspris. För det mesta används den här funktionen för katalogbaserade rader i projektofferter och projektkontrakt.

För projektbaserade rader representerar ett kontrakt avtalet efter det har vunnits. Eftersom förhandlingsprocessen vanligtvis föregår vinsten kopieras alltid den prissättning som är kopplad till offerten som den är till en ny prislista och bifogas kontraktet. Den nya prislistan kan inte ändras utanför kontraktets omfattning. Den här begränsningen bidrar till att skydda den prislista som förhandlades efter eventuella prisändringar som inträffar i huvudprislistan.

Produkterna bör konfigureras så att de har standardkostnads- och prislistor i produktkatalogen. Du måste använda listpris, standardkostnad och aktuell kostnad om du vill konfigurera standardkostnad och listpriser. Standardprislista används endast på en offertrad eller i en projektkontraktrad om systemet inte kan hitta en prislisterad för produkten i produktprislistan för offert eller projektkontraktet.

Självkostnaden för produktkatalograder kan ändras mellan offerter. Det här är viktigt eftersom du inte behöver följa upp kostnaderna noggrant, men du kan inte ange driftsvinster för projektåtaganden. Som standard används produktens standardkostnad som självkostnad. Standardsjälvkostnaden kan emellertid uppdateras på offertraden om det finns ett annat självkostnadspris för offerten.

## <a name="price-list-items"></a>Prislisteposter

Du kan lägga till produkter från en produktkatalog i olika prislistor. Prislistrader för produkter refererar alltid till en specifik enhet. Priser för en produkt på prislisteposter kan konfigureras som ett valutabelopp. Du kan även konfigurera den som en funktion i listpris, aktuell kostnad eller standardkostnad.

PSA stöder olika avrundningsalternativ när priser konfigureras som en funktion i listpriset, standardkostnad eller aktuell kostnad. Förutom att använda flera prissättningsmetoder och avrundningsalternativ kan du associera rabattlistor med prislisteposter. 

> ![Du kan lägga till produkter från en katalog i olika prislistor](media/basic-guide-16.png)

När du skapar en ny anpassad prislista för en offert genom att **Skapa anpassad prissättning** på sidan **Projektoffert** skapas en kopia av prislistan och fältet **Entitet** i rubriken på den nya prislistan anges till **försäljningsentitet**. Namnet på den nya prislistan läggs till med namnet på offerten och tidstämpeln. Du kan även använda namnet på den nya prislistan och namnet på offerten i anpassade arbetsflöden om du vill utlösa ytterligare granskning och godkännanden för offerter som använder anpassad prissättning.

 
## <a name="default-product-price-list"></a>Standardprislista för en produkt.
Varje kundpost har ett fält för **standardprislista** där du kan ange en prislista som överensstämmer med kundens valuta. I PSA anges värdet inte automatiskt i det här fältet. När ett anpassat prissättningsavtal med en viss kund finns kan du använda det här fältet för att associera en prislista med den kunden.

Entiteterna affärsmöjlighet, offert och projektkontrakt använder följande ordning för att ange standardprislistor för produkter. Samma order används för prislistor för projekt.

1.  Offert
2.  Affärsmöjlighet
3.  Kund
4.  Globala inställningar för PSA

Som standard listar fältet **produkt** på offertraden alla aktiva produkter i offertens produktprislista. Om en produkt har inaktiverats eller om det är en utkast produkt visas den inte, även om den är i prislistan. 

Produktkatalograder läggs till som fakturarader på den första fakturan som skapas för ett projektkontrakt. På en utkastfaktura kan dessa fakturarader tas bort. I så fall visas raderna på en efterföljande faktura tills de har fakturerats, eller tills fakturan skickas till kunden. I PSA kan du inte fakturera en del av en produktfakturarad. När produktraderna från projektkontraktet faktureras skapas verkliga värden. De faktiska värdena länkas emellertid inte till den relaterade projektentiteten. Produkter som bygger på projektkontraktrader är med andra ord oberoende av projektbaserade användningstider. PSA spårar inte materialförbrukningen i projekt.