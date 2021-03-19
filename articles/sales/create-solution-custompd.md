---
title: Skapa en lösning för anpassade prissättningsdimensioner
description: I det här ämnet finns information om hur du skapar lösningar för anpassade prissättningsdimensioner.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278440"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Skapa en lösning för anpassade prissättningsdimensioner

 _**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_ 

>[!IMPORTANT]
>Alla anpassningar av ändringar i prisdimension ska vara i en separat lösning. Denna viktiga rekommenderade metod ger flexibilitet att uppdatera eller ta bort ändringar efter behov, den bidrar till att underlätta återanvändning av ditt arbete samt gör det lättare att överföra ändringar till andra instanser. När du har gjort alla nödvändiga ändringar exporterar du lösningen som en **hanterad** lösning och importerar den sedan till andra instanser för återanvändning.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Skapa en lösning för anpassade prissättningsdimensioner

1.  Välj **Inställningar** > **Lösningar** och välj sedan **Ny**.
2.  Namnge lösningen *<your organization name>-prissättningsdimensioner*.
3. Ange återstående information som krävs och klicka sedan på **Spara**.

  ![Skapa en anpassad lösning för prissättningsdimension](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lägg till alla obligatoriska entiteter och relaterade komponenter i prisdimensionslösningen

Lägg till följande Project Service-entiteter i din prissättningslösning för att göra viktiga schemaändringar i prissättningslösningen. När du har slutfört den här proceduren kommer entiteterna att känna igen de nya prissättningsdimensionerna.

1.  Välj **Inställningar** > **Lösningar** och dubbelklicka sedan på **<*ditt organisationsmamn*> prissättningsdimensioner**.
2.  I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.
3.  I dialogrutan **lösningskomponenter** markerar du följande entiteter:
 
   - **Faktisk**
   - **Bokningsbar resurs**
   - **Beräkningsrad**
   - **Projektuppgift**
   - **Information om fakturarad**
   - **Journalrad**
   - **Information om projektkontraktrad**
   - **Projektgruppmedlem**
   - **Information om offertrad**
   - **Pålägg för rollpris**
   - **Pris för roll**
   - **Tidspost**
 
   ![Lägg till lösning för anpassade prissättningsdimensioner](./media/Existing-entities-to-PD-solution.png)
 
 4. För varje entitet granskar du de komponenter som läggs till och den slutliga listan över entitetstillgångar för respektive entitet. 

   >[!NOTE]
   > Inkludera alla formulär och vyer för samtliga valda entiteter.

  ![Tillagda entiteter](./media/solution-component-selection.png)


5.  När du uppmanas att inkludera eventuella beroende entiteter för de valda entiteterna väljer du **Nej, inkludera inte nödvändiga komponenter.**

    ![Inkludera beroende enheter](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]