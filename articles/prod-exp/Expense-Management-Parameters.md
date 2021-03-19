---
title: Parametrar för utgiftshantering
description: Följande parametrar styr beteendet i utgiftshanteringen.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 498d597fe811192ce313a1b0384de81e7ef55c58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271946"
---
# <a name="expense-management-parameters"></a>Parametrar för utgiftshantering


Parametrarna styr det allmänna beteendet i utgiftshanteringen.

### <a name="general"></a>Allmän

| **Fält**                                                | **Beskrivning**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardpris för körsträcka**                             | Ange återbetalningssatsen för kostnaden för körsträckan. Kostnaden multipliceras med den körsträcka som anges för utgiften för att beräkna det belopp som har återbetalats för reseutgiften.                       |
|**Privata utgifter som betalas av**                             | Välj vem som är ansvarig för att betala transaktionsbelopp för kreditkort som är kategoriserade som personliga.                                                                                                     |
|**Visa hela utgiftsrapporten i mindre detaljnivå**               | Välj det här alternativet om du vill visa alla utgifter för en utgiftsrapport när detaljerna för det ursprungliga dokumentet visas för en specifik verifikation som skapades när utgiftsrapporten bokfördes.              |
|**Förauktorisering för resa är obligatoriskt**                 | Välj det här alternativet om du vill kräva att en reserekvisition skickas och godkänns innan en medarbetare kan skicka en utgiftsrapport.                                                                    |
|**Tillåt redigering av distributioner före bokföring**            | Ange om distributionerna av en utgiftsrapport kan redigeras innan den bokförs.                                                                                                                 |
|**Utvärdera policy för utgiftshantering**                     | Välj när utgifter utvärderas för att avgöra om en utgiftspolicy har överträtts. Utgifter kan kontrolleras för överträdelser när utgiftsposten registreras och sparas, eller när utgiften skickas för godkännande. Policyreglerna för kvitton som är obligatoriska kommer att kontrolleras när utgiftsraden sparas.                   |
|**Tillåt företagsinterna utgiftsrader**                         | Ange om utgifter för andra juridiska entiteter ska tillåtas i en utgiftsrapport.                                                                                                          |
|**Tillåt redigering av växelkurs för kreditkortsutgifter** | Välj det här alternativet om du vill tillåta användaren att redigera växelkursen för importerade kreditkortsutgifter.                                                                        |
|**Hierarkiska fält som ska visas på flera nivåer**                  | Välj vilka godkännarfält som ska visas när tilldelningstypen för utgiftsrapportarbetsflödet är en hierarki, och valet Hierarki är inställt på att använda godännandehierarkin, godkännande av utgifter på flera nivåer. När hierarkin för godkännande på flera nivåer används för ett arbetsflöde visas de valda fälten och är redigerbara i utgiftsrapporten. |
|**Ange kreditkortsnummer för medarbetare (uppdatering juli 2017)**     | Välj om ett nummer på 15 eller 16 tecken kan anges och sparas i fältet **Kort-ID** på sidan **Kreditkort** för en anställd.                                                                          |

### <a name="financial"></a>Finansiell verksamhet

| **Fält**                                                            | **Beskrivning**     |
|----------------------------------------------------------------------|------------------------------------|
|**Transaktionsregistrets dagliga journalnamn**                                         | Välj namnet på den redovisningsjournal som godkända utgiftsrapporter ska bokföras på.            |
|**Aktivera momsåterbetalning från utgifter**                                  | Välj det här alternativet om du vill aktivera återbetalning av moms för berättigande utgifter. Alternativet kan inte aktiveras om amerikanska moms- och skatteregler är aktiverade.      |
|**Bokföra förskott omedelbart**                                     | Välj det här alternativet om du vill bokföra en godkänd förskottsbetalning när löne- och överföringsprocessen har slutförts. Om alternativet inte har valts genererar betalnings- och överföringsprocessen en allmän journal som inte bokförs. |
|**Korrigera redovisningsdatum vid bokföring**                             | Välj det här alternativet om du vill uppdatera redovisningsdatumet då utgifter bokförs, om aktuell period är spärrad eller stängd. Redovisningsdatumet sätts till nästa öppna period.   |
|**Tillåt gruppering av transaktioner baserat på motkonto angivet i betalningsmetod**      | Välj det här alternativet om du vill sammanfatta utgiftstransaktioner för en utgiftsrapport utifrån det motkonto som anges i betalningsmetoden för utgifterna.   
|**Inklusive moms**                                                   | Välj det här alternativet om du vill inkludera moms i utgiftsbeloppet som standard.             |
|**Frisläpp inteckningar vid stängning av reserekvisitioner**            | Välj det här alternativet om du vill släppa intecknade medel när en godkänd reserekvisition stängs.                                                                                   |
|**Tillåt sändning av reserekvisition för budgetöverskridningar för budgetregister och projektbudget** | Välj det här alternativet om du vill att medarbetare ska kunna skicka reserekvisitioner för godkännande som överskrider antingen den tillåtna budgeten som har ställts in i budgetregistret eller den tillåtna budgeten för ett projekt.            |
|**Tillåt sändning av utgiftsrapport för budgetöverskridningar för budgetregister och projektbudget**    | Välj det här alternativet om du vill att medarbetare ska kunna skicka utgiftsrapporter för godkännande som överskrider antingen den tillåtna budgeten som har ställts in i budgetregistret eller den tillåtna budgeten för ett projekt.                |
|**Tillåt godkännande av utgiftsrapport för budgetöverskridningar för budgetregister**                | Välj det här alternativet om du vill tillåta godkännare att godkänna utgiftsrapporter som överstiger den tillåtna budgeten som har ställts in i budgetregistret.                                                                       |

### <a name="per-diem"></a>Per dag

| **Fält**                             | **Beskrivning**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minsta antal timmar för traktamente**           | Ange det minsta antalet timmar som en medarbetare måste arbeta under en dag för att kunna få traktamente för resekostnader.  Värdet används endast som standardvärde för fältet Minsta antal timmar på traktamentesnivåerna.                                                                                      |
|**Procentandel för måltider**                          | Ange standardprocentsats för traktamentet för måltider som används på den första och sista dagen av reseutgiften när fältet **Beräkna måltidsreducering** är inställt på antingen **Måltidstyp per dag** eller **Antal måltider per dag**. Arbetsdagen den första och den sista dagen kan vara kortare än en vanlig arbetsdag. Därför kan beloppet för traktamentet dessa dagar skilja sig från standardbeloppet. Om procentsatsen har värdet 0 blir avdragen för första och sista dagen 0,00. |
|**Procentandel för hotell**                        | Ange standardprocenten av traktamentet för hotell som används på den första och sista dagen av resekostnaderna. Arbetsdagen den första och den sista dagen kan vara kortare än en vanlig arbetsdag. Därför kan beloppet för traktamentet dessa dagar skilja sig från standardbeloppet. Om procentsatsen har värdet 0 blir avdragen för första och sista dagen 0,00.                                              |
|**Annan procent**                        | Ange standardprocenten av traktamentet för diverse utgifter som används på den första och sista dagen av resekostnaderna. Arbetsdagen den första och den sista dagen kan vara kortare än en vanlig arbetsdag. Därför kan beloppet för traktamentet dessa dagar skilja sig från standardbeloppet. Om procentsatsen har värdet 0 blir avdragen för första och sista dagen 0,00.                                                                                                     |
|**Reducering av procentsats för frukost** | Ange det belopp som traktamentet minskar med för frukost. Om en anställd till exempel får en kostnadsfri frukost kan du minska beloppet för traktamentet med 10 procent.                               |
|**Reducering av procentsats för lunch**    | Ange det belopp som traktamentet minskar med för lunch. Om en anställd till exempel får en kostnadsfri lunch kan du minska beloppet för traktamentet med 15 procent.                                       |
|**Reducering av procentsats för middag**   | Ange det belopp som traktamentet minskar med för middag. Om en anställd till exempel får en kostnadsfri middag kan du minska beloppet för traktamentet med 25 procent.                                     |
|**Beräkna måltidsavdrag efter**         | Välj hur systemet ska beräkna måltidsavdrag i traktamentet genom att välja om minskningen ska baseras på måltidstypen per resa eller per dag, eller om minskningen ska baseras på antalet måltider som tillåts per dag.|
|**Avrundning av traktamente**                  | Välj vilken typ av avrundning som ska användas för traktamente. Om du väljer normal avrundning avrundas varje traktamentsutgift som har beloppet 0,50 till 1,00 och varje traktamentsutgift som har ett belopp som är mindre än 0,50 avrundas nedåt till 0,00.                                                                                              |
|**Basera beräkningen av traktamente på**         | Välj om ett traktamentsbelopp ska baseras på en kalenderdag eller en 24-timmarsperiod.       |

### <a name="fax-cover-pages"></a>Faxförsättsblad

| **Fält**                      | **Beskrivning**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Anvisningar**                   | Ange de instruktioner som medarbetarna måste följa när de skapar ett försättsblad för ett fax som används för att skicka kvitton som är relaterade till en utgiftsrapport. Klicka på knappen **Översättningar** för att ange språkspecifik text som ska visas baserat på användarspråket. |
|**Användar-ID (information om streckkoder)** | Välj det här alternativet om du vill lagra en unik identifierare för medarbetaren i streckkoden som används på försättsbladet i faxet.                 |
|**Streckkod**                      | Välj den streckkod som används på försättsbladet i faxet. Streckkoder 39 och 128 kan användas i utgiftshantering.               |

### <a name="anti-corruption"></a>Anti-korruption

|                 <strong>Fält</strong>                 |                                                                                                                                                                                            <strong>Beskrivning</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Visa attestering för anti-korruption</strong>  | Välj det här alternativet om du vill visa anti-korruptionstexten när du skapar en utgiftsrapport. Särskilda utgiftskategorier kan sedan aktiveras som kräver att attesteringen för anti-korruption väljs i utgiftsrapporten. En presentkategori som är relaterad till en statlig officiell kostnad kan till exempel kräva att medarbetaren bekräftar att utgiften uppfyller företagets policy vad gäller myndighetstjänstemän. |
| <strong>Anti-korruptionsmeddelande för avsändare</strong> |                                                                                             Ange den text som ska visas för medarbetaren när du skapar en ny utgiftsrapport. Klicka på knappen <strong>Översättningar</strong> för att ange språkspecifik text som ska visas baserat på användarspråket.                                                                                             |
| <strong>Anti-korruptionsmeddelande för godkännare</strong>  |                                                                                             Ange den text som ska visas för godkännaren när du skapar en ny utgiftsrapport. Klicka på knappen <strong>Översättningar</strong> för att ange språkspecifik text som ska visas baserat på användarspråket.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]