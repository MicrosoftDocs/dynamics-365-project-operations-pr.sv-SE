---
title: Översikt över resursavstämning
description: I det här ämnet finns information om se till att resursbokningar och uppdrag till projekt är anpassade.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125740"
---
# <a name="resource-reconciliation-overview"></a>Översikt över resursavstämning

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

För teammedlemmar kombineras inte bokningar och tilldelningar är löst kopplade. Med andra ord kan resurser ha tilldelningar, men inga bokningar, eller så kan de inte ha bokningar men inga tilldelningar. Vanligtvis justeras projektbokningar och tilldelningar så att resurserna har rätt kapacitet för att utföra sina aktivitetstilldelningar. Bokningarna kan emellertid vara baserade på tillgänglighet, och tidsinställningar för aktiviteter kan ändras när projektet fortsätter. Därför är den fria kopplingen av bokningar och tilldelningar flexiblare.

Fliken **avstämning** på formuläret **Projekt** låter projektledarna avstämma teammedlemmarnas bokningar och deras tilldelningar för sina projektteam.

Fliken **avstämning** visar bokningar och tilldelningar ned till nivån för enskilda uppgiftstilldelningen för varje teammedlem. Timmar visas i celler som kan representera tidsperioder från månader ned till dagar.

Fliken visar även en total nettosumma för projektet tillsammans med en **total** kolumn.

För varje resurs beräknar fliken en skillnad mellan en teammedlems bokningar och sammanslagningen av teammedlemmens aktivitetstilldelningar. Vi rekommenderar att skillnaden är 0 (noll). Det bör alltså inte finnas någon skillnad mellan bokningar och tilldelningar. Skillnader är färgade och tonade för att framhäva två villkor:

- **Underskott för bokning** – Underskott för bokning uppstår om en resurs har fler tilldelningar än bokningar. Eftersom denna kapacitet inte har reserverats kan en projektledare korrigera problemet genom att utöka resursens bokningar så att underskottet täcks.
- **Överflödiga bokningar** – Överflödiga bokningar inträffar när en resurs har bokats i projektet men inte tilldelats aktiviteter. Det här tillståndet kan vara acceptabelt i de fall då resursen togs i projektet före tilldelning av uppgifter. I andra fall är inte resursen planerad att tilldelas till uppgifter. I så fall bör projektledaren överväga att annullera resursbokningarna så att kapaciteten kan användas för ett annat projekt.

I vissa fall kan du se en nettoskillnad i noll för en resurs (t.ex. månadsnivån) när du visar tid på en högre nivå än dag nivå (till exempel månadsnivån). Om du visar tid på veckonivån kan du se att det finns tilldelningar på noll timmar och bokningar på 40 timmar under den första veckan men tilldelningar på 40 timmar och bokningar på noll timmar i den andra veckan i månaden. Generellt synkroniseras bokningarna och tilldelningarna, men de skiljer sig från en vecka till nästa.

När du visar högre tidsnivåer visar har celler i fliken **avstämning** har en indikator som meddelar att det finns olikheter på lägre nivåer. Genom att dubbelklicka i en cell kan du zooma in för att visa skillnaden. Du kan sedan högerklicka för att zooma ut. Genom att välja en resurs och sedan använda kontrollen **nästa skillnad** i verktygsfältet i rutnätet kan du gå vidare till nästa skillnad mellan bokningar och tilldelningar för resursen. Därefter kan du använda kontrollen **föregående skillnad** för att gå tillbaka. Du kan också inaktivera skillnadsindikator och navigeringsbeteende under **inställningar**.


I situationer där du har aktivitetstilldelningar för en resurs men inga bokningar, på sidan **Projekt** på fliken **Avstämning**, välj underskott för bokningen och sedan **utöka bokning**. I dialogrutan **utöka bokning** visas och visar den bokning som behövs för att lösa resursens underskott. Den visar även resursens befintliga bokningar för alla projekt eller andra schemalagda entiteter. Om du väljer **OK** för att skapa bokningen för resursen, oavsett resursens tillgänglighet, kan det leda till överbokning.

Projektledaren eller resursansvarig kan sedan använda schemaläggningstavlan för att hantera alla situationer där en resurs har blivit överbokad utanför sin kapacitet.

