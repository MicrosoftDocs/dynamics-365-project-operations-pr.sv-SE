---
title: Värden
description: I det här ämne finns information om hur du arbetar med verkliga värden i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085530"
---
# <a name="actuals"></a>Faktiska värden 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Faktiska värden är den mängd arbete som har slutförts i ett projekt. De skapas som ett resultat av tids- och utgiftsposter samt journalposter och fakturor.

## <a name="journal-lines-and-time-submission"></a>Journalrader och tidsöverföring

Mer information om tidspost finns i [Översikt över tidspost](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tid och material

När en tidspost som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.

### <a name="fixed-price"></a>Fast pris

När en tidspost som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.

### <a name="default-pricing"></a>Standardprissättning

Logiken för att skapa standardpriser finns på journalraden. Fältvärdet från tidsposten kopieras till journalraden. Värdena innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.

De fält som påverkar standardpriser, t.ex. **Roll** och **Organisationsenhet** används för att fastställa korrekt pris på journalraden. Du kan lägga till ett anpassat fält i tidsposten. Om du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten Faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.

## <a name="journal-lines-and-basic-expense-submission"></a>Journalrader och grundläggande kostnadsöverföring

Mer information om utgiftspost finns i [Översikt över utgiftspost](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tid och material

När en post för grundläggande utgift som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.

### <a name="fixed-price"></a>Fast pris

När en post för grundläggande utgift som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.

### <a name="default-pricing"></a>Standardprissättning

Logiken för att ange standardpriser för utgifter baseras på utgiftskategorin. Datumet för transaktionen, kontraktsraden som projektet är mappat till och valutan används för att bestämma rätt prislista. För själva priset anges emellertid som standard det belopp som har angetts direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning.

Kategoribaserade poster av standardpriser per enhet på utgiftposter är inte tillgängliga.

## <a name="use-entry-journals-to-record-costs"></a>Använda postjournaler för att registrera kostnader

Du kan använda postjournaler för att registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms. Journaler kan användas för följande ändamål:

- Registrera materialets faktiska kostnader och försäljning i ett projekt.
- Flytta faktiska värden för transaktioner från ett annat system till Microsoft Dynamics 365 Project Operations.
- Registrera kostnader som har inträffat i ett annat system. Kostnaderna kan vara anskaffnings- eller underleverantörskostnader.

> [!IMPORTANT]
> Programmet verifierar inte journalradtypen eller den relaterade prissättningen som har angetts på journalraden. Därför bör endast en användare som är helt medveten om redovisningseffekten som faktiska värden har på projektet använda sig av postjournaler för att skapa verkliga värden. På grund av den här journaltypens inverkan bör du noggrant välja vem som har åtkomst till att skapa postjournaler.
## <a name="record-actuals-based-on-project-events"></a>Registrera faktiska värden baserat på projekthändelser

Project Operations registrerar ekonomiska transaktioner som inträffar under ett projekt. Dessa transaktioner registreras som faktiska värden. I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Resursen tillhör samma organisationsenhet som projektets avtalade enhet

<table>
<thead>
<tr>
<th rowspan="3">Händelse</th>
<th colspan="4">Fakturerbart eller sålt projekt</th>
<th rowspan="3">Projekt i stadiet för försäljning</th>
<th rowspan="3">Internt projekt</th>
</tr>
<tr>
<th colspan="2">Tid och material</th>
<th colspan="2">Fast pris</th>
</tr>
<tr>
<th>Faktiska värden</th>
<th>Transaktionsvaluta</th>
<th>Fast pris</th>
<th>Transaktionsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>En tidspost skapas.</td>
<td colspan="6">Ingen aktivitet i entiteten för faktiska värden</td>
</tr>
<tr>
<td>En tidspost skickas.</td>
<td colspan="6">Ingen aktivitet i entiteten för faktiska värden</td>
</tr>
<tr>
<td rowspan="2">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</td>
<td>Faktisk kostnad</td>
<td>Valuta för avtalande enhet</td>
<td rowspan="2">Faktisk kostnad</td>
<td rowspan="2">Valuta för avtalande enhet
<td rowspan="2">Faktisk kostnad</td>
<td rowspan="2">Faktisk kostnad</td>
</tr>
<tr>
<td>Ofakturerad faktiskt försäljning - debiterbart</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="3">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</td>
<td>Faktisk kostnad</td>
<td>Valuta för avtalande enhet</td>
<td rowspan="3">Faktisk kostnad</td>
<td rowspan="3">Valuta för avtalande enhet</td>
<td rowspan="3">Faktisk kostnad</td>
<td rowspan="3">Faktisk kostnad</td>
</tr>
<tr>
<td>Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="2">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</td>
<td>Ofakturerad återförd försäljning</td>
<td>Projektkontraktets valuta</td>
<td rowspan="2">Fakturerad försäljning för milstolpe</td>
<td rowspan="2">Projektkontraktets valuta</td>
<td rowspan="2">Saknas</td>
<td rowspan="2">Saknas</td>
</tr>
<tr>
<td>Fakturerad försäljning</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="3">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</td>
<td>Ofakturerad återförd försäljning</td>
<td>Projektkontraktets valuta</td>
<td rowspan="3">Saknas</td>
<td rowspan="3">Saknas</td>
<td rowspan="3">Saknas</td>
<td rowspan="3">Saknas</td>
</tr>
<tr>
<td>Fakturerad försäljning - debiterbar för den nya kvantiteten</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Fakturerad försäljning - icke-debiterbar för skillnaden</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="2">En faktura korrigeras för att öka det debiterbara antalet.</td>
<td>Fakturerad försäljning - återförd</td>
<td>Projektkontraktets valuta</td>
<td rowspan="5">
<ul>
<li>Fakturerad återförd försäljning för milstolpe</li>
<li>Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></li>
</ul>
</td>
<td rowspan="5">Projektkontraktets valuta</td>
<td rowspan="5">Saknas</td>
<td rowspan="5">Saknas</td>
</tr>
<tr>
<td>Fakturerad försäljning</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="3">En faktura korrigeras för att minska det debiterbara antalet.</td>
<td>Fakturerad försäljning - återförd</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Fakturerad försäljning för den nya kvantiteten</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Ofakturerad försäljning - debiterbar för skillnaden</td>
<td>Projektkontraktets valuta</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet

<table>
<thead>
<tr>
<th rowspan="3">Händelse</th>
<th colspan="4">Fakturerbart eller sålt projekt</th>
<th rowspan="3">Projekt i stadiet för försäljning</th>
<th rowspan="3">Internt projekt</th>
</tr>
<tr>
<th colspan="2">Tid och material</th>
<th colspan="2">Fast pris</th>
</tr>
<tr>
<th>Faktiska värden</th>
<th>Transaktionsvaluta</th>
<th>Fast pris</th>
<th>Transaktionsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>En tidspost skapas.</td>
<td colspan="6">Ingen aktivitet i entiteten för faktiska värden</td>
</tr>
<tr>
<td>En tidspost skickas.</td>
<td colspan="6">Ingen aktivitet i entiteten för faktiska värden</td>
</tr>
<tr>
<td rowspan="4">Tiden godkänns och inga ändringar i eller ökningar av fakturerbara timmar inträffar under godkännandet.</td>
<td>Faktisk kostnad</td>
<td>Valuta för avtalande enhet</td>
<td rowspan="4">Faktisk kostnad</td>
<td rowspan="4">Valuta för avtalande enhet</td>
<td rowspan="4">Faktisk kostnad</td>
<td rowspan="4">Faktisk kostnad</td>
</tr>
<tr>
<td>Ofakturerad faktiskt försäljning - debiterbart</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Kostnad för resursenhet</td>
<td>Valuta för resursenhet</td>
</tr>
<tr>
<td>Försäljning inom organisationen</td>
<td>Valuta för avtalande enhet</td>
</tr>
<tr>
<td rowspan="5">Tiden godkänns och minska i fakturerbara timmar inträffar under godkännandet.</td>
<td>Faktisk kostnad</td>
<td>Valuta för avtalande enhet</td>
<td rowspan="5">Faktisk kostnad</td>
<td rowspan="5">Valuta för avtalande enhet</td>
<td rowspan="5">Faktisk kostnad</td>
<td rowspan="5">Faktisk kostnad</td>
</tr>
<tr>
<td>Kostnad för resursenhet</td>
<td>Valuta för resursenhet</td>
</tr>
<tr>
<td>Försäljning inom organisationen</td>
<td>Valuta för avtalande enhet</td>
</tr>
<tr>
<td>Ofakturerad faktiskt försäljning - debiterbar för den nya kvantiteten</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Ofakturerad faktiskt försäljning - icke-debiterbar för skillnaden</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="2">En faktura bekräftas och inga ändringar i eller ökningar av fakturerbara timmar inträffar.</td>
<td>Ofakturerad återförd försäljning</td>
<td>Projektkontraktets valuta</td>
<td rowspan="2">Fakturerad försäljning för milstolpe</td>
<td rowspan="2">Projektkontraktets valuta</td>
<td rowspan="2">Saknas</td>
<td rowspan="2">Saknas</td>
</tr>
<tr>
<td>Fakturerad försäljning</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="3">En faktura bekräftas och en ökning av fakturerbara timmar inträffar.</td>
<td>Ofakturerad återförd försäljning</td>
<td>Projektkontraktets valuta</td>
<td rowspan="3">Saknas</td>
<td rowspan="3">Saknas</td>
<td rowspan="3">Saknas</td>
<td rowspan="3">Saknas</td>
</tr>
<tr>
<td>Fakturerad försäljning - debiterbar för den nya kvantiteten</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Fakturerad försäljning - icke-debiterbar för skillnaden</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="2">En faktura korrigeras för att öka det debiterbara antalet.</td>
<td>Fakturerad försäljning - återförd</td>
<td>Projektkontraktets valuta</td>
<td rowspan="5">
<ul>
<li>Fakturerad återförd försäljning för milstolpe</li>
<li>Ändra status för milstolpe från <strong>fakturerad</strong> till <strong>klar för faktura</strong></li>
</ul>
</td>
<td rowspan="5">Projektkontraktets valuta</td>
<td rowspan="5">Saknas</td>
<td rowspan="5">Saknas</td>
</tr>
<tr>
<td>Fakturerad försäljning</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td rowspan="3">En faktura korrigeras för att minska det debiterbara antalet.</td>
<td>Fakturerad försäljning - återförd</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Fakturerad försäljning för den nya kvantiteten</td>
<td>Projektkontraktets valuta</td>
</tr>
<tr>
<td>Ofakturerad försäljning - debiterbar för skillnaden</td>
<td>Projektkontraktets valuta</td>
</tr>
</tbody>
</table>
