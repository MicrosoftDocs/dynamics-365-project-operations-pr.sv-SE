---
title: Stänga en offert - lite
description: I det här ämnet finns information om hur du stänger en offert i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994158"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="de96c-103">Stänga en offert - lite</span><span class="sxs-lookup"><span data-stu-id="de96c-103">Close a quote - lite</span></span>

<span data-ttu-id="de96c-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="de96c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de96c-105">En projektoffert kan stängas som Vunnen eller Förlorad.</span><span class="sxs-lookup"><span data-stu-id="de96c-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="de96c-106">Ett offertutkast kan komma att stängas eftersom aktiverings- och ändringsåtgärder för offerter inte stöds i Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="de96c-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="de96c-107">Stänga en offert som Vunnen</span><span class="sxs-lookup"><span data-stu-id="de96c-107">Close a quote as Won</span></span>

<span data-ttu-id="de96c-108">När du stänger en projektoffert som "Vunnen" får den statusen "Stängd" och statusorsaken "Vunnen".</span><span class="sxs-lookup"><span data-stu-id="de96c-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="de96c-109">Om du stänger offerten blir projektofferten skrivskyddad och ett utkast skapas i ett projektkontrakt som innehåller offertinformationen.</span><span class="sxs-lookup"><span data-stu-id="de96c-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="de96c-110">Eftersom en stängd offert inte kan öppnas på nytt kommer en bekräftelsedialog att bekräfta dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="de96c-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="de96c-111">Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.</span><span class="sxs-lookup"><span data-stu-id="de96c-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="de96c-112">Ekonomiska följder av att stänga en offert som Vunnen</span><span class="sxs-lookup"><span data-stu-id="de96c-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="de96c-113">Om några faktiska värden för tid i ett projekt fortfarande är kopplade till ett offertutkast, registreras endast kostnaden för tid eller utgifter.</span><span class="sxs-lookup"><span data-stu-id="de96c-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="de96c-114">När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad.</span><span class="sxs-lookup"><span data-stu-id="de96c-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="de96c-115">Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktraden.</span><span class="sxs-lookup"><span data-stu-id="de96c-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="de96c-116">Om kostnadens faktiska värden refererar till en tids- och materialkontraktrad, skapas motsvarande icke-fakturerade försäljningsfakturerade faktiska värden när offerten stängs och projektkontraktet skapas.</span><span class="sxs-lookup"><span data-stu-id="de96c-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="de96c-117">Om de faktiska kostnaderna refererar till en kontraktrad med fast pris, kommer programmet att sluta bearbeta om de faktiska kostnader som bygger på delningsfaktureringsregler för projektkontraktskunderna.</span><span class="sxs-lookup"><span data-stu-id="de96c-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="de96c-118">Stänga en offert som förlorad:</span><span class="sxs-lookup"><span data-stu-id="de96c-118">Closing a quote as lost:</span></span>

<span data-ttu-id="de96c-119">När du stänger en projektoffert som "Förlorad" får den statusen "Stängd" och statusorsaken "Förlorad".</span><span class="sxs-lookup"><span data-stu-id="de96c-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="de96c-120">Om du stänger offerten blir projektofferten skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="de96c-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="de96c-121">Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.</span><span class="sxs-lookup"><span data-stu-id="de96c-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="de96c-122">Om projektofferten som har stängts som Förlorad refererar till ett projekt på någon av raderna markeras det också som Stängt.</span><span class="sxs-lookup"><span data-stu-id="de96c-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="de96c-123">Eventuella resursbokningar från den dagen framåt annulleras.</span><span class="sxs-lookup"><span data-stu-id="de96c-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="de96c-124">När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.</span><span class="sxs-lookup"><span data-stu-id="de96c-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]