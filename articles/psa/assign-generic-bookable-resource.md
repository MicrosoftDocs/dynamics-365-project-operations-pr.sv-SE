---
title: Tilldela allmänna bokningsbara resurser till en uppgift och ett projektteam
description: I det här ämnet finns information om bokning av generiska resurser till aktivitets- och projektgrupper.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145425"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Tilldela allmänna bokningsbara resurser till en uppgift och generera resurskrav 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Utöver att boka och tilldela namngivna och verkliga resurser i projektet kan du tilldela allmänna resurser till projektaktiviteter. Dessa resurser kan användas som platshållare för namngivna resurser tills du är klar att bemanna projektet med namngivna resurser. 

1. I Project Service Automation (PSA), öppna sidan **projekt** och på fliken **schema** anger du positionsnamnet för den generiska resursen i cellen **Resurs** i schemat. Du kan också klicka på **Resurs** i cellen för att öppna resursväljaren och sedan ange namnet på den generiska resurs som du vill skapa.

![Skapa och tilldela en generisk teammedlem](media/RM-how-to-9.png)

Detta öppnar panelen **Snabbregistrering: Projektteammedlem**. 

2. Ange roll och organisationsenhet för den allmänna resursteammedlemmen och klicka sedan på **Spara**.

![Snabb skapande av generisk teammedlem](media/RM-how-to-10.png)

3. När du har skapat en ny generisk resursteammedlem tilldelas den aktiviteten. Du kan fortsätta att tilldela den allmänna resursen till andra uppgifter i aktivitetsschemat.

![Tilldela befintlig generisk teammedlem till uppgifter](media/RM-how-to-11.png)

4. När du har tilldelat den generiska resursen kan du skapa ett resurskrav och utföra den genom att direkt boka eller skicka en resursförfrågan till en resursansvarig.

![Skapa ett krav för en generisk teammedlem](media/RM-how-to-12.png)

Förutom att använda resursväljaren som nämnts ovan kan du lägga till allmänna resurser direkt i rutnätet med den generiska teammedlemmen. Resurserna läggs till med ett resurskrav som baseras på start- och slutdatumen och allokeringsmetoden som anges i panelen **Snabbregistrering: Projektteammedlem**.

Du kan se en skillnad om du lägger till den allmänna teammedlemmen direkt och sedan tilldelar fler uppgifter till den allmänna resursen än de som krävs för att täcka antalet timmar. Klicka **Generera krav** om du vill generera om behovet för att balansera de timmar som krävs för tilldelningarna.

Du kan också klicka på länken **resurskrav** i teamets rutnät för att öppna kravet och lägga till kunskaper, önskade resurser etc.

![Resurskrav](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]