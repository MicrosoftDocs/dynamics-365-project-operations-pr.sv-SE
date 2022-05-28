---
title: Affärstransaktioner i Project Operations
description: Detta ämne ger en översikt över konceptet med affärstransaktioner i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582226"
---
# <a name="business-transactions-in-project-operations"></a>Affärstransaktioner i Project Operations

_**Gäller till:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I Microsoft Dynamics 365 Project Operations är *affärstransaktion* ett abstrakt koncept som inte representeras av någon entitet. Vissa vanliga fält och processer i entiteter är dock utformade för att använda begreppet affärstransaktioner. Följande entiteter använder denna abstraktion:

- Information om offertrad
- Information om kontraktrad
- Beräkningsrader
- Journalrader
- Faktiska värden

Av dessa entiteter mappas Information om offertrad, Information om kontraktrad och Beräkningsrader till *beräkningsfasen* i projektlivscykeln. Entiteterna Journalrader och Faktiska värden mappas till *körningsfasen* i projektlivscykeln.

Project Operations behandlar poster i samtliga dessa fem entiteter som affärstransaktioner. Den enda skillnaden är att poster i de entiteter som är mappade till beräkningsfasen (Information om offertader, Information om kontraktsrad samt Beräkningsrader) betraktas som *ekonomiska prognoser*, medan poster i de entiteter som är mappade till körningsfasen (journalsrader och faktiska värden) betraktas som *ekonomiska fakta* som redan har inträffat.

Mer information finns i [Beräkningar](../project-management/estimating-projects-overview.md) och [faktiska värden](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncept som är unika för affärstransaktioner

Följande koncept är unika för begreppet affärstransaktioner:

- Transaktionstyp
- Transaktionsklass
- Transaktionens ursprung
- Transaktionskoppling

### <a name="transaction-type"></a>Transaktionstyp

Transaktionstyp representerar tidpunkten för och sammanhanget mellan de ekonomiska konsekvenserna för ett projekt. Den representeras av ett alternativuppsättning som har följande värden som stöds i Project Operations:

- Kostnad
- Projektkontrakt
- Ofakturerad försäljning
- Fakturerad försäljning
- Försäljning inom organisationen
- Kostnad för resursenhet

### <a name="transaction-class"></a>Transaktionsklass

Transaktionsklass representerar de olika typer av kostnader som uppstår i projekt. Den representeras av ett alternativuppsättning som har följande värden som stöds i Project Operations:

- Tid
- Utgift
- Material
- Avgift
- Milstolpe
- Skatt

> [!NOTE]
> Värdet **milstolpe** används vanligtvis av affärslogiken för fakturering med fast pris i Project Operations.

### <a name="transaction-origin"></a>Transaktionens ursprung

Transaktionens ursprung är en entitet som lagrar ursprunget för varje affärstransaktion för att underlätta rapportering och spårning. När projektkörningen börjar skapar varje affärstransaktion en ytterligare affärstransaktion som i sin tur skapar ytterligare en affärstransaktion, och så vidare.

### <a name="transaction-connection"></a>Transaktionskoppling

Transaktionskoppling är en entitet som lagrar relationen mellan två liknande affärstransaktioner, t.ex. kostnad och relaterade verkliga försäljningar, eller transaktionsåterföringar som startas av faktureringsaktiviteter såsom fakturabekräftelse eller fakturakorrigeringar.

Tillsammans kan du med hjälp av transaktionsursprunget och entiteterna för transaktionskoppling spåra relationer mellan affärstransaktioner och åtgärder som orsakat att en specifik affärstransaktion skapats.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
