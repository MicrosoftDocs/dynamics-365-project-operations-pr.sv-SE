---
title: Arbeta med datamodellen Project Service Automation
description: I det här ämnet finns information om hur du arbetar med datamodellen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8d63a1b36abe0a154c43e99738340f32f28c2f5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120295"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Arbeta med datamodellen Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation utökar andra app-entiteter och presenterar egna entiteter i Common Data Service datamodellen. I det här ämnet beskrivs några av de entiteter som du kommer att stöta på i vanliga scenarier för PSA-rapportering.

## <a name="reporting-on-opportunities"></a>Rapportera affärsmöjligheter

Project Service Automation utvidgar entiteten **affärsmöjlighet** för Dynamics 365 Sales genom att lägga till fält som aktiverar projektbaserade scenarier. De här fälten identifieras med ett schemanamn som föregås av **msdyn\_**. Ett nytt fält som är viktigt för rapportering av PSA-affärsmöjligheter är **ordertyp**. Ett värde för **arbetsbaserat** på det här fältet anger att affärsmöjligheten är en PSA-möjlighet. Andra fält som har lagts till i entiteten omfattar **Avtalande organisation** som hämtar den organisation som innehar affärsmöjligheten och **kontoansvarig**, som hämtar namnet på den kontoansvarige som är ansvarig för affärsmöjligheten.

Entiteten för **affärsmöjlighet** innehåller även fält som är relaterade till Project Service. **Faktureringsmetod** anger om affärsmöjlighetsraden ska faktureras utifrån tid och material eller med fastpris och **projekt** hämtar namnet på det projekt som ska säkerhetskopiera affärsmöjligheten. Andra fält som du kan skapa en rapport över hämta kostnader och kundens budgetbelopp för radartikeln.

## <a name="reporting-on-quotes"></a>Rapportering om offerter

PSA utökar entiteten för Sales **offert** genom att lägga till projektrelaterade fält. **Ordertypen** skiljer på PSA-offerter från icke-PSA-offerter. Ett värde för **arbetsbaserat** på det här fältet anger att offerten är en PSA-offert. Andra fält som kan vara relevanta för rapportering på PSA-offerter inkluderar beloppsfält, t.ex. **debiterbara kostnader**, **icke debiterbara kostnader**, **bruttomarginal**, **uppskattningar** och **budget**. Andra användbara fält anger om offerten är lönsam, om den ska vara avslutad i schemat och om den uppfyller kundens budgetförväntningar.

PSA utvidgar även entiteten försäljning **offertrad**. Ett fält som PSA lägger till är **faktureringsmetod** som anger hur offertraden ska faktureras (tid och material eller fast pris). Andra fält som har lagts till i entiteten har skapat ett närliggande projekt som ska säkerhetskopiera offertraden, fakturering, kostnad och budget.

PSA lägger också till nya entiteter som är relaterade till datamodellen Dynamics 365. Här följer några exempel:

- **Information om offertrad** – entiteten innehåller projektets beräkningsinformation för offertraden. Den har två poster för varje offertrad. En post lagrar kostnad och kostnadsinformation för offertraden och den andra posten lagrar försäljningsbeloppet och försäljningsinformationen för offertraden.
- **Faktureringsschema för offertrad** – entiteten innehåller faktureringsschema för offertraden. Schemat skapas utifrån den faktureringsfrekvens som tilldelas offertraden.
- **Milstolpe för offertrad** – den här entiteten innehåller faktureringsmilstolpar för offertrader med fast pris.
- **Analyssammanfattning av offertrad** – entiteten innehåller ekonomisk information för offertraden. Informationen kan användas för rapportering av offererad försäljning och beräknade kostnadsbelopp efter olika dimensioner.

Andra entiteter som PSA lägger till i offerter är **Prislista för projekt för offertrad**, **Resurskategori för offertrad** och **Transaktionskategori för offertrad**.

![Diagram som visar citat, en offertrad och projektrelationer](media/PS-Reporting-image2.png "Diagram som visar citat, en offertrad och projektrelationer")

## <a name="reporting-on-project-contracts"></a>Rapportering om projektkontrakt

PSA utökar entiteten för försäljning **order** som används när projektkontrakt registreras. Det lägger till ett viktigt nytt fält **ordertyp** som identifierar kontraktet som ett PSA-projekt i stället för en försäljningsorder. Ett värde för **arbetsbaserat** på det här fältet anger att ordern är ett PSA-projektkontrakt. Andra nya fält som läggs till i entiteten **Order** hämtar information om kostnader, PSA-kontraktstatus och den organisation som äger kontraktet.

PSA utvidgar även entiteten försäljning **Säljorderrader**. Bland de fält som läggs till finns fält som hämtar faktureringsmetoden (tid och material eller fast pris), kundbudgetbelopp och underliggande projekt.

PSA lägger också till nya entiteter som är utformade för projektkontrakt. Här följer några exempel:

- **Information om projektkontraktrad** – entiteten innehåller information om radnivå som slås samman till kontraktradbeloppet. Detta kan vara så detaljerad som radartiklar som skapas från ett projektschema på uppgiftsnivå.
- **Faktureringsschema för kontraktrad** – den här entiteten innehåller det faktureringsschema som skapas utifrån den fakturafrekvens som tilldelats kontraktraden.
- **Milstolpe för kontraktet** – entiteten innehåller faktureringsmilstolpar för kontraktrader som har en faktureringsperiod med fast pris.

Andra entiteter som PSA lägger till i kontrakt är **Prislista för projektkontraktrad**, **Resurskategori för projektkontraktrad** och **Transaktionskategori för projektkontraktrad**.

![Diagram som visar order, orderrad och projektrelationer](media/PS-Reporting-image3.png "Diagram som visar order, orderrad och projektrelationer")

## <a name="reporting-on-projects"></a>Rapportering om projekt

Entiteten **projekt** och den relaterade entiteten är exklusiva till PSA. **Projekt** är den översta entiteten som används för att hämta arbete och kostnadssida för åtgärder. Här följer en lista över relaterade entiteter:

- **Projektteammedlem** – den här entiteten innehåller information om de bokningsbara resurser som har tilldelats projektet. Resurserna kan vara allmänna bokningsbara resurser, eller så kan de heta bokningsbara resurser som antingen anges av projektledaren eller genererats från projektschemat.
- **Projektuppgift** – den här entiteten innehåller de uppgifter som projektplanen eller schemat utgör.
- **Resurstilldelning** – den här entiteten innehåller uppgiftstilldelningen för bokningsbara resursen.
- **Resurskrav** – den här entiteten innehåller krav för alla generiska resursteammedlemmar.
- **Beräkna** och **Beräkna rad** – de här entiteterna har ett huvud/rad-förhållande och innehåller utgiftsberäkningar för projektet. Uppgiftsberäkningar lagras i entiteten **resursberäkning**.

![Diagram som visar resurskrav och projektrelationer](media/PS-Reporting-image4.png "Diagram som visar resurskrav och projektrelationer")

## <a name="reporting-on-resources"></a>Rapportering av resurser

Projektresurser använder entiteten **Bokningsbar resurs** från Universal Resource Scheduling (URS) som delas med andra program, t.ex. Microsoft Dynamics 365 Field Service. Här följer en lista över de entiteter som du kan behöva använda när du rapporterar till projektresurser:

- **Bokningsbar resurs** – den här entiteten representerar användaren, kontakten, den generiska resursen, kontot, gruppen eller utrustningen som används i projektteamet.
- **Egenskaper för bokningsbar resurs** – entiteten innehåller kunskaper, certifieringar eller utbildning för resursen. Egenskaperna kan ha klassificeringsvärden som definieras av bedömningsmodellen.
- **Kategori för bokningsbar resurs** – entiteten representerar den bokningsbara resursens roll.
- **Bokningar för bokningsbar resurs** – entiteten motsvarar den tid som har bokats på projekt för resursen. Varje bokning har både en huvudentitet och radentiteter och varje rad har en status som representerar bokningens status.

![Diagram som visar bokningsbara resurser och egenskapsrelationer](media/PS-Reporting-image5.png "Diagram som visar bokningsbara resurser och egenskapsrelationer")

## <a name="reporting-on-actual-transactions"></a>Rapportering av faktiska transaktioner

När du godkänner en tidsrapport eller en utgift eller fakturerar ett kontrakt i PSA, registreras affärstransaktionen i den **faktiska** entiteten. Entiteten kan ligga till grund för nästan alla ekonomiska relaterade rapporter i PSA. Den **faktiska** entiteten hämtar kostnads- och försäljningstransaktioner för affärshändelsen. Dessutom hämtas många relevanta attribut.

När du arbetar med den **faktiska** entiteten är det viktigt att du förstår vilken transaktion eller vilka transaktioner som registreras i entiteten och när transaktionerna registreras. Nedan visas ett typiskt flöde när du arbetar med tidstransaktioner (flödet för utgiftsposter är liknande):

1. När tidsposten sparas skapas inga poster i den **faktiska** entiteten.
2. När tidsposten sparas skickas inga poster i den **faktiska** entiteten.
3. När tidsposten har godkänts skapas en post i den **faktiska** entiteten och en andra post kan också skapas. I den första posten lagrar kostnaden för tidsposten. I den andra posten lagras det ofakturerade försäljningsbeloppet för tidsposten. Den andra posten är beroende av att projektet antingen har en kund, en offert eller en kontraktrad tilldelad.

    | Dokumentdatum | Transaktionstyp | Transaktionsklass | Kund         | Kontrakt   | Resurs     | Resursroll | Faktureringstyp | Kvantitet | Enhetspris | Belopp |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Kostnad             | Time              | Alpine Ski House | Alpine CRM | Greta Andreasson | Projektledare   | Debiterbart   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Ofakturerad försäljning   | Time              | Alpine Ski House | Alpine CRM | Greta Andreasson | Projektledare   | Debiterbart   | 8.0      | 100.00     | 800.00 |

    De här två posterna är separata men relaterade poster. De är varken debet eller kredit.

4. Om ett kontrakt är associerat med projektet skapas ytterligare två poster i den **aktuella** entiteten när tidsposten faktureras. Först skapas ett negativt belopp för den fakturerade försäljningsposten. Den här posten återför den fakturerade försäljningen. För det andra skapas en transaktion för den fakturerade försäljningen. De här posterna är emellertid åtskilda men relaterade poster, inte debet och kredit.

    | Dokumentdatum | Transaktionstyp | Transaktionsklass | Kund         | Kontrakt   | Resurs     | Resursroll | Faktureringstyp | Kvantitet | Enhetspris | Belopp   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Ofakturerad försäljning   | Time              | Alpine Ski House | Alpine CRM | Greta Andreasson | Projektledare   | Debiterbart   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Fakturerad försäljning     | Time              | Alpine Ski House | Alpine CRM | Greta Andreasson | Projektledare   | Debiterbart   | 8.0      | 100.00     | 800.00   |

Entitetsposten **Transaktionsursprung** registrerar ursprunget för **faktiska** posten och entiteten **Transaktionskoppling** registrerar relaterade poster för **faktisk** post. Dessutom innehåller den **faktiska** posten refererar till projektet, projektkontraktet (ordern), bokningsbar resurs och kunden.

![Diagram över transaktionsanslutning, ursprung och faktiska relationer](media/PS-Reporting-image6.png "Diagram över transaktionsanslutning, ursprung och faktiska relationer")
