---
title: Tidsplan för utgifter för en förfrågan om federala beviljanden
description: I det här ämnet finns information om tidsplanen för utgifter för förfrågan om federala beviljanden.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288986"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0816c-103">Tidsplan för utgifter för en förfrågan om federala beviljanden</span><span class="sxs-lookup"><span data-stu-id="0816c-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0816c-104">Enligt Office of Management and Budget Circular A-133, organ som erhåller federala fonder underkastade granskningskrav, vilka även kallas enstaka revisioner.</span><span class="sxs-lookup"><span data-stu-id="0816c-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="0816c-105">Granskningsprocessen används för att rapportera om de federala stödens intäkter och utgifter på återkommande basis.</span><span class="sxs-lookup"><span data-stu-id="0816c-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="0816c-106">En del av rapporten för en enskild granskning inkluderar tidsplanen för utgifter för federala beviljanden (SEFA).</span><span class="sxs-lookup"><span data-stu-id="0816c-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="0816c-107">Tidsplanen för utgifter för en förfrågan om federala beviljanden innehåller titel och nummer i Catalog of Federal Domestic Assistance (CFDA), anslagsnummer, året för anslaget, namnet på det federala organ som tillhandahåller anslaget samt namnet på den direkta entiteten.</span><span class="sxs-lookup"><span data-stu-id="0816c-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="0816c-108">Förfrågan gäller en särskild period.</span><span class="sxs-lookup"><span data-stu-id="0816c-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="0816c-109">Den perioden är vanligtvis samma som bokslutsperioden, som är ett räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="0816c-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="0816c-110">Förfrågan innehåller anslag med projektionsdatum i det valda datumintervallet.</span><span class="sxs-lookup"><span data-stu-id="0816c-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="0816c-111">Kolumnen **Tilldelande organ** för förfrågan visar anslagets kund eller, när det gäller ett direkt anslag, det tilldelande organet.</span><span class="sxs-lookup"><span data-stu-id="0816c-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="0816c-112">För ett direkt anslag visar kolumnen **Direkt organ** anslagets kund.</span><span class="sxs-lookup"><span data-stu-id="0816c-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="0816c-113">Om anslaget inte är ett direkt anslag är kolumnen **Direkt organ** tom.</span><span class="sxs-lookup"><span data-stu-id="0816c-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="0816c-114">Konfigurera CFDA-kluster</span><span class="sxs-lookup"><span data-stu-id="0816c-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="0816c-115">Du måste konfigurera de CFDA-kluster som kan kopplas till CFDA-nummer i tidsplanen för utgifter för en förfrågan om federala beviljanden.</span><span class="sxs-lookup"><span data-stu-id="0816c-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="0816c-116">Gå till **Projektledning och redovisning \> Konfiguration \> Anslag \> Katalog med kluster av federalt inhemskt stöd**.</span><span class="sxs-lookup"><span data-stu-id="0816c-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="0816c-117">Välj **Nytt** för att skapa ett CFDA-kluster.</span><span class="sxs-lookup"><span data-stu-id="0816c-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="0816c-118">Ange klusternamnet.</span><span class="sxs-lookup"><span data-stu-id="0816c-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="0816c-119">Välj **Spara** för att spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="0816c-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="0816c-120">Ställ in CFDA-nummer</span><span class="sxs-lookup"><span data-stu-id="0816c-120">Set up CFDA numbers</span></span>

<span data-ttu-id="0816c-121">Du måste konfigurera de CFDA-nummer som kan läggas till i anslag och inkluderas i tidsplanen för utgifter för en förfrågan om federala beviljanden.</span><span class="sxs-lookup"><span data-stu-id="0816c-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="0816c-122">Gå till **Projektledning och redovisning \> Konfiguration \> Anslag \> Katalog med nummer för federalt inhemskt stöd**.</span><span class="sxs-lookup"><span data-stu-id="0816c-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="0816c-123">Välj **Nytt** för att skapa ett CFDA-nummer.</span><span class="sxs-lookup"><span data-stu-id="0816c-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="0816c-124">I kolumnen **Nummer** anger du CFDA-numret.</span><span class="sxs-lookup"><span data-stu-id="0816c-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="0816c-125">Tryck på tangenten **TAB**.</span><span class="sxs-lookup"><span data-stu-id="0816c-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="0816c-126">I kolumnen **Beskrivning** anger du CFDA-titeln.</span><span class="sxs-lookup"><span data-stu-id="0816c-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="0816c-127">Tryck på tangenten **TAB**.</span><span class="sxs-lookup"><span data-stu-id="0816c-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="0816c-128">Valfritt: I fältet **Programkluster** lägger du till lämpligt CFDA-kluster.</span><span class="sxs-lookup"><span data-stu-id="0816c-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="0816c-129">Välj **Spara** för att spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="0816c-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0816c-130">Ställ in anslag som ska rapporteras för tidsplanen för utgifter för en förfrågan om federala beviljanden</span><span class="sxs-lookup"><span data-stu-id="0816c-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="0816c-131">Gå till **Projektledning och redovisning \> Anslag \> Anslag** och välj ett befintligt anslag.</span><span class="sxs-lookup"><span data-stu-id="0816c-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="0816c-132">Under snabbfliken **Konfiguration**, i fältet **Katalog med federalt inhemskt stöd**, tilldelar du CFDA-numret.</span><span class="sxs-lookup"><span data-stu-id="0816c-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="0816c-133">CFDA-numret för anslaget avgör CFDA-klustret för rapportering.</span><span class="sxs-lookup"><span data-stu-id="0816c-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="0816c-134">Under snabbfliken **Kontaktinformation** anger du information om tilldelaren genom att följa dessa steg:</span><span class="sxs-lookup"><span data-stu-id="0816c-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="0816c-135">I fältet **Anslagets kund** anger du den kund som är ansvarig för anslaget.</span><span class="sxs-lookup"><span data-stu-id="0816c-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="0816c-136">För ett befintligt anslag kan den här informationen redan finnas.</span><span class="sxs-lookup"><span data-stu-id="0816c-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="0816c-137">Ange om anslagskunden är finansiären.</span><span class="sxs-lookup"><span data-stu-id="0816c-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="0816c-138">Om anslagskunden är finansiären lämnar du kryssrutan **Direkt** omarkerad.</span><span class="sxs-lookup"><span data-stu-id="0816c-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="0816c-139">Om en annan kund är finansiär och anslagskunden ansvarar för utgifterna och spårning av pengarna, markerar du kryssrutan **Direkt**.</span><span class="sxs-lookup"><span data-stu-id="0816c-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="0816c-140">Om du markerade kryssrutan **Direkt** i föregående steg anger du, i fältet **Tilldelande organ**, den kund som tillhandahöll anslaget.</span><span class="sxs-lookup"><span data-stu-id="0816c-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="0816c-141">Det tilldelande organet och anslagskunden kan inte vara samma kund.</span><span class="sxs-lookup"><span data-stu-id="0816c-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="0816c-142">Här är ett exempel på ett direkt anslag:</span><span class="sxs-lookup"><span data-stu-id="0816c-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="0816c-143">Den federala regeringen finansierade ett infrastrukturprojekt för en delstat.</span><span class="sxs-lookup"><span data-stu-id="0816c-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="0816c-144">Den federala regeringen gav delstaten pengar att spendera.</span><span class="sxs-lookup"><span data-stu-id="0816c-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="0816c-145">I det här fallet är den federala regeringen det tilldelande organet och delstaten är anslagskunden.</span><span class="sxs-lookup"><span data-stu-id="0816c-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="0816c-146">När du först aktiverar funktionen anges de första CFDA-numren med hjälp av de befintliga numren på anslagen.</span><span class="sxs-lookup"><span data-stu-id="0816c-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="0816c-147">Exkludera anslag från SEFA-rapportering utifrån anslagstypen</span><span class="sxs-lookup"><span data-stu-id="0816c-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="0816c-148">Gå till **Projektledning och redovisning \> Konfiguration \> Anslag \> Anslagstyper**.</span><span class="sxs-lookup"><span data-stu-id="0816c-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="0816c-149">Under snabbfliken **Standardinformation** markerar du kryssrutan **Exkludera från tidsplan för utgifter för federala beviljanden**.</span><span class="sxs-lookup"><span data-stu-id="0816c-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="0816c-150">Välj **Spara** för att spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="0816c-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="0816c-151">Kör Tidsplan för utgifter för en förfrågan om federala beviljanden</span><span class="sxs-lookup"><span data-stu-id="0816c-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="0816c-152">Gå till **Projektledning och redovisning \> Förfrågningar och rapporter \> Anslagsförfrågan \> Tidsplan för utgifter för federala beviljanden**.</span><span class="sxs-lookup"><span data-stu-id="0816c-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="0816c-153">I avsnittet **Parametrar** följer du dessa steg:</span><span class="sxs-lookup"><span data-stu-id="0816c-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="0816c-154">I fältet **Datumintervall** väljer du koden för datumintervallet.</span><span class="sxs-lookup"><span data-stu-id="0816c-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="0816c-155">Du kan också definiera datumintervallet i fälten **Från datum** och **Till datum**.</span><span class="sxs-lookup"><span data-stu-id="0816c-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="0816c-156">Valfritt: Om du endast vill ta med fakturerade transaktioner som intäkt i förfrågan ställer du in alternativet **Inkludera endast fakturerade intäkter** på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0816c-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="0816c-157">Kolumner</span><span class="sxs-lookup"><span data-stu-id="0816c-157">Columns</span></span>

<span data-ttu-id="0816c-158">I tidsplanen för utgifter för en förfrågan om federala beviljanden finns följande kolumner:</span><span class="sxs-lookup"><span data-stu-id="0816c-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="0816c-159">Katalog med namn på kluster av federalt inhemskt stöd</span><span class="sxs-lookup"><span data-stu-id="0816c-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="0816c-160">Tilldelande organ</span><span class="sxs-lookup"><span data-stu-id="0816c-160">Grantor agency</span></span>
- <span data-ttu-id="0816c-161">Direkt organ</span><span class="sxs-lookup"><span data-stu-id="0816c-161">Pass-through agency</span></span>
- <span data-ttu-id="0816c-162">Namn på anslag</span><span class="sxs-lookup"><span data-stu-id="0816c-162">Grant name</span></span>
- <span data-ttu-id="0816c-163">Anslags-ID</span><span class="sxs-lookup"><span data-stu-id="0816c-163">Grant ID</span></span>
- <span data-ttu-id="0816c-164">ID för anslagsansökan</span><span class="sxs-lookup"><span data-stu-id="0816c-164">Grant application ID</span></span>
- <span data-ttu-id="0816c-165">Katalog med federalt inhemskt stöd</span><span class="sxs-lookup"><span data-stu-id="0816c-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="0816c-166">Kvitton</span><span class="sxs-lookup"><span data-stu-id="0816c-166">Receipts</span></span>
- <span data-ttu-id="0816c-167">Utgifter</span><span class="sxs-lookup"><span data-stu-id="0816c-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]