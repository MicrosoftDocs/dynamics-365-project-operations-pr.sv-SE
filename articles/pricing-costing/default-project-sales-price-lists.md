---
title: Standardprislistor
description: Den här artikeln innehåller information om standard försäljning och kostnadsprislistor i Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410285"
---
# <a name="default-price-lists"></a>Standardprislistor

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

## <a name="sales-price-lists"></a>Försäljningsprislistor

Varje projektoffert och kontrakt i Dynamics 365 Project Operations innehåller en standardprislista. 

### <a name="price-list-default-on-project-quotes"></a>Standardprislista för projektofferter
Systemet slutför följande process för att avgöra vilken prislista som ska vara standard för en projektoffert:

1. Systemet söker efter prislistorna som är kopplade till kontots projektprislistor. 
1. Om det finns inga projektprislistor som är kopplade till kontoposten kontrollerar systemet de försäljningsprislistor som är kopplade till de projektparametrar som överensstämmer med projektoffertens valuta.
1. Därefter kontrollerar systemet giltighetsdatum för de prislistor som överensstämmer med datumintervallet för projektofferten. Mer bestämt det datum då offerten skapades.
1. Om det finns flera prislistor som är giltiga för projektoffertens datum används alla prislistor i enlighet med projektofferten.
1. Om det inte finns några prislistor som gäller datumen för projektofferten finns ingen standardprislista för projekt i projektofferten. Ett varningsmeddelande kommer att visas i projektofferten. Meddelandet anger att faktiska värden och uppskattningar i projektet inte kommer att prissättas eftersom det inte finns några projektprislistor bifogade.

### <a name="price-list-default-on-project-contracts"></a>Standardprislista för projektkontrakt 
Systemet slutför följande process för att avgöra vilken prislista som ska vara standard för ett projektkontrakt:

1. Om kontraktet skapas från en offert kopieras projektprislistorna i offerten separat och kopplas till projektkontraktet.
1. Om kontraktet skapas från grunden söker systemet igenom de prislistor som är kopplade till kontots projektprislistor. Om det inte finns projektprislistor som är kopplade till kontoposten kontrollerar systemet de försäljningsprislistor som är kopplade till de projektparametrar som överensstämmer med projektkontraktets valuta.
1. Därefter kontrollerar systemet giltighetsdatum för de prislistor som överensstämmer med datumintervallet för projektkontraktet. Mer bestämt det datum då kontraktet skapades.
1. Om det finns flera prislistor som är giltiga för kontraktets datum används alla prislistor i enlighet med kontraktet.
1. Om det inte finns några prislistor som gäller datumet för kontraktet används ingen projektprislista i enlighet med kontraktet. Ett varningsmeddelande kommer att visas i projektkontraktet. Meddelandet anger att faktiska värden och uppskattningar i projektet inte kommer att prissättas eftersom det inte finns några projektprislistor bifogade.

## <a name="cost-price-lists"></a>Prislistor för självkostnad

Prislistor för självkostnad hämtas inte från någon entitet i Project Operations. Det görs alltid en bestämning av vilken kostnadsprislista som ska användas per transaktion. Systemet slutför följande process för att avgöra vilken prislista som ska användas för projektkostnader:

1. Systemet söker efter de prislistor som är kopplade till projektets kontrakterande organisationsenhet.
1. Därefter kontrollerar systemet giltighetsdatumet för prislistor som överensstämmer med datumet på inkommande uppskattning eller utfall.

    - *Uppskattning* avser något av tre sammanhang i Project Operations:

        - Projektuppskattningsrad
        - Information om offertrad
        - Kontraktradsinformation

    - *Utfall* avser någon av tre källor till utfall i Project Operations:

       - Inmatningsjournalrader som skapas manuellt, eller korrigeringsjournalrader som skapas i en korrigeringsjournal
       - Journalrader som skapas under inlämningen av tid, utgift eller materialanvändningsloggar
       - Information om fakturarad

    När Project Operations matchar giltighetsdatumet för den inkommande journalraden eller fakturaraden i *utfall* används fältet **Transaktionsdatum**.

    - Om flera prislistor är giltiga vid datumet på den inkommande uppskattningen eller utfallet, väljs den prislista som skapades senast.
    - Om det inte finns prislistor som är kopplade till projektets kontrakterande organisationsenhet kontrollerar systemet de kostnadsprislistor som är kopplade till de projektparametrar som överensstämmer med projektets valuta.

## <a name="enable-multi-currency-cost-price-list"></a>Aktivera prislista för självkostnad för flera valutor

Den här inställningen finns i **Inställningar** \> **Parametrar**. Standardvärdet är **Nej**.

När den här inställningen är aktiverad (det vill säga att värdet är **Ja**) fungerar systemet på följande sätt:

- Då tillåts att kostnadsprislistor i valfri valuta associeras med organisationsenheten. Det går till exempel att bifoga en kostnadsprislista i valutan EUR till en organisationsenhet i valutan USD. Systemet fortsätter att verifiera att kostnadsprislistor som är kopplade till en organisationsenhet inte har överlappande giltighetsdatum.
- Den verifierar att kostnadsprislistor som är kopplade till projektparametrar inte har överlappande giltighetsdatum, även om de har olika valutor. Det här beteendet skiljer sig från standardbeteendet (det vill säga beteendet när värdet anges som **Nej**). I standardbeteendet verifieras endast kostnadsprislistor med **samma** valuta för icke-överlappande giltighetsdatum.
- För ett sammanhang för inkommande transaktioner avgörs kostnadsprislistan endast utifrån giltighetsdatumet. Detta beteende skiljer sig från standardbeteendet, där systemet väljer den kostnadsprislista som överensstämmer med både valutan i projektet och giltighetsdatumet.

På grund av dessa funktionsförändringar kan Project Operations-kunderna ha en global kostnadsprislista som är relevant för hela företaget. De behöver inte ha prislistor i varje valuta för åtgärderna. Den globala prislistan har giltighetsdatum och gör det möjligt att ange kostnadsnivåer i vilken valuta som helst för en specifik kombination av prissättningsvärden. Valutan i kostnadsprislistan används endast för att ange standardvärden när poster för **Rollpriser**, **Kategoripriser** och **Prislista** skapas. Den används inte för att fastställa prislistan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
