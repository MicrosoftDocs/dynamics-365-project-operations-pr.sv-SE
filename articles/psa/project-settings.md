---
title: Projektinställningar
description: I det här ämnet finns information om inställningar för projekthantering.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 075cbdd30c4986e514e4d357a08ef99cf3eb101f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601316"
---
# <a name="project-settings"></a>Projektinställningar

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Använd följande inställningar för att komma åt funktionerna för projektplanering.

## <a name="work-template"></a>Arbetsmall

För att skapa ett projektschema skapar du en projektkalendermall som definierar antalet arbetstimmar per dag och alla öppettider för företaget. Om du vill skapa en projektkalendermall associerar du en arbetsmall med fältet **kalendermallen** för projektet. Skapa en arbetsmall genom att följa stegen nedan.

1. I PSA, i vänster navigationsfönster, klicka på **Resurser**. 
2. På listsidan **Resurser**, öppna en användarpost och välj sedan **Visa arbetstimmar**.

  > [!NOTE]
  > Kontrollera att popup-fönster tillåts på webbsidan. På så sätt kan du se resursens arbetstider.
  
3. På sidan **månatlig visning**, klicka på **konfigurera**. En lista med tre alternativ visas: 

  - Nytt veckoschema
  - Arbetsschema för en dag
  - Ledig tid

> ![Ange alternativ.](media/project-13.png)

4. Välj **Nytt veckoschema** och ange alternativen för det här resursschemat. Du kan ange ett återkommande veckoschema, dagliga timparametrar, företagets öppettider och mycket annat.
5. Ange datumintervall, välj **Spara** och klicka på **Stäng**. 
6. Gå tillbaka till listsidan **Resurser** och välj den resurs som du anger arbetstider för. 
7. Välj **Ange kalender som** för att ställa in arbetsmallen. 
8. I dialogrutan **Arbetsmall** anger du ett namn på arbetsmallen och klickar på **Använd**. 

Du kan nu associera arbetsmallen med en projektkalendermall.

## <a name="resource-roles"></a>Resursroller

Termen *resursroller* refererar till den uppsättning färdigheter, kompetenser och certifieringar som en person måste ha för att utföra en specifik uppsättning uppgifter i ett projekt. Med hjälp av PSA kan du ange kostnaden och fakturera en resurs tid utifrån den roll som resursen är associerad med. Varje organisation måste konfigurera de här rollerna med hjälp av den vänstra navigeringen på menyn **Project Service**.

Varje organisation måste skapa de här rollerna på sidan **Aktiva resurskategorier**. Om du vill öppna den här sidan markerar du **Resursroller**.

## <a name="price-lists"></a>Prislistor

Prislistor låter dig ställa in självkostnads- och försäljningspriser, utgiftskategorier, produkter och andra element i en organisation. Innan du anger ekonomiska uppskattningar för arbetet som måste levereras för ett projekt måste du skapa en bakomliggande utgifts- och prislista. I avsnittet parametrar bör du även ange en standardkostnads- och försäljningsprislista som gäller alla projekt som skapas i organisationen. På sidan **Aktiva projektparametrar** ser du till att du anger en standardkostnads- och försäljningsprislista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
