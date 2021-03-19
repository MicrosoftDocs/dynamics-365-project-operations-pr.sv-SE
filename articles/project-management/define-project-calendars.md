---
title: Definiera projektkalendrar
description: I det här ämnet finns information om hur du använder en projektkalender för att följa upp projektschemat.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286990"
---
# <a name="define-project-calendars"></a><span data-ttu-id="b326a-103">Definiera projektkalendrar</span><span class="sxs-lookup"><span data-stu-id="b326a-103">Define project calendars</span></span>

<span data-ttu-id="b326a-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b326a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b326a-105">För att skapa ett projektschema skapar du en projektkalendermall som definierar antalet arbetstimmar per dag och alla öppettider för företaget.</span><span class="sxs-lookup"><span data-stu-id="b326a-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="b326a-106">Om du vill skapa en projektkalendermall associerar du en arbetsmall med fältet **kalendermallen** för projektet.</span><span class="sxs-lookup"><span data-stu-id="b326a-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="b326a-107">Skapa en arbetsmall genom att följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="b326a-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="b326a-108">I vänster navigeringsfönster, välj **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="b326a-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="b326a-109">På listsidan **Resurser**, öppna en användarpost och välj sedan **Visa arbetstimmar**.</span><span class="sxs-lookup"><span data-stu-id="b326a-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b326a-110">Kontrollera att popup-fönster tillåts på webbsidan.</span><span class="sxs-lookup"><span data-stu-id="b326a-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="b326a-111">På så sätt kan du se resursens arbetstider.</span><span class="sxs-lookup"><span data-stu-id="b326a-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="b326a-112">På sidan **månatlig visning**, klicka på **konfigurera**.</span><span class="sxs-lookup"><span data-stu-id="b326a-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="b326a-113">En lista med tre alternativ visas:</span><span class="sxs-lookup"><span data-stu-id="b326a-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="b326a-114">Nytt veckoschema</span><span class="sxs-lookup"><span data-stu-id="b326a-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="b326a-115">Arbetsschema för en dag</span><span class="sxs-lookup"><span data-stu-id="b326a-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="b326a-116">Ledig tid</span><span class="sxs-lookup"><span data-stu-id="b326a-116">Time Off</span></span>

4. <span data-ttu-id="b326a-117">Välj **Nytt veckoschema** och ange alternativen för det här resursschemat.</span><span class="sxs-lookup"><span data-stu-id="b326a-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="b326a-118">Du kan ange ett återkommande veckoschema, dagliga timparametrar, företagets öppettider och mycket annat.</span><span class="sxs-lookup"><span data-stu-id="b326a-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="b326a-119">Ange datumintervall, välj **Spara** och klicka på **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="b326a-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="b326a-120">Gå tillbaka till listsidan **Resurser** och välj den resurs som du anger arbetstider för.</span><span class="sxs-lookup"><span data-stu-id="b326a-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="b326a-121">Välj **Ange kalender som** för att ställa in arbetsmallen.</span><span class="sxs-lookup"><span data-stu-id="b326a-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="b326a-122">I dialogrutan **Arbetsmall** anger du ett namn på arbetsmallen och klickar på **Använd**.</span><span class="sxs-lookup"><span data-stu-id="b326a-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="b326a-123">Du kan nu associera arbetsmallen med en projektkalendermall.</span><span class="sxs-lookup"><span data-stu-id="b326a-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]