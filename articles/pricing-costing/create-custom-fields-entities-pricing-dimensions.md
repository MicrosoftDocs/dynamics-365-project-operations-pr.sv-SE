---
title: Skapa anpassade fält och entiteter som prissättningsdimensioner
description: I det här ämnet finns information om hur du skapar anpassade alternativuppsättningar eller entiteter.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085578"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Skapa anpassade fält och entiteter som prissättningsdimensioner

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Slutför följande steg varje gång du vill skapa en anpassad alternativuppsättning eller entitet på.

> [!IMPORTANT]
> Vi rekommenderar att du gör alla anpassade prisändringar i en separat lösning. Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans. När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Skapa en anpassad lösning för prissättningsdimensioner
1. Klicka på **inställningar** > **lösningar** och klicka sedan på **Ny** för att skapa en ny lösning. 
2. Ge lösningen ett namn, **\<your organization name> prissättningsdimensioner** , ange den information som krävs och klicka sedan på **Spara**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Skapa anpassade fält och alternativuppsättningar i dimensionslösningen för prissättning

En prissättningsdimension kan vara en alternativuppsättning eller en entitet. Båda måste skapas i din prissättningslösning. Stegen i den här proceduren förklarar hur du skapar entitetbaserade dimensioner och alternativuppsättningsdimensioner.

### <a name="entity-based-dimensions"></a>Entitetsbaserade dimensioner

1. Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Entiteter**.
3. Klicka på **Ny** om du vill skapa en ny entitet som heter **standardrubrik**. 
4. Ange återstående information som krävs och klicka sedan på **Spara**.


### <a name="option-set-based-dimensions"></a>Alternativuppsättningsbaserade dimensioner 
Du kan skapa två alternativbaserade dimensioner. Använd **Resursens arbetsplats** för att spåra priset för platsarbetet **Start** och arbete **på plats** och använda **resursens arbetstider** med värdena **Reguljär** och **Övertid** för att tillämpa en markering när arbetet har slutförts.


1. Gå till **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **alternativuppsättningar**. 
3. Klicka på **ny** om du vill skapa en ny alternativuppsättning, ange den information som krävs och klicka sedan på **spara**.

## <a name="create-data-for-entity-based-dimensions"></a>Skapa data för entitetsbaserade dimensioner

Du kan skapa data för entitetsbaserade dimensioner manuellt, eller genom att använda Microsoft Excel import- eller servicesamtal. Följ stegen nedan om du vill skapa två standardrubriker **Systemtekniker** och **Senior systemtekniker** från den entitetbaserade dimensionen **Standardrubrik**. Om de data du vill skapa är små, som i följande exempel, kan du använda ett standardformulär.

1. Välj **Avancerad sökning** , markera enhetens **standardrubrik** och välj sedan **resultat**. Alla rader i entiteten **standardrubrik** visas.
2. Välj **Ny** och i fältet **Namn** ange "Systemtekniker" och välj sedan **Spara**.
3. Stäng formuläret. 
4. Skapa en ny standardrubrik för "senior systemteknikern" genom att upprepa steg 1-3.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lägg till alla obligatoriska entiteter och relaterade komponenter i prisdimensionslösningen
Du måste lägga till följande entiteter i din prissättningslösning. Följ stegen i den här proceduren för att göra vissa viktiga schemaändringar i prissättningslösningen så att enheterna blir medvetna om de nya prissättningsdimensionerna.

1. Välj **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
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


> [!NOTE]
> Se till att du tar med alla formulär och vyer för varje vald entitet.

4. Klicka på **Nej** om du uppmanas att ta med alla beroende entiteter för de valda entiteterna ovan.

