---
title: Typer av projektstadier
description: I det här ämnet finns information om projektstadier.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148125"
---
# <a name="project-stage-types"></a><span data-ttu-id="f41c5-103">Typer av projektstadier</span><span class="sxs-lookup"><span data-stu-id="f41c5-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f41c5-104">Projektstadier designas för att återspegla projektets status allt eftersom det fortlöper.</span><span class="sxs-lookup"><span data-stu-id="f41c5-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="f41c5-105">Anpassningar kan användas för att automatiskt uppdatera stadier i flöden för affärsprocesser, Power Automate eller tillägg för plugin-program.</span><span class="sxs-lookup"><span data-stu-id="f41c5-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="f41c5-106">Följande stadier definieras i standardvärdet för BPF:</span><span class="sxs-lookup"><span data-stu-id="f41c5-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="f41c5-107">Skapa</span><span class="sxs-lookup"><span data-stu-id="f41c5-107">New</span></span>
- <span data-ttu-id="f41c5-108">Offert</span><span class="sxs-lookup"><span data-stu-id="f41c5-108">Quote</span></span>
- <span data-ttu-id="f41c5-109">Planera</span><span class="sxs-lookup"><span data-stu-id="f41c5-109">Plan</span></span>
- <span data-ttu-id="f41c5-110">Leverera</span><span class="sxs-lookup"><span data-stu-id="f41c5-110">Deliver</span></span>
- <span data-ttu-id="f41c5-111">Slutför</span><span class="sxs-lookup"><span data-stu-id="f41c5-111">Complete</span></span>
- <span data-ttu-id="f41c5-112">Stäng</span><span class="sxs-lookup"><span data-stu-id="f41c5-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="f41c5-113">Nytt</span><span class="sxs-lookup"><span data-stu-id="f41c5-113">New</span></span>

<span data-ttu-id="f41c5-114">När du skapar ett projekt anges projektstadiet till **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="f41c5-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="f41c5-115">Om projektet skapades från en mall kan det finnas schema-, uppskattnings- och teamdata.</span><span class="sxs-lookup"><span data-stu-id="f41c5-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="f41c5-116">I annat fall är det bara en disposition av projektet och resterande komponenter måste anges.</span><span class="sxs-lookup"><span data-stu-id="f41c5-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="f41c5-117">Offert</span><span class="sxs-lookup"><span data-stu-id="f41c5-117">Quote</span></span>

<span data-ttu-id="f41c5-118">När du associerar ett projekt med en offert eller när du skapar det från ett projekt från offert, anges projektstadiet som **Offert**, och de uppskattade start- och slutdatumen uppdateras.</span><span class="sxs-lookup"><span data-stu-id="f41c5-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="f41c5-119">När projektet är i stadiet **Offert** visas information om offerten på fliken **Försäljning** fliken på sidan **Projektentitet**.</span><span class="sxs-lookup"><span data-stu-id="f41c5-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="f41c5-120">Planera</span><span class="sxs-lookup"><span data-stu-id="f41c5-120">Plan</span></span>

<span data-ttu-id="f41c5-121">När du vinner en offert som är associerad med ett projekt och projekt flyttas till fasen **Kontrakt** uppdateras projektfasen till **Planera**.</span><span class="sxs-lookup"><span data-stu-id="f41c5-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="f41c5-122">När projektet är i stadiet **Planera** visas information om kontraktet på fliken **Projektentitet**.</span><span class="sxs-lookup"><span data-stu-id="f41c5-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="f41c5-123">Leverera</span><span class="sxs-lookup"><span data-stu-id="f41c5-123">Deliver</span></span>

<span data-ttu-id="f41c5-124">När projektplanen är klar och du är redo att starta projektet ska projektledaren uppdatera projektfasen till **Leverera** för att visar att projektet har påbörjats.</span><span class="sxs-lookup"><span data-stu-id="f41c5-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="f41c5-125">Slutför</span><span class="sxs-lookup"><span data-stu-id="f41c5-125">Complete</span></span> 

<span data-ttu-id="f41c5-126">När arbetet för projektet har slutförts kan projektledaren uppdatera fasen till att **slutföras**.</span><span class="sxs-lookup"><span data-stu-id="f41c5-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="f41c5-127">Om du uppdaterar projektfasen till **Slutföra** anger projektledaren att arbetet är 100 procent klart, men att projektet hålls öppet så att väntande tid- eller utgiftsposter kan registreras.</span><span class="sxs-lookup"><span data-stu-id="f41c5-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="f41c5-128">Stäng</span><span class="sxs-lookup"><span data-stu-id="f41c5-128">Close</span></span>

<span data-ttu-id="f41c5-129">När alla transaktioner har registreras kan projektledaren uppdatera fasen till att **Stäng**.</span><span class="sxs-lookup"><span data-stu-id="f41c5-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="f41c5-130">Vid den tidpunkten kan inga transaktioner registreras och projektet får värdet skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="f41c5-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
