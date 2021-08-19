---
title: Värden
description: Den ämne innehåller information om hur du arbetar med faktiska värden i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a086fe0be67c21ed73793b6f3b58b47ad08eaa4e8a4c98870b4b2264562e3dce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991823"
---
# <a name="actuals"></a>Utfall 

_**Gäller till:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Faktiska värden representerar den granskade och godkända ekonomiska förloppet och schemalägger förloppet för ett projekt. De skapas som ett resultat av godkännande av tid, utgifter, materialanvändningsposter och aktivitetsposter och fakturor.

## <a name="journal-lines-and-time-submission"></a>Journalrader och tidsöverföring

Mer information om tidspost finns i [Översikt över tidspost](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tid och material

När en tidspost som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.

### <a name="fixed-price"></a>Fast pris

När en tidspost som skickas är kopplad till ett projekt som är mappat till en kontraktrad för fast pris skapar systemet en journalrad för kostnad.

### <a name="default-pricing"></a>Standardprissättning

Logiken för att skapa standardpriser finns på journalraden. Fältvärdet från tidsposten kopieras till journalraden. Värdena innehåller datumet för transaktionen, kontraktsraden som projektet är mappat till och valutaresultatet i rätt prislista.

De fält som påverkar standardpriser, t.ex. **Roll** och **Resursenhet** används för att bestämma lämpligt pris på journalraden. Du kan lägga till ett anpassat fält i tidsposten. Om du vill att fältvärdet ska spridas ut till faktiska värden skapar du fältet i tabellerna **Faktiska värden** och **Journalrad**. Använd anpassad kod om du vill föra över det valda fältvärdet från Tidspost till Faktiska värden via raden med hjälp av transaktioners ursprung. Mer information om transaktioners ursprung och anslutningar finns i [Länka faktiska värden till ursprungliga poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Journalrader och grundläggande kostnadsöverföring

Mer information om utgiftspost finns i [Översikt över utgiftspost](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tid och material

När en post för grundläggande utgift som skickas är länkad till ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader, en för kostnad och en för en icke-fakturerad försäljning.

### <a name="fixed-price"></a>Fast pris

När en inlämnad grundläggande utgiftspost är länkad till ett projekt som är mappat till en fast prisavtal, skapar systemet en journalrad för kostnad.

### <a name="default-pricing"></a>Standardprissättning

Logiken för att ange standardpriser för utgifter baseras på utgiftskategorin. Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista. De fält som påverkar standardpriser, t.ex. **Transaktionskategori** och **Resursenhet** används för att bestämma lämpligt pris på journalraden. Detta fungerar emellertid endast om prismodellen i prislistan är **Pris per enhet**. Om prismodellen är **Vid kostnad** eller **Pålägg på kostnad** används det pris som anges när kostnadsposten skapas för kostnad och priset på försäljningsjournalraden beräknas baserat på prissättningsmetoden. 

Du kan lägga till ett anpassat fält i utgiftsposten. Om du vill att fältvärdet ska spridas ut till faktiska värden skapar du fältet i tabellerna **Faktiska värden** och **Journalrad**. Använd anpassad kod om du vill föra över det valda fältvärdet från Tidspost till Faktiska värden via raden med hjälp av transaktioners ursprung. Mer information om transaktioners ursprung och anslutningar finns i [Länka faktiska värden till ursprungliga poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Journalrader och inlämning av materialförbrukningslogg

Mer information om utgiftspost finns i [materialförbrukningslogg](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tid och material

När en inskickad användningsloggpost för material länkas till ett projekt som är mappat till en tids- och materialkontraktrad skapas två faktureringsrader, en för kostnad och en för ofakturerad försäljning.

### <a name="fixed-price"></a>Fast pris

När en inlämnad post för materialförbrukningslogg är länkad till ett projekt som är mappat till en fast prisavtal, skapar systemet en journalrad för kostnad.

### <a name="default-pricing"></a>Standardprissättning

Logiken för att ange standardpriser för material baseras på produkten och enhetskombinationen. Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista. De fält som påverkar standardpriser, t.ex. **Produkt-ID** och **Enhet** används för att bestämma lämpligt pris på journalraden. Detta fungerar emellertid endast för katalogprodukter. För inskrivningsprodukter används priset som angavs när posten för materialanvändningslogg skapades för kostnad och försäljningspris på journalraderna. 

Du kan lägga till ett anpassat fält i posten **Materialförbrukningslogg**. Om du vill att fältvärdet ska spridas ut till faktiska värden skapar du fältet i tabellerna **Faktiska värden** och **Journalrad**. Använd anpassad kod om du vill föra över det valda fältvärdet från Tidspost till Faktiska värden via raden med hjälp av transaktioners ursprung. Mer information om transaktioners ursprung och anslutningar finns i [Länka faktiska värden till ursprungliga poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Använda postjournaler för att registrera kostnader

Du kan använda postjournaler för att registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms. Journaler kan användas för följande ändamål:

- Flytta transaktionsdata från ett annat system till Microsoft Dynamics 365 Project Operations.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
