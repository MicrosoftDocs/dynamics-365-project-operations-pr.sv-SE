---
title: Uppdatera beräkning vid färdigställande
description: I det här ämnet finns information om hur du uppdaterar projektionen av arbetsinsatsen i ett projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286450"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="2434c-103">Uppdatera beräkning vid färdigställande</span><span class="sxs-lookup"><span data-stu-id="2434c-103">Update estimate at completion</span></span>

<span data-ttu-id="2434c-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="2434c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2434c-105">Det är vanligt att projektledaren ändrar de ursprungliga uppskattningarna för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="2434c-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="2434c-106">Omprojektioner av projekt är projektledarens uppfattning om uppskattningar, med tanke på projektets aktuella status.</span><span class="sxs-lookup"><span data-stu-id="2434c-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="2434c-107">Vi rekommenderar dock inte att projektledare ändrar baslinjenumren, eftersom projektbaslinjen representerar den etablerade sanningen för projektets schema och kostnadsberäkning, och alla projektintressenter har gått med på det.</span><span class="sxs-lookup"><span data-stu-id="2434c-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="2434c-108">Det finns två sätt som en projektledare kan använda för att förnya arbetet för uppgifter:</span><span class="sxs-lookup"><span data-stu-id="2434c-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="2434c-109">Åsidosätt standardtid som krävs för att slutföra (ETC) en ny uppskattning av den faktiska resterande insatsen för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="2434c-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="2434c-110">Åsidosätt standardförlopp i procent med en ny uppskattning av det faktiska förloppen för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="2434c-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="2434c-111">Var och en av dessa är en omberäkning av aktivitetens ETC, uppskattning för att slutföra (EAC) och förloppsprocent och den planerade insatsavvikelsen för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="2434c-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="2434c-112">Procenten för EAC, ETC och förloppsprocent för sammanfattningsaktiviteterna beräknas om, och produktionen skapas som en ny projektion av insatsavvikelsen.</span><span class="sxs-lookup"><span data-stu-id="2434c-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]