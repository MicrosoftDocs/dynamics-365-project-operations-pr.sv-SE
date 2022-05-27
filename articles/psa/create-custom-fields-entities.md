---
title: Skapa anpassade fält och entiteter
description: I det här ämnet beskrivs hur du skapar alternativuppsättningar och entiteter i din egen lösning i Power Apps-plattformen.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d2fbe6a4061a93ac3186bbc8624bf5d16209cdf9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574406"
---
# <a name="create-custom-fields-and-entities"></a>Skapa anpassade fält och entiteter 

[!include [banner](../includes/psa-now-project-operations.md)]

Slutför följande steg varje gång du vill skapa en anpassad alternativuppsättning eller entitet på Power Apps-plattformen.  
Procedurerna i det här ämnet ska slutföras med webbgränssnittet för PSA (Project Service Automation).

> [!IMPORTANT]
> Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning. Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans. När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning

En prissättningsdimension kan vara en alternativuppsättning eller en entitet. Båda måste skapas i din prissättningslösning. Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.

### <a name="entity-based-dimensions"></a>Entitetsbaserade dimensioner

1. I PSA, klicka på **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter**.
3. Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**. Ange återstående information som krävs och klicka sedan på **Spara**.

> ![Definition av entiteten standardrubrik.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Alternativuppsättningsbaserade dimensioner 
Du kan skapa två alternativbaserade dimensioner. Använd **Resursens arbetsplats** för att spåra priset för platsarbetet **Start** och arbete **på plats** och använda **resursens arbetstider** med värdena **Reguljär** och **Övertid** för att tillämpa en markering när arbetet har slutförts.


1. I PSA, klicka på **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **alternativuppsättningar**. 
3. Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetsplats.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetstimmar.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Skapa data för entitetsbaserade dimensioner

Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal. Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**. Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.

1. I PSA, klicka på **Avancerad sökning**. Markera entiteten **Standardrubrik** och klicka sedan på **Resultat**. Alla rader i entiteten **standardrubrik** visas.
2. Klicka på **Ny**. I fältet **Namn** anger du på "Systemtekniker" och klicka på **Spara**.
3. Stäng formuläret. 
4. Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.

> ![Exempeldata för entiteten Standardrubrik.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
