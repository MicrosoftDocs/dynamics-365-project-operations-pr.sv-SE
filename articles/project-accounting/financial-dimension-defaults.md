---
title: Standardvärden för ekonomisk dimension
description: I det här ämnet finns information om hur du ställer in standardvärden för ekonomiska dimensioner.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642385"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="03d43-103">Standardvärden för ekonomisk dimension</span><span class="sxs-lookup"><span data-stu-id="03d43-103">Financial dimension defaults</span></span>

<span data-ttu-id="03d43-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="03d43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="03d43-105">Dynamics 365 Project Operations använder ramverket [finansiella dimensioner](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) i Dynamics 365 Finance i syfte att ge ytterligare insikter i projektredovisning och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="03d43-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="03d43-106">Det går att ange ekonomiska standarddimensioner för en kund, projektfinansieringskälla, milstolpe, projektkontraktrad eller projekt.</span><span class="sxs-lookup"><span data-stu-id="03d43-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="03d43-107">Definiera ekonomiska standarddimensioner för en kund</span><span class="sxs-lookup"><span data-stu-id="03d43-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="03d43-108">Standardvärden för kunddimensioner anges i Finance.</span><span class="sxs-lookup"><span data-stu-id="03d43-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="03d43-109">Slutför följande steg för att ställa in standardinställningar.</span><span class="sxs-lookup"><span data-stu-id="03d43-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="03d43-110">Gå till **kundreskontra** > **kunder** > **alla kunder**.</span><span class="sxs-lookup"><span data-stu-id="03d43-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="03d43-111">På sidan **kunder** på fliken **ekonomiska dimensioner** anger du värden för den ekonomiska dimensionen för en specifik kund.</span><span class="sxs-lookup"><span data-stu-id="03d43-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="03d43-112">Definiera ekonomiska standarddimensioner för projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="03d43-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="03d43-113">Projektkontrakt skapas och underhålls i Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="03d43-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="03d43-114">Redovisningsproviders för projektkontrakt anges i modulen **projektledning och redovisning** i Finance.</span><span class="sxs-lookup"><span data-stu-id="03d43-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="03d43-115">Ange ekonomiska dimensioner för en projektfinansieringskälla</span><span class="sxs-lookup"><span data-stu-id="03d43-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="03d43-116">Gå till **Projektledning och redovisning** > **Projekt** > **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="03d43-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="03d43-117">Markera den post du vill uppdatera och på fliken **Projektkontrakt** väljer du **Visa standardredovisning**.</span><span class="sxs-lookup"><span data-stu-id="03d43-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="03d43-118">Visa **Relaterad information** och välj fliken **Finansieringskällor**.</span><span class="sxs-lookup"><span data-stu-id="03d43-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="03d43-119">Ange standardvärden för ekonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="03d43-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="03d43-120">Observera att de ekonomiska dimensionerna standard från kundkontot.</span><span class="sxs-lookup"><span data-stu-id="03d43-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="03d43-121">Ange ekonomiska dimensioner för en projektkontraktrad</span><span class="sxs-lookup"><span data-stu-id="03d43-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="03d43-122">Gå till **Projektledning och redovisning** > **Projekt** > **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="03d43-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="03d43-123">Markera den post du vill uppdatera och på fliken **Projektkontrakt** väljer du **Visa standardredovisning**.</span><span class="sxs-lookup"><span data-stu-id="03d43-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="03d43-124">Visa **Relaterad information** och välj fliken **Kontraktrader**.</span><span class="sxs-lookup"><span data-stu-id="03d43-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="03d43-125">Ange standardvärden för ekonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="03d43-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="03d43-126">De ekonomiska dimensionerna är tillämpliga och kan endast användas med kontraktrader av fast pris (milstolpe).</span><span class="sxs-lookup"><span data-stu-id="03d43-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="03d43-127">Dessa standardvärden används för relaterade a conto-transaktioner och fakturarader.</span><span class="sxs-lookup"><span data-stu-id="03d43-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="03d43-128">Definiera ekonomiska standarddimensioner för projekt</span><span class="sxs-lookup"><span data-stu-id="03d43-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="03d43-129">Projekt skapas och underhålls i CDS.</span><span class="sxs-lookup"><span data-stu-id="03d43-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="03d43-130">Redovisningsproviders för projekt anges i modulen **projektledning och redovisning** i Finance.</span><span class="sxs-lookup"><span data-stu-id="03d43-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="03d43-131">Gå till **projektledning och redovisning** > **projekt** > **alla projekt**.</span><span class="sxs-lookup"><span data-stu-id="03d43-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="03d43-132">Markera den post du vill uppdatera och på fliken **Projekt** väljer du **Visa standardredovisning**.</span><span class="sxs-lookup"><span data-stu-id="03d43-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="03d43-133">Visa **Relaterad information** och välj fliken **Inställning**.</span><span class="sxs-lookup"><span data-stu-id="03d43-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="03d43-134">Ange standardvärden för ekonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="03d43-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="03d43-135">Observera att de ekonomiska dimensionerna standard från kundkontot.</span><span class="sxs-lookup"><span data-stu-id="03d43-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="03d43-136">Om projektet är associerat med en kontraktrad med flera projektkontraktkunder används den primära kunden för att standardisera ekonomiska dimensioner.</span><span class="sxs-lookup"><span data-stu-id="03d43-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="03d43-137">Projektets ekonomiska standarddimensioner används för att ange standard för journalrader för tid-, utgifts- och avgiftstransaktioner i **Project Operations integrationsjournalen** och på relaterade projekt fakturarader.</span><span class="sxs-lookup"><span data-stu-id="03d43-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
