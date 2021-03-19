---
title: Preliminärboka krav
description: I det här ämnet finns information om hur du preliminärbokar krav.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282940"
---
# <a name="soft-book-requirements"></a>Preliminärboka krav

[!include [banner](../includes/psa-now-project-operations.md)]

Ett resurskrav kan vara en fast bokning. En fast bokning skapar ett förslag som förbrukar resursens kapacitet. Förslaget skickas sedan tillbaka till användaren som skapade begäran för godkännande. En preliminär bokning lägger till en resurs i ett projektteam och har en annan status på schemaläggningstavlan, men den förbrukar inte resursens kapacitet. Om du vill preliminärboka en resurs från schemaläggingstavlan anger du fältet **bokningsstatus** fältet boknings status till **preliminär**.

![Bokningsstatusen är inställd på preliminär](media/Resource-Management-image77.png)

När fliken **Team** finns i vyn **Namngivna teammedlemmar** visas resursen där. De preliminärbokade timmarna rapporteras i kolumnen **preliminärbokade timmar**.

![Preliminärbokade timmar i vyn Namngivna teammedlemmar](media/Resource-Management-image78.png)

Preliminärbokade teammedlemmar kan tilldelas uppgifter.

![Preliminärbokade teammedlemmar tilldelade till en uppgift.](media/Resource-Management-image79.png)

På fliken **avstämning** visas inga bokningar för en preliminärbokad resurs eftersom fliken **avstämning** endast betraktar fasta bokningar.

![Preliminärbokad resurs utan bokningar på fliken avstämning](media/Resource-Management-image80.png)

> [!NOTE]
> Du kan inte preliminärboka en resurs från ett krav som har genererats från en allmän teammedlem.

På schemaläggningstavlan används olika färger för preliminärbokningar för en resurs.

![Preliminärbokningar på schemaläggningstavlan](media/Resource-Management-image81.png)

Om du vill konvertera en preliminärbokning till en fast bokning högerklickar du på preliminärbokningen och väljer sedan **ändra status** \> **fast bokning** \> **fast**.

![Ändra bokningsstatus till fast](media/Resource-Management-image82.png)

Bokningen ändras och status ändras på Schemaläggningstavlan. Eftersom bokningsstatusen är **hård** visas resursen som bokad och dess kapacitet och tillgänglighet justeras.

Du kan använda samma metod för att annullera en fast bokning eller en preliminär bokning från Schemaläggningstavlan.

Om du vill konvertera en preliminär bokning till en fast bokad på projektets flik **Team** klickar du på resursen och väljer **bekräfta**.

![Bekräfta kommando](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]