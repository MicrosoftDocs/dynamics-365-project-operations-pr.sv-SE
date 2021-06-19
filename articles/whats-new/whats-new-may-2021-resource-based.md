---
title: Nyheter i maj 2021 – Project Operations för resursscenarier/icke lagerbaserade scenarier
description: Det här ämnet innehåller information om kvalitetsuppdateringarna som är tillgängliga i maj 2021-versionen av Project Operations för resurs-/ej lagerbaserade scenarier.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07ae18faef6acb9d64b889bbfdba89de0c96a453
ms.sourcegitcommit: d48dce64f6c5b16db3250096715c9d9f92a81971
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083948"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i maj 2021 – Project Operations för resursscenarier/icke lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

- Project Operations i Dynamics 365 Dataverse-miljöversion 4.10.0.186
- Projekthantering och redovisning i Finance and Operations-appmiljöer version 10.0.18

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- [Schemaläggningslägen](../project-management/scheduling-modes.md): Projektledare kan nu definiera om ett projekt bör hanteras med fast varaktighet, fast arbete eller fasta enheter.
- [Ange körsträcka med hjälp av nivåer av körsträckepriser](../expense/set-up-mileage.md): Uppdatera nivån av körsträckepriser för anställdas utgiftsrapporter.

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Följande lista visar de mappningar med dubbelriktad skrivning som har ändrats eller lagts till i Project Operations-versionen maj 2021.

| Entitetsmappning | Uppdaterad version | Kommentarer |
| --- | --- | --- |
| Källa för projektfinansiering (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synkronisera projektkontraktkundens betalningsvillkor. |
| Projektfakturaförslag version 2 (fakturor) | 1.0.0.3 | Synkronisera betalningsvillkor för proforma-fakturor. |
| Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kvalitetsuppdateringar |
| Projekt V2 (msdyn\_projects) | 1.0.0.2 | Kvalitetsuppdateringar |

Kör alltid den senaste versionen av mappningen i din miljö och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och Finance and Operations-applösningsversion. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md).

Om du har problem med att starta mappningen följer du instruktionerna i avsnittet [Problem med saknade tabellkolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelriktad skrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2227635 | Värdena i fälten **Enhetsgrupp** och **Enhet** hämtas från produkten i rutnätet **Materialberäkningar**. |
| Fakturering och prissättning | 2234127 | Fältet **Uppgifts-ID** integreras nu korrekt med Dataverse-projektets verkliga värden när en leverantörsfaktura publiceras. |
| Fakturering och prissättning | 2235564 | Genom att spara journalraden ser du till att valutan som visas i journalraden matchar standardvalutan med raden efter att den har sparats. |
| Fakturering och prissättning | 2246671 | Om en transaktion blir icke debiterbar under fakturering vänder den ursprungliga icke fakturerade försäljningsposten och skapar en ny icke fakturerad försäljningspost som icke fakturerbar. |
| Fakturering och prissättning | 2264042 | En giltig fakturakorrigering får inte blockeras om det finns en fakturakorrigeringsdetalj som inte är giltig i miljön. |
| Fakturering och prissättning | 2146367 | Projektfakturahuvudets mappning för dubbelriktad skrivning utökas till att omfatta betalningsvillkor. |
|   Affärsmöjlighetshantering | 2086888 | Lägg inte till roller och kategorier som inaktiveras innan du kopierar en offert till debiterbara roller och kategorier för en nyligen kopierad offert. |
|   Affärsmöjlighetshantering | 2234376 | Skrivskyddade fält är gråmarkerade i rutnätet **Materialberäkningar**. |
|   Affärsmöjlighetshantering | 2238337 | En offert som bygger på en kontakt kan sparas även om den inte är associerad med en projektprislista. |
|   Affärsmöjlighetshantering | 2239810 | Om en offert stängs när den förloras stängs även det associerade projektet och eventuella bokningar avbryts. |
| Projektplanering och spårning | 2099559 | Lade till ytterligare valideringar för systemhälsa innan rutnätet **Projektuppgifter** öppnas. |
| Projektplanering och spårning | 2178987 | Åtgärdade ett fel som inträffar när man väljer **Nästa steg** på sidan **Projekt**. |
| Resurshantering | 2224817 | Funktionen som utvidgar standardvärdena till rätt bokningsstatus. |
| Tidspost | 2202476 | Sidan **Tidspost** använder nu kontroll för att reagera på rutnät och åtgärdar problem som feljustering av rutnät. |
| Tidspost | 2223377 | Tidsposten döljs från avsnittet **Relaterade** på sidan **Bokningsbar resurs** för att undvika förvirring om användbarhet. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Projektledning och redovisning | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations för Resursbaserade scenarier: Det går inte att konvertera offert till vunnen på grund av ett integrationsfel. |
| Projektledning och redovisning | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Ett fel uppstår när du försöker associera en kontraktrad med ett projekt-ID på grund av kontroll av överlappande kontraktrader och transaktionstyper. |
| Projektledning och redovisning | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** ställer in finansieringskällans fakturadress från en annan kund. |
| Resor och utgifter | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Ett registreringsfel i samband med inställning för körsträckor kan uppstå. |
| Resor och utgifter | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funktionen **Dela för personlig** fungerar inte för utgiftstransaktioner i utländsk valuta. |
| Resor och utgifter | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Värden i listrutan för utgiftskategori visar felaktiga kategorier för delegater, oavsett om de är en resurs. |
| Resor och utgifter | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Det går inte att spara en koncernintern utgiftsrapport på grund av ett valideringsfel för **Resurs/kategori**. |
| Resor och utgifter | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Fel beräkning av körsträckepris i registrering av utgiftsrapport har delade rader. |
| Resor och utgifter | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Det går inte att registrera en koncernintern utgiftsrapport när moms ingår och förskjutningskontotypen i betalningsmetoden är **Arbetare**. |
| Resor och utgifter | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Återta dataentiteten **TrvRequisitionLine** och det associerade unika indexet. |
| Resor och utgifter | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | I utgiftsrapporten kan källdokumentrad skapas och uppdateras. |
| Resor och utgifter | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | En felaktig reskontrajournal visas i ett scenario där momsen har angetts i destinationsadressen. |
| Resor och utgifter | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Utgiftsberäkningen raderas inte från Ekonomi när den raderas från Dataverse. |
| Resor och utgifter | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | När utgiftskategorin är en kategori som inte är en projektkategori kopieras inte de ekonomiska mått som valts på sidan **Utgifter** till utgiftsrapporten. |
