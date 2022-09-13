---
title: Fastställ försäljningspriser för projektberäkningar och utfall
description: Den här artikeln innehåller information om hur försäljningspriser för projektberäkningar och utfall avgörs.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410164"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Fastställ försäljningspriser för projektberäkningar och utfall

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

För att fastställa försäljningspriser på uppskattningar och utfall i Microsoft Dynamics 365 Project Operations använder systemet först datum och valuta i den inkommande uppskattningen eller utfallet för att fastställa försäljningsprislistan. I själva sammanhanget använder systemet fältet **Transaktionsdatum** för att avgöra vilken prislista som är tillämplig. När försäljningsprislistan har fastställts avgör systemet försäljnings- eller fakturataxan.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Fastställa försäljningstaxor på rader för utfall och uppskattningar för Tid

Uppskattning för **Tid** refererar till:

- Information om offertrad för **Tid**.
- Information om kontraktrad för **Tid**.
- Resurstilldelning i ett projekt.

Utfall för **Tid** refererar till:

- Journalraderna Inmatning och Korrigering för **Tid**.
- Journalrader som skapas när en tidspost skickas in.
- Information om fakturarad för **Tid**. 

När en prislista för försäljning har fastställts slutför systemet följande steg för att ange standardfakturataxan.

1. Systemet matchar kombinationen av fälten **Roll** och **Resursenhet** i uppskattningen eller utfallet för **Tid** med rollprisraderna i prislistan. Matchningen förutsätter att du använder de medföljande prissättningsdimensionerna för fakturataxa. Om du har konfigurerat prissättning så att den baseras på andra fält än, eller utöver, **Roll** och **Resursenhet** används den kombinationen av fält för att hämta en matchande rollprisrad.
1. Om systemet hittar en rollprisrad som har en fakturataxa för kombinationen av fälten **Roll** och **Resursenhet**, används den fakturataxan som standardtaxa.
1. Om systemet inte kan matcha värden för **Roll** och **Resursenhet** hämtas rollprisraderna som har matchande värden för fältet **Roll** men null-värden för fältet **Resursenhet**. När en matchande rollprispost hittas används fakturataxan från den posten som standardtaxa. Matchningen förutsätter en färdig konfiguration för den relativa prioriteten hos **Roll** mot **Resursenhet** som en försäljningsprissättningsdimension.

> [!NOTE]
> Om du konfigurerar en annan prioritering av fälten **Roll** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det föregående beteendet i enlighet med detta. Systemet hämtar rollprisposter som har värden som matchar varje prissättningsdimension i prioritetsordning. Rader som har null-värden för dessa dimensioner kommer sist.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Fastställa försäljningstaxor på rader för utfall och uppskattningar för Utgift

Uppskattning för **Utgift** refererar till:

- Information om offertrad för **Utgift**.
- Information om kontraktrad för **Utgift**.
- Rader för utgiftsuppskattningar för ett projekt.

Utfall för **Utgift** refererar till:

- Journalraderna Inmatning och Korrigering för **Utgift**.
- Journalrader som skapas när en utgiftspost skickas in.
- Information om fakturarad för **Utgift**. 

När en prislista för försäljning har fastställts slutför systemet följande steg för att ange ett standardföräljningspris per enhet.

1. Systemet matchar kombinationen av fälten **Kategori** och **Enhet** på uppskattningsraden för **Utgift** mot kategoriprisraderna i prislistan.
1. Om systemet hittar en kategoriprisrad som har en försäljningstaxa för kombinationen av **Kategori** och **Enhet** används den försäljningstaxan som standardtaxa.
1. Om en matchande kategoriprisrad hittas i systemet kan prissättningsmetoden användas för att ange standardförsäljningspriset. I följande tabell visas standardiseringen av utgiftspriset i Project Operations.

    | Sammanhang | Prismodell | Standardpris |
    | --- | --- | --- |
    | Beräkning | Pris per enhet | Baserat på kategoriprisraden. |
    |        | Vid kostnad | 0.00 |
    |        | Pålägg över kostnad | 0.00 |
    | Faktisk | Pris per enhet | Baserat på kategoriprisraden. |
    |        | Vid kostnad | Utifrån den relaterade faktiska kostnaden. |
    |        | Pålägg över kostnad | Ett pålägg tillämpas enligt definitionen på kategoriprisraden i enhetens kostnadstaxa för relaterade faktiska kostnadsvärden. |

1. Om systemet inte kan matcha värdena **Kategori** och **Enhet** ställs försäljningstaxan in på **0** (noll) som standard.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Fastställa försäljningstaxa på rader för utfall och uppskattning för Material

Uppskattning för **Material** refererar till:

- Information om offertrad för **Material**.
- Information om kontraktrad för **Material**.
- Materialuppskattningsrader för ett projekt.

Utfall för **Material** refererar till:

- Journalraderna Inmatning och Korrigering för **Material**.
- Journalrader som skapas när en materialanvändningslogg skickas in.
- Information om fakturarad för **Material**. 

När en prislista för försäljning har fastställts slutför systemet följande steg för att ange ett standardföräljningspris per enhet.

1. Systemet matchar kombinationen av fälten **Produkt** och **Enhet** på uppskattningsraden för **Material** mot prislistepostraderna i prislistan.
1. Om systemet hittar en prislistepostrad som har en försäljningstaxa för kombinationen av **Produkt** och **Enhet** och prissättningsmetoden är **Valutabelopp**, används det försäljningspris som anges på prislistan. 
1. Om värdena i fälten **Produkt** och **Enhet** inte matchar eller om prissättningsmetoden är någon annan än **Valutabelopp** ställs försäljningstaxan in på **0** (noll) som standard. Detta beror på att Project Operations endast stöder prismodellen **Valutabelopp** för material som används i ett projekt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
