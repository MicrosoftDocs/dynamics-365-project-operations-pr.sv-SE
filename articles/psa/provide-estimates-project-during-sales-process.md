---
title: Tillhandahålla uppskattningar av arbete för ett projekt under försäljningsprocessen
description: Tillhandahålla arbetsuppskattningar för ett projekt under säljprocessen i Project Service
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120610"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="ae0f5-103">Tillhandahålla uppskattningar av arbete för ett projekt under försäljningsprocessen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ae0f5-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ae0f5-104">Under försäljningsprocessen, kan du använda offertrader för ta fram försäljningsuppskattningar från början.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="ae0f5-105">-funktioner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ger ett mer vetenskapligt och deterministiskt sätt att skapa säljuppskattningar, detta genom att bryta ned arbetsuppgifter och associera relevanta attribut som bidrar till projektuppskattningarna i den uppdelade arbetsstrukturen för arbetsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="ae0f5-106">När du vinner försäljningen kan du använda den associerade uppdelade arbetsstrukturen i projektplanen, och förfina den efter behov för slutförande av projektet.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="ae0f5-107">Länka ett projekt till en offertrad</span><span class="sxs-lookup"><span data-stu-id="ae0f5-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="ae0f5-108">När du skapar en projektbaserad offertrad kan skapa du ett nytt projekt från offertraden.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="ae0f5-109">Du kan sedan använda projektmallar som är antingen förkonfigurerade standardprojektplaner och ekonomiska uppskattningar som är gemensamma för din organisation, eller en kopia av en projektplan och uppskattningar från tidigare projekt.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="ae0f5-110">När skapar ett projekt och väljer en projektmall ger det en grund för att förfina projektplan, uppskattningar och rollkrav.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="ae0f5-111">Genom att skapa ett projekt från offerten associeras projektet automatiskt med på offertraden.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="ae0f5-112">Komponenter för uppskattning av projekt</span><span class="sxs-lookup"><span data-stu-id="ae0f5-112">Project estimate components</span></span>  
 <span data-ttu-id="ae0f5-113">Den uppdelade arbetsstrukturen i ett projekt är ett sätt att bryta ned arbete i uppgifter, upprätthålla en hierarki av uppgifter och tilldela en uppskattning av vilken insats som krävs för att slutföra varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="ae0f5-114">Du kan också koppla roller till en uppgift för att visa en uppskattning av vilken typ av resurs som krävs för att slutföra en uppgift och ett schema.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="ae0f5-115">Den uppdelade arbetsstrukturen hjälper dig att fastställa uppskattningar av arbetsinsats och schema.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="ae0f5-116">Som standard använder projektet standardprislistan som du definierade tidigare.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="ae0f5-117">Kostnads- och försäljningspriserna som är definierade i prislistorna hjälper till att fastställa ekonomiska uppskattningar för uppdelning av projektets arbete.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="ae0f5-118">Om projektet är kopplat till en offert och offerten har en annan prislista som standard, används offertens prislista för ekonomiska beräkningar.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="ae0f5-119">Importera uppskattningar från ett projekt till en offert</span><span class="sxs-lookup"><span data-stu-id="ae0f5-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="ae0f5-120">När du har projektuppskattningar i projektet kan importera du dessa uppskattningar till offertraden:</span><span class="sxs-lookup"><span data-stu-id="ae0f5-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="ae0f5-121">I **Information om offertrad** klickar du på **Importera från beräkning**.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="ae0f5-122">Välj om du vill importera projektberäkningar sammanfattade efter nodnivån transaktionstyp, roll eller uppdelad arbetsstruktur.</span><span class="sxs-lookup"><span data-stu-id="ae0f5-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ae0f5-123">Se även</span><span class="sxs-lookup"><span data-stu-id="ae0f5-123">See Also</span></span>  
 [<span data-ttu-id="ae0f5-124">Guiden för projektledare</span><span class="sxs-lookup"><span data-stu-id="ae0f5-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
