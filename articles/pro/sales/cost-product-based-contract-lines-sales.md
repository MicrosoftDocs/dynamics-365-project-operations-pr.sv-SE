---
title: Kostnads- produktbaserade kontraktrader - lite
description: I det här ämnet finns information om hur du skapar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003563"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="16dd7-103">Kostnads- produktbaserade kontraktrader - lite</span><span class="sxs-lookup"><span data-stu-id="16dd7-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="16dd7-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="16dd7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="16dd7-105">Produktbaserade kontraktrader Dynamics 365 Project Operations inkluderar fältet **Självkostnad**, som lagrar självkostnadspriset för produkten för lönsamhetsberäkningar i efterföljande led.</span><span class="sxs-lookup"><span data-stu-id="16dd7-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="16dd7-106">När en produktbaserad kontraktrad skapas för en katalogprodukt utgår radkostnaden från fältet **Standardkostnad** i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="16dd7-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="16dd7-107">Fältet **Standardkostnad** i produktkatalogen är konfigurerat i organisationens basvaluta.</span><span class="sxs-lookup"><span data-stu-id="16dd7-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="16dd7-108">När styckkostnaden används på kontraktraden konverteras den till försäljningsvalutan i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="16dd7-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="16dd7-109">Styckkostnad på en produktbaserad kontraktrad</span><span class="sxs-lookup"><span data-stu-id="16dd7-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="16dd7-110">Syftet med en styckkostnad på en produktbaserad kontraktrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning av en enhet.</span><span class="sxs-lookup"><span data-stu-id="16dd7-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="16dd7-111">Om du inte alltid behöver det finns vissa scenarier där kostnaden för produkten kan rabatteras av leverantören.</span><span class="sxs-lookup"><span data-stu-id="16dd7-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="16dd7-112">Föreställ dig följande scenario:</span><span class="sxs-lookup"><span data-stu-id="16dd7-112">Consider the following scenario:</span></span>

<span data-ttu-id="16dd7-113">Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer.</span><span class="sxs-lookup"><span data-stu-id="16dd7-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="16dd7-114">Fabrikam tillhandahåller installationstjänster, men robotarmarna är från Trey Research.</span><span class="sxs-lookup"><span data-stu-id="16dd7-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="16dd7-115">Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Trey Research, kan de ge Fabrikam en särskild rabatt för den här affären.</span><span class="sxs-lookup"><span data-stu-id="16dd7-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="16dd7-116">I det här fallet skapar Fabrikam en produktbaserad kontraktrad för Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="16dd7-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="16dd7-117">En kostnad per enhet anges för detta kontrakt.</span><span class="sxs-lookup"><span data-stu-id="16dd7-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="16dd7-118">Kostnaden skiljer sig från kostnaden för robotarmar från Trey Research.</span><span class="sxs-lookup"><span data-stu-id="16dd7-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]