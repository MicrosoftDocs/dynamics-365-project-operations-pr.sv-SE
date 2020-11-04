---
title: Skicka en resursbegäran
description: I den här ämnet finns information om hur du skickar en förfrågan för en projektresurs.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085633"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="5683a-103">Skicka en resursbegäran</span><span class="sxs-lookup"><span data-stu-id="5683a-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5683a-104">Du kan skicka in ett genererat resursbehov som en resursförfrågan.</span><span class="sxs-lookup"><span data-stu-id="5683a-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="5683a-105">Förfrågan skickas sedan till en resursansvarig för att uppfylla.</span><span class="sxs-lookup"><span data-stu-id="5683a-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="5683a-106">I Project Service Automation (PSA), på sidan **Projekt** , klicka på fliken **Team** för att visa en lista över bokningsbara resurser.</span><span class="sxs-lookup"><span data-stu-id="5683a-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="5683a-107">Markera den allmänna resurs som har ett resurskrav i listan och klicka på **skicka förfrågan**.</span><span class="sxs-lookup"><span data-stu-id="5683a-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Skicka en resursbegäran](media/RM-how-to-18.png)

<span data-ttu-id="5683a-109">Status för begäran för den allmänna teammedlemmen ändras till **skickad**.</span><span class="sxs-lookup"><span data-stu-id="5683a-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="5683a-110">När förfrågan har uppfyllts av resursansvarig ersätts den allmänna resursen av en namngiven resurs om resursansvariges begäran uppfyller bokningen av en namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="5683a-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="5683a-111">Annars kvarstår den allmänna resursen på teamet och status för förfrågan ändras till **måste granskas** om resursansvarig har föreslagit en namngiven resurs.</span><span class="sxs-lookup"><span data-stu-id="5683a-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
