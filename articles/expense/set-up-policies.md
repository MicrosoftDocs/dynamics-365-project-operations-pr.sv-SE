---
title: Definiera utgiftspolicyer
description: Du kan definiera utgiftspolicyer som medarbetarna måste följa när de registrerar och skickar utgiftsrapporter och reserekvisitioner.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896663"
---
# <a name="define-expense-policies"></a><span data-ttu-id="caafd-103">Definiera utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="caafd-103">Define expense policies</span></span>

<span data-ttu-id="caafd-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="caafd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="caafd-105">Du kan definiera policyer som medarbetarna måste följa när de registrerar och skickar utgiftsrapporter och reserekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="caafd-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="caafd-106">Med hjälp av utgiftspolicyer kan du effektivt hantera utgifter.</span><span class="sxs-lookup"><span data-stu-id="caafd-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="caafd-107">Du kan till exempel ange en policy för hotellutgifter i New York City, vilket anger att utgiftskostnaden per natt inte får överskrida 250 USD.</span><span class="sxs-lookup"><span data-stu-id="caafd-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="caafd-108">Om en arbetare skickar en utgiftsrapport eller en reserekvisition där rumskostnaden överstiger det här beloppet meddelar systemet</span><span class="sxs-lookup"><span data-stu-id="caafd-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="caafd-109">medarbetaren som policybeloppet för utgiften har överskridits.</span><span class="sxs-lookup"><span data-stu-id="caafd-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="caafd-110">Du kan konfigurera meddelandet som medarbetaren får när du</span><span class="sxs-lookup"><span data-stu-id="caafd-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="caafd-111">definierar policy.</span><span class="sxs-lookup"><span data-stu-id="caafd-111">define the policy.</span></span>      
        
<span data-ttu-id="caafd-112">Du kan definiera tre typer av policyer:</span><span class="sxs-lookup"><span data-stu-id="caafd-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="caafd-113">**Varning**: kan medarbetaren skicka en utgiftsrapport eller reserekvisition men kostnaden markeras för alla godkännare och</span><span class="sxs-lookup"><span data-stu-id="caafd-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="caafd-114">för senare rapportering.</span><span class="sxs-lookup"><span data-stu-id="caafd-114">for later reporting.</span></span>        

- <span data-ttu-id="caafd-115">**Fel**: kräver att medarbetaren ändrar utgifterna för att följa principen innan du skickar utgiftsrapporten eller reserekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="caafd-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="caafd-116">**Motivering**: kräver att arbetaren eller chefen anger en motivering för att policybeloppet överskrids innan utgiftsrapporten skickas eller reserekvisitionen skickas.</span><span class="sxs-lookup"><span data-stu-id="caafd-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="caafd-117">Policytips</span><span class="sxs-lookup"><span data-stu-id="caafd-117">Policy tips</span></span>
<span data-ttu-id="caafd-118">Här följer några förslag som kan hjälpa dig när du skapar nya policyer för utgiftshantering:</span><span class="sxs-lookup"><span data-stu-id="caafd-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="caafd-119">Policyer är datumeffektiva vilket innebär att en policy inte börjar gälla om den skapas med ett datum efter det datum då kostnaden inträffade.</span><span class="sxs-lookup"><span data-stu-id="caafd-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="caafd-120">Du kan till exempel skapa en ny policy i dag för att upprätthålla en maximal måltidsutgift på 50 USD.</span><span class="sxs-lookup"><span data-stu-id="caafd-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="caafd-121">Alla befintliga utgifter som angavs i igår kontrolleras inte mot den här policyn.</span><span class="sxs-lookup"><span data-stu-id="caafd-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="caafd-122">När du skapar en policy för en utgiftskategori som kan specificeras bör du lägga till ett villkor för utgiftsradtypen.</span><span class="sxs-lookup"><span data-stu-id="caafd-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="caafd-123">Vissa policyer, t.ex. krav på kvitton, kanske inte passar för specificerade rader.</span><span class="sxs-lookup"><span data-stu-id="caafd-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="caafd-124">I det här fallet gäller policyn endast för rubrikraden eller en rad som inte har specificerats.</span><span class="sxs-lookup"><span data-stu-id="caafd-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="caafd-125">Utgiftshanteringspolicye utvärderas mot källentiteten som standard.</span><span class="sxs-lookup"><span data-stu-id="caafd-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="caafd-126">För koncerninterna scenarier kan du ange att policyn ska utvärderas mot målentiteten (lånande entitet) i stället.</span><span class="sxs-lookup"><span data-stu-id="caafd-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="caafd-127">Om du vill köra policyer mot målentiteten aktiverar du funktionen **Utvärdera utgiftspolicy mot låntagande juridisk person** på arbetsytan **Funktionshantering**.</span><span class="sxs-lookup"><span data-stu-id="caafd-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="caafd-128">När policyer utvärderas</span><span class="sxs-lookup"><span data-stu-id="caafd-128">When to evaluate policies</span></span>

<span data-ttu-id="caafd-129">I parametrar för utgiftshantering kan du välja om du vill utvärdera policyer för utgiftshantering när en rad sparas eller när en utgiftsrapport skickas.</span><span class="sxs-lookup"><span data-stu-id="caafd-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="caafd-130">Om du väljer att utvärdera när en rad sparas får användarna tidigare insyn i vad de behöver göra för att slutföra sina utgiftsrapporter samtidigt.</span><span class="sxs-lookup"><span data-stu-id="caafd-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="caafd-131">Annars kan du försena utvärdering av policyer och spara tid genom att validera i slutet, under överföringen till arbetsflödet.</span><span class="sxs-lookup"><span data-stu-id="caafd-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
