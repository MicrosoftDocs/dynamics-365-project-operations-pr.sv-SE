---
title: Skapa projektmall
description: Skapa en projektmall i Project Service
author: ruhercul
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085553"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="11140-103">Skapa en projektmall (Project Service)</span><span class="sxs-lookup"><span data-stu-id="11140-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="11140-104">Med projektmallar sparar du tid om ditt företag regelbundet bjuder på liknande typer av projekt.</span><span class="sxs-lookup"><span data-stu-id="11140-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="11140-105">Du får en standarduppsättning roller och uppskattade timmar för en typ av projekt.</span><span class="sxs-lookup"><span data-stu-id="11140-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="11140-106">Kontoansvariga och projektledare kan skapa projekt baserade på en projektmall eller så kan de kan kopiera mallen och göra sin egen.</span><span class="sxs-lookup"><span data-stu-id="11140-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="11140-107">Komponenter i en projektmall</span><span class="sxs-lookup"><span data-stu-id="11140-107">Components of project template</span></span>
 <span data-ttu-id="11140-108">En projektmall består av tre komponenter:</span><span class="sxs-lookup"><span data-stu-id="11140-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="11140-109">**Uppdelad arbetsstruktur** : En uppdelad arbetsstruktur i en projektmall har samma uppsättning element som i projektet.</span><span class="sxs-lookup"><span data-stu-id="11140-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="11140-110">Du kan skapa en uppgiftshierarki, koppla roller till en aktivitet, definiera attribut i scheman, ange beroenden och visa alla data i Gantt.</span><span class="sxs-lookup"><span data-stu-id="11140-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="11140-111">Den uppdelade arbetsstrukturen projektmallar har också stöd för uppgiftslägen för varje uppgift.</span><span class="sxs-lookup"><span data-stu-id="11140-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="11140-112">Det är ingen skillnad mellan en projektmall och ett projekt när ett arbetsschema skapas.</span><span class="sxs-lookup"><span data-stu-id="11140-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="11140-113">**Projektberäkningar** : Projektberäkningar i mallar fungerar på samma sätt som de gör i projekt, förutom att prislistorna som ska användas som standard för utgifts- och försäljningspriser alltid utgör standardkostnad och -försäljningsprislistor angivna i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-parametrarna.</span><span class="sxs-lookup"><span data-stu-id="11140-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="11140-114">Övriga funktioner är desamma som i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="11140-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="11140-115">**Projektteambildning** : När ett projektteam bildas för en projektmall går det inte att boka en namngiven resurs i en mall.</span><span class="sxs-lookup"><span data-stu-id="11140-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="11140-116">Du kan använda **Generera projektteam** i den uppdelade arbetsstrukturen för att generera en uppsättning allmänna resurser.</span><span class="sxs-lookup"><span data-stu-id="11140-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="11140-117">Du kan även ange de kunskaper som krävs och kompetenser för allmänna resurser.</span><span class="sxs-lookup"><span data-stu-id="11140-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="11140-118">Du kan inte ersätta en allmän resurs med en bokningsbar resurs i projektmallar.</span><span class="sxs-lookup"><span data-stu-id="11140-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="11140-119">Skapa ett projekt från en mall</span><span class="sxs-lookup"><span data-stu-id="11140-119">Create a project from a template</span></span>  
 <span data-ttu-id="11140-120">Du kan skapa ett projekt från en mall på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="11140-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="11140-121">Du kan välja en projektmall i projektet för att snabbt skapa formulär när du skapar ett projekt i offerten.</span><span class="sxs-lookup"><span data-stu-id="11140-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="11140-122">När du skapar ett projekt genom att klicka på **Nytt projekt** visas i formuläret innan du sparar posten.</span><span class="sxs-lookup"><span data-stu-id="11140-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="11140-123">Härifrån kan du klicka på fältet **Välj en mall** om du vill välja från listan över fördefinierade projektmallar i organisationen.</span><span class="sxs-lookup"><span data-stu-id="11140-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="11140-124">Klicka på **Skapa projekt från en mall** på sidan **Projektmall** om du vill skapa ett projekt från mallen.</span><span class="sxs-lookup"><span data-stu-id="11140-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="11140-125">Kopiera komponenter av en mall till ett projekt</span><span class="sxs-lookup"><span data-stu-id="11140-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="11140-126">När du kopierar komponenter i en mall till ett projekt finns det några saker du bör känna till.</span><span class="sxs-lookup"><span data-stu-id="11140-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="11140-127">**Kopiera en uppdelad arbetsstruktur** : När du kopierar den uppdelade arbetsstrukturen från en projektmall, om projektet har en annan projektkalender än mallen, används arbetstimmarna från projektets kalender i schemat över aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="11140-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="11140-128">Detta ändrar schemat till den säkerhetskopierade projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="11140-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="11140-129">På samma sätt tar den första uppgiften i den uppdelade arbetsstrukturen projektets startdatum, så att resten av hierarkischemat för uppgiften uppdateras baserat på varaktighet och beroenden som anges i mallen för uppdelad arbetsstruktur.</span><span class="sxs-lookup"><span data-stu-id="11140-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="11140-130">**Kopiera projektberäkningar** : När du kopierar över projektets beräkningsrader uppdateras prislistorna baserat på projektets ägande enhet för självkostnadslistan och kunden för försäljningslistan.</span><span class="sxs-lookup"><span data-stu-id="11140-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="11140-131">Enhetskostnaden och försäljningspriserna fastställs utifrån dessa prislistor på projekt som är kopplade till en försäljningsenhet.</span><span class="sxs-lookup"><span data-stu-id="11140-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="11140-132">**Kopiera ett projektteam** : När du kopierar ett projektteam från mallen till ett projekt kopieras de allmänna resurserna över tillsammans med de angivna färdigheterna och kompetenserna i mallen.</span><span class="sxs-lookup"><span data-stu-id="11140-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="11140-133">Allmänna resurstilldelningar hanteras också i projektmallen.</span><span class="sxs-lookup"><span data-stu-id="11140-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="11140-134">Se även</span><span class="sxs-lookup"><span data-stu-id="11140-134">See Also</span></span>  
 [<span data-ttu-id="11140-135">Guiden för projektledare</span><span class="sxs-lookup"><span data-stu-id="11140-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
