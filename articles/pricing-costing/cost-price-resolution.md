---
title: Avgör kostnadstaxa för projektbaserade beräkningar och utfall
description: Den här artikeln innehåller information om hur kostnadstaxor för projektbaserade beräkningar och utfall avgörs.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475301"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Avgör kostnadstaxa för projektbaserade beräkningar och utfall

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

För att fastställa självkostnader för uppskattningar och utfall i Microsoft Dynamics 365 Project Operations använder systemet först datum och valuta i den inkommande uppskattningen eller utfallet för att fastställa försäljningsprislistan. I själva sammanhanget använder systemet fältet **Transaktionsdatum** för att avgöra vilken prislista som är tillämplig. Värdet **Transaktionsdatum** för inkommande uppskattning eller utfall jämförs med värdena **Effektiv start (tidszonsoberoende)** och **Effektivt slut (tidszonsoberoende)** på prislistan. När prislistan för självkostnad har fastställts avgör systemet kostnadstaxan.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Avgöra kostnadstaxor i uppskattning och utfall för Tid

Uppskattning för **Tid** refererar till:

- Information om offertrad för **Tid**.
- Information om kontraktrad för **Tid**.
- Resurstilldelning i ett projekt.

Utfall för **Tid** refererar till:

- Journalraderna Inmatning och Korrigering för **Tid**.
- Journalrader som skapas när en tidspost skickas in.

När en prislista för självkostnad har fastställts slutför systemet följande steg för att ange en standardkostnadstaxa.

1. Systemet matchar kombinationen av fälten **Roll**, **Resursföretag** och **Resursenhet** i uppskattningen eller utfallet för **Tid** med rollprisraderna i prislistan. Denna matchning förutsätter att du använder standardprissättningsdimensionerna för arbetskostnad. Om du konfigurerade systemet för att matcha andra fält än, eller utöver, **Roll**, **Resursföretaget** och **Resursenhet** används en annan kombination för att hämta en matchande rollprisrad.
1. Om systemet hittar en rollprisrad som har en kostnadstaxa för kombinationen av **Roll**, **Resursföretag** och **Resursenhet**, används den kostnadstaxan som standard.
1. Om systemet inte kan matcha värdena **Roll**, **Resursföretag** och **Resursenhet** släpps dimensionen med lägst prioritet och systemet söker efter de rollprisrader som har matchningar för de andra två dimensionsvärdena och fortsätter att släppa dimensioner tills en matchande rollprisrad hittas. Kostnadstaxan från den posten används som standardkostnad. Om det inte finns någon matchande rollprisrad anges priset till **0** (noll) som standard.

> [!NOTE]
> Om du konfigurerar en annan prioritering av fälten **Roll** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det föregående beteendet i enlighet med detta. Systemet hämtar rollprisposter som har värden som matchar varje prissättningsdimension i prioritetsordning. Rader som har null-värden för dessa dimensioner kommer sist.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Avgöra kostnadstaxor på utfall och uppskattning för Utgift

Uppskattning för **Utgift** refererar till:

- Information om offertrad för **Utgift**.
- Information om kontraktrad för **Utgift**.
- Utgiftsuppskattningar för ett projekt.

Utfall för **Utgift** refererar till:

- Journalraderna Inmatning och Korrigering för **Utgift**.
- Journalrader som skapas när en utgiftspost skickas in.

När en prislista för självkostnad har fastställts slutför systemet följande steg för att ange en standardkostnadstaxa.

1. Systemet matchar kombinationen av fälten **Kategori** och **Enhet** i uppskattningen eller utfallet för **Utgift** med kategoriprisraderna i prislistan.
1. Om systemet hittar en kategoriprisrad som har en kostnadstaxa för kombinationen av fälten **Kategori** och **Enhet** används den kostnadstaxan som standardkostnad.
1. Om systemet inte kan matcha värdena **Kategori** och **Enhet** ställs priset in på **0** (noll) som standard.
1. I uppskattningen, om systemet hittar en matchande kategoriprisrad men prissättningsmetoden är någon annan än **Pris per enhet**, ställs kostnadstaxan in på **0** (noll) som standard.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Avgöra kostnadstaxa på utfall och uppskattning för Material

Uppskattning för **Material** refererar till:

- Information om offertrad för **Material**.
- Information om kontraktrad för **Material**.
- Materialuppskattningar för ett projekt.

Utfall för **Material** refererar till:

- Journalraderna Inmatning och Korrigering för **Material**.
- Journalrader som skapas när en materialanvändningslogg skickas in.

När en prislista för självkostnad har fastställts slutför systemet följande steg för att ange en standardkostnadstaxa.

1. Systemet använder kombinationen av fälten **Produkt** och **Enhet** i uppskattningen eller utfallet för **Material** med prislistepostrader i prislistan.
1. Om systemet hittar en prislistepostsrad som har en kostnadstaxa för kombinationen av fälten **Produkt** och **Enhet** används den kostnadstaxan som standardkostnad.
1. Om systemet inte kan matcha värdena för **Produkt** och **Enhet** ställs enhetskostnaden in på **0** (noll) som standard.
1. I uppskattningen eller utfallet, om systemet hittar en matchande prislistepostsrad men prissättningsmetoden är någon annan än **Valutabelopp**, ställs enhetskostnaden in på **0** som standard. Detta beror på att Project Operations endast stöder prismodellen **Valutabelopp** för material som används i ett projekt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
