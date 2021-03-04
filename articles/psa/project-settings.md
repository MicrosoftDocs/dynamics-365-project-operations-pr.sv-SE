---
title: Projektinställningar
description: I det här ämnet finns information om inställningar för projekthantering.
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148170"
---
# <a name="project-settings"></a><span data-ttu-id="e2660-103">Projektinställningar</span><span class="sxs-lookup"><span data-stu-id="e2660-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e2660-104">Använd följande inställningar för att komma åt funktionerna för projektplanering.</span><span class="sxs-lookup"><span data-stu-id="e2660-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="e2660-105">Arbetsmall</span><span class="sxs-lookup"><span data-stu-id="e2660-105">Work template</span></span>

<span data-ttu-id="e2660-106">För att skapa ett projektschema skapar du en projektkalendermall som definierar antalet arbetstimmar per dag och alla öppettider för företaget.</span><span class="sxs-lookup"><span data-stu-id="e2660-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="e2660-107">Om du vill skapa en projektkalendermall associerar du en arbetsmall med fältet **kalendermallen** för projektet.</span><span class="sxs-lookup"><span data-stu-id="e2660-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="e2660-108">Skapa en arbetsmall genom att följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="e2660-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="e2660-109">I PSA, i vänster navigationsfönster, klicka på **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="e2660-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="e2660-110">På listsidan **Resurser**, öppna en användarpost och välj sedan **Visa arbetstimmar**.</span><span class="sxs-lookup"><span data-stu-id="e2660-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="e2660-111">Kontrollera att popup-fönster tillåts på webbsidan.</span><span class="sxs-lookup"><span data-stu-id="e2660-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="e2660-112">På så sätt kan du se resursens arbetstider.</span><span class="sxs-lookup"><span data-stu-id="e2660-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="e2660-113">På sidan **månatlig visning**, klicka på **konfigurera**.</span><span class="sxs-lookup"><span data-stu-id="e2660-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="e2660-114">En lista med tre alternativ visas:</span><span class="sxs-lookup"><span data-stu-id="e2660-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="e2660-115">Nytt veckoschema</span><span class="sxs-lookup"><span data-stu-id="e2660-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="e2660-116">Arbetsschema för en dag</span><span class="sxs-lookup"><span data-stu-id="e2660-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="e2660-117">Ledig tid</span><span class="sxs-lookup"><span data-stu-id="e2660-117">Time Off</span></span>

> ![Ange alternativ](media/project-13.png)

4. <span data-ttu-id="e2660-119">Välj **Nytt veckoschema** och ange alternativen för det här resursschemat.</span><span class="sxs-lookup"><span data-stu-id="e2660-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="e2660-120">Du kan ange ett återkommande veckoschema, dagliga timparametrar, företagets öppettider och mycket annat.</span><span class="sxs-lookup"><span data-stu-id="e2660-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="e2660-121">Ange datumintervall, välj **Spara** och klicka på **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="e2660-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="e2660-122">Gå tillbaka till listsidan **Resurser** och välj den resurs som du anger arbetstider för.</span><span class="sxs-lookup"><span data-stu-id="e2660-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="e2660-123">Välj **Ange kalender som** för att ställa in arbetsmallen.</span><span class="sxs-lookup"><span data-stu-id="e2660-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="e2660-124">I dialogrutan **Arbetsmall** anger du ett namn på arbetsmallen och klickar på **Använd**.</span><span class="sxs-lookup"><span data-stu-id="e2660-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="e2660-125">Du kan nu associera arbetsmallen med en projektkalendermall.</span><span class="sxs-lookup"><span data-stu-id="e2660-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="e2660-126">Resursroller</span><span class="sxs-lookup"><span data-stu-id="e2660-126">Resource roles</span></span>

<span data-ttu-id="e2660-127">Termen *resursroller* refererar till den uppsättning färdigheter, kompetenser och certifieringar som en person måste ha för att utföra en specifik uppsättning uppgifter i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="e2660-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="e2660-128">Med hjälp av PSA kan du ange kostnaden och fakturera en resurs tid utifrån den roll som resursen är associerad med.</span><span class="sxs-lookup"><span data-stu-id="e2660-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="e2660-129">Varje organisation måste konfigurera de här rollerna med hjälp av den vänstra navigeringen på menyn **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="e2660-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="e2660-130">Varje organisation måste skapa de här rollerna på sidan **Aktiva resurskategorier**.</span><span class="sxs-lookup"><span data-stu-id="e2660-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="e2660-131">Om du vill öppna den här sidan markerar du **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="e2660-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="e2660-132">Prislistor</span><span class="sxs-lookup"><span data-stu-id="e2660-132">Price lists</span></span>

<span data-ttu-id="e2660-133">Prislistor låter dig ställa in självkostnads- och försäljningspriser, utgiftskategorier, produkter och andra element i en organisation.</span><span class="sxs-lookup"><span data-stu-id="e2660-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="e2660-134">Innan du anger ekonomiska uppskattningar för arbetet som måste levereras för ett projekt måste du skapa en bakomliggande utgifts- och prislista.</span><span class="sxs-lookup"><span data-stu-id="e2660-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="e2660-135">I avsnittet parametrar bör du även ange en standardkostnads- och försäljningsprislista som gäller alla projekt som skapas i organisationen.</span><span class="sxs-lookup"><span data-stu-id="e2660-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="e2660-136">På sidan **Aktiva projektparametrar** ser du till att du anger en standardkostnads- och försäljningsprislista.</span><span class="sxs-lookup"><span data-stu-id="e2660-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
