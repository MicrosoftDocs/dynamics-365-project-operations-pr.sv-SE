---
title: Uppdatera ett projekt
description: I det här ämnet finns information om uppdatering av projekt i Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993393"
---
# <a name="update-a-project"></a><span data-ttu-id="b8703-103">Uppdatera ett projekt</span><span class="sxs-lookup"><span data-stu-id="b8703-103">Update a project</span></span>

<span data-ttu-id="b8703-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b8703-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8703-105">Nedan visas en sammanfattning av de fält som kan uppdateras i ett projekt efter att det har skapats och alla relevanta effekter av uppdateringarna.</span><span class="sxs-lookup"><span data-stu-id="b8703-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="b8703-106">Projektinformationsfält</span><span class="sxs-lookup"><span data-stu-id="b8703-106">Project detail fields</span></span>

- <span data-ttu-id="b8703-107">**Namn**: Projektets namn.</span><span class="sxs-lookup"><span data-stu-id="b8703-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="b8703-108">**Beskrivning**: En översikt över projektet.</span><span class="sxs-lookup"><span data-stu-id="b8703-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="b8703-109">**Kund**: Företaget som projektet ska levereras till.</span><span class="sxs-lookup"><span data-stu-id="b8703-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="b8703-110">**Kalendermall**: Arbetstimmarna för projektet.</span><span class="sxs-lookup"><span data-stu-id="b8703-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="b8703-111">När fältet ändras beräknas hela schemat om.</span><span class="sxs-lookup"><span data-stu-id="b8703-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="b8703-112">**Valuta**: Valutan för projektet.</span><span class="sxs-lookup"><span data-stu-id="b8703-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="b8703-113">Det här fältet hämtas baserat på valutan som definieras i kontrakteringsenheten.</span><span class="sxs-lookup"><span data-stu-id="b8703-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="b8703-114">När kontrakteringsenheten uppdateras uppdateras även fältet.</span><span class="sxs-lookup"><span data-stu-id="b8703-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="b8703-115">**Kontrakteringsenhet**: Den organisationsenhet som representerar den företagsgrupp eller avdelning som framför allt är ansvarig för att ta hem försäljningen och hantera leveransen av arbetet och tjänsterna till kunden.</span><span class="sxs-lookup"><span data-stu-id="b8703-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="b8703-116">**Projektledare**: Den medlem i projektteamet som har behörighet att granska och godkänna tidsposter och utgifter.</span><span class="sxs-lookup"><span data-stu-id="b8703-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="b8703-117">Uppskattningsfält</span><span class="sxs-lookup"><span data-stu-id="b8703-117">Estimate fields</span></span>

- <span data-ttu-id="b8703-118">**Uppskattat startdatum** : Datumet då projektet kommer att starta.</span><span class="sxs-lookup"><span data-stu-id="b8703-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="b8703-119">När det här fältet uppdateras kommer alla uppgifter i projektet att förskjutas proportionerligt med det nya startdatumet.</span><span class="sxs-lookup"><span data-stu-id="b8703-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="b8703-120">**Slutdatum**: Datumet då projektet planeras sluta.</span><span class="sxs-lookup"><span data-stu-id="b8703-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="b8703-121">**Insats**: Projektets uppskattade insats.</span><span class="sxs-lookup"><span data-stu-id="b8703-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="b8703-122">När uppgifter läggs till i projektet går det inte längre att redigera det här fältet.</span><span class="sxs-lookup"><span data-stu-id="b8703-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="b8703-123">**Uppskattad arbetskostnad**: Projektets uppskattade arbetskostnad.</span><span class="sxs-lookup"><span data-stu-id="b8703-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="b8703-124">När arbetskostnader läggs till i projektet går det inte längre att redigera det här fältet.</span><span class="sxs-lookup"><span data-stu-id="b8703-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="b8703-125">**Uppskattade utgifter**: Projektets uppskattade utgifter.</span><span class="sxs-lookup"><span data-stu-id="b8703-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="b8703-126">När utgifter läggs till i projektet går det inte längre att redigera det här fältet.</span><span class="sxs-lookup"><span data-stu-id="b8703-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="b8703-127">Fält för projektets faktiska värden</span><span class="sxs-lookup"><span data-stu-id="b8703-127">Project actual fields</span></span>
- <span data-ttu-id="b8703-128">**Faktisk start** : Datumet då projektet startades.</span><span class="sxs-lookup"><span data-stu-id="b8703-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="b8703-129">**Faktiskt slut**: Uppdateras när ett projekt har slutförts.</span><span class="sxs-lookup"><span data-stu-id="b8703-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="b8703-130">Projektstatusfält</span><span class="sxs-lookup"><span data-stu-id="b8703-130">Project status fields</span></span>

- <span data-ttu-id="b8703-131">**Övergripande projektstatus**: Det övergripande projekthälsotillståndet från projektledaren.</span><span class="sxs-lookup"><span data-stu-id="b8703-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="b8703-132">**Kommentarer**: om den aktuella hälsan för projektet som projektledaren har tillhandahållit.</span><span class="sxs-lookup"><span data-stu-id="b8703-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]