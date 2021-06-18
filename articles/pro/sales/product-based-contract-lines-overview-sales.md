---
title: Produktbaserade kontraktrader - lite
description: I det här ämnet finns information om produktbaserade kontraktrader.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994563"
---
# <a name="product-based-contract-lines-overview---lite"></a>Produktbaserade kontraktrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Du kan skapa produktbaserade kontraktrader i Dynamics 365 Project Operations. Produktbaserade kontraktrader kan vara manuellt skapade rader eller vara artiklar från produktkatalogen.

## <a name="product-catalog"></a>Produktkatalog

Produkterna i produktkatalogen har en standardenhet och enhetsgrupp. Om flera produkter delar samma uppsättning attribut kan du skapa en produktfamilj som även har dessa attribut. Alla produkter i samma produktfamilj ärver samma uppsättning attribut.

Ett företag säljer till exempel prenumerationslicenser för olika sorters program. Alla prenumerationsprogram har följande två attribut:

- Antal användare
- Prenumerationens varaktighet (i månader)

Om du vill behålla den här typen av katalog skapar du en produktfamilj som heter **Prenumerationsprogramvara**. Lägg till attributen **Antal användare** och **Prenumerationens varaktighet** i produktfamiljen. Lägg sedan till enskilda produkter i produktfamiljen **Prenumerationsprogram**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Lägga till produktkatalogartiklar i ett projektkontrakt

Projektkontrakt har avsnitt för två typer av rader: projektbaserade och produktbaserade. Produktbaserade rader innehåller alla produkter och enheter i produktprislistan i kontraktet. Produkter som inte ingår i kontraktets produktprislista kan läggas till.

Du kan välja produkter från andra prislistor eller direkt från produktkatalogen. När du väljer produkter direkt från en produktkatalog används standardprislistan för produkten för produktens försäljningspris. Om ingen standardprislista har angetts sätts priset till 0 (noll).

Om en kontraktrad bygger på en produktkatalog kan du åsidosätta försäljningspriset direkt på raden. En kontraktrad har fältet **Prissättning** med de två värdena:

- **Åsidosätt prissättning**
- **Använd standard**

Om du här fältet **Prissättning** till **Åsidosätt prissättning** ställs inget standardpris in. Ange ett pris för produkten på kontraktraden. Om du ställer in fältet på **Använd standard** används standardförsäljningspriset och fältet kan inte redigeras.

När du har installerat Project Operations anges standardförsäljningspriserna på de produktbaserade raderna i ett kontrakt. Fältet **Prissättning** anges till **Åsidosätt prissättning** så att du kan redigera standardpriset på kontraktraderna. Det här är en Project Operations-specifik åsidosättning av beteendet hos projektbaserade rader i Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]