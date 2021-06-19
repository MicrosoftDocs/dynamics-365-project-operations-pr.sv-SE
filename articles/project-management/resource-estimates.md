---
title: Ekonomisk kalkyl för resurstid på projekt
description: Den ämne information om hur ekonomiska resurser för tid beräknas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010808"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Ekonomisk kalkyl för resurstid på projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Ekonomisk kalkyl för tid beräknas utifrån tre faktorer: 

- Typ av generisk eller namngiven teammedlem som har tilldelats varje uppgift i noden i projektplan. 
- Arbetets typ eller komplexitet.
- Spridningen av insats för resursens tilldelning för uppgiften. 

De första två faktorerna påverkar enhetskostnaden eller faktureringstakten för en resurstilldelning. Enhetskostnaden eller fakturataxan för en resurstilldelning fastställs av attributen för den tilldelade resursen. Attributen omfattar den organisationsenhet resursen tillhör och standardrollen för resursen. Du kan också lägga till anpassade attribut som är relevanta för ditt företag för resursen, som standardtitel eller erfarenhetsnivå och få dem att påverka enhetskostnaden eller faktureringsgraden för uppdraget.
Förutom resursens attribut kan attribut för arbete, såsom uppgiften även påverka enhetens faktureringskurs eller kostnadstaxa. Till exempel, när vissa uppgifter är mer komplexa, resulterar resursens tilldelning till dessa specifika uppgifter i en högre enhetskostnad eller faktureringsgrad än uppgifter som är mindre komplexa.   

Den tredje faktorn är antalet timmar i den takten. I fall där en uppgift täcker två prisperioder är det troligt att den första delen av resurstilldelningen för den uppgiften kostar och prissätts annorlunda än den andra delen av uppgiften. Insatsberäkningen för varje resurstilldelning är ett komplext värde som lagras med den dagliga fördelningen av insats per dag.

För detaljerade instruktioner om hur du ställer in anpassade attribut för arbete och resurser som pris- och kostnadsdimensioner, se [Översikt över prisdimensioner](../pricing-costing/pricing-dimensions-overview.md).

Den ekonomiska uppskattningen för varje resurstilldelning beräknas som **hastighet/timmar för uppgiften multiplicerat med antalet timmar.**  I likhet med ansträngningsuppskattningen är den ekonomiska uppskattningen för kostnader och intäkter för varje resurstilldelning ett komplext värde som lagras med den dagliga fördelningen av det monetära beloppet per dag. 

## <a name="summarizing-financial-estimates-for-time"></a>Sammanfatta ekonomiska resultat för tid
En ekonomisk beräkning för tid för en uppgift i noden är summan av de ekonomiska kostnaderna för alla resurstilldelningar för den uppgiften.

En ekonomisk uppskattning för tid på en sammanfattning eller överordnad uppgift är summan av de ekonomiska uppskattningarna för alla dess underordnade uppgifter. Detta är den beräknade arbetskostnaden för projektet. 

![Resursuppskattningar](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standardvärden för självkostnad och kostnadsvaluta

Standardkostnadspriset kommer från de prislistor som är kopplade till projektets kontraktenhet. Projektets kostnadsvaluta är den kontrakterande enhetens valuta på projektet. Vid en resurstilldelning lagras den ekonomiska kostnadsberäkningen i projektkostnadsvalutan. Ibland skiljer sig valutan som kostnadskostnaden ställs in i prislistan i från projektets kostnadsvaluta. I så fall konverterar programmet valutan som kostnadspriset är inställt i för valutan i projektet. Rutnätet **Beräkningar**, alla kostnadsberäkningar visas och sammanfattas i projektets kostnadsvaluta. 

## <a name="default-bill-rate-and-sales-currency"></a>Standardvärden för fakturataxan och försäljningsvaluta

Standardförsäljningspriset kommer från projektprislistorna som bifogas det relaterade projektavtalet om affären har vunnits, eller från det relaterade projektofferten om affären fortfarande befinner sig i förförsäljningsstadiet. Projektets försäljningsvaluta är alltid valutan för projektofferten eller projektavtalet. Vid en resurstilldelning lagras den ekonomiska beräkningen för försäljning i projektförsäljningsvalutan. Till skillnad från kostnad kan försäljningspriset som ställs in i prislistan aldrig skilja sig från projektets försäljningsvaluta. Det finns inget scenario där valutakonvertering behövs. Rutnätet **Beräkningar**, alla försäljningsberäkningar visas och sammanfattas i projektets försäljningsvaluta. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
