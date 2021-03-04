---
title: Följa upp projektstatus
description: Spåra projektstatus i Project Service
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149610"
---
# <a name="track-a-projects-status-project-service"></a>Följa upp projektstatus (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Använd [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] för att följa utvecklingen i ett kundprojekt.  

När engagemanget fortlöper, uppdateras projektstadier för att återspegla stadiet för åtagandet:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nytt**    | När du skapar ett projekt anges stadiet till **Nytt**. Om du har skapat projektet från en mall kan projektet i detta skede ha ett schema, uppskattningar och teamdata. Annars blir den projektets disposition och du måste manuellt ange resten av projektkomponenterna. |
|  **Offert**   |      När du associerar ett projekt till en offert eller skapar det från en offert, anges projektstadiet som **Offert**, och de uppskattade start- och slutdatumen uppdateras också. När projektet är i offertstadiet visas information om offerten på fliken **Försäljning** fliken på sidan **Projekt**.      |
|   **Planera**   |                                     När du vinner en offert som är associerad med ett projekt och åtagandet övergår i kontraktstadiet uppdateras projektfasen till **Planera**. Information om kontraktet visas på fliken **Försäljning** på sidan **Projekt**.                                      |
| **Slutförd** |                    När du är klar med arbetet i projektet du kan byta stadium **Slutfört**. Det är underförstått att arbetet är 100 % färdigt när projektstadiet anges till slutfört, men projektet hålls öppet för eventuella väntande tids- och utgiftsutgifter ska registreras.                     |
|  **Stäng**   |           Om du inte förväntar dig fler transaktioner ska loggas och alla transaktioner har registrerats i projektet kan du manuellt ange stadiet till **Stäng**. När projektet är inställt på **Stäng** kan du inte logga några fler transaktioner i projektet och projektet är skrivskyddat.           |

## <a name="to-track-a-projects-status"></a>Följa upp projektstatus  

1.  Gå till **Project Service > Projekt**.  

2.  Klicka på projektet du vill arbeta med.  

3.  Välj nedpilen bredvid projektnamnet i fältet överst på skärmen och klicka på **Projektspårning**.  

4.  Välj **Insatsspårning** eller **Kostnadsspårning** i listrutan ovanför uppgiftslistan.  

5.  Dubbelklicka på en uppgift om du vill redigera den. Du kan också flytta eller ändra storlek på staplarna i Gantt-schemat om du vill ändra tid och förlopp för en uppgift.  

### <a name="see-also"></a>Se även  
 [Guiden för projektledare](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]