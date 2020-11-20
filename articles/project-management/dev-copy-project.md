---
title: Ta fram projektmallar med Kopiera projekt
description: I det här ämnet finns information om hur du skapar projektmallar med den anpassade åtgärden Kopiera projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131635"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="2bad7-103">Ta fram projektmallar med Kopiera projekt</span><span class="sxs-lookup"><span data-stu-id="2bad7-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="2bad7-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="2bad7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2bad7-105">Med Dynamics 365 Project Operations kan du kopiera ett projekt och återställa alla tilldelningar till de allmänna resurser som representerar rollen.</span><span class="sxs-lookup"><span data-stu-id="2bad7-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="2bad7-106">Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.</span><span class="sxs-lookup"><span data-stu-id="2bad7-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="2bad7-107">När du väljer **Kopiera projekt** uppdateras statusen för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="2bad7-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="2bad7-108">Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar.</span><span class="sxs-lookup"><span data-stu-id="2bad7-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="2bad7-109">Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="2bad7-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="2bad7-110">Den anpassade åtgärden Kopiera projekt</span><span class="sxs-lookup"><span data-stu-id="2bad7-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="2bad7-111">Namn</span><span class="sxs-lookup"><span data-stu-id="2bad7-111">Name</span></span> 

<span data-ttu-id="2bad7-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="2bad7-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="2bad7-113">Indataparametrar</span><span class="sxs-lookup"><span data-stu-id="2bad7-113">Input parameters</span></span>
<span data-ttu-id="2bad7-114">Det finns tre indataparametrar:</span><span class="sxs-lookup"><span data-stu-id="2bad7-114">There are three input parameters:</span></span>

| <span data-ttu-id="2bad7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bad7-115">Parameter</span></span>          | <span data-ttu-id="2bad7-116">Type</span><span class="sxs-lookup"><span data-stu-id="2bad7-116">Type</span></span>   | <span data-ttu-id="2bad7-117">Värden</span><span class="sxs-lookup"><span data-stu-id="2bad7-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="2bad7-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="2bad7-118">ProjectCopyOption</span></span>  | <span data-ttu-id="2bad7-119">String</span><span class="sxs-lookup"><span data-stu-id="2bad7-119">String</span></span> | <span data-ttu-id="2bad7-120">**{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="2bad7-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="2bad7-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="2bad7-121">SourceProject</span></span>      | <span data-ttu-id="2bad7-122">Entitetsreferens</span><span class="sxs-lookup"><span data-stu-id="2bad7-122">Entity Reference</span></span> | <span data-ttu-id="2bad7-123">Källprojekt</span><span class="sxs-lookup"><span data-stu-id="2bad7-123">Source Project</span></span> |
| <span data-ttu-id="2bad7-124">Mål</span><span class="sxs-lookup"><span data-stu-id="2bad7-124">Target</span></span>             | <span data-ttu-id="2bad7-125">Entitetsreferens</span><span class="sxs-lookup"><span data-stu-id="2bad7-125">Entity Reference</span></span> | <span data-ttu-id="2bad7-126">Målprojekt</span><span class="sxs-lookup"><span data-stu-id="2bad7-126">Target Project</span></span> |


- <span data-ttu-id="2bad7-127">**{"clearTeamsAndAssignments":true}**: Tre standardbeteenden för Project for the Web och tar bort alla tilldelningar och teammedlemmar.</span><span class="sxs-lookup"><span data-stu-id="2bad7-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="2bad7-128">**{"removeNamedResources":true}** Standardbeteendet för Project Operations och återför tilldelningar till generiska resurser.</span><span class="sxs-lookup"><span data-stu-id="2bad7-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="2bad7-129">Mer standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="2bad7-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="2bad7-130">Specificera vilka fält som ska kopieras</span><span class="sxs-lookup"><span data-stu-id="2bad7-130">Specify fields to copy</span></span> 
<span data-ttu-id="2bad7-131">När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.</span><span class="sxs-lookup"><span data-stu-id="2bad7-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
