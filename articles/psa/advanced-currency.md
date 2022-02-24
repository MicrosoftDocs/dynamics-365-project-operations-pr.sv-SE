---
title: Scenarier med flera valutor (version 3.x)
description: I den här ämnet finns information om scenarier med flera valutor.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: bdb9ccad84e0f510118502d4253f5c83a760f8bb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145695"
---
# <a name="multiple-currency-scenarios"></a>Scenarier med flera valutor

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 har två koncept av valutor:

- **Transaktionsvaluta** – valutan som en transaktion inträffar i. 
- **Basvaluta** - valutan för Dynamics 365-instansen. Den här valutan konfigureras när en Dynamics 365-instans etableras. Den kan inte ändras.

Exempel: Contoso US sålde 100 t-shirts till en kund i Sverige för 15 GPB. Följande tabell visar hur den här transaktionen registreras i entiteten orderprodukt.

| Produkt | Kvantitet | Pris per enhet | Valuta | Belopp | Växelkurs | Pris per enhet (bas)| Belopp (bas)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-shirt | 100      | 15             | GBP      | 1500   | 0.94          | 17.25               | 1,725       |

Kolumnen **valuta** visar transaktionsvalutan, som är den valuta som försäljningen inträffade i. Kolumnen **växelkurs** som är associerad med transaktionsvalutan och basvalutan. Basvalutan är US dollar (USD). Den här basvalutan konfigurerades när Dynamics 365-instansen etablerades.
När tabellen visas registreras varje transaktion både i transaktionsvalutan och i basvalutan. Dynamics 365 använder valutakursen för att beräkna beloppen i basvalutan.

## <a name="project-service-automation-extensions"></a>Project Service Automation-tillägg

Dynamics 365 Project Service Automation påverkar transaktionsvalutan eftersom affärstransaktioner vanligen har två aspekter: kostnad och försäljning.

Följande entiteter betraktas som affärstransaktioner:

- Information om offertrad
- Information om projektkontraktrad
- Beräkningsrad
- Journalrad
- Information om fakturarad
- Faktiskt

I var och en av dessa entiteter finns en post som representerar kostnadsbeloppet eller försäljningsbeloppet. För alla Dynamics 365-entiteter som har fältet **Belopp** innehåller varje post belopp både i transaktionsvalutan och i basvalutan. 

PSA utökar konceptet för transaktionsvaluta för kostnaden och försäljningen på följande sätt:

- Kostnadstransaktionsvalutan för tidstransaktioner kommer alltid från valutan i den organisationsenhet som äger eller hanterar projektet. Organisationsenheten kallas för den upphandlande enheten.
- Försäljningstransaktionsvalutan för tids- och utgiftstransaktioner kommer alltid från valutan i projektkontraktet.
- Kostnadstransaktionsvalutan för utgifter kommer från den valuta som utgiftstransaktionen skapades i.

## <a name="multiple-currency-scenario"></a>Scenario med flera valutor

I det här avsnittet beskrivs ett exempel på ett projekt som Contoso UK levererar för en kund med namnet Fabrikam, Japan. Så här gör du när scenariot har ställts in:

1. GBP och japanska yen (JPY) ställs in under **inställningar** \> **verksamhetsstyrning** \> **valutor**. 
2. Ett kundkonto med namnet **Fabrikam - Japan** har ställts in och JPY väljs som valuta för kontot.
3. En organisationsenhet med namnet **Contoso UK** har ställts in och GBP valts som valuta.
4. Ett projektkontrakt skapas, där **Contoso UK** anges som den upphandlande enheten och **Fabrikam – Japan** anges som kund.
5. Projektkontraktrader skapas utifrån fakturering för de olika transaktionsklasserna i projektet, t.ex. fakturering för tid jämfört med fakturering för utgifter.
6. Ett projekt skapas där **Contoso UK** anges som den upphandlande enheten. Det här projektet skapas och mappas till projektkontraktraderna.


När du använder en uppskattning som innehåller information om offertrader, projektkontraktradens information eller på uppskattningsraden i schemat skapas två poster alltid i entiteten. En post är för kostnad och den andra posten är för försäljning.

- Som standard anges transaktionsvalutan för kostnadsposten till valutan för projektets upphandlande enhet. I det här exemplet är valutan GBP.
- Som standard anges transaktionsvalutan för försäljningsposten till valutan för projekkontraktet. I det här exemplet är valutan JPY.

När verkliga värden skapas för tid med hjälp av tidstransaktion eller journalrad händer följande:

- Som standard anges transaktionsvalutan för kostnadsposten till valutan för projektets upphandlande enhet.
- Som standard anges transaktionsvalutan för försäljningsposten till valutan för projekkontraktet.

När verkliga värden skapas för utgifter av utgiftsposten eller journalrad händer följande:

- Du kan registrera utgiftsbeloppet i valfri valuta. Välj valuta med hjälp av valutaväljaren på sidan **utgiftspost** eller på sidan **journalrad**. Som standard anges transaktionsvalutan för kostnadsposten till valutan på utgiftsposten. 
- Som standard anges transaktionsvalutan för försäljningsposten till valutan för projekkontraktet. För att ställa in den här valutan konverteras först transaktionsbeloppet i den valuta som användaren har angett i basvalutan. Därefter konverteras beloppet till projektkontraktets valuta. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Beräknar sammanslagningar när faktiska projekt registreras i flera transaktionsvalutor

I Dynamics 365 hanterar automatiskt sammanslagning av belopp i olika valutor. Här följer ett exempel.

| Transaktionsklass | Transaktionstyp| Date   | Resurs | Transaktionskategori | Kvantitet | Enhetspris | Belopp      | Växelkurs | Belopp i bas |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Ofakturerad försäljning   | 14 juni | Joel  |                      | 8 tim    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Time              | Ofakturerad försäljning   | 15 juni | Joel  |                      | 8 tim    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Expense           | Ofakturerad försäljning   | 16 juni | Joel  | Hotell                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Expense           | Ofakturerad försäljning   | 17 juni | Joel  | Biluthyrning           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Om du vill beräkna det totala fakturerade försäljningsvärdet i projektet kan du skapa ett fält för sammanslagning för fältet **belopp** i alla relaterade, ej fakturerade försäljningsvärden. Sammanslagningsfältet är en konstruktion av Dynamics 365 som gör det enkelt att skapa formler för relaterade poster.
