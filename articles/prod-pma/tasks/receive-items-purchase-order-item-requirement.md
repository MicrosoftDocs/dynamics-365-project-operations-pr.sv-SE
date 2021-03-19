---
title: Inleverera artiklar på inköpsorder från artikelbehov
description: I den här ämne beskrivs hur du tar emot artiklar på en inköpsorder från ett artikelbehov.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2083516ff929113fd6db377acfe5aeb104666dd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288250"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="1a007-103">Inleverera artiklar på inköpsorder från artikelbehov</span><span class="sxs-lookup"><span data-stu-id="1a007-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a007-104">I den här ämne beskrivs hur du tar emot artiklar på en inköpsorder från ett artikelbehov.</span><span class="sxs-lookup"><span data-stu-id="1a007-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="1a007-105">Om du använder ett artikelbehov i stället för en artikeltransaktion kan du planera för leverans precis innan artikeln faktiskt används, skapa en inköpsorder, ta med artikeln i ramverket för handelsavtal och ta med artikelbehovet i produktionsplaneringen.</span><span class="sxs-lookup"><span data-stu-id="1a007-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="1a007-106">I den här uppgiften används USSI-datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="1a007-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1a007-107">I navigerings fönstret går du till **moduler > projektledning och redovisning > projekt > alla projekt**.</span><span class="sxs-lookup"><span data-stu-id="1a007-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="1a007-108">Klicka på länken i önskad rad i listan.</span><span class="sxs-lookup"><span data-stu-id="1a007-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="1a007-109">Välj plan i åtgärdsrutan **åtgärd**.</span><span class="sxs-lookup"><span data-stu-id="1a007-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="1a007-110">Välj **artikelkrav**.</span><span class="sxs-lookup"><span data-stu-id="1a007-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="1a007-111">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="1a007-111">Select **New**.</span></span>
6. <span data-ttu-id="1a007-112">Ange eller välj ett värde i den nya raden i fältet **artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="1a007-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="1a007-113">I fältet **Kvantitet** anger du ett nummer.</span><span class="sxs-lookup"><span data-stu-id="1a007-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="1a007-114">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="1a007-114">Select **Save**.</span></span>
9. <span data-ttu-id="1a007-115">Välj plan i åtgärdsrutan **Hantera**.</span><span class="sxs-lookup"><span data-stu-id="1a007-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="1a007-116">Välj **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="1a007-116">Select **Functions**.</span></span>
11. <span data-ttu-id="1a007-117">Välj **Skapa en ny inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="1a007-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="1a007-118">Markera kryssrutan **Inkludera alla**.</span><span class="sxs-lookup"><span data-stu-id="1a007-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="1a007-119">I fältet **Leverantörskonto** field, enter or select a value.</span><span class="sxs-lookup"><span data-stu-id="1a007-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="1a007-120">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a007-120">Select **OK**.</span></span>
15. <span data-ttu-id="1a007-121">I navigeringsfönstret går du till **moduler > leverantörsreskontra > inköpsorder > alla inköpsorder**.</span><span class="sxs-lookup"><span data-stu-id="1a007-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="1a007-122">Klicka på länken i önskad rad i listan.</span><span class="sxs-lookup"><span data-stu-id="1a007-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="1a007-123">Välj plan i åtgärdsrutan **Köpa**.</span><span class="sxs-lookup"><span data-stu-id="1a007-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="1a007-124">Välj **Bekräfta**.</span><span class="sxs-lookup"><span data-stu-id="1a007-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="1a007-125">Välj plan i åtgärdsrutan **Ta emot**.</span><span class="sxs-lookup"><span data-stu-id="1a007-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="1a007-126">Välj **Produktinleverans**.</span><span class="sxs-lookup"><span data-stu-id="1a007-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="1a007-127">I fältet **Produktinleverans** skriver du ett värde.</span><span class="sxs-lookup"><span data-stu-id="1a007-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="1a007-128">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a007-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]