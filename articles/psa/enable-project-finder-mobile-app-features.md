---
title: Aktivera funktionerna för Project Finder Mobile-appen
description: Aktivera funktionerna i appen Project Finder Mobile för Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144570"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivera funktionerna för Project Finder Mobile-appen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Dina resurser kan använda appen Project Finder Mobile på sina telefoner med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i syfte att hitta nya projekt att arbeta med och uppdatera sina kompetenser.  
  
 Appen finns tillgänglig för [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner och [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Du måste välja vissa alternativ bland parameterinställningarna för din organisationsenhet, om du vill göra det möjligt för användarna att visa resurskrav för projekt samt uppdatera kompetenser.
  
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
|Projektledare|- En resurs registrerar sig för ett projekt med Project Finder Mobile-appen.|  
|Resurs|- Det projektarbete som resursen har registrerats för har redan gjorts av en annan resurs.<br />- Begäran om färdighetsgodkännande har godkänts eller avvisats.<br />- Begäran om projektregistrering har godkänts eller avvisats.|  
  
## <a name="privacy-notice"></a>Sekretessmeddelande  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Se även  
 [Konfigurera resurser](../psa/set-up-resources.md)
