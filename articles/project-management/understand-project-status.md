---
title: Förstå projektstatus
description: Detta ämne ger information om statusen för projekt i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993438"
---
# <a name="understand-project-status"></a><span data-ttu-id="2f2dc-103">Förstå projektstatus</span><span class="sxs-lookup"><span data-stu-id="2f2dc-103">Understand project status</span></span>

<span data-ttu-id="2f2dc-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="2f2dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2f2dc-105">Avsnittet **Status** på sidan **Projektentitet** ges en sammanfattning av ett projekts hälsa baserat på kostnad och arbetsinsats.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="2f2dc-106">Fält för statussammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f2dc-106">Status summary fields</span></span>

- <span data-ttu-id="2f2dc-107">Fältet **övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="2f2dc-108">Detta fält använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="2f2dc-109">I fältet **kommentarer** kan projektledaren ange kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="2f2dc-110">Fältet **Status uppdaterades** senast går inte att redigera.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="2f2dc-111">Värdet i det här fältet är en tidstämpel som anger när statusen senast uppdaterades.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="2f2dc-112">Fälten **Schemalägg resultat** och **Kostnadsresultat** anges rutnätet utifrån spårningsdatumet.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="2f2dc-113">När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva kan du ange att dessa fält är uppdaterade till **Före**.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="2f2dc-114">När schema och kostnadsavvikelse för rotnoden är negativa anges dessa fält till **Efter**.</span><span class="sxs-lookup"><span data-stu-id="2f2dc-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]