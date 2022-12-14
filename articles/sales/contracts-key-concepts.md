---
title: Koncept som är unika för projektbaserade kontrakt
description: Den här artikeln innehåller information om huvudkoncepten i projektkontrakt i Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 48053bf6209d0a997e4e8766e29d77f994da06b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825869"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Koncept som är unika för projektbaserade kontrakt

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_



Den här artikeln innehåller grundläggande begrepp som du bör känna till innan du börjar använda Projektkontrakt i Dynamics 365 Project Operations:

## <a name="owning-company"></a>Ägande företag

Det ägande företaget är den juridiska personen från modulen **Projekthantering- och redovisning** för Project Operations från Dynamics 365 Finance. Det ägande företaget representerar den juridiska personen som redovisar kostnaden och intäkterna från en affär.

## <a name="contracting-unit"></a>Kontrakteringsenhet

Kontrakteringsenheten representerar den avdelning eller praxis som äger projektleveransen. Du kan konfigurera resurskostnader för varje kontrakteringsenhet. När du anger resurskostnaden för en resurs kan du också ange olika kostnadstaxor för resurser. Den kontrakterande enheten lånar dessa resurser från annan avdelning eller praxis inom företaget. Kostnadstaxor för resurser kallas för överföringspriser, resurslån eller växelpriser. När du konfigurerar kostnadstaxan för att låna resurser från andra avdelningar använder du valutan för låneavdelningen.

## <a name="cost-currency"></a>Kostnadens valuta

Kostnadsvaluta är den valuta i vilken kostnaderna rapporteras på skärmen. Valutan härleds från valutan som är kopplad till fältet **Kontrakteringsenhet** i kontraktet och projektet. Kostnader kan loggas i valfri valuta i ett projekt. Det genomförs dock valutakonvertering från den valuta som kostnaderna bokfördes i till projektets kostnadsvaluta när den visas på skärmen.

På grund av att växelkurserna i Common Data Service-plattformen (CDS) inte kan vara datumeffektiva kan det hända att totalkostnaden på skärmen kan ändras med tiden om du uppdaterar växelkursen. Kostnader som registreras i databasen förblir emellertid oförändrade eftersom beloppen lagras i den valuta de uppkom i.

## <a name="sales-currency"></a>Försäljningsvaluta

Försäljningsvaluta i Project Operations är den valuta som de uppskattade och faktiska försäljningsbeloppen registreras och visas i. Försäljningsvaluta är också den valuta i vilken kunden faktureras för affären. I ett projektkontrakt hämtas försäljningsvalutan från kund- eller kontoposten och kan ändras när kontraktet skapas. När ett kontrakt skapas genom att en offert stängs som vunnen, används valutan i kontraktet som standard från valutan i offerten.

När du skapar ett projektkontrakt från grunden går det inte att redigera fältet **Försäljningsvaluta**. Prislistor för produkt och projekt hämtas på grundval av denna valuta i kontraktet.

Till skillnad från kostnader kan försäljningsvärden endast registreras i försäljningsvalutan.

## <a name="billing-method"></a>Faktureringsmetod

Det finns vanligtvis två typer av kontrakteringsmodeller för projekt, fast avgift och konsumtionsbaserad. Dessa modeller representeras i Project Operations som faktureringsmetoder med två möjliga värden:

- Tid och material: en förbrukningsbaserad kontrakteringsmodell där varje kostnad backas upp av motsvarande intäkt. När du uppskattar eller ådrar dig fler kostnader ökar även motsvarande uppskattade och faktiska försäljning. Ange gränser som inte får överskridas på kontraktrader som har den här faktureringsmetoden, som utgör ett tak för den faktiska intäkten. Uppskattad omsättning påverkas inte av gränser som inte ska överskridas.
- Fast pris: en kontrakteringsmodell med fast avgift som anger att försäljningsvärden blir oberoende av kostnaderna. Försäljningsvärdet är fast och ändras inte när du uppskattar eller ådrar dig fler kostnader.

## <a name="project-price-lists"></a>Projektprislistor

Projektprislistor används för standardpriser, inte kostnadstaxor, för tid, utgifter och andra projektrelaterade komponenter. Det kan finnas flera prislistor. Varje prislista har ett eget giltighetsdatum för varje projektkontrakt. Överlappande giltighetsdatum i projektprislistor stöds inte i Project Operations.

När ett projektkontrakt skapas genom att vinna en projektoffert kopieras projektprislistorna med kontraktnamnet och datumet. Kopiering av den här informationen utgör en anpassad prissättning för projektkomponenter i projektkontraktet.

## <a name="transaction-classes"></a>Transaktionsklasser

Project Operations har stöd för fyra typer av transaktionsklasser:

- Tid
- Utgift
- Material
- Avgift

Kostnads- och försäljningsvärden kan uppskattas och uppstå i transaktionsklasserna Tid, Utgifter och Material. Avgift är en intäktsklass av transaktioner.

## <a name="work-entities-and-billing-entities"></a>Arbetsentiteter och faktureringsentiteter

Entiteter som representerar arbete är projekt och uppgifter. Entiteter som representerar faktureringsaspekter är kontraktrader. Du kan knyta olika arbetsentiteter till faktureringsalternativ genom att koppla dem till kontraktrader.

## <a name="multi-customer-deals"></a>Affärer med flera kunder

Affärer med flera kunder har fler än en kund som ska faktureras i en affär. Vanliga exempel på detta:

- OEM-företag och deras partner: partner och återförsäljare säljer en produkt med några mervärdestjänster och som vanligtvis innebär en särskild affär med kunden. OEM-tillverkaren kan finansiera en del av projektet. 

- Projekt inom den offentliga sektorn: flera avdelningar inom en lokal myndighet är eniga om att finansiera ett projekt och faktureras enligt en på förhand överenskommen uppdelning. Ett skoldistrikt och kommunen är till exempel eniga om att bygga en simbassäng.

## <a name="invoice-schedules"></a>Faktureringsscheman

Faktureringsscheman är specifika för varje kontraktrad och krävs för att automatisk fakturering ska fungera. Faktureringsscheman skapas utifrån vissa start- och slutdatum och faktureringsfrekvenser. Faktureringsscheman används i kontraktfasen när den automatiska skapandeprocessen för fakturor konfigureras. När ett projektkontrakt skapas från en offert kopieras faktureringsschemat till projektkontraktet från offerten.

## <a name="changes-from-dynamics-365-sales-orders"></a>Ändringar från Dynamics 365 Sales-order

Kontrakt i Project Operations bygger på order i Dynamics 365 Sales. Det finns emellertid viktiga avvikelser och skillnader i funktionerna. Kontrakt har sina egna formulär och gränssnittselement, affärsregler, affärslogik i plugin-program och skript på klientsidan som gör dem unika från order. Av dessa skäl bör du inte använda en Sales-order och ett Project Operations-kontrakt på samma sätt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
