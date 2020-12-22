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
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642430"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="95ba6-103">Ta fram projektmallar med Kopiera projekt</span><span class="sxs-lookup"><span data-stu-id="95ba6-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="95ba6-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="95ba6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="95ba6-105">Dynamics 365 Project Operations stöder möjligheten att kopiera ett projekt och återställa eventuella tilldelningar till de generiska resurser som representerar rollen.</span><span class="sxs-lookup"><span data-stu-id="95ba6-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="95ba6-106">Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.</span><span class="sxs-lookup"><span data-stu-id="95ba6-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="95ba6-107">När du väljer **Kopiera projekt** uppdateras statusen för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="95ba6-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="95ba6-108">Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar.</span><span class="sxs-lookup"><span data-stu-id="95ba6-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="95ba6-109">Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.</span><span class="sxs-lookup"><span data-stu-id="95ba6-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="95ba6-110">Den anpassade åtgärden Kopiera projekt</span><span class="sxs-lookup"><span data-stu-id="95ba6-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="95ba6-111">Namn</span><span class="sxs-lookup"><span data-stu-id="95ba6-111">Name</span></span> 

<span data-ttu-id="95ba6-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="95ba6-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="95ba6-113">Indataparametrar</span><span class="sxs-lookup"><span data-stu-id="95ba6-113">Input parameters</span></span>
<span data-ttu-id="95ba6-114">Det finns tre indataparametrar:</span><span class="sxs-lookup"><span data-stu-id="95ba6-114">There are three input parameters:</span></span>

| <span data-ttu-id="95ba6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="95ba6-115">Parameter</span></span>          | <span data-ttu-id="95ba6-116">Typ</span><span class="sxs-lookup"><span data-stu-id="95ba6-116">Type</span></span>   | <span data-ttu-id="95ba6-117">Värden</span><span class="sxs-lookup"><span data-stu-id="95ba6-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="95ba6-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="95ba6-118">ProjectCopyOption</span></span>  | <span data-ttu-id="95ba6-119">Sträng</span><span class="sxs-lookup"><span data-stu-id="95ba6-119">String</span></span> | <span data-ttu-id="95ba6-120">**{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="95ba6-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="95ba6-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="95ba6-121">SourceProject</span></span>      | <span data-ttu-id="95ba6-122">Entitetsreferens</span><span class="sxs-lookup"><span data-stu-id="95ba6-122">Entity Reference</span></span> | <span data-ttu-id="95ba6-123">Källprojekt</span><span class="sxs-lookup"><span data-stu-id="95ba6-123">Source Project</span></span> |
| <span data-ttu-id="95ba6-124">Mål</span><span class="sxs-lookup"><span data-stu-id="95ba6-124">Target</span></span>             | <span data-ttu-id="95ba6-125">Entitetsreferens</span><span class="sxs-lookup"><span data-stu-id="95ba6-125">Entity Reference</span></span> | <span data-ttu-id="95ba6-126">Målprojekt</span><span class="sxs-lookup"><span data-stu-id="95ba6-126">Target Project</span></span> |


- <span data-ttu-id="95ba6-127">**{"clearTeamsAndAssignments":true}**: Tre standardbeteenden för Project for the Web och tar bort alla tilldelningar och gruppmedlemmar.</span><span class="sxs-lookup"><span data-stu-id="95ba6-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="95ba6-128">**{"removeNamedResources":true}** Standardbeteendet för Project Operations och återställer tilldelningar till generiska resurser.</span><span class="sxs-lookup"><span data-stu-id="95ba6-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="95ba6-129">Mer standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="95ba6-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="95ba6-130">Specificera vilka fält som ska kopieras</span><span class="sxs-lookup"><span data-stu-id="95ba6-130">Specify fields to copy</span></span> 
<span data-ttu-id="95ba6-131">När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.</span><span class="sxs-lookup"><span data-stu-id="95ba6-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
