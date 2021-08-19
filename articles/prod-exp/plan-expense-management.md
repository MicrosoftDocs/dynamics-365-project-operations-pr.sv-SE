---
title: Konfigurera utgiftshantering
description: I den här artikeln beskrivs vad du bör tänka på samt vilka beslut du måste fatta under planeringsprocessen innan du konfigurerar utgiftshantering i Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca4362b0ff5d37b131e1d96e311aa48ac20397618314936944ba66e458dbdc2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007483"
---
# <a name="configure-expense-management"></a>Konfigurera utgiftshantering

I det här ämnet beskrivs vad du bör tänka på samt vilka beslut du måste fatta under planeringsprocessen innan du konfigurerar utgiftshantering. I utgiftshantering kan du lagra information om betalningsmetoder, reserekvisitioner, utgiftsrapporter, principer och så vidare.

Många av de beslut du fattar när du planerar din konfiguration av utgiftshantering bygger på organisationens hierarki och finansiella struktur, men du måste läsa planeringsdokumenten för dessa områden.

## <a name="intercompany-expenses"></a>Koncerninterna utgifter

När du aktiverar koncerninterna utgifter tillåter du att juridiska personer och medarbetare ådrar sig utgifter för en annan juridisk persons räkning och samlar in betalning från den juridiska personen inom organisationen. Exempel: En anställd i juridisk person A färdigställer ett projekt för juridisk person B och projektet ådrar sig resekostnader. Om koncerninterna kostnader har aktiverats kan medarbetaren sedan skicka in en utgiftsrapport som bokför utgiften till juridisk person B och kostnaden måste sedan betalas av juridisk person A. Om organisationen inte har flera juridiska personer behöver du inte aktivera koncerninterna utgifter.

**Beslut:** Vill du aktivera koncerninterna utgifter?

## <a name="financial-management"></a>Ekonomihantering

Utgiftshantering är nära integrerad med den ekonomiska förvaltningen av organisationen. Mycket av din konfiguration av utgiftshanteringen bygger på de beslut som du har fattat om organisationens ekonomi. I följande avsnitt beskrivs de olika områden som kräver planering och beslut, utifrån organisationens ekonomiska beslut och vägledning från ditt ledarskapsteam.

### <a name="per-diems"></a>Traktamente

Du måste definiera traktamenten för medarbetare som din organisation tillhandahåller. Eftersom traktamenten vanligtvis används för att täcka utgifter som måltider, logi och andra oförutsedda utgifter, kan du skapa regler för traktamenten som organisationen erbjuder. Traktamentstaxa kan baseras på tid på året, resmål eller både och. När du definierar en traktamentsregel kan du ange att en procentsats av traktamentstaxan ska dras in om en arbetare får gratis måltider eller tjänster. Du kan även definiera nivåer av traktamentstaxa för att ange ett minsta och högsta antal timmar som traktamentstaxan kan gälla för en arbetares resa.

**Beslut:**

- Förvalda traktamentsregler för första och sista dagen:

    - Vad är det minsta antalet timmar som en medarbetare kan ansöka om för en dag och fortfarande få traktamente?
    - Finns det en minskning av beloppet som erbjuds för måltider för första dagen och sista dagen? Om det finns en reducering, vad är procentsatsen för minskningen?
    - Finns det en minskning av beloppet som erbjuds för ett hotell för första dagen och sista dagen? Om det finns en reducering, vad är procentsatsen för minskningen?
    - Finns det en minskning av beloppet som erbjuds för andra utgifter som uppstår för första dagen och sista dagen? Om det finns en reducering, vad är procentsatsen för minskningen?

- Standardregler för traktamente:

    - Finns det till exempel en procentsats för minskning av traktamentet för varje måltid om måltider är kostnadsfria? Om det finns en reducering, vad är procentsatsen för minskningen för varje måltid?
    - Beräknas minskningen för måltider per dag, per resa eller per antal måltider per dag?
    - Ska traktamentets belopp avrundas på vanligt sätt eller avrundas uppåt?
    - Beräknas traktamentet för en 24-timmarsperiod eller en kalenderdag?

- Traktamentsregler som baseras på plats:

    - Varierar traktamentstaxan beroende på plats? Vilka platser ingår?
    - Om traktamentstaxan varierar beroende på plats kan du för varje plats ange vilken procentsats som ska användas för följande typer av utgifter:

        - Måltider
        - Hotell
        - Andra utgifter

### <a name="expense-management-journals-and-accounts"></a>Journaler och konton för utgiftshantering

Utgiftshantering kräver att du använder flera journaler och konton. Du måste till exempel bestämma om samma konto ska användas för förskott och kreditkortstvister.

**Beslut:**

- Vilken redovisningsjournal bokförs godkända utgiftsrapporter i?
- Vilket konto används för kontantförskott?
- Ska kontantförskott bokföras direkt?

### <a name="payment-methods"></a>Betalningsmetoder

När du tillåter medarbetare att ådra sig utgifter för företagets räkning måste du definiera de betalningsmetoder som medarbetarna får använda. Du kan till exempel tillåta anställda att använda kontanter eller ett företagskreditkort. Du kan även tillåta anställda att använda privata kreditkort och sedan återbetala de anställda. Du måste fatta följande beslut för varje betalningsmetod som du tillåter.

**Beslut:**

- Vilka betalningsmetoder är tillåtna?
- Vem äger utgifterna för betalningsmetoden?
- Finns det en motkontotyp? Om det finns en motkontotyp anger du den.
- Om det finns en motkontotyp anger du kontot.
- Om betalningsmetoden är ett kreditkort ska betalningsmetoden endast användas med importerade transaktioner?

### <a name="expense-categories-and-shared-categories"></a>Utgiftskategorier och delade kategorier

När medarbetare skapar en utgiftsrapport måste varje utgiftspost vara associerad med en utgiftskategori. Utgiftskategorier härleds från delade kategorier som kan delas av alla juridiska entiteter i organisationen. Kategorierna kan även delas i projekthantering och redovisning, beroende på hur organisationen har definierats. Baserat på definitionen av din organisation och vägledning från implementeringsteamet avgör du om kategorierna som används i utgiftshantering endast ska användas i utgiftshantering eller delas mellan projekthantering och redovisning och utgiftshantering. Observera att dessa kategorier kan delas mellan projekt och utgifter eller projekt och produktion, men inte mellan utgifter och produktion. Du måste fatta följande beslut för varje utgiftskategori.

**Beslut:**

- Vilken är utgiftskategorin? Exempel är kategorier för flygningar, hotell och sträcka.
- Kan utgiftskategorin också användas i projekthantering och redovisning?
- Vilken är utgiftstypen?
- Vilken är standardbetalningsmetoden för utgiftskategorin?
- Måste utgifter i utgiftskategorin specificeras?
- Vilken är det huvudsakliga standardkontot utgiftskategorin?
- Vad är standardmomsgruppen för utgiftskategorin?
- Är fler betalningsmetoder tillåtna i utgiftskategorin? Om ytterligare betalningsmetoder tillåts anger du dem.
- Finns det några underkategorier i den här utgiftskategorin? Om det finns underkategorier måste du också fatta följande beslut:

    - Har någon av underkategorierna exkluderats från momsåterbetalning?
    - Vad är momsgruppen för underkategorierna?

Om utgiftskategorin också används i projekthantering och redovisning ska du besvara de återstående frågorna. Annars går du vidare till nästa avsnitt.

- Vilka kostnadskonton ska användas för följande utgifter?

    - Kostnad
    - Löneallokering
    - PIA-kostnadsvärde
    - Kostnadsartikel
    - PIA-kostnad värdeartikel
    - Upplupen förlust
    - PIA, upplupen förlust

- Vilka intäktskonton ska användas för följande?

    - Fakturerad intäkt
    - Upplupna intäkter – försäljningsvärde
    - Pia – försäljningsvärde
    - Upplupna intäkter – produktion
    - PIA – Produktion
    - Upplupna intäkter – vinst
    - PIA – vinst
    - Upplupna intäkter – prenumeration
    - PIA-prenumeration

### <a name="taxes"></a>Skatter

För utgiftrelaterad skatt måste du bestämma vad som ska tas med eller vara aktiverat i utgiftsrapporter.

**Beslut:**

- Ingår moms i utgiftsbeloppen?
- Ska återbetalning av skatt aktiveras på utgifter?

    > [!NOTE]
    > När du planerar redovisningen kan du inte aktivera återbetalning av skatt för utgifter om du beslutade att tillämpa amerikanska moms- och skatteregler. (För att tillämpa amerikanska moms- och skatteregler ställer du in alternativet **Tillämpa momsregler** på **Ja**.)

## <a name="policies"></a>Principer

Genom att skapa principer för utgiftsrapporter kan du hjälpa organisationen att spara tid och pengar när anställda ådrar sig utgifter för dess räkning. Med hjälp av principer garanteras att medarbetarna håller sig inom budgeten, anger all information som krävs och att de endast spenderar pengar efter behov. Du måste fatta följande beslut för varje utgiftsrapportprincip och varje princip för godkännande av utgiftsrapporter som du skapar.

**Beslut:**

- Vad är namnet på principen?
- Vad används utgiftsprincipen till?
- Om du tidigare har beslutat att aktivera koncerninterna utgifter, vilka företag i organisationen gäller den här principen för?
- När börjar principen gälla?
- När upphör principen att gälla?
- Vad är principregeln?
- Vad är resultatet av principregeln?


[!INCLUDE[footer-include](../includes/footer-banner.md)]