---
title: Konfigurera resursroller
description: Konfigurera resursroller i Project Service
author: JohnPBurrows
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
ms.openlocfilehash: deaff0977ebb50382a28494fba2a1c34ed5cc9b4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144930"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="ac09c-103">Konfigurera resursroller (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ac09c-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ac09c-104">Roller spelar en viktig roll i projektplaneringen, vid bestämning av resursbehov eller utgifterna för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="ac09c-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="ac09c-105">För varje roll projektet kräver måste du skapa en resursroll och associera färdigheter och kompetenser med den rollen.</span><span class="sxs-lookup"><span data-stu-id="ac09c-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="ac09c-106">Du kanske vill skapa exempelvis roller för utvecklare, projektledare eller speltestare.</span><span class="sxs-lookup"><span data-stu-id="ac09c-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="ac09c-107">Du ska också ange färdighets- och kompetensnivåer som krävs för rollen.</span><span class="sxs-lookup"><span data-stu-id="ac09c-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="ac09c-108">Konfigurera resursroller för att säkerställa effektiv projektuppskattning för din organisation.</span><span class="sxs-lookup"><span data-stu-id="ac09c-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="ac09c-109">Kontrollera också att du anger faktureringstypen exakt.</span><span class="sxs-lookup"><span data-stu-id="ac09c-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="ac09c-110">Ett objekt med en icke-debiterbar faktureringstyp visas inte på kontrakt eller offertrader.</span><span class="sxs-lookup"><span data-stu-id="ac09c-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="ac09c-111">När du har skapat resursroller kan du ställa in självkostnads- och försäljningspriser med en prislista.</span><span class="sxs-lookup"><span data-stu-id="ac09c-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="ac09c-112">Gör följande för varje roll som du vill lägga till:</span><span class="sxs-lookup"><span data-stu-id="ac09c-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="ac09c-113">Gå till **Project Service > Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="ac09c-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="ac09c-114">Klicka på **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="ac09c-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="ac09c-115">I området **Allmän** anger du ett namn för rollen i fältet **Namn** och fyller sedan i övriga fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="ac09c-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="ac09c-116">Klicka på **Spara** för att skapa posten så att du kan fortsätta redigera den.</span><span class="sxs-lookup"><span data-stu-id="ac09c-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="ac09c-117">I området **Färdigheter** klicka på **+** för att lägga till en färdighet.</span><span class="sxs-lookup"><span data-stu-id="ac09c-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="ac09c-118">I fönstret **Rollkompetenskrav** klickar du i fältet **Färdighet**, klickar på knappen **Sök** och väljer en färdighet.</span><span class="sxs-lookup"><span data-stu-id="ac09c-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="ac09c-119">Välj en kompetens för färdigheten och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="ac09c-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="ac09c-120">Fortsätt att lägga till färdigheter efter behov.</span><span class="sxs-lookup"><span data-stu-id="ac09c-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="ac09c-121">Klicka på **Spara** i skärmens nedre högra hörn när du är klar.</span><span class="sxs-lookup"><span data-stu-id="ac09c-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="ac09c-122">För att göra denna resursroll tillgänglig för projekt att använda, klicka på **Aktivera**.</span><span class="sxs-lookup"><span data-stu-id="ac09c-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ac09c-123">Se även</span><span class="sxs-lookup"><span data-stu-id="ac09c-123">See Also</span></span>  
 [<span data-ttu-id="ac09c-124">Konfigurera resurser</span><span class="sxs-lookup"><span data-stu-id="ac09c-124">Set up resources</span></span>](../psa/set-up-resources.md)
