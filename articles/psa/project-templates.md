---
title: Projektmallar
description: I det här ämnet finns information om hur du använder projektmallar för att snabbkonfigurera projekt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123058"
---
# <a name="project-templates"></a><span data-ttu-id="d6bf2-103">Projektmallar</span><span class="sxs-lookup"><span data-stu-id="d6bf2-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d6bf2-104">En projektmall är en fördefinierad ramverk som hjälper dig att snabbt och enkelt starta ett projekt.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="d6bf2-105">Du kan använda en fördefinierad mall för att skapa ett nytt projekt med en enkel klickning.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="d6bf2-106">Du måste liksom för projekt definiera förutsättningarna för projektmallar.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="d6bf2-107">Du måste definiera en projektkalender för varje projektmall och roller och prislistor måste vara fördefinierade i organisationen så att komponenterna i mallen har användbara data.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="d6bf2-108">En projektmall består av tre komponenter: ett schema, projektuppskattningar och projektteammedlemmar.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="d6bf2-109">Schemalägg</span><span class="sxs-lookup"><span data-stu-id="d6bf2-109">Schedule</span></span>

<span data-ttu-id="d6bf2-110">Ett schema i en projektmall har samma uppsättning element som ett schema i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="d6bf2-111">Du kan skapa en uppgiftshierarki, koppla roller till uppgifter, definiera attribut i scheman och ange beroenden.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="d6bf2-112">Ett schema i en projektmallen stöder även uppgiftslägen för varje uppgift.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="d6bf2-113">Därför stöder den schemaläggningsmotorn.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="d6bf2-114">Du måste associera en projektkalender med projektet.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="d6bf2-115">När du skapar ett arbetsschema är det ingen skillnad mellan en projektmall och ett projekt.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="d6bf2-116">Projektberäkningar</span><span class="sxs-lookup"><span data-stu-id="d6bf2-116">Project estimates</span></span>

<span data-ttu-id="d6bf2-117">Projektuppskattningar i projektmallen fungerar på samma sätt som projektuppskattningar i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="d6bf2-118">Kostnaden och försäljningspriset hämtas emellertid från standardkostnads- och försäljningsprislistorna som definieras i parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="d6bf2-119">Skapa ett projekt från en mall</span><span class="sxs-lookup"><span data-stu-id="d6bf2-119">Creating a project from a template</span></span>
 
<span data-ttu-id="d6bf2-120">Det finns flera sätt att skapa ett projekt från en projektmall:</span><span class="sxs-lookup"><span data-stu-id="d6bf2-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="d6bf2-121">När du skapar ett projekt från en offert kan du välja en projektmall i dialogrutan **Snabbregistrering: projekt**.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Snabbregistrering: dialogrutan Projekt](media/project-11.png)

- <span data-ttu-id="d6bf2-123">När du skapar ett projekt genom att välja **Nytt projekt**, visas sidan **Projekt** innan posten sparas.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="d6bf2-124">I fältet **Välj en mall** väljer du en av de fördefinierade projektmallarna i organisationen.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="d6bf2-125">Använd **Skapa projekt från en mall** på sidan **Mallentitet**.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="d6bf2-126">Kopiera komponenter av en mall till ett projekt</span><span class="sxs-lookup"><span data-stu-id="d6bf2-126">Copying components of template to project</span></span>

<span data-ttu-id="d6bf2-127">När du kopierar komponenterna i en projektmall till ett projekt kan det hända att en del åsidosättningar inträffar, beroende på inställningarna i projektet.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="d6bf2-128">Kopiera schemat</span><span class="sxs-lookup"><span data-stu-id="d6bf2-128">Copying the schedule</span></span>

<span data-ttu-id="d6bf2-129">När du kopierar schemat från en projektmall, om projektet har en annan projektkalender än mallen, används arbetstimmarna från projektets kalender i schemat över uppgiftsschemat.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="d6bf2-130">På så sätt justeras schemat till att matcha den säkerhetskopierade projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="d6bf2-131">På samma sätt tar den första uppgiften i schemat projektets startdatum och schemat för resten av hierarkin uppdateras baserat på varaktighet och beroenden som anges i mallen.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="d6bf2-132">Kopiera projektberäkningar</span><span class="sxs-lookup"><span data-stu-id="d6bf2-132">Copying project estimates</span></span> 

<span data-ttu-id="d6bf2-133">När du kopierar över beräkningsrader för projekt uppdateras prislistorna.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="d6bf2-134">För självkostnadslistan bygger uppdateringarna på projektets ägande enhet.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="d6bf2-135">För försäljningsprislistan bygger de på kunden.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="d6bf2-136">För projekt som är förknippade med en försäljningsentitet bestäms enhetskostnaden och försäljningspriserna baserat på dessa prislistor.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="d6bf2-137">Kopiera ett projektteam</span><span class="sxs-lookup"><span data-stu-id="d6bf2-137">Copying a project team</span></span>

<span data-ttu-id="d6bf2-138">När ett projektgrupp kopieras från en projektmall till ett projekt, kopieras de generiska resurserna tillsammans med de färdigheter och färdigheter som definieras i mallen.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="d6bf2-139">Allmänna resurstilldelningar hanteras också i projektmallen.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="d6bf2-140">Namngivna resurser stöds inte i projektmallar.</span><span class="sxs-lookup"><span data-stu-id="d6bf2-140">Named resources aren't supported in project templates.</span></span>
