---
title: Konfigurera anpassade fält som prissättningsdimensioner
description: I det här ämnet finns information om hur du ställer in prissättningsdimensioner med anpassade fält.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 744c561d023d7ef5ed79947e69f2de8a3902fb41
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650250"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Konfigurera anpassade fält som prissättningsdimensioner

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Innan du börjar förutsätter det här ämnet att du har slutfört procedurerna i avsnitten [Skapa anpassade fält och entiteter](create-custom-fields-entities-pricing-dimensions.md) och [Lägg till önskade anpassade fält till prisinställningar och transaktionsenheter](add-custom-fields-price-setup-transactional-entities.md). Om du inte har slutfört de här procedurerna går du tillbaka och slutför dem och går sedan tillbaka till ämne. 

I det här ämnet finns information om hur du ställer in anpassade prissättningsdimensioner. På sidan **Parametrar** visar fliken **Beloppsbaserade prissättningsdimensioner** visar posterna i enheterna för prisdimension. Som standard finns det två rader i rutnätet på den här fliken:

- **msdyn_resourcecategory** (roll)
- **msdyn_OrganizationalUnit** (organisationsenhet)

> [!IMPORTANT]
> Ta inte bort de här raderna. Om du inte behöver dem kan du emellertid välja att inte använda dem i en specifik kontext genom att ange **Gäller för kostnad**, **Gäller för försäljning** och **Gäller för inköp** till **Nej**. Genom att ange dessa attributvärden till **Nej** fås inte samma effekt som en prissättningsdimension.

För att ett fält ska bli en prissättningsdimension måste det vara:

- Skapat som ett fält i entiteterna **Rollpris** och **Pålägg för rollpris**. Mer information om hur du gör detta finns i [lägga till anpassade fält i prisinställningar och transaktionella entiteter](add-custom-fields-price-setup-transactional-entities.md).

- Skapad som en rad i tabellen **prisdimension**. Du kan till exempel lägga till prisdimensionsrader som de visas i följande bild. 

![Beloppsbaserade prissättningsrader](media/Amt-based-PD.png)

Resursens arbetstider (**msdyn_resourceworkhours**) har lagts till som en kodtyp och att de har lagts till i rutnätet på fliken **Påläggsbaserad prissättningsdimension**.

![Påläggsbaserade prissättningsdimensionsrader](media/Markup-based-PD.png)


> [!IMPORTANT]
> Alla ändringar av dimensionsdata för prissättning i den här tabellen, befintlig eller ny, sprids till affärslogik för prissättnings först efter att cacheminnet har uppdaterats. Det kan ta upp till 10 minuter att uppdatera cacheminnet. Tillåt den här tidsperioden för att se de ändringar i prisstandardlogik som måste uppkomma från ändringar i data för prissättningsdimension.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attribut för prissättningsdimensionstabellen
I följande avsnitt finns information om de olika attributen i tabellen **prissättningsdimensioner**.

### <a name="pricing-dimension-name"></a>Namn på prissättningsdimension
Värdet ska vara exakt samma som schemanamnet för fältet som läggs till i tabellen **rollpris** för anpassade prissättningsdimensioner. Mer information om hur du lägger till fält i tabellen **rollpris** se [Lägg till anpassade fält i prisinställningar och transaktionella entiteter](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Typ av dimension
Det finns två typer av prissättningsdimensioner:
  
  - **Beloppsbaserade dimensioner**: dimensionsvärdena från inmatningskontexten matchas mot dimensionsvärdena på raden **rollpris** och priset/kostnaden är standardvärdet i tabellen **rollpris**.
  - **Påläggsbaserade dimensioner**: Detta är dimensioner där kommer att anta trestegsprocess för att ta fram pris/kostnad
 
    1. De icke påläggsbaserade dimensionsvärdena från inmatningskontexten matchas till rollprisraden för att uppnå grundpriset.
    2. Dimensionsvärdena från inmatningskontexten matchas till **Pålägg för rollpris** för att uppnå pålägg i procent.
    3. Det procentuella pålägget från det andra steget tillämpas på grundpriset som fås från tabellen **rollpris** i det första steget för att nå slutligt pris/kostnad.
   
   I följande tabell visas beräkningen av Pålägg för pris.
  
| Roll        | Organisationsenhet    |Arbetsplats      |Standardrubrik      |Arbetstid för resurs      |  Pålägg|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|På plats            |                    |Övertid                 |15     |
|             | Contoso India|Lokal             |                    |Övertid                 |10     |
|             | Contoso US   |Lokal             |                    |Övertid                 |20     |


Om en resurs från Contoso India vars grundpris är 100 USD arbetar på plats och de loggar 8 timmar regelbundet och 2 timmar övertid i tidsposten använder baspriset på 100 under åtta timmar för att registrera 800 USD. För två timmars övertid beräknas ett pålägg på 15 % på baspriset på 100 för att få ett enhetspris på 115 USD och registrera en totalkostnad på 230 USD.

### <a name="applicable-to-cost"></a>Gäller för kostnad 
Om värdet är angivet till **ja** anger det att dimensionsvärdet från inmatningskontexten ska användas för att matcha **rollpriset** och **pålägg för rollpris** när kostnads- och påläggspriserna hämtas.

### <a name="applicable-to-sales"></a>Gäller för försäljning
Om värdet är angivet till **ja** anger det att dimensionsvärdet från inmatningskontexten ska användas för att matcha **rollpriset** och **pålägg för rollpris** när fakturerings- och påläggspriserna hämtas.

### <a name="applicable-to-purchase"></a>Gäller för inköp
Om värdet är angivet till **ja** anger det att dimensionsvärdet från inmatningskontexten ska användas för att matcha **rollpriset** och **pålägg för rollpris** när inköpspriset hämtas. Scenarier med underleverantörskap stöds inte och därför används inte det här fältet. 

### <a name="priority"></a>Prioritet
Genom att ange dimensionsprioriteten kan producera ett pris även om det inte går att hitta en exakt matchning mellan värdena för indata och värdena för tabellerna **Rollpris** eller **Pålägg för rollpris**. I det här scenariot använder null-värden för omatchade dimensionsvärden genom vägning av dimensionerna i prioritetsordning.

- **Kostnadsprioritet**: värdet för dimensionens kostnadsprioritet anger vikten av dimensionen när den matchas mot inställningarna av självkostnader. Värdet för **kostnadsprioritet** måste vara unikt mellan de dimensioner som **gäller för kostnaden**.
- **Försäljningsprioritet**: värdet för dimensionens försäljningsprioritet anger vikten av dimensionen när den matchas mot inställningarna av försäljningspris eller faktureringskostnader. Värdet för **försäljningsprioritet** måste vara unikt mellan de dimensioner som **gäller för försäljning**.
