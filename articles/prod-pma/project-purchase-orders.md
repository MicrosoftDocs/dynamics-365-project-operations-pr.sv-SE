---
title: Inköpsorder för ett projekt
description: I den här artikeln beskrivs olika metoder som du kan använda för att skapa inköpsorder för ett projekt. Vilken metod du ska använda beror på inköpsorderns syfte och när de inköpta artiklarna förbrukas och debiteras ett projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289211"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="dbcef-104">Inköpsorder för ett projekt</span><span class="sxs-lookup"><span data-stu-id="dbcef-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbcef-105">I den här artikeln beskrivs olika metoder som du kan använda för att skapa inköpsorder för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="dbcef-106">Vilken metod du ska använda beror på inköpsorderns syfte och när de inköpta artiklarna förbrukas och debiteras ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="dbcef-107">Metoder för att skapa en inköpsorder</span><span class="sxs-lookup"><span data-stu-id="dbcef-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="dbcef-108">Du kan använda någon av följande metoder för att skapa en inköpsorder i projektledning och redovisning.</span><span class="sxs-lookup"><span data-stu-id="dbcef-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="dbcef-109">Syftet med inköpsordern avgör när inköpsordern konsumeras och därför när artiklar debiteras för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dbcef-110">Metod</span><span class="sxs-lookup"><span data-stu-id="dbcef-110">Method</span></span></th>
<th><span data-ttu-id="dbcef-111">Syfte</span><span class="sxs-lookup"><span data-stu-id="dbcef-111">Purpose</span></span></th>
<th><span data-ttu-id="dbcef-112">Förbrukning av artiklar</span><span class="sxs-lookup"><span data-stu-id="dbcef-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dbcef-113">Skapa en inköpsorder direkt från ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="dbcef-114">Använd den här metoden om du vill köpa artiklar från en extern leverantör för förbrukning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="dbcef-115">Du kan skapa inköpsorder på två sätt:</span><span class="sxs-lookup"><span data-stu-id="dbcef-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="dbcef-116">Från själva projektet.</span><span class="sxs-lookup"><span data-stu-id="dbcef-116">From the project itself.</span></span> <span data-ttu-id="dbcef-117">I det här fallet är projektet redan definierat för inköpsordern.</span><span class="sxs-lookup"><span data-stu-id="dbcef-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="dbcef-118">Genom att navigera till projektets inköpsorder.</span><span class="sxs-lookup"><span data-stu-id="dbcef-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="dbcef-119">Du måste välja både leverantören och projektet för att skapa inköpsordern.</span><span class="sxs-lookup"><span data-stu-id="dbcef-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="dbcef-120">Artiklar förbrukas när leverantörsfakturan uppdateras.</span><span class="sxs-lookup"><span data-stu-id="dbcef-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dbcef-121">Skapa en inköpsorder från en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="dbcef-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="dbcef-122">Använd den här metoden om du vill köpa artiklar när du skapar en försäljningsorder från ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="dbcef-123">Artiklar förbrukas när försäljningsordern faktureras kunden.</span><span class="sxs-lookup"><span data-stu-id="dbcef-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dbcef-124">Skapa en inköpsorder från ett artikelkrav.</span><span class="sxs-lookup"><span data-stu-id="dbcef-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="dbcef-125">Använd den här metoden om du vill köpa artiklar när du skapar ett artikelkrav från ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dbcef-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="dbcef-126">Artiklar förbrukas när följesedeln för artikelkrav uppdateras.</span><span class="sxs-lookup"><span data-stu-id="dbcef-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="dbcef-127">När du uppdaterar leverantörsfakturan eller följesedeln uppmanas du att uppdatera följesedeln på artikelkravet.</span><span class="sxs-lookup"><span data-stu-id="dbcef-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="dbcef-128">Mer information finns i [Ta emot varor på inköpsordern från artikelkravet](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="dbcef-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]