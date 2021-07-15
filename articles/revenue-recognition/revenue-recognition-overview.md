---
title: Intäktsredovisning – Översikt
description: I det här ämnet finns information om vyn intäktsredovisning i Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368048"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="35ee2-103">Intäktsredovisning – Översikt</span><span class="sxs-lookup"><span data-stu-id="35ee2-103">Revenue recognition overview</span></span>

<span data-ttu-id="35ee2-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="35ee2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="35ee2-105">I Dynamics 365 Project Operations varierar principerna för intäktsredovisning baserat på den valda faktureringsmetoden för ett projekt eller en del av projektet.</span><span class="sxs-lookup"><span data-stu-id="35ee2-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="35ee2-106">I det här ämnet finns information om vyn intäktsredovisning i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="35ee2-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="35ee2-107">Transaktionerna redovisas med hjälp av metoden för fakturering av tid och material</span><span class="sxs-lookup"><span data-stu-id="35ee2-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="35ee2-108">Kostnads- och intäktsredovisning är anslutna.</span><span class="sxs-lookup"><span data-stu-id="35ee2-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="35ee2-109">Transaktionskostnad och ej fakturerad försäljning bokförs med hjälp av [integrationsjournal för Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="35ee2-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="35ee2-110">Projektkostnads- och intäktsprofil avgör om ej fakturerade försäljningstransaktioner bokförs i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="35ee2-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="35ee2-111">Om **Periodisera intäkter** väljs kommer systemet att använda kontona **Försäljningsvärde för PIA** och **Försäljningsvärde för periodiserade intäkter**.</span><span class="sxs-lookup"><span data-stu-id="35ee2-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="35ee2-112">Följande är ett exempel på denna metod.</span><span class="sxs-lookup"><span data-stu-id="35ee2-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="35ee2-113">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="35ee2-113">Transaction type</span></span> | <span data-ttu-id="35ee2-114">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-114">Debit/Credit</span></span> | <span data-ttu-id="35ee2-115">Belopp</span><span class="sxs-lookup"><span data-stu-id="35ee2-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="35ee2-116">Försäljningsvärde för PIA</span><span class="sxs-lookup"><span data-stu-id="35ee2-116">WIP Sales value</span></span> | <span data-ttu-id="35ee2-117">Debet</span><span class="sxs-lookup"><span data-stu-id="35ee2-117">Debit</span></span> | <span data-ttu-id="35ee2-118">100</span><span class="sxs-lookup"><span data-stu-id="35ee2-118">100</span></span> |
  | <span data-ttu-id="35ee2-119">Försäljningsvärde för periodiserade intäkter</span><span class="sxs-lookup"><span data-stu-id="35ee2-119">Accrued revenue sales value</span></span> | <span data-ttu-id="35ee2-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-120">Credit</span></span> | <span data-ttu-id="35ee2-121">100</span><span class="sxs-lookup"><span data-stu-id="35ee2-121">100</span></span> |

- <span data-ttu-id="35ee2-122">Intäkter redovisas i samband med fakturering.</span><span class="sxs-lookup"><span data-stu-id="35ee2-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="35ee2-123">Systemet använder kontot **Fakturerad intäkt** i samband med bokföring.</span><span class="sxs-lookup"><span data-stu-id="35ee2-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="35ee2-124">Följande är ett exempel på denna metod.</span><span class="sxs-lookup"><span data-stu-id="35ee2-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="35ee2-125">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="35ee2-125">Transaction type</span></span> | <span data-ttu-id="35ee2-126">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-126">Debit/Credit</span></span> | <span data-ttu-id="35ee2-127">Belopp</span><span class="sxs-lookup"><span data-stu-id="35ee2-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="35ee2-128">Kundsaldo</span><span class="sxs-lookup"><span data-stu-id="35ee2-128">Customer balance</span></span> | <span data-ttu-id="35ee2-129">Debet</span><span class="sxs-lookup"><span data-stu-id="35ee2-129">Debit</span></span> | <span data-ttu-id="35ee2-130">120</span><span class="sxs-lookup"><span data-stu-id="35ee2-130">120</span></span> |
  | <span data-ttu-id="35ee2-131">Omsättningsskatt</span><span class="sxs-lookup"><span data-stu-id="35ee2-131">Sales tax payable</span></span> | <span data-ttu-id="35ee2-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-132">Credit</span></span> | <span data-ttu-id="35ee2-133">20</span><span class="sxs-lookup"><span data-stu-id="35ee2-133">20</span></span> |
  | <span data-ttu-id="35ee2-134">Fakturerad intäkt</span><span class="sxs-lookup"><span data-stu-id="35ee2-134">Invoiced Revenue</span></span> | <span data-ttu-id="35ee2-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-135">Credit</span></span> | <span data-ttu-id="35ee2-136">100</span><span class="sxs-lookup"><span data-stu-id="35ee2-136">100</span></span> |

- <span data-ttu-id="35ee2-137">Om intäkter periodiseras när den ej fakturerade försäljningen bokförs kommer systemet att återföra den periodiserade intäkten vid fakturering.</span><span class="sxs-lookup"><span data-stu-id="35ee2-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="35ee2-138">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="35ee2-138">Transaction type</span></span> | <span data-ttu-id="35ee2-139">Debet/kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-139">Debit/Credit</span></span> | <span data-ttu-id="35ee2-140">Belopp</span><span class="sxs-lookup"><span data-stu-id="35ee2-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="35ee2-141">Försäljningsvärde för PIA</span><span class="sxs-lookup"><span data-stu-id="35ee2-141">WIP Sales value</span></span> | <span data-ttu-id="35ee2-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="35ee2-142">Credit</span></span> | <span data-ttu-id="35ee2-143">100</span><span class="sxs-lookup"><span data-stu-id="35ee2-143">100</span></span> |
  | <span data-ttu-id="35ee2-144">Försäljningsvärde för periodiserade intäkter</span><span class="sxs-lookup"><span data-stu-id="35ee2-144">Accrued revenue sales value</span></span> | <span data-ttu-id="35ee2-145">Debet</span><span class="sxs-lookup"><span data-stu-id="35ee2-145">Debit</span></span> | <span data-ttu-id="35ee2-146">100</span><span class="sxs-lookup"><span data-stu-id="35ee2-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="35ee2-147">Transaktionerna redovisas med hjälp av faktureringsmetoden för fast pris</span><span class="sxs-lookup"><span data-stu-id="35ee2-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="35ee2-148">Kostnads- och intäktsredovisning är separata.</span><span class="sxs-lookup"><span data-stu-id="35ee2-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="35ee2-149">Transaktionskostnaden bokförs med hjälp av [integrationsjournalen för Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="35ee2-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="35ee2-150">Ej fakturerade försäljningstransaktioner skapas inte.</span><span class="sxs-lookup"><span data-stu-id="35ee2-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="35ee2-151">Intäkter kan redovisas under faktureringen om projektets kostnad och intäktsprofil har **Princip som används för beräkningar av projektslutförande** anges som **Ingen PIA**.</span><span class="sxs-lookup"><span data-stu-id="35ee2-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="35ee2-152">Använd bara denna metod för enklare, mer kortsiktiga projekt.</span><span class="sxs-lookup"><span data-stu-id="35ee2-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="35ee2-153">Intäkter kan redovisasmed hjälp av uppskattningar av fastprisintäkter, med antingen metoden **Slutfört kontrakt** eller **Slutförd intäktsredovisning i procent**.</span><span class="sxs-lookup"><span data-stu-id="35ee2-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35ee2-154">Ytterligare resurser</span><span class="sxs-lookup"><span data-stu-id="35ee2-154">Additional resources</span></span>
[<span data-ttu-id="35ee2-155">Konfigurera redovisning för fakturerbar projektartikel</span><span class="sxs-lookup"><span data-stu-id="35ee2-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="35ee2-156">Intäktsberäkningar för fastprisprojekt</span><span class="sxs-lookup"><span data-stu-id="35ee2-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="35ee2-157">Hantera intäktsberäkningar</span><span class="sxs-lookup"><span data-stu-id="35ee2-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="35ee2-158">Kostnad för slutförandemetoder</span><span class="sxs-lookup"><span data-stu-id="35ee2-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]