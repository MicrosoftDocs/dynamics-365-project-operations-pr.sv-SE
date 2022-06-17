---
title: Ange körsträcka med hjälp av nivåer av körsträckepris
description: Den här artikeln innehåller information om kilometerantal och nivåer för kilometerantal.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930156"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Ange körsträcka med hjälp av nivåer av körsträckepris

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

När en utgift rapporteras och den valda utgiftskategorin är **Körsträcka** beräknas beloppet för den utgiftsraden enligt beloppet *pris per körsträcka*. Det här beloppet fastställs med hjälp av definierade körsträckenivåer eller, om inga nivåer av körsträckepris har ställts in, genom att följa en standardkostnad per körsträcka. 

Nivåer av körsträckepris kan ställas in genom att gå till **Utgiftshantering** > **Konfiguration** > **Allmänt** > **Utgiftskategorier** > **Körsträcka** > **Kategorikonfiguration**.

När du har uppgraderat till 10.0.18 kan du överväga att aktivera körsträckefunktionen efter att ha granskat designändringarna nedan om din organisation använder utgiftskategorin för körsträcka. 

Den nya utformningen av nivåer av körsträckepris påverkar hur värdet i fältet **Kvantitet** bearbetas. Före lanseringen av 10.0.18 var värdet i fältet **Kvantitet** den nedre gränsen. När ackumulering överstiger det värdet används motsvarande pris.  Från och med 10.0.18 betraktas värdet i fältet **Kvantitet** som den övre gränsen. Motsvarande pris används om körsträckan är mindre än värdet i fältet **Kvantitet**.  Den nya modellen för körsträckenivåer hjälper till med enhetlighet över körsträckenivåer och bättre användbarhet.   

Alla godkända utgiftsrapporter beräknas om vid publicering enligt den nya utformningen.

## <a name="example"></a>Exempel
 
### <a name="before-version-10018"></a>Före version 10.0.18
Med två nivåer av körsträckepris representerar fältet **Kvantitet** på varje nivå den lägre körsträckegränsen. För närvarande har nivå ett ett värde på noll (0) och ett pris på 0,45, och nivå två har ett värde på 1 000 och ett pris på 0,25. Om den ansamlade körsträckan passerar värdet i fältet används det relaterade priset. Om det inte finns någon rad med noll kvantitet används det körsträckepris som definieras i Utgiftshantering. 
 
Om en anställd skickar en utgiftsrapport med 1 500 miles blir de två körsträckeraderna i den utlagda utgiftsrapporten: 1 000 (pris 0,45) + 500 (pris 0,25) = 575,00.

### <a name="after-version-10018"></a>Efter version 10.0.18
I 10.0.18 representerar fältet **Kvantitet** på varje nivå den övre gränsen av nivån. För närvarande har nivå ett ett värde på 999 och ett pris på 0,45, och nivå två har ett värde på 999 999 999,00 och ett pris på 0,25. Om den ansamlade körsträckan passerar värdet i fältet **Kvantitet** används det relaterade priset. Om alla övre gränser överskrids använder systemet det körsträckepris som definieras i Utgiftshantering. 
 
För att kunna beräkna samma scenario korrekt måste nivåuppsättningen ändras. Fältet **Kvantitet** i nivå ett har ett värde på 999,00 och ett värde på 999 999 999,00 i nivå två. Om en anställd överskrider den totala kvantiteten kilometer i nivå ett använder systemet det körsträckepris som definieras i Utgiftshantering. 
  
Om en anställd skickar en utgiftsrapport med 1 500 miles blir de två körsträckeraderna i den utlagda utgiftsrapporten: 1 000 (pris 0,45) + 500 (pris 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aktivera beräkning av körsträckebelopp för flera körsträckenivåer med samma prisfunktion

Funktionen **Beräkning av körsträckebelopp för flera körsträckenivåer med samma pris** förbättrar beräkningen av körsträckepris. Aktivera den här funktionen genom att följa stegen nedan.

1. Gå till **Arbetsytor** > **Funktionshantering**. 
2. I listan letar du upp och väljer **Beräkning av körsträckebelopp för flera körsträckenivåer med samma pris** och välj **Aktivera nu**.

När du har aktiverat funktionen återställer du körsträckenivåer så att de återspeglar värdet i fältet **Kvantitet**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
