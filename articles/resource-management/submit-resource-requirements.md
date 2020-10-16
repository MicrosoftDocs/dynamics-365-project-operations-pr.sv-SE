---
title: Skicka en resursbegäran
description: Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961752"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="f0e90-104">Skicka en resursbegäran</span><span class="sxs-lookup"><span data-stu-id="f0e90-104">Submit a resource request</span></span>

<span data-ttu-id="f0e90-105">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="f0e90-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0e90-106">Du kan skicka in ett genererat resursbehov som en resursförfrågan.</span><span class="sxs-lookup"><span data-stu-id="f0e90-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="f0e90-107">Förfrågan skickas sedan till en resursansvarig för att uppfylla.</span><span class="sxs-lookup"><span data-stu-id="f0e90-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="f0e90-108">I Dynamics 365 Project Operations, på sidan **Projekt**, väljer du fliken **Team** för att visa en lista över bokningsbara resurser.</span><span class="sxs-lookup"><span data-stu-id="f0e90-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="f0e90-109">Välj den generiska resurs som har ett resurskrav i listan och klicka på **Skicka förfrågan**.</span><span class="sxs-lookup"><span data-stu-id="f0e90-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="f0e90-110">Status för begäran för den allmänna teammedlemmen ändras till **skickad**.</span><span class="sxs-lookup"><span data-stu-id="f0e90-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="f0e90-111">När förfrågan har uppfyllts ersätts den generiska resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="f0e90-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="f0e90-112">om resursansvarig föreslår en namngiven resurs kvarstår annars den generiska resursen i teamet och status för förfrågan ändras till **Måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="f0e90-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
