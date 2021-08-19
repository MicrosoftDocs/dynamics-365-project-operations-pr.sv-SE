---
title: Länka utfall till ursprungliga poster
description: Detta ämne beskriver hur du länkar faktiska värden till ursprungliga poster, till exempel tidspost, utgiftspost eller materialanvändningsloggar.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991778"
---
# <a name="link-actuals-to-original-records"></a>Länka utfall till ursprungliga poster

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


I Dynamics 365 Project Operations är *affärstransaktion* ett abstrakt koncept som inte representeras av någon entitet. Vissa vanliga fält och processer i entiteter är dock utformade för att använda begreppet affärstransaktioner. Följande entiteter använder detta koncept:

- Information om offertrad
- Information om kontraktrad
- Beräkningsrader
- Journalrader
- Faktiska värden

Av dessa entiteter mappas **Information om offertrad**, **Information om kontraktrad** och **Beräkningsrader** till beräkningsfasen i projektlivscykeln. Entiteterna **Journalrader** och **Faktiska värden** mappas till körningsfasen i projektlivscykeln.

Project Operations känner igen poster i dessa fem entiteter som affärstransaktioner. Den enda skillnaden är att poster i entiteter som är mappade till beräkningsfasen betraktas som ekonomiska prognoser, medan posterna i entiteter som är mappade till körningsfasen betraktas som ekonomiska fakta som redan har inträffat.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncept som är unika för affärstransaktioner
Följande koncept är unika för begreppet affärstransaktioner:

- Transaktionstyp
- Transaktionsklass
- Transaktionens ursprung
- Transaktionskoppling

### <a name="transaction-type"></a>Transaktionstyp

Transaktionstyp representerar tidpunkten för och sammanhanget mellan de ekonomiska konsekvenserna för ett projekt. Den representeras av ett alternativuppsättning som har följande värden som stöds i Project Operations:

  - Kostnad
  - Projektkontrakt
  - Ofakturerad försäljning
  - Fakturerad försäljning
  - Försäljning inom organisationen
  - Kostnad för resursenhet

### <a name="transaction-class"></a>Transaktionsklass

Transaktionsklass representerar de olika typer av kostnader som uppstår i projekt. Den representeras av ett alternativuppsättning som har följande värden som stöds i Project Operations:

  - Tid
  - Utgift
  - Material
  - Avgift
  - Milstolpe
  - Moms

Värdet **milstolpe** används vanligtvis av affärslogiken för fakturering i fast pris i Project Operations.

### <a name="transaction-origin"></a>Transaktionens ursprung

**Transaktionsursprung** är en entitet som lagrar ursprunget för varje affärstransaktion. När ett projekt pågår ger varje affärstransaktion upphov till en annan affärstransaktion, som i sin tur skapar en annan och så vidare. Entiteten för transaktionens ursprung har utformats för att lagra data om varje transaktioners ursprung, så att det blir mer rapportering och spårning. 

### <a name="transaction-connection"></a>Transaktionskoppling

**Transaktionskoppling** är en entitet som lagrar relationen mellan två liknande affärstransaktioner, t.ex. kostnader och relaterade verkliga försäljningar, eller transaktionsåterföringar som startas av faktureringsaktiviteter som fakturabekräftelse eller fakturakorrigering.

Tillsammans kan du med hjälp av **transaktionsursprunget** och **transaktionskoppling** spåra relationer mellan affärstransaktioner och åtgärder som medför att en specifik affärstransaktion skapas.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exempel: hur transaktionens ursprung fungerar med transaktionskoppling

I följande exempel visas den vanligaste bearbetningen av tidsposter i en Project Operations projektlivscykel.

> ![Bearbetning av hela tiden i en Project Service-livscykel.](media/basic-guide-17.png)
 
1. Ett tidsinläggsinlämnande skapar två journalrader: en rad för kostnad och en rad för obefintlig försäljning.
2. Eventuellt godkännande av en tidspost skapar två faktiska värden: en faktisk för kostnad och ett faktiskt värde för ofakturerad försäljning.
3. När en ny projektfaktura skapas kommer transaktionen för fakturaraden med hjälp av data från ofakturerat faktiskt försäljningsvärde. 
4. När fakturan bekräftas skapas två nya faktiska värden: en ofakturerad återföring av faktisk försäljning och en fakturerad faktisk försäljning.

Var och en av dessa händelser skapar en post i entiteterna **Transaktionens ursprung** och **Transaktionsanslutning**. Med hjälp av de här nya posterna kan relationer skapa en historik mellan posterna som skapas över tidspost, rad, faktiska värden och fakturaradsinformation.

I följande tabell visas posterna i entiteten för **transaktionens ursprung** för arbetsflöde.

| Händelse                        | Ursprung                   | Ursprungstyp                       | Transaktion                       | Transaktionstyp         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Skicka tidspost        | Registrera tidspost GUID   | Tidspost                        | Post för journalrad GUID (kostnad)   | Journalrad             |
| Registrera tidspost GUID       | Tidspost               | Post för journalrad GUID (försäljning)  | Journalrad                      |                          |
| Tidsgodkännande                | Post för journalrad GUID | Journalrad                      | Ofakturerad försäljningspost GUID        | Faktiskt                   |
| Registrera tidspost GUID       | Tidspost               | Ofakturerad försäljningspost GUID        | Faktiskt                            |                          |
| Post för journalrad GUID     | Journalrad             | Faktisk kostnadspost GUID           | Faktiskt                            |                          |
| Registrera tidspost GUID       | Tidspost               | Faktisk kostnadspost GUID           | Faktisk                            |                          |
| Skapa faktura             | Registrera tidspost GUID   | Tidspost                        | Transaktion på fakturaraden GUID     | Transaktion på fakturaraden |
| Post för journalrad GUID     | Journalrad             | Transaktion på fakturaraden GUID     | Transaktion på fakturaraden          |                          |
| Bekräfta faktura         | Fakturarad GUID        | Fakturarad                      | Fakturerad försäljningspost GUID          | Faktiskt                   |
| Faktura GUID                 | Faktura                  | Fakturerad försäljningspost GUID          | Faktiskt                            |                          |
| Information om fakturarad GUID     | Information om fakturarad      | Fakturerad försäljningspost GUID          | Faktiskt                            |                          |
| Registrera tidspost GUID       | Tidspost               | Fakturerad försäljningspost GUID          | Faktiskt                            |                          |
| Post för journalrad GUID     | Journalrad             | Fakturerad försäljningspost GUID          | Faktiskt                            |                          |
| Registrera tidspost GUID       | Tidspost               | Ofakturerad återförd försäljning GUID      | Faktiskt                            |                          |
| Post för journalrad GUID     | Journalrad             | Ofakturerad återförd försäljning GUID      | Faktiskt                            |                          |
| Korrigeringsfaktura, utkast     | Gammal ILD-GUID             | Transaktion på fakturaraden          | Korrigering ILD GUID               | Transaktion på fakturaraden |
| Gammal FR GUID                  | Fakturarad             | Korrigering ILD GUID               | Transaktion på fakturaraden          |                          |
| Gammal faktura GUID             | Faktura                  | Korrigering ILD GUID               | Transaktion på fakturaraden          |                          |
| Registrera tidspost GUID       | Tidspost               | Korrigering ILD GUID               | Transaktion på fakturaraden          |                          |
| Post för journalrad GUID     | Journalrad             | Korrigering ILD GUID               | Transaktion på fakturaraden          |                          |
| Bekräftad fakturakorrigering | Gammal ILD-GUID             | Transaktion på fakturaraden          | Återförd fakturerad faktisk försäljning GUID | Faktiskt                   |
| Gammal FR GUID                  | Fakturarad             | Återförd fakturerad faktisk försäljning GUID | Faktiskt                            |                          |
| Gammal faktura GUID             | Faktura                  | Återförd fakturerad faktisk försäljning GUID | Faktiskt                            |                          |
| Registrera tidspost GUID       | Tidspost               | Återförd fakturerad faktisk försäljning GUID | Faktiskt                            |                          |
| Post för journalrad GUID     | Journalrad             | Återförd fakturerad faktisk försäljning GUID | Faktiskt                            |                          |
| Gammal ILD-GUID                 | Transaktion på fakturaraden | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Gammal FR GUID                  | Fakturarad             | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Gammal faktura GUID             | Faktura                  | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Registrera tidspost GUID       | Tidspost               | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Post för journalrad GUID     | Journalrad             | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Korrigering ILD GUID          | Transaktion på fakturaraden | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Korrigering FR GUID           | Fakturarad             | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |
| Korrigeringsfaktura GUID      | Faktura                  | Ny ofakturerad faktisk försäljning GUID    | Faktiskt                            |                          |

I följande tabell visas posterna i entiteten för **Transaktionskoppling** för arbetsflöde.

| Händelse                          | Transaktion 1                 | Transaktion 1 roll | Transaktion 1 typ           | Transaktion 2                | Transaktion 2 roll | Transaktion 2 typ |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Skicka tidspost          | Journalrad (försäljning) GUID     | Ofakturerad försäljning     | msdyn_journalline            | Journalrad (kostnad) GUID     | Kostnad               | msdyn_journalline  |
| Tidsgodkännande                  | Ofakturerad faktisk (försäljning) GUID  | Ofakturerad försäljning     | msdyn_actual                 | Faktisk kostnad (kostnad) GUID       | Kostnad               | msdyn_actual       |
| Skapa faktura               | Information om fakturarad GUID      | Fakturerad försäljning       | msdyn_invoicelinetransaction | Ofakturerad faktisk försäljning GUID   | Ofakturerad försäljning     | msdyn_actual       |
| Bekräfta faktura           | Återföra faktiskt värde GUID         | Återföring          | msdyn_actual                 | Ursprunglig ofakturerad försäljning GUID | Ursprunglig           | msdyn_actual       |
| Fakturerad försäljning GUID              | Fakturerad försäljning                  | msdyn_actual       | Ofakturerad faktisk försäljning GUID   | Ofakturerad försäljning               | msdyn_actual       |                    |
| Korrigeringsfaktura, utkast       | Transaktion på fakturaraden GUID | Utbyte          | msdyn_invoicelinetransaction | Fakturerad försäljning GUID            | Ursprunglig           | msdyn_actual       |
| Bekräfta fakturakorrigering     | Fakturerad återförd försäljning GUID    | Återföring          | msdyn_actual                 | Fakturerad försäljning GUID            | Ursprunglig           | msdyn_actual       |
| Ny ofakturerad faktisk försäljning GUID | Utbyte                     | msdyn_actual       | Fakturerad försäljning GUID            | Ursprunglig                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
