---
title: Viktiga begrepp i projektofferter
description: I det här ämnet finns information om hur du använder projektofferter i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896303"
---
# <a name="project-quote-key-concepts"></a>Viktiga begrepp i projektofferter

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_


Följande är viktiga begrepp som du bör känna till innan du börjar använda projektofferter i Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Kontrakteringsenhet

Kontrakteringsenheten representerar den avdelning eller praxis som äger projektleveransen. Du kan konfigurera resurskostnader för varje kontrakteringsenhet. När du anger resurskostnaden för en resurs i kontrakteringsenheten kan du också konfigurera olika kostnadstaxor för resurser som kontrakteringsenheten lånar från, eller annan avdelning eller praxis inom företaget. Detta kallas för överföringspriser, resurslån och växelpriser. När du konfigurerar kostnaden för att låna resurser från andra avdelningar kan du också välja att konfigurera dessa kostnadstaxor i valutan för låneavdelningen.

## <a name="cost-currency"></a>Kostnadens valuta

Kostnadsvaluta i Project Operations är den valuta i vilken kostnaderna rapporteras. Valutan härleds från valutan som är kopplad till fältet **Kontrakteringsenhet** i offerten, kontraktet och projektet. Kostnader kan loggas i valfri valuta i ett projekt. Det genomförs dock valutakonvertering från den valuta som kostnaderna bokfördes i till projektets kostnadsvaluta.

På grund av att växelkurserna i CDS-plattformen inte kan vara datumeffektiva kan det hända att totalkostnaden på skärmen kan ändras med tiden om du uppdaterar växelkursen. Kostnader som registreras i databasen förblir emellertid oförändrade eftersom beloppen lagras i den valuta de uppkom i.

## <a name="sales-currency"></a>Försäljningsvaluta

Försäljningsvaluta i Project Operations är den valuta som de uppskattade och faktiska försäljningsbeloppen registreras och visas i. Det är också den valuta i vilken kunden faktureras för affären. I en projektoffert är hämtas försäljningsvalutan från kund- eller kontoposten och kan ändras när offerten skapas. När offerten har sparats går det inte att ändra försäljningsvaluta. Prislistor för produkt och projekt hämtas på grundval av försäljningsvalutan i offerten.

Till skillnad från kostnader kan försäljningsvärden endast registreras i försäljningsvalutan.

## <a name="billing-method"></a>Faktureringsmetod

Projekt har vanligtvis en fast avgift och konsumtionsbaserade avtalsmodeller. Detta representeras i Project Operations som **Faktureringsmetod** och har två värden: Tid och material och Fast pris.

- **Tid och material:** det här är en förbrukningsbaserad avtalsmodell där varje kostnad backas upp av motsvarande intäkt. När du uppskattar eller ådrar dig fler kostnader ökar även motsvarande uppskattade och faktiska försäljning. Du kan ange gränser som inte ska överskridas för offertrader som har denna faktureringsmetod. Detta blir taket för den faktiska intäkten. Uppskattad omsättning påverkas inte av gränser som inte ska överskridas.
- **Fast pris:** det här är en avtalsmodell med fast avgift som anger att försäljningsvärden blir oberoende av kostnaderna. Försäljningsvärdet är fast och ändras inte när du uppskattar eller ådrar dig fler kostnader.

## <a name="project-price-lists"></a>Projektprislistor

Projektprislistor är prislistor som används för standardpriser, inte kostnadstaxor, för tid, utgifter och andra projektrelaterade komponenter. Det kan finnas flera prislistor, och varje lista kan ha sin egen datumeffektivitet för varje projektoffert. Överlappande datumeffektivitet i projektprislistor stöds in i Project Operations.

## <a name="product-price-lists"></a>Produktprislistor

Produktprislistor är prislistor som används för standardpriser, inte kostnadstaxor för produktbaserade rader i en offert. Det finns bara en produktprislista per offert.

## <a name="transaction-classes"></a>Transaktionsklasser

Project Operations har stöd för fyra typer av transaktionsklasser:

- Tid
- Utgift
- Material
- Avgift

Kostnads- och försäljningsvärden kan uppskattas och uppstå i transaktionsklasserna Tid, Utgifter och Material. Avgift är en intäktsklass av transaktioner.

## <a name="work-entities-and-billing-entities"></a>Arbetsentiteter och faktureringsentiteter

Entiteter som representerar arbete är Projekt och Uppgifter. Entiteter som representerar faktureringar är Offertrader och Kontraktrader. Du kan länka olika arbetsentiteter till faktureringsalternativ genom att associera dem med offert- eller kontraktrader.

## <a name="multi-customer-deals"></a>Affärer med flera kunder

Affärer med flera kunder är när det finns fler än en kund som ska faktureras. Vanliga exempel på detta:

- **OEM-företag och deras partner:** partner och återförsäljare säljer en produkt som har mervärdestjänster. Det här är vanligtvis ett scenario där du under en specifik affär med en kund har OEM-företaget möjlighet att finansiera en del av projektet. 

- **Projekt inom den offentliga sektorn:** flera avdelningar inom en lokal myndighet är eniga om att finansiera ett projekt och faktureras enligt en på förhand överenskommen uppdelning. Ett skoldistrikt och en kommun eller avdelning av en lokal myndighet är till exempel eniga om att bygga en simbassäng.

## <a name="invoice-schedules"></a>Faktureringsscheman

Faktureringsscheman är specifika för varje offertrad och är också valfria. Faktureringsscheman skapas utifrån vissa start- och slutdatum och faktureringsfrekvenser. Faktureringsscheman används i kontraktfasen när den automatiska skapandeprocessen för fakturor konfigureras. I offertstadiet är scheman valfria. När du skapar faktureringsscheman i steget **Offert** kopieras de till projektkontrakt som skapas när en projektoffert vinns.

## <a name="changes-from-dynamics-365-sales-quote"></a>Ändringar från Dynamics 365 Sales-offert:

Project Operations-offerter bygger på Dynamics 365 Sales-offerter. Det finns emellertid vissa viktiga skillnader i funktionalitet som du ska vara medveten om:

- Åtgärderna **Revidera** och **Aktivera** stöds inte.
- Project Operations-offerter har två olika typer av rader. Den ena är för projekt och den andra är för produkter.
- Project Operations-offerter har sina egna formulär och gränssnittselement, affärsregler, affärslogik i plugin-program och skript på klientsidan som gör dem unika från Sales-offerter.

Av dessa anledningar bör du inte använda en Sales-offert och en Project Operations-offert på samma sätt.
