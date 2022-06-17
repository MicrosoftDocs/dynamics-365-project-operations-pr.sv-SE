---
title: Projektplanera API-resultat
description: Denna artikel innehåller information om API-prestandajämförelser för projektschemat och identifierar metodtips för en optimal användning.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911204"
---
# <a name="project-schedule-api-performance"></a>Projektplanera API-resultat

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier, Lite-distribution - affär med proforma-fakturering, Project for the Web_

Denna artikel innehåller information om prestandajämförelser för programmeringsgränssnitten (API) i projektschemaprogrammet och identifierar metodtips för en optimal användning.

## <a name="project-scheduling-service"></a>Tjänsten för projektscheman
Tjänsten för projektplanering är en tjänst för flera klientorganisationer som körs i Microsoft Azure. Den har utformats för att förbättra interaktionen genom att ge en snabb och smidig upplevelse när användare arbetar med projekt. Förbättringarna sker genom att acceptera ändringsförfrågningar, bearbeta dessa och sedan omedelbart returnera resultatet. Tjänsten finns kvar asynkront för Dataverse och blockerar inte användare från att utföra andra åtgärder.

API:er för projektschemaläggning är beroende av att tjänsten för projektschemaläggning kan köra förfrågningar som beskrivs mer i detalj i senare avsnitt i denna artikel.

API:er för projektscheman är utformade för att fungera med följande entiteter för uppdelad arbetsstruktur (WBS):

  - Project
  - Projektuppgift
  - Beroende för projektuppgift
  - Projektteammedlem
  - Resurstilldelning
  
Både färdiga fält och anpassade fält stöds. Om inget annat anges stöds alla standardåtgärder, till exempel skapa, uppdatera och ta bort. Mer information finns i [Använda API i projektschemat för att utföra åtgärder och schemalägga entiteter](schedule-api-preview.md).

Som en del av API:er i projektschemat har ett arbetsenhetsmönster lagts till. Detta mönster kallas "OperationSet" och kan användas när flera förfrågningar måste bearbetas i en enda transaktion.

I följande illustration illustreras det flöde som en partner kommer att uppleva när denna funktion används.

![Tjänste flöde för Dataverse och projektschemaläggnning.](./media/dataverse-project-scheduling-service-flow.png)

**Steg 1**: En klient utför ett API-anrop till en slutpunkt med Open Data (OData) i Dataverse för att skapa en OperationSet.

**Steg 2**: När nya OperationSet har skapats returneras ett **OperationSetId**-värde.

**Steg 3**: Klienten använder värdet **OperationSetId** för att göra en annan API-förfrågan till projektplaneringen. Resultatet blir en begäran om att skapa, uppdatera eller ta bort en schemaläggningsentitet. När den här förfrågan utförs, sker metadataverifiering. Om valideringen misslyckas avslutas förfrågan, och ett fel returneras.

**Steg 4a–4c**: Dessa steg representerar ACCEPT-fasen. Klienten anropar API **ExecuteOperationSetV1**, som skickar alla ändringar till tjänsten för projektschemaläggning i en enda batch. Tjänsten för projektschemaläggning kör sina egna valideringar i batchen på begäran. Vid valideringsfel ångras batchen och ett undantag returneras till anroparen. Om batchen godkänns av tjänsten för projektplanering uppdateras statusen för OperationSet till att reflektera det faktum att OperationSet bearbetas av tjänsten för projektschemaläggning.

**Steg 5**: Detta steg steget representerar PERSIST-fasen. Tjänsten för projektplanering skriver asynkront bathcen till Dataverse i en transaktion. Om skrivåtgärden slutförs korrekt markeras OperationSet som **Slutförd**. Alla fel återställer transaktionen och batchen, och OperationSet markeras som **Misslyckades**.

## <a name="performance-methodology"></a>Prestandametodik
Körningstiden definieras som tiden från anropet till API:n **ExecuteOperationSetV1** tills tjänsten för projektschemaläggning har slutat skriva till Dataverse. Alla åtgärder körs sammanlagt 2 200 gånger, och måtten för körningstiden för P99 rapporteras. Åtgärder med en enda post samt massåtgärder mäts.

För en åtgärd med en enda post innehåller OperationSet en enda begäran. För massåtgärder innehåller den 20, 50 eller 100 förfrågningar. Varje masstorlek rapporteras separat.

Dessa åtgärder körs på en UR 15 Project Operations Lite-distribution i Nordamerika.

## <a name="results"></a>Resultat
### <a name="create-operations"></a>Skapa åtgärder
#### <a name="single-record-create-operations"></a>Åtgärder för att skapa en enda post
I följande tabell visas körningstiderna för skapandet av en enda post. Tiderna anges i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Post&nbsp;&nbsp;&nbsp;-typ</th>
    <th class="tg-0lax" colspan="2">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Uppgift</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tilldelning</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Beroende</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Åtgärder för mass-skapande
I följande tabell visas körningstiderna för skapandet av många poster. Microsoft har i synnerhet mätt körningstiderna för skapandet av 20, 50 respektive 100 poster i en enda OperationSet. Tiderna anges i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Post&nbsp;&nbsp;&nbsp;-typ</th>
    <th class="tg-0lax" colspan="6">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 poster</th>
    <th class="tg-0lax" colspan="2">50 poster</th>
    <th class="tg-0lax" colspan="2">100 poster</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Uppgift</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tilldelning</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Beroende</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Mass-skapandeåtgärder för entiteterna **Projekt** och **Teammedlem** tas inte med i den här tabellen eftersom körningen för dessa åtgärder liknar körningen när API för att skapa enda enskild post anropas flera gånger. Dessa API:er körs direkt i Dataverse.

I följande illustration visas en ritad bild över körningstiderna för entiteterna **Uppgift**, **Tilldelning** samt **Beroende** då 20, 50 respektive 100 poster skapas och alla fält som stöds används.

![Skapa en tidsgraf för postkörning.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Uppdateringsåtgärder
#### <a name="single-record-update-operations"></a>Uppdateringsåtgärder för att skapa en enda post
I följande tabell visas körningstiderna för uppdatering av en enda post. Tiderna anges i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Post&nbsp;&nbsp;&nbsp;-typ</th>
    <th class="tg-0lax" colspan="2">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriska fält </th>
    <th class="tg-0lax">Alla fält som stöds</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Uppgift</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Uppdateringsåtgärder för entiterna **Resurstilldelningar** och **Projektuppgiftsberoende** stöds inte.

#### <a name="bulk-update-operations"></a>Åtgärder för massuppdatering
I följande tabell visas körningstiderna för uppdateringen av många poster. Microsoft har i synnerhet mätt körningstiderna för uppdatering av 20, 50 respektive 100 poster i en enda OperationSet. Tiderna anges i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Post&nbsp;&nbsp;&nbsp;-typ</th>
    <th class="tg-0lax" colspan="6">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 poster</th>
    <th class="tg-0lax" colspan="2">50 poster</th>
    <th class="tg-0lax" colspan="2">100 poster</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
    <th class="tg-0lax">Obligatoriska fält</th>
    <th class="tg-0lax">Alla fält som stöds</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Uppgift</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Uppdateringsåtgärder för entiterna **Resurstilldelningar** och **Projektuppgiftsberoende** stöds inte.

I följande illustration visas en ritad bild över körningstiderna för entiteterna Uppgift och Teammedlem då 20, 50 respektive 100 poster uppdateras och alla fält som stöds används.

![Uppdatera tidsgraf för postkörning.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Borttagningsåtgärder
#### <a name="single-record-delete-operations"></a>Borttagningsåtgärder för en enda post
I följande tabell visas körningstiderna för borttagning av en enda post. Tiderna anges i sekunder.

| Posttyp | Tid  |
|-------------|-------|
| Uppgift        | 20.12 |
| Tilldelning  | 10.86 |
| Teammedlem | 12.52 |
| Beroende  | 20.89 |

> [!NOTE]
> Borttagningsåtgärder i entiteten **Projekt** stöds inte.

#### <a name="bulk-delete-operations"></a>Massborttagningsåtgärder
I följande tabell visas körningstiderna för borttagning av många poster. Microsoft har i synnerhet mätt körningstiderna för borttagning av 20, 50 respektive 100 poster i en enda OperationSet. Tiderna anges i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Post&nbsp;&nbsp;&nbsp;-typ</th>
    <th class="tg-0lax" colspan="3">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 poster</th>
    <th class="tg-0lax">50 poster</th>
    <th class="tg-0lax">100 poster</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Uppgift</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tilldelning</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlem</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Beroende</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Borttagningsåtgärder i entiteten **Projekt** stöds inte.

I följande illustration visas en ritad bild över körningstiderna för entiteterna **Uppgift**, **Tilldelning**, **Teammedlem** och **Beroende** då 20, 50 respektive 100 poster tas bort.

![Ta bort tidsgraf för postkörning.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observationer
För varje poståtgärd tar API **ExecuteOperationSet** cirka 800 millisekunder för att skicka en förfrågan till tjänsten för projektschemaläggning. Det tar cirka fem sekunder för tjänstne för projektschemaläggning att bearbeta nyttolasten och anropa Dataverse. Resten av körningstiden går åt till att köra affärslogik och skriva data till databasen i Dataverse.

När 100 poster skapas, uppdateras eller tas bort tar det ungefär tre sekunder för API **ExecuteOperationSet** att skicka förfrågan till schemaläggningstjänsten för projektet. Det tar cirka fem sekunder för tjänsten för projektschemaläggning att bearbeta förfrågan och anropa Dataverse. Massåtgärder måste betala en engångsskatt för **tjänsten för projektschemaläggning** för samtliga poster i OperationSet. Därför har massåtgärder en betydligt kortare genomsnittlig körningstid än åtgärder med en enda post.

## <a name="scenarios"></a>Scenarion
I följande tabell visas körningstiderna när API:er för projektschema används för att utföra specifika scenarier. Tiderna anges i sekunder.

| Scenario                                                                   | Tid  |
|----------------------------------------------------------------------------|-------|
| Skapa ett projekt med 40 uppgifter.                                      | 36.01 |
| Skapa ett projekt med 40 uppgifter och 20 beroenden.                  | 38.11 |
| Skapa ett projekt med 40 uppgifter och 30 tilldelningar.                   | 60.17 |
| Skapa ett projekt med 40 uppgifter, 20 beroenden och 30 tilldelningar. | 60.27 |

## <a name="best-practices"></a>Metodtips
Utifrån resultaten av det föregående scenariot presterar API:erna bättre under följande villkor:

  - Gruppera ihop så många åtgärder som möjligt. Den genomsnittliga körningen för massåtgärder är bättre än den genomsnittskörning som har körts för åtgärder med en enda post. Ju mindre antal OperationSets som används, desto snabbare blir den genomsnittliga körningstiden.
  - Ange endast de minimiattribut som krävs för att du ska kunna utföra ditt scenario. Var selektiv i fråga om de typer av fält som inte krävs men som ingår i en OperationSet-förfrågan. Fält som innehåller externa nycklar eller sammanslagningsfält påverkar prestandan negativt.
