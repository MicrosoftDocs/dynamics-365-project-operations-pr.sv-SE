---
title: Produktbaserade kontraktrader för kostnadsredovisning
description: I det här ämnet finns information om hur du skapar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4085771"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="97da6-103">Produktbaserade kontraktrader för kostnadsredovisning</span><span class="sxs-lookup"><span data-stu-id="97da6-103">Costing product-based contract lines</span></span>

<span data-ttu-id="97da6-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="97da6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="97da6-105">Produktbaserade kontraktrader i Dynamics 365 Project Operations inkluderar fältet **Självkostnad** , som lagrar produktens självkostnad för beräkningar av vinsten.</span><span class="sxs-lookup"><span data-stu-id="97da6-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="97da6-106">När en produktbaserad kontraktrad skapas för en katalogprodukt används kostnaden för den produktbaserade kontraktraden från fältet **Standardkostnad** i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="97da6-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="97da6-107">Fältet **Standardkostnad** i produktkatalogen är konfigurerat i organisationens basvaluta.</span><span class="sxs-lookup"><span data-stu-id="97da6-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="97da6-108">När styckkostnaden används på kontraktraden konverteras den till försäljningsvalutan i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="97da6-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="97da6-109">Styckkostnad på en produktbaserad kontraktrad</span><span class="sxs-lookup"><span data-stu-id="97da6-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="97da6-110">Syftet med en styckkostnad på en produktbaserad kontraktrad är att det ska vara möjligt att använda olika kostnader för en produkt för varje försäljning av en enhet.</span><span class="sxs-lookup"><span data-stu-id="97da6-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="97da6-111">Om du inte alltid behöver det finns vissa scenarier där kostnaden för produkten kan rabatteras av leverantören.</span><span class="sxs-lookup"><span data-stu-id="97da6-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="97da6-112">Föreställ dig följande scenario:</span><span class="sxs-lookup"><span data-stu-id="97da6-112">Consider the following scenario:</span></span>

<span data-ttu-id="97da6-113">Fabrikam Robotics installerar robotarmar på Adatum Corporations monteringslinjer.</span><span class="sxs-lookup"><span data-stu-id="97da6-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="97da6-114">Fabrikam tillhandahåller installationstjänster, men robotarmarna anskaffas från Trey Research.</span><span class="sxs-lookup"><span data-stu-id="97da6-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="97da6-115">Om installationen av robotarmar på Adatum Corporation öppnar en ny bransch vertikalt för Trey Research, kan de ge Fabrikam en särskild rabatt för den här affären.</span><span class="sxs-lookup"><span data-stu-id="97da6-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="97da6-116">I det här fallet skapar Fabrikam en produktbaserad kontraktrad för robotarmar och inför ett styckpris för det här kontraktet som skiljer sig från standardkostnaden för robotarmar från Trey Research.</span><span class="sxs-lookup"><span data-stu-id="97da6-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
