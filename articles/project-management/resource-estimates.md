---
title: Resursberäkningar
description: I det här ämnet finns information om hur resursuppskattningar beräknas i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286540"
---
# <a name="resource-estimates"></a><span data-ttu-id="34e24-103">Resursberäkningar</span><span class="sxs-lookup"><span data-stu-id="34e24-103">Resource estimates</span></span>

<span data-ttu-id="34e24-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="34e24-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="34e24-105">Resursuppskattningar kommer från tidsfasade arbetsinsatser som har definierats i den uppdelade arbetsstrukturen tillsammans med tillämpliga prissättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="34e24-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="34e24-106">Vanligtvis är beräkningen **taxa/timme för varje roll x timmar.**</span><span class="sxs-lookup"><span data-stu-id="34e24-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="34e24-107">Den tidsfasade arbetsinsatsen för varje resurs lagras i resurstilldelningsposten.</span><span class="sxs-lookup"><span data-stu-id="34e24-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="34e24-108">Prissättningen lagras i en fördefinierad prislista.</span><span class="sxs-lookup"><span data-stu-id="34e24-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="34e24-109">Enhetskonvertering används på grundval av tillämplig prislista.</span><span class="sxs-lookup"><span data-stu-id="34e24-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resursuppskattningar](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="34e24-111">Standardvärden för självkostnad och kostnadsvaluta</span><span class="sxs-lookup"><span data-stu-id="34e24-111">Default cost price and cost currency</span></span>

<span data-ttu-id="34e24-112">Självkostnader används som standard från organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="34e24-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="34e24-113">Standardvärden för fakturataxan och försäljningsvaluta</span><span class="sxs-lookup"><span data-stu-id="34e24-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="34e24-114">Försäljningspriser tillämpas en gång per affär.</span><span class="sxs-lookup"><span data-stu-id="34e24-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="34e24-115">Hierarkin för försäljningsprislista är som standard följande:</span><span class="sxs-lookup"><span data-stu-id="34e24-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="34e24-116">Organisation</span><span class="sxs-lookup"><span data-stu-id="34e24-116">Organization</span></span>
2. <span data-ttu-id="34e24-117">Kund</span><span class="sxs-lookup"><span data-stu-id="34e24-117">Customer</span></span>
3. <span data-ttu-id="34e24-118">Offert/kontrakt</span><span class="sxs-lookup"><span data-stu-id="34e24-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]