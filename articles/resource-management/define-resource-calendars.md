---
title: Ange resurskalendrar
description: I det här ämnet finns information om hur du definierar arbetstidskalendrar för resurser i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279835"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="69bf4-103">Ange resurskalendrar</span><span class="sxs-lookup"><span data-stu-id="69bf4-103">Define resource calendars</span></span>

<span data-ttu-id="69bf4-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="69bf4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69bf4-105">Varje bokningsbar resurs som arbetar i ett projekt måste ha en kalender med arbetstid för att definiera deras tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="69bf4-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="69bf4-106">Arbetstider för en resurs kan definieras på två sätt:</span><span class="sxs-lookup"><span data-stu-id="69bf4-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="69bf4-107">Definiera enskilda kalenderregler för en resurs</span><span class="sxs-lookup"><span data-stu-id="69bf4-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="69bf4-108">Använda en befintlig kalendermall för resursen</span><span class="sxs-lookup"><span data-stu-id="69bf4-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="69bf4-109">Definiera arbetstider för en resurs</span><span class="sxs-lookup"><span data-stu-id="69bf4-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="69bf4-110">I menyn **Resurser** väljer du **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="69bf4-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="69bf4-111">Från rutnätsvyn väljer du tillämplig **bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="69bf4-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="69bf4-112">På sidan **Resursinformation** väljer du fliken **Arbetstider**. Som standard använder kalendern för bokningsbara resurser arbetstiderna från mallen med normala arbetstider som definierats för organisationen.</span><span class="sxs-lookup"><span data-stu-id="69bf4-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="69bf4-113">Om du vill uppdatera arbetstiderna högerklickar du på startdatumet för den föreslagna kalenderregeln som ska definieras.</span><span class="sxs-lookup"><span data-stu-id="69bf4-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="69bf4-114">Använd menyn Kalenderregel om du vill definiera en kalenderregel för en specifik dag, återstoden av serien eller hela kalendern.</span><span class="sxs-lookup"><span data-stu-id="69bf4-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="69bf4-115">När du har valt alternativet kan du definiera:</span><span class="sxs-lookup"><span data-stu-id="69bf4-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="69bf4-116">Den veckodag då arbetstiderna ska gälla.</span><span class="sxs-lookup"><span data-stu-id="69bf4-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="69bf4-117">Arbetstiderna för varje dag.</span><span class="sxs-lookup"><span data-stu-id="69bf4-117">The working times within each day.</span></span>
    - <span data-ttu-id="69bf4-118">Tidszonen för kalenderregeln.</span><span class="sxs-lookup"><span data-stu-id="69bf4-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="69bf4-119">I tillämpliga fall kan du även ange ledig tid för regeln.</span><span class="sxs-lookup"><span data-stu-id="69bf4-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="69bf4-120">Tillämpa en kalendermall på en resurs</span><span class="sxs-lookup"><span data-stu-id="69bf4-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="69bf4-121">I menyn **Resurser** väljer du **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="69bf4-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="69bf4-122">Välj upp till 25 **bokningsbara resurser** som ska uppdateras från rutnätsvyn.</span><span class="sxs-lookup"><span data-stu-id="69bf4-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="69bf4-123">Välj **Ange kalender** så visas en dialogruta med en lista över tillgängliga arbetstidsmallar.</span><span class="sxs-lookup"><span data-stu-id="69bf4-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="69bf4-124">Välj mallen du vill använda och välj sedan **Tillämpa**.</span><span class="sxs-lookup"><span data-stu-id="69bf4-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]