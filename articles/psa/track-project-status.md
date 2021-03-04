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
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="18bd1-103">Följa upp projektstatus (Project Service)</span><span class="sxs-lookup"><span data-stu-id="18bd1-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="18bd1-104">Använd [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] för att följa utvecklingen i ett kundprojekt.</span><span class="sxs-lookup"><span data-stu-id="18bd1-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="18bd1-105">När engagemanget fortlöper, uppdateras projektstadier för att återspegla stadiet för åtagandet:</span><span class="sxs-lookup"><span data-stu-id="18bd1-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="18bd1-106">**Nytt**</span><span class="sxs-lookup"><span data-stu-id="18bd1-106">**New**</span></span>    | <span data-ttu-id="18bd1-107">När du skapar ett projekt anges stadiet till **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="18bd1-108">Om du har skapat projektet från en mall kan projektet i detta skede ha ett schema, uppskattningar och teamdata.</span><span class="sxs-lookup"><span data-stu-id="18bd1-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="18bd1-109">Annars blir den projektets disposition och du måste manuellt ange resten av projektkomponenterna.</span><span class="sxs-lookup"><span data-stu-id="18bd1-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="18bd1-110">**Offert**</span><span class="sxs-lookup"><span data-stu-id="18bd1-110">**Quote**</span></span>   |      <span data-ttu-id="18bd1-111">När du associerar ett projekt till en offert eller skapar det från en offert, anges projektstadiet som **Offert**, och de uppskattade start- och slutdatumen uppdateras också.</span><span class="sxs-lookup"><span data-stu-id="18bd1-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="18bd1-112">När projektet är i offertstadiet visas information om offerten på fliken **Försäljning** fliken på sidan **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="18bd1-113">**Planera**</span><span class="sxs-lookup"><span data-stu-id="18bd1-113">**Plan**</span></span>   |                                     <span data-ttu-id="18bd1-114">När du vinner en offert som är associerad med ett projekt och åtagandet övergår i kontraktstadiet uppdateras projektfasen till **Planera**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="18bd1-115">Information om kontraktet visas på fliken **Försäljning** på sidan **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="18bd1-116">**Slutförd**</span><span class="sxs-lookup"><span data-stu-id="18bd1-116">**Complete**</span></span> |                    <span data-ttu-id="18bd1-117">När du är klar med arbetet i projektet du kan byta stadium **Slutfört**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="18bd1-118">Det är underförstått att arbetet är 100 % färdigt när projektstadiet anges till slutfört, men projektet hålls öppet för eventuella väntande tids- och utgiftsutgifter ska registreras.</span><span class="sxs-lookup"><span data-stu-id="18bd1-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="18bd1-119">**Stäng**</span><span class="sxs-lookup"><span data-stu-id="18bd1-119">**Close**</span></span>   |           <span data-ttu-id="18bd1-120">Om du inte förväntar dig fler transaktioner ska loggas och alla transaktioner har registrerats i projektet kan du manuellt ange stadiet till **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="18bd1-121">När projektet är inställt på **Stäng** kan du inte logga några fler transaktioner i projektet och projektet är skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="18bd1-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="18bd1-122">Följa upp projektstatus</span><span class="sxs-lookup"><span data-stu-id="18bd1-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="18bd1-123">Gå till **Project Service > Projekt**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="18bd1-124">Klicka på projektet du vill arbeta med.</span><span class="sxs-lookup"><span data-stu-id="18bd1-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="18bd1-125">Välj nedpilen bredvid projektnamnet i fältet överst på skärmen och klicka på **Projektspårning**.</span><span class="sxs-lookup"><span data-stu-id="18bd1-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="18bd1-126">Välj **Insatsspårning** eller **Kostnadsspårning** i listrutan ovanför uppgiftslistan.</span><span class="sxs-lookup"><span data-stu-id="18bd1-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="18bd1-127">Dubbelklicka på en uppgift om du vill redigera den.</span><span class="sxs-lookup"><span data-stu-id="18bd1-127">Double-click any task to edit it.</span></span> <span data-ttu-id="18bd1-128">Du kan också flytta eller ändra storlek på staplarna i Gantt-schemat om du vill ändra tid och förlopp för en uppgift.</span><span class="sxs-lookup"><span data-stu-id="18bd1-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="18bd1-129">Se även</span><span class="sxs-lookup"><span data-stu-id="18bd1-129">See Also</span></span>  
 [<span data-ttu-id="18bd1-130">Guiden för projektledare</span><span class="sxs-lookup"><span data-stu-id="18bd1-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
