---
title: Huvudbegrepp vid underleverantörskap
description: I ämnet förklaras några viktiga begrepp som används vid underleverantörskap i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994298"
---
# <a name="key-concepts-in-subcontracting"></a>Huvudbegrepp vid underleverantörskap

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I ämnet finns några viktiga begrepp som du bör känna till innan du börjar använda underleverantörsfunktionen i Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Kontrakteringsenhet för underleverantör

Kontrakteringsenheten representerar den avdelning eller praktik som äger leveranserna av det slutliga projektet. Kontrakteringsenheten är också den avdelning som ingår i kontraktrelationen med leverantören.

## <a name="purchase-currency"></a>Inköpsvaluta

I Project Operations är inköpsvalutan den valuta som underkontraktet skapas i. Det är också valutan som underleverantörers kostnader för ett projekt registreras i. Inköpsvalutan kan skilja sig från projektvalutan och projektvalutan kan i sin tur skilja sig från försäljningsvalutan.

## <a name="billing-methods-on-subcontract-lines"></a>Faktureringsmetoder på underleverantörsrader

För projekt finns det vanligtvis en kontraktsmodell med fast kostnad och en förbrukningsbaserad modell. Project Operations stöder dessa faktureringsmetoder i försäljnings- och köpkontexterna. Faktureringsmetoderna för ett köp fungerar på följande sätt:

- **Tid och material** – När en underavtalsrad använder faktureringsmetoden **Tid och material** registreras tidskostnaden i projektet som underleverantörers arbete i det projektet och posttiden. Dessa kostnadstransaktioner från underleverantörer matchas sedan med radobjekten på leverantörsfakturor. I den här modellen kan projektledare som använder Project Operations matcha och verifiera leverantörsfakturarader med den underleverantörstid som har registrerats och godkänts. När verifieringen är klar kommer tidigare faktiska kostnader som registrerats efter godkännande att återställas och nya faktiska kostnader som bygger på leverantörsfakturan skapas i projektet.
- **Fast pris** – I den här kontraktsmodellen med fast avgifter baseras leverantörsfakturor på fasta milstolpar. Men underleverantörers resurser kan också rapportera tid. Tiden granskas och godkänns sedan av projektledaren. När den har godkänts skapar Project Operations tillfälliga faktiska kostnader i projektet. När leverantören skickar en faktura för en milstolpe kan projektledaren matcha tidigare registrerade faktiska kostnader mot milstolpen. När verifieringen är klar kommer de faktiska kostnaderna att återföras och den milstolpebaserade kostnaden registreras.

## <a name="project-price-lists-on-subcontracts"></a>Projektprislistor för underkontrakt

Projektprislistor är prislistor som används för att ange inköpspriser för tid, utgifter och andra projektrelaterade komponenter. Det kan finnas flera prislistor som alla kan ha ett underavtal med egen giltighetstid i Project Operations. Project Operations stöder inte överlappande giltighetsdatum i projektprislistor för ett underavtal.

## <a name="transaction-classes-on-subcontracts"></a>Transaktionsklasser för underavtal

Project Operations har stöd för fyra typer av transaktionsklasser:

- Tid
- Utgift
- Material
- Avgift

Inköpskostnader kan endast beräknas och uppstå för transaktionsklasserna **Tid**, **Utgift** och **Material**. **Avgift** är en transaktionsklass endast för intäkter och är inte tillgänglig när det gäller inköp.

## <a name="purchase-pricing-dimensions"></a>Prissättningsdimensioner för inköp

Prissättningsdimensioner låter dig bestämma vilka attribut som ska användas för konfiguration av inköpspris och standardvärden för tidstransaktioner. När det gäller inköp stöder Project Operations endast fasta dimensionsuppsättningar för konfiguration av inköpspris och standardinställda priser. För konfiguration av inköpspris och standardinställda priser på underavtalsrader och tidstransaktioner i underavtal är attributen **Roll** och **Bokningsbar resurs**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]