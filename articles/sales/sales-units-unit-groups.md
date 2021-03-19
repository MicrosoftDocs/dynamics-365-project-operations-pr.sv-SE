---
title: Enheter och enhetsgrupper
description: Det här avsnittet innehåller information om hur du skapar enheter och enhetsgrupper i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277360"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="3e69f-103">Enheter och enhetsgrupper</span><span class="sxs-lookup"><span data-stu-id="3e69f-103">Units and unit groups</span></span>

<span data-ttu-id="3e69f-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="3e69f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3e69f-105">Enheterna är de kvantiteter eller de mått du säljer dina produkter eller tjänster i.</span><span class="sxs-lookup"><span data-stu-id="3e69f-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="3e69f-106">Om du till exempel säljer trädgårdsredskap kan du sälja dem i enheter som paket, lådor och lastpallar</span><span class="sxs-lookup"><span data-stu-id="3e69f-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="3e69f-107">En enhetsgrupp är en samling av dessa olika enheter.</span><span class="sxs-lookup"><span data-stu-id="3e69f-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="3e69f-108">Följ stegen i det här ämnet genom att kontrollera att du har tilldelats rollen systemadministratör eller Sales Professional-ansvarig eller har motsvarande behörighet.</span><span class="sxs-lookup"><span data-stu-id="3e69f-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="3e69f-109">Skapa en enhetsgrupp</span><span class="sxs-lookup"><span data-stu-id="3e69f-109">Create a unit group</span></span>

1. <span data-ttu-id="3e69f-110">I webbplatsöversikten, markera **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="3e69f-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="3e69f-111">Välj **Ny** och dialogrutan **Skapa enhetsgrupp** ange enhetsruta.</span><span class="sxs-lookup"><span data-stu-id="3e69f-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="3e69f-112">I fältet **Primär enhet** anger du den lägsta måttenheten som produkten kommer att säljas i.</span><span class="sxs-lookup"><span data-stu-id="3e69f-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="3e69f-113">Du kan till exempel ange "stycke" eller "ounce".</span><span class="sxs-lookup"><span data-stu-id="3e69f-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="3e69f-114">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e69f-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="3e69f-115">Lägg till enheter till en enhetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="3e69f-115">Add units to a unit group</span></span>

1. <span data-ttu-id="3e69f-116">Öppna en enhetsgrupp och på fliken **relaterad** väljer du **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="3e69f-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="3e69f-117">Du ser att den primära enheten redan lagts till.</span><span class="sxs-lookup"><span data-stu-id="3e69f-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="3e69f-118">Välj **Lägg till ny enhet** och på sidan **Snabbregistrering: enhet** i fältet **Namn** anger du namnet för enheten.</span><span class="sxs-lookup"><span data-stu-id="3e69f-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="3e69f-119">I fältet **kvantitet** ange den kvantitet som enheten ska innehålla.</span><span class="sxs-lookup"><span data-stu-id="3e69f-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="3e69f-120">Om en låda till exempel innehåller 2 stycken skriver du "2".</span><span class="sxs-lookup"><span data-stu-id="3e69f-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="3e69f-121">I fältet **Basenhet** väljer du en basenhet för att fastställa den lägsta mått enheten för enheten.</span><span class="sxs-lookup"><span data-stu-id="3e69f-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="3e69f-122">Du kan till exempel välja "stycke".</span><span class="sxs-lookup"><span data-stu-id="3e69f-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="3e69f-123">Välj **Spara**:</span><span class="sxs-lookup"><span data-stu-id="3e69f-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]