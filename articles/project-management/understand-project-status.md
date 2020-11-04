---
title: Förstå projektstatus
description: I det här ämnet finns information om den status som projekt i Dynamics 365 Project Operations har tilldelats.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085412"
---
# <a name="understand-project-status"></a><span data-ttu-id="b71fe-103">Förstå projektstatus</span><span class="sxs-lookup"><span data-stu-id="b71fe-103">Understand project status</span></span>

<span data-ttu-id="b71fe-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b71fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b71fe-105">I avsnittet **Status** på sidan **Projektentitet** ges en sammanfattning av ett projekts hälsa baserat på kostnad och arbetsinsats.</span><span class="sxs-lookup"><span data-stu-id="b71fe-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="b71fe-106">Fält för statussammanfattning</span><span class="sxs-lookup"><span data-stu-id="b71fe-106">Status summary fields</span></span>

- <span data-ttu-id="b71fe-107">Fältet **Övergripande projektstatus** är ett redigerbart fält som visar projektets övergripande status.</span><span class="sxs-lookup"><span data-stu-id="b71fe-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="b71fe-108">Detta fält använder färgkodning, t.ex. grön, gul och röd för att indikera ökande risker.</span><span class="sxs-lookup"><span data-stu-id="b71fe-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="b71fe-109">I fältet **Kommentarer** kan projektledaren ange kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="b71fe-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="b71fe-110">Fältet **Status uppdaterades senast** går inte att redigera.</span><span class="sxs-lookup"><span data-stu-id="b71fe-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="b71fe-111">Värdet i det här fältet är en tidstämpel som anger när statusen senast uppdaterades.</span><span class="sxs-lookup"><span data-stu-id="b71fe-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="b71fe-112">Fälten **Schemalägg resultat** och **Kostnadsresultat** anges utifrån spårningsrutnätet.</span><span class="sxs-lookup"><span data-stu-id="b71fe-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="b71fe-113">När schema och kostnadsavvikelse för rotnoden i vyn **Insatsspårning** är positiva uppdateras dessa fält till **Före**.</span><span class="sxs-lookup"><span data-stu-id="b71fe-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="b71fe-114">När schema och kostnadsavvikelse för rotnoden är negativa anges dessa fält till **Efter**.</span><span class="sxs-lookup"><span data-stu-id="b71fe-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
