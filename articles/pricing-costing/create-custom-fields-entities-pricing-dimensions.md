---
title: Skapa anpassade fält och entiteter som prissättningsdimensioner
description: I det här ämnet finns information om hur du skapar anpassade alternativuppsättningar eller entiteter.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4912087d7a19f5f342beff94723acd6131ce2dd8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580708"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Skapa anpassade fält och entiteter som prissättningsdimensioner

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Slutför följande steg när du vill skapa en anpassad alternativuppsättning eller -entitet för att använda denna som en prissättningsdimension. Mer information finns i [Översikt över prissättningsdimensioner](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning. Denna viktiga bästa praxis ger flexibilitet i framtiden att uppdatera eller ta bort ändringar efter behov. Detta kommer också att bidra till återanvändningen av ditt arbete och göra det enklare att överföra dessa ändringar till en annan instans När du har gjort alla nödvändiga ändringar, exportera då denna lösning som en **hanterad lösning** och importera den till andra instanser för att återanvända din prissättningskonfiguration.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning

En prissättningsdimension kan vara en alternativuppsättning eller en entitet. Båda måste skapas i din prissättningslösning. Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.

### <a name="entity-based-dimensions"></a>Entitetsbaserade dimensioner
Skapa entitetsbaserade dimensioner genom att följa dessa steg:

1. Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.
2. I det vänstra navigeringsfönstret i lösningsutforskaren väljer du **Entiteter**.
3. Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**. 
4. Ange återstående information som krävs och klicka sedan på **Spara**.

> ![Definition av entiteten standardrubrik.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Alternativuppsättningsbaserade dimensioner 
Du kan skapa två alternativbaserade dimensioner. 

- Använd **Arbetsplats för resurs** för att spåra priset för arbete på platsen **Start** och platsen **På plats**. 
- Använd **Arbetstider för resurs** med värdena **Vanlig** och **Övertid** för att tillämpa ett pålägg när arbetet är slutfört.

Följande grafik ger en vy över dimensionen **Arbetsplats för resurs**. 

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetsplats.](media/Option-set-PD-called-Resource-Work-Location.png)

Följande grafik ger en vy över dimensionen **Arbetstider för resurs**. 

> ![Alternativuppsättningsbaserad prissättningsdimension med namnet Resursens arbetstimmar.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I det vänstra navigeringsfönstret i lösningsutforskaren väljer du **Alternativuppsättningar**. 
3. Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.

## <a name="create-data-for-entity-based-dimensions"></a>Skapa data för entitetsbaserade dimensioner

Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal. Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**. Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.

1. Välj **Avancerad sökning**.
2. Markera entiteten **Standardrubrik** och välj sedan **Resultat**. Alla rader i entiteten **standardrubrik** visas.
3. Välj **Ny** och i fältet **Namn** ange "Systemtekniker" och välj sedan **Spara**.
4. Stäng sidan. 
5. Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.

> ![Exempeldata för entiteten Standardrubrik.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]