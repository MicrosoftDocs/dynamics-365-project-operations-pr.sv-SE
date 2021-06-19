---
title: Bestämma projektkostnad och intäktsberäkningar
description: Fastställa uppskattningar av projektets utgifter och intäkter i Project Service
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a81214baafc2017b3d67e6b8bb5b2de19025b10f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015263"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Bestämma projektkostnad och intäktsberäkningar 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektberäkningar ger den ekonomiska vyn för det beräknade och schemalagda arbetet i projektets uppdelade arbetsstruktur. Beräkningsvyn informerar om utgifters och intäkters inverkan på planerat arbete. Beräkningsvyn är ett verktyg för att visa information på ett antal fördefinierade dimensioner som informerar dig om de ekonomiska följderna av projektet.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Kostnad och försäljningsvärde för projektet  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prislistor anger utgiften och fakturataxan för roller som projekt använder. Du kan bestämma utgifts- och intäktseffekten av arbetet utifrån de roller som hör till uppgifterna i projektets uppdelade arbetsstruktur.  
  
## <a name="cost-price-defaulting"></a>Standardsjälvkostnad  
Varje projekt hör till en organisation (anges i **Ägande enhet** i projektet). Prislista som är associerad med den ägande organisationsenheten bestämmer självkostnaden per enhet. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] avgör självutgifter för roller genom att söka efter en kombination av roll, enhet och organisationsenhet i självkostnadslistan för att få den korrekta självkostnaden för dagen som gäller på beräkningsrader.  
  
Om kombinationen av roll, enhet och organisationsenhet inte resulterar i en självkostnad från den ägande enhetens prislista, ignoreras enheten till förmån för kombinationen av roll och organisationsenhet. Om det finns en självkostnad, detta pris konverteras till enheten som du väljer på beräkningsraden.  
  
Om kombinationen av roll och organisationsenhet inte resulterar i en självkostnad, ignoreras organisationsenheten till förmån för kombinationen av roll och enhet, och priset återställs till standardvärdet efter omräkning vid behov.  
  
 Om det inte finns ett pris för rollen, är standardsjälvkostnaden 0,00 på beräkningsraden.  
  
 Alla utgiftsbelopp på beräkningsraderna för projektkostnad visas i den ägande organisationsenhetens valuta.  
  
## <a name="sales-price-defaulting"></a>Standardförsäljningspris  
Försäljningsprislistan baseras på den försäljningsenhet som projektet är kopplat till. Försäljningsprislistan som är associerad offerten eller kontraktet bestämmer enhetens försäljningspris. Om offerten eller kontraktet har en anpassad prislista är detta standardförsäljningsprislistan för projektberäkningar. Om det inte finns någon koppling till försäljningsenheterna blir standardförsäljningsprislistan som konfigurerats i parameterinställningarna standardförsäljningsprislista för projektet. Varje beräkningsrad har en resursorganisationsenhet associerad för att ange organisationsenheten som resurserna kommer att bokas från för att slutföra aktiviteten. Försäljningspriset för de associerade rollerna fastställs genom att söka efter en kombination av roll, enhet och resursorganisationsenhet i försäljningsprislistan för att få det korrekta försäljningspriset för dagen som gäller på beräkningsraderna.  
  
Om kombinationen av roll, enhet och resursorganisationsenhet inte resulterar i ett försäljningspris från försäljningsprislistan, ignorerar systemet enheten och söker efter en kombination av roll och resursorganisationsenhet. Om ett försäljningspris hittas konverteras detta till den enhet som du väljer på försäljningsberäkningsraden.  
  
Om systemet inte hittar ett pris för rollen, måste standardförsäljningspriset vara 0,00 på beräkningsraden.  
  
Beräkningsvyn har en rutnätsvy som visar ett platt rutnät av beräkningsrader med enhet, totala utgift och försäljningspris.  
  
## <a name="time-phased-view-of-project-estimates"></a>Tidsfasad vy över projektberäkningar  
I den tidsfasade vyn för projektberäkningar visas beräkningsdata från rutnätsvyn som standard efter roll, och visar en spridning av beräkningsdata över tidslinjen i den valda tidsskalan.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Allokering av insatsberäkning utifrån uppgiftsläge  
I den tidsfasade vyn fördelas total beräknad insats för uppgiften genom att ett visst antal insatstimmar per enhet allokeras per enhetstidsperiod för den valda tidsskalan. I Project Service avgör uppgiftsläget hur insats allokeras över uppgiftens tid. De två typerna av allokering är jämn allokering och arbetstidsbaserad allokering. 
  
## <a name="work-hours-based-allocation"></a>Arbetstidsbaserad allokering  
Läget automatisk tidsplanering för en uppgift styr att för antalet resurser som beräknas för uppgiften, beräknas de användas för det fullständiga antalet arbetstimmar per dag. Det gäller när insatsen allokeras genom att dela den över hela tiden för uppgifterna även i den tidsfasade vyn. Till exempel, på en tidskala per "Dag" för en uppgift som beräknas slutföras av en resurs kommer insatsen inte att överstiga antalet arbetstimmar per dag som definieras i projektkalendern. Därför säkerställer alltid insatsallokeringen att resurserna beräknas användas under hela dagen.  
  
## <a name="even-distribution"></a>Jämn distribution  
Läget för manuellt schemalagda uppgifter använder inte arbetstimmar, projektkalender eller antalet resurser som har definierats för uppgiften. Uppgiftsschemat baseras på indata från användaren. För sådana uppgifter finns det inte några begränsande faktorer för insatsallokeringen per enhetstidsperiod för den valda tidsskalan. Den totala insatsen för uppgiften delas och allokeras lika för varje enhetstidsperiod på den valda tidsskalan.  
  
På detta sätt bestämmer uppgiftsläget som definieras för uppgiften insatsdistributionen eller allokeringen av insats per enhetstidsperiod i tidsfasade beräkningar.  
  
## <a name="grouping-and-time-phasing-options"></a>Alternativ för gruppering och tidsfasning  
Med den här vyn kan du förstå fördelningen av beräkningar av insats, utgift och försäljning per dag, vecka, månad eller år. Med alternativet Gruppera efter kan beräkningsdata visas för två andra dimensioner: kategori och resurs. I både rutnätsvyn och den tidsfasade vyn kan du välja vilka fält som ska visas. Summor för respektive tidsblock visas längst ned och anger total beräknad insats, kostnad och försäljning per dag, vecka, månad eller år.  
  
Självkostnads- och försäljningspriserna beror på datum. När priset för rollerna ändras blir det tydligare i den tidsfasade vyn när beräkningsdata visas efter "Resurs" och tidsfasas per vecka.  
  
## <a name="expense-estimates"></a>Utgiftsberäkningar  
Alla utgifter som uppkommer i projektet som inte är direkt relaterade till arbete som ska förbrukas kan registreras i projektberäkningar i rutnätsvyn. Med hjälp av alternativet **Lägg till en ny utgiftsberäkning** i rutnätsvy kan du göra detta. Utgiftsberäkningarna kan registreras för en specifik uppgift eller för hela projektet. Du kan välja utgiftskategorier på dessa rader och välja ett preliminärt datum när utgiften förväntas påföras. Om den associerade självkostnads- och försäljningsprislistan har standardpriser, eller påläggsprocentsatser definierade för utgiftskategorier, anges det som standard på beräkningsraden vid associeringen.  
  
### <a name="see-also"></a>Se även  
 [Guiden för projektledare](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]