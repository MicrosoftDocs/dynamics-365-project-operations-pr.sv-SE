---
title: Översikt över värden
description: I det här ämnet finns information om projektets faktiska värden.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
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
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368183"
---
# <a name="actuals-overview"></a>Översikt över värden

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faktiska värden är den mängd arbete som har slutförts i ett projekt. Projektets faktiska värden kan spåras tillbaka till källdokumenten. Dessa källdokument innehåller både tid, utgift och journaltransaktioner samt fakturor.

![Så här spåras projektets faktiska resultat till källdokument](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Skicka tidspost

I PSA när en tidspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader. En rad är för kostnad och den andra raden är för ofakturerad försäljning. När en tidspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad. 

Logik för att ange standardpriser finns på journalraden. Alla fältvärden från en tidspost kopieras till journalraden. Fälten innehåller datumet för transaktionen, kontraktraden som projektet är mappat till och valutaresultatet i rätt prislista. 

De fält som påverkar standardpriser, t.ex. **Roll** och **Organisatinsenhet** gör att ett korrekt pris anges som standard på journalraden. Om du lägger till ett anpassat fält i tidsposten och du vill att fältvärdet ska spridas till faktiska värden, skapar du fältet på entiteten faktiska värden och använder fältmappningar för att kopiera fältet från tidsposten till det faktiska värdet.

## <a name="submitting-an-expense-entry"></a>Skicka en utgiftspost

I PSA när en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för tid och material skapas två journalrader. En rad är för kostnad och den andra raden är för ofakturerad försäljning. När en utgiftspost skickas för ett projekt som är mappat till en kontraktrad för fast pris skapas endast en journalrad för kostnad.

Logik för att ange standardpriser för utgifter baseras på den utgiftskategori som är vald på sidan **utgiftspost**. Datumet för transaktionen, kontraktraden som projektet är mappat till och valutan används för att bestämma rätt prislista. För själva priset anges emellertid det belopp som användaren har angett direkt på de relaterade utgiftsjournalraderna för kostnad och försäljning som standard.

I den aktuella versionen av PSA är kategoribaserade poster av per enhet standardpriser på utgiftposter inte tillgängliga.

## <a name="using-entry-journals-to-record-costs"></a>Använda postjournaler för att registrera kostnader

I PSA kan du med hjälp av postjournaler registrera kostnader eller intäkter i transaktionsklasserna material, avgift, tid, utgift eller moms. En journal har ett huvud, rader och en **Bekräfta**-åtgärd. Här följer några scenarier där du kan använda en journal:

- Du måste registrera materialets faktiska kostnader och försäljning i ett projekt.
- Du måste flytta faktiska värden för transaktioner från ett annat system till PSA.
- Du måste registrera kostnader som inträffat i ett annat system, t.ex. inköp eller legotillverkningskostnader.

> [!IMPORTANT]
> Att använda postjournaler för att skapa verkliga värden ska endast utföras av en användare som är helt medveten om den redovisning som påverkar de faktiska värdena för projektet. Detta beror på att programmet inte validerar journalradtypen eller den relaterade prissättningen som har angetts på journalraden. På grund av den här journaltypens påverkan bör du vara försiktig med att få tillgång till skapa postjournaler.     


## <a name="recording-actuals-based-on-project-events"></a>Registrera faktiska värden baserat på projekthändelser

PSA registrerar ekonomiska transaktioner som inträffar under ett projekt. Dessa transaktioner registreras som **faktiska värden**. I följande tabell visas de olika typerna av faktiska värden som skapas, beroende på om projektet är ett tids- och materiallager, fast pris-projekt eller om det är i stadiet för försäljning eller ett internt projekt.

**Resursen tillhör samma organisationsenhet som projektets avtalade enhet**

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

**Resursen tillhör en organisationsenhet som skiljer sig från projektets avtalade enhet**

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