---
title: Skapa en anpassad lösning för prissättningsdimensioner
description: I det här ämnet beskrivs hur du skapar en anpassad lösning när du skapar anpassade prisdimensioner.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285010"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="f5d04-103">Skapa en anpassad lösning för prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="f5d04-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="f5d04-104">Alla anpassningar av ändringar i prisdimension ska vara i en separat lösning.</span><span class="sxs-lookup"><span data-stu-id="f5d04-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="f5d04-105">Med den här viktiga rekommenderade metod som passar för att uppdatera eller ta bort ändringar efter behov, får du hjälp med att återanvända arbetet, och det gör det lättare att överföra ändringarna till en annan instans.</span><span class="sxs-lookup"><span data-stu-id="f5d04-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="f5d04-106">När du gör nödvändiga ändringar exporterar du lösningen som en **hanterad lösning** och importerar den till andra instanser för att återanvända prissättningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="f5d04-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="f5d04-107">Välj **Inställningar** > **Lösningar** och välj sedan **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f5d04-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="f5d04-108">Ge lösningen ett namn, **\<your organization name> prissättningsdimensioner**, ange den information som krävs och klicka sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="f5d04-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Skapa en anpassad lösning för prissättningsdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f5d04-110">Lägg till alla obligatoriska entiteter och relaterade komponenter i prisdimensionslösningen</span><span class="sxs-lookup"><span data-stu-id="f5d04-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="f5d04-111">Du måste lägga till följande Project Service-entiteter i din prissättningslösning.</span><span class="sxs-lookup"><span data-stu-id="f5d04-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="f5d04-112">Slutför stegen i den här proceduren för att göra vissa viktiga schemaändringar i prissättningslösningen så att enheterna blir medvetna om de nya prissättningsdimensionerna.</span><span class="sxs-lookup"><span data-stu-id="f5d04-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="f5d04-113">Välj **inställningar** > **lösningar** och dubbelklickar på **\<your organization name> prissättningsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="f5d04-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f5d04-114">I lösningsutforskaren på den vänstra navigeringsrutan väljer du **Lägg till befintliga** > **Entiteter**.</span><span class="sxs-lookup"><span data-stu-id="f5d04-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="f5d04-115">I dialogrutan **lösningskomponenter** markerar du följande entiteter:</span><span class="sxs-lookup"><span data-stu-id="f5d04-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="f5d04-116">Faktisk</span><span class="sxs-lookup"><span data-stu-id="f5d04-116">Actual</span></span>
- <span data-ttu-id="f5d04-117">Bokningsbar resurs</span><span class="sxs-lookup"><span data-stu-id="f5d04-117">Bookable Resource</span></span>
- <span data-ttu-id="f5d04-118">Beräkningsrad</span><span class="sxs-lookup"><span data-stu-id="f5d04-118">Estimate Line</span></span>
- <span data-ttu-id="f5d04-119">Projektuppgift</span><span class="sxs-lookup"><span data-stu-id="f5d04-119">Project Task</span></span>
- <span data-ttu-id="f5d04-120">Information om fakturarad</span><span class="sxs-lookup"><span data-stu-id="f5d04-120">Invoice Line Detail</span></span>
- <span data-ttu-id="f5d04-121">Journalrad</span><span class="sxs-lookup"><span data-stu-id="f5d04-121">Journal Line</span></span>
- <span data-ttu-id="f5d04-122">Information om projektkontraktrad</span><span class="sxs-lookup"><span data-stu-id="f5d04-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="f5d04-123">Projektteammedlem</span><span class="sxs-lookup"><span data-stu-id="f5d04-123">Project Team Member</span></span>
- <span data-ttu-id="f5d04-124">Information om offertrad</span><span class="sxs-lookup"><span data-stu-id="f5d04-124">Quote Line Detail</span></span>
- <span data-ttu-id="f5d04-125">Pålägg för rollpris</span><span class="sxs-lookup"><span data-stu-id="f5d04-125">Role Price Markup</span></span>
- <span data-ttu-id="f5d04-126">Pris för roll</span><span class="sxs-lookup"><span data-stu-id="f5d04-126">Role Price</span></span> 
- <span data-ttu-id="f5d04-127">Tidspost</span><span class="sxs-lookup"><span data-stu-id="f5d04-127">Time Entry</span></span> 

> ![Lägg till befintliga entiteter i lösningen för prissättningsdimensioner](media/Existing-entities-to-PD-solution.png)

> ![Välj lösningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="f5d04-130">Se till att du tar med alla formulär och vyer för varje vald entitet.</span><span class="sxs-lookup"><span data-stu-id="f5d04-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="f5d04-131">Klicka på **Nej** om du uppmanas att ta med alla beroende entiteter för de valda entiteterna.</span><span class="sxs-lookup"><span data-stu-id="f5d04-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Inkludera inte alla relaterade komponenter](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]