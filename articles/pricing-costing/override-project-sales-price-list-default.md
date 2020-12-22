---
title: Åsidosätt projektförsäljningsprislistor
description: I det här ämnet finns information om hur du skapar anpassade försäljningsprislistor.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672253"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="369fa-103">Åsidosätt projektförsäljningsprislistor</span><span class="sxs-lookup"><span data-stu-id="369fa-103">Override project sales price lists</span></span>

<span data-ttu-id="369fa-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="369fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="369fa-105">Kundspecifika projektprislistor</span><span class="sxs-lookup"><span data-stu-id="369fa-105">Customer-specific project price lists</span></span>

<span data-ttu-id="369fa-106">Kundspecifika prisavtal kan anges som projektprislistor för en kontopost i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="369fa-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="369fa-107">Om du vill skapa en kundspecifik projektprislista i området **försäljning** navigerar du till kontoposten.</span><span class="sxs-lookup"><span data-stu-id="369fa-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="369fa-108">Öppna listsidan **Konton**.</span><span class="sxs-lookup"><span data-stu-id="369fa-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="369fa-109">Leta upp och dubbelklicka på en kundpost om du vill öppna informationssidan **konto**.</span><span class="sxs-lookup"><span data-stu-id="369fa-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="369fa-110">I fliken **Projektprislistor** väljer du **+ Ny projektprislista**.</span><span class="sxs-lookup"><span data-stu-id="369fa-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="369fa-111">På sidan **Ny projektprislista** väljer du en prislista i listrutan.</span><span class="sxs-lookup"><span data-stu-id="369fa-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="369fa-112">Endast prislistor som har kontexten inställd på **försäljning** och vars valuta överensstämmer med kontovalutan.</span><span class="sxs-lookup"><span data-stu-id="369fa-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="369fa-113">Namnge associationen och välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="369fa-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="369fa-114">En kundspecifik projektprislista skapas.</span><span class="sxs-lookup"><span data-stu-id="369fa-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="369fa-115">Den här prislistan används som standard för projektkostnader i projektofferter eller kontrakt som skapats för den här kunden när offertens eller projektkontraktets slutdatum faller inom giltighetsdatum för prislistan.</span><span class="sxs-lookup"><span data-stu-id="369fa-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="369fa-116">Anpassad prissättning på projektofferter</span><span class="sxs-lookup"><span data-stu-id="369fa-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="369fa-117">På projektofferter kan du ange att projektprissättningen ska börja med en standard prislista som hämtas som standard från kunden eller från projektets parametrar.</span><span class="sxs-lookup"><span data-stu-id="369fa-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="369fa-118">När du behöver anpassa prissättningen av projekt som hör ihop med en viss offert kan du Visa den från den associerade entiteten projektprislistor.</span><span class="sxs-lookup"><span data-stu-id="369fa-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="369fa-119">Följ stegen nedan om du vill skapa ett specifikt offererat projektpris.</span><span class="sxs-lookup"><span data-stu-id="369fa-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="369fa-120">Öppna projektoffert, välj fliken **Projektprislistor**.</span><span class="sxs-lookup"><span data-stu-id="369fa-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="369fa-121">I underrutnätet väljer du **Skapa anpassad prissättning**.</span><span class="sxs-lookup"><span data-stu-id="369fa-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="369fa-122">Alla projektprislistor som är bifogade till offerten kopieras till nya prislistor.</span><span class="sxs-lookup"><span data-stu-id="369fa-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="369fa-123">Namnen på de nya prislistorna återspeglar namnet på offerten med en datum- och tidsstämpling för när prislistorna skapades.</span><span class="sxs-lookup"><span data-stu-id="369fa-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="369fa-124">Du kan använda var och en av dessa prislistor och göra uppdateringar av arbete (rollpris) och kostnader för utgift (kategoripris).</span><span class="sxs-lookup"><span data-stu-id="369fa-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="369fa-125">Dessa priser gäller endast för detta projektoffert.</span><span class="sxs-lookup"><span data-stu-id="369fa-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="369fa-126">Prislistor för projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="369fa-126">Price lists on a project contract</span></span>

<span data-ttu-id="369fa-127">I ett projektkontrakt är projektpriset alltid standard som en anpassad prislista med namnet på kontraktet och datum-tidsstämpeln som läggs till i namnet.</span><span class="sxs-lookup"><span data-stu-id="369fa-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="369fa-128">Detta gäller oavsett om kontraktet skapades när offerten vanns eller om kontraktet skapades från grunden.</span><span class="sxs-lookup"><span data-stu-id="369fa-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="369fa-129">Om det behövs kan du ta bort kopplingen till den anpassade prislistan och associera en standardprislista till projektkontraktet i stället.</span><span class="sxs-lookup"><span data-stu-id="369fa-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="369fa-130">När du associerar en standardprislista med projektprislistorna för en offert eller ett kontrakt påverkas alla eventuella ändringar av priserna i prislistan för alla offerter och kontrakt som använder prislistan.</span><span class="sxs-lookup"><span data-stu-id="369fa-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
