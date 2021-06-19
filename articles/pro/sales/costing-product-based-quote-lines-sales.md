---
title: Produktbaserade offertrader för kostnadsredovisning
description: I det här ämnet finns information om hur man lägger till en självkostnad på en produktbaserad offertrad.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003473"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="d6f3c-103">Produktbaserade offertrader för kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="d6f3c-103">Costing product-based quote lines</span></span>

<span data-ttu-id="d6f3c-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="d6f3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d6f3c-105">Produktbaserade offertrader i Dynamics 365 Project Operations har även fältet **självkostnad**.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="d6f3c-106">Det här fältet används för att spåra självkostnaden för produkten på offertraden och för vinstberäkningarna nedströms.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="d6f3c-107">När en produktbaserad offertrad skapas för en katalogprodukt används kostnaden för den produktbaserade offertraden från fältet **Standardkostnad** i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="d6f3c-108">Standardkostnadsfältet i produktkatalogen är konfigurerat i organisationens basvaluta.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="d6f3c-109">Standardstyckkostnaden på den produktbaserade offertraden omvandlas till försäljningsvalutan i offerten.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="d6f3c-110">Styckkostnad på en produktbaserad offertrad</span><span class="sxs-lookup"><span data-stu-id="d6f3c-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="d6f3c-111">Syftet med en styckkostnad på en produktbaserad offertrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="d6f3c-112">Detta är inte ett typiskt scenario, men ibland kan kostnaden för produkten rabatteras av leverantören, beroende på vilken kund som genomför det slutliga köpet.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="d6f3c-113">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d6f3c-113">For example:</span></span>

<span data-ttu-id="d6f3c-114">Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="d6f3c-115">Fabrikam tillhandahåller installationstjänster, men robotarmarna anskaffas från Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="d6f3c-116">Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Treys robotarmar, kan Trey ge Fabrikam en särskild rabatt för den här affären.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="d6f3c-117">I det här fallet skapas en produktbaserad offertrad för robotarmar och du kan ange en särskild styckkostnad för offerten.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="d6f3c-118">Den här kostnaden skiljer sig från standardkostnaden för Treys robotarmar.</span><span class="sxs-lookup"><span data-stu-id="d6f3c-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]