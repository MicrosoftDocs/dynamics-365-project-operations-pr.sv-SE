---
title: Definiera projektkalendrar
description: Ämnet innehåller information om hur du använder en kalendermall på ett projekt för att följa upp projektschemat.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999018"
---
# <a name="define-project-calendars"></a><span data-ttu-id="951c5-103">Definiera projektkalendrar</span><span class="sxs-lookup"><span data-stu-id="951c5-103">Define project calendars</span></span>

<span data-ttu-id="951c5-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="951c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="951c5-105">För att skapa och hantera ett projekt måste du använda en kalendermall för projektet.</span><span class="sxs-lookup"><span data-stu-id="951c5-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="951c5-106">Kalendermallen definierar följande projektattribut:</span><span class="sxs-lookup"><span data-stu-id="951c5-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="951c5-107">Arbetstider, inklusive start- och sluttid</span><span class="sxs-lookup"><span data-stu-id="951c5-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="951c5-108">Arbetsdagar</span><span class="sxs-lookup"><span data-stu-id="951c5-108">Working days</span></span>
- <span data-ttu-id="951c5-109">Kalenderundantag, som lediga dagar</span><span class="sxs-lookup"><span data-stu-id="951c5-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="951c5-110">Kalendermallen som används för ett projekt är en kopia av kalendermallen som har definierats i organisationens inställningar.</span><span class="sxs-lookup"><span data-stu-id="951c5-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="951c5-111">Om du ändrar kalendermallen överförs inte ändringarna till projektets arbetstider.</span><span class="sxs-lookup"><span data-stu-id="951c5-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="951c5-112">För att ändra projektets arbetstider måste en ny mall användas.</span><span class="sxs-lookup"><span data-stu-id="951c5-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="951c5-113">Det finns två viktiga krav om du vill skapa en kalendermall för organisationen:</span><span class="sxs-lookup"><span data-stu-id="951c5-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="951c5-114">Ange mallens önskade arbetstider med hjälp av en ny eller befintlig bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="951c5-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="951c5-115">Skapa en ny kalendermall och associera mallen med den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="951c5-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="951c5-116">**Definiera arbetstider i mallen**</span><span class="sxs-lookup"><span data-stu-id="951c5-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="951c5-117">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="951c5-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="951c5-118">Skapa en ny resurs att referera till i kalendermallen eller välj en befintlig resurs.</span><span class="sxs-lookup"><span data-stu-id="951c5-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="951c5-119">Välj resursens flik **Arbetstider** och följ instruktionerna i [Ange arbetstider för en resurs](/dynamics365/field-service/set-work-hours-resource.md) för att konfigurera kalenderreglerna.</span><span class="sxs-lookup"><span data-stu-id="951c5-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="951c5-120">**Skapa en ny kalendermall**</span><span class="sxs-lookup"><span data-stu-id="951c5-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="951c5-121">Gå till **Inställningar** \> **Kalendermall**.</span><span class="sxs-lookup"><span data-stu-id="951c5-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="951c5-122">Välj **Ny** och ange namn, beskrivning och mallresurs.</span><span class="sxs-lookup"><span data-stu-id="951c5-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="951c5-123">När en resurs refereras till i en kalendermall associeras en kopia av resursens kalender med kalendermallen.</span><span class="sxs-lookup"><span data-stu-id="951c5-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="951c5-124">Om du ändrar arbetstider i den kopierade mallen överförs inte ändringarna till kalendermallen.</span><span class="sxs-lookup"><span data-stu-id="951c5-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="951c5-125">Du kan nu associera arbetsmallen med en projektkalendermall.</span><span class="sxs-lookup"><span data-stu-id="951c5-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

