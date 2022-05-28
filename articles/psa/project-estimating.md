---
title: Projektkostnader och intäkter
description: I det här ämnet finns information om hur du uppskattar projektkostnader och intäkter.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ecac3a08b2405e697eb260bbab991458dbe69f4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581904"
---
# <a name="project-costs-and-revenue"></a>Projektkostnader och intäkter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektberäkningar ger den ekonomiska vyn för det beräknade och schemalagda arbetet i projektets schema. Fliken **Beräkningar** på sidan **projekt** visar utgifts- och intäktseffekten för det arbete som du planerar. Den innehåller också information om många fördefinierade dimensioner. 

> ![Fliken Beräkningar.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Kostnad och försäljningsvärden för projektet

Prislistor anger utgiften och fakturataxan för roller i ett projekt. Du kan bestämma utgifts- och intäktseffekten utifrån rollerna som är associerade med befattningsnamnet och den namngivna resurs som är tilldelad en aktivitet. Om det finns uppgifter som inte har några tilldelningar (generiska eller namngivna) kan du inte få kostnads- eller försäljningsberäkningar. Värden för kostnad och försäljning betraktar det datum som har definierats i prislistorna.

### <a name="default-cost-price"></a>Standardpris för självkostnad  

Varje projekt tillhör en organisation. Den här organisationen visas i fältet **upphandlande enhet** i projektet. Prislistan som är associerad med den upphandlande enheten används för att fastställa självkostnaden för enheten. För att bestämma korrekta självkostnad på roller för det datum som definieras på uppskattningsrader, söker du efter kombinationen av roll, enhet och organisationsenhet i självkostnadslistan. 

För att självkostnaden ska kunna beräknas måste alla uppgifter tilldelas en resurs. Alla otilldelade uppgifter får självkostnaden 0,00.

Om kombinationen av roll, enhet och organisationsenhet inte returnerar en självkostnad från den upphandlande enhetens prislista, ignoreras enheten. Det söker i stället efter kombinationen av roll och organisationsenhet. Om en självkostnad påträffas används konverteringsfaktorer för att konvertera den till den enhet du valde på uppskattningsraden.

Om kombinationen av roll och organisationsenhet inte returnerar en självkostnad ignorerar systemet organisationsenheten. I stället görs en sökning efter kombinationen av roll och enhet för att ange standardpriset (när alla konverteringar har tillämpats).

Om systemet inte hittar ett pris för rollen, måste självkostnaden vara på beräkningsraden anges till standardvärdet **0,00**. Alla utgiftsbelopp på beräkningsraderna för projektkostnad registreras i den upphandlande enhetens valuta.

> [!NOTE]
> Som standard lagrar Microsoft Dynamics 365 kostnadsbelopp i basvalutan. De kostnadsbelopp som visas på fliken **Beräkningar** gäller emellertid i den upphandlande enhetens valuta.  

### <a name="default-sales-price"></a>Standardpris för försäljning 

Försäljningsprislistan avgörs av antingen den försäljningsenhet som projektet är kopplat till eller till projektkunden. När en försäljningsentitet, till exempel en affärsmöjlighet, en offert eller ett kontrakt, associeras med projektet, bestäms försäljningspriset för den aktuella enheten av den prislista som är associerad med offerten eller kontraktet. Om offerten eller kontraktet har en anpassad prislista, används den prislistan som standardförsäljningsprislista för projektberäkningar. Om det inte finns någon koppling till försäljningsentiteterna används standardförsäljningsprislistan från parametrarna som projektets standardförsäljningsprislista som matchas av kundvalutan som definieras för projektet.

Varje beräkningsrad har en resursenhet kopplad till den. Resursenheten anger den organisationsenhet som resurser är bokade från för att slutföra uppgiften. Om du vill fastställa försäljningspriset för de associerade rollerna söker du efter kombinationen av roll, enhet och resursenhet i försäljningsprislistan. Om det inte finns några tilldelningar för uppgiften är försäljningspriset för uppgiften 0,00.

Om kombinationen av roll, enhet och resursenhet inte returnerar ett försäljningspris från försäljningsprislistan ignoreras enheten av systemet. Det söker i stället efter kombinationen av roll och resursenhet. Om ett försäljningspris påträffas används konverteringsfaktorer för att konvertera den till den enhet du valde på försäljningsberäkningsraden. 

Om kombinationen av roll och resursenhet inte returnerar ett försäljningspris från försäljningsprislistan ignoreras resursenheten av systemet. I stället görs en sökning efter kombinationen av roll och enhet för att ange standardpriset (när alla konverteringar har tillämpats).

Om systemet inte hittar ett pris för rollen, måste försäljningspriset vara på beräkningsraden anges till standardvärdet **0,00**.

Fliken **Beräkningar** innehåller en rutnätsvy som visar beräknade rader. I rutnätet finns kolumner för enheten, total självkostnad och totalt försäljningspris, som du ser på följande bild. 

> ![Rutnätsvy på fliken Beräkningar.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Tidsfasad vy över projektberäkningar

I vyn tidsfaser i projektberäkningar visar beräkningsdata från rutnätsvy över tidslinjen i en tidsskala som du har valt. Som standard pivoteras beräkningsdata i dimensionen **roll**.

> ![Tidsfasad vy för projektberäkningar.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Allokering av beräknad insats utifrån uppgiftsläge

I den tidsfasade vyn fördelar du total beräknad insats för uppgiften genom att insatstimmar per enhet allokeras per enhetstidsperiod i den valda tidsskalan. Uppgiftsläge avgör uppgiftsläget hur insats allokeras över uppgiftens tid. De två typerna av allokering är **jämn** och **arbetstidsbaserad**.

### <a name="work-hours-based-allocation"></a>Arbetstidsbaserad allokering
 
I läget för automatisk schemaläggningsuppgift ställs de dagliga standardtimmarna för uppgiftsresurser in som hela timkostnaden för arbetet. Detta beteende gäller när insatsen allokeras genom att dela den över hela tiden för uppgifterna även i den tidsfasade vyn. Om du till exempel beräknar att uppgiften kommer att slutföras av en resurs i tidsskalan **Dag** kommer insatsen som allokeras per dag inte att överstiga antalet arbetstimmar per dag som definieras i projektkalendern. Därför säkerställer alltid insatsallokeringen att resurserna beräknas användas under hela dagen.

### <a name="even-allocation"></a>Jämn allokering

I manuellt läge för schemalagd uppgift används inte arbetstiderna från projektkalendern. Uppgiftsschemat baseras istället på indata från användaren. För dessa uppgifter finns det inte några begränsande faktorer för insatsallokeringen per enhetstidsperiod för den valda tidsskalan. Den totala insatsen för uppgiften delas och allokeras lika för varje enhetstidsperiod på den valda tidsskalan. På detta sätt bestämmer uppgiftsläget som definieras för uppgiften insatsdistributionen eller allokeringen av insats per enhetstidsperiod i tidsfasade beräkningar.

## <a name="grouping-and-time-phasing-options"></a>Alternativ för gruppering och tidsfasning

Den tidsfasade vyn visar fördelningen av beräkningar av insats, utgift och försäljning per dag, vecka, månad eller år. Som standard pivoteras beräkningsdata i dimensionen **roll**. Du kan emellertid använda alternativet **gruppera efter** om du vill pivotera två andra dimensioner: **kategori** och **resurs**.

I både rutnätsvy och vyn med tidsfaser kan du välja vilka fält som ska visas. Summorna för varje tidsblock visas längst ned i projektet. De visar den totala beräknade insatsen och försäljningen för dag, vecka, månad eller år. Standardsjälvkostnaden och försäljningspriset beror på datumet. De ändras alltså för varje resurs, beroende på vilken vy med tidsfaser som du har valt.

## <a name="expense-estimates"></a>Utgiftsberäkningar

Knappen **Lägg till en ny utgiftsberäkning** i rutnätsvyn låter dig registrera alla utgifter som påförts i projektet, men som inte är direkt relaterade till arbete. Du kan registrera utgiftsberäkningar för en specifik uppgift eller för hela projektet. Välj utgiftskategorier och preliminärt datum då du förväntar dig utgiften. Om den associerade självkostnadslistan och försäljningsprislistan har standardpriser (eller påläggsprocentsatser definierade för utgiftskategorier) och anges automatiskt på beräkningsraden vid associeringen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
