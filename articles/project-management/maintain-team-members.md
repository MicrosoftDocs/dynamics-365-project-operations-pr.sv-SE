---
title: Underhålla teammedlemmar
description: I det här ämnet finns information om bokning av namngivna resurser till projektteam och tilldela dem till uppgifter.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 00312c5a701768e0042e7e0236477c192690ded3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998658"
---
# <a name="maintain-team-members"></a>Underhålla teammedlemmar

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan lägga till en namngiven resurs i projektteamet genom att boka dem direkt på teamet.

1. I Dynamics 365 Project Operations, gå till **projekt** och välj de öppna projekt du bokar för.
2. På sidan **Projekt** under fliken **Team**, välj **Ny**. 
3. I dialogrutan **Snabbregistrering av projektteammedlem** väljer du den bokningsbara resursen. Fältet **Roll** fylls i med resursens standardroll om de har en tilldelad. Du kan ändra rollen. 
4. Välj de från- och till-datum som resursen behövs och välj allokeringsmetod för resursens kapacitet. 
5. I fältet **Projektgodkännare** väljer du **Ja** om du vill att teammedlemmen ska vara en projektgodkännare. Teammedlemmen kan godkänna skickade tids- och utgiftsposter för det här projektet. 
6. Välj **Spara**.

Du kan nu tilldela den bokade resursen till aktiviteter i projektet. På sidan **Projekt**, under fliken **Schema** tilldelar du uppgifter till den nya resursen. Resursväljaren som startas från fältet **resurser** i uppgiftsrutnätet visar de team medlemmar som du kan välja.


I Project Operations är inte resursbokningar och uppgiftstilldelningar tätt kopplade. När du använder resursväljaren i schemat kan du tilldela uppgifter till teammedlemmar så att de blir fler timmar än de som ingår i projektet.

Skillnaderna mellan bokföringar och tilldelningar av teammedlemmar visas på flikarna **Team** och **Resursavstämningar**. Du kan även stämma av skillnaderna mellan bokningar och tilldelningar för resurser på en mer detaljerad nivå.

Använd resursväljaren under fliken **Schema** om du vill söka efter och välja bokningsbara resurser som inte redan ingår i projektteamet. Dessa resurser visas i resursväljaren som **Andra resurser**.

När du gör ett val läggs resursen till i projektteamet och tilldelas uppgiften, men inga bokningar skapas.

Du kan använda den utökade bokningsfunktionen på fliken **avstämning** eller **Schemaläggningstavla** för att boka resursens kapacitet på projektet.

När en teammedlem är bokad i projektet kan du använda **Underhåll bokningar** eller **Schemaläggningstavlan** direkt för att hantera deras bokningar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]