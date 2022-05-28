---
title: Traktamentskostnader
description: I det här ämnet finns information om hur du arbetar med traktamentskostnader.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596072"
---
# <a name="per-diem-expenses"></a>Traktamentskostnader

> [!IMPORTANT] 
> Funktionen som beskrivs i det här avsnittet är tillgänglig för mottagande användare som en del av en privat förhandsversion.

Ett traktamente är en fast, förutbestämd daglig ersättning som ett företag betalar till sina anställda för kostnader (hotell), måltider samt oförutsedda kostnader som de anställda ådrar sig när de reser i arbetssyfte. Företaget betalar denna ersättning till de anställda istället för att betala de faktiska resekostnaderna. Anställda kan använda sina traktamenten för **oförutsedda utgifter/annat** för att täcka dricks, rumsservice, tvätt- och kemtvättskostnader i samband med viktiga affärsmöten. Traktamentet kan variera beroende på om arbetsgivaren väljer att ersätta de sammanlagda kostnaderna för boende och måltider, eller endast för kostnader för måltider och oförutsedda kostnader.

Traktamentstaxa kan baseras på tid på året, resmål eller både och. När du skapar en traktamentsregel kan du ange att en procentandel av traktamentet ska dras in om en anställd bjuds på måltider eller tjänster. Du kan även ange ett minimum av timmar och ett maximalt antal timmar per månad som traktamentet kan tillämpas på en anställds resande.

Traktamentet beräknas som den totala ersättning som erbjuds per dag minus den måltidsrabatt (kostnad för kostnadsfria måltider) som ges till den anställde.

## <a name="configure-per-diems"></a>Konfigurera traktamenten

Så här konfigurerar du traktamenteutgifter:

1. Gå till **Utgiftshantering** \> **Inställningar** \> **Allmänt** \> **Parametrar för utgiftshantering**.
2. På fliken **Traktamente**, i fältet **Beräkna måltidsrabatt med**, väljer du hur traktamenten ska beräknas:

    - **Måltidstyp per resa** – Beräkna traktamentet utifrån den typ av måltid som angetts (frukost, lunch eller middag) samt utifrån den måltidsrabatt som anges för respektive måltidstyp för traktamentet under resans varaktighet.
    - **Måltidstyp per dag** – Beräkna traktamentet utifrån den typ av måltid som angetts samt utifrån den måltidsrabatt som anges för respektive måltidstyp för traktamentet per dag.
    - **Antal måltider per dag** – Beräkna traktamentet baserat på antalet måltider som anges per dag samt baserat på måltidsavdraget för det antal måltider som tillhandahålls varje dag.

3. Gå till **Utgiftshantering** \> **Inställningar** \> **Beräkningar och koder** \> **Per traktamenteplatser**.
4. Lägg till platser där traktamenten kan användas.
5. För varje plats som du lägger till väljer du på fliken **Traktamente** den traktamentetaxka och den valuta som säller mellan specifika start- och slutdatum för boende, måltider och andra utgifter. Om du vill konfigurera traktamentetaxor och valutor går du till **Utgiftshantering** \> **Inställningar** \> **Beräkningar och koder** \> **Traktamenten**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Traktamenten i det nya utgiftsgränssnittet

Traktamentefunktionen stöds på den nya arbetsytan **Utgiftshantering** i Microsoft Dynamics 365 Finance version 10.0.25 och senare.

Följ stegen nedan för att aktivera traktamenten:

1. Ppå arbetsytan **Funktionshantering** letar du upp och väljer funktionen **Nya utgiftsrapporter** i listan och väljer sedan **Aktivera nu**.
2. Leta upp och välj funktionen **Nytt gränssnitt för traktamente för utgiftsrapport** i listan, och välj sedan **Aktivera nu**.

## <a name="how-the-feature-works"></a>Så här fungerar funktionen

Detta avsnitt innehåller exempel på tre konfigurationsscenarier. För varje exempel anges fältet **Beräkna måltidsrabatt efter** som ett annat värde. I alla tre exempel är det totala belopp som ska betalas detsamma tills måltidsavdraget tillämpas. Därefter skiljer sig det totala belopp som ska betalas för varje exempel.

Följ stegen nedan om du vill skapa en traktamentskostnad som används för alla tre exempel.

1. Gå till **Arbetsytor** \> **Utgiftshantering**.
2. Välj **Ny utgiftsrapport** eller markera en befintlig utgiftsrapport.
3. Lägg till en ny utgift. I fältet **Kategori** väljer du **Traktamente**. Välj plats samt start- och slutdatum för resan. Traktamentetillägget för boende, måltider och oförutsedda (övriga) utgifter beräknas utifrån den dagliga ersättning som angetts för den valda platsen.

    Du kan till exempel välja **Redmond (USA)** som plats. Den dagliga ersättningen för den platsen är 150 US-dollar (USD 150) för boende, USD 75 för måltider samt USD 5 för oförutsedda utgifter. Startdatum är den 10 januari och slutdatum är den 14 januari. Den valda varaktigheten är därför fem dagar när den valda konfigurationen är kalenderdagar med tid, och den valda tiden börjar och slutar klockan 12:00 på start- och slutdatum. Detta är beräkningarna:

    - Totalt belopp som ska betalas = 5 × (150 + 75 + 5) = 5 × 230 = USD 1 150
    - Andelen för måltider och oförutsedda utgifter av totalsumman = 5 × (75 + 5) = USD 400

Om frukost, lunch och middag tillhandahållits under resan måste dessa måltider redovisas som måltidsrabatt.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exempel 1: Traktamente där måltidsrabatter baseras på måltidstyp per resa

I det här exemplet är måltidsavdraget 30 procent för frukost, 30 procent för lunch och 40 procent för middag. På sidan **Parametrar för utgiftshantering** anges fältet **Beräkna måltidsreduktion med** som **Måltidstyp per resa**. Här är beräkningarna om den anställde fick tre frukostar, två luncher och noll middagar:

- Måltidsavdrag = (3 × \[75 × 30 %\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Måltider och oförutsedda utgifter = 400 – 112,50 = USD 287,50
- Totalt belopp som ska betalas = Total ersättning – måltidsavdrag = 1 150 –112,50 = USD 1 037,50

![Traktamentesutgift där måltidsavdrag baseras på måltidstyp per resa.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exempel 2: Traktamente där måltidsrabatter baseras på måltidstyp per dag

I det här exemplet är måltidsavdraget 30 procent för frukost, 30 procent för lunch och 40 procent för middag. På sidan **Parametrar för utgiftshantering** anges fältet **Beräkna måltidsavdrag med** som **Måltidstyp per dag**. I det här fallet avmarkerar du kryssrutorna i rutnätet **Måltider** i dialogrutan **Redigera utgift** för att ange vilka måltider som tillhandahållits dig under resan.

Här följer exempelvis beräkningarna som gjordes under de tre första dagarna av resan:

- Avdrag per dag under de första tre dagarna = 75 dagar × 30 % = USD 22,50
- Totalt måltidsavdrag = 3 × 22,50 = USD 67,50
- Måltider och oförutsedda utgiffter för dagarna 1 till 3 = 75 – 22,50 = USD 57,50
- Summa för måltider och oförutsedda utgifter = summan av måltider och oförutsedda utgifter över fem dagar = 400 – 67,50 = USD 332,50
- Totalt belopp som ska betalas = Totalt belopp – måltidsavdrag = 1 150 –67,50 = USD 1 082,50

![Traktamentesutgift där måltidsavdrag baseras på måltidstyp per dag.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exempel 3: Traktamente där måltidsavdrag baseras på antal måltider per dag

I det här exemplet beräknas avdraget utifrån antalet måltider som tillhandahållits per dag (det vill säga fältet **Beräkna måltidsavdrag med** på sidan **Parametrar för utgiftshantering** anges som **Antal måltider per dag**). I rutnätet **Måltider** i dialogrutan **Redigera utgift** rensar du kryssrutorna för att indikera vilka måltider som tillhandahållits.
I det här fallet baseras måltidsavdrahet endast på det # som angavs, och inte på den typ av måltid (frukost/lunch/middag) som tillhandahållits.

Här är beräkningarna för traktamente när den dagliga ersättningen uppgår till USD 150 för boende, USD 75 för måltider samt USD 5 för oförutsedda utgifter:

- **Totalt belopp som ska betalas** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1 150
- **En måltid:** Måltidsrabatt = 20 % = USD 15
- **Två måltider:** Måltidsrabatt = 50 % = USD 37,50
- **Tre måltider:** Måltidsrabatt = 100 % = USD 75

Här är beräkningarna för den **ersättningen för måltider och oförutsedda utgifter**, som inkluderar USD 5 för oförutsedda utgifter:

- Dag 1 – Två tillhandahållna måltider = (75–37,50) + 5 = 37,50 + 5 = USD 42,50
- Dag 2 – Två tillhandahållna måltider = (75–37,50) + 5 = 37,50 + 5 = USD 42,50
- Dag 3 – En tillhandahållen måltid = (75–15) + 5 = 60 + 5 = USD 65
- Dag 4 – Inga tillhandahållna måltider = (75–0) + 5 = 75 + 5 = USD 80
- Dag 5 – Tre tillhandahållna måltider = (75–75) + 5 = 0 + 5 = USD 5

- Totalt för måltider och oförutsedda utgifter = Måltider och oförutsedda utgifter för Dag 1+ Dag 2 +Dag 3+Dag 4+ Dag 5 = USD 235
- Totalt måltidsavdrag = Måltidsavdrag för Dag 1+ Dag 2 +Dag 3+Dag 4+ Dag 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Totalt belopp som ska betalas = Total ersättning – Totalt måltidsavdrag = USD 1 150 – USD 165 = USD 985

![Traktamentesutgift där måltidsavdraget baseras på antalet måltider per dag.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Från och med Finance version 10.0.23 kan du inte skapa traktamentesutgifter med överlappande datum om du använder det omarbetade utgiftsgränssnittet. Om du försöker, kommer du att erhålla ett felmeddelande.
