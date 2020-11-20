---
title: Konfigurera inställningar för ytterligare parametrar
description: Konfigurera ytterligare parameterinställningar i Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129385"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfigurera ytterligare parameterinställningar (Project Service)

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
