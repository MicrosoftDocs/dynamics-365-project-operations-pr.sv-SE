---
title: Varför återställs priset till standardvärdet noll för tidskostnadstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för tidsutgiftstillgångar.
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
ms.openlocfilehash: 65f2bc773a376800928cc3746691061d8e290f74
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285820"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Varför återställs priset till standardvärdet noll för tidskostnadstillgångar?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dessa Vanliga frågor och svar gäller tillgångar där transaktionsklassen anges som Tid och transaktionstypen som Kostnad. Följande tre kontroller hjälper dig att felsöka anledningen till att priset anges som standardvärdet 0 för tidskostnadstillgångar.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Kontrol 1: Hitta självkostnadsprislistan för projektet

Hitta projekt via projektfältet för tillgången och gå sedan till projektsidan. Klicka på kontraktenhetslänken i fältet. Kontrollera om den upphandlande enheten har en prislista i rutnätet för självkostnadslistor den upphandlade enhetens sida.

Om det finns mer än en prislista har du hittat problemet. Project Service har endast stöd för en prislista per organisationsenhet. Ta bort alla prislistor från denna entitet tills endast en enda prislista finns kopplad i rutnätet för självkostnadslistor för organisationsenheten.

Om inga prislistor har kopplats till organisationsenheten, anteckna då valutan för organisationsenheten. Gå till Project Service och därefter till Parametrar och öppna fliken Prislistor. Kontrollera om det finns några prislistor med kontext angiven som Kostnad samt valuta som matchar valutan i organisationsenheten.
 
Om det inte finns några prislistor som matchar dessa villkor har du hittat problemet. Se till att du har minst en prislista vars sammanhang anges som Kostnad och vars valuta matchar valutan för organisationsenheten.

Om det finns mer än en prislista som matchar detta villkor, fortsätt då att läsa igenom detta dokument om du vill göra fler kontroller.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Kontroll 2: Är någon av de prislistor som anges ovan giltig för det aktuella datumet för tidskostnadstillgången?

För att Project Service ska beakta en prislista för standardprissättning bör den prislistan vara tillämpbar för datumet för tidskostnadstillgången. Kontrollera följande för att se om ovanstående prislista/prislistor är tillämpbar(a):

- Kontrollera att start- och slutdatum på fliken Allmänt för bifogade prislistor inte är tomma. Om start- och slutdatum i ovanstående prislistor är tomma har du hittat problemet. 
- Anteckna fältet Startdatum för din tidskostnadstillgång och kontrollera om någon av de prislistor som identifierats gäller för detta datum. Till exempel bör datumet för tidskostnadstillgången hamna inom ramarna för start- och slutdatum i prislistan. 
    - Om det inte finns någon prislista som omfattar detta datum för tidskostnadstillgången har du hittat problemet. Ändra prislistans start- och slutdatum så att prislistan omfattar datumet för tidskostnadstillgången. 
    - Om det finns mer än en prislista som täcker datumet för tidskostnadstillgången har du hittat problemet. Du kan åtgärda detta genom att redigera start- och slutdatum för prislistorna så att det finns bara en enda prislista som omfattar datumet för tidskostnadstillgången. 
    - Om det finns bara en prislista som omfattar detta datum för tidskostnadstillgången, gå då vidare till nästa kontroll i dokumentet.
När du har utfört nödvändiga korrigeringar, skapa då på nytt en tidspost, godkänn denna och kontrollera att tidskostnadstillgången anger ett giltigt pris.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Kontroll 3: Finns det ett pris i prislistan för prissättning på tidskostnadstillgången?

Om du har slutfört kontrollerna 1 och 2 bör du nu ha en enda prislista som gäller datumet för tidskostnadstillgången. Öppna denna prislista och gå till fliken Rollpriser. Kontrollera att det finns en rad i rutnätet för prissättningen för tidskostnadstillgången.

Om det inte finns någon rad i rutnätet för rollpriser för prissättning för tidskostnadstillgången har du hittat problemet. Skapa en rad i rutnätet Rollpriser för prissättning i tidskostnadstillgången. När detta är gjort, skapa då på nytt en tidspost, godkänn denna och kontrollera att tidskostnadstillgången anger ett giltigt pris.
 
Om du fortfarande inte ser något giltigt pris på din tidskostnadstillgång efter att ha utfört de tre kontrollerna ovan, vänligen skapa då ett supportärende.





[!INCLUDE[footer-include](../includes/footer-banner.md)]