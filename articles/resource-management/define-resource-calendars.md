---
title: Ange resurskalendrar
description: I det här ämnet finns information om hur du definierar arbetstidskalendrar för resurser i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961956"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="ddef3-103">Ange resurskalendrar</span><span class="sxs-lookup"><span data-stu-id="ddef3-103">Define resource calendars</span></span>

<span data-ttu-id="ddef3-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="ddef3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ddef3-105">Varje bokningsbar resurs som arbetar i ett projekt måste ha en kalender med arbetstid för att definiera deras tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="ddef3-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="ddef3-106">Arbetstider för en resurs kan definieras på två sätt:</span><span class="sxs-lookup"><span data-stu-id="ddef3-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="ddef3-107">Definiera enskilda kalenderregler för en resurs</span><span class="sxs-lookup"><span data-stu-id="ddef3-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="ddef3-108">Använda en befintlig kalendermall för resursen</span><span class="sxs-lookup"><span data-stu-id="ddef3-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="ddef3-109">Definiera arbetstider för en resurs</span><span class="sxs-lookup"><span data-stu-id="ddef3-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="ddef3-110">I menyn **Resurser** väljer du **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="ddef3-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ddef3-111">Från rutnätsvyn väljer du tillämplig **bokningsbar resurs**.</span><span class="sxs-lookup"><span data-stu-id="ddef3-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="ddef3-112">På sidan **Resursinformation** väljer du fliken **Arbetstider**. Som standard använder kalendern för bokningsbara resurser arbetstiderna från mallen med normala arbetstider som definierats för organisationen.</span><span class="sxs-lookup"><span data-stu-id="ddef3-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="ddef3-113">Om du vill uppdatera arbetstiderna högerklickar du på startdatumet för den föreslagna kalenderregeln som ska definieras.</span><span class="sxs-lookup"><span data-stu-id="ddef3-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="ddef3-114">Använd menyn Kalenderregel om du vill definiera en kalenderregel för en specifik dag, återstoden av serien eller hela kalendern.</span><span class="sxs-lookup"><span data-stu-id="ddef3-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="ddef3-115">När du har valt alternativet kan du definiera:</span><span class="sxs-lookup"><span data-stu-id="ddef3-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="ddef3-116">Den veckodag då arbetstiderna ska gälla.</span><span class="sxs-lookup"><span data-stu-id="ddef3-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="ddef3-117">Arbetstiderna för varje dag.</span><span class="sxs-lookup"><span data-stu-id="ddef3-117">The working times within each day.</span></span>
    - <span data-ttu-id="ddef3-118">Tidszonen för kalenderregeln.</span><span class="sxs-lookup"><span data-stu-id="ddef3-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="ddef3-119">I tillämpliga fall kan du även ange ledig tid för regeln.</span><span class="sxs-lookup"><span data-stu-id="ddef3-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="ddef3-120">Tillämpa en kalendermall på en resurs</span><span class="sxs-lookup"><span data-stu-id="ddef3-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="ddef3-121">I menyn **Resurser** väljer du **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="ddef3-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ddef3-122">Välj upp till 25 **bokningsbara resurser** som ska uppdateras från rutnätsvyn.</span><span class="sxs-lookup"><span data-stu-id="ddef3-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="ddef3-123">Välj **Ange kalender** så visas en dialogruta med en lista över tillgängliga arbetstidsmallar.</span><span class="sxs-lookup"><span data-stu-id="ddef3-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="ddef3-124">Välj mallen du vill använda och välj sedan **Tillämpa**.</span><span class="sxs-lookup"><span data-stu-id="ddef3-124">Select the template you want to use, and then select **Apply**.</span></span>
