---
title: Konfigurera redovisning för interna projekt
description: I det här ämnet finns information om hur du konfigurerar redovisningspraxis för interna projekt i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858000"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="43b47-103">Konfigurera redovisning för interna projekt</span><span class="sxs-lookup"><span data-stu-id="43b47-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="43b47-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="43b47-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="43b47-105">Med interna projekt kan företag spåra kostnader som är relaterade till aktiviteter som inte debiteras en kund.</span><span class="sxs-lookup"><span data-stu-id="43b47-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="43b47-106">Exempel på interna projekt är:</span><span class="sxs-lookup"><span data-stu-id="43b47-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="43b47-107">Utveckla en produkt, t.ex. en mobilapp, och spåra kostnaden för utvecklingen.</span><span class="sxs-lookup"><span data-stu-id="43b47-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="43b47-108">Hantera tid och utgifter före köpet.</span><span class="sxs-lookup"><span data-stu-id="43b47-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="43b47-109">Det här interna projektet före försäljning kan konverteras till ett fakturerbart projekt om offerten vinns.</span><span class="sxs-lookup"><span data-stu-id="43b47-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="43b47-110">Ett projekt som inte är associerat med ett kontrakt i Dynamics 365 Project Operations behandlas som internt.</span><span class="sxs-lookup"><span data-stu-id="43b47-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="43b47-111">Projektkostnad och intäktsprofiler används inte för att bestämma redovisningsreglerna för projektet.</span><span class="sxs-lookup"><span data-stu-id="43b47-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="43b47-112">Intern projektkostnad bokförs alltid med vinst och förlust-principer.</span><span class="sxs-lookup"><span data-stu-id="43b47-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="43b47-113">Redovisningskonton för bokföringar definieras på sidan **Bokföringsinställningar för transaktionsregister**.</span><span class="sxs-lookup"><span data-stu-id="43b47-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="43b47-114">Tidstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera kontot **Löneallokering**.</span><span class="sxs-lookup"><span data-stu-id="43b47-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="43b47-115">Utgiftstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera **motkonto för utgift**.</span><span class="sxs-lookup"><span data-stu-id="43b47-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="43b47-116">Artikeltransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera kontot **Kostnad - artikel**.</span><span class="sxs-lookup"><span data-stu-id="43b47-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="43b47-117">När transaktioner har bokförts i projektet, om projektet är associerat med ett projektkontrakt, kommer systemet att återföra alla ackumulerade transaktioner och skapa nya fakturerbara transaktioner.</span><span class="sxs-lookup"><span data-stu-id="43b47-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="43b47-118">De fakturerbara transaktionerna följer redovisningsreglerna som har definierats i respektive projektkostnads- och intäktsprofil.</span><span class="sxs-lookup"><span data-stu-id="43b47-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
