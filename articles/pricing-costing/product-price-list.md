---
title: Produktprislistor
description: I det här ämne finns information om prislistorna för katalogpriser som används för projektofferter och kontrakt.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593266"
---
# <a name="product-price-lists"></a>Produktprislistor

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

 I Project Operations, **Produktprislistor** och relaterad prislistepost stöder funktionen för prissättning av produkter på produktbaserade offert- och avtalsrader. För produkter som används i projekt används prislisteobjektposterna för projektprislistor. 

Produkterna bör konfigureras så att de har standardkostnads- och prislistor i produktkatalogen. Använda listpris, standardkostnad och aktuell kostnad om du vill konfigurera standardkostnad och listpriser. Standardprislista används endast på en offertrad eller i en projektkontraktrad om systemet inte kan hitta en prislisterad för produkten i produktprislistan för offert eller projektkontraktet.

Självkostnaden för produktkatalograder kan ändras mellan offerter. Det här är viktigt eftersom du inte behöver följa upp kostnaderna noggrant, men du kan inte ange driftsvinster för projektåtaganden. Som standard används produktens standardkostnad som självkostnad. Standardsjälvkostnaden kan emellertid uppdateras på offertraden om det finns ett annat självkostnadspris för offerten.

## <a name="price-list-items"></a>Prislisteposter

Du kan lägga till produkter från en produktkatalog i olika prislistor. Prislistrader för produkter refererar alltid till en specifik enhet. Priser för en produkt på prislisteposter kan konfigureras som ett valutabelopp. Du kan även konfigurera den som en funktion i listpris, aktuell kostnad eller standardkostnad.

Prisfunktioner stöder olika avrundningsalternativ när produktpriser konfigureras som en funktion i listpriset, standardkostnad eller aktuell kostnad. Förutom att använda flera prissättningsmetoder och avrundningsalternativ kan du associera rabattlistor med prislisteposter. 

 
## <a name="default-product-price-list"></a>Standardprislista för en produkt.
Varje kundpost har ett fält för **standardprislista** där du kan ange en prislista som överensstämmer med kundens valuta. Ett standardvärde anges inte automatiskt i det här fältet. När ett anpassat prissättningsavtal med en viss kund finns kan du använda det här fältet för att associera en prislista med den kunden.

Entiteterna affärsmöjlighet, offert och projektkontrakt använder följande ordning för att ange standardprislistor för produkter. Samma order används för prislistor för projekt.

1.  Offert
2.  Affärsmöjlighet
3.  Kund
4.  Globala inställningar 

Som standard listar fältet **produkt** på offertraden alla aktiva produkter i offertens produktprislista. Om en produkt har inaktiverats eller om det är en utkast produkt visas den inte, även om den är i prislistan. 

Produktkatalograder läggs till som fakturarader på den första fakturan som skapas för ett projektkontrakt. På en utkastfaktura kan dessa fakturarader tas bort. I så fall visas raderna på en efterföljande faktura tills de har fakturerats, eller tills fakturan skickas till kunden. Du kan inte fakturera en del av en produktfakturarad. När produktraderna från projektkontraktet faktureras skapas verkliga värden. De faktiska värdena länkas emellertid inte till den relaterade projektentiteten. Produkter som bygger på projektkontraktrader är med andra ord oberoende av projektbaserade användningstider. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
