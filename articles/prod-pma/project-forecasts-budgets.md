---
title: Projektprognoser och budgetar
description: Microsoft Dynamics 365 Finance tillhandahåller projektprognoser och projektbudgetar för hantering och styrning av dina projekt.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1c1cde984334af8cc30e7899e3cf0b38467666f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999648"
---
# <a name="project-forecasts-and-budgets"></a>Projektprognoser och budgetar

[!include [banner](../includes/banner.md)]

Det finns två sätt att hantera och kontrollera dina projekt: projektprognoser och projektbudgetar. 

Använd prognoser om organisationen har ett operationellt perspektiv och fokuserar på intäkter och kostnader som härleds från vissa transaktioner. Använd projektbudgettering om din organisation fokuserar mer på de ekonomiska beloppen. 

Både projektprognoser och projektbudgetar använder prognosmodeller för att hålla planerade transaktionsbelopp. 

Varje metod har sina fördelar. Tänk på följande innan du väljer en metod för organisationen.

|   Allokeringsmetod       |           Projektprognoser            |        Projektbudgetering                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Periodfördelning**     | Du kan inte explicit fördela transaktioner över en räkenskapsperiod. Istället baseras prognosen och kontrollen av prognosen på projektets livslängd. Eftersom prognoser baseras på ett visst datum måste du ange perioden från datumet. | Du kan fördela transaktioner över hela projektet eller en räkenskapsperiod. Om du fördelar över en period kan du överföra oanvända belopp till nästa räkenskapsperiod. |
| **Visa transaktioner**  | Du kan visa transaktioner i prognosformulären, där du ser prognoserna för hela företaget och för alla projekt oavsett hierarkin. Om du vill fokusera på ett visst projekt måste du filtrera informationen.                                       | Du kan visa budgeterade transaktioner för en enskild projekthierarkin. Därför kan du visa transaktionsdetaljer för ett överordnat projekt eller dess underprojekt.                 |
| **Transaktionsloggfiler** | När du anger prognostransaktioner kan du använda alla attribut som finns för en faktisk transaktion. Detta gör det möjligt att mer detaljerat i prognosen. Du kan till exempel ange information om kvantiteter, arbetare, artiklar eller radegenskaper.         | När du anger budgetdetaljer kan du endast använda belopp, kategorier och aktiviteter.                    |
| **Säkerhet**              | Prognoser bygger på de transaktioner du anger i prognosformulären och omfattar ingen funktion för processkontroll. Alla arbetare som har behörighet till ett prognosformulär kan ändra informationen utan godkännande.                                        | Vid budgetering används arbetsflödessystemet för att spara ändringshantering och du kan spara historiken.         |
| **Entitetstyper**           | Prognostransaktionsposter baseras på antalet enheter och på priser för kostnads- och försäljningsenheter.  | Budgetinformationen bygger på belopp som delas upp mellan kostnader och intäkter.                                          |
| **Prognosmodeller**       | Eftersom varje prognos måste associeras med en modell kan du skapa flera prognosmodeller och även konfigurera delmodeller.           | Projektbudgetar begränsar de prognosmodeller som används för budgetering. Färre prognosmodeller kan öka konsekvensen i projektionerna.                           |
| **Kostnadsöverskridningar**         | Du kan endast tillåta eller inte tillåta att transaktioner som orsakar en kostnadsöverskridning tas med i transaktionen.   | Projektbudgetering tillhandahåller ytterligare kontrollalternativ för användare. Du kan tillåta varningar och överskridningar.                    |
| **Kontroll**               | Prognoskontrollen utförs med hjälp av prognosreducering. Faktiska belopp subtraheras från prognostiserade transaktions saldon utan någon spårning. Det kan göra det svårare att spåra var de faktiska transaktionerna inträffade.                   | I projektbudgetkontrollen subtraheras de faktiska beloppen från belopp i den resterande budgeten. Detta möjliggör en tydligare granskning.                                   |

## <a name="project-forecasts"></a>Projektprognoser
När du använder projektprognoser kan du ange prognostransaktioner i prognosformulär för varje transaktionstyp. Alla attribut som är tillgängliga för en faktisk transaktion kan användas för en prognostransaktion, till exempel radlönsamhet, radattribut, arbetare eller beskrivningar. Du kan också få tid på att fakturera en kund. 

Projekt prognostransaktioner baseras på enheter och belopp. 

Du måste koppla varje projektprognos till en prognosmodell. När du anger en prognostransaktion föreslås en prognosmodell automatiskt. Prognosmodellen fungerar som en behållare för prognostransaktionerna. 

Du kan ange prognosmodeller som delmodeller för en modell. På så sätt kan du prognostisera efter region, tidsperiod eller avdelning. Du kan kopiera prognostransaktionerna i en modell för att skapa en ny modell, och du kan även överföra transaktionerna till redovisningen. Eftersom det finns en 1:1-relation mellan en prognos och en modell utgör varje prognosmodell en separat budget för ett projekt. 

Prognosmodeller kan använda prognostiserad reducering som styr funktion i projekt. Vid en prognosreducering minskar faktiska transaktioner saldon för prognostransaktioner. Eftersom prognosreducering tillämpas på det högsta projektet i hierarkin ger den emellertid en begränsad översikt över ändringarna i prognosen. Om en arbetare t.ex. är associerad med ett del projekt bokförs de faktiska transaktionerna för arbetaren i det överordnade projektet. Det kan göra det svårt att spåra ändringar eftersom du inte enkelt kan fastställa vilken transaktion som ett del projekt har orsakat nedsättning av prognosbeloppet från. Därför bör du skapa en kopia av en prognosmodell för att minska prognosen. Du kan sedan använda rapporter för att visa vad som ursprungligen prognostiserades. 

Du kan ändra, kopiera, ta bort eller överföra projektprognoser till en redovisningsbudget. Det finns emellertid ingen processkontroll. Alla arbetare som har behörighet till ett prognosformulär kan göra ändringar utan revidering.

-   **Revidera** – du kan revidera en prognostransaktion i samma formulär där de ursprungliga posterna skapades.
-   **Kopiera eller radera** – när du kopierar prognostransaktioner kopierar du transaktionsraderna med en prognosmodell till en annan prognosmodell. När du tar bort en prognos tar du bort prognostransaktionerna från en prognosmodell. Om du vill begränsa de prognostransaktioner som kopieras eller tas bort väljer du specifika transaktionstyper och datum. Detta gör att du kan kopiera eller ta bort specifika delar av en prognos.
-   **Överföring** – när du överför en projektprognos till en redovisningsbudget överför du prognostransaktionerna för en prognosmodell till en redovisningsbudget. Du kan skriva över alla tidigare överförda transaktioner i redovisningsbudgeten som du överför projektprognosen till.

## <a name="project-budgets"></a>Projektbudgetar
Projektbudgetering är en enklare metod än prognoser, även om den integreras med prognosmodeller. Den använder ett enkelt formulär för inmatning för information om ursprungliga budgetar och revideringar och tillåter endast projektioner som baseras på belopp, kategori eller aktivitet. 

I projektbudgetering måste alla originalbudgetar och revideringar skickas till ett projektarbetsflöde för godkännande. Med arbetsflöden får du ökad kontroll över processen och skapa en ändringshistorikpost. 

Projektbudget påminner om budgetering i redovisningsmodulen, men är snabbare och enklare att konfigurera. Många av alternativen i redovisningsbudgetering, t.ex. nummer serier eller valuta, behöver inte ställas in separat för projekt.

Projektbudgetar associeras automatiskt med två prognosmodeller, en för ursprunglig budget och en för resterande budget. Därför kan rapporter som bygger på prognosmodeller använda budgetdata. När en projektbudget är bekräftad skapar systemet prognostransaktioner baserade på de associerade modellerna, som används för rapporter och kontrollsyften.

## <a name="forecast-models"></a>Prognosmodeller
Prognosmodeller har en hierarki med ett enda lager. Detta innebär att en projektprognos måste vara associerad med en prognosmodell.

Om du använder projektprognoser kan du identifiera modeller som del modeller. Du kan sedan skapa prognoser efter avdelning, tidsperiod eller region. Du kan till exempel skapa en prognosmodell för ett år och sedan skapa delmodeller för de regionala prognoserna Nordost, Sydost, Nordväst och Sydväst som regionala cheferna skickar in. Genom att välja olika alternativ i tillgängliga rapporter kan du visa information efter total prognos eller efter delmodell.





[!INCLUDE[footer-include](../includes/footer-banner.md)]