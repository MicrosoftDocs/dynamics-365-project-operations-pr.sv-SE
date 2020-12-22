---
title: Kostnad för slutförandemetoder
description: Detta ämne innehåller information om de metoder som används för att beräkna kostnaden för att slutföra ett projekt.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531568"
---
# <a name="cost-to-complete-methods"></a><span data-ttu-id="a21b0-103">Kostnad för slutförandemetoder</span><span class="sxs-lookup"><span data-stu-id="a21b0-103">Cost to complete methods</span></span>

<span data-ttu-id="a21b0-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="a21b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a21b0-105">Detta ämne innehåller information om de metoder som används för att beräkna kostnaden för att slutföra ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a21b0-105">This topic provides information about the methods used to calculate the cost to complete a project.</span></span> <span data-ttu-id="a21b0-106">Det finns flera metoder som du kan använda för att beräkna kostnaden för att slutföra ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a21b0-106">There are multiple methods you can use to calculate the cost to complete a project.</span></span> 

<span data-ttu-id="a21b0-107">När du skapar en uppskattning för ett projekt kan du på sidan **Skapa uppskattning**, i fältet **Kostnad för att slutföra metod**, välja någon av följande kostnader för att slutföra metoder.</span><span class="sxs-lookup"><span data-stu-id="a21b0-107">When you create an estimate for a project, on the **Create estimate** page, in the **Cost to complete method** field, you can select one of the following cost to complete methods.</span></span>

| <span data-ttu-id="a21b0-108">Kostnad för att slutföra metod</span><span class="sxs-lookup"><span data-stu-id="a21b0-108">Cost to complete method</span></span>    | <span data-ttu-id="a21b0-109">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a21b0-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21b0-110">Total kostnad – faktisk</span><span class="sxs-lookup"><span data-stu-id="a21b0-110">Total cost-actual</span></span>            | <span data-ttu-id="a21b0-111">Ange uppskattningskostnader manuellt i fälten **Totalkostnad** eller **Total kvantitet** med hjälp av knappen **Kostnadsuppskattning** på **sidan Uppskattning**.</span><span class="sxs-lookup"><span data-stu-id="a21b0-111">Enter estimate costs manually in the **Total cost** or **Total quantity** fields using the **Cost estimate** button on the **Estimate page**.</span></span> <span data-ttu-id="a21b0-112">Systemet subtraherar de faktiska kostnaderna från de summor du angett.</span><span class="sxs-lookup"><span data-stu-id="a21b0-112">The system subtracts the actual costs from the totals you entered.</span></span> <span data-ttu-id="a21b0-113">Summan är kostnaden för att slutföra projektet.</span><span class="sxs-lookup"><span data-stu-id="a21b0-113">The total is the cost to complete the project.</span></span> <span data-ttu-id="a21b0-114">Den här metoden använder inte utgiftsuppskattningar och resurstilldelningar som angetts i Project Operations som skapats i Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a21b0-114">This method doesn't use the expense estimates and resources assignments entered in Project Operations built within Microsoft Dataverse.</span></span> <span data-ttu-id="a21b0-115">Den totala kostnaden eller den totala kvantiteten kan uppdateras manuellt efter behov.</span><span class="sxs-lookup"><span data-stu-id="a21b0-115">The total cost or total quantity can be updated manually as needed.</span></span>  |
| <span data-ttu-id="a21b0-116">Total faktisk prognos</span><span class="sxs-lookup"><span data-stu-id="a21b0-116">Total forecast-actual</span></span>        | <span data-ttu-id="a21b0-117">Resurstilldelningar och utgiftsuppskattningar används för att fastställa det totala projektprognosbeloppet.</span><span class="sxs-lookup"><span data-stu-id="a21b0-117">Resource assignments and expense estimates are used to determine the total project forecast amount.</span></span> <span data-ttu-id="a21b0-118">Faktiska kostnader jämförs mot denna prognos för att beräkna kostnaden som ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="a21b0-118">Actual costs are compared against this forecast to calculate the cost to complete.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a21b0-119">Som föregående uppskattning</span><span class="sxs-lookup"><span data-stu-id="a21b0-119">As previous estimate</span></span>         | <span data-ttu-id="a21b0-120">Här används samma uppskattningsmetoder som användes under föregående period.</span><span class="sxs-lookup"><span data-stu-id="a21b0-120">The same estimate methods that was used in the previous period is used here.</span></span> <span data-ttu-id="a21b0-121">Den här metoden kräver en prognosmodell om den föregående perioden kräver en prognosmodell.</span><span class="sxs-lookup"><span data-stu-id="a21b0-121">This method requires a forecast model if the previous period required a forecast model.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a21b0-122">Ange att kostnaden ska slutföras till noll</span><span class="sxs-lookup"><span data-stu-id="a21b0-122">Set cost to complete to zero</span></span> | <span data-ttu-id="a21b0-123">Denna metod används vanligtvis innan uppskattningsprojektet elimineras, matchar totala uppskattningar med bokförda faktiska transaktioner och avmarkerar kolumnen **Kostnad för att slutföra**.</span><span class="sxs-lookup"><span data-stu-id="a21b0-123">Typically used before the estimate project is eliminated, this method matches total estimates with posted actual transactions and clears the **Cost to complete** column.</span></span> <span data-ttu-id="a21b0-124">Efter slutförande blir resultatet alltid 100 procent.</span><span class="sxs-lookup"><span data-stu-id="a21b0-124">When complete, the result is always 100 percent.</span></span> <span data-ttu-id="a21b0-125">För varje kostnadsrad som du skapar avmarkeras kryssrutan **Prognosticering** och den totala uppskattningen kopieras från den föregående kostnadsuppskattningen.</span><span class="sxs-lookup"><span data-stu-id="a21b0-125">For each cost line that you create, the **Forecasting** check box is cleared and the total estimate is copied from the previous cost estimate.</span></span> <span data-ttu-id="a21b0-126">Den faktiska förbrukningen för uppskattningsperioden dras från kostnaden för att slutföra projektet.</span><span class="sxs-lookup"><span data-stu-id="a21b0-126">The actual consumption for the estimate period is deducted from the cost to complete the project.</span></span>              |
| <span data-ttu-id="a21b0-127">Från kostnadsmall</span><span class="sxs-lookup"><span data-stu-id="a21b0-127">From cost template</span></span>           | <span data-ttu-id="a21b0-128">Kostnaden för att slutföra den konfigurerade metoden i kostnadsmallen som är kopplad till det valda uppskattningsprojektet.</span><span class="sxs-lookup"><span data-stu-id="a21b0-128">The cost to complete method that is set up in the cost template that's associated with the selected estimate project.</span></span>                                                                                                                                                                                                                                                                                                                                                                          |