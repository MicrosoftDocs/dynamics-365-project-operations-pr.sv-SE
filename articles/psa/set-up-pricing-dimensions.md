---
title: Konfigurera anpassade fält som prissättningsdimensioner
description: I den här artikeln finns information om hur du ställer in anpassade prissättningsdimensioner.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 14d27b53b42744d47e298bf5a926c1262dbf44d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922619"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Konfigurera anpassade fält som prissättningsdimensioner 

[!include [banner](../includes/psa-now-project-operations.md)]

Innan du börjar förutsätter den här artikeln att du har slutfört procedurerna i artiklar [Skapa anpassade fält och entiteter](create-custom-fields-entities.md) och [Lägg till anpassade fält till prisinställningar och transaktionsenheter](field-references.md). Om du inte har slutfört de här procedurerna går du tillbaka och slutför dem och går sedan tillbaka till artikeln. 

I den här artikeln finns information om hur du ställer in anpassade prissättningsdimensioner. I webbgränssnittet Project Service på sidan **Parametrar** visar fliken **Beloppsbaserade prissättningsdimensioner** posterna i entiteterna för prissättningsdimensioner. Som standard skapar installation av Project Service 2 rader i rutnätet på den här fliken:

- **msdyn_resourcecategory** (roll)
- **msdyn_OrganizationalUnit** (organisationsenhet)

> [!IMPORTANT]
> Ta inte bort de här raderna. Om du inte behöver dem kan du emellertid välja att inte använda dem i en specifik kontext genom att ange **Gäller för kostnad**, **Gäller för försäljning** och **Gäller för inköp** till **Nej**. Genom att ange dessa attributvärden till **Nej** fås inte samma effekt som en prissättningsdimension.

För att ett fält ska bli en prissättningsdimension måste det vara:

- Skapat som ett fält i entiteterna **Rollpris** och **Pålägg för rollpris**. Mer information om hur du gör detta finns i [lägga till anpassade fält i prisinställningar och transaktionella entiteter](field-references.md).
- Skapad som en rad i tabellen **prisdimension**. Du kan till exempel lägga till prisdimensionsrader som de visas i följande bild. 

![Beloppsbaserade prissättningsrader.](media/Amt-based-PD.png)

Observera att that resursens arbetstider (**msdyn_resourceworkhours**) har lagts till som en kodtyp och att de har lagts till i rutnätet på fliken **Påläggsbaserad prissättningsdimension**.

![Påläggsbaserade prissättningsdimensionsrader.](media/Markup-based-PD.png)

> [!IMPORTANT]
> Alla ändringar av dimensionsdata för prissättning i den här tabellen, befintlig eller ny, sprids till Project Service affärslogik för prissättnings först efter att cacheminnet har uppdaterats. Det kan ta upp till 10 minuter att uppdatera cacheminnet. Tillåt den här tidsperioden för att se de ändringar i prisstandardlogik som måste uppkomma från ändringar i data för prissättningsdimension.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attribut för prissättningsdimensionstabellen
I följande avsnitt finns information om de olika attributen i tabellen **prissättningsdimensioner**.

### <a name="pricing-dimension-name"></a>Namn på prissättningsdimension
Värdet ska vara exakt samma som schemanamnet för fältet som läggs till i tabellen **rollpris** för anpassade prissättningsdimensioner. Mer information om hur du lägger till fält i tabellen **rollpris** se [Lägg till anpassade fält i prisinställningar och transaktionella entiteter](field-references.md).

### <a name="type-of-dimension"></a>Typ av dimension
Det finns två typer av prissättningsdimensioner:
  
  - **Beloppsbaserade dimensioner**: dimensionsvärdena från inmatningskontexten matchas mot dimensionsvärdena på raden **rollpris** och priset/kostnaden är standardvärdet i tabellen **rollpris**.
  - **Påläggsbaserade dimensioner**: Detta är dimensioner där Project Service kommer att anta följande trestegsprocess för att ta fram pris/kostnad
 
    1. Project Service matchar de icke påläggsbaserade dimensionsvärdena från inmatningskontexten till rollprisraden för att uppnå grundpriset.
    2. Project Service matchar alla dimensionsvärdena från inmatningskontexten till **Pålägg för rollpris** för att uppnå pålägg i procent.
    3. Project Service använder procentuellt pålägg från det andra steget till grundpriset som fås från tabellen **rollpris** i det första steget för att nå slutligt pris/kostnad.
   
   I följande tabell visas beräkningen av Pålägg för pris.
  
| Roll        | Organisationsenhet    |Arbetsplats      |Standardrubrik      |Arbetstid för resurs      |  Pålägg|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|På plats            |                    |Övertid                 |15     |
|             | Contoso India|Lokal             |                    |Övertid                 |10     |
|             | Contoso US   |Lokal             |                    |Övertid                 |20     |


Om en resurs från Contoso India vars grundpris är 100 USD arbetar på plats och de loggar 8 timmar regelbundet och 2 timmar övertid i tidsposten använder Project Service baspriset på 100 under åtta timmar för att registrera 800 USD. För två timmars övertid beräknas ett pålägg på 15 % på baspriset på 100 för att få ett enhetspris på 115 USD och registrera en totalkostnad på 230 USD.

### <a name="applicable-to-cost"></a>Gäller för kostnad 
Om värdet är angivet till **ja** anger det att dimensionsvärdet från inmatningskontexten ska användas för att matcha **rollpriset** och **pålägg för rollpris** när kostnads- och påläggspriserna hämtas.

### <a name="applicable-to-sales"></a>Gäller för försäljning
Om värdet är angivet till **ja** anger det att dimensionsvärdet från inmatningskontexten ska användas för att matcha **rollpriset** och **pålägg för rollpris** när fakturerings- och påläggspriserna hämtas.

### <a name="applicable-to-purchase"></a>Gäller för inköp
Om värdet är angivet till **ja** anger det att dimensionsvärdet från inmatningskontexten ska användas för att matcha **rollpriset** och **pålägg för rollpris** när inköpspriset hämtas. För närvarande har Project Service inte stöd för scenarier med underleverantörskap så det här fältet används inte. 

### <a name="priority"></a>Prioritet
Genom att ange dimensionsprioriteten kan Project Service producera ett pris även om det inte går att hitta en exakt matchning mellan värdena för indata och värdena för tabellerna **Rollpris** eller **Pålägg för rollpris**. I det här scenariot använder Project Service null-värden för omatchade dimensionsvärden genom vägning av dimensionerna i prioritetsordning.

- **Kostnadsprioritet**: värdet för dimensionens kostnadsprioritet anger vikten av dimensionen när den matchas mot inställningarna av självkostnader. Värdet för **kostnadsprioritet** måste vara unikt mellan de dimensioner som **gäller för kostnaden**.
- **Försäljningsprioritet**: värdet för dimensionens försäljningsprioritet anger vikten av dimensionen när den matchas mot inställningarna av försäljningspris eller faktureringskostnader. Värdet för **försäljningsprioritet** måste vara unikt mellan de dimensioner som **gäller för försäljning**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
