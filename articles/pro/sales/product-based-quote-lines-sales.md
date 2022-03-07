---
title: Produktbaserade offertrader - lite
description: I det här ämnet finns information om att arbeta med projektbaserade offertrader.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994473"
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