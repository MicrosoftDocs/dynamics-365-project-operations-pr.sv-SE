---
title: Skapa en anpassad lösning för prissättningsdimensioner
description: I det här ämnet beskrivs hur du skapar en anpassad lösning när du skapar anpassade prisdimensioner.
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
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995288"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Skapa en anpassad lösning för prissättningsdimensioner

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Alla anpassningar av ändringar i prisdimension ska vara i en separat lösning. Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans. När du gör nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.

1. Välj **Inställningar** > **Lösningar** och välj sedan **Ny**. 
2. Ge lösningen ett namn, **\<your organization name> prissättningsdimensioner**, ange den information som krävs och klicka sedan på **Spara**.

> ![Skapa en anpassad lösning för prissättningsdimensioner.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Lägg till alla obligatoriska entiteter och relaterade komponenter i prisdimensionslösningen
Du måste lägga till följande Project Service-entiteter i din prissättningslösning. Slutför stegen i den här proceduren för att göra vissa viktiga schemaändringar i prissättningslösningen så att enheterna blir medvetna om de nya prissättningsdimensionerna.

1. Välj **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**. 
2. I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.
3. I dialogrutan **lösningskomponenter** markerar du följande entiteter:

- Faktisk
- Bokningsbar resurs
- Beräkningsrad
- Projektuppgift
- Information om fakturarad
- Journalrad
- Information om projektkontraktrad
- Projektteammedlem
- Information om offertrad
- Pålägg för rollpris
- Pris för roll 
- Tidspost 

> ![Lägg till befintliga entiteter i lösningen för prissättningsdimensioner.](media/Existing-entities-to-PD-solution.png)

> ![Välj lösningskomponenter.](media/Dimension-Components.png)

> [!NOTE]
> Se till att du tar med alla formulär och vyer för varje vald entitet.

4. Klicka på **Nej** om du uppmanas att ta med alla beroende entiteter för de valda entiteterna.

> ![Inkludera inte alla relaterade komponenter.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]