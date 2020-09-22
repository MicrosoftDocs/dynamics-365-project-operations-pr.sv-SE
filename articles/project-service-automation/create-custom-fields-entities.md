---
title: Skapa anpassade fält och entiteter
description: I det här ämnet beskrivs hur du skapar alternativuppsättningar och entiteter i din egen lösning i Power Apps-plattformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756281"
---
# <a name="create-custom-fields-and-entities"></a>Skapa anpassade fält och entiteter 

Slutför följande steg varje gång du vill skapa en anpassad alternativuppsättning eller entitet på Power Apps-plattformen.  
Procedurerna i det här ämnet ska slutföras med webbgränssnittet för PSA (Project Service Automation).

> [!IMPORTANT]
> Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning. Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans. När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Skapa en anpassad lösning för prissättningsdimensioner
1. Klicka på **inställningar** > **lösningar** i PSA och klicka sedan på **Ny** för att skapa en ny lösning. 
2. Ge lösningen ett namn, **\<din organisations namn > prissättningsdimensioner**, ange den information som krävs och klicka sedan på **Spara**.

> ![Skapa en anpassad lösning för prissättningsdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning

En prissättningsdimension kan vara en alternativuppsättning eller en entitet. Båda måste skapas i din prissättningslösning. Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.

### <a name="entity-based-dimensions"></a>Entitetsbaserade dimensioner

1. I PSA, klicka på **Inställningar** > **Lösningar** och dubbelklicka sedan på  **\<organisationens namn > prissättningsdimensioner**.
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter**.
3. Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**. Ange återstående information som krävs och klicka sedan på **Spara**.

> ![Entiteten standardrubrik](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Alternativuppsättningsbaserade dimensioner 
Du kan skapa två alternativbaserade dimensioner. Använd **Resursens arbetsplats** för att spåra priset för platsarbetet **Start** och arbete **på plats** och använda **resursens arbetstider** med värdena **Reguljär** och **Övertid** för att tillämpa en markering när arbetet har slutförts.


1. I PSA, klicka på **Inställningar** > **Lösningar** och dubbelklicka sedan på  **\<organisationens namn > prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **alternativuppsättningar**. 
3. Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetsplats ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetstimmar ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Skapa data för entitetsbaserade dimensioner

Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal. Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**. Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.

1. I PSA, klicka på **Avancerad sökning**. Markera entiteten **Standardrubrik** och klicka sedan på **Resultat**. Alla rader i entiteten **standardrubrik** visas.
2. Klicka på **Ny**. I fältet **Namn** anger du på "Systemtekniker" och klicka på **Spara**.
3. Stäng formuläret. 
4. Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.

> ![Exempeldata för entiteten för standardrubrik ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lägg till alla obligatoriska PSA-entiteter och relaterade komponenter i prisdimensionslösningen
Du måste lägga till följande Project Service-entiteter i din prissättningslösning. Följ stegen i den här proceduren för att göra vissa viktiga schemaändringar i prissättningslösningen så att enheterna blir medvetna om de nya prissättningsdimensionerna.

1. I PSA, klicka på **Inställningar** > **Lösningar** och dubbelklicka sedan på  **\<organisationens namn > prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.
3. I dialogrutan **lösningskomponenter** markerar du följande entiteter:

- Faktiskt
- Bokningsbar resurs
- Beräkningsrad
- Information om fakturarad
- Journalrad
- Information om projektkontraktrad
- Projektteammedlem
- Information om offertrad
- Pålägg för rollpris
- Pris för roll 
- Tidspost 

> ![Lägg till befintliga entiteter i lösningen för prissättningsdimensioner](media/Existing-entities-to-PD-solution.png)

> ![Välj lösningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> Se till att du tar med alla formulär och vyer för varje vald entitet.

4. Klicka på **Nej**om du uppmanas att ta med alla beroende entiteter för de valda entiteterna ovan.

> ![Inkludera inte alla relaterade komponenter](media/Do-not-include-required.png)


