---
title: Försäljningsberäkningar och projekt
description: I det här ämnet finns information om hur du kan dra nytta av schemat och uppskattningarna i försäljningsprocessen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756194"
---
# <a name="sales-estimates-and-projects"></a>Försäljningsberäkningar och projekt

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Under försäljningsprocessen kan du skapa försäljningsuppskattningar genom att länka ett projekt till en försäljningsoffert. På det här sättet kan deterministisk uppskattning genomföras under försäljningsprocessen, för att dra nytta av funktionerna för projektplanering och uppskattning. Om försäljningen går igenom kan den användas som bas för att använda schemat för försäljningsuppskattningen som grund för ytterligare förfining av projektplanen.

## <a name="linking-a-project-to-a-quote-line"></a>Länka ett projekt till en offertrad

När du skapar en projektbaserad offertrad kan du skapa ett nytt projekt eller associera ett befintligt projekt med sidan **offertrad**. 

> ![Offertradsformulär](media/project-8.png)
 
När du skapar ett nytt projekt från offertradsinformationen kan du dra nytta av projektmallar. Projektmallar är modellprojekt som representerar vanliga projektplaner och ekonomiska uppskattningar som är typiska i en organisation. De kan också representera kopior av projektplaner och uppskattningar från tidigare projekt.

> ![Information om offertrad](media/project-9.png)
  
När du skapar projektet från offerten associeras projektet automatiskt med på offertraden.

## <a name="components-of-estimates-in-a-project"></a>Komponenter i uppskattningar i ett projekt

Med ett schema kan du dela upp arbete i uppgifter, underhålla en hierarki med uppgifter, avgöra vilka resurser som krävs för att slutföra en uppgift och tilldela en uppskattning av vilken insats som krävs för att slutföra en uppgift.

Du kan ange arbetsinsats och schemauppskattningar med hjälp av fälten på fliken **schema** på sidan **projekt**. Eftersom en prislista associeras med projektet beräknas ekonomiska uppskattningar med hjälp av självkostnads- och försäljningspriser som definieras i prislistan.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importera uppskattningar från ett projekt till en offert

När du har definierat projektuppskattningar kan du importera dem till offertraden. På sidan **Information om offertrad**, välj **Importera från uppskattningar** i menyfliksområdet för att sammanfatta projektuppskattningar efter transaktionstyp, roll eller aktivitetsnivå.
