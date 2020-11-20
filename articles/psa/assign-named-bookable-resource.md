---
title: Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter
description: I det här ämnet finns information om hur man bokar namngivna resurser till projektteam och tilldelar dem till uppgifter.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130195"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan lägga till en namngiven resurs i projektteamet genom att boka dem direkt på teamet. Följ stegen nedan.

1. I Project Service Automation, gå till **projekt** och välj de öppna projekt du bokar för.
2. På sidan **Projekt** på fliken **Team**, klicka på **Ny**. 

![Lägga till en teammedlem från fliken team](media/RM-how-to-1.png)

3. I dialogrutan **Snabbregistrering av projektteammedlem** väljer du den bokningsbara resursen. Fältet **Roll** fylls i med resursens standardroll om de har en tilldelad. Du kan ändra rollen vid behov. 
4. Välj de från- och till-datum som resursen behövs och välj allokeringsmetod för resursens kapacitet. 
5. Om du vill att teammedlemmen ska vara en projektgodkännare väljer du **Ja** i fältet **projektgodkännare**. Detta innebär att teammedlemmen kan godkänna skickade tid- och utgiftsposter för det här projektet. 
6. Klicka på **Spara**.

![Lägga till en teammedlem i formuläret snabbregistrering](media/RM-how-to-2.png)


Du kan nu tilldela den bokade resursen till aktiviteter i projektet. PÅ sidan **projekt** klickar du på fliken **schema** för att tilldela uppgifter till den nya resursen. Resursväljaren som startas från fältet **resurser** i uppgiftsrutnätet visar de team medlemmar som du kan välja.

![Tilldela en teammedlem till en uppgift på fliken schema](media/RM-how-to-3.png)

I version 3 av Project Service Automation (PSA), är inte resursbokningar och uppgiftstilldelningar tätt kopplade. Det innebär att när du använder resursväljaren i schemat kan du tilldela uppgifter till teammedlemmar så att de blir fler timmar än de som ingår i projektet.
Du kan se skillnaderna mellan bokningar av teammedlemmar och tilldelningar på fliken **Team** eller på fliken **resursavstämningar**. Du kan även stämma av skillnaderna mellan bokningar och tilldelningar för resurser på en mer detaljerad nivå.

![Fliken Resursavstämning](media/RM-how-to-4.png)

Du kan även använda resursväljaren på fliken **schema** om du vill söka efter och välja bokningsbara resurser som inte redan ingår i projektteamet. De visas i resursväljaren som **andra resurser**.

![Tilldela en uppgift till en icke-teammedlemresurs](media/RM-how-to-5.png)

När du gör detta läggs resursen till i projektteamet och tilldelas uppgiften, men inga bokningar skapas.

![Teammedlem med tilldelningar och inga bokningar](media/RM-how-to-6.png)

Du kan använda den utökade bokningsfunktionen på fliken **avstämning** eller **Schemaläggningstavla** för att boka resursens kapacitet på projektet.

![Utöka bokningar för en teammedlem på fliken resursavstämning](media/RM-how-to-7.png)

När en teammedlem är bokad i projektet kan du använda underhåll bokningar eller använda schemaläggningstavlan direkt för att hantera deras bokningar.
