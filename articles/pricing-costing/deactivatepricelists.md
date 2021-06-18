---
title: Inaktivera prislistor
description: Här ämne hur du inaktiverar eller tar bort oanvända eller gamla prislistor.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001358"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="bddf7-103">Inaktivera prislistor</span><span class="sxs-lookup"><span data-stu-id="bddf7-103">Deactivate price lists</span></span> 

<span data-ttu-id="bddf7-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="bddf7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bddf7-105">Du måste slutföra två steg om du vill ta bort Dynamics 365 Project Operations gamla eller oanvända prislistor.</span><span class="sxs-lookup"><span data-stu-id="bddf7-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="bddf7-106">Ta bort eller radera prislistan från specifika sidor.</span><span class="sxs-lookup"><span data-stu-id="bddf7-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="bddf7-107">Inaktivera eller ta bort prislistan från aktiva prislistor på sidan **Prislistor**.</span><span class="sxs-lookup"><span data-stu-id="bddf7-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="bddf7-108">Du måste slutföra båda stegen för att helt ta bort en prislista.</span><span class="sxs-lookup"><span data-stu-id="bddf7-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="bddf7-109">Det räcker inte att utföra steg 2, som är att direkt ta bort eller inaktivera prislistan från vyn Aktiva prislistor.</span><span class="sxs-lookup"><span data-stu-id="bddf7-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="bddf7-110">Du måste också ta bort prislistans association från alla platser som anges i steg 1.</span><span class="sxs-lookup"><span data-stu-id="bddf7-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="bddf7-111">Ta bort prislistan från specifika sidor</span><span class="sxs-lookup"><span data-stu-id="bddf7-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="bddf7-112">Om du vill ta bort en prislista från Project Operations går du till följande sidor:</span><span class="sxs-lookup"><span data-stu-id="bddf7-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="bddf7-113">Sidan **Projektparameter** > fliken **Prislistor**</span><span class="sxs-lookup"><span data-stu-id="bddf7-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="bddf7-114">Sidan **Organisationsenhet** > rutnätet **Prislistor**</span><span class="sxs-lookup"><span data-stu-id="bddf7-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="bddf7-115">Sidan **Konto** > rutnätet **Projektprislistor**</span><span class="sxs-lookup"><span data-stu-id="bddf7-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="bddf7-116">Sidan **Projektofferter** > rutnätet **Projektprislistor**: Detta gäller för alla aktiva projektofferter.</span><span class="sxs-lookup"><span data-stu-id="bddf7-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="bddf7-117">Sidan **Projektkontrakt** > rutnätet **Projektprislistor**: Detta gäller för alla aktiva projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="bddf7-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="bddf7-118">För varje sida måste du markera den prislista du vill ta bort och sedan välja **Ta bort**.</span><span class="sxs-lookup"><span data-stu-id="bddf7-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="bddf7-119">Ta bort eller inaktivera prislistan från sidan Prislistor</span><span class="sxs-lookup"><span data-stu-id="bddf7-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="bddf7-120">Om du vill ta bort en prislista från de aktiva prislistorna går du **Försäljning** > **Kunder** > **Prislistor**.</span><span class="sxs-lookup"><span data-stu-id="bddf7-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="bddf7-121">Välj den prislista som du vill ta bort och tryck sedan på **Ta bort**.</span><span class="sxs-lookup"><span data-stu-id="bddf7-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="bddf7-122">Om prislistan refereras till befintliga transaktioner går det inte att ta bort den.</span><span class="sxs-lookup"><span data-stu-id="bddf7-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="bddf7-123">Om det händer kan du inaktivera prislistan så att den inte visas i några vyer.</span><span class="sxs-lookup"><span data-stu-id="bddf7-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="bddf7-124">Om du vill inaktivera prislistan markerar du prislistan igen och väljer sedan **Inaktivera**.</span><span class="sxs-lookup"><span data-stu-id="bddf7-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
