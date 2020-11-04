---
title: Reserekvisitioner
description: I det här ämnet finns information om reserekvisitioner.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085409"
---
# <a name="travel-requisitions"></a><span data-ttu-id="cdb5a-103">Reserekvisitioner</span><span class="sxs-lookup"><span data-stu-id="cdb5a-103">Travel requisitions</span></span>

<span data-ttu-id="cdb5a-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="cdb5a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cdb5a-105">En reserekvisition visar de utgifter som uppstår i samband med resan.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="cdb5a-106">En reserekvisition skickas för granskning och kan användas för att godkänna utgifter.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="cdb5a-107">Du kan behöva skicka in en reserekvisition innan du ådrar dig kostnader som debiteras organisationen.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="cdb5a-108">Detta krav gäller oavsett om du debiterar utgifter till ett företags kreditkort, spenderar pengar som du erhåller från ett förskott eller ådrar dig utgifter som inte kommer att betalas tillbaka av företaget.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="cdb5a-109">Reserekvisitioner och principer kan användas för att hantera organisationens utgifter.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="cdb5a-110">Om din organisation till exempel arbetar med ett fastprisprojekt som kräver resa, måste reseutgifterna för projektets teammedlemmar passa i projektbudgeten.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="cdb5a-111">Genom att kräva att resekostnaderna godkänns innan de uppkommer kan organisationen se till att projektet förblir inom budgeten.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="cdb5a-112">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="cdb5a-112">Configuration</span></span> 

<span data-ttu-id="cdb5a-113">Reserekvisitioner kan konfigureras som "obligatoriska" genom att aktivera parametern "Förauktorisering av resa är obligatorisk" i utgiftshanteringsparametrar.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="cdb5a-114">Skapa och skicka en reserekvisition</span><span class="sxs-lookup"><span data-stu-id="cdb5a-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="cdb5a-115">Gå till **Mina utgifter: reserekvisition** och välj **Ny reserekvisition**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="cdb5a-116">Ange ett syfte och en destination för rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="cdb5a-117">I fältet **Resebeskrivning** anger du eventuell ytterligare information.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="cdb5a-118">För var och en av de förväntade kostnaderna, t.ex. flyg, måltider och hyrbil, skapar du en utgiftsradartikel.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="cdb5a-119">Ange uppskattat datum, uppskattat belopp och valuta för varje utgift.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="cdb5a-120">När du har lagt till de förväntade utgifterna väljer du **Spara**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="cdb5a-121">När du är klar att skicka reserekvisitionen väljer du **Arbetsflöde** > **Skicka**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="cdb5a-122">Du kan visa godkända reserekvisitioner under **Mina utgifter: reserekvisition**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="cdb5a-123">Visa tillgängliga reserekvisitioner</span><span class="sxs-lookup"><span data-stu-id="cdb5a-123">View available travel requisitions</span></span>

<span data-ttu-id="cdb5a-124">Du kan visa alla dina godkända reserekvisitioner under **Mina utgifter: reserekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="cdb5a-125">Godkänn reserekvisitioner</span><span class="sxs-lookup"><span data-stu-id="cdb5a-125">Approve travel requisitions</span></span>

<span data-ttu-id="cdb5a-126">Välj den reserekvisition som du vill godkänna och välj sedan **Arbetsflöde** > **Godkänn**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="cdb5a-127">Skicka in en utgiftsrapport med hjälp av en godkänd reserekvisition</span><span class="sxs-lookup"><span data-stu-id="cdb5a-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="cdb5a-128">Skapa en ny utgiftsrapport och i rubriken för utgiftsrapporten, och från listan över godkända reserekvisitioner, väljer du **Mappa till reserekvisition**.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="cdb5a-129">Fältet **Reserekvisitionsbelopp** uppdateras automatiskt i utgiftsrapportrubriken.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="cdb5a-130">Lägg till alla utgifter som uppstår för resan.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="cdb5a-131">Om fältet **Förauktoriserad** är aktiverat uppdateras avstämt belopp och godkänt belopp för den angivna utgiftskategorin.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="cdb5a-132">När du mappar en utgiftsrapport till en godkänd reserekvisition får transaktionsbeloppet inte vara större än det godkända beloppet.</span><span class="sxs-lookup"><span data-stu-id="cdb5a-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
