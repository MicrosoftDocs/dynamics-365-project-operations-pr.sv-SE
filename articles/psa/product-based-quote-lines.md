---
title: Produktbaserade offertrader
description: I det här ämnet finns information om produktbaserade offertrader.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151275"
---
# <a name="product-based-quote-lines"></a>Produktbaserade offertrader

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Du kan skapa produktbaserade offertrader i Dynamics 365 Project Service Automation. Produktbaserade offertrader kan vara "skriva in" eller vara artiklar från produktkatalogen.

## <a name="product-catalog"></a>Produktkatalog

Produkterna i en Dynamics 365-produktkatalog har en standardenhet och enhetsgrupp. Om flera produkter delar samma uppsättning attribut kan du skapa en produktfamilj som även har dessa attribut. Alla produkter i samma produktfamilj ärver samma uppsättning attribut.

Ett företag säljer till exempel prenumerationslicenser för en mängd olika program. Alla prenumerationsprogram har följande två attribut:

- Antal användare 
- Prenumerationens varaktighet (i månader)

Ett bra sätt att upprätthålla den här typen av katalog är att skapa en produktfamilj som heter **prenumerationsprogram** och som har **antal användare** och **prenumerationens varaktighet** som attribut. Du kan sedan lägga till enskilda produkter, till **Dynamics 365 Sales** eller **Dynamics 365 Field Service** till produktfamiljen **prenumerationsprogram**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Lägga till produktkatalogartiklar i en projektoffert

Projektofferter och projektkontraktsidor har avsnitt för två typer av rader: projektbaserade rader och produktbaserade rader. För produktbaserade rader används Dynamics 365 för att lägga till objekt från en produktkatalog i en offert. Listrutan på offertraden eller projektkontraktraden innehåller alla produkter och enheter i produktprislistan som är kopplade till offerten eller projektkontraktet. Du kan även lägga till produkter som inte ingår i offertens produktprislista.

Dessutom kan du välja produkter från andra prislistor eller välja produkter direkt från produktkatalogen. När du väljer produkter direkt från en produktkatalog används standardprislistan för produkten för att hämta produktens försäljningspris. Om ingen standardprislista har angetts sätts priset till 0 (noll).

Om en offertrad bygger på en produktkatalog kan du åsidosätta försäljningspriset direkt på offertraden. Observera att en offertrad i fältet Dynamics 365 har fältet **prissättning**. Två värden är tillgängliga:

- Åsidosätt prissättning  
- Använd standard

Om du anger det här fältet till **Åsidosätt prissättning** anger Dynamics 365 inte något standardpris. Du måste ange ett pris för produkten på offertraden. Om du anger det här fältet till **använd standard** använder Dynamics 365 standardförsäljningspriset och låser fältet för att förhindra redigering.

När du har installerat PSA anges standardförsäljningspriserna på de produktbaserade raderna i en offert. Fältet **Prissättning** anges sedan till **åsidosätta prissättning** så att du kan redigera standardpriset på offertraderna.

> ![Ställa in åsidosätta prissättning](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Kvantitetsfaktorer för produkter

I PSA används kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter. För prenumerationsbaserade produkter uttrycks kvantitet på offert- eller projektkontraktraden som antalet användarmånader.

Vanligt vis lagras priset på prenumerationsprogram i katalogen som priset per användare i månaden. Du kan emellertid använda andra tidsbeskrivningar i stället. Under försäljningsprocessen är priset på offertraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av IT-säljaren. Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader. Den kvantitet som används för att beräkna beloppet på offertraden är en produkt av antalet användare och antalet prenumerationsmånader.

För att kunna stödja den här typen av försäljning introducerade PSA begreppet kvantitetsfaktorer. För kvantitetskategorin förlitar sig sig på produktattribut i Dynamics 365. När du konfigurerar specifika egenskaper för en produkt kan du använda PSA för att flagga en del uppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.

PSA verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer. När en produkt som du har konfigurerat kvantitetsfaktorer för läggs till på en offertrad blir fältet **kvantitet** på offertraden skrivskyddat. När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknar PSA kvantiteten på offertraden.

Dynamics 365 kan till exempel ha följande egenskaper: 

- **Antal användare** - antalet användare 
- **Antal månader** - antalet prenumerationsmånader
- **Produkt-SKU** 

Egenskaperna **Antal användare** och **Antal för månader** kan flaggas som kvantitetsrapporter genom att egenskaperna för produktraden redigeras. 

> ![Flaggantalet användare och inga månader som kvalitetsfaktorer](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]