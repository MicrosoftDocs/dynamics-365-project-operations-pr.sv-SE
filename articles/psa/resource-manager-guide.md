---
title: Guide för resurshanterare
description: En guide till resurshantering i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 4a26a384dfaf6b974ed35105434152e655ff6444
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085748"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="437ec-103">Guide för resursansvariga (Project Service)</span><span class="sxs-lookup"><span data-stu-id="437ec-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="437ec-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktionerna i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] hjälper dig att hitta rätt resurser i rätt tid för rätt projekt, samt se till att alla resurser används på ett effektivt sätt.</span><span class="sxs-lookup"><span data-stu-id="437ec-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="437ec-105">Använd ditt företags konsulter på ett effektivt sätt, och effektivt tillsammans med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="437ec-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="437ec-106">Dessa ger dig de verktyg du behöver för att schemalägga resurser baserat på krav och scheman i konsultprojekt och dina konsulteras färdigheter och tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="437ec-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="437ec-107">Du kan snabbt hitta de mest kvalificerade konsulterna som är tillgängliga för arbete i projekt, och ser du enkelt hur du schemalägger dem bättre under loppet av varje projekt.</span><span class="sxs-lookup"><span data-stu-id="437ec-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="437ec-108">Schemaläggning av resurser hjälper dig att göra följande:</span><span class="sxs-lookup"><span data-stu-id="437ec-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="437ec-109">Matcha resurser till projekt, baserat på hur väl deras kunskaper och färdighetsnivåer matchar resurskraven för projektet.</span><span class="sxs-lookup"><span data-stu-id="437ec-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="437ec-110">Matcha schemat för en resurs till en projektkalender, baserat på deras tillgänglighet och schemalagda lediga tid.</span><span class="sxs-lookup"><span data-stu-id="437ec-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="437ec-111">Den färgkodade kalendern ger visuell information om resurstillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="437ec-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="437ec-112">Granska varje konsults kapacitet och kontrollera hur kapaciteten som används för tillfället.</span><span class="sxs-lookup"><span data-stu-id="437ec-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="437ec-113">Detta kan hjälpa dig att hitta var en konsult kan vara under- eller överutnyttjad, eller om de arbetar i full kapacitet.</span><span class="sxs-lookup"><span data-stu-id="437ec-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="437ec-114">Tilldela en procentsats eller ett visst antal timmar för en arbetstagares kapacitet till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="437ec-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="437ec-115">Göra gruppresursbokningar.</span><span class="sxs-lookup"><span data-stu-id="437ec-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="437ec-116">Preliminärboka eller gör en fast bokning av resurser, och konvertera preliminärbokade timmar till fast bokade timmar i ett steg.</span><span class="sxs-lookup"><span data-stu-id="437ec-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="437ec-117">Automatiskt skapa en projektgrupp baserat på resurser som definierats i en uppdelad arbetsstruktur för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="437ec-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="437ec-118">Uppfylla resursbegäranden (boka, föreslå, hitta ersättningsresurser).</span><span class="sxs-lookup"><span data-stu-id="437ec-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="437ec-119">Tilldela resurser enligt en central modell (resursansvarig tilldelar) eller hybridmodell (resursansvarig och andra chefer kan tilldela).</span><span class="sxs-lookup"><span data-stu-id="437ec-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="437ec-120">Mer information om hur du anger en central jämfört med en kombinerad hanteringsmodell finns i [Konfigurera ytterligare parameterinställningar (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="437ec-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="437ec-121">Du kan hantera resurser effektivt mellan projekt och se till att projekten bemannas på lämpligt sätt.</span><span class="sxs-lookup"><span data-stu-id="437ec-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="437ec-122">Du måste utföra följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="437ec-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="437ec-123">[Hantera resursförfrågningar](../psa/manage-resource-requests.md)</span><span class="sxs-lookup"><span data-stu-id="437ec-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="437ec-124">Matcha dina konsulters färdigheter och kompetenser till rätt projekt.</span><span class="sxs-lookup"><span data-stu-id="437ec-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="437ec-125">[Visa resurstillgänglighet](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="437ec-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="437ec-126">Kontrollera tillgänglighet för konsulterna i en kalendervy.</span><span class="sxs-lookup"><span data-stu-id="437ec-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="437ec-127">[Visa resursutnyttjande](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="437ec-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="437ec-128">Se den procentandel av tid som dina konsulter är bokade för närvarande.</span><span class="sxs-lookup"><span data-stu-id="437ec-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="437ec-129">[Schemalägg resurser för ett projekt.](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="437ec-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="437ec-130">Schemalägg konsulter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="437ec-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="437ec-131">Läs mer om att skicka resursbegäranden för enskilda projekt i [Skicka resursbegäran](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="437ec-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="437ec-132">Se även</span><span class="sxs-lookup"><span data-stu-id="437ec-132">See Also</span></span>  
 <span data-ttu-id="437ec-133">[Översikt över Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="437ec-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="437ec-134">[Administratörsguide](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="437ec-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="437ec-135">[Guide för kontohanteraren](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="437ec-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="437ec-136">[Guiden för projektledare](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="437ec-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="437ec-137">Guide för tid, utgifter och samarbete</span><span class="sxs-lookup"><span data-stu-id="437ec-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
