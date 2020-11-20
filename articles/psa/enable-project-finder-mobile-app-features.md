---
title: Aktivera funktionerna för Project Finder Mobile-appen
description: Aktivera funktionerna i appen Project Finder Mobile för Project Service
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132985"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivera funktionerna för Project Finder Mobile-appen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Dina resurser kan använda appen Project Finder Mobile på sina telefoner med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i syfte att hitta nya projekt att arbeta med och uppdatera sina kompetenser.  
  
 Appen finns tillgänglig för [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner och [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Du måste ange ett par olika alternativ i parameterinställningen för din organisationsenhet så att användarna kan visa projektresurskrav och uppdatera sina färdigheter.  
  
> [!NOTE]
>  Project Finder Mobile-appen fungerar bara med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], inte med installationer för lokal version.  
  
1. Gå till **Project Service > Parametrar**.  
  
2. Klicka på den parameterinställning du vill använda för att tillåta Project Finder Mobile-appfunktionerna.  
  
3. I området **Allmänt** anger du **Resurskrav visas för resurser** till **Ja**.  
  
4. Ange **Tillåt resurs att uppdatera färdighet** till **Ja**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Detta är en global inställning. Projektledare kan ange om ett enskilt projekt kommer att visas i det projektets **projektteam**-sida.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-postaviseringar  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] skickar e-post som berör begäran om resurser till följande mottagare vid följande tidpunkter:  
  
|Mottagare|Händelse|  
|---------------|-----------|  
|Projektledare|-   När en resurs registrerar sig för ett projekt med Project Finder Mobile-appen.|  
|Resurs|-   När det projektarbete som resursen har registrerats för redan har slutförts av en annan resurs.<br />-   När deras begäran om kompetensgodkännande har godkänts eller avvisats.<br />-   När deras begäran om projektregistrering har godkänts eller avvisats.|  
  
## <a name="privacy-notice"></a>Sekretessmeddelande  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Se även  
 [Konfigurera resurser](../psa/set-up-resources.md)
