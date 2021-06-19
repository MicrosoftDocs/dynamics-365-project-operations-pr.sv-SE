---
title: Godkännandeuppsättningar
description: Det här ämnet innehåller information om godkännandeuppsättning, förfrågningar och underuppsättningen för dessa åtgärder.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116893"
---
# <a name="approval-sets"></a><span data-ttu-id="5c9b1-103">Godkännandeuppsättningar</span><span class="sxs-lookup"><span data-stu-id="5c9b1-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5c9b1-104">Godkännandeuppsättningar samlar godkännandeförfrågningar i mindre underuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="5c9b1-105">Med hjälp av den här grupperingen kan godkännanden bearbetas i projektordning och det går att försöka och sekvensera igen.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="5c9b1-106">Genom att gruppera ökar tillförlitligheten och spårningen för godkännandebearbetning för stora godkännanden.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="5c9b1-107">Godkännandeuppsättningar anger det övergripande bearbetningstillståndet för de relaterade posterna.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="5c9b1-108">När en godkännandepost bearbetas med hjälp av en godkännandeuppsättning flyttas posten från **Skickad** till **Godkänd** och avlänkas från godkännandeuppsättningen.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="5c9b1-109">Om en post misslyckas när den skickas för godkännande har posten fortfarande statusen **Skickad** och godkännandeuppsättningen markeras som misslyckad.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="5c9b1-110">I godkännandeuppsättningen loggas felmeddelandet om felet.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="5c9b1-111">Bearbetning av godkännanden och godkännandeuppsättningar</span><span class="sxs-lookup"><span data-stu-id="5c9b1-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="5c9b1-112">Godkännanden som köas för bearbetning visas i vyn **Bearbetningsgodkännanden**.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="5c9b1-113">Systemet försöker bearbeta alla poster flera gånger asynkront, inklusive att försöka utföra ett godkännande igen om det inte gick att utföra tidigare försök.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="5c9b1-114">I fältet **Livstid för godkännandeuppsättning** registreras antalet försök kvar att bearbeta uppsättningen innan den markeras som misslyckad.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="5c9b1-115">Misslyckade godkännanden och godkännandeuppsättningar</span><span class="sxs-lookup"><span data-stu-id="5c9b1-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="5c9b1-116">I vyn **Misslyckade godkännanden** listas alla godkännanden som kräver användaråtgärd.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="5c9b1-117">Öppna de associerade godkännandeuppsättningsloggarna för att identifiera orsaken till felet.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="5c9b1-118">Om du väljer **Försök igen** läggs detta till i godkännandeuppsättningens livstid, förs godkännandeuppsättningen tillbaka till statusen **Bearbetar** och försöker att bearbeta de återstående posterna.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="5c9b1-119">Konfigurera godkännandeuppsättningar</span><span class="sxs-lookup"><span data-stu-id="5c9b1-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="5c9b1-120">Aktivera funktionen Godkännandeuppsättningar</span><span class="sxs-lookup"><span data-stu-id="5c9b1-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="5c9b1-121">Innan du aktiverar funktionen Godkännandeuppsättningar bör du kontrollera att inga godkännanden för närvarande bearbetas.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="5c9b1-122">Gå till sidan **Projektparametrar** och välj **Funktionskontroll** > **Aktivera moderna godkännanden**.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="5c9b1-123">Inaktivera funktionen Godkännandeuppsättningar</span><span class="sxs-lookup"><span data-stu-id="5c9b1-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="5c9b1-124">Innan du inaktiverar funktionen Godkännandeuppsättningar bör du kontrollera att inga godkännanden för närvarande bearbetas.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="5c9b1-125">Gå till sidan **Projektparametrar** och välj **Funktionskontroll** > **Inaktivera moderna godkännanden**.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="5c9b1-126">Konfigurera det asynkrona tröskelvärdet</span><span class="sxs-lookup"><span data-stu-id="5c9b1-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="5c9b1-127">När godkännandeuppsättningar skapas flyttas bearbetning till bakgrunden när det valda antalet poster för godkännande överskrider det angivna tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="5c9b1-128">Använd fältet **Asynkront tröskelvärde** för att konfigurera när godkännandeprocessen ska köras synkront eller asynkront.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="5c9b1-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="5c9b1-129">Valid values are:</span></span>

  - <span data-ttu-id="5c9b1-130">Noll: Alla förfrågningar ska bearbetas asynkront.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="5c9b1-131">Nummer som är större än noll: Godkännanden bearbetas asynkront endast när det skickade antalet godkännanden överskrider detta värde.</span><span class="sxs-lookup"><span data-stu-id="5c9b1-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
