---
title: Skapa en ny mall för arbetstid
description: Ämnet beskriver hur du skapar en mall för arbetstid i Project Service.
author: ruhercul
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997218"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="e0daa-103">Skapa en mall för arbetstid (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e0daa-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e0daa-104">För att skapa och hantera ett projekt måste du använda en kalendermall för projektet.</span><span class="sxs-lookup"><span data-stu-id="e0daa-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="e0daa-105">Kalendermallen definierar följande projektattribut:</span><span class="sxs-lookup"><span data-stu-id="e0daa-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="e0daa-106">Arbetstider, inklusive start- och sluttid</span><span class="sxs-lookup"><span data-stu-id="e0daa-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="e0daa-107">Arbetsdagar</span><span class="sxs-lookup"><span data-stu-id="e0daa-107">Working days</span></span>
- <span data-ttu-id="e0daa-108">Kalenderundantag, som lediga dagar</span><span class="sxs-lookup"><span data-stu-id="e0daa-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="e0daa-109">Kalendermallen som används för ett projekt är en kopia av kalendermallen som har definierats i organisationens inställningar.</span><span class="sxs-lookup"><span data-stu-id="e0daa-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="e0daa-110">Om du ändrar kalendermallen överförs inte ändringarna till projektets arbetstider.</span><span class="sxs-lookup"><span data-stu-id="e0daa-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="e0daa-111">För att ändra projektets arbetstider måste en ny mall användas.</span><span class="sxs-lookup"><span data-stu-id="e0daa-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="e0daa-112">Det finns två viktiga krav om du vill skapa en kalendermall för organisationen:</span><span class="sxs-lookup"><span data-stu-id="e0daa-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="e0daa-113">Ange mallens önskade arbetstider med hjälp av en ny eller befintlig bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="e0daa-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="e0daa-114">Skapa en ny kalendermall och associera mallen med den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="e0daa-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="e0daa-115">**Definiera arbetstider i mallen**</span><span class="sxs-lookup"><span data-stu-id="e0daa-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="e0daa-116">Gå till **Resurser** \> **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="e0daa-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="e0daa-117">Skapa en ny resurs att referera till i kalendermallen eller välj en befintlig resurs.</span><span class="sxs-lookup"><span data-stu-id="e0daa-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="e0daa-118">Välj resursens flik **Arbetstider** och följ instruktionerna i [Ange arbetstider för en resurs](/dynamics365/field-service/set-work-hours-resource.md) för att konfigurera kalenderreglerna.</span><span class="sxs-lookup"><span data-stu-id="e0daa-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="e0daa-119">**Skapa en ny kalendermall**</span><span class="sxs-lookup"><span data-stu-id="e0daa-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="e0daa-120">Gå till **Inställningar** \> **Kalendermall**.</span><span class="sxs-lookup"><span data-stu-id="e0daa-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="e0daa-121">Välj **Ny** och ange namn, beskrivning och mallresurs.</span><span class="sxs-lookup"><span data-stu-id="e0daa-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="e0daa-122">När en resurs refereras till i en kalendermall associeras en kopia av resursens kalender med kalendermallen.</span><span class="sxs-lookup"><span data-stu-id="e0daa-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="e0daa-123">Om du ändrar arbetstider i den kopierade mallen överförs inte ändringarna till kalendermallen.</span><span class="sxs-lookup"><span data-stu-id="e0daa-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="e0daa-124">Se även</span><span class="sxs-lookup"><span data-stu-id="e0daa-124">See Also</span></span>  
 [<span data-ttu-id="e0daa-125">Konfigurera resurser</span><span class="sxs-lookup"><span data-stu-id="e0daa-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
