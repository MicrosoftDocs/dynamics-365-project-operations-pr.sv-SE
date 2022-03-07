---
title: Affärstransaktioner
description: I det här ämnet finns information om affärstransaktioner.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 28555f29e65c11255c8966f3d4b900512aa01c30fef0a9cef3a3794edaf92a0b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987548"
---
# <a name="business-transactions"></a>Affärstransaktioner

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation är *affärstransaktion* ett abstrakt koncept som inte representeras av någon entitet. Vissa vanliga fält och processer i entiteter är dock utformade för att använda begreppet affärstransaktioner. Följande entiteter använder denna abstraktion:

- Information om offertrad
- Information om kontraktrad
- Beräkningsrader
- Journalrader
- Faktiska värden

Av dessa entiteter mappas Information om offertrad, Information om kontraktrad och Beräkningsrader till beräkningsfasen i projektlivscykeln. Entiteterna Journalrader och Faktiska värden mappas till körningsfasen i projektlivscykeln.

PSA behandlar poster i dessa fem entiteter som affärstransaktioner. Den enda skillnaden är att poster i entiteter som är mappade till beräkningsfasen betraktas som ekonomiska prognoser, medan posterna i entiteter som är mappade till körningsfasen betraktas som ekonomiska fakta som redan har inträffat.

Mer information finns i [Beräkningar](estimates.md) och [faktiska värden](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncept som är unika för affärstransaktioner
Följande koncept är unika för begreppet affärstransaktioner:

- Transaktionstyp
- Transaktionsklass
- Transaktionens ursprung
- Transaktionskoppling

### <a name="transaction-type"></a>Transaktionstyp

Transaktionstyp representerar tidpunkten för och sammanhanget mellan de ekonomiska konsekvenserna för ett projekt. Den representeras av ett alternativuppsättning som har följande värden som stöds i PSA:
- Kostnad
- Projektkontrakt
- Ofakturerad försäljning
- Fakturerad försäljning
- Försäljning inom organisationen
- Kostnad för resursenhet

### <a name="transaction-class"></a>Transaktionsklass

Transaktionsklass representerar de olika typer av kostnader som uppstår i projekt. Den representeras av ett alternativuppsättning som har följande värden som stöds i PSA:

- Time
- Expense
- Material
- Avgift
- Milstolpe
- Moms

Värdet **milstolpe** används vanligtvis av affärslogiken för fakturering i fast pris i PSA.

### <a name="transaction-origin"></a>Transaktionens ursprung

Transaktionsursprung är en entitet som lagrar ursprunget för varje affärstransaktion. När projektkörningen startar kommer respektive affärstransaktion att ge upphov till en ytterligare affärstransaktion, som i sin tur skapar ännu en, och så vidare. Entiteten för transaktionsursprung har utformats för att lagra data om respektive transaktions ursprung i syfte att underlätta rapportering och spårbarhet. 

### <a name="transaction-connection"></a>Transaktionskoppling

Transaktionskoppling är en entitet som lagrar relationen mellan två liknande affärstransaktioner, t.ex. kostnader och relaterade verkliga försäljningar, eller transaktionsåterföringar som startas av faktureringsaktiviteter som fakturabekräftelse eller fakturakorrigering.

Tillsammans kan du med hjälp av transaktionsursprunget och transaktionskoppling spåra relationer mellan affärstransaktioner och åtgärder som medför att en specifik affärstransaktion skapas.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exempel: hur transaktionens ursprung fungerar med transaktionskoppling

I följande exempel visas den vanligaste bearbetningen av tidsposter i en PSA projektlivscykel.

> ![Bearbetning av hela tiden i en Project Service-livscykel.](media/basic-guide-17.png)
 
1. Inlämning av en tidspost innebär att två journalrader skapas: en för kostnad och en för ofakturerad försäljning.
2. Eventuellt godkännande av en tidspost innebär att två faktiska värden skapas: en för kostnad och en för ofakturerad försäljning.
3. När en användare skapar en projektfaktura skapas transaktionen för fakturaraden med hjälp av data från ofakturerat faktiskt försäljningsvärde. 
4. När fakturan bekräftas skapas två nya faktiska värden: en ofakturerad återföring av försäljningen och en fakturerad faktisk försäljning.

Varje händelse utlöser skapandet av poster i entiteterna av transaktionens ursprung och transaktionskoppling så att du kan spåra relationer mellan de poster som skapas i en tidspost, journalrad-, faktiska värden och information om fakturarad.

I följande tabell visas posterna i entiteten för transaktionens ursprung för föregående arbetsflöde.

| Händelse                        | Ursprung                   | Ursprungstyp                       | Transaktion                       | Transaktionstyp         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Skicka tidspost        | Registrera tidspost GUID   | Tidspost                        | Post för journalrad GUID (kostnad)   | Journalrad             |
| Registrera tidspost GUID       | Tidspost               | Post för journalrad GUID (försäljning)  | Journalrad                      |                          |
| Tidsgodkännande                | Post för journalrad GUID | Journalrad                      | Ofakturerad försäljningspost GUID        | Faktiskt                   |
| Registrera tidspost GUID       | Tidspost               | Ofakturerad försäljningspost GUID        | Faktiskt                            |                          |
| Post för journalrad GUID     | Journalrad             | Faktisk kostnadspost GUID           | Faktiskt                            |                          |
| Registrera tidspost GUID       | Tidspost               | Faktisk kostnadspost GUID           | Faktiskt                            |                          |
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

I följande tabell visas posterna i entiteten för transaktionskoppling för föregående arbetsflöde.

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