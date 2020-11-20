---
title: Försäljningsberäkningar och projekt
description: I det här ämnet finns information om hur du kan dra nytta av schemat och uppskattningarna i försäljningsprocessen.
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120700"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="49739-103">Försäljningsberäkningar och projekt</span><span class="sxs-lookup"><span data-stu-id="49739-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="49739-104">Under försäljningsprocessen kan du skapa försäljningsuppskattningar genom att länka ett projekt till en försäljningsoffert.</span><span class="sxs-lookup"><span data-stu-id="49739-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="49739-105">På det här sättet kan deterministisk uppskattning genomföras under försäljningsprocessen, för att dra nytta av funktionerna för projektplanering och uppskattning.</span><span class="sxs-lookup"><span data-stu-id="49739-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="49739-106">Om försäljningen går igenom kan den användas som bas för att använda schemat för försäljningsuppskattningen som grund för ytterligare förfining av projektplanen.</span><span class="sxs-lookup"><span data-stu-id="49739-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="49739-107">Länka ett projekt till en offertrad</span><span class="sxs-lookup"><span data-stu-id="49739-107">Linking a project to a quote line</span></span>

<span data-ttu-id="49739-108">När du skapar en projektbaserad offertrad kan du skapa ett nytt projekt eller associera ett befintligt projekt med sidan **offertrad**.</span><span class="sxs-lookup"><span data-stu-id="49739-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Offertradsformulär](media/project-8.png)
 
<span data-ttu-id="49739-110">När du skapar ett nytt projekt från offertradsinformationen kan du dra nytta av projektmallar.</span><span class="sxs-lookup"><span data-stu-id="49739-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="49739-111">Projektmallar är modellprojekt som representerar vanliga projektplaner och ekonomiska uppskattningar som är typiska i en organisation.</span><span class="sxs-lookup"><span data-stu-id="49739-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="49739-112">De kan också representera kopior av projektplaner och uppskattningar från tidigare projekt.</span><span class="sxs-lookup"><span data-stu-id="49739-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Information om offertrad](media/project-9.png)
  
<span data-ttu-id="49739-114">När du skapar projektet från offerten associeras projektet automatiskt med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="49739-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="49739-115">Komponenter i uppskattningar i ett projekt</span><span class="sxs-lookup"><span data-stu-id="49739-115">Components of estimates in a project</span></span>

<span data-ttu-id="49739-116">Med ett schema kan du dela upp arbete i uppgifter, underhålla en hierarki med uppgifter, avgöra vilka resurser som krävs för att slutföra en uppgift och tilldela en uppskattning av vilken insats som krävs för att slutföra en uppgift.</span><span class="sxs-lookup"><span data-stu-id="49739-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="49739-117">Du kan ange arbetsinsats och schemauppskattningar med hjälp av fälten på fliken **schema** på sidan **projekt**.</span><span class="sxs-lookup"><span data-stu-id="49739-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="49739-118">Eftersom en prislista associeras med projektet beräknas ekonomiska uppskattningar med hjälp av självkostnads- och försäljningspriser som definieras i prislistan.</span><span class="sxs-lookup"><span data-stu-id="49739-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="49739-119">Importera uppskattningar från ett projekt till en offert</span><span class="sxs-lookup"><span data-stu-id="49739-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="49739-120">När du har definierat projektuppskattningar kan du importera dem till offertraden.</span><span class="sxs-lookup"><span data-stu-id="49739-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="49739-121">På sidan **Information om offertrad**, välj **Importera från uppskattningar** i menyfliksområdet för att sammanfatta projektuppskattningar efter transaktionstyp, roll eller aktivitetsnivå.</span><span class="sxs-lookup"><span data-stu-id="49739-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
