---
title: Varför återställs priset till standardvärdet noll för löpande löner?
description: Följande tre kontroller hjälper dig att felsöka anledningen till att priset anges som standardvärdet 0 för löpande löner.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 85a177ec-ad61-450d-bfe6-cdea7a415566
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ccbad4ac969ffe4f09744557e2a9be68aa93e8c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756279"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Varför återställs priset till standardvärdet noll för löpande löner?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dessa Vanliga frågor och svar gäller utgiftstillgångar där transaktionsklassen anges som Utgift och transaktionstypen som Ofakturerad försäljning. Följande tre kontroller hjälper dig att felsöka anledningen till att priset (fakturataxa) anges som 0 för löpande löner.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Kontrol 1: Hitta försäljningsprislistan för projektet

Hitta projektet i projektfältet för tillgången och gå till projektsidan. Gå sedan till fliken Försäljning. I rutnätet för projektkontraktrader klickar du på länken i fältet Projektkontrakt. Projektkontraktssidan öppnas. På sidan projektkontrakt går du till fliken Projektprislistor. Kontrollera om det finns minst en prislista kopplad hit.

Om det inte finns någon prislista i rutnätet Projektprislistor för projektkontraktet, gör då följande:

- Lägg till en prislista i rutnätet för projektprislistor. Prislistorna som kan kopplas här bör ha sammanhangsfältet inställt på "Försäljning" och prislistans valutafält bör överensstämma med projektkontraktets valutafält. När du har gjort gör nödvändiga korrigeringar, skapa då på nytt en utgiftspost, godkänn denna och bekräfta att den ofakturerade försäljningen anger ett giltigt pris.
- Om du har en eller flera prislistor kopplade till rutnätet för projektprislistor för projektkontraktet, gå då till kontroll 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Kontroll 2: Är de prislistor som anges ovan giltiga för det aktuella datumet för försäljningstillgången?

För att Project Service ska beakta en prislista för standardprissättning bör den prislistan vara tillämpbar för datumet i tidsförsäljningstillgången. Kontrollera följande för att se om ovanstående prislista/prislistor är tillämpbar(a):

- Börja med att kontrollera att start- och slutdatum på fliken Allmänt för bifogade prislistor inte är tomma. Om start- och slutdatum i ovanstående prislistor är tomma har du hittat problemet. 
- Notera fältet för startdatum på din tidsförsäljningstillgång och kontrollera om någon av de prislistor som identifieras gäller för detta datum. Till exempel bör datumet för den tidsförsäljningstillgången hamna inom ramarna för start- och slutdatum i prislistan. 
    - Om det inte finns någon prislista som omfattar datumet i den tidsförsäljningstillgången har du hittat problemet. Ändra prislistans start- och slutdatum så att prislistan omfattar datumet för tidsförsäljningstillgången. 
    - Om det finns mer än en prislista som omfattar datumet i tidsförsäljningstillgången har du hittat problemet. Du kan åtgärda detta genom att redigera start- och slutdatum i prislistan/-listorna så att det finns bara en enda prislista som omfattar datumet för tidsförsäljningstillgången. 
    - Om det bara finns en enda prislista som omfattar detta datum för tidsförsäljningstillgången går du vidare till Kontroll 3.
När du har gjort nödvändiga korrigeringar, skapa då på nytt en utgiftspost, godkänn denna och bekräfta att den ofakturerade försäljningen anger ett giltigt pris.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Kontroll 3: Finns det ett giltigt pris för utgiftskategorin i prislistan för tillämpbara projekt? 

Om du har slutfört kontrollerna 1 och 2 bör du nu bara ha en enda projektprislista som gäller för datumet för tidsförsäljningstillgången. Öppna denna projektprislista och gå till fliken Kategoripriser. Kontrollera att det finns en rad i rutnätet för utgiftskategoritillgången
 
- Finns ingen rad har du hittat problemet. Skapa en rad i rutnätet Kategoripris för kategorin i din utgiftstillgång. När detta är gjort, skapa då på nytt en utgiftspost, godkänn denna och bekräfta att den ofakturerade säljtillgången anger ett giltigt pris. 
- Om det finns en rad för utgiftskategorin i rutnätet för kategoripriser kan du kontrollera om den har ett giltigt pris.

För att förstå vad ett giltigt pris är, använd dessa metoder:

- Om fältet Prissättningsmetod på raden Kategoripris har angetts som Till kostnad, så kommer enhetsavgiften för säljtillgången Utgift att återställas till standardvärdet i posten Utgifter.
- Om fältet Prissättningsmetod på raden Kategoripris anges som Påläggsfaktor procent kontrollerar du om fältet Procent anges som ett giltigt värde. Priset per enhet för din säljtillgång Utgift återställs till standardvärdet genom att tillämpa denna påläggsprocent på priset i posten Utgift.
- Om fältet Prissättningsmetod på raden Kategoripris anges som Pris per enhet, kontrollerar du om fältet Pris anges som ett giltigt värde. Priset per enhet i din säljtillgång Utgift kommer att återställas till standardbeloppet i fältet Pris.

Om prisinställningen för utgiftskategorin är ogiltig har du hittat problemet. Lösningen är att redigera kategoriprisraden med ett pris som är giltigt för utgiftskategorin i enlighet med ovanstående regler. När detta är gjort, skapa då på nytt en utgiftspost, godkänn denna och kontrollera sedan att den ofakturerade säljtillgången får ett giltigt pris.

Om du fortfarande inte ser något giltigt pris på säljtillgången Utgift efter att ha följt de tre kontrollerna ovan, vänligen skapa då ett supportärende.


