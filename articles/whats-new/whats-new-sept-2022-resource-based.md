---
title: Nyheter september 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i september 2022-versionen av Microsoft Dynamics 365 Project Operations för resurs-/icke-lagerbaserade scenarier.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634828"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter september 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.46.0.60
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.29

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

| Funktionsområde | Funktionsnamn | Mer information |
| --- | --- | --- |
| Administrering av affärsmöjligheter | **Revision och aktivering av offerter**<br>Med Project Operations får försäljningsprocessen fullt stöd. Projektofferter kan aktiveras så att de motsvarar ett tillstånd där offerten är skrivskyddad och granskas. Aktiverade offerter kan revideras för att skapa nya offerter med ett stegvis revisionsnummer. Aktiverade projektofferter eller offertrevisioner kan stängas som vunna eller förlorade. | [Aktivera och revidera en projektoffert](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturering och prissättning | **Tidszonens agnostiska pris är standard**<br>Project Operations har introducerat konceptet med ett tidszon agnostiskt datum för alla projektets faktiska värden. Ett nytt fält, **Transaktionsdatum**, är nu tillgängligt på rader och faktiska värden och används för att lagra datumet då transaktionen inträffade, men utan att konvertera det datumet till Coordinated Universal Time. Det här datumet används i processer nedströms, till exempel för standardpris och skapande av fakturor. | <p>[Avgör kostnadstaxa för projektbaserade beräkningar och utfall](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Fastställa försäljningspriser för projektbaserade beräkningar och utfall](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fakturering och prissättning | **Datum då priset ska gälla åsidosätts i Project Operations**<br>Datumspecifika prisändringar är ett sätt att åsidosätta eller ändra specifika priser i prislistan. | [Datumspecifika prisändringar](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Legotillverkning | **Förfakturering av underleverantör och leverantörsfaktura**<br>Med den här funktionen kan kunderna skapa underleverantörer för att köpa resurstid, utgiftskategorier och material som används för projektarbete. Det gör det även möjligt för kunder att registrera, i appar för ekonomi och drift, leverantörsfakturor som ska vara tillgängliga för projektansvariga för Dataverse-verifiering. | <p>[Underleverantörshantering](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Skapa leverantörsfakturor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tid och utgift | **Global godkännare**<br>Med den här funktionen kan oberoende ISV (programvaruleverantör) och centraliserat godkännande aktiveras, oavsett projekt- eller teammedlemsstatus i projektet. | [Säkerhet och godkännanden](/dynamics365/project-operations/approvals/approvals-security) |
| Utgiftshantering | **Möjlighet att publicera utgiftsansvar i leverantörsvaluta**<br>Denna funktion gör det möjligt att bokföra utgiftsrapporter i en leverantörsvaluta för kontantbetalningsmetoden. | [Möjlighet att publicera utgiftsansvar i leverantörsvaluta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektupphandling | **Använd betalning av leverantör vid betalning**<br>Med den här funktionen kan du använda funktionen Betala när betald (PWP) används i andra miljöer än lager i Project Operations. Det gör att leverantörsbetalningarna kan blockeras/bevaras, baserat på lagringsvillkor, tills betalningen tas emot från kunden. | [Använd betalning av leverantör vid betalning](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektupphandling | **Inköpsrekvisitioner för ett projekt**<br>Med den här funktionen kan användare skapa projektrelaterade köporder i juridiska entiteter där Project Operations på Dynamics 365 Customer Engagement-integrering har aktiverats. Projektinköpsorder kan användas för att registrera icke-lager materialanskaffning mot projektet av inköpsavdelningens profil. Projektinköpsorder synkroniseras inte med Dataverse. Du kan emellertid använda en virtuell entitet för att ytbehandla projektorderraderna i Dataverse för att få information om projektledare. Projektrelaterad leverantörsfakturakostnad integreras med entiteten projektets faktiska värden i Dataverse. Projektkostnaden registreras i projektreskontran med hjälp av integreringsjournalen för Project Operations. | |
|Projektplanering och spårning|**Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter** </br> </br>Med redigerings-API:t för resurstilldelningsredigering kan utvecklare programmässigt ange en uppgiftstilldelningsobjekts insats i alla datumintervall som stöds för en mer detaljerad planering av tidsfasad insats.|[Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

I följande tabell visas mappningar med dubbelskrivning som har ändrats eller lagts till i september 2022-versionen av Project Operations.

| Entitetsmappning | Uppdaterad version | Kommentarer |
| -------------- | ------------------- | ------------|
| Faktiska värden för Project Operations-integration (msdyn_actuals) | 1.0.0.15 | Den här mappningen stöder underleverantörs faktiska värden som bearbetas med Project Operations för resursbaserade scenarier. |
| Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices) | 1.0.0.2 | Den här mappningen stöder underleverantörs faktiska värden som bearbetas med Project Operations för resursbaserade scenarier. |
| Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Den här mappningen stöder underleverantörs faktiska värden som bearbetas med Project Operations för resursbaserade scenarier. |

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Fakturering och prissättning | 2754422 | Material och kostnader för förs inte över till ekonomi när projekt kopieras i Dataverse. |
| Tid och utgift | 2787409 | En icke-giltig godkännare kan godkänna en icke-projekttidspost. |
| Administrering av affärsmöjligheter | 2788907 | Uppdaterat felmeddelande om unique validation för orderrader som innehåller flaggar. |
| Tid och utgift | 2842253 | Null-undantagshantering för tidsgodkännande. |
| Fakturering och prissättning | 2844181 | Misslyckande att få korrelations-ID blockerar fakturaskapande. |
| Fakturering och prissättning | 2876628 | QLD, CLD – Beräkna prislistematchning bör använda tidigare datumintervallfält i prislistan. |
| Legotillverkning | 2893222 | Om ingen roll har angetts för en underleverantörsrad bör det vara möjligt att välja den raden på en teammedlem för alla roller. |

### <a name="project-management-and-accounting-in-finance"></a>Projektledning och redovisning i Ekonomi

Om du vill ha information om felkorrigeringar som ingår i denna uppdatering loggar du in på Microsoft Dynamics Lifecycle Services och visar [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funktioner aktiveras som standard i kommande version

Följande tabeller listar de funktioner som aktiveras som standard i version 10.0.30. De flesta funktioner som har aktiverats automatiskt kan inaktiveras i [Funktionshantering](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). I framtiden kan vissa funktioner som har aktiverats automatiskt tas bort från funktionshanteringen och bli obligatoriska. Den här förändringen säkerställer att kunderna använder aktuella funktioner så att förbättringarna kan bygga på den aktuella funktionen när de läggs till. Funktioner aktiveras aldrig automatiskt på mindre än ett år, såvida de inte är nödvändiga.

| Funktionsnamn | Aktiveringsdatum | Funktion som lagts till | Funktionens tillstånd | Modul |
| --- | --- | --- |--- |--- |
| Aktivera asynkron åtgärd när användaren behöver växla mellan synkronisering och asynkrona åtgärder | 21 oktober 2022 | 9 april 2021 | På som standard | Utgiftshantering |
| Utvärdering av kostnadspolicyn för obligatoriska kostnader | 21 oktober 2022 | 20 december 2021 | På som standard | Utgiftshantering |
| Listvy över utgiftsrapporter som skapats genom att delegera medarbetare | 21 oktober 2022 | 19 februari 2020 | På som standard | Utgiftshantering |
| Beräkning av totalsummor för körklart antal räkenskapsår | 21 oktober 2022 | 10 maj 2022 | På som standard | Utgiftshantering |
