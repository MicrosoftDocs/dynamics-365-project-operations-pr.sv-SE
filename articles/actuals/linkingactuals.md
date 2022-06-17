---
title: Transaktionens ursprung – Länka faktiska värden till källan
description: I denna artikel förklaras hur konceptet med transaktioners ursprung används för att länka faktiska värden till ursprungliga källposter, till exempel tidspost, utgiftspost eller materialanvändningsloggar.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921324"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Transaktionens ursprung – Länka faktiska värden till källan

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Transaktioners ursprungposter skapas för att länka faktiska värden till källan, till exempel tidsposter, utgiftsposter, materialanvändningsloggar och projektfakturor.

I följande exempel visas den vanligaste bearbetningen av tidsposter i en Project Operations projektlivscykel.

> ![Bearbetningstidsposter i Project Operations.](media/basic-guide-17.png)
 
1. Inlämning av en tidspost innebär att två journalrader skapas: en för kostnad och en för ofakturerad försäljning.
2. Eventuellt godkännande av en tidspost innebär att två faktiska värden skapas: en för kostnad och en för ofakturerad försäljning.
3. När en användare skapar en projektfaktura skapas transaktionen för fakturaraden med hjälp av data från ofakturerat faktiskt försäljningsvärde.
4. När fakturan bekräftas skapas två nya faktiska värden: en ofakturerad återföring av försäljningen och en fakturerad faktisk försäljning.

Varje händelse i detta behandlingsarbetslöse utlöser skapandet av poster i transaktionens ursprungsentitet så att du kan spåra relationer mellan de poster som skapas i en tidspost, journalrad-, faktiska värden och information om fakturarad.

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
| Korrigeringsfaktura GUID      | Faktura                  | Ny ofakturerad faktisk försäljning GUID    | Faktisk                            |                          |


I följande illustration visas länkarna som skapas mellan faktiska värden och källorna till dessa vid olika händelser med hjälp av ett exempel på tidsposter i Project Operations.

> ![Hur faktiska värden länkas till källposter i Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
