---
title: Konfigurera inställningar för ytterligare parametrar
description: Konfigurera ytterligare parameterinställningar i Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 0ceaa3af630df132339895a8497e49daf2e102c3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592357"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfigurera ytterligare parameterinställningar (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

När du har konfigurerat artiklarna i föregående avsnitt, måste du ange ytterligare projektparametrar som ska användas till dina projekt. När du först installerade [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] så skapade du en parameterinställning för att först skapa alla poster som krävs för [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] att fungera. Nu är det dags att gå tillbaka och konfigurera ytterligare fält för de här inställningarna.  
  
 Du måste ha konfigurerat följande inställningar:  
  
-   Organisationsenhet  
  
-   Faktureringsfrekvens  
  
-   Arbetstidsmall  
  
-   Prislista  
 
I det här steget ska du också ange vilken typ av resursallokering som du vill använda:  
  
- **Central**. Bara resursansvariga kan fördela resurser till projekt.  
  
- **Hybrid**. Resursansvariga, projektledare och kontoansvariga kan fördela resurser till projekt.  
  
 
Om du vill konfigurera projektparametrar:  
  
1. Gå till **Project Service > Parametrar**.  
  
2. Klicka på den parameterinställning som du vill konfigurera (den som du skapade när du först installerade [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), eller klicka på **Ny** för att skapa en ny.  
  
3. I området **Allmänt** anger du alla alternativ för dina projektparametrar.  
  
4. I området **Prislista**, klicka på **+** om du vill lägga till en prislista, väljer en prislista i listrutan **Prislista för projektparameter** och klickar sedan på **Spara**.  
  
5. Klicka på knappen **Spara** längst ned till höger på skärmen.  

> [!NOTE]
> Projektparameterposten måste finnas kvar för att Project Service ska fungera korrekt. Den här posten bör inte tas bort.

### <a name="see-also"></a>Se även  
 [Konfigurera resurser](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
