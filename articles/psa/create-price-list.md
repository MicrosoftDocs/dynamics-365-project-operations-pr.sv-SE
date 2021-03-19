---
title: Skapa en prislista
description: Skapa en prislista i Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290337"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="9b0e8-103">Skapa en prislista (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9b0e8-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9b0e8-104">Prislistor innehåller en mall som dina kontoansvariga kan använda för att skapa offerter och projekt, och för fastställande av utgifterna för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="9b0e8-105">De ger en radartikellista över roller och utgifter och det pris som du tar betalt för varje.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="9b0e8-106">Du kan skapa flera prislistor så att du kan ha separata prisstrukturer för olika regioner som du säljer produkterna i eller för olika försäljningskanaler.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="9b0e8-107">Det är en god idé att skapa minst en prislista för varje valuta som du vill fakturera dina kunder i.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="9b0e8-108">Om du vill skapa ekonomiska uppskattningar för arbetet som ska levereras, kontrollera att varje projekt har en bakomliggande utgifts- och prislista.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="9b0e8-109">Skapa en standardkostnad och försäljningsprislista som gäller alla projekt skapade inom din organisation.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="9b0e8-110">Prislistor är beroende av roller och utgiftskategorier, så innan du skapar en prislista kontrollerar du att du redan har konfigurerat rollerna och utgiftskategorierna som du vill använda när du skapar prislistan.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="9b0e8-111">Gå till **Project Service > Prislistor**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="9b0e8-112">Klicka på **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="9b0e8-113">I **Kontext** väljer du om prislistan gäller **Kostnad**, **Köp** eller **Försäljning**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="9b0e8-114">Ange ett namn på prislistan i **Namn**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="9b0e8-115">I **Valuta** väljer du den valuta som du ska använda för fakturering eller utgiftsredovisning.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="9b0e8-116">I **Tidsenhet** anger du tidsperioden som priset gäller, till exempel dag eller timme.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="9b0e8-117">Fyll i **Startdatum**, **Slutdatum** och **Beskrivning** efter behov.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="9b0e8-118">Klicka på **Spara** för att skapa posten så att du kan fortsätta redigera den.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="9b0e8-119">Om du vill lägga till ett pris för rollen i prislistan, klickar du på **+** under **Rollpriser**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="9b0e8-120">I fönstret **Priser för roll** fyller du i uppgifterna och klickar sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9b0e8-121">Fortsätt att lägga till priser för roll efter behov.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="9b0e8-122">Klicka på **Spara** i skärmens nedre högra hörn när du är klar.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="9b0e8-123">Om du vill lägga till ett pris för utgiftskategori prislistan klickar du på **+** under **kategoripriser**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="9b0e8-124">I fönstret **Pris för transaktionskategori** fyller du i uppgifterna och klickar sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9b0e8-125">Fortsätt att lägga till priser för kategori efter behov.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="9b0e8-126">Klicka på **Spara** i skärmens nedre högra hörn när du är klar.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="9b0e8-127">Om du vill lägga till prislisteposter till prislistan klickar du på **+** under **Prislisteposter**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="9b0e8-128">I fönstret **Prislisteposter** fyller du i uppgifterna och klickar sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9b0e8-129">Fortsätt att lägga till prislisteposter efter behov.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="9b0e8-130">Klicka på **Spara** i skärmens nedre högra hörn när du är klar.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="9b0e8-131">Om du vill lägga till områdesrelationer i prislistan klickar du på **+** under **Områdesrelationer**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="9b0e8-132">I fönstret **Ny anslutning** fyller du i uppgifterna och klickar sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9b0e8-133">Fortsätt lägga till områdesrelationer om det behövs.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="9b0e8-134">Klicka på **Spara** i skärmens nedre högra hörn när du är klar.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9b0e8-135">Se även</span><span class="sxs-lookup"><span data-stu-id="9b0e8-135">See Also</span></span>  
 [<span data-ttu-id="9b0e8-136">Konfigurera Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9b0e8-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]