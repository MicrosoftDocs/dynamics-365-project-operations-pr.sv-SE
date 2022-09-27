---
title: Huvudbegrepp vid underleverantörskap
description: I den här artikeln finns information om viktiga begrepp som kan användas vid underkonfigurering i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9577169f12198222e647ed07ae8a1b6c55da4323
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522771"
---
# <a name="key-concepts-in-subcontracting"></a>Huvudbegrepp vid underleverantörskap


_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I den här artikeln finns information om viktiga begrepp som du bör känna till innan du börjar använda underleverantörsfunktionen i Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Kontrakteringsenhet för underleverantör

Kontrakteringsenheten representerar den avdelning eller praktik som äger leveranserna av det slutliga projektet. Kontrakteringsenheten är också den avdelning som ingår i kontraktrelationen med leverantören.

## <a name="purchase-currency"></a>Inköpsvaluta

I Project Operations är inköpsvalutan den valuta som underkontraktet skapas i. Det är också valutan som underleverantörers kostnader för ett projekt registreras i. Inköpsvalutan kan skilja sig från projektvalutan och projektvalutan kan i sin tur skilja sig från försäljningsvalutan.

## <a name="billing-methods-on-subcontract-lines"></a>Faktureringsmetoder på underleverantörsrader

För projekt finns det vanligtvis en kontraktsmodell med fast kostnad och en förbrukningsbaserad modell. Project Operations stöder dessa faktureringsmetoder i försäljnings- och köpkontexterna. Faktureringsmetoderna för ett köp fungerar på följande sätt:

- **Tid och material** – När en underavtalsrad använder faktureringsmetoden **Tid och material** registreras tidskostnaden i projektet som underleverantörers arbete i det projektet och posttiden. Dessa kostnadstransaktioner från underleverantörer matchas sedan med radobjekten på leverantörsfakturor. I den här modellen kan projektledare som använder Project Operations matcha och verifiera leverantörsfakturarader med den underleverantörstid som har registrerats och godkänts. När verifikationen är klar kommer tidigare faktiska kostnader som registrerats efter godkännande att återställas och nya faktiska kostnader som bygger på leverantörsfakturan skapas i projektet.
- **Fast pris** – I den här kontraktsmodellen med fast avgifter baseras leverantörsfakturor på fasta milstolpar. Men underleverantörers resurser kan också rapportera tid. Tiden granskas och godkänns sedan av projektledaren. När den har godkänts skapar Project Operations tillfälliga faktiska kostnader i projektet. När leverantören skickar en faktura för en milstolpe kan projektledaren matcha tidigare registrerade faktiska kostnader mot milstolpen. När verifikationen är klar kommer de faktiska kostnaderna att återföras och den milstolpebaserade kostnaden registreras.

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
