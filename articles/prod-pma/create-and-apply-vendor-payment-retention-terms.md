---
title: Skapa och tillämpa villkor för innehållen leverantörsbetalning
description: I det här ämnet finns information om hur du konfigurerar och upprätthåller villkor för innehållen leverantörsbetalning.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085677"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="28b92-103">Skapa och tillämpa villkor för innehållen leverantörsbetalning</span><span class="sxs-lookup"><span data-stu-id="28b92-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="28b92-104">Det är användbart att konfigurera villkor för innehållen leverantörsbetalning för ett projekt när organisationen vill hålla inne del av betalningen som ska göras till en leverantör.</span><span class="sxs-lookup"><span data-stu-id="28b92-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="28b92-105">T.ex. när du vill spärra betalning till en leverantör tills de produkter som levererats uppfyller dina förväntningar.</span><span class="sxs-lookup"><span data-stu-id="28b92-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="28b92-106">Villkor för innehållen leverantörsbetalning kan anges när du förhandlar ett leverantörskontrakt.</span><span class="sxs-lookup"><span data-stu-id="28b92-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="28b92-107">Skapa villkor för innehållen leverantörsbetalning</span><span class="sxs-lookup"><span data-stu-id="28b92-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="28b92-108">Du kan ange procentandelen av leverantörsbetalningen som ska hållas inne och procentandelen av de belopp som har hållits inne tidigare och som ska släppas.</span><span class="sxs-lookup"><span data-stu-id="28b92-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="28b92-109">Belopp hålls automatiskt inne på leverantörsfakturor tills kontraktet når det angivna slutsteget.</span><span class="sxs-lookup"><span data-stu-id="28b92-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="28b92-110">När du har konfigurerat villkoren för kvarhållande kan du tillämpa dem på vilket projekt som helst för den leverantören.</span><span class="sxs-lookup"><span data-stu-id="28b92-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="28b92-111">Följ stegen nedan om du vill konfigurera och upprätthålla villkor för innehållen leverantörsbetalning.</span><span class="sxs-lookup"><span data-stu-id="28b92-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="28b92-112">Gå till **Projekthantering och redovisning** > **Kvarhållning** > **Villkor för innehållen leverantörsbetalning**.</span><span class="sxs-lookup"><span data-stu-id="28b92-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="28b92-113">Välj **Ny** om du vill lägga till ett nytt villkor för kvarhållande för leverantören.</span><span class="sxs-lookup"><span data-stu-id="28b92-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="28b92-114">Värdet **Regel-ID** för det nya villkoret anges automatiskt.</span><span class="sxs-lookup"><span data-stu-id="28b92-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="28b92-115">Ange en kort beskrivning i fältet **Beskrivning** och på snabbfliken **Villkor** väljer du **Lägg till rad** för att ange villkorsvärden för följande:</span><span class="sxs-lookup"><span data-stu-id="28b92-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="28b92-116">**Procentandel av levererade enheter** : Ange en procentandel som slutförts av villkoret.</span><span class="sxs-lookup"><span data-stu-id="28b92-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="28b92-117">Belopp hålls automatiskt inne på leverantörsfakturor tills projektslutförandet är lika med den specificerade procentandelen.</span><span class="sxs-lookup"><span data-stu-id="28b92-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="28b92-118">Om du till exempel anger 50,00 kvarhålls beloppen tills projektet har slutförts till 50 procent.</span><span class="sxs-lookup"><span data-stu-id="28b92-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="28b92-119">**Procent att hålla inne** : Ange en procentandel av leverantörsfakturans belopp som ska hållas inne.</span><span class="sxs-lookup"><span data-stu-id="28b92-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="28b92-120">Om du till exempel anger 10,00 kvarhålls 10 procent av beloppet på en leverantörsfaktura tills projektet når slutförandeprocenten som angetts i fältet **Procentandel av levererande enheter**.</span><span class="sxs-lookup"><span data-stu-id="28b92-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="28b92-121">**Procentandel som ska släppas** : Välj **Lägg till rad** om du vill ange en procentandel av tidigare kvarhållna belopp som ska frisläppas för den valda slutförandenivån av projektet.</span><span class="sxs-lookup"><span data-stu-id="28b92-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="28b92-122">Om du har fler än en milstolpe för olika nivåer av projektslutförande anger du en separat rad för villkor för kvarhållande för varje kvarhållningsregel.</span><span class="sxs-lookup"><span data-stu-id="28b92-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="28b92-123">Varje rad kan ange en annan kvarhållandeprocentandel och en annan procentandel för varje angiven nivå av projektets slutförande.</span><span class="sxs-lookup"><span data-stu-id="28b92-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="28b92-124">När du har skapat villkor för kvarhållande för en leverantör kan du tillämpa villkoren på ett projekt.</span><span class="sxs-lookup"><span data-stu-id="28b92-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="28b92-125">Tillämpa villkor för leverantörskvarhållande på ett projekt</span><span class="sxs-lookup"><span data-stu-id="28b92-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="28b92-126">Gå till **Projekthantering och redovisning** > **Projekt** > **Alla projekt** och öppna ett projekt från projektets listsida.</span><span class="sxs-lookup"><span data-stu-id="28b92-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="28b92-127">Under snabbfliken **Leverantörsavtal** väljer du **Lägg till rad**.</span><span class="sxs-lookup"><span data-stu-id="28b92-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="28b92-128">I fältet **Kontokod** väljer du något av följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="28b92-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="28b92-129">**Tabell** : Villkoren för leverantörskvarhållande gäller för en enskild leverantör.</span><span class="sxs-lookup"><span data-stu-id="28b92-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="28b92-130">**Grupp** : Villkoren för leverantörskvarhållande gäller för alla leverantörer i en leverantörsgrupp.</span><span class="sxs-lookup"><span data-stu-id="28b92-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="28b92-131">**Alla** : Villkoren för leverantörskvarhållande gäller för alla leverantörer.</span><span class="sxs-lookup"><span data-stu-id="28b92-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="28b92-132">I fältet **Leverantör/leverantörsgrupp** väljer du den leverantör eller leverantörsgrupp som villkoren för leverantörskvarhållande gäller för.</span><span class="sxs-lookup"><span data-stu-id="28b92-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="28b92-133">Om du valde **Alla** i föregående steg är detta fält inte tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="28b92-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="28b92-134">I fältet **Villkor för leverantörskvarhållning** väljer du de kvarhållningsvillkor som du skapade i föregående procedur.</span><span class="sxs-lookup"><span data-stu-id="28b92-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="28b92-135">Om projektet även har ställts in för betala vid betalning (PWP) för leverantören anger du tröskelvärdet i procent för projektet i fältet **Tröskelvärdesprocent för PWP**.</span><span class="sxs-lookup"><span data-stu-id="28b92-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="28b92-136">Villkoren för leverantörskvarhållande visas även på inköpsorder som du skapar för leverantören.</span><span class="sxs-lookup"><span data-stu-id="28b92-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
