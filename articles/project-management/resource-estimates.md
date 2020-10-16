---
title: Resursberäkningar
description: I det här ämnet finns information om hur resursuppskattningar beräknas i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928612"
---
# <a name="resource-estimates"></a><span data-ttu-id="ad1ef-103">Resursberäkningar</span><span class="sxs-lookup"><span data-stu-id="ad1ef-103">Resource estimates</span></span>

<span data-ttu-id="ad1ef-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="ad1ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ad1ef-105">Resursuppskattningar kommer från tidsfasade arbetsinsatser som har definierats i den uppdelade arbetsstrukturen tillsammans med tillämpliga prissättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="ad1ef-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="ad1ef-106">Vanligtvis är beräkningen **taxa/timme för varje roll x timmar.**</span><span class="sxs-lookup"><span data-stu-id="ad1ef-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="ad1ef-107">Den tidsfasade arbetsinsatsen för varje resurs lagras i resurstilldelningsposten.</span><span class="sxs-lookup"><span data-stu-id="ad1ef-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="ad1ef-108">Prissättningen lagras i en fördefinierad prislista.</span><span class="sxs-lookup"><span data-stu-id="ad1ef-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="ad1ef-109">Enhetskonvertering används på grundval av tillämplig prislista.</span><span class="sxs-lookup"><span data-stu-id="ad1ef-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resursuppskattningar](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="ad1ef-111">Standardvärden för självkostnad och kostnadsvaluta</span><span class="sxs-lookup"><span data-stu-id="ad1ef-111">Default cost price and cost currency</span></span>

<span data-ttu-id="ad1ef-112">Självkostnader används som standard från organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="ad1ef-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="ad1ef-113">Standardvärden för fakturataxan och försäljningsvaluta</span><span class="sxs-lookup"><span data-stu-id="ad1ef-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="ad1ef-114">Försäljningspriser tillämpas en gång per affär.</span><span class="sxs-lookup"><span data-stu-id="ad1ef-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="ad1ef-115">Hierarkin för försäljningsprislista är som standard följande:</span><span class="sxs-lookup"><span data-stu-id="ad1ef-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="ad1ef-116">Organisation</span><span class="sxs-lookup"><span data-stu-id="ad1ef-116">Organization</span></span>
2. <span data-ttu-id="ad1ef-117">Kund</span><span class="sxs-lookup"><span data-stu-id="ad1ef-117">Customer</span></span>
3. <span data-ttu-id="ad1ef-118">Offert/kontrakt</span><span class="sxs-lookup"><span data-stu-id="ad1ef-118">Quote/contract</span></span>
