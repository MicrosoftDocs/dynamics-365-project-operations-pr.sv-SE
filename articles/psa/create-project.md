---
title: Skapa ett projekt
description: Skapa ett projekt i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085552"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="a2510-103">Skapa ett projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a2510-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a2510-104">Skapa ett projekt med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktionerna i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] när du vill skapa en möjlighet, en offert eller ett avtal för projektbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="a2510-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="a2510-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktionerna hjälper dig att hantera ditt projekt från affärsmöjlighet till slutförande.</span><span class="sxs-lookup"><span data-stu-id="a2510-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="a2510-106">När du skapar ett projekt ska du också skapa en uppdelad arbetsstruktur, vilket påverkar dina offerter, utgiftsuppskattningar och resurshantering.</span><span class="sxs-lookup"><span data-stu-id="a2510-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="a2510-107">Gå till **Project Service > Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a2510-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="a2510-108">Klicka på **Nytt projekt**.</span><span class="sxs-lookup"><span data-stu-id="a2510-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="a2510-109">I området **Sammanfattning** ange ett namn för projektet och sedan fylla i så många detaljer som möjligt.</span><span class="sxs-lookup"><span data-stu-id="a2510-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="a2510-110">Objekt som är markerade med en röd asterisk (\*) är obligatoriska.</span><span class="sxs-lookup"><span data-stu-id="a2510-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="a2510-111">Klicka på **Spara** för att skapa projektet så att du kan fortsätta redigera det.</span><span class="sxs-lookup"><span data-stu-id="a2510-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="a2510-112">Därefter skapar du en uppdelad arbetsstruktur för projektet för att definiera aktiviteter, tid och resursroller som behövs för projektet.</span><span class="sxs-lookup"><span data-stu-id="a2510-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="a2510-113">Vid schemaläggning respekterar Project Service Automation tidszonen i den använda mallen **Arbetstimme**.</span><span class="sxs-lookup"><span data-stu-id="a2510-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="a2510-114">När du visar schemauppgifter visas start- och slutdatum för en aktivitet i användarens tidszon.</span><span class="sxs-lookup"><span data-stu-id="a2510-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="a2510-115">Detta gäller andra tidsfaser i formuläret **projekt**.</span><span class="sxs-lookup"><span data-stu-id="a2510-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="a2510-116">Om användarens tidszon inte överensstämmer med tidszonen för mallen arbetstid som används för projektet visas en varning om att skillnaden inträffar.</span><span class="sxs-lookup"><span data-stu-id="a2510-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="a2510-117">Se även</span><span class="sxs-lookup"><span data-stu-id="a2510-117">See Also</span></span>  
 [<span data-ttu-id="a2510-118">Guiden för projektledare</span><span class="sxs-lookup"><span data-stu-id="a2510-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
