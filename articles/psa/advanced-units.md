---
title: Enhetsgrupper och enheter
description: I det här ämnet finns information om enhetsgrupper och enheter.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009593"
---
# <a name="unit-groups-and-units"></a>Enhetsgrupper och enheter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Enhetsgrupper och enheter är grundläggande entiteter i Microsoft Dynamics 365. En enhet är en enskild enhet och flera enheter kan grupperas i enhetsgrupper. En enhetsgrupp kallas ibland för enhetsschema i användargränssnittet i Dynamics 365 (UI). 

Här är några exempel på enheter och enhetsgrupper:
 
- **Enhetsgrupp**: avstånd 
    - **Enheter**: mil, kilometer och så vidare.
- **Enhetsgrupp**: Tid
    - **Enheter**: timme, dag, vecka och så vidare. 

När du skapar flera enheter i en enhetsgrupp måste du också skapa en konverteringsfaktor mellan dem genom att ange den första enheten som du anger som standardenhet eller primär enhet för enhetsgruppen. 

Till exempel i enhetsgruppen **Tid** om du ställer in **timme** som den första enheten kommer system ange **timme** som standardenhet. Om nästa enhet som du konfigurerar är **dag** måste du ange en konverteringsfaktor för **dag** till **timme**. Om du sedan lägger till **vecka** som en tredje enhet måste du ange en konverteringsfaktor för **vecka** utifrån **dag** eller **timme**. 

I följande bild visas en exempelinställning för enheten **Dag** där fältet **kvantitet** visar antalet timmar som befinner sig på en dag och **vecka** där fältet **antal** visar antalet dagar i veckan.

> ![Enhetsgrupp: informationssida](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Använda enheter och enhetsgrupper

Dynamics 365 Project Service Automation använder enheter och enhetsgrupper för att bearbeta beräkningar och transaktioner för både utgifter och tid. 

För utgifter har varje utgiftskategori en standardenhetsgrupp och enhet. Dessa värden anges som standardvärden för prislistetransaktioner för utgiftskategorier. 

Du har till exempel en utgiftskategori som heter **Körsträcka**. Den har en enhetsgrupp med namnet **avstånd** och en standardenhet med namnet **mil**. Om du anger enhetsgruppen **avstånd** så att den har två enheter (**Mil** och **Kilometer**) kan du ange två priser för kategorin **körsträcka** på en prislista: pris per mil och pris per kilometer.

| Utgiftskategori  | Enhetsgrupp  | Enhet      | Prismodell  | Pris per enhet  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Körsträcka           | Avstånd      | Mil      | Pris per enhet    | 10 USD            |
| Körsträcka           | Avstånd      | Kilometer | Pris per enhet    |  6 USD            |

När du anger en utgift i ett projekt avgör systemet priset via kombinationen av kategorin och enheten i kostnaden. 

| Beskrivning av utgift        | Utgiftskategori  | Enhet  | Kvantitet  | Enhetspris   |
|----------------------------|---------------------|-------|-----------|----------------|
| Köra till kundens plats | Körsträcka             | Mil  | 10        | 10 USD         |

För tid har varje prislistehuvud ett fält för **standardtidenhet**. Värdet anges när du skapar ett prislistehuvud. Enheten används sedan för att ange alla rollbaserade priser på den prislistan.

Beräkningsrader för fältet **tid på offert** kan uttryckas i valfri tidsenhet. Beräkningsrader i projekt och tidstransaktioner för projekt kan emellertid endast använda tidsenheten **timme**. Om enheten på tidsposten eller uppskattningsraden inte överensstämmer med enheten på prislisteraden för den rollen, konverteras priset till de enheter som är definierade i projektberäkningen eller den faktiska transaktionen i projektet.

Följande exempel visar hur PSA använder enhetsgrupperna, enheterna och konverteringsfaktorerna.
- Enheter

   - **Enhetsgrupp**: Tid 
   - **Enheter**: timme 
    
    - **Dag** - konverteringsfaktor: 8 timmar       
    - **Vecka** - konverteringsfaktor: 40 timmar  
        
- Inställning av prislista för projekt A:

    - **Namn**: UK förs. pris 2016 
    - **Standardtidsenhet**: dag 
    - **Valuta**: GBP

| Roll      | Enhetsgrupp | Enhet | Organisationsenhet | Pris   |
|-----------|------------|------|---------------------|---------|
| Utvecklare | Tid       | dag  | Contoso Storbritannien          | 800 GBP |

### <a name="time-entry"></a>Tidspost

I följande tabell visas den resulterande försäljningstransaktionen som skapats av PSA för ett tre timmars projekt.


| Projekt   | Uppgift    | Roll      | Kvantitet | Enhet  | Enhetspris | Ofakturerat försäljningsbelopp |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Design  | Utvecklare | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Vanliga frågor om tidsenhet

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Konverterar PSA till olika enheter vad gäller utgifter?
Nr Enhetskonvertering fungerar endast för tid. För utgifter, om systemet inte kan hitta ett pris för kombinationen av utgiftskategorin och enheten är priset som standard inställt på 0,00.

### <a name="why-does-psa-convert-time-units"></a>Varför konverterar PSA tidsenheter?
I vissa länder eller regioner finns det ett juridiskt krav som faktureringsavgifterna ställs in i dagar. Prisförhandling och rabattering under offertcykeln görs med hjälp av dagsräntor för varje fakturerbar roll. Schemaberäkning och tidsregistrering sker i timmar. För att kunna stödja denna skillnad i tidsenheter kan PSA konvertera tidsenheter.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Kan tidsenheter ändras i projektberäkningar?
Nr Schemaberäkningen är för närvarande begränsad till timmar och kan inte ändras.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Kan enheter och enhetsgrupper redigeras, tas bort och läggas till?
Ja. Med undantag för enhetsgruppen **Tid** och enheten **timme** kan alla enheter tas bort och du kan lägga till nya enheter. I PSA kan enhetsgruppen **Tid** och enheten **Timme** inte tas bort. De kan emellertid uppdateras med översatt text för fältet **namn**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]