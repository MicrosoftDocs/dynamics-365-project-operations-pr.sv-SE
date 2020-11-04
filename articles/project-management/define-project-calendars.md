---
title: Definiera projektkalendrar
description: I det här ämnet finns information om hur du använder en projektkalender för att följa upp projektschemat.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085714"
---
# <a name="define-project-calendars"></a><span data-ttu-id="cd670-103">Definiera projektkalendrar</span><span class="sxs-lookup"><span data-stu-id="cd670-103">Define project calendars</span></span>

<span data-ttu-id="cd670-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="cd670-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cd670-105">För att skapa ett projektschema skapar du en projektkalendermall som definierar antalet arbetstimmar per dag och alla öppettider för företaget.</span><span class="sxs-lookup"><span data-stu-id="cd670-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="cd670-106">Om du vill skapa en projektkalendermall associerar du en arbetsmall med fältet **kalendermallen** för projektet.</span><span class="sxs-lookup"><span data-stu-id="cd670-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="cd670-107">Skapa en arbetsmall genom att följa stegen nedan.</span><span class="sxs-lookup"><span data-stu-id="cd670-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="cd670-108">I vänster navigeringsfönster, välj **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="cd670-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="cd670-109">På listsidan **Resurser** , öppna en användarpost och välj sedan **Visa arbetstimmar**.</span><span class="sxs-lookup"><span data-stu-id="cd670-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="cd670-110">Kontrollera att popup-fönster tillåts på webbsidan.</span><span class="sxs-lookup"><span data-stu-id="cd670-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="cd670-111">På så sätt kan du se resursens arbetstider.</span><span class="sxs-lookup"><span data-stu-id="cd670-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="cd670-112">På sidan **månatlig visning** , klicka på **konfigurera**.</span><span class="sxs-lookup"><span data-stu-id="cd670-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="cd670-113">En lista med tre alternativ visas:</span><span class="sxs-lookup"><span data-stu-id="cd670-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="cd670-114">Nytt veckoschema</span><span class="sxs-lookup"><span data-stu-id="cd670-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="cd670-115">Arbetsschema för en dag</span><span class="sxs-lookup"><span data-stu-id="cd670-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="cd670-116">Ledig tid</span><span class="sxs-lookup"><span data-stu-id="cd670-116">Time Off</span></span>

4. <span data-ttu-id="cd670-117">Välj **Nytt veckoschema** och ange alternativen för det här resursschemat.</span><span class="sxs-lookup"><span data-stu-id="cd670-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="cd670-118">Du kan ange ett återkommande veckoschema, dagliga timparametrar, företagets öppettider och mycket annat.</span><span class="sxs-lookup"><span data-stu-id="cd670-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="cd670-119">Ange datumintervall, välj **Spara** och klicka på **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="cd670-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="cd670-120">Gå tillbaka till listsidan **Resurser** och välj den resurs som du anger arbetstider för.</span><span class="sxs-lookup"><span data-stu-id="cd670-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="cd670-121">Välj **Ange kalender som** för att ställa in arbetsmallen.</span><span class="sxs-lookup"><span data-stu-id="cd670-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="cd670-122">I dialogrutan **Arbetsmall** anger du ett namn på arbetsmallen och klickar på **Använd**.</span><span class="sxs-lookup"><span data-stu-id="cd670-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="cd670-123">Du kan nu associera arbetsmallen med en projektkalendermall.</span><span class="sxs-lookup"><span data-stu-id="cd670-123">You can now associate the work template with a project calendar template.</span></span>
