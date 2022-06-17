---
title: Hantera projektprislistor i en offert
description: Den här artikeln innehåller information om att arbeta med entiteten projektprislista.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8439a03e6557ec531405048ec4149344e283242e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933176"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Hantera projektprislistor i en offert

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations utökar entiteten för prislista i Dynamics 365 Sales. 

## <a name="key-entities"></a>Nyckelentiteter

En prislista innehåller information som ges av fyra olika entiteter:

- **Prislista**: den här entiteten lagrar information om sammanhang, valuta, giltighetsdatum och tidsenhet för prissättningstid. Sammanhang visar om prislistan uttrycker kostnadstariffer eller försäljningspriser. 
- **Valuta**: med den här entiteten lagras prisvalutan i prislistan. 
- **Datum**: den här entiteten används när systemet försöker ange ett standardpris i en transaktion. En prissättning väljer den prislista som har giltighetsdatum som omfattar datumet för transaktionen. Om mer än en prislista är giltig för transaktionsdatumet är kopplat till den relaterade offerten, kontraktet eller organisationsenheten blir inget pris standard. 
- **Tid**: den här entiteten lagrar den tidsenhet som priserna uttrycks för, t.ex. dag eller timkostnad. 

Entiteten för prislista har tre relaterade tabeller som lagrar priser:

  - **Rollpris**: i den här tabellen lagras en tariff för en kombination av värden för roll och organisationsenheter och används för att konfigurera rollbaserade priser för personal.
  - **Pris för transaktionskategori**: i den här tabellen lagras priser per transaktionskategori och används för att ställa in priser för utgiftskategorier.
  - **Prislisteobjekt**: i den här tabellen lagras priserna för katalogprodukter.
 
Prislista är en prislista. En prislista är en kombination av entiteten prislista och relaterade rader i tabellerna rollpris, transaktionskategoripris och prislisteobjekt.

## <a name="resource-roles"></a>Resursroller

Termen *resursroller* refererar till den uppsättning färdigheter, kompetenser och certifieringar som en person måste ha för att utföra en specifik uppsättning uppgifter i ett projekt.

Personaltider anges utifrån den roll som en resurs fyller i ett specifikt projekt. För personalresurser är kostnad och fakturering baserad på resursrollen. Tid kan vara pris i valfri enhet i enhetsgruppen för **tid**.

Enhetsgruppen **Tid** skapas när du installerar Project Operations. Den har en standardenhet på **timme**. Du kan inte ta bort, byta namn på eller redigera attributen för enhetsgruppen **Tid** eller enheten **Timme**. Men du kan lägga till andra enheter i enhetsgruppen för **tid**. Om du försöker ta bort antingen enhetsgruppen **Tid** eller enheten **Timme** kan det leda till fel i affärslogiken.
 
## <a name="transaction-categories-and-expense-categories"></a>Transaktionskategorier och utgiftskategorier

Resekostnader och andra utgifter som ingår i projektkonsulter faktureras till kunden. Prissättning av utgiftskategorier slutförs med hjälp av prislistor. Flyg, hotell och hyrbil är exempel på utgiftskategorier. Varje rad i en prislista för utgifter anger prissättningen för en specifik utgiftskategori. Följande tre metoder används för att pris- och utgiftskategorier:

- **Vid kostnad**: kostnaden faktureras till kunden och inget pålägg används.
- **Påläggsprocent**: procentsatsen för den faktiska kostnaden faktureras till kunden. 
- **Pris per enhet**: ett faktureringspris anges för varje enhet i utgiftskategorin. Det belopp som faktureras för kunden beräknas utifrån antalet utgiftsenheter som konsulterna rapporterar. Körsträcka använder prismodellen pris per enhet. Exempelvis kan utgiftskategorin körsträcka konfigureras för 30 USD per dag eller 2 USD per mil. När en konsult rapporterar körsträcka i ett projekt beräknas faktureringsbeloppet utifrån det antal mil som konsulten rapporterat.
 
## <a name="project-sales-pricing-and-overrides"></a>Prissättning för projektförsäljning och åsidosättningar

För projektofferter och kontrakt har en projektprislista ett annat pris för åsidosättningsmönster än en produktprislista. På en produktkatalogbaserad offertrad kan du åsidosätta priset till roller och kategorier direkt på offertraden, eftersom varje offertrad pekar till exakt ett katalogobjekt. På en projektrelaterad offertrad kan du emellertid inte åsidosätta priset för roller och kategorier direkt på offertraden. Använd projektprislistan för ge stöd till de två distinkta åsidosättningarna.

> [!NOTE]
> Vi rekommenderar att du har en separat prislista för dina projektresurser och dina katalogobjekt, eftersom det finns skillnader mellan de två när du åsidosätter priserna.

Följande entiteter kan ha en eller flera associerade försäljningsprislistor för projektprissättning:

- Kund (konto) 
- Affärsmöjlighet 
- Offert 
- Projektkontrakt

Associationen mellan dessa entiteter och en prislista visas i projektprislistorna. Du kan associera en eller flera prislistor med entiteterna kund, affärsmöjlighet, offert och projektkontraktförsäljning.

En standardprislista för projekt anges inte automatiskt i en kundpost. Du kan emellertid bifoga en projektprislista manuellt till kundposten. Däremot bör du endast bifoga en projektprislista manuellt när du har ett anpassat prissättningsavtal med kunden. 

När en projektpris lista är kopplad till en försäljningsenhet verifieras följande information:

- Prislistan har kontexten **försäljning**. 
- Prislistans valuta matchar kundvalutan. 

I ett projektkontrakt används följande prioriteringsordning för att automatiskt ange relaterade projektprislistor:

1. Offert
2. Affärsmöjlighet
3. Kund 
4. Globala inställningar 

När en projektprislista anges som standard verifierar systemet att valutan överensstämmer med kundens valuta och att standardprislistorna som har angetts har kontexten **försäljning**.

Du kan associera flera projektprislistor med entiteterna kund, affärsmöjlighet, offert och projektkontrakt. Den här funktionen har stöd för tidsspecifika standardpriser för ett långvarigt projektkontrakt, där du kan behöva mer än en prislista för att ta hänsyn till prisuppdateringar som sker på grund av inflation. Om de prislistor som du associerar med en entitet för kund, affärsmöjlighet, offert eller projektkontrakt har överlappande giltighetsdatum kan standardpriset vara fel. Därför bör du kontrollera att projektprislistor som har överlappande giltighetsdatum inte är associerade med dessa entiteter.

### <a name="deal-specific-price-overrides"></a>Avtalsspecifika prisåsidosättningar

Du kan skapa detaljerade åsidosättningar för valda priser på projektprislistor som anges som standard i en offert eller ett projektkontrakt.

Ett projektkontrakt får som standard alltid en kopia av huvudsakliga försäljningsprislistan i stället för en direkt länk till den. Detta bidrar till att säkerställa att prisavtal som görs med en kund för en arbetsbeskrivning (SOW) inte ändras om huvudsakliga prislistan ändras.

I en offert kan du emellertid använda en huvudsaklig prislista. Du kan också kopiera en huvudsaklig prislista och redigera den om du vill skapa en anpassad prislista som bara gäller för den offerten. Om du vill skapa en ny prislista som är specifik för en offert väljer du sidan **Offert** och **Skapa anpassad prissättning**. Du kan bara komma åt den aktuella projektprislistan från offerten. 

När du skapar en anpassad projektprislista kopieras endast projektkomponenterna för prislistan. Med andra ord skapas en ny prislista som skapas som en kopia av den befintliga projektprislistan som är kopplad till offerten, och den nya prislistan har endast relaterade rollpriser och transaktionskategoripriser.
  
## <a name="tracking-costs"></a>Spåra kostnader

Project Operations spårar kostnader för användning av tid för mänsklig resurs i projekt. Dessutom spåras kostnaderna för andra utgifter som inträffat under projektet, t.ex. resekostnader.

På samma sätt som med faktureringskostnader är kostnadstariffer för personal även inställda med hjälp av prislistor. Här är de viktigaste skillnaderna i hur prislista för självkostnad och listan för försäljningspris används:

- En resurs kostnadstaxa kan inte skrivas över i ett specifikt projekt, kontrakt eller offert. Faktureringsavgifter kan dock åsidosättas per avtal om ändringar görs som är specifika för det aktuella erbjudandet. 

- Följande order används för att matcha en prislista för självkostnad:

    1. Prislista för självkostnad är kopplad till organisationsenheten.
    2. Prislista för självkostnad är kopplad till Project Operations-parametrarna. Eftersom prislista för självkostnad i många olika valutor kan kopplas till parametrar, slutförs en valutamatchning mellan valutan i den upphandlande organisationsenheten för projektet, kontraktet eller offerten och valutan i prislistan för självkostnad.
    3. För utgifter gäller prissättningsmetoderna Vid kostnad och Pålägg på kostnad inte prislistor för självkostnad. Även om de här prissättningsmetoderna används på rader för prislista för självkostnad för att konfigurera kostnaderna för en transaktionskategori ignoreras de och ingen standardsjälvkostnad anges.


[!INCLUDE[footer-include](../includes/footer-banner.md)]