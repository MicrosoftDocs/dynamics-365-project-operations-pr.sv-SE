---
title: Nyheter i mars 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Detta ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i mars 2022-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600764"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i mars 2022 – Project Operations för resurs-/icke-lagerbaserade scenarier

*Gäller: Project Operations för resurs-/icke-lagerbaserade scenarier*

Detta ämne gäller följande komponenter och versioner av Microsoft Dynamics 365 Project Operations:

- Project Operations i en Dataverse-miljö, version 4.30.0.99
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.25

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Traktamente stöds nu i den nya och förbättrade moderna arbetsytan för utgifter. Företag som använder traktamente kan använda den här funktionen för att ge användarna ett enkelt sätt att skicka in och få ersättning för sina traktamentesutgifter. Mer information finns i [Traktamentesutgifter](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

I följande lista visas mappningar med dubbelskrivning som har ändrats eller lagts till i mars 2022-versionen av Project Operations.

| **Entitetsmappning** | **Uppdaterad version** | **Kommentarer** |
| --- | --- | --- |
| Exportentitet msdyn\_projectvendorinvoicelines på fakturarad för projektleverantör för Project Operations-integrering | 1.0.0.3 | Mappningar som har uppdaterats för att justeras mot entiteten för leverantörsfakturarad i Dataverse. <br>Aktivera inte mappningsversion 1.0.0.4. Denna kommer att vara klar att användas i kombination med Finance-miljön i version 10.0.26 i nästa månadsuppdatering. |

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningsversionen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av mappningen visas i kolumnen **Version** på sidan **Dubbelriktad skrivning**. Du aktiverar en ny version av mappningen genom att välja **Tabellmappningsversioner**, välja senaste versionen och sedan spara den valda versionen. Om du har anpassat en färdig tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på problem när du ska köra mappningen följer du instruktionerna i avsnittet [Problem med saknade kolumner i mappningar](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbelskrivning.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Tid och utgift | 2388011 | Visa avvisningskommentarer till inskickare av tidsposter vid massgodkännande. |
| Projektplanering och spårning | 2495294 | Projektinformationen får inte vara redigerbar på sidan **Uppgiftsinformation**. |
| Fakturering och prissättning | 2499605 | Kontraktmilstolpar som skapas från offertmilstolpar är felaktigt markerade som skrivskyddade. |
| Projektplanering och spårning | 2506050 | Åtgärdsuppsättningen förblir väntande i en timme om det inte finns någon ändring att spara. Uppsättningen markeras sedan felaktigt som **Misslyckad** istället för att slutföras omedelbart. |
| Fakturering och prissättning | 2507401 | Standardmässiga kontrakteringsenheter anges felaktigt i projekt på grund av fel i cachelagring. |
| Fakturering och prissättning | 2541660 | **Validering av generering av försäljningsorder** i dubbelskrivning bör endast användas för projektbaserade order. |
| Fakturering och prissättning | 2552745 | Moms delas inte upp mellan kunder som har konfigurerat delade faktureringsregler. |
| Fakturering och prissättning | 2558859 | Bättre felmeddelanden när prissättningsmått konfigureras. |
| Fakturering och prissättning | 2558933 | **Importera från projektberäkningar** misslyckas när **msdyn\_project** läggs till som prissättningsmodell. |
| Fakturering och prissättning | 2559101 | Borttagning av projektparameter blockeras inte och förorsakar problem. |
|   Affärsmöjlighetshantering | 2570390 | Plugin-programmet med dubbelskrivning gör att kontotypen för offerter, order och affärsmöjligheter måste vara **Kund**, även när kontotypen inte är korrekt. |
| Fakturering och prissättning | 2586097 | Faktiska värden för delad kostnad återförs inte när ett projekt tas bort från en projektkontraktrad. |
| Fakturering och prissättning | 2589619 | Moms på oregistrerade material sprids till ofakturerad faktisk försäljning och till fakturan. |
|   Affärsmöjlighetshantering | 2594015 | En offert kan inte stängas som "vunnen" för kunder som har betalningsvillkoren **Net60**. |
| Projektplanering och spårning | 2595841 | I Project for the Web får användarna ett felmeddelande om att **msdyn\_actualstart** saknas när de skapar en ny resursbegäran. |
| Tid och utgift | 2602511 | Fältet **Avvisades av** för tidsposter visar **System** istället för en namngiven användare som avvisare. |
| Tid och utgift | 2602528 | En projektgodkännare kan godkänna tid för projekt där de inte anges som godkännare. |
| Fakturering och prissättning | 2608550 | En korrigeringsfaktura kan bekräftas även om originalversionen inte ändrats. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Projektledning och redovisning | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Det finns en felmatchning mellan Finance och Project Operations i den tillåtna längden för fältet **Kategori-ID**. |
| Projektledning och redovisning | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekt med fast pris kan inte tas bort när fältet **Fakturering på konto** har angetts som **Vinst och förlust** och principen om **Slutförd procent** används. |
| Projektledning och redovisning | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Fel momsgrupp för standardförsäljning anges i projektinstallationen på utgiftsrader i integreringsjournalen för Project Operations. |
| Projektledning och redovisning | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Du kan inte redigera sidhuvudmåtten för projektfakturaförslag i en integrerad distribution med Project Operations. |
| Projektledning och redovisning | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Koncerninterna leverantörsfakturor får inte integreras med Dataverse. |
| Projektledning och redovisning | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Det finns ett matchningsfel i valutan för kundsaldo och i rapportvalutan. |
| Projektledning och redovisning | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Du kan publicera en projektfaktura även om kunden pausats för alla fakturor. |
| Projektledning och redovisning | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Knappen **Ta bort alla rader** saknas i projektfakturaförslag som har vyerna **Rubrik** och **Rader**. |
| Projektledning och redovisning | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | När du publicerar en leverantörsfaktura uppstår följande fel: "Redovisningsdatumet för fakturan måste ligga i samma räkenskapsår som den relaterade köpta ordern. Kör processen för räkenskapsårets slut på inköpsordern eller ändra datumet till det aktuella räkenskapsåret." |
| Resor och utgifter | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Den tilldelade kostnaden för ett projekt frigörs inte efter att reserekvisitionens kostnader har frisatts. |
| Resor och utgifter | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Följande fel uppstår när du skickar en utgiftsrapport: "Stackspårning: företaget finns inte." |
| Resor och utgifter | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Standard-**Projekt-ID** anges inte i utgiftsrapporter när parametern **Kräv aktivitet för journal** har markerats för projektet. |
| Resor och utgifter | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Knappen **Inläggsutgifter** fungerar inte korrekt i Project Operations för resurs-/icke lagerbaserade scenarier. |
| Resor och utgifter | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Det finns ett problem med **Taxa per kilometer** för en resekostnadsrapport som innehåller passagerare. |
| Resor och utgifter | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Utgifter för kilometerantal för anställda summeras inte korrekt när två olika typer av färdmedel används i utgiftskategorin för **Kilometerantalsnivå**. |
| Resor och utgifter | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Uppslag för fältet **Projekt** på en reserekvisitionsrad returnerar inte rätt lista med projekt. |
| Resor och utgifter | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Granskat kilometerantal** visar en varning i utgiftsrapporter. |
| Resor och utgifter | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | OCR-tjänsten för optisk teckenigenkänning fungerar inte på grund av ett problem med URL-adressen för OCR-utgiftstjänsten. |
| Resor och utgifter | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | När funktionen **Förmåga att specificera återkommande utgifter snabbt** har aktiverats, kommer beloppen på objektiseringsraderna i utgiftsrapporter att ändras varje gång sidan **Objektisering** att öppnas. |
| Resor och utgifter | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Du kan inte ta bort en utgiftsrapport om den tillfälliga listan har fler än en godkännare. |

## <a name="removed-and-deprecated-features"></a>Borttagna och inaktuella funktioner

Ämnet [Borttagna och inaktuella funktioner i Project Operations](removed-depreciated-features-project.md) beskriver funktioner som har tagits bort eller gjorts inaktuella för Dynamics 365 Project Operations.

- En borttagen funktion är inte längre tillgänglig i produkten.
- En borttagen funktion befinner sig inte i aktiv utveckling och kan komma att tas bort i en kommande uppdatering.

Ett meddelande om inaktualisering kommer att visas i ämnet [Borttagna eller inaktuella funktioner i Project Operations](removed-depreciated-features-project.md) 12 månader innan någon funktion tas bort från produkten.

För icke-bakåtkompatibla ändringar som endast påverkar kompileringstiden men är binärt kompatibla med begränsade lägen och produktionsmiljöer, blir utfasningstiden kortare än 12 månader. Vanligtvis är dessa ändringar funktionsuppdateringar som måste göras till kompileraren.
