---
title: Projektanslag
description: I det här ämnet beskrivs hur du skapar eller ändrar ett anslag.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289391"
---
# <a name="project-grants"></a><span data-ttu-id="75e61-103">Projektanslag</span><span class="sxs-lookup"><span data-stu-id="75e61-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75e61-104">Ett anslag är ett penningbidrag för ett visst syfte eller projekt.</span><span class="sxs-lookup"><span data-stu-id="75e61-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="75e61-105">Det finns vanligtvis begränsningar för hur ett anslag kan spenderas.</span><span class="sxs-lookup"><span data-stu-id="75e61-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="75e61-106">I Projektledning och redovisning kan du ange och spåra anslag samt definiera relationer till projekt och projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="75e61-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="75e61-107">Till exempel kan du utföra följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="75e61-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="75e61-108">Associera anslag med projekt och finansieringskällor via länkar till sidorna **Projekt** och **Projektkontraktsinformation**.</span><span class="sxs-lookup"><span data-stu-id="75e61-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="75e61-109">Ange och spåra ändringar av ett anslag när det flyttas från en status till en annan.</span><span class="sxs-lookup"><span data-stu-id="75e61-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="75e61-110">Ange och spåra kostnader, begärda belopp och tilldelade belopp.</span><span class="sxs-lookup"><span data-stu-id="75e61-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="75e61-111">Skapa huvudanslag och associera delanslag med dem.</span><span class="sxs-lookup"><span data-stu-id="75e61-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="75e61-112">Du kan skapa ett anslag genom att ange alla detaljer i en ny post, eller så kan du kopiera informationen från ett befintligt anslag och sedan uppdatera dem.</span><span class="sxs-lookup"><span data-stu-id="75e61-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="75e61-113">Skapa ett nytt anslag</span><span class="sxs-lookup"><span data-stu-id="75e61-113">Create a new grant</span></span>

1. <span data-ttu-id="75e61-114">Gå till **Projektledning och redovisning** \> **Anslag** \> **Anslag**.</span><span class="sxs-lookup"><span data-stu-id="75e61-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="75e61-115">Välj **Nytt** \> **Anslag**.</span><span class="sxs-lookup"><span data-stu-id="75e61-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="75e61-116">På sidan med anslagsinformation, under snabbfliken **Allmänt**, i fältet **Anslags-ID**, ange en alfanumerisk identifierare för anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="75e61-117">I fältet **Anslagsnamn** anger du ett namn på anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="75e61-118">I fälet **Beskrivning** lägger du till information om det nya anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="75e61-119">De flesta andra fält på sidan är valfria och du kan ange så lite eller så mycket information som du vill.</span><span class="sxs-lookup"><span data-stu-id="75e61-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="75e61-120">I följande lista beskrivs den information som anges på varje snabbflik på sidan med information om anslaget:</span><span class="sxs-lookup"><span data-stu-id="75e61-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="75e61-121">**Allmänt** – Ange anslagets namn, status, beskrivning, syfte och belopp.</span><span class="sxs-lookup"><span data-stu-id="75e61-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="75e61-122">**Kontaktinformation** – Ange detaljer om personalmedlemmar, avdelningen som hanterar anslaget och anslagets kund eller organisationen som beviljar anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="75e61-123">Du kan också ange om organisationen är en direkt enhet som tar emot anslaget och sedan vidarebefordrar det till en annan mottagare.</span><span class="sxs-lookup"><span data-stu-id="75e61-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="75e61-124">Välj **Lägg till** om du vill lägga till kontaktinformation, t.ex. telefonnummer och e-postadresser till organisationen som tillhandahåller anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="75e61-125">**Datum och deadlines** – Ange datum som är relaterade till anslaget och anslagsansökan.</span><span class="sxs-lookup"><span data-stu-id="75e61-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="75e61-126">Exempel: förfallodatum för ansökan, inlämningsdatum och datum då anslaget godkändes eller avvisas.</span><span class="sxs-lookup"><span data-stu-id="75e61-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="75e61-127">**Associerade projekt och projektkontrakt** – Du kan bara ange information på den här snabbfliken om fältet **Anslagets status** under snabbfliken **Allmänt** är inställd på **Aktivt** eller **Tilldelat**.</span><span class="sxs-lookup"><span data-stu-id="75e61-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="75e61-128">Välj bland följande alternativ för att slutföra den relaterade uppgiften:</span><span class="sxs-lookup"><span data-stu-id="75e61-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="75e61-129">**Lägg till finansieringskälla** – Lägg till en ny finansieringskälla för anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="75e61-130">Du kan ange all information nu eller också kan du använda standardinformationen och sedan uppdatera den senare.</span><span class="sxs-lookup"><span data-stu-id="75e61-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="75e61-131">**Lägg till projektkontrakt** – Lägg till eller uppdatera information om projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="75e61-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="75e61-132">**Lägg till projekt** – Lägg till eller uppdatera projektinformation.</span><span class="sxs-lookup"><span data-stu-id="75e61-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="75e61-133">**Inställningar** – Ange information om matchningsmedel, om det behövs.</span><span class="sxs-lookup"><span data-stu-id="75e61-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="75e61-134">Många organisationer som tilldelar anslag kräver att mottagaren lägger ned en specifik summa eller resurser för att matcha det belopp som tilldelas i anslaget.</span><span class="sxs-lookup"><span data-stu-id="75e61-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="75e61-135">I fältet **Lokalt projekt eller spårnings-ID** kan du ange en identifierare som skiljer sig från projektets identifierare.</span><span class="sxs-lookup"><span data-stu-id="75e61-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="75e61-136">Om en del av anslaget tilldelas en annan organisation ställer du in alternativet **Undertilldelare** på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="75e61-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="75e61-137">För anslag som tilldelas i USA kan du ange om ett anslag ska tilldelas enligt ett statligt medgivande eller ett federalt medgivande.</span><span class="sxs-lookup"><span data-stu-id="75e61-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="75e61-138">**Information om utnyttjande** – Lägg till eller uppdatera information om hur ofta anslag kan utnyttjas, debiteras eller spenderas.</span><span class="sxs-lookup"><span data-stu-id="75e61-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="75e61-139">Skapa ett nytt anslag från en kopia</span><span class="sxs-lookup"><span data-stu-id="75e61-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="75e61-140">Gå till **Projektledning och redovisning** \> **Anslag** \> **Anslag**.</span><span class="sxs-lookup"><span data-stu-id="75e61-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="75e61-141">Välj **Nytt** \> **Kopiera från anslag**.</span><span class="sxs-lookup"><span data-stu-id="75e61-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="75e61-142">Ange en alfanumerisk identifierare och ett namn för det nya anslaget och klicka sedan på **OK**.</span><span class="sxs-lookup"><span data-stu-id="75e61-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="75e61-143">På sidan med anslagsinformation granskar du detaljerna för det kopierade anslaget och gör de ändringar som behövs.</span><span class="sxs-lookup"><span data-stu-id="75e61-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="75e61-144">De flesta fälten på sidan är valfria.</span><span class="sxs-lookup"><span data-stu-id="75e61-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="75e61-145">Visa eller ändra anslagsinformation</span><span class="sxs-lookup"><span data-stu-id="75e61-145">View or modify grant details</span></span>

1. <span data-ttu-id="75e61-146">Gå till **Projektledning och redovisning** \> **Anslag** \> **Anslag**.</span><span class="sxs-lookup"><span data-stu-id="75e61-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="75e61-147">Välj det anslag som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="75e61-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="75e61-148">I åtgärdsfönstret under fliken **Anslag** i gruppen **Upprätthåll** väljer du **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="75e61-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="75e61-149">Granska anslagsinformationen och gör de ändringar som behövs.</span><span class="sxs-lookup"><span data-stu-id="75e61-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]