---
title: Hantera flera tidszoner
description: När ett projekt skapas baseras tidszonen på den tidszon som har angetts i mallen för arbetstid.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d3fc0453e3038839107a98c4179e6bd4aede95cf4a5fcfe2d52f823b83029485
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988718"
---
# <a name="manage-time-zones"></a>Hantera flera tidszoner

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


## <a name="projects"></a>Projekt

När ett projekt skapas baseras tidszonen på den tidszon som har angetts i mallen för arbetstid. I formuläret **Projektet** är datumen alltid relativa till tidszonen för den användare som är inloggad på varje flik, med undantag för fliken **Uppgift**. När du visar uppdelad arbetsstruktur visas alltid datumen i projektets tidszon.

## <a name="tasks"></a>Aktiviteter

När en uppgift skapas styrs starttid, sluttid och timmar/dag av arbetstiderna för projektet. Om en uppgift till exempel skapas med ett projekt vars tidszon är -8 PST och har följande arbetstider: 9:00 till 17:00 måndag till fredag. Uppgifter som skapas utan en tilldelning håller sig till starttiden och sluttiden i projektkalendern.

## <a name="manage-resources-with-time-zones"></a>Hantera resurser med tidszoner

För korrekta och förutsägbara resultat när du använder **Utöka bokning** finns två viktiga förutsättningar som måste uppfyllas:  

- Användaren måste konfigurera tidszonen för sina enheter så att den motsvarar den tidszon som har angetts i systemets **anpassningsinställningar**.
 
  ![Tidszonsinställningar i Windows 10.](media/reconcile-assignments-03.png)

  ![Tidszonsinställningar i inställningar för personliga alternativ.](media/reconcile-assignments-04.png)
 
- Den bokningsbara resursen måste innehålla minst en minuts arbetstid som överlappar med de profiler som används för att definiera det begärda tillägget. Till exempel följande resurser med arbetstider som faller mellan 9:00 och 19:00. 

  ![Jämförelse av resursprofiler.](media/reconcile-assignments-05.png)

Följande tabell visar:

- En projektkalendermall
- Resurs A: den här resursen har samma kalender och finns i samma tidszon som i projektet. Starttiden för bokningarna blir 9:00.
- Resurs B: den här resursen finns i en annan tidszon än projektet och startar klockan 7:00 i sin tidszon. Bokningarna kan emellertid börja klockan 9:00 eftersom det är den tidigaste starttiden för tilldelningens profil.
- Resurser C och D: resurserna finns i olika tidszoner, de skiljer sig från varandra och projektet och deras bokningar startas inte tidigare än deras respektive tillgängliga starttider.

|Entity  |Kalender  |
|-|-|
|Projektkalendermall   | ![projektkalender.](media/reconcile-assignments-06.png) |
|Resurs A  | ![Resurs A kalendern.](media/reconcile-assignments-06.png) |
|Resurs B  |  ![Resurs B kalendern.](media/reconcile-assignments-07.png) |
|Resurs C  |  ![Resurs C kalendern.](media/reconcile-assignments-08.png) |
|Resurs D  | ![Resurs D kalendern.](media/reconcile-assignments-09.png)  |
 
När du navigerar till vyn **Avstämning** visas resurstilldelningarna och tillhörande bokningsunderskott.

![Vyn avstämning före tillägg.](media/reconcile-assignments-10.png)

När funktionen för att utöka bokning har använts för varje resurs utökas bokningarna för varje resurs eftersom arbetstiderna för varje resurs överlappar profilen för underskottet.

![Vyn avstämning efter bokningstillägget.](media/reconcile-assignments-11.png) 

Observera att informationen i bokningarna visar olikheter i starttiden för bokningarna. Bokningarna börjar inte tidigare än starttiden för tilldelningens profil och tidigast den tillgängliga starttiden för resursen.

![Nya bokningar av resurserna på schemaläggningstavlan.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]