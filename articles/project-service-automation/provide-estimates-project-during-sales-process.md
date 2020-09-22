---
title: Tillhandahålla uppskattningar av arbete för ett projekt under försäljningsprocessen
description: Tillhandahålla arbetsuppskattningar för ett projekt under säljprocessen i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756273"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Tillhandahålla uppskattningar av arbete för ett projekt under försäljningsprocessen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Under försäljningsprocessen, kan du använda offertrader för ta fram försäljningsuppskattningar från början. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktioner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ger ett mer vetenskapligt och deterministiskt sätt att skapa säljuppskattningar, detta genom att bryta ned arbetsuppgifter och associera relevanta attribut som bidrar till projektuppskattningarna i den uppdelade arbetsstrukturen för arbetsuppgiften.  
  
 När du vinner försäljningen kan du använda den associerade uppdelade arbetsstrukturen i projektplanen, och förfina den efter behov för slutförande av projektet.  
  
## <a name="link-a-project-to-a-quote-line"></a>Länka ett projekt till en offertrad  
 När du skapar en projektbaserad offertrad kan skapa du ett nytt projekt från offertraden. Du kan sedan använda projektmallar som är antingen förkonfigurerade standardprojektplaner och ekonomiska uppskattningar som är gemensamma för din organisation, eller en kopia av en projektplan och uppskattningar från tidigare projekt. När skapar ett projekt och väljer en projektmall ger det en grund för att förfina projektplan, uppskattningar och rollkrav. Genom att skapa ett projekt från offerten associeras projektet automatiskt med på offertraden.  
  
## <a name="project-estimate-components"></a>Komponenter för uppskattning av projekt  
 Den uppdelade arbetsstrukturen i ett projekt är ett sätt att bryta ned arbete i uppgifter, upprätthålla en hierarki av uppgifter och tilldela en uppskattning av vilken insats som krävs för att slutföra varje aktivitet. Du kan också koppla roller till en uppgift för att visa en uppskattning av vilken typ av resurs som krävs för att slutföra en uppgift och ett schema.  
  
 Den uppdelade arbetsstrukturen hjälper dig att fastställa uppskattningar av arbetsinsats och schema. Som standard använder projektet standardprislistan som du definierade tidigare. Kostnads- och försäljningspriserna som är definierade i prislistorna hjälper till att fastställa ekonomiska uppskattningar för uppdelning av projektets arbete.  
  
 Om projektet är kopplat till en offert och offerten har en annan prislista som standard, används offertens prislista för ekonomiska beräkningar.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importera uppskattningar från ett projekt till en offert  
 När du har projektuppskattningar i projektet kan importera du dessa uppskattningar till offertraden:  
  
-   I **Information om offertrad** klickar du på **Importera från beräkning**. 

-   Välj om du vill importera projektberäkningar sammanfattade efter nodnivån transaktionstyp, roll eller uppdelad arbetsstruktur.  
  
### <a name="see-also"></a>Se även  
 [Guiden för projektledare](../project-service/project-manager-guide.md)
