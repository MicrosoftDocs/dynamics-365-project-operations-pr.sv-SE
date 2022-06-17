---
title: Produktbaserade offertrader - lite
description: Den här artikeln innehåller information om att arbeta med produktbaserade offertrader.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: db0700e789202a8fdd0ef3b49959421ac54fb9ad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914332"
---
# <a name="product-based-quote-lines-overview---lite"></a>Produktbaserade offertrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Du kan skapa produktbaserade offertrader i Dynamics 365 Project Operations. Produktbaserade offertrader kan läggas till manuellt eller vara artiklar från produktkatalogen.

## <a name="product-catalog"></a>Produktkatalog

Vara produkterna i en produktkatalog har en standardenhet och enhetsgrupp. Om flera produkter delar samma uppsättning attribut kan du skapa en produktfamilj som delar dessa attribut. 

Ett företag säljer till exempel prenumerationslicenser för olika sorters program. Alla prenumerationsprogram har följande två attribut:

- Antal användare
- Prenumerationens varaktighet i månader

För att upprätthålla den här typen av katalog är att skapa en produktfamilj som heter **prenumerationsprogram** och lägga till antalet användare och prenumerationens varaktighet som attribut. Härnäst kan du lägga till enskilda produkter i produktfamiljen **prenumerationsprogram**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Lägg till produktkatalogartiklar i en projektoffert

Sidorna **Projektofferter** och **projektkontrakt** har avsnitt för projektbaserade rader och produktbaserade rader. För produktbaserade rader inkluderar listrutan på offertraden eller projektkontraktraden innehåller alla produkter och enheter i produktprislistan. Du kan även lägga till produkter som inte ingår i produktprislista.

Dessutom kan du välja produkter från andra prislistor eller direkt från produktkatalogen. När du väljer produkter direkt från en produktkatalog används standardprislistan för produkten för att hämta produktens försäljningspris. Om ingen standardprislista har angetts sätts priset till (0).

När en offertrad bygger på en produktkatalog kan du åsidosätta försäljningspriset direkt på offertraden. En offertrad i fältet **prissättning** med två tillgängliga värden:

- **Åsidosätt prissättning**
- **Använd standard**

Om du väljer **Åsidosätt prissättning** är inte standardpriset angivet. Du måste istället ange ett pris för produkten på offertraden. Om du väljer **Använd standard** används standard försäljningspriset och fältet är låst för redigering.

Standardförsäljningspriser anges på de produktbaserade raderna i en offert. Fältet **Prissättning** anges sedan till **åsidosätta prissättning** så att du kan redigera standardpriset på offertraderna. Det här är en projektrelaterad åsidosättning av projekt för de produktbaserade radfunktionerna i Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]