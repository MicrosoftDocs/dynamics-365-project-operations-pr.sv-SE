---
title: Intäktsredovisning – Översikt
description: I det här ämnet finns information om vyn intäktsredovisning i Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013778"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="92d26-103">Intäktsredovisning – Översikt</span><span class="sxs-lookup"><span data-stu-id="92d26-103">Revenue recognition overview</span></span>

<span data-ttu-id="92d26-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="92d26-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="92d26-105">I Dynamics 365 Project Operations varierar principerna för intäktsredovisning baserat på den valda faktureringsmetoden för ett projekt eller en del av projektet.</span><span class="sxs-lookup"><span data-stu-id="92d26-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="92d26-106">I det här ämnet finns information om vyn intäktsredovisning i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="92d26-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="92d26-107">Transaktionerna redovisas med hjälp av metoden för fakturering av tid och material</span><span class="sxs-lookup"><span data-stu-id="92d26-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="92d26-108">Kostnads- och intäktsredovisning är anslutna.</span><span class="sxs-lookup"><span data-stu-id="92d26-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="92d26-109">Transaktionskostnad och ej fakturerad försäljning bokförs med hjälp av [integrationsjournal för Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="92d26-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="92d26-110">Projektkostnads- och intäktsprofil avgör om ej fakturerade försäljningstransaktioner bokförs i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="92d26-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="92d26-111">Om **Periodisera intäkter** väljs kommer systemet att använda kontona **Försäljningsvärde för PIA** och **Försäljningsvärde för periodiserade intäkter**.</span><span class="sxs-lookup"><span data-stu-id="92d26-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="92d26-112">Följande är ett exempel på denna metod.</span><span class="sxs-lookup"><span data-stu-id="92d26-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="92d26-113">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="92d26-113">Transaction type</span></span> | <span data-ttu-id="92d26-114">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-114">Debit/Credit</span></span> | <span data-ttu-id="92d26-115">Belopp</span><span class="sxs-lookup"><span data-stu-id="92d26-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="92d26-116">Försäljningsvärde för PIA</span><span class="sxs-lookup"><span data-stu-id="92d26-116">WIP Sales value</span></span> | <span data-ttu-id="92d26-117">Debet</span><span class="sxs-lookup"><span data-stu-id="92d26-117">Debit</span></span> | <span data-ttu-id="92d26-118">100</span><span class="sxs-lookup"><span data-stu-id="92d26-118">100</span></span> |
  | <span data-ttu-id="92d26-119">Försäljningsvärde för periodiserade intäkter</span><span class="sxs-lookup"><span data-stu-id="92d26-119">Accrued revenue sales value</span></span> | <span data-ttu-id="92d26-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-120">Credit</span></span> | <span data-ttu-id="92d26-121">100</span><span class="sxs-lookup"><span data-stu-id="92d26-121">100</span></span> |

- <span data-ttu-id="92d26-122">Intäkter redovisas i samband med fakturering.</span><span class="sxs-lookup"><span data-stu-id="92d26-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="92d26-123">Systemet använder kontot **Fakturerad intäkt** i samband med bokföring.</span><span class="sxs-lookup"><span data-stu-id="92d26-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="92d26-124">Följande är ett exempel på denna metod.</span><span class="sxs-lookup"><span data-stu-id="92d26-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="92d26-125">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="92d26-125">Transaction type</span></span> | <span data-ttu-id="92d26-126">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-126">Debit/Credit</span></span> | <span data-ttu-id="92d26-127">Belopp</span><span class="sxs-lookup"><span data-stu-id="92d26-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="92d26-128">Kundsaldo</span><span class="sxs-lookup"><span data-stu-id="92d26-128">Customer balance</span></span> | <span data-ttu-id="92d26-129">Debet</span><span class="sxs-lookup"><span data-stu-id="92d26-129">Debit</span></span> | <span data-ttu-id="92d26-130">120</span><span class="sxs-lookup"><span data-stu-id="92d26-130">120</span></span> |
  | <span data-ttu-id="92d26-131">Omsättningsskatt</span><span class="sxs-lookup"><span data-stu-id="92d26-131">Sales tax payable</span></span> | <span data-ttu-id="92d26-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-132">Credit</span></span> | <span data-ttu-id="92d26-133">20</span><span class="sxs-lookup"><span data-stu-id="92d26-133">20</span></span> |
  | <span data-ttu-id="92d26-134">Fakturerad intäkt</span><span class="sxs-lookup"><span data-stu-id="92d26-134">Invoiced Revenue</span></span> | <span data-ttu-id="92d26-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-135">Credit</span></span> | <span data-ttu-id="92d26-136">100</span><span class="sxs-lookup"><span data-stu-id="92d26-136">100</span></span> |

- <span data-ttu-id="92d26-137">Om intäkter periodiseras när den ej fakturerade försäljningen bokförs kommer systemet att återföra den periodiserade intäkten vid fakturering.</span><span class="sxs-lookup"><span data-stu-id="92d26-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="92d26-138">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="92d26-138">Transaction type</span></span> | <span data-ttu-id="92d26-139">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-139">Debit/Credit</span></span> | <span data-ttu-id="92d26-140">Belopp</span><span class="sxs-lookup"><span data-stu-id="92d26-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="92d26-141">Försäljningsvärde för PIA</span><span class="sxs-lookup"><span data-stu-id="92d26-141">WIP Sales value</span></span> | <span data-ttu-id="92d26-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="92d26-142">Credit</span></span> | <span data-ttu-id="92d26-143">100</span><span class="sxs-lookup"><span data-stu-id="92d26-143">100</span></span> |
  | <span data-ttu-id="92d26-144">Försäljningsvärde för periodiserade intäkter</span><span class="sxs-lookup"><span data-stu-id="92d26-144">Accrued revenue sales value</span></span> | <span data-ttu-id="92d26-145">Debet</span><span class="sxs-lookup"><span data-stu-id="92d26-145">Debit</span></span> | <span data-ttu-id="92d26-146">100</span><span class="sxs-lookup"><span data-stu-id="92d26-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="92d26-147">Transaktionerna redovisas med hjälp av faktureringsmetoden för fast pris</span><span class="sxs-lookup"><span data-stu-id="92d26-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="92d26-148">Kostnads- och intäktsredovisning är separata.</span><span class="sxs-lookup"><span data-stu-id="92d26-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="92d26-149">Transaktionskostnaden bokförs med hjälp av [integrationsjournalen för Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="92d26-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="92d26-150">Ej fakturerade försäljningstransaktioner skapas inte.</span><span class="sxs-lookup"><span data-stu-id="92d26-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="92d26-151">Intäkter kan redovisas under faktureringen om projektets kostnad och intäktsprofil har **Princip som används för beräkningar av projektslutförande** anges som **Ingen PIA**.</span><span class="sxs-lookup"><span data-stu-id="92d26-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="92d26-152">Använd bara denna metod för enklare, mer kortsiktiga projekt.</span><span class="sxs-lookup"><span data-stu-id="92d26-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="92d26-153">Intäkter kan redovisasmed hjälp av uppskattningar av fastprisintäkter, med antingen metoden **Slutfört kontrakt** eller **Slutförd intäktsredovisning i procent**.</span><span class="sxs-lookup"><span data-stu-id="92d26-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92d26-154">Ytterligare resurser</span><span class="sxs-lookup"><span data-stu-id="92d26-154">Additional resources</span></span>
[<span data-ttu-id="92d26-155">Konfigurera redovisning för fakturerbar projektartikel</span><span class="sxs-lookup"><span data-stu-id="92d26-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="92d26-156">Intäktsberäkningar för fastprisprojekt</span><span class="sxs-lookup"><span data-stu-id="92d26-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="92d26-157">Hantera intäktsberäkningar</span><span class="sxs-lookup"><span data-stu-id="92d26-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="92d26-158">Kostnad för slutförandemetoder</span><span class="sxs-lookup"><span data-stu-id="92d26-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]