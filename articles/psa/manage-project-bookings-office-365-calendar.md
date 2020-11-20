---
title: Hantera projekt och bokningar i din Office 365-kalender
description: Så här hanterar du projekt och bokningar i din Office 365-kalender
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 31ff541f5b817c29b162c38c282df8cfd866e375
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129070"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Hantera projekt och bokningar i din kalender (Project Service)

> [!Note]
> INAKTUELLT: Den här funktionen har utfasats och är inte längre tillgänglig.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Visa personliga möten, projektarbetsbokningar och arbetsorder för Field Service-tilldelningar med hjälp av [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalendern.  
  
 Eftersom allt är samlat på ett ställe, blir det enkelt att hantera din dag. Dina möten, avtalade tider, bokningar och uppgifter är tillgängliga i din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender.  
  
 Om du använder [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kan du också ange dina personliga möten i tidinmatningsvyn för Project Service. Detta gör att projekt- och resursansvariga vet din tillgänglighet för projekt. Dessutom sparar du tid eftersom du inte behöver ange information om privata möten två gånger. Du kan helt enkelt importera dina personliga möten från din kalender till tidinmatningsvyn för Project Service.  
  
 Din kalender synkroniserar projekt- och arbetsorderbokningar från dagens datum och upp till fyra veckor framåt. Denna inställning kan inte ändras.  
  
 Synkroniserar stöds endast åt ena hållet, från PSA till din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender. Du kan synkronisera i omvänd ordning. 
  
 För information om hur du använder din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, se [Kalendern i Outlook på webben för företag](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Konfiguration  
 Innan du kan visa och hantera dina bokningar i din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, måste du konfigurera ett par saker.  
  
- Du måste ha autentiseringsuppgifter för [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] global administratör eller Dynamics 365-systemadministratör.  
  
- Din administratör måste konfigurera e-postserverprofilen, och varje enskild användare måste konfigurera sin e-postlåda. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Ställa in e-postbearbetning via serversynkronisering](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Aktivera synkronisering för din organisation (administratörsuppgift)  
  
1.  I huvudmenyn klickar du på **Inställningar** > **Administration**.  
  
2.  Klicka på **Systeminställningar.**  
  
3.  Klicka på fliken **Synkronisering**.  
  
4.  Under **Välja om du vill aktivera synkronisering av resursbokning med**, markera **Synkronisera resursbokning med Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Aktivera synkronisering för din användarprofil (användaraktivitet)  
  
1.  Klicka på knappen **Inställningar** längst upp till höger på skärmen.  
  
2.  Klicka på **Alternativ**.  
  
3.  Klicka på fliken **Synkronisering**.  
  
4.  Under **Resursbokningssynkronisering med Outlook** markerar du **Synkronisera resursbokning med Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importera dina personliga möten (användaraktivitet)  
 Du kan importera dina personliga möten från din kalender till inmatningsvyn för Project Service Automation.  
  
1. Öppna kalendern i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] och klicka på **Importera data**.  
  
2. Välj **Möten från Exchange** på skärmen Filter, och klicka sedan på **Använd**.  
  
3. Systemet kommer att hämta avtalade tider i inmatningsvyn för tid i form av föreslagna poster från den aktuella veckan. Klicka på **Föregående** eller **Nästa**.  
  
4. Markera den avtalade tiden som du vill lägga till i inmatningsvyn för Project Service Automation.  
  
5. I popup-rutan **Tidspost** markerar du lämpliga alternativ för att konvertera den avtalade tiden till en inmatningsvy för Project Service Automation.  
  
6. Klicka på **Spara**.  
  
### <a name="see-also"></a>Se även  
 [Guide för tid, utgifter och samarbete](../psa/time-expense-collaboration-guide.md)
