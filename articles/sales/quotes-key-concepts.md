---
title: Koncept som är unika för projektbaserade offerter
description: Den här artikeln innehåller information om projektofferter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824374"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncept som är unika för projektbaserade offerter

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Innan du börjar använda projektoffert i Microsoft Dynamics 365 Project Operations du bör vara medveten om följande nyckelbegrepp.

## <a name="owning-company"></a>Ägande företag

Det ägande företaget representerar den juridiska person som äger projektleveransen. Kunden i offerten ska vara en giltig kund i den juridiska entiteten i ekonomi- och driftapparna. Valutan i det att äga företaget och valutan för den kontraktenhet som har valts i en projektbaserad offert måste matcha.

## <a name="contracting-unit"></a>Kontrakteringsenhet

Kontrakteringsenheten representerar den avdelning eller praxis som äger projektleveransen. Du kan konfigurera resurskostnader för varje kontrakteringsenhet. När du anger resurskostnaden för en resurs i kontrakteringsenheten kan du också konfigurera olika kostnadstaxor för resurser som kontrakteringsenheten lånar från, eller annan avdelning eller praxis inom företaget. Denna kostnadstaxa kallas för överföringspriser, resurslån och växelpriser. När du konfigurerar kostnaden för att låna resurser från andra avdelningar kan du också välja att konfigurera dessa kostnadstaxor i valutan för låneavdelningen.

## <a name="cost-currency"></a>Kostnadens valuta

Kostnadsvaluta i Project Operations är den valuta i vilken kostnaderna rapporteras. Valutan härleds från valutan som är kopplad till fältet **Kontrakteringsenhet** i offerten, kontraktet och projektet. Kostnader kan registreras i valfri valuta i ett projekt. Det genomförs dock valutakonvertering från den valuta som kostnaderna bokfördes i till projektets kostnadsvaluta.

På grund av att växelkurserna i Dataverse-plattformen inte kan vara datumeffektiva kan det hända att totalkostnaden på skärmen kan ändras med tiden om du uppdaterar växelkursen. Kostnader som registreras i databasen förblir emellertid oförändrade eftersom beloppen lagras i den valuta de uppkom i.

## <a name="sales-currency"></a>Försäljningsvaluta

Försäljningsvaluta i Project Operations är den valuta som de uppskattade och faktiska försäljningsbeloppen registreras och visas i. Det är också den valuta i vilken kunden faktureras för affären. I en projektoffert är hämtas försäljningsvalutan från kund- eller kontoposten och kan ändras när offerten skapas. När offerten har sparats går det inte att ändra försäljningsvaluta. Förinställda produkt- och projektprislistor ställs in på grundval av försäljningsvalutan i offerten.

Till skillnad från kostnader kan försäljningsvärden **endast** registreras i försäljningsvalutan.

## <a name="billing-method"></a>Faktureringsmetod

Projekt har vanligtvis en fast avgift och konsumtionsbaserade avtalsmodeller. I Project Operations representeras ett projekts kontraktmodell av faktureringsmetoden. Faktureringsmetod har två värden: tid och material eller fast pris.

- **Tid och material** – En förbrukningsbaserad kontrakteringsmodell där varje kostnad backas upp av motsvarande intäkt. När du uppskattar eller ådrar dig fler kostnader ökar även motsvarande uppskattade och faktiska försäljning. Du kan ange gränser som inte ska överskridas för offertrader som har denna faktureringsmetod. På så sätt kan du begränsa den faktiska inkomsten. Uppskattad omsättning påverkas inte av gränser som inte ska överskridas.
- **Fast pris** – En kontrakteringsmodell med fast avgift där försäljningsvärden är oberoende av kostnaderna. Försäljningsvärdet är fast och ändras inte när du uppskattar eller ådrar dig fler kostnader.

## <a name="project-price-lists"></a>Projektprislistor

Projektprislistor är prislistor som används för standardpriser, inte kostnadstaxor, för tid, utgifter och andra projektrelaterade komponenter. Det kan finnas flera prislistor, och varje lista kan ha sin egen datumeffektivitet för varje projektoffert. Project Operations stöder inte överlappande giltighetsdatum i projektprislistor.

## <a name="product-price-lists"></a>Produktprislistor

Produktprislistor är prislistor som används för standardpriser, inte kostnadstaxor för produktbaserade rader i en offert. Det finns bara en produktprislista per offert.

## <a name="transaction-classes"></a>Transaktionsklasser

Project Operations har stöd för fyra typer av transaktionsklasser:

- Tid
- Utgift
- Material
- Avgift

Kostnads- och försäljningsvärden kan uppskattas och uppstå i transaktionsklasserna **Tid**, **Utgifter** och **Material**. **Avgift** är en intäktsklass av transaktioner.

## <a name="work-entities-and-billing-entities"></a>Arbetsentiteter och faktureringsentiteter

Projekt och uppgifter är enheter som representerar arbete. Offertrader och Kontraktrader är enheter som representerar fakturering. Du kan länka olika arbetsentiteter till faktureringsalternativ genom att associera dem med offert- eller kontraktrader.

## <a name="multi-customer-deals"></a>Affärer med flera kunder

Affärer med flera kunder är när det finns fler än en kund som ska faktureras. Här följer några vanliga exempel:

- **Original Equipment Manufacturer (OEM) företag och deras partners** – Partner och återförsäljare säljer en produkt som har mervärdestjänster. Under en affär med en kund erbjuder OEM vanligtvis att finansiera en del av projektet.
- **Projekt inom den offentliga sektorn** – flera avdelningar inom en lokal myndighet är eniga om att finansiera ett projekt och faktureras enligt en på förhand överenskommen uppdelning. Ett skoldistrikt och en kommun eller avdelning av en lokal myndighet är till exempel eniga om att bygga en simbassäng.

## <a name="invoice-schedules"></a>Faktureringsscheman

Faktureringsscheman är specifika för varje offertrad och är valfria. Faktureringsscheman skapas utifrån specifika start- och slutdatum och faktureringsfrekvenser. De används i kontraktfasen när den automatiska skapandeprocessen för fakturor konfigureras. I offertstadiet är faktureringsscheman valfria. Om de skapas under offertstadiet kopieras de till projektkontrakt som skapas när en projektoffert vinns.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Skillnader från Dynamics 365 Sales-offerter

Project Operations-offerter bygger på Dynamics 365 Sales-offerter. Det finns emellertid vissa viktiga skillnader i funktionalitet som du ska vara medveten om:

- Project Operations-offerter har två olika typer av rader, en för projekt och en för produkter.
- Project Operations-offerter har sin egen sida och användargränssnitt (UI) element, affärsregler, affärslogik i plugin-program och skript på klientsidan som skiljer dem från Sales-offerter.
- I Sales kan du bifoga flera beställningar till en enskild försäljningsoffert. I Project Operations kan bara bifoga ett projektkontrakt till en projektoffert.
- När du vinner en försäljningsoffert kan den relaterade affärsmöjligheten vara öppen. När en projektoffert har vunnits stängs den relaterade affärsmöjligheten.
- En försäljningsoffert innehåller inte några fält och begrepp som ingår i en projektoffert. Fälten inkluderar **Kontrakteringsenhet**, **Kontoansvarig** och **Faktureringsadress, kontaktperson**.
- Försäljningsofferter och projektofferter identifieras även av ett alternativbaserat fält **Typ**. För en försäljningsoffert har det här fältet värdet **artikelbaserat**. För projektofferter används värdet **arbetsbaserad**.

På grund av skillnaderna bör du inte använda utbytbara Sales-offerter och Project Operations-offerter.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
