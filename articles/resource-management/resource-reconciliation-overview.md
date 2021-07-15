---
title: Resursavstämning – Översikt
description: Detta ämne innehåller information som hjälper dig att se till att resursbokningar och tilldelningar för projekt justeras.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c48589e745dbf6e3a51ae749b9b45491d26406e
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368228"
---
# <a name="resource-reconciliation-overview"></a>Resursavstämning – Översikt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

För teammedlemmar kombineras inte bokningar och tilldelningar är löst kopplade. Med andra ord kan resurser ha tilldelningar men inga inga bokningar, eller också kan de ha bokningar men inga tilldelningar. Vanligtvis justeras projektbokningar och tilldelningar så att resurserna har rätt kapacitet för att utföra sina aktivitetstilldelningar. Bokningarna kan emellertid vara baserade på tillgänglighet, och tidsinställningar för aktiviteter kan ändras när projektet fortsätter. Därför är den fria kopplingen av bokningar och tilldelningar flexiblare.

Fliken **Avstämning** på sidan **Projekt** låter projektledarna avstämma teammedlemmarnas bokningar och deras tilldelningar för sina projektteam.

Fliken **avstämning** visar bokningar och tilldelningar ned till nivån för enskilda uppgiftstilldelningen för varje teammedlem. Timmar anges i celler som kan representera perioder från månader till dagar. Fliken visar även en total nettosumma för projektet tillsammans med en **total** kolumn.

För respektive resurs beräknar fliken **Avstämning** skillnaden mellan teammedlemmens bokning och en sammanslagning av teammedlemmens uppgiftstilldelningar. Vi rekommenderar att skillnaden är 0 (noll). Det bör alltså inte finnas någon skillnad mellan bokningar och tilldelningar. Skillnader är färgade och tonade för att framhäva två villkor:

- **Underskott för bokning** – Underskott för bokning uppstår om en resurs har fler tilldelningar än bokningar. Eftersom kapaciteten inte har reserverats kanske projektledaren vill korrigera problemet genom att utöka resursens bokningar så att underskottet täcks.
- **Överflödiga bokningar** – Överflödiga bokningar inträffar när en resurs har bokats i projektet men inte tilldelats aktiviteter. Det här tillståndet kan vara acceptabelt i de fall då resursen bokats i projektet före tilldelningen av uppgifter. I andra fall där det inte finns någon plan för att tilldela resursen till uppgifter bör projektledaren dock överväga att avbryta resursens bokningar. På så sätt kan kapaciteten användas för ett annat projekt.

I vissa fall kan du se en nettoskillnad på noll för en resurs (t.ex. månadsnivån) när du visar tid på en högre nivå än dagsnivå (till exempel månadsnivån). Med andra ord motsvarar bokningarna tilldelningarna. Om du visar tid på veckonivån kan du se att det finns tilldelningar på noll timmar och bokningar på 40 timmar under den första veckan men tilldelningar på 40 timmar och bokningar på noll timmar i den andra veckan i månaden. Generellt synkroniseras bokningarna och tilldelningarna, men de skiljer sig från en vecka till nästa.

När du visar högre tidsnivåer har cellerna i fliken **Avstämning** en indikator som meddelar att det finns olikheter på lägre nivåer. Genom att dubbeltrycka eller dubbelklicka i en cell kan du zooma in för att visa skillnaden. Du kan sedan trycka och hålla (eller högerklicka) för att zooma ut. Genom att välja en resurs och sedan använda kontrollen **Nästa skillnad** i verktygsfältet i rutnätet kan du gå vidare till nästa skillnad mellan bokningar och tilldelningar för resursen. Därefter kan du använda kontrollen **föregående skillnad** för att gå tillbaka. Du kan också inaktivera skillnadsindikator och navigeringsbeteende under **inställningar**.

I situationer där du har uppgiftstilldelningar för en resurs men inga bokningar väljer du bokningsbristen på fliken **Avstämning** på sidan **Projekt** och sedan **Utöka bokning**. I dialogrutan **Utöka bokning** som visas anges den bokning som krävs för att adressera resursens underskott. Dialogrutan visar även resursens befintliga bokningar för alla projekt eller andra schemalagda entiteter. Om du väljer **OK** för att skapa bokningen för resursen, oavsett resursens tillgänglighet, kan det leda till överbokning.

Bokningar som skapas genom åtgärden **Utöka bokning** associeras med det primära projektkravet. När ett tillägg initieras går det inte att fastställa det specifika kravet som måste utökas, detta eftersom resursen kan vara associerad med mer än ett krav för projektet.

Projektledaren eller resursansvarig kan sedan använda schemaläggningstavlan för att hantera alla situationer där en resurs har blivit överbokad utöver sin kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]