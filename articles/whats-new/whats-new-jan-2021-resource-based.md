---
title: Nyheter i januari 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: I det här ämnet finns information om de kvalitetsuppdateringar som är tillgängliga i utgåvan av Project Operations för januari 2021 för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 50874d771afe03b08bd95b670f7095bc2d61509d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599568"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i januari 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_


Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

  - Project Operations i Dataverse-miljöversion 4.6.0.154
  - Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.16

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| **Distribution och konfiguration** | 2106818 | Åtgärdade det namn på webbresurs som orsakade problem relaterade till anpassningen av en sida. |
| **Fakturering och prissättning** | 2091908 | Åtgärdade synligheten för alternativen **Lås prissättning** och **Använd aktuell prissättning** på sidan **Faktura** när Project Operations installeras tillsammans med Dynamics 365 Field Service. |
| **Fakturering och prissättning** | 2103058 | Uppdaterade **Projektsummor** så att dessa kan hantera null-värden för den faktiska kostnaden för en uppgift. |
| **Fakturering och prissättning** | 2116100 | Förbättrade felmeddelanden som används med funktionen **Korrigera poster för faktiska värden**. |
| **Fakturering och prissättning** | 2116129 | Bättre synlighet för utgifter på fliken **Beräkningar** på sidan **Projekt**. |
| **Fakturering och prissättning** | 2119112 | Fast sammansättning av faktisk försäljning och faktiska kostnader när olika växelkurser används. |
| **Fakturering och prissättning** | 2134705 | Åtgärdade felet" "Kan inte läsa egenskapen **getResourceString** för icke-definierad" när sidan **Faktura** öppnas och Field Service har installerats. |
| **Administrering av affärsmöjligheter** | 2022195 | Det uppgiftsbaserade faktureringsrutnätet på sidan **Projekt** innehåller en ikon som anger att det finns en kontrakt- eller offertrad länkad till uppgiften. |
| **Administrering av affärsmöjligheter** | 2029135 | Åtgärdade affärsprocessfelet som uppstår när en användare försöker öppna en fakturarad på en bekräftad faktura med ett fakturerat förskott. |
| **Administrering av affärsmöjligheter** | 2040713 | Åtgärdade skriptfelet som uppstår när en faktura skapas från ett kontrakt och Field Service installeras. |
| **Projektplanering och spårning** | 2090202 | Markerade affärsregler som inte längre används som **inaktuella**. |
| **Tid och utgift** | 2091249 | Stramade åt kontrollerna så att användaren inte kan ändra uppgiften på en tidspost som har godkänts eller skickats. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| **Projektledning och redovisning** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Felaktigt kontraktbelopp på sidan **Kredit** för ett fastprisprojekt med multipla finansieringskällor. |
| **Projektledning och redovisning** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Platshållaren **Invoiceproposal.PSAnfRefProjId** visar inte projekt-ID för arbetsflödet **Granska projektfakturaförslag**. |
| **Projektledning och redovisning** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Fel kassarabattdatum används när projektfakturaförslag publiceras. |
| **Projektledning och redovisning** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Borttagning och avläsning av resurstilldelningar i Project OPerations fördubblar projektprognosposter i Finance. |
| **Projektledning och redovisning** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | I Project Operations går det inte att skapa projektberäkningar i Dataverse utan att det finns en kontraktrad i projektet. |
| **Projektledning och redovisning** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Ekonomiska aspekter av en projektkostnadstransaktion synkroniseras inte med den relaterade verifikationen och kostnadsrapportens redovisningsdistribution när kostnader läggs upp i Saldo. |
| **Projektledning och redovisning** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filtret **Fakturastatus** för bokförda projekttransaktioner för fastprisprojekt fungerar inte. |
| **Projektledning och redovisning** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Den omvända beräkningselimineringen fungerar inte i avsnittet **Periodiskt**. |
| **Projektledning och redovisning** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Rader för fakturaförslag kan raderas i Project Operations när detta integreras med Dataverse. |
| **Projektledning och redovisning** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Funktion som förhindrar aktivering av flera kontraktrader utan Dataverse-integrering. |
| **Projektledning och redovisning** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | När kreditfaktureringen är lika med vinst och förlust, visas den fakturerade omsättningen som noll på sidan Beräkningar. |
| **Projektledning och redovisning** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Fakturakorrigeringar fungerar inte i integrerade miljöer. |
| **Projektledning och redovisning** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Fel konto väljs i samband med bokföring av PIA/försäljningsvärde i koncerninterna projektfaktureringar. |
| **Projektledning och redovisning** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | I Project Operations går det inte att uppdatera beroenden för beräkningsuppgifter i Dataverse. |
| **Projektledning och redovisning** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Att upprepade gånger ta bort Project Operations-integreringsjournaler i Finance leder till dataförlust. |
| **Projektledning och redovisning** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Följande fel uppstår när ett projektfakturaförslag bokförs: "Transaktionen balanserar inte rapporteringsvalutan när förskottsfakturan dras av". |
| **Projektledning och redovisning** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Fel projekt-ID anges när standardprojektkontraktet har uppdaterats i Project Operations. |
| **Projektledning och redovisning** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Beräknings- och intäktsidentifiering kan inte slutföras när Project Operations har aktiverats. |
| **Projektledning och redovisning** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Om du tar bort ett projekt från ett kontrakt i Project Operations återställs inte standardprojektet i kontraktet. |
| **Projektledning och redovisning** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | I en koncernintern faktura i Project Operations visas fel utgiftsrader i listan **Lägg till rad**. |
| **Resor och utgifter** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Det går inte att bokföra utgiftsrader eftersom timkonfiguration saknas på kontraktraden. |
| **Resor och utgifter** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | När projekt-/kategorivalidering är obligatoriskt visas inte de utgiftskategorier som är associerade med projektet i utgiftsrapporten. |
| **Resor och utgifter** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Förskottssaldot uppdateras inte när en utgiftsrapport bokförs per rad. |
| **Resor och utgifter** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Jobbet **Uppdatera betalningsinformation** misslyckas efter att ha återställt avtal där en faktura betalades genom två betalningstransaktioner eller fler. |
| **Resor och utgifter** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Det finns ett problem med beräkningen av sista dagens måltidsrabatt för utgiftskategorin per dag. |
| **Resor och utgifter** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | I rapporten **Utgiftstyp per anställd** visas inte specificerade utgifter om en användares första anslutning skedde i språkkombination es-MX. |
| **Resor och utgifter** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Leverantörsbetalningen för en faktura för utgiftsrapport använder fel summeringskonto för bokföring av kostnader. |
| **Resor och utgifter** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | När en utgiftsrapport bokförs med **Tillåt gruppering av transaktioner baserat på konto för motbetalning** och **Korrigering av redovisningsdatum vid bokföring** aktiverade, visas bokföringsdatum som ej grupperade i tabellen **Redovisningsdistribution**, vilket påverkar momsposterna. |
| **Resor och utgifter** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Mappning av underkategorier för utgifter tas bort när kryssrutan Använd i utgifter avmarkeras och markeras igen. |
| **Resor och utgifter** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | En koncernintern utgiftsrapport kan inte skapas om projekt-ID:t läggs till på huvudnivå. |
| **Resor och utgifter** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Det finns ett problem med utgiftsbetalningar när utgiftsbeloppet överstiger förskottsbeloppet. |
| **Resor och utgifter** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Fältet **Projekt-ID** på en koncernintern utgiftsrapport är tomt om användarrollen tilldelats en specifik organisation. |
| **Resor och utgifter** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Utgiftskategorin är låst när en ny utläggsrad läggs till. |
| **Resor och utgifter** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Om du specificerar utgiftsrapportrader som redan är delade resulterar detta i en ofullständigt bokförd verifikation för leverantörsreskontra\huvudbok. På grund av dubbletten av **TRVEXPTRANS. SOURCEDOCUMENTLINE** drabbas utforskaren för redovisningskälla också av fel. |
| **Resor och utgifter** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Det index som läggs till i tabellen **TRVREQUISITIONLINE** och för vilket kunden har dubbletter, resulterar i fel i samband med uppgraderingen. |
| **Resor och utgifter** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | I Project Operations går det inte att skapa eller godkänna tid med koncerninterna uppgifter i Dataverse. |

## <a name="regulatory-updates"></a>Regleringsuppdateringar

Information om regeluppdateringar för appar för ekonomi och drift finns i [Regeluppdateringar](/dynamics365/finance/localizations/regulatory-updates). Du kan också logga in på LCS och visa de planerade regeluppdateringarna med hjälp av verktyget för att söka efter problem. Med problemsökning kan du söka efter land, typ av funktion och utgåva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]