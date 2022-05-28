---
title: Hantera projektbaserade affärsmöjligheter
description: I det här ämnet finns information om hur du arbetar med affärsmöjligheter som är relaterade till projekt.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f39940ac063a8c202f33797ed649518907563e31
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600442"
---
# <a name="manage-project-based-opportunities"></a>Hantera projektbaserade affärsmöjligheter

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektbaserade företag har vanligtvis sina operationer för leveransspridning i flera länder och geografier. Kostnaden för projektkörningen och leveransen kan variera beroende på vilken geografi eller avdelning som hanterar leveransen. Detta kan i sin tur påverka avtalets marginaler. Leverans av projektbaserade tjänster innebär vanligtvis stora kvantiteter mänsklig tid, avsevärda kostnader för resor, materialkostnader och andra utgifter.

Projektbaserade affärsmöjligheter i Dynamics 365 Project Operations har utformats med tillägg till Dynamics 365 Sales. I ämnet finns information om de olika fälten och affärslogiken i de ytterligare funktioner som krävs av projektbaserade företag för att hantera projektbaserade affärsmöjligheter.

## <a name="view-all-project-based-opportunities"></a>Visa alla projektbaserade affärsmöjligheter

En lista över alla projektbaserade affärsmöjligheter kan ses från listsidan **Affärsmöjlighet**. 

1. Gå till **Försäljning** > **Affärsmöjligheter**.
2. Använd **Vyväxlare** för att välja andra filtrerade vyer av affärsmöjligheterna. Du kan skapa egna vyer med anpassade filtervillkor för att konfigurera dessa vyer och navigeringsalternativ.

Projektmöjligheter kan skapas eller tas bort från den här listsidan eller informationssidan.

## <a name="business-process-flow-for-project-based-deals"></a>Affärsprocessflöde för projektbaserade affärer

Följande affärsprocessflöden stöds för projektbaserade affärer i Project Operations:

- Affärsprocessen Lead till affärsmöjlighet
- Affärsmöjlighet, försäljningsprocess

### <a name="lead-to-opportunity-business-process"></a>Affärsprocessen Lead till affärsmöjlighet 
Affärsprocessen Lead till affärsmöjlighet stöder följande steg:

| Scen | Mappad entitet | Funktioner |
| --- | --- | --- |
| Kvalificera | Lead | Kvalificera lead för att skapa ett konto, en kontakt och en affärsmöjlighet. |
| Ta fram | Affärsmöjlighet | Utveckla affärsmöjligheten och lägg till mer information om det arbete som ingår, viktiga intressenter och konkurrens. |
| Föreslå | Affärsmöjlighet | Utarbeta förslaget och få godkännande från det interna granskningsteamet. |
| Stängning | Affärsmöjlighet | Vinn affärsmöjligheten för att stänga affären. |

### <a name="opportunity-sales-process"></a>Affärsmöjlighet, försäljningsprocess
Affärsmöjlighetens försäljningsprocess i Project Operations är ett tillägg till affärsflöde för affärsmöjlighetens försäljningsprocess i programmet Sales. Affärsprocessen är utformad för att stödja följande stadier i en projektbaserad affärsmöjlighet.

| Scen | Mappad entitet | Funktioner |
| --- | --- | --- |
| Kvalificera | Affärsmöjlighet | Kvalificera lead för att skapa ett konto, en kontakt och en affärsmöjlighet. |
| Föreslå | Offert | Utarbeta förslaget med hjälp av offerter och få godkännande från det interna granskningsteamet. |
| Kontrakt | Projektkontrakt | Vinn offerten för att skapa kontraktet och påbörja körning och leverans av projektet. |
| Stängning | Projektkontrakt | Slutför arbetet och stäng projektkontraktet. |

> [!NOTE]
> Om ditt projektbaserade avtal har inletts med en lead ges affärsprocessen Lead till affärsmöjlighet företräde.
>
> Om ditt projektbaserade avtal har inletts med en affärsmöjlighet ges försäljningsprocessen för affärsmöjligheten företräde.

Du kan redigera produktens affärsprocessflöde eller skapa egna affärsprocessflöden för att spåra din försäljningsprocess efter behov. Mer information om affärsprocessflödet finns i [Översikt över affärsprocessflöden](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]