---
title: Transaktionsanslutningar – Länka faktiska värden av olika transaktionstyper
description: I denna artikel beskrivs hur en transaktionskoppling används för att länka faktiska värden av olika typer för att spåra lönsamhet, faktureringseftersläpning och fakturerade kontra ofakturerade intäktsberäkningar.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926108"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transaktionsanslutningar – Länka faktiska värden av olika transaktionstyper

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Transaktionskopplingsposter skapas för att länka faktiska värden av olika typer när tid, utgifter eller materialanvändning flyttas i dess livscykel från offert- eller förförsäljningsstadiet till kontraktstadiet, godkännanden och/eller återkallanden, fakturering och potentiellt kreditering eller korrigeringsfakturering.

I följande exempel visas den vanligaste bearbetningen av tidsposter i en Project Operations projektlivscykel.

> ![Bearbetningstidsposter i Project Operations.](media/basic-guide-17.png)

Förlj dessa steg för bearbetning av tidsposter i en Project Operations-projektlivscykel: 

1. Inlämning av en tidspost innebär att två journalrader skapas: en för kostnad och en för ofakturerad försäljning. 
2. Eventuellt godkännande av en tidspost innebär att två faktiska värden skapas: en för kostnad och en för ofakturerad försäljning. Dessa två faktiska värden kopplas med hjälp av transaktionsanslutningar.
3. När en användare skapar en projektfaktura skapas transaktionen för fakturaraden med hjälp av data från ofakturerat faktiskt försäljningsvärde.
4. När fakturan bekräftas skapar detta två nya faktiska värden: en ofakturerad återföring av försäljning och en fakturerad faktisk försäljning. Återförda ofakturerade försäljningen och den ursprungliga ofakturerade faktiska försäljningen kopplas genom att återföra transaktionskopplingar. Den fakturerade försäljningen och de ursprungliga ofakturerade faktiska försäljningarna kopplas ävne i syfte att visa kopplingarna mellan de intäkter som en gång var eftersläpande eller pågående projekt (WIP) till vad som nu är fakturerad intäkt.   

Varje händelse i bearbetningsarbetsflödet utlöser skapandet av poster i tabellen för **transaktionskoppling**. Detta hjälper till att skapa en spårning av relationerna mellan de poster som skapas över tidsinmatning, journalrad, faktiska värden och fakturaradsinformation.

I följande tabell visas posterna i entiteten för **transaktionskoppling** för föregående arbetsflöde.

|Händelse                   |Transaktion 1                 |Transaktion 1 roll |Transaktion 1 typ       |Transaktion 2          |Transaktion 2 roll |Transaktion 2 typ |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Skicka tidspost   |Journalrad (försäljning) GUID     |Ofakturerad försäljning |msdyn_journalline            |Journalrad (kostnad) GUID     |Kostnad            |msdyn_journalline  |
|Tidsgodkännande           |Ofakturerad faktisk (försäljning) GUID  |Ofakturerad försäljning |msdyn_actual                 |Faktisk kostnad (kostnad) GUID       |Kostnad            |msdyn_actual       |
|Skapa faktura        |Information om fakturarad GUID      |Fakturerad försäljning   |msdyn_invoicelinetransaction |Ofakturerad faktisk försäljning GUID   |Ofakturerad försäljning  |msdyn_actual       |
|Bekräfta faktura    |Återföra faktiskt värde GUID         |Återföring      |msdyn_actual                 |Ursprunglig ofakturerad försäljning GUID |Ursprunglig        |msdyn_actual       |
|                        |Fakturerad försäljning GUID             |Fakturerad försäljning   |msdyn_actual                 |Ofakturerad faktisk försäljning GUID   |Ofakturerad försäljning  |msdyn_actual       |
|Korrigeringsfaktura, utkast |Transaktion på fakturaraden GUID|Utbyte      |msdyn_invoicelinetransaction |Fakturerad försäljning GUID            |Ursprunglig        |msdyn_actual       |
|Bekräfta fakturakorrigering|Fakturerad återförd försäljning GUID  |Återföring      |msdyn_actual                 |Fakturerad försäljning GUID            |Ursprunglig        |msdyn_actual       |
|                        |Nytt GUID för ofakturerad försäljning |Utbyte            |msdyn_actual                 |Fakturerad försäljning GUID            |Ursprunglig        |msdyn_actual       |


I följande illustration visas de kopplingar som skapas mellan olika typer av faktiska värden olika händelser med hjälp av ett exempel på tidsposter i Project Operations.

> ![Hur faktiska värden av olika typer kopplas till varandra i Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
