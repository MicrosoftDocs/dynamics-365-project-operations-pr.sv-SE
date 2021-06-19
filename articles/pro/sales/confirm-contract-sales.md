---
title: Bekräfta ett projektkontrakt
description: I det här ämnet finns information om hur du bekräftar ett kontrakt i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003698"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="a06d9-103">Bekräfta ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a06d9-103">Confirm a project contract</span></span>

<span data-ttu-id="a06d9-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="a06d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a06d9-105">Ett projektkontrakt i Dynamics 365 Project Operations kan vara aktivt på grund av **Bekräftad** eller stängs med orsaken **Förlorad**.</span><span class="sxs-lookup"><span data-stu-id="a06d9-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="a06d9-106">När du bekräftar ett projektkontrakt uppdateras statusen från **Utkast** till **Aktiv** och statusorsaken är **Bekräftat**.</span><span class="sxs-lookup"><span data-stu-id="a06d9-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="a06d9-107">Ett aktivt eller stängt kontrakt kan inte redigeras eller öppnas på nytt.</span><span class="sxs-lookup"><span data-stu-id="a06d9-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="a06d9-108">Ekonomiska följder av att bekräfta ett projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a06d9-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="a06d9-109">När ett projektkontrakt bekräftas omberäknar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och skapa nya faktiska värden för kostnad.</span><span class="sxs-lookup"><span data-stu-id="a06d9-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="a06d9-110">De nya faktiska värdena för kostnad behandlas sedan baserat på den faktureringsmetod som är kopplad till projektkontraktsraden.</span><span class="sxs-lookup"><span data-stu-id="a06d9-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="a06d9-111">Om det faktiska värdet för kostnad refererar till en kontraktrad för tid och material återskapas automatiskt motsvarande ofakturerade faktiska värden för försäljning.</span><span class="sxs-lookup"><span data-stu-id="a06d9-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="a06d9-112">Om det faktiska värdet för kostnad refererar till en kontraktrad för fast pris avbryter programmet ombearbetningen av de faktiska värdena för kostnad.</span><span class="sxs-lookup"><span data-stu-id="a06d9-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="a06d9-113">Gränser som inte får överskridas, konfiguration av debiterbarhet och prissättning och kostnader för de faktiska värdena utvärderas och uppdateras sedan som en del av bekräftelseprocessen.</span><span class="sxs-lookup"><span data-stu-id="a06d9-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="a06d9-114">Stänga ett projektkontrakt som förlorat</span><span class="sxs-lookup"><span data-stu-id="a06d9-114">Close a project contract as lost</span></span>

<span data-ttu-id="a06d9-115">När du stänger ett projektkontrakt som förlorat uppdateras kontraktets status till **Stängt** och statusorsaken är **Förlorat**.</span><span class="sxs-lookup"><span data-stu-id="a06d9-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="a06d9-116">Projektkontraktet blir skrivskyddat.</span><span class="sxs-lookup"><span data-stu-id="a06d9-116">The project contract becomes read-only.</span></span> <span data-ttu-id="a06d9-117">En bekräftelsedialog visas innan ändringarna är slutförda eftersom du inte kan öppna ett stängt projektkontrakt igen.</span><span class="sxs-lookup"><span data-stu-id="a06d9-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="a06d9-118">Om projektkontraktet som stängs som förlorat refererar ett projekt på dess rader markeras det projektet som stängt.</span><span class="sxs-lookup"><span data-stu-id="a06d9-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="a06d9-119">Eventuella resursbokningar från den dagen framåt annulleras.</span><span class="sxs-lookup"><span data-stu-id="a06d9-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="a06d9-120">Eventuella ofakturerade faktiska värden för försäljning i projektkontraktet som inte redan finns på en faktura återförs.</span><span class="sxs-lookup"><span data-stu-id="a06d9-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="a06d9-121">I Dynamics 365 Project Operations om du stänger ett projektkontrakt som förlorat påverkar inte detta status för den associerade affärsmöjligheten.</span><span class="sxs-lookup"><span data-stu-id="a06d9-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="a06d9-122">Affärsmöjligheten förblir öppen och måste stängas manuellt.</span><span class="sxs-lookup"><span data-stu-id="a06d9-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]