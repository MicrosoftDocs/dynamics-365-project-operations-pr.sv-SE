---
title: Granska förhandsgranskningen av faktureringen i projekt och projektkontrakt
description: I det här ämnet finns information om hur du granskar tids-, utgifts- och produkteftersläpningar och hur du markerar dem som klara för fakturering.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bcdcc0cae06ce61bd582d56a8398e718051ff564
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123985"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="51075-103">Granska förhandsgranskningen av faktureringen i projekt och projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="51075-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="51075-104">När en transaktion är klar för att en faktura ska skapas och bearbetas ska transaktionen vara **klar att fakturera**.</span><span class="sxs-lookup"><span data-stu-id="51075-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="51075-105">I det här ämnet beskrivs typerna av transaktioner som kan skapas.</span><span class="sxs-lookup"><span data-stu-id="51075-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="51075-106">Granska eftersläpning för fakturering av tid och material</span><span class="sxs-lookup"><span data-stu-id="51075-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="51075-107">När en tids- eller utgiftspost skickas och godkänns för ett projekt skapar PSA ett faktiskt projektvärde.</span><span class="sxs-lookup"><span data-stu-id="51075-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="51075-108">Om kombinationen av projektet och transaktionsklassen är mappad till en kontraktrad för ett tids- och materialprojekt, skapas två faktiska värden när posten godkänns:</span><span class="sxs-lookup"><span data-stu-id="51075-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="51075-109">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="51075-109">Cost actual</span></span> 
- <span data-ttu-id="51075-110">Ofakturerad faktisk försäljning</span><span class="sxs-lookup"><span data-stu-id="51075-110">Unbilled sales actual</span></span>

<span data-ttu-id="51075-111">Fakturerade försäljningsvärden representerar eftersläpad fakturering och deras faktureringsstatus måste anges som **klar för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="51075-112">När en projektfaktura skapas kopieras automatiskt fakturerade försäljningsvärden som är markerade **att faktureras** som fakturaradinformation.</span><span class="sxs-lookup"><span data-stu-id="51075-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="51075-113">Om du vill granska eftersläpad fakturering för tid och material, gå till **försäljning** \> **fakturering** \> **Eftersläpad fakturering av tid och material**.</span><span class="sxs-lookup"><span data-stu-id="51075-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="51075-114">Markera alla faktiska värden för ofakturerad försäljning som är klara för fakturering och välj sedan **klar för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="51075-115">Faktureringsstatusen för dessa verkliga värden ändras till **klart för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Eftersläpad fakturering av tid och material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="51075-117">Granska eftersläpad produktfakturering</span><span class="sxs-lookup"><span data-stu-id="51075-117">Review the product billing backlog</span></span>

<span data-ttu-id="51075-118">När ett projektkontrakt har produktbaserade kontraktrader beaktas de i PSA för fakturering när en faktura skapas för projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="51075-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="51075-119">Alla produkter som har kontraktrader som är markerade **Klar att fakturera** kopieras till projektfakturan som projektfakturarader.</span><span class="sxs-lookup"><span data-stu-id="51075-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="51075-120">Om du vill granska eftersläpad fakturering av produkter, gå till **Försäljning** \> **Fakturering** \> **Eftersläpad produktfakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="51075-121">Markera alla produktbaserade kontraktrader som är klara för fakturering och välj sedan **klar för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="51075-122">Faktureringsstatusen för dessa rader ändras till **klart för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Eftersläpad produktfakturering](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="51075-124">Granska faktureringsmilstolpar i kontrakt med fast pris</span><span class="sxs-lookup"><span data-stu-id="51075-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="51075-125">Varje projektkontraktrad som har faktureringsmetod med fast pris måste definiera kontraktmilstolpar.</span><span class="sxs-lookup"><span data-stu-id="51075-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="51075-126">De här kontraktsmilstolparna kan endast faktureras om de har markerats **Klar att fakturera**.</span><span class="sxs-lookup"><span data-stu-id="51075-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="51075-127">Om du vill granska faktureringsmilstolpar går du **försäljning** \> **fakturering** \> **milstolpar med fast pris**.</span><span class="sxs-lookup"><span data-stu-id="51075-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="51075-128">Markera alla milstolpar för ofakturerad försäljning som är klara för fakturering och välj sedan **klar för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="51075-129">Faktureringsstatusen för dessa milstolpar ändras till **klart för fakturering**.</span><span class="sxs-lookup"><span data-stu-id="51075-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Milstolpar med fast pris](media/FPBacklog.png)
