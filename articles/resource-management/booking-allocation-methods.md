---
title: Metoder för bokning av allokeringar
description: I det här ämnet finns information om hur bokningsmetoder fungerar i Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 358eb5a6ccf1dd09f8056a20dbf6906e2c3803bd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280060"
---
# <a name="booking-allocation-methods"></a>Metoder för bokning av allokeringar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Oavsett om du lägger till en teammedlem direkt i ett projekt på fliken **Team** eller schemalägger en resurs till ett projekt eller krav via schemaläggningstavlan, finns det några olika bokningsallokeringsmetoder du kan använda. Det här ämnet lär dig hur de olika metoderna fungerar och vilka metoder som kan leda till överbokning av resurser.

## <a name="booking-allocation-methods"></a>Metoder för bokning av allokeringar

Du kan använda sex olika typer av bokningstilldelningar:

- [Full kapacitet](#full)
- [Återstående kapacitet](#remaining)
- [Procentandel kapacitet](#percentage)
- [Fördela timmar jämnt](#evenly)
- [Timmar, frontinläsning](#front)
- [Nej](#none)

### <a name="full-capacity"></a><a name="full"></a>Full kapacitet 
Metoden full kapacitet bokar resursens fulla kapacitet för angivna från- och till-datum. Om en resurs exempelvis har en kalender med 8 timmars arbetsdag 5 dagar i veckan, kommer start- och slutdatum som täcker 5 arbetsdagar att boka resursen i 40 timmar. Bokningen görs utan hänsyn till resursens återstående kapacitet. Om en resurs redan bokats under perioden för andra projekt kommer de 40 timmarna att bokas som extratimmar, vilket eventuellt kan förorsaka överbokningar.

### <a name="remaining-capacity"></a><a name="remaining"></a>Återstående kapacitet
Metoden återstående kapacitet finns bara att tillgå när du bokar direkt till ett projekt via schemaläggningstavlan. Denna metod bokar resursens tillgängliga kapacitet inom angivet datumintervall. Om en resurs exempelvis har en kapacitet på 40 timmar per vecka och redan har bokats 10 timmar, kommer bokning för samma vecka resultera i bokning av de återstående 30 timmarnas kapacitet för den veckan.

### <a name="percentage-capacity"></a><a name="percentage"></a>Procentandel kapacitet
Metoden Procentandelskapacitet bokar resursen under en viss procentandel av resursens kapacitet för angivna från- och till-datum. Om en resurs exempelvis har en kalender med 8 timmars arbetsdag 5 dagar i veckan, kommer start- och slutdatum som täcker 5 arbetsdagar till 50 % kapacitet att boka resursen i 20 timmar. Enskilda dagliga bokningar sprids ut jämnt över perioden, till exempel 4 timmar per dag i detta exempel. Bokningen görs utan hänsyn till resursens återstående kapacitet. Om en resurs redan bokats under perioden för andra projekt kommer de 20 timmarna att bokas som extratimmar, vilket eventuellt kan förorsaka överbokningar.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Fördela timmar jämnt
Metoden Fördela timmar jämnt bokar resursen under ett angivet antal timmar och fördelar tiden jämnt per dag under angivna från- och till-datum. Om du exempelvis bokar en resurs under 20 timmar under en 5-dagarsperiod kommer denna metod att fördela de 20 timmarna jämnt på fyra timmar per dag. Bokningen görs utan hänsyn till resursens återstående kapacitet. Om en resurs redan bokats under perioden för andra projekt kommer de 20 timmarna att bokas som extratimmar, vilket eventuellt kan förorsaka överbokningar.

### <a name="front-load-hours"></a><a name="front"></a>Timmar, frontinläsning
Metoden Timmar, tidigareläggning bokar resursen under ett angivet antal timmar och tidigarelägger timmarna per dag under angivna från- och till-datum. Tidigareläggningen förbrukar resursens tillgängliga kapacitet i ordningen ”först in-först förbrukad”. Om resursens arbetsschema exempelvis är åtta timmar per dag, fem dagar i veckan, och inga bokningar finns för tillfället, medför bokning av resursen under 20 timmar under en period om fem arbetsdagar i följande dagliga bokningsmönster: 

|                           |    Dag 1    |    Dag 2    |    Dag 3    |    Dag 4    |    Dag 5    |    Totalt    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Befintliga bokningar**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Ny bokning**          |    8        |    8        |    4        |    0        |    0        |    20       |

Metoden med tidigareläggning beaktar befintliga bokningar och tillgänglig kapacitet. Om samma resurs exempelvis redan har 20 timmars bokningar under arbetsveckan kommer nya bokningar att förbruka återstående kapacitet enligt följande:

|                     | Dag 1 | Dag 2 | Dag 3 | Dag 4 | Dag 5 | Totalt |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Befintliga bokningar** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Ny bokning**       | 0     | 0     | 4     | 8     | 8     | 20    |

Eftersom tillgänglig kapacitet beaktas kan det hända att du får ett felmeddelande om resursen inte har någon återstående kapacitet som kan tas upp av bokningen. Med denna metod kan du inte överboka.

### <a name="none"></a><a name="none"></a>Ingen
Metoden Ingen är endast tillgänglig när du bokar från fliken **Team** i ett projekt. Denna metod lägger till resursen som en teammedlem i projektet, men skapar inga bokningar som skulle kunna ta upp resursens kapacitet. Den här metoden används när teammedlemmen som utgör förvald projektledare läggs till när du har skapat ett projekt. Projektledaranvändaren som skapade projektet läggs till som standard i projektet så att projektets entitetspost har en ägare och projektet har en granskare. Om du vill boka resursen kan du - eftersom denna användare inte har några bokningar - antingen ta bort och sedan åter lägga till dem med hjälp av en annan fördelningsmetod, eller också lägga till resursen i aktiviteter och sedan använda **Utöka bokningar** på fliken **Avstämning** för att skapa bokningar för tilldelningarna.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Tilldelningsmetoder som leder till överbokning
Sammanfattningsvis kan följande tilldelningsmetoder medföra överbokning om resursen redan bundits till andra projekt (eller för andra arbetsorder eller schemalagda entiteter):

- Full kapacitet
- Procentandelskapacitet
- Fördela timmar jämnt

När du använder någon av dessa tre tilldelningsmetoder meddelas du inte om resursen överbokas. För att korrigera en överbokning måste du använda schemaläggningstavlan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]