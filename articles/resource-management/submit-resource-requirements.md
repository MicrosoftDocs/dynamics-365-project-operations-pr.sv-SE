---
title: Skicka en resursbegäran
description: Du kan skicka in ett genererat resursbehov som en resursförfrågan. Förfrågan skickas sedan till en resursansvarig för att uppfylla.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128845"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="174ee-104">Skicka en resursbegäran</span><span class="sxs-lookup"><span data-stu-id="174ee-104">Submit a resource request</span></span>

<span data-ttu-id="174ee-105">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="174ee-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="174ee-106">Du kan skicka in ett genererat resursbehov som en resursförfrågan.</span><span class="sxs-lookup"><span data-stu-id="174ee-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="174ee-107">Förfrågan skickas sedan till en resursansvarig för att uppfylla.</span><span class="sxs-lookup"><span data-stu-id="174ee-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="174ee-108">I Dynamics 365 Project Operations, på sidan **Projekt**, väljer du fliken **Team** för att visa en lista över bokningsbara resurser.</span><span class="sxs-lookup"><span data-stu-id="174ee-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="174ee-109">Välj den generiska resurs som har ett resurskrav i listan och klicka på **Skicka förfrågan**.</span><span class="sxs-lookup"><span data-stu-id="174ee-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="174ee-110">Status för begäran för den allmänna teammedlemmen ändras till **skickad**.</span><span class="sxs-lookup"><span data-stu-id="174ee-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="174ee-111">När förfrågan har uppfyllts ersätts den generiska resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="174ee-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="174ee-112">om resursansvarig föreslår en namngiven resurs kvarstår annars den generiska resursen i teamet och status för förfrågan ändras till **Måste granskas**.</span><span class="sxs-lookup"><span data-stu-id="174ee-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
