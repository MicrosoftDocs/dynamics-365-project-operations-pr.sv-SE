---
title: Traktamente
description: I det här ämnet finns information om traktamentsregler som används i utgiftshantering.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085414"
---
# <a name="per-diems"></a><span data-ttu-id="91e29-103">Traktamente</span><span class="sxs-lookup"><span data-stu-id="91e29-103">Per diems</span></span>

<span data-ttu-id="91e29-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="91e29-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="91e29-105">Ett traktamente är ett belopp som betalas till en arbetare som reser i arbetet.</span><span class="sxs-lookup"><span data-stu-id="91e29-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="91e29-106">I utgiftshantering kan du skapa traktamentsregler för olika resesituationer.</span><span class="sxs-lookup"><span data-stu-id="91e29-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="91e29-107">Traktamentstaxa kan baseras på tid på året, resmål eller både och.</span><span class="sxs-lookup"><span data-stu-id="91e29-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="91e29-108">När du skapar en traktamentsregel kan du ange att en procentsats av traktamentstaxan ska dras in om en arbetare får gratis måltider eller tjänster.</span><span class="sxs-lookup"><span data-stu-id="91e29-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="91e29-109">Du kan även ange ett minsta och högsta antal timmar som traktamentstaxan kan gälla för en arbetares resa.</span><span class="sxs-lookup"><span data-stu-id="91e29-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="91e29-110">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="91e29-110">Configuration</span></span> 

1. <span data-ttu-id="91e29-111">Om du vill lägga till traktamentsplatser går du till **Konfigurera** > **Beräkningar och koder** > **Traktamentsplatser**.</span><span class="sxs-lookup"><span data-stu-id="91e29-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="91e29-112">För varje plats som läggs till ovan väljer du en traktamentstaxa och en valuta som är giltig mellan ett specifikt start- och slutdatum för hotell, måltider och andra utgifter.</span><span class="sxs-lookup"><span data-stu-id="91e29-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="91e29-113">Traktamentstaxa och valutor konfigureras under **Konfigurera** > **Beräkningar och koder** > **Traktamente**.</span><span class="sxs-lookup"><span data-stu-id="91e29-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="91e29-114">På sidan **Traktamentsplatser** konfigurerar du nivåer av traktamentstaxa.</span><span class="sxs-lookup"><span data-stu-id="91e29-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="91e29-115">Med nivåerna av traktamentstaxa kan du definiera procentandelen av en daglig ersättning för hotell, måltider och andra utgifter.</span><span class="sxs-lookup"><span data-stu-id="91e29-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="91e29-116">Om du vill ange reducering av procentandel för frukost, lunch eller middag, uppdaterar du fälten på sidan **Parametrar för utgiftshantering** under fliken **Traktamente**.</span><span class="sxs-lookup"><span data-stu-id="91e29-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="91e29-117">Skicka utgifter med traktamente</span><span class="sxs-lookup"><span data-stu-id="91e29-117">Submit expenses using per diem</span></span>
<span data-ttu-id="91e29-118">Om du vill skicka in utgifter med traktamente använder du utgiftskategorin **Traktamente** när du skapar en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="91e29-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="91e29-119">Ange **Traktamente från datum** , **Traktamente till datum** och **Traktementsplats**.</span><span class="sxs-lookup"><span data-stu-id="91e29-119">Enter the **Per diem from date** , **Per diem to date** ,  and the **Per diem location**.</span></span> <span data-ttu-id="91e29-120">Beloppet beräknas utifrån traktamentstaxan för den valda platsen och måltidsminskningen beräknas baserat på nivåerna av traktamentstaxa.</span><span class="sxs-lookup"><span data-stu-id="91e29-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
