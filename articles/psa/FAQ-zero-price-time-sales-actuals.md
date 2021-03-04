---
title: Varför återställs priset till standardvärdet noll för tidsförsäljningstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för tidsförsäljningstillgångar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146235"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Varför återställs priset till standardvärdet noll för tidsförsäljningstillgångar?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dessa Vanliga frågor och svar gäller tillgångar där transaktionsklassen anges som Tid och transaktionstypen som Ofakturerad försäljning. Följande tre kontroller hjälper dig att felsöka anledningen till att priset (fakturataxa) anges som standardvärdet 0 för tidsförsäljningstillgångar.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Kontroll 1: Hitta försäljningsprislistan för projektet

Hitta projektet i projektfältet för tillgången och gå till projektsidan. Gå sedan till fliken Försäljning, och i rutnätet för projektkontraktrader klickar du på länken i fältet Projektkontrakt. Projektkontraktsidan öppnas. På sidan projektkontrakt går du till fliken Projektprislistor. Kontrollera om det finns minst en prislista kopplad hit. Om det inte finns någon prislista i rutnätet Projektprislistor för projektkontraktet har du hittat problemet. Lägg till en prislista i rutnätet för projektprislistor. Prislistorna som kan kopplas här bör ha sammanhangsfältet inställt på "Försäljning" och prislistans valutafält bör överensstämma med projektkontraktets valutafält. När du har gjort nödvändiga korrigeringar, skapa då på nytt en tidspost, godkänn denna och kontrollera att den ofakturerade försäljningstillgången anger ett giltigt pris. 

Om du har en eller flera prislistor kopplade till rutnätet för projektprislistor för projektkontraktet, fortsätt då till nästa kontroll i dokumentet.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Kontroll 2: Är de prislistor som anges ovan giltiga för det aktuella datumet för tidsförsäljningstillgången?

För att Project Service ska beakta en prislista för standardprissättning bör den prislistan vara tillämpbar för datumet för tidsförsäljningstillgången. Kontrollera följande för att se om ovanstående prislista/prislistor är tillämpbar(a):
- Kontrollera att start- och slutdatum på fliken Allmänt för bifogade prislistor inte är tomma. Om start- och slutdatum i ovanstående prislistor är tomma har du hittat problemet. 
- Anteckna fältet Startdatum på din tidsförsäljningstillgång och kontrollera om någon av de prislistor som identifieras gäller för detta datum. Till exempel bör datumet för tidsförsäljningstillgången hamna inom ramarna för start- och slutdatum i prislistan. 
    - Om det inte finns någon prislista som behandlar det datumet i tidsförsäljningstillgången har du hittat problemet. Ändra prislistans start- och slutdatum så att prislistan täcker datumet för tidsförsäljningstillgången. 
    - Om det finns mer än en prislista som täcker datumet i tidsförsäljningstillgången har du hittat problemet. Du kan åtgärda detta genom att redigera start- och slutdatum i prislistan/-listorna så att det finns bara en enda prislista som täcker datumet för tidsförsäljningstillgången. 
    - Om det bara finns en enda prislista som täcker detta datum för tidsförsäljningstillgången går du till Kontroll 3.
När du har utfört nödvändiga korrigeringar, skapa då på nytt en tidspost, godkänn denna och kontrollera att tidsförsäljningstillgången anger ett giltigt pris.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Kontroll 3: Finns det ett pris i prislistan för prissättning på tidsförsäljningstillgången?

Om du har slutfört kontrollerna 1 och 2 bör du nu ha en enda prislista som gäller datumet för tidsförsäljningstillgången. Öppna denna prislista och gå till fliken Rollpriser. Kontrollera att det finns en rad i rutnätet för prissättningen för tidsförsäljningstillgångar.

Om det inte finns någon rad i rutnätet för rollpriser för prissättning i tidsförsäljningen har du hittat problemet. Skapa en rad i rutnätet Rollpriser för prissättning i tidsförsäljningstillgången. När detta är gjort, skapa då på nytt en tidspost, godkänn denna och kontrollera att tidsförsäljningstillgången anger ett giltigt pris.

Om du fortfarande inte ser något giltigt pris på tidsförsäljningstillgången efter att ha följt de tre kontrollerna ovan, vänligen skapa då ett supportärende. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]