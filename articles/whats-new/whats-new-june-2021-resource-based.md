---
title: Nyheter i juni 2021 – Project Operations för resurs/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i juni 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028306"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i juni 2021 – Project Operations för resurs/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande Dynamics 365 Project Operations komponenter och versioner:

- Project Operations i Dynamics 365 Dataverse miljöversion 4.11.0.156 eller 4.11.0.164.
- Projekthantering och redovisning i appar för ekonomi drift, version 10.0.19.

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- Möjlighet att ta bort [förslagsrader i Projektfaktura för justeringsscenarier](../invoicing/correct-project-invoice-proposals.md).
- Objekterade utgiftsrader återspeglar underkategorinamn i utgiftsrapporten [Utgiftsrapporter – Nya funktioner](../expense/expense-reports-reimagined.md#new-features).
- Betalningsmetod är tillgänglig i den nya utgiftsrutan när en ny kostnad skapas.
- Allmän API-tillgänglighet för projektscheman. Med den här nya funktionen kan kunderna programmässigt skapa, uppdatera och ta bort åtgärder för projektuppgifter, resurstilldelningar, aktivitetsberoenden och medlemsposter i projektteamet. Mer information finns i [Använda API i projektschemat för att utföra åtgärder med planeringsentiteter](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen. 

En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av mappningen i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar din Project Operations Dataverse-lösning och lösningsversionen för apparna för ekonomi och drift. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av kartan visas på sidan **Dubbelriktad skrivning** i kolumnen **Version**. Aktivera en ny version av kartan genom att välja **tabellmappningsversioner**, välja den senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på ett problem som startar kartan, följ instruktionerna i avsnittet [Saknade tabellkolumner saknas på kartor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbla skrivningar.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2281417 | Åtgärdade problemet med misslyckandet med den automatiska faktureringsåtgärden genom fakturaschemat. |
| Fakturering och prissättning | 2287835 | Bättre prestanda för fakturabekräftelse. |
| Administrering av affärsmöjligheter | 2222555 | Materialuppskattningsavgifter måste kopieras korrekt för att citera radinformation när du använder **Importera från projektberäkning**. |
| Administrering av affärsmöjligheter | 2223427 | Nu är det tillåtet med anpassningar för åtgärden **GenerateRetainersFromRetainerScheduleOptions**. |
| Administrering av affärsmöjligheter | 2277528 | Beräkning av fast milstolpe för fakturering för projektkontraktrader med flera kunder. |
| Projektplanering och spårning | 2226110 | Åtgärdade problemet med funktionen **Generera krav** i rutnätet **projektteam**. |
| Projektplanering och spårning | 2208109 | Användare kan inte skapa ett projekt i en valuta med relaterade uppgifter i en annan valuta. |
| Projektplanering och spårning | 2258228 | Listan över fält som tillåts ändra med entiteter **planering** med hjälp av Schema-API har uppdaterats. |
| Projektplanering och spårning | 2293989 | Rätt språkinställningar och nationella inställningar måste skickas till rutnätet **Projektuppgifter**. |
| Resurshantering | 2220493 | Åtgärdade användarupplevelsen i rutnätet **Uppgift** när en resursbegäran snabbt markerades som slutförd. |
| Resurshantering | 2330496 | Åtgärdade problemet med inläsningen av **planeringstavlan**. (Kvalitetsuppdatering finns i version 4.11.0.164) |
| Tid och utgift | 2194431 | Rutnätet **Tidspost** måste hedra början på veckan som anges i **Systeminställningar**. |
| Tid och utgift | 2277311 | När du har tagit bort värdet i en cell i rutnätet **tidspost** blir markören kvar i rutnätet. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde | Referensnummer | Kvalitetsuppdatering |
| --- | --- | --- |
| Projektledning och redovisning | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Formuläranteckningar** och **formulärkonfiguration** visas inte under **projekthanteringskonfigurationen** i juridiska entiteter för Ekonomi när de är integrerade med Project Operations. |
| Projektledning och redovisning | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Standardbeskrivningen för moms är tom när **Bokföringstyp** = **Moms** för projektfaktura. |
| Projektledning och redovisning | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Dubbel transaktion bokförs när uppgiftsbaserad fakturering används i Dataverse med Project Operations-integrering. |
| Projektledning och redovisning | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procentsatsen för intäktsidentifiering är felaktig när Project Operations-integrering används. |
| Projektledning och redovisning | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Periodiserade intäkter dubblas när du använder en väntande leverantörsfaktura i ett Project Operations integrerat scenario. |
| Projektledning och redovisning | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Det gick inte att bokföra integreringsregeln kan inte läggas upp om intäktsprofilregeln har angetts till konfigurationen **Grupp**. |
| Projektledning och redovisning | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Det går inte att lägga upp en inköpsfaktura för en projektorder med rader med flera måttenheter. |
| Projektledning och redovisning | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Standardvärdet för ekonomiska data för ett projekt kan inte uppdateras med dataentiteten projekt **V2**. |
| Projektledning och redovisning | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Partiprocessen för att skapa projektuppskattningar tar för lång tid att slutföra. |
| Projektledning och redovisning | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Genom att radera ett kontrakt raderas också adressen som är kopplad till kunden |
| Resor och utgifter | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Arbetsflödesvillkoret för godkännande av utgiftsrapport utvärderas inte korrekt. |
| Resor och utgifter | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Principen för utgiftsrapport är inte korrekt utvärdera Projekt-ID. |
| Resor och utgifter | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Åtgärden, **Dela upp i personligt för administrativa utgifter**, fungerar inte korrekt. |
| Resor och utgifter | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Utgiftsrapportens motiveringar raderas av misstag när vissa reserekvisitioner raderas. Detta inträffar när du återbeslutar utgiftsrapporten och rekvisitionen på samma sätt. |
| Resor och utgifter | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Det har ett problem med mobilappen Utgifter när fältet **Projekt-ID** krävs av principer för utgiftsrapport. |
| Resor och utgifter | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Koncerninterna utgifter som hör till ett projekt kan inte redigeras. I stället visas följande felmeddelande: "Objektreferens har inte angetts till en instans av ett objekt". |
| Resor och utgifter | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Fel valuta och belopp visas i bankunderläggsvalutan efter att en utgiftsrapport har angetts. |
| Resor och utgifter | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Förbättringar av funktionen *ta bort kreditkortstransaktioner*, har gjorts.  |
| Resor och utgifter | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Moms som ingår i en utgiftsrapport beräknas inte konsekvent när en annan rapportvaluta anges i en juridisk person. |
| Resor och utgifter | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Resultatet påverkas när en ny resekostnad läggs till. |
| Resor och utgifter | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Utgiftsregeln utlöses inte i utgiftsrapporten. |
| Resor och utgifter | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Om du överför en ny delad kategori med hjälp av ramverket Datahantering tas alla underkategorier bort för alla delade kategorier. |
| Resor och utgifter | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | När du skapar en utgiftsrad och väljer en kategori visas följande felmeddelande: "Kombinationen av Momsgrupp DOM och artikel Momsgrupp STD är inte giltig." |
| Resor och utgifter | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Det finns synkroniseringsproblem i mobilprogrammet Utgifter. |
