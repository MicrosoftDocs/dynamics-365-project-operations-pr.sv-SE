---
title: Bestämma projektkostnad och intäktsberäkningar
description: Fastställa uppskattningar av projektets utgifter och intäkter i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 66fa8f4374caa08b07663cc9d261bfff8ce30c87
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133030"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Bestämma projektkostnad och intäktsberäkningar 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektberäkningar ger den ekonomiska vyn för det beräknade och schemalagda arbetet i projektets uppdelade arbetsstruktur. Beräkningsvyn informerar om utgifters och intäkters inverkan på planerat arbete. Beräkningsvyn är ett verktyg för att visa information på ett antal fördefinierade dimensioner som informerar dig om de ekonomiska följderna av projektet.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Kostnad och försäljningsvärde för projektet  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prislistor anger utgiften och fakturataxan för roller som projekt använder. Du kan bestämma utgifts- och intäktseffekten av arbetet utifrån de roller som hör till uppgifterna i projektets uppdelade arbetsstruktur.  
  
## <a name="cost-price-defaulting"></a>Standardsjälvkostnad  
Varje projekt hör till en organisation (anges i **Ägande enhet** i projektet). Prislista som är associerad med den ägande organisationsenheten bestämmer självkostnaden per enhet. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] avgör självutgifter för roller genom att söka efter en kombination av roll, enhet och organisationsenhet i självkostnadslistan för att få den korrekta självkostnaden för dagen som gäller på beräkningsrader.  
  
Om kombinationen av roll, enhet och organisationsenhet inte resulterar i en självkostnad från den ägande enhetens prislista, ignoreras enheten och kombinationen av roll och organisationsenhet används i stället. Om det finns en självkostnad, detta pris konverteras till enheten som du väljer på beräkningsraden.  
  
Om kombinationen av roll och organisationsenhet inte resulterar i en självkostnad, ignoreras organisationsenheten och kombinationen av roll och enhet används i stället. Priset används som standard när du har använt någon konvertering om det behövs.  
  
 Om det inte finns ett pris för rollen, är standardsjälvkostnaden 0,00 på beräkningsraden.  
  
 Alla utgiftsbelopp på beräkningsraderna för projektkostnad visas i den ägande organisationsenhetens valuta.  
  
## <a name="sales-price-defaulting"></a>Standardförsäljningspris  
Försäljningsprislistan baseras på den försäljningsenhet som projektet är kopplat till. Försäljningsprislistan som är associerad offerten eller kontraktet bestämmer enhetens försäljningspris. Om offerten eller kontraktet har en anpassad prislista, är den standardförsäljningsprislista för projektberäkningar. Om det inte finns någon koppling till försäljningsenheterna blir standardförsäljningsprislistan som konfigurerats i parameterinställningarna standardförsäljningsprislista för projektet. Varje beräkningsrad har en resursorganisationsenhet associerad för att ange organisationsenheten som resurserna kommer att bokas från för att slutföra aktiviteten. Försäljningspriset för de associerade rollerna fastställs genom att söka efter en kombination av roll, enhet och resursorganisationsenhet i försäljningsprislistan för att få det korrekta försäljningspriset för dagen som gäller på beräkningsraderna.  
  
Om kombinationen av roll, enhet och resursorganisationsenhet inte resulterar i ett försäljningspris från försäljningsprislistan, ignorerar systemet enheten och söker efter en kombination av roll och resursorganisationsenhet. Om ett försäljningspris hittas konverteras det till enheten som du väljer på försäljningsberäkningsraden.  
  
Om systemet inte hittar ett pris för rollen, måste standardförsäljningspriset vara 0,00 på beräkningsraden.  
  
Beräkningsvyn har en rutnätsvy som visar ett platt rutnät av beräkningsrader med enhet, totala utgift och försäljningspris.  
  
## <a name="time-phased-view-of-project-estimates"></a>Tidsfasad vy över projektberäkningar  
I den tidsfasade vyn för projektberäkningar visas beräkningsdata från rutnätsvyn som standard efter roll, och visar en spridning av beräkningsdata över tidslinjen i den valda tidsskalan.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Allokering av insatsberäkning utifrån uppgiftsläge  
I den tidsfasade vyn fördelas total beräknad insats för uppgiften genom att ett visst antal insatstimmar per enhet allokeras per enhetstidsperiod för den valda tidsskalan. I Project Service avgör uppgiftsläget hur insats allokeras över uppgiftens tid. De två typerna av allokering är jämn allokering och arbetstidsbaserad allokering  
  
## <a name="work-hours-based-allocation"></a>Arbetstidsbaserad allokering  
Läget automatisk tidsplanering för en uppgift styr att för antalet resurser som beräknas för uppgiften, beräknas de användas för det fullständiga antalet arbetstimmar per dag. Det gäller när insatsen allokeras genom att dela den över hela tiden för uppgifterna även i den tidsfasade vyn. Till exempel, på en tidskala per "Dag" för en uppgift som beräknas slutföras av en resurs kommer insatsen inte att överstiga antalet arbetstimmar per dag som definieras i projektkalendern. Därför säkerställer alltid insatsallokeringen att resurserna beräknas användas under hela dagen.  
  
## <a name="even-distribution"></a>Jämn distribution  
Läget för manuellt schemalagda uppgifter använder inte arbetstimmar, projektkalender eller antalet resurser som har definierats för uppgiften. Uppgiftsschemat baseras på indata från användaren. För sådana uppgifter finns det inte några begränsande faktorer för insatsallokeringen per enhetstidsperiod för den valda tidsskalan. Den totala insatsen för uppgiften delas och allokeras lika för varje enhetstidsperiod på den valda tidsskalan.  
  
På detta sätt bestämmer uppgiftsläget som definieras för uppgiften insatsdistributionen eller allokeringen av insats per enhetstidsperiod i tidsfasade beräkningar.  
  
## <a name="grouping-and-time-phasing-options"></a>Alternativ för gruppering och tidsfasning  
Med den här vyn kan du förstå fördelningen av beräkningar av insats, utgift och försäljning per dag, vecka, månad eller år. Med alternativet Gruppera efter kan beräkningsdata visas för två andra dimensioner: kategori och resurs. I både rutnätsvyn och den tidsfasade vyn kan du välja vilka fält som ska visas. Summor för varje tidsblock visas längst ned och anger total beräknad insats, utgift och försäljning för dag, vecka, månad eller år.  
  
Vilken standardvärde utgifts- och försäljningspriset har beror på datumet. När priset för rollerna ändras blir det tydligare i den tidsfasade vyn när beräkningsdata visas efter "Resurs" och tidsfasas per vecka.  
  
## <a name="expense-estimates"></a>Utgiftsberäkningar  
Alla utgifter som uppkommer i projektet som inte är direkt relaterade till arbete som ska förbrukas kan registreras i projektberäkningar i rutnätsvyn. Med hjälp av alternativet **Lägg till en ny utgiftsberäkning** i rutnätsvy kan du göra detta. Utgiftsberäkningarna kan registreras för en viss uppgift eller för hela projektet. Du kan välja att utgiftsföra kategorier på de här raderna och välja ett preliminärt datum när utgiften förväntas uppkomma. Om den associerade självkostnads- och försäljningsprislistan har standardpriser, eller påläggsprocentsatser definierade för utgiftskategorier, anges det som standard på beräkningsraden vid associeringen.  
  
### <a name="see-also"></a>Se även  
 [Guiden för projektledare](../psa/project-manager-guide.md)
