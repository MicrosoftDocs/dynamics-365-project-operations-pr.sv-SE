---
title: Traktamente
description: I det här ämnet finns information om traktamentsregler som används i utgiftshantering.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276325"
---
# <a name="per-diems"></a><span data-ttu-id="5ed7c-103">Traktamente</span><span class="sxs-lookup"><span data-stu-id="5ed7c-103">Per diems</span></span>

<span data-ttu-id="5ed7c-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="5ed7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="5ed7c-105">Ett traktamente är ett belopp som betalas till en arbetare som reser i arbetet.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="5ed7c-106">I utgiftshantering kan du skapa traktamentsregler för olika resesituationer.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="5ed7c-107">Traktamentstaxa kan baseras på tid på året, resmål eller både och.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5ed7c-108">När du skapar en traktamentsregel kan du ange att en procentsats av traktamentstaxan ska dras in om en arbetare får gratis måltider eller tjänster.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5ed7c-109">Du kan även ange ett minsta och högsta antal timmar som traktamentstaxan kan gälla för en arbetares resa.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="5ed7c-110">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="5ed7c-110">Configuration</span></span> 

1. <span data-ttu-id="5ed7c-111">Om du vill lägga till traktamentsplatser går du till **Konfigurera** > **Beräkningar och koder** > **Traktamentsplatser**.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="5ed7c-112">För varje plats som läggs till ovan väljer du en traktamentstaxa och en valuta som är giltig mellan ett specifikt start- och slutdatum för hotell, måltider och andra utgifter.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="5ed7c-113">Traktamentstaxa och valutor konfigureras under **Konfigurera** > **Beräkningar och koder** > **Traktamente**.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="5ed7c-114">På sidan **Traktamentsplatser** konfigurerar du nivåer av traktamentstaxa.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="5ed7c-115">Med nivåerna av traktamentstaxa kan du definiera procentandelen av en daglig ersättning för hotell, måltider och andra utgifter.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="5ed7c-116">Om du vill ange reducering av procentandel för frukost, lunch eller middag, uppdaterar du fälten på sidan **Parametrar för utgiftshantering** under fliken **Traktamente**.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="5ed7c-117">Skicka utgifter med traktamente</span><span class="sxs-lookup"><span data-stu-id="5ed7c-117">Submit expenses using per diem</span></span>
<span data-ttu-id="5ed7c-118">Om du vill skicka in utgifter med traktamente använder du utgiftskategorin **Traktamente** när du skapar en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="5ed7c-119">Ange **Traktamente från datum**, **Traktamente till datum** och **Traktementsplats**.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="5ed7c-120">Beloppet beräknas utifrån traktamentstaxan för den valda platsen och måltidsminskningen beräknas baserat på nivåerna av traktamentstaxa.</span><span class="sxs-lookup"><span data-stu-id="5ed7c-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]